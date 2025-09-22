# **Penjelasan Desain**
Proyek ini adalah implementasi ulang (replika) sederhana dari halaman profil Instagram menggunakan Tailwind CSS. Desainnya berfokus pada pendekatan mobile-first, memastikan tata letak dan elemen-elemennya terlihat baik di perangkat seluler sebelum dioptimalkan untuk layar yang lebih besar seperti tablet dan desktop. Tujuannya adalah untuk mendemonstrasikan kemampuan Tailwind dalam membangun antarmuka pengguna yang responsif dengan cepat, hanya menggunakan utility classes.

# **Pertanyaan README!**
## **1. Keputusan grid-cols/gap di Tiap Breakpoint**
saya memutuskan untuk menggunakan pendekatan mobile-first pada tata letak grid, yang mana artiny aku memprioritaskan tampilan untuk layar kecil terlebih dahulu, baru kemudian menyesuaikannya untuk layar yang lebih besar.

#### **- Mobile (Default):**
saya tidak menambahkan kelas grid-cols untuk layar terkecil. krena Berkat prinsip mobile-first, Tailwind secara otomatis mengatur feed-nya menjadi satu kolom. Ini pilihan terbaik karena di layar HP, satu foto per baris membuat gambar terlihat besar dan jelas, mencegah tumpang tindih.

#### **-Tablet (md):**
 Ketika layar membesar ke ukuran tablet, saya menggunakan md:grid-cols-2. Ini memanfaatkan ruang horizontal yang lebih lebar dengan menampilkan dua foto per baris. Pengguna bisa melihat lebih banyak konten tanpa banyak menggulir.

#### **-Desktop (lg):**
 Untuk layar desktop, saya memakai lg:grid-cols-3. Tiga kolom adalah format yang umum dan nyaman dilihat untuk galeri foto di layar lebar, memberikan tampilan yang rapi dan profesional seperti Instagram versi desktop.

Selain itu, saya menyesuaikan jarak antar foto dengan gap-1 dan md:gap-2. Jarak yang lebih kecil di mobile (gap-1) membantu menghemat ruang, sedangkan jarak yang lebih besar di tablet (md:gap-2) membuat tampilan tidak terlalu padat.

## **2. Memanfaatkan Utility Responsive Tailwind untuk Masalah Layout**
saya menggunakan fitur responsif Tailwind untuk mengatasi masalah tata letak, terutama pada bagian header profil, agar tampilannya fleksibel di berbagai perangkat.

#### **-Tata Letak Header:**
 Di perangkat mobile, foto profil dan statistik tersusun secara vertikal dengan flex flex-col. Namun, begitu beralih ke tablet (md:), saya mengubahnya menjadi horizontal dengan md:flex-row. Ini adalah contoh bagaimana satu baris kode bisa mengubah tata letak secara drastis untuk tampilan yang lebih efisien.

#### **-Ukuran Elemen:**
 saya juga mengatur ukuran foto profil dan tombol agar proporsional. Foto profil memiliki ukuran w-24 h-24 di mobile, kemudian membesar menjadi md:w-48 md:h-48 di tablet. Hal yang sama berlaku untuk tombol; mereka memiliki lebar penuh di mobile (w-full) tetapi menyesuaikan diri menjadi md:w-auto di tablet.

## **3. Trade-off Antara Banyak Utility Classes vs. Component CSS**
Dalam proyek ini, saya memilih untuk memakai banyak utility classes daripada membuat file CSS terpisah. Ini punya kelebihan dan kekurangan.

#### **1. Kelebihan Utility Classes:**

- Sangat Cepat: saya bisa langsung mengaplikasikan gaya di dalam kode HTML. Ini mempercepat proses pembuatan dan eksperimen dengan tata letak.

- Mudah Diubah: Kalau ingin mengubah gaya, saya hanya perlu mengedit beberapa kelas langsung di HTML, tidak perlu bolak-balik ke file lain.

#### **2. Kekurangan Utility Classes:**

- Kode HTML "berbobot/besar":
Baris kode class bisa menjadi sangat panjang dan kurang rapi. Ini bisa menyulitkan saat membaca kode, terutama bagi orang lain.

- Kurang Terstruktur:
Jika ada banyak elemen yang memiliki gaya sama, saya harus mengulang semua kelasnya. Jika proyeknya semakin besar, ini bisa jadi tidak efisien.

Secara keseluruhan, untuk proyek praktikum seperti ini, pendekatan utility-first yang saya gunakan adalah pilihan yang sangat tepat karena memungkinkan saya fokus pada implementasi dan memahami cara kerja Tailwind dengan cepat.