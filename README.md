# Konfigurasi Server Platform Belanja Online


## 1. Perbarui Sistem Operasi
> sudo apt update && sudo apt upgrade -y


## 2. Apache Web Server
- `Sudo Apt Update`

- `sudo apt install apache2 -y`

- Konfigurasi Direktori Web :
  + Direktori utama : /var/www/html/
  + Ubah izin :
    * sudo chown -R www-data:www-data /var/www/html
    * sudo chmod -R 755 /var/www/html

- Tes Server : Akses melalui browser: http://<IP-Server>
## 3. 

