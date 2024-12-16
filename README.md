# Konfigurasi Server Platform Belanja Online


## 1. Perbarui Sistem Operasi
> sudo apt update && sudo apt upgrade -y


## 2. Apache Web Server
- `Sudo Apt Update`

- `sudo apt install apache2 -y`

- Konfigurasi Direktori Web :
  + Direktori utama : /var/www/html/
  + Ubah izin :
    * `sudo chown -R www-data:www-data /var/www/html`
    * `sudo chmod -R 755 /var/www/html`

- Tes Server : Akses melalui browser: http://IP-Server


## 3. MySQL Database
- `sudo apt install mysql-server -y`
- Konfigurasi Database WordPress :
  + `sudo mysql`
 
  + `CREATE DATABASE wordpress;`

    `CREATE USER 'salvado_user'@'%' IDENTIFIED BY 'Slvd.Ags_160825';`

    `GRANT ALL PRIVILEGES ON wordpress.* TO 'salvado_user'@'%';`

    `FLUSH PRIVILEGES;`

  + `SHOW DATABASES;`


## 4. PHP
- `sudo apt install php libapache2-mod-php php-mysql php-cli php-curl php-zip php-gd -y`
- Tes PHP:
  + Buat file: /var/www/html/info.php.
    <?php
    phpinfo();
    ?>
- Akses: http://IP-Server/info.php


## 5. FTP (vsftpd)
- `sudo apt install vsftpd -y`
  + Edit file konfigurasi:
    `sudo nano /etc/vsftpd.conf`
  + Pastikan parameter berikut aktif:
    `anonymous_enable=NO`
    `local_enable=YES`
    `write_enable=YES`
  + Restart
    `sudo systemctl restart vsftpd`




