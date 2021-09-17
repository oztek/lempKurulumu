# LEMP Kurulumu

## Ubuntu Kurulumu

Eğer DigitalOcean gibi bir yerden server aldığımızı düşünürsek zaten otomatik olarak kurulum yapılmış oluyor.

### Güncelleme

	root@server#apt update
	root@server#apt dist-upgrade

### Kullanıcı Ekleme

	root@server#adduser kullaniciadi
	root@server#mkdir /home/kullaniciadi/.shh
	root@server#chown -R kullaniciadi:kullaniciadi /home/kullaniciadi/.ssh
