# LEMP Kurulumu

## Ubuntu Kurulumu

Eğer DigitalOcean gibi bir yerden server aldığımızı düşünürsek zaten otomatik olarak kurulum yapılmış oluyor.

### Güncelleme

	root@server#apt update
	root@server#apt dist-upgrade

### Kullanıcı Ekleme

	root@server#adduser kullaniciadi
	root@server#mkdir /home/kullaniciadi/.shh
	root@server#usermod -a -G sudo kullaniciadi
	root@server#chown -R kullaniciadi:kullaniciadi /home/kullaniciadi/.ssh

## Fail2ban kurulumu

	sudo apt install fail2ban
	sudo vi /etc/fail2ban/jail.d/defaults-debian.conf

	[DEFAULT]
	bantime = -1
	findtime = 1w
	maxtry = 1

	sudo service fail2ban restart
	sudo fail2ban-client status sshd


