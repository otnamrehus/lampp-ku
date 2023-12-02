# Lampp-Ku [PC]
Lampp (PHP7.4-Apache, MySQL5.6 dam PHPMyAdmin) Versi PC
Persiapan
1. Web Server
   - Port: 7070 -> 80 [ mengarah ke port 80 ]
   - Port: 7022 -> 22 [ mengarah ke port 22 - ssh ]
2. MySQL Server / Login PHPMyAdmin
   - Root Username/Pass [ root/password ]
   - User Username/Pass [ mysql/password ]
3. SSH Server
   User Username/Pass [ root/1 ]
4. Persiapkan paket git
   apt update && apt -y install nano git
5. Siapkan direktori baru
   mkdir -p ~/docker/

Instalasi
1. Download docker-compose
   git clone https://github.com/otnamrehus/lampp-ku.git
2. Jalankan perintah docker dengan docker-compose
   docker-composer -p 'lamppku' -d --build 
3. Hentikan dan jalankan docker-compose [container-container/service]
   docker-composer -p 'lamppku' stop   # hentikan container
   docker-composer -p 'lamppku' start  # jalankan container 
5. Hentikan dan jalankan docker-compose
   docker-composer -p 'lamppku' down # hentikan sekaligus hapus container
6. Tambahan service [zerotier-one] sebagai Tunneling , karena telah terinstall sebelumnya
   zerotier-cli join 565799d8f6bdd3c d   # Koneksi ke VPN

Running
1. Web Server (Via Browser)
   http://localhost:7070
2. PHPMyAdmin (Via Browser)
   http://localhost:7171
3. Remote Server [SSH](Via Terminal)
   sudo ssh -p 7022 root@ip_address
4. Remote Server [SFTP] (Via Terminal)
   sudo sftp -P 7022 root@ip_address
