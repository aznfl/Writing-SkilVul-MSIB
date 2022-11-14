# **Writing Test Week 2-Back End Bootcamp**
## **Sequelize**
___
> **Sequelize** ialah ORM (Object Relational Mapping) Node JS yang berbasis promise. Dan fitur fitur yang ada di Sequelize dapat mengelola dan mengatur data di database dengan cepat, dan efisien.

**Salah Satu Cara Setting Database dengan Sequelize**
```javascript
const Sequelize = require('sequelize');

const sequelize = new Sequelize ('mongodb://localhost:27017/test-mongo')
```

## **MongoDB**
___
> **MongoDB** adalah database berbasis relasional dan salah satu database open source NoSQL yang cukup populer digunakan.

- MongoDB dapat dijalankan menggunakan shell dan GUI.
- GUI Tools Official dari MongoDB yaitu [MongoDB Compass](https://www.mongodb.com/products/compass)
- Batas maksimal ukuran document pada MongoDB adalah 16MB.
- Konsep penyimpanan MongoDB semi struktural atau tidak struktural, dan tidak harus memiliki relasi layaknya tabel-tabel MySQL.
- **Keuntungan** menggunakan MongoDB yaitu model data spesifik dan memiliki skema fleksibel dalam mengembangkan aplikasi modern.

**3 Komponen Database MongoDB**
- *Database* ialah tempat untuk menyimpan berbagai macam Collection.
- *Collection* ialah tempat kumpulan dari berbagai macam document.
- *Document* ialah data-data yang di simpan di dalam collection.

**MongoDB memiliki 2 Schema Desaign, yaitu :**
- *Embedding* yaitu menyematkan data secara langsung atau dalam satu desain.
- *Referencing* yaitu menyematkan data secara terpisah dan mengisialisasikan dengan menggunakan key data tersebut.

## **Mongoose**
___
> **Mongoose** adalah library yang bisa dibilang sebagai Object Modelling MongoDB untuk NodeJS.

- Cara menginstal Mongoose
    ```javascript
    npm install mongoose
    ```
- Cara membuat koneksi ke database
    ```javascript
    const mongoose = require('mongoose');

    const DB_URL = 'mongodb://localhost:27017/test-mongo'

    const db = mongoose.connect(DB_URL)

        db.
    then(() => {
    console.log("database terkoneksi")
    })
    .catch((err) => {
    console.log(err)
    })
    ```
- Cara pembuatan schema mongoose
    ```javascript
    const mongoose = require('mongoose')
    const { Schema } = mongoose

    const userSchema = new Schema({
        name: String,
        email: {
            type: String,
            required: true
        },
        password: String,
    })

    const User = mongoose.model("User", userSchema)
    ```
- **Berikut salah satu contoh penggunaan CRUD dengan mongoose :**
    ```javascript
    //Pencarian salah satu data Tugas
    getTugasByID: async(req, res) => {
        try {
        const data = req.body

        const users = await Tugas.findOne({id: data.name})
    
        res.status(201).json({
            message: "data has been created!!",
            data: users
        })
        
        } catch (error) {
        res.status(500).json({
            message: "data not created!!"
        })
        }
    },
    ```
- Berikut Documentasi lengkap untuk penggunaan [CRUD Operations](https://www.mongodb.com/docs/v6.0/crud/)

## **Docker**
___
> **Docker** ialah software yang menjalankan suatu aplikasi menggunakan container.

- *Docker* bisa menjalankan lebih dari 1 container secara bersamaan
- *Docker* dibuat menggunakan bahasa pemrograman Javascript. Dan mulai dikenalkan pada tahun 2013.
- Fungsi Docker yaitu sebagai penyedia layanan virtual bagi aplikasi yg diinstall pada sebuah host. 
- *Docker* men-sharing kernel dari host OS, serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja.
- *Docker* akan menyediakan hal-hal yang diperlukan untuk aplikasi mulai dari akses file, koneksi internet, hingga port agar aplikasi dapat berjalan dengan mulus

- *Container* adalah tumpukan dari layer image.

- Berikut adalah Docker Component :
    - Client
    - Host
    - Registry

- Perintah untuk menginstal suatu image dari Docker Hub ke dalam local system
```
$ docker pull <image_name>
```

- Perintah untuk menjalankan suatu container pada Docker
```
$ docker run <container_id>
```

- Perintah untuk menghapus docker container
```
$ docker kill MyContainer
```

-  Perintah untuk push suatu image ke dalam Docker Registry
```
$ docker push myorg/img
```

- Perintah untuk melihat seluruh list container yang sedang berjalan
```
$ docker ps
```