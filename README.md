# PRAKTIKUM 4 - Pemrograman WEB
```
Mochamad Amri Adrian Wiratama
311910226
TI.19.A2
Universitas Pelita Bangsa
```
# Langkah 1
<i>Membuat dokumen HTML. Setelah itu buat struktur dasar HTML</i>
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Box Element</title>
</head>
<body>
  <header>
    <h1>Box Element</h1>
  </header>
</body>
</html>
```
![Langkah 1](https://user-images.githubusercontent.com/56380838/115408916-78d56600-a21b-11eb-8fc6-339125f8f493.png)

# Langkah 2
<i>Membuat box element dengan tag div</i>
```
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
</section>
```
![Langkah 2](https://user-images.githubusercontent.com/56380838/115408923-7bd05680-a21b-11eb-9cb9-fa2573b5acd6.png)

# Langkah 3
<i>Tambahkan deklarasi CSS pada head untuk membuat float elemen</i>
```
<style>
        div {
            float:left;
            padding: 10px;
        }
        .div1 {
            background: red;
        }
        .div2 {
            background: yellow;
        }
        .div3 {
            background: green;
        }
        .div4 {
            background-color: blue;
            clear: left;
            float: none;
        }
</style>
```

![Langkah 3](https://user-images.githubusercontent.com/56380838/115408936-7f63dd80-a21b-11eb-8599-d56413056268.png)

# Langkah 4
<i>Mengatur Clearfix Element. Clearfix digunakan untuk mengatur element setelah float element</i>
* Tambahkan element div lainnya seteleah div3
```
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
  <div class="div4">Div 4</div>
</section>
```
* Kemudian atur property clear pada CSS
```
.div4 {
  background-color: blue;
  clear: left;
  float: none;
}
```
![Langkah 4](https://user-images.githubusercontent.com/56380838/115408948-825ece00-a21b-11eb-8eda-4439a876bcbe.png)

# Membuat Layout Sederhana
## Langkah 1
```
Buat folder baru dengan nama lab4_layout, kemudian buat file baru didalamnya dengan nama `home.html`, dan file css dengan nama `style.css`. 
```
* Kemudian kodingan di file `home.html`
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="hero"></section>
        <section id="wrapper">
            <section id="main"></section>
            <aside id="sidebar"></aside>
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
* Dan kemudian kodingan di file `style.css`.
```
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}
body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
}
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```
![Langkah 5 1](https://user-images.githubusercontent.com/56380838/115410032-7e7f7b80-a21c-11eb-8222-1a80e8977991.png)

* Dan dibuka d browser nya, maka tampilan nya akan seperti ini,

![Langkah 5 2](https://user-images.githubusercontent.com/56380838/115410065-863f2000-a21c-11eb-87f6-3ae398607199.png)
## Langkah 2
Membuat Navogasi pada CSS
```
/* navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}
nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
```
![Langkah 6](https://user-images.githubusercontent.com/56380838/115411647-d965a280-a21d-11eb-8ae8-4e2c98877a2c.png)

## Langkah 3
### Membuat Hero Panel
Membuat hero panel dengan menambahkan kode berikut pada HTML dan CSS.
* Codingan tambahan pada `home.html`
```
<section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
* Tambahan Codingan pada file `style.css`
```
/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}
#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}
#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}
```
![Langkah 7 1](https://user-images.githubusercontent.com/56380838/115413035-0e262980-a21f-11eb-8f3e-84acdd8f4e39.png)
#### Hasilnya
![Langkah 7 2](https://user-images.githubusercontent.com/56380838/115413057-12524700-a21f-11eb-9a2e-7b33aee95a36.png)
## Langkah 4 
### Mengatur Layout Main dan Sidebar
```
/* main content */
#wrapper {
    margin: 0;
}
#main {
    float: left;
    width: 640px;
    padding: 20px;
}

