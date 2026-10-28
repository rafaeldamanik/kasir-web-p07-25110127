# Hasil Pengujian Praktikum 7

Nama: ISI NAMA ANDA
NIM: ISI NIM ANDA
Kelas: TK Grup D

Isi hasil berdasarkan pengujian sendiri. Jangan mengisi Lulus sebelum mencoba.

| No | Skenario | Hasil yang diharapkan | Hasil aktual | Status |
|---|---|---|---|---|
| 1 | Buka halaman pertama | Form kosong dan belum ada ringkasan | ISI | ISI |
| 2 | Buku Tulis, 12000, 10 | Ringkasan dengan Rp12.000 dan 10 unit | ISI | ISI |
| 3 | Stok 0 | Diterima sebagai 0 unit | ISI | ISI |
| 4 | Harga -12000 | Ditolak dan isian lama tetap terlihat | ISI | ISI |
| 5 | Stok 2.5 | Ditolak | ISI | ISI |
| 6 | Harga abc | Ditolak | ISI | ISI |
| 7 | Nama hanya spasi | Ditolak server | ISI | ISI |
| 8 | Nama <b>Buku Tulis</b> | Tag tampil sebagai teks, tidak menebalkan hasil | ISI | ISI |
| 9 | Kosongkan form | Semua input dan ringkasan kembali kosong | ISI | ISI |
| 10 | Harga 00012000 dan stok 000 | Harga Rp12.000 dan stok 0 unit | ISI | ISI |

## Jawaban pemahaman

**1. Mengapa form menggunakan POST?**

POST digunakan untuk mengirim data form ke server untuk diproses tanpa menampilkan seluruh data tersebut di URL.

**2. Apa perbedaan `id` dan `name`?**

`id` digunakan untuk mengidentifikasi elemen HTML, sedangkan `name` digunakan sebagai nama data yang dikirim ke server melalui form.

**3. Mengapa stok nol tidak boleh dianggap gagal?**

Karena stok nol merupakan nilai yang valid. Artinya, produk sedang tidak memiliki persediaan, bukan berarti input salah.

**4. Apa perbedaan `trim`, validasi, dan `htmlspecialchars`?**

`trim` digunakan untuk menghapus spasi di awal dan akhir teks. Validasi digunakan untuk memeriksa apakah input sesuai aturan. `htmlspecialchars` digunakan untuk mengubah karakter khusus agar ditampilkan sebagai teks dan tidak diproses sebagai kode HTML.

**5. Apakah produk tersimpan permanen? Jelaskan.**

Tidak. Data hanya diproses pada request saat ini dan belum disimpan ke database atau session. Karena itu, data tidak tersimpan secara permanen.

**6. Mengapa POST tidak otomatis membuat aplikasi aman?**

Karena data yang dikirim melalui POST tetap bisa dimanipulasi. Oleh sebab itu, server harus melakukan validasi input dan encoding output untuk mengurangi risiko keamanan.

## Kendala dan perbaikan

Kendala yang saya alami terdapat pada modul nomor 14, yaitu kesalahan penulisan nilai harga untuk pengujian input negatif. Pada modul tertulis `12000`, padahal seharusnya `-12000`. Kesalahan tersebut membuat pengujian tidak sesuai dengan tujuan untuk menguji penolakan harga negatif.

Perbaikannya adalah mengganti nilai input menjadi `-12000`, kemudian menjalankan pengujian kembali untuk memastikan sistem menolak harga negatif dan mempertahankan isian form sebelumnya.