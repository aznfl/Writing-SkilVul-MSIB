# **Writing Test Week 2-Back End Bootcamp**
## **Database**
___

> **Database** adalah tempat untuk menyimpan data/koleksi yang terstruktur, dimana didalamnya terdapat informasi-informasi atau data-data yang bersifat elektronik.

- Cara mengakses database biasanya menggunakan aplikasi yang bernama **DBMS (Database Management System)**
- Database yang akan digunakan dan dipelajari yaitu berbasis **SQL (Structured Query Language)**

Ada berbagai macam aplikasi untuk membuat database berbasis SQL, yaitu :
- MySql
- MariaDB
- PostgreSql
- Oracle

Beberapa istilah di database :
- **Table** adalah kumpulan value yang dibangun oleh baris dan kolom, yang didalamnya berisikan atribut dari sebuah data.
- **Field/Attribute** adalah kolom dari sebuah tabel dimana masing-masing field memiliki tipe data masing-masing.
- **Record** merupakan kumpulan nilai yang saling terkait. Record merupakan isi dari sebuah tabel.


## **MySql**
___

> **MySql** ialah DBMS yang *Open Source* dan kompatible untuk banyak platform.

- Port yang biasa digunakan di Mysql yaitu `3306`

- Saat menggunakan MySql yang dibutuhkan adalah Mysql Server, bisa menggunakan salah satu di bawah ini :
    1. CLI
    2. Workbench
    3. DBeaver
    4. TablePlus
    5. Phpmyadmin

Cara mengakses database Mysql menggunakan CLI :
```
mysql -u root -p // lalu masukkan password
mysql -u root // jika tidak menggunakan password
```

Cara menampilkan list database :
```
show databases;
```

Cara mengakses salah satu dari list database :
```
use nama_database;
```

**Berikut beberapa Data Type di SQL :**
- Number
    - `int` -> Tipe data untuk angka bulat
    - `float` -> Tipe data untuk angka menggunakan koma
    - `decimal` -> Tipe data angka pecahan (desimal), dimana jumlah angka pecahan (angka di belakang koma) sudah di tentukan dari awal.

- String
    - `char` -> Tipe data string dengan fixed length dan memori sesuai panjang yang didefinisikan
    - `varchar` -> Tipe data string dengan penyimpanan karakter yang fleksibel max 255
    - `text` -> Tipe data string dengan penyimpanan yang lebih panjang dari varchar 
    - `enum` -> Tipe data yang khusus untuk kolom dimana nilai datanya sudah kita tentukan sebelumnya. 

- Date Time
    - `date` -> Tipe data untuk menyimpan tanggal ('CCYY-MM-DD')
    - `datetime` -> Tipe data untuk menyimpan tanggal dan waktu ('CCYY-MM-DD hh:mm:ss')
    - `time` -> Tipe data untuk menyimpan waktu (‘hh:mm:ss’)
    - `timestamp` -> Time data untuk menyimpan tanggal dan waktu dan juga UTC nya atau timezone (CCYY-MM-DD hh:mm:ss +00:00')
- `boolean` -> Tipe ini hanya menyimpan 2 tipe data yaitu TRUE dan FALSE, dan dapat di convert menjadi int dengan representasi TRUE = 1, dan FALSE = 0
- `DEFAULT` -> Tipe data untuk set default value jika tidak di assign dengan value
- `NULL` -> Tipe data kosong atau tipe data yang belum di assign dengan value / data

**Beberapa perintah dasar di SQL :**
- DDL (Data Definition Language) -> bermain di *table*
- DML (Data Manipulation Language) -> bermain di *data*
- DCL (Data Control Language)

**1. DDL (Data Definition Language)**
- `CREATE` -> Command untuk membuat sebuah database dan table
- `ALTER` -> Command untuk mengubah struktur dari tabel yang dipilih, seperti menambahkan atau menghapus kolom/field, membuat atau menghapus primary key, mengubah jenis kolom/field yang ada, dan mengubah kolom atau nama tabel
- `DROP` -> Command untuk menghapus Database, Table, dan View atau Index
- 