/* sidebar area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
```
![Langkah 8](https://user-images.githubusercontent.com/56380838/115413097-1a11eb80-a21f-11eb-80c7-13eb2b48ff36.png)
### Membuat Sidebar Widget
Mengatur main content dan sidebar dengan property `float`.
* Tambahan Coding pada file `home.html.`
```
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
       </ul>
    </div>
    <div class="widget-box">
       <h3 class="title">Widget Text</h3>
       <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
pharetra est nunc, nec pretium nunc pretium ac.</p>
   </div>
</aside>
```
* Tambahan Codingan pada file `style.css`
```
/* widget */
.widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
}
.widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
}
.widget-box ul {
    list-style-type:none;
}
.widget-box li {
    border-bottom:1px solid #eee;
}
.widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
}
.widget-box li:hover a {
    background-color:#eee;
}
.widget-box p {
    padding:15px;
    line-height:25px;
}
```
![Langkah 9 1](https://user-images.githubusercontent.com/56380838/115414087-f3a08000-a21f-11eb-8eae-3067889011f1.png)
#### Hasilnya
![Langkah 9 2](https://user-images.githubusercontent.com/56380838/115414108-f7340700-a21f-11eb-80c3-9354064a4009.png)
## Langkah 5
### Mengatur Tampilan Footer
* Untuk mengatur footer, tambahkan kode CSS sebagai berikut.
```
/* footer */
footer {
    clear:both;
    background-color:#1d1d1d;
    padding:20px;
    color:#eee;
}
```
![Langkah 10](https://user-images.githubusercontent.com/56380838/115414123-fa2ef780-a21f-11eb-8c62-4fb54502ac99.png)
## Langkah 6
### Menambahkan Element lain pada Main Content
* Tambahkan Coding pada File `home.html`
```
<section id="main">
    <div class="row">
        <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
    </div>
</section>
```
* Kemudian Tambahkan juga pada file `style.css`
```
/* box */
.box {
    display:block;
    float:left;
    width:33.333333%;
    box-sizing:border-box;
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
    padding:0 10px;
    text-align:center;
}
.box h3 {
    margin: 15px 0;
}
.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}
box img {
    border: 0;
    vertical-align: middle;
}
.image-circle {
    border-radius: 50%;
}
.row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
    content:'';
    display:table;
}
.row:after,
.entry:after {
    clear:both;
}
```
![Langkah 11 1](https://user-images.githubusercontent.com/56380838/115415188-e46e0200-a220-11eb-8906-420821402e32.png)
#### HASILNYA
![Langkah 11 2](https://user-images.githubusercontent.com/56380838/115415201-e6d05c00-a220-11eb-8c42-f0a4cd44b814.png)

## Langkah 7
### Menambah Content Artikel
* Untuk membuat content artikel, tambahkan kode berikut pada `section main`.
```
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
class="right-img">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
</article>
```
* Dan ini Codingan untuk file `style.css`.
```
.divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
}
/* entry */
   .entry {
    margin: 15px 0;
}
   .entry h2 {
    margin-bottom: 20px;
}
.entry p {
    line-height: 25px;
}
.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}
.entry .right-img {
    float: right;
}
```
![Langkah 12](https://user-images.githubusercontent.com/56380838/115415224-ecc63d00-a220-11eb-954a-cfbd02ebd752.png)
#### HASILNYA
![Langkah 12 1](https://user-images.githubusercontent.com/56380838/115415217-e9cb4c80-a220-11eb-8d4a-c93ab12af896.png)

# PERTANYAAN & TUGAS !
## 1. Tambahkan Layout untuk menu About
### buat single layout yang berisi deskripsi, portofolio, dll.
## 2. Tambahkan Layout untuk menu Contact
### yang berisi form isian: Nama, Email, Message, dll.
# 1. Tambahkan Layout untuk menu About
## Membuat dokumen html dengan nama `about.html` sebagai berikut.
![Pertanyaan1](https://user-images.githubusercontent.com/56380838/115421837-88a67780-a226-11eb-80c4-c87f36ea0c35.png)
## Lalu di CSS nya
![Pertanyaan1 4](https://user-images.githubusercontent.com/56380838/115422390-0e2a2780-a227-11eb-8ff8-b13e666bc4ad.png)
## Hasil nya saat menekan menu About akan seperti ini tampilan nya
![Pertanyaan1 2](https://user-images.githubusercontent.com/56380838/115421848-8b08d180-a226-11eb-8e52-2e097627a48b.png)
# 2. Tambahkan Layout untuk menu Contact
## Buat file HTML baru dengan nama kontak.html, dan buat form yang berisi: `nama`, `email`, `message`, dll
![Pertanyaan 2 1](https://user-images.githubusercontent.com/56380838/115423880-631a6d80-a228-11eb-8af5-6fec35b4239d.png)
## Lalu menambahkan CSS nya
![Pertanyaan 2 2](https://user-images.githubusercontent.com/56380838/115423900-657cc780-a228-11eb-9d15-0f218fd223af.png)
## Hasil nya setelah saya menekan menu Kontak, maka akan tampil seperti dibawah ini
![Pertanyaan 2 3](https://user-images.githubusercontent.com/56380838/115423919-6877b800-a228-11eb-8cee-034d2c57a767.png)
