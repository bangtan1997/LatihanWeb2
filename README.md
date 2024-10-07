Nama  : Anita (312310244)

# LatihanWeb2
# Langkah 1: Membuat Dokumen HTML
Langkah pertama adalah membuat struktur dasar HTML pada index.html seperti berikut
![Screenshot (150)](https://github.com/user-attachments/assets/333d325c-0e79-41f4-9d98-d0ea4d196275)
ini menunjukkan tampilan dasar halaman HTML sebelum ditambahkan gaya CSS yang diterapkan.
# Langkah 2: Menambahkan CSS Internal
Selanjutnya tambahkan CSS internal di dalam tag <head>:
![Screenshot (151)](https://github.com/user-attachments/assets/f1d35df8-5d27-411f-b52b-698a43e06d03)
Tangkapan layar ini menunjukkan perubahan tampilan setelah CSS internal dan inline diterapkan, seperti perubahan warna teks dan tata letak.
# Langkah 3: Menambahkan CSS Inline
CSS inline diterapkan langsung di elemen <p>:
![Screenshot (152)](https://github.com/user-attachments/assets/fe34e2e7-11f6-4ea2-b8ba-8522cef9d969)
Di tangkapan layar ini, file CSS eksternal telah diterapkan, sehingga gaya pada navigasi dan elemen lainnya menjadi lebih terstruktur.
# Langkah 4: Menambahkan CSS Eksternal
Buat file eksternal ( assets/css/style.css) dan hubungkan ke dokumen HTML:
![Screenshot (154)](https://github.com/user-attachments/assets/89463305-452e-43f4-b831-c658ff0adc0d)
Ini adalah hasil akhir setelah semua jenis CSS (internal, inline, dan eksternal) diterapkan, termasuk penggunaan selector ID, class, dan elemen.
# Langkah 5: Menggunakan Selector CSS
Gunakan selector CSS seperti ID dan class:
![Screenshot (155)](https://github.com/user-attachments/assets/983e125f-26d2-4cc4-a3c2-652384099f66)
Ini adalah hasil akhir setelah semua jenis CSS (internal, inline, dan eksternal) diterapkan, termasuk penggunaan selector ID, class, dan elemen.
# Pertanyaan
1. Perbedaan Elemen Pemilih ( h1 {...}) vs. ID Pemilih ( #intro h1 {...}):
h1 {...}: Ini adalah selector tag. Deklarasi ini akan mengaplikasikan aturan CSS ke semua elemen h1 yang ada di halaman HTML.
#intro h1 {...}: Ini adalah selector gabungan yang lebih spesifik. Deklarasi ini hanya akan mengaplikasikan aturan CSS ke elemen h1 yang ada di dalam elemen dengan ID intro.

2. Urutan Prioritas CSS Internal, Eksternal, dan Inline:
Ketika sebuah elemen memiliki CSS yang dideklarasikan secara internal, eksternal, dan inline untuk elemen yang sama, CSS inline memiliki prioritas tertinggi. Ini karena aturan spesifisitas CSS, di mana inline lebih spesifik dibandingkan deklarasi internal dan eksternal.

Urutan prioritas:
Inline CSS (paling spesifik)
Internal CSS (jika berada di dalam tag <style> di halaman yang sama)
Eksternal CSS (dideklarasikan di file CSS terpisah)

3.ID Pemilih Prioritas dan Kelas:
Jika elemen HTML memiliki ID dan class sekaligus, dan masing-masing selector terdapat deklarasi CSS, maka prioritasnya bergantung pada spesifisitas. Selector ID lebih spesifik dibandingkan class, sehingga deklarasi CSS pada ID akan mengesampingkan deklarasi pada class.
