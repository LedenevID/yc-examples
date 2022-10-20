yc compute instance create \
	--name nameinstance \
	--hostname nameinstance.ru \
	--preemptible=true \
	--zone ru-central1-b \
	--network-interface subnet-name=default-ru-central1-b,nat-ip-version=ipv4 \
	--create-boot-disk type=network-ssd,size=20GB,image-folder-id=standard-images,image-family=ubuntu-2204-lts,auto-delete=yes \
	--metadata serial-port-enable=1 \
	--ssh-key ~/.ssh/id_rsa.pub
