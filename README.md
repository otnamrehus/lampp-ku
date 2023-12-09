# Lampp-Ku
Lampp (PHP7.4-Apache, MySQL5.6 dam PHPMyAdmin) Versi PC

Persiapan
1. Web Server
   - Port: 7000 -> 80 [ mengarah ke port 80 ]
   - Port: 7022 -> 22 [ mengarah ke port 22 - ssh ]
2. MySQL Server / Login PHPMyAdmin
   - Root Username/Pass [ root/password ]
   - User Username/Pass [ mysql/password ]
3. SSH Server
   - User Username/Pass [ root/1 ]
4. apt update && apt -y install nano git     ## Persiapkan paket git
5. mkdir -p ~/docker/     ##  Siapkan direktori baru

INSTALASI
1. git clone https://github.com/otnamrehus/lampp-ku.git    ## Download docker-compose
2. docker-composer -p 'lamppku' -d --build  ## Jalankan perintah docker dengan docker-compose
3. docker-composer -p 'lamppku' stop   ## hentikan container
4. docker-composer -p 'lamppku' start  ## jalankan container 
5. docker-composer -p 'lamppku' down  ## hentikan sekaligus hapus container
6. Opsional Step [Jika menggunakan VPN]:
   
   zerotier-cli join 565799d8f6bdd3c d  ## Koneksi ke VPN  (Tambahan service [zerotier-one] sebagai Tunneling , karena telah terinstall sebelumnya)


JALANKAN 
1. http://localhost:7000   ##  Web Server (Via Browser)   
2. http://localhost:7007   ##  PHPMyAdmin (Via Browser)   
3. sudo ssh -p 7022 root@ip_address   ### Nginx Server [SSH]  (Via Terminal)
4. sudo sftp -P 7022 root@ip_address  ### Nginx Server [SFTP]  (Via Terminal)
6. sudo ssh -p 7023 root@ip_address   ### MySQL Server [SSH]  (Via Terminal)
7. sudo sftp -P 7023 root@ip_address  ### MySQL Server [SFTP]  (Via Terminal)

MENU SERVER
apt update -y &&
apt install git &&
git clone https://github.com/otnamrehus/lampp-haproxy.git &&
cd lampp-haproxy &&
chmod +x server.sh &&
./server.sh
