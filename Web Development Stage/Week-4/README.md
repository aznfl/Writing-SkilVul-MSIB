# **Writing Test Week 4**

# **JAVASCRIPT INTERMEDIATE**

## **Asynchronoous Async Await**
> **Async Await** merupakan sebuah syntax khusus yang digunakan untuk menangani Promise agar penulisan code lebih efisien dan rapih. Fitur ini hadir sejak ES2017 dan fitur ini mempermudah kita dalam menangani proses asynchronous. 

> **Kegunaan :**
> - `async` -> mengubah function menjadi asynchronous
> - `await` -> menunda eksekusi hingga proses asynchronous selesai, await juga bisa digunakan berkali-kali di dalam function.

Contoh : 
```javascript
    const getData = async (a = API_List) => {
    const respons = await fetch(a);
    const result = await respons.json();
    const data = await result.results;
    };
```

## **Git dan Github Lanjutan**
Git dan Github bisa kita gunakan untuk kolaborasi saat mengerjakan sebuah project dengan rekan tim kita.

Fitur yang digunakan ialah **Branch**

- Untuk menghindari konflik saat mengerjakan, tidak boleh mengerjakannya dalam satu branch, kita harus membuat beberapa branch sesuai dengan tugas masing-masing.

Berikut beberapa perintah yang digunakan :
**1. Membuat sebuah branch baru**
```
git branch fitur_register
```

**2. Melihat list branch**
```
git branch
```

**3. Berpindah ke branch tertentu**
```
git checkout fitur_register
```

**4. Menghapus branch**
```
git branch -d fitur_register
```

**5. Untuk menggabungkan beberapa branch yang telah kita buat**

Pertama : pindah ke master
```
git checkout master
```

Kedua : lakukan merge
```
git merge halaman_login
```

## **Responsive Web Design (RWD)**
> **Responsive Web Design (RWD)** adalah bertujuan membuat desain website kita dapat di akses dalam device apapun

> **Breakpoint** ialah perubahan yang terjadi pada tampilan saat berganti device atau ukuran width

**1. Menambahkan Viewport di dalam tag head di Html**
```html
<meta name="viewport" content="width=device-width, inital-scale=1.0">
```

**2. Menambahkan style max-width di tag element**
```html
<img style="max-width: 100%;" src="image/me.png" alt="image">
```

**3. Menggunakan Media Query**
- Memisahkan file css untuk masing-masing device
```html
<!-- untuk device laptop -->
<link rel="stylesheet" href="styles/main.css">

<!-- untuk device mobile -->
<link rel="stylesheet" media="screen and (max-width: 500px) href="styles/main.mobile.css>
```
- Menggunakan 1 file css untuk berbagai device
```html
<!-- HTML -->
<link rel="stylesheet" href="styles/main.css">
```
```css
/* CSS */
body {
    background-color: white;
}

@media screen and (max-width: 500px){
    body {
        background-color: grey;
    }
}
```

**4. Menggunakan Range Media Query Min and Max**
```css
body {
    background-color: white;
}

/* Styling ini akan dijalankan jika width pada device lebih atau sama dengan 500px dan maksimum 700px */
/* Styling ini tidak akan dijalankan jika width lebih dari 700px */
@media screen and (min-width: 500px) and (max-width: 700px){
    body {
        background-color: grey;
    }
}
```

## **Bootstrap 5**
> **Bootstrap** adalah framework HTML, CSS, dan JavaScript yang berfungsi untuk mendesain website responsive dengan cepat dan mudah. 

- Framework open source ini diciptakan pada tahun 2011 oleh Mark Otto dan Jacob Thornton dari Twitter. Itulah kenapa dulunya Bootstrap dinamakan Twitter Blueprint. 

- Dengan bootstrap bisa memudahkan kita untuk membuat sebuah tampilan website yang baik dan juga sudah responsive

- Kita bisa memakai tools yang di sudah disediakan bootstrap

- Kita bisa melihat tools tersebut di website `https://getbootstrap.com/`


