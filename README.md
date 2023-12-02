# Lampp-Ku [PC]
Lampp (PHP7.4-Apache, MySQL5.6 dam PHPMyAdmin) Versi PC <br><br><br>
<b>Persiapan</b>
1. &nbsp; Web Server <br>
&nbsp; - Port: 7070 -> 80 [ mengarah ke port 80 ] <br>
&nbsp; - Port: 7022 -> 22 [ mengarah ke port 22 - ssh ] <br>
2. &nbsp; MySQL Server / Login PHPMyAdmin <br>
&nbsp; - Root Username/Pass [ root/password ] <br>
&nbsp; - User Username/Pass [ mysql/password ] <br>
3. &nbsp; SSH Server<br>
&nbsp; User Username/Pass [ root/1 ] <br>
4. &nbsp; Persiapkan paket git <br>
&nbsp; apt update && apt -y install nano git <br>
5. &nbsp; Siapkan direktori baru <br> 
&nbsp;  mkdir -p ~/docker/ <br><br><br>

<b>Instalasi</b>
1. &nbsp; Download docker-compose <br>
&nbsp; git clone https://github.com/otnamrehus/lampp-ku.git <br>
2. &nbsp; Jalankan perintah docker dengan docker-compose <br>
&nbsp; docker-composer -p 'lamppku' -d --build 
3. &nbsp; Hentikan dan jalankan docker-compose [container-container/service] <br>
&nbsp; docker-composer -p 'lamppku' stop   &nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; # hentikan container<br>
&nbsp; docker-composer -p 'lamppku' start  &nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; # jalankan container <br>
4. &nbsp; Hentikan dan jalankan docker-compose <br>
&nbsp; docker-composer -p 'lamppku' down   &nbsp;&nbsp;&nbsp; &nbsp;&nbsp;# hentikan sekaligus hapus container<br>
5. &nbsp; Tambahan service [zerotier-one] sebagai Tunneling , karena telah terinstall sebelumnya  <br>
&nbsp; zerotier-cli join 565799d8f6bdd3c d   &nbsp;&nbsp;&nbsp; &nbsp;&nbsp;# Koneksi ke VPN <br><br><br>

<b>Running</b>
1. &nbsp;Web Server <i>(Via Browser)</i> <br>
&nbsp; http://localhost:7070 <br>
2. &nbsp;PHPMyAdmin <i>(Via Browser)</i><br>
&nbsp; http://localhost:7171 <br>
3. &nbsp;SSH <i>(Via Terminal)</i><br>
&nbsp;sudo ssh -p 7022 root@ip_address <br>
