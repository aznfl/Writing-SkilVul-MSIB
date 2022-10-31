# **Writing Test Week 1-Back End Bootcamp**
## **Web Server & RESTful API**
___

### **Web Server**
> **Web Server** ialah Software yang menerima request & memberikan response terhadap HTTP atau HTTPS.

> **Fungsi dari Web Server** ialah untuk melakukan atau mentransfer berkas permintaan pengguna melalui protokol komunikasi yang telah ditentukan sedemikian rupa. Halaman web yang diminta terdiri dari berkas teks, video, gambar, file dan banyak lagi.

Berikut beberapa contoh aplikasi dari web server :
1. NGINX
2. Apache
3. MS Server

### **RESTful API**
> **REST (Representational State Transfer)** ialah salah satu tipe arsitektur software yang mewakili serangkaian batasan yang harus diikuti saat Anda mengembangkan aplikasi di internet.
> **RESTful API** ialah suatu REST yang mampu memenuhi ketentuan dan batasan yang ditetapkan oleh gaya arsitektur REST itu sendiri.

- RESTful API mengirim dan menerima data dalam bentuk JSON
- REST API dapat membatasi beberapa sumber daya berdasarkan tingkat authorized access
- Blueprint sebuah RESTful API dinamakan dengan API Specification


HTTP Method yang biasa digunakan :
- `GET` A GET request -> meminta untuk menerima salinan sumber daya
- `POST` A POST request -> mengirimkan data ke server untuk membuat sumber daya baru
- `DELETE` A DELETE request -> mengikirimkan untuk menghapus sumber daya
- `PUT` A PUT request -> mengirimkan data ke server untuk mengubah sumber daya yang ada
- `PATCH` (Partial)

> Contoh **EndPoint** dari method GET `api/product/{id}` ialah untuk menampilkan product dari id tersebut
- Penulisan sebuah EndPoint jika memiliki nama yang panjang bisa menggunakan `kebab-case`

Status Code yang muncul ketika transfer data :
- `2xx` -> success
- `3xx` -> redirect
- `4xx` -> client error
- `5xx` -> server error

Aplikasi yang biasa digunakan untuk mengecek sebuah API :
- Postman
- Insomnia.api
- Thunder Client (Extensi VS Code )

## **Intro Node.Js**
___

> **Node.Js** adalah runtime environment lintas platform single-thread yang dibangun berdasarkan engine JavaScript V8 Chrome. Singkatnya, Node.js adalah sebuah runtime untuk JavaScript

- Node.Js beroperasi dalam satu thread (single-threaded), yaitu tidak membuat thread baru untuk setiap permintaan. Thread adalah rangkaian instruksi yang perlu dilakukan oleh server.
- Node.js menggunakan operasi I/O non-blocking, dimana saat client mengirim permintaan ke web server, event loop single-threaded Node JS akan mengambil permintaan tersebut lalu mengirimkannya ke worker thread untuk diproses. 
- Node.Js tidak memblokir thread dan membuang-buang resource CPU dengan menunggu respons, Node JS akan terus mengerjakan tugas berikutnya. Maka, Node.js bisa menangani sejumlah besar permintaan secara bersamaan.

Berikut beberepa engine yang digunakan untuk menjalankan baris kode JavaScript Node.js :
- Chakra
- Spider Monkey
- V8

> Dengan Node.Js kita bisa membuat aplikasi Web Apps, Mobile Apps, dan Backend Apps.

> **NPM (Node Package Manager)** adalah package dan dependency manager utama pada NodeJS
Berikut code penginstalannya :
```
npm install --save name_package
npm install --save-dev name_package
npm install --global name_package
```

Berikut beberapa Module Built-in yang bisa langsung di pakai :
```javascript
require("path")
require("fs")
require("http")
require("assert")
```

Contoh Penggunaan :
```javascript
const http = require('http');

http.createServer(function(req, res) {
    res.writeHead(200, {'Content-Type': 'text/html'});
    res.write('Hello World');
    res.end();
}).listen(8080);