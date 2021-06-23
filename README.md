# tugas10_backupdanrestore
# Nama : Nunuk Panca Wulan
# Kelas : TI.19.B2
# Nim : 311910260
# TUGAS Backup dan Restore Menggunakan Perintah SQL
# 1. BUKA CMD MASUK MYSQL USE DATABASE YANG MAU DI BACKUP
![image](https://user-images.githubusercontent.com/81863210/123095760-9cee3700-d458-11eb-8ecc-304f791c90eb.png)
# 2. LIAT TABEL DAN LAKUKAN PROSES PENGUNCIAN TABLE
![image](https://user-images.githubusercontent.com/81863210/123096128-fa828380-d458-11eb-8574-8d50a6795a7b.png)
# 3. LAKUKAN PROSES BACKUP TABLE DENGAN PERINTAH : SELECT * INTO OUTFILE 'b_pelanggan' from pelanggan;
![image](https://user-images.githubusercontent.com/81863210/123096382-3ddcf200-d459-11eb-930b-67314a123d04.png)
# 4. JIKA PROSES BACKUP BERHASIL MAKA AKAN MUNCUL FILE BACKUP PADA DIREKTORI
# C: xampp/mysql/data/nunuk_panca_wulan_311910260
![image](https://user-images.githubusercontent.com/81863210/123096861-b93ea380-d459-11eb-98c1-40f16c9941b2.png)
# 5. DELETE TABLE PELANGGAN
![image](https://user-images.githubusercontent.com/81863210/123097415-54d01400-d45a-11eb-8c4e-8275dfdc6fed.png)
# 6. DATA YANG TELAH DI BACKUP DAPAT DIKEMBALIKAN KAPAN SAJA BILA DIPERLUKAN . SINTAKS SQL YANG DIGUNAKAN ADALAH
# LOAD DATA INFILE. PERINTAH YANG DIJALANKAN ADALAH LOAD DATA INFILE 'b_pelanggan' into table pelanggan;
![image](https://user-images.githubusercontent.com/81863210/123098445-5bab5680-d45b-11eb-966d-6cd9d4f773a2.png)
# TUGAS Backup DAN RESTORE MENGGUNAKAN MySQLDump
# 1.Menuju ke folder aplikasi mysqldump di xamp/mysql/bin
# Jalankan shell atau commad prompt dan ketikkan perintah berikut untuk memulai dump database : mysqldump -u root -p wilianto_311910184 > backup2.sql
![image](https://user-images.githubusercontent.com/81863210/123101365-2ce2af80-d45e-11eb-9407-93e55612b201.png)
# 2. Jika proses backup berhasil maka akan muncul file backup pada direktori
# C:\xampp\mysql\bin
![image](https://user-images.githubusercontent.com/81863210/123101611-7206e180-d45e-11eb-9465-3997a27c6bc7.png)
# 3. Data yang telah dibackup dapat di restrore kembali ke dalam database dengan perintah : mysqldump -u root -p wilianto_311910184 < C:\xampp\mysql\bin\backup2.sql
![image](https://user-images.githubusercontent.com/81863210/123104368-1558f600-d461-11eb-86d6-0ab0b5529291.png)
# Tulisakan script cron job untuk melakukan backupotomatis setiap hari minggu jam 12 malam !
# 0 0 * * 7 mysqldump -u root -p nunuk_panca_wulan_311910260 > backup2.sql
