#Device Information
Armbian 5.90 - Debian Buster
STB B860H Pulpstone Rooted
Sandisk 16 GB Class 10 Micro SD

#Software Information
Pi-hole V.5
Pi-hole-FTL V.5
Web Based Configuration V.5

#Document Writed On
11/05/2020 | 23:17

#Topic Information
Pi-hole-Universal Ad Blocker

#Document Version
version 1.0

#A.Pengenalan
Pi-hole merupakan sebuah aplikasi yang dapat dijalankan pada linux atau docker
Fungsi utama Pi-hole adalah untuk memblokir iklan yang ada pada internetimana akan meningkatkan kinerja jaringan dalam mengakses sebuah website.

#B.Fungsi
1. DNS Blacklist
2. DNS Whitelist
3. Local DNS
4. DNS Query monitoring

#C.Cara Kerja Pi-hole
Sebelum mengetahui cara kerja Pi-hole kita harus memahami terlebih dahulu apa itu DNS Server ?
DNS (Domain Name System) server adalah server yang dapat melayani permintaan dari client untuk mengetahui alamat yang digunakan oleh sebuah domain.
Sumber: https://idwebhost.com/blog/pengertian-dan-fungsi-dns-server/

Jadi sederhananya adalah sebuah DNS server merupakan sebuah buku kontak yang menyimpan nomor telepon seseorang,
Contoh Budi ingin menelepon Sinta tetapi dia tidak tahu berapa nomor telepon sinta
maka budi akan mencari nomor telepon sinta di buku kontak.

Coba bayangkan lebih mudah mengingat IP 182.180.23.xx atau website.com ? nah itulah pemahaman singkat dari sebuah DNS

Oke, lanjut ke bagaimana cara kerja Pi-hole. ketika kita mengakses sebuah website DNS server akan memberitahu domain yang harus kita kunjungi untuk mengakses situs tersebut, termasuk domain penyedia layanan iklan pada website
Nah, disini Pi-hole mulai beraksi dengan cara memblokir Domain dan Drop trafik untuk menampilkan resource dari penyedia iklan, yang hasilnya ketika pengguna mengakses suatu website dia tidak dapat melihat iklan yang seharusnya ada, karena sudah di blokir oleh Pi-hole tadi.

#D.Keuntungan Menggunakan Pi-hole
1. Menghemat Kuota/FUP Internet.
2. Mempercepat Akses suatu website.
3. Mencegah iklan pop-up.
4. Mencegah iklan yang berbahaya.
5. Mampu memblokir situs website berbahaya.

#E.Kerugian Menggunakan Pi-hole
1. Pemilik website tidak mendapatkan monetize dari penyedia iklan.
2. Ketika mengakses website baru, memerlukan sedikit waktu untuk akses (Domain Check Pi-hole).
3. Pengguna tidak dapat mengakses suatu website yang diblokir oleh Pi-hole, kecuali menggunakan Proxy Server Atau VPN.

#F.Cara Install Pi-hole
1. login root terminal
2. lakukan update repository dan upgrade

	apt update -y
	apt upgrade -y

3. install Pi-hole terbaru
	
	curl -sSL https://install.pi-hole.net | bash


Source:	https://github.com/pi-hole/pi-hole
Pi-Hole Document: https://docs.pi-hole.net/