Nama  : Anita (312310244)

# LatihanWeb2
# Langkah 1: Membuat Dokumen HTML
Langkah pertama adalah membuat struktur dasar HTML pada index.html seperti berikut:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
        <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    <nav>
        <a href="lab2_css_dasar.html">CSS Dasar</a>
        <a href="lab2_css_eksternal.html">CSS Eksternal</a>
        <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <div id="intro">
        <h1>Hello World</h1>
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah Pemrograman Web.</p>
        <a class="button btn-primary" href="#intro">Informasi selengkapnya</a>
    </div>
</body>
</html>

![Screenshot (150)](https://github.com/user-attachments/assets/333d325c-0e79-41f4-9d98-d0ea4d196275)
ini menunjukkan tampilan dasar halaman HTML sebelum ditambahkan gaya CSS yang diterapkan.

# Langkah 2: Menambahkan CSS Internal
Selanjutnya tambahkan CSS internal di dalam tag <head>:

  <style>
    body {
        font-family: 'Open Sans', sans-serif;
    }
    header {
        min-height: 80px;
        border-bottom: 1px solid #77CCEF;
    }
    h1 {
        font-size: 24px;
        color: #0F189F;
        text-align: center;
    }
    h1 i {
        color: #6d6a6b;
    }
</style>

![Screenshot (151)](https://github.com/user-attachments/assets/f1d35df8-5d27-411f-b52b-698a43e06d03)
Tangkapan layar ini menunjukkan perubahan tampilan setelah CSS internal dan inline diterapkan, seperti perubahan warna teks dan tata letak.
# Langkah 3: Menambahkan CSS Inline
CSS inline diterapkan langsung di elemen <p>:

<p style="text-align: center; color: #ccd8e4;">Teks ini diatur menggunakan CSS inline.</p>

![Screenshot (152)](https://github.com/user-attachments/assets/fe34e2e7-11f6-4ea2-b8ba-8522cef9d969)
Di tangkapan layar ini, file CSS eksternal telah diterapkan, sehingga gaya pada navigasi dan elemen lainnya menjadi lebih terstruktur.

# Langkah 4: Menambahkan CSS Eksternal
Buat file eksternal ( assets/css/style.css) dan hubungkan ke dokumen HTML:

<link rel="stylesheet" href="assets/css/style.css" type="text/css">
Isi dari assets/css/style.css:

nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}

nav a:hover {
    background: #0B6B3A;
}

![Screenshot (154)](https://github.com/user-attachments/assets/89463305-452e-43f4-b831-c658ff0adc0d)
Ini adalah hasil akhir setelah semua jenis CSS (internal, inline, dan eksternal) diterapkan, termasuk penggunaan selector ID, class, dan elemen.

# Langkah 5: Menggunakan Selector CSS
Gunakan selector CSS seperti ID dan class:

#intro {
    background: #418fb1;
    padding: 10px;
}

.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
}

.btn-primary {
    background: #E42A42;
}
![Screenshot (155)](https://github.com/user-attachments/assets/983e125f-26d2-4cc4-a3c2-652384099f66)
Ini adalah hasil akhir setelah semua jenis CSS (internal, inline, dan eksternal) diterapkan, termasuk penggunaan selector ID, class, dan elemen.

# Pertanyaan
1. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
  Perbedaan antara pendeklarasian CSS h1 {...} dan #intro h1 {...} terletak pada spesifikasi selektor yang digunakan untuk menentukan elemen mana yang akan dipengaruhi oleh aturan CSS tersebut.
- Selektor h1:
> Mengacu pada semua elemen <h1> di dalam dokumen HTML.
> Aturan ini akan diterapkan ke setiap elemen <h1> tanpa memandang konteks atau posisi elemen tersebut di dalam struktur HTML.
-Selektor #intro h1:
> Merupakan selektor yang lebih spesifik, mengacu pada elemen <h1> yang berada di dalam elemen dengan ID intro.
> Ini berarti hanya <h1> yang merupakan anak (atau keturunan) dari elemen dengan ID intro yang akan terpengaruh oleh aturan CSS tersebut.

2.Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS padaelemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
  Ketika ada deklarasi CSS secara internal, eksternal, dan inline pada elemen yang sama, inline CSS memiliki prioritas tertinggi dan akan ditampilkan di browser.
> inline CSS:
Diterapkan langsung pada elemen HTML menggunakan atribut style. Contoh:
<h1 style="color: red;">Judul</h1>
Dalam contoh ini, teks "Judul" akan berwarna merah karena inline CSS diterapkan langsung pada elemen <h1>.
> Internal CSS:
Didefinisikan dalam tag <style> di dalam bagian <head> dari dokumen HTML.Contoh:
<head>
  <style>
    h1 {
      color: blue;
    }
  </style>
</head>
Dengan internal CSS ini, semua elemen <h1> di halaman tersebut akan berwarna biru, kecuali jika ada aturan lain yang lebih spesifik.
> External CSS:
Didefinisikan dalam file terpisah yang dihubungkan ke dokumen HTML menggunakan tag <link>. Contoh:
<link rel="stylesheet" type="text/css" href="styles.css">
3. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
  Ketika sebuah elemen HTML memiliki ID dan class, dan masing-masing memiliki deklarasi CSS, maka declaration ID akan memiliki prioritas lebih tinggi dibandingkan dengan declaration class. Ini berarti bahwa jika ada konflik antara gaya yang ditentukan oleh ID dan class, gaya dari ID yang akan diterapkan pada elemen tersebut di browser.
  Spesifisitas adalah cara browser menentukan aturan CSS mana yang harus diterapkan ketika ada beberapa aturan yang dapat berlaku untuk elemen yang sama. Berikut adalah urutan spesifisitas dari yang tertinggi ke terendah:
- Inline styles (prioritas tertinggi)
- ID selectors (bernilai 100)
- Class selectors (bernilai 10)
- Type selectors (bernilai 1)
Contoh Kasus

<!DOCTYPE html>
<html>
<head>
    <style>
        #paragraf-1 {
            color: blue; /* Gaya untuk ID */
        }
        .text-paragraf {
            color: green; /* Gaya untuk class */
        }
    </style>
</head>
<body>
    <p id="paragraf-1" class="text-paragraf">Ini adalah paragraf.</p>
</body>
</html>

Elemen <p> memiliki ID paragraf-1 dan class text-paragraf.
CSS mendeklarasikan warna teks untuk ID sebagai biru dan untuk class sebagai hijau.
Karena ID selector (#paragraf-1) memiliki spesifisitas lebih tinggi daripada class selector (.text-paragraf), maka warna teks yang ditampilkan di browser akan berwarna biru.

