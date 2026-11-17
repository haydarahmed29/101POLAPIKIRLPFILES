# 101.Polapikir landing page

- index.html: beranda (link di bio)
- p/*.html: 5 halaman produk Rp 27.000, tiap halaman ada kartu paket 59rb
- video/: animasi situasi dan mockup aplikasi (MP4 + poster JPG)

Tiap file HTML sudah berdiri sendiri (desain dan script ada di dalamnya).
Link lynk.id diisi di blok CONFIG di bagian atas tiap file HTML. Isinya sama di keenam file.

Letak file: index.html di root, halaman produk di folder p/, video di folder video/.
Kalau semua file ditaruh dalam satu folder yang sama, di CONFIG isi pageBase: "" dan homeUrl: "index.html".
Video dicari di folder video/ dulu, kalau tidak ada dicari di folder yang sama dengan halamannya.

Upload ke GitHub, aktifkan GitHub Pages (Settings, Pages, branch main).
Jangan pakai raw.githubusercontent.com untuk video: di iPhone (Safari) sering tidak mau diputar.

## Halaman PWA (4 aplikasi)

- p/polapikir-habit.html, p/polapikir-66-hari.html, p/polapikir-hidup-teratur.html, p/polapikir-gabungan.html
- Tiap halaman: hero, 6 video animasi 4:5 (720x900, 10 detik, loop, ada musik dan SFX, mulai tanpa suara, tombol Suara untuk menyalakan), carousel mockup aplikasi 9:16 (720x1274, 9 detik), lalu tombol Ambil dan kartu upsell.
- Video animasi: video/<slug>-1 sampai -6 (.mp4 dan .jpg). Mockup: video/app-habit-1..3, app-66hari-1..3, app-teratur-1..3, app-gabungan-1..4.
- Tombol Ambil memakai CONFIG: pwa.habit, pwa.hari66, pwa.teratur, gabungan.link. Upsell PWA ke gabungan.link, upsell Gabungan ke semua.link.

## Tema gelap dan terang

- Tombol di pojok kanan atas tiap halaman. Default mengikuti pengaturan HP atau komputer, pilihan disimpan (localStorage) dan berlaku di semua halaman.
- Tiap video dan mockup punya dua versi: `nama.mp4` (latar hitam) dan `nama-light.mp4` (latar putih), lengkap dengan poster `.jpg`.
- Halaman gelap memakai versi putih (-light), halaman terang memakai versi hitam, supaya video selalu kontras dengan halamannya.

## Harga (CONFIG)

Harga ditulis penuh: Rp 27.000 (satuan), Rp 57.000 (paket 5 alat), Rp 97.000 (tiap aplikasi), Rp 148.000 (Gabungan), Rp 177.000 (Semua). Ubah di blok CONFIG (angka saja).

## Tambahan konversi

- Bar Ambil menempel di bawah layar di 9 halaman produk. Muncul saat tidak ada tombol Ambil lain yang terlihat.
- FAQ di tiap halaman produk. Jawaban "cara terima", "bentuk" (5 alat harian), dan "refund" diisi di CONFIG.faq. Kalau null, pertanyaannya disembunyikan.
- Beranda: tombol produk bertuliskan "Lihat detail" karena membuka halaman produk, bukan checkout. Mockup aplikasi di beranda memakai app-*-1 (tanpa tanggal).
