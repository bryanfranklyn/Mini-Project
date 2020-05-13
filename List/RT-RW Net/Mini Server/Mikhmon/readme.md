#Document Writed On
12/05/2020 | 17:06

#Topic Information
Mini Server - Mikhmon

#Document Version
version 1.0

#Software Information
*Armbian 5.90 Debian 10 Buster
*Apache2 Web Server
*PHP 7
*Mikhmon V3

#Minimum Requirement
Router Board.

1.Router Board MikroTik Level 4.
2.Clock speed CPU 650 MHz
3.Router OS v6.3x.x
4.Webserver.

PC, SBC.
Bisa menjalankan webserver Apache/NGINX + PHP (v5.4.x /up).

#A.Update Repository 

apt-get update --allow-releaseinfo-change

#B.Install Apache2

apt-get install apache2

#C.Install PHP

apt-get install apache2

#D.Download & Install Mikhmon

wget https://codeload.github.com/laksa19/mikhmonv3/zip/master
unzip mikhmonv3-master

cp -f -r mikhmonv3-master /var/www/html/mikhmon

chmod 755 /var/www/html

systemctl apache2 reload

#E.Setting mikhmon

*Buka Browser
*Ketik htpp://alamat_ip/mikhmon

##login mikhmon
username: admin
password: 1234

##koneksi mikhmon dan router
_Pastikan API mikrotik sudah aktif_
IP>service>enable API port 8728
