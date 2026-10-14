# IPScope — IP Intelligence

Website statis berbahasa Indonesia untuk melihat detail alamat IP publik. Dirancang agar bisa dibuka dari HP dan dipublikasikan ke GitHub Pages atau hosting statis lain.

## Fitur

- Otomatis memeriksa IP publik saat halaman dibuka.
- Pencarian alamat IPv4 dan IPv6.
- Detail perkiraan geolokasi: negara, wilayah, kota, kode pos, lintang/bujur, dan kode regional.
- Detail jaringan: ISP, organisasi, ASN, dan domain bila tersedia.
- Zona waktu, offset UTC, waktu lokal dari API, dan informasi mata uang bila tersedia.
- Tautan ke OpenStreetMap jika koordinat tersedia.
- Salin IP dan ekspor data JSON.
- Tidak menyimpan riwayat pencarian, tidak menggunakan cookie, dan tidak memerlukan API key sendiri.
- Memakai IPWho.is sebagai penyedia utama dan ipapi sebagai cadangan saat layanan utama gagal.

## Cara membuka di HP

1. Ekstrak ZIP.
2. Buka `index.html` di browser modern. Jika browser membatasi permintaan API dari file lokal, publikasikan folder ini ke GitHub Pages atau hosting HTTPS statis.
3. Koneksi internet diperlukan untuk mengambil data IP.

## Publikasi melalui GitHub Pages

1. Buat repository baru di GitHub.
2. Unggah `index.html` ke root repository.
3. Masuk ke **Settings → Pages**, pilih deployment dari branch utama dan folder root.
4. Buka URL GitHub Pages setelah publikasi selesai.

## Catatan akurasi dan privasi

- Lokasi IP adalah perkiraan berdasarkan basis data jaringan. Lokasi dapat menunjuk kota pusat ISP atau titik keluar VPN/proxy, bukan posisi GPS perangkat.
- Website tidak bisa menentukan nama pemilik IP, alamat rumah, atau lokasi real-time seseorang dari IP saja.
- Deteksi VPN/proxy/Tor hanya ditampilkan jika provider benar-benar mengembalikan data tersebut. Paket API gratis yang digunakan dapat tidak menyertakan data ini.
- Saat pencarian dilakukan, alamat IP yang dicari dikirim ke layanan API eksternal untuk mendapatkan hasil. Jangan gunakan untuk memproses data yang tidak berhak Anda akses.
- Kuota, kebijakan, skema, dan ketersediaan layanan pihak ketiga bisa berubah. Website tidak memiliki backend sendiri.

## API yang digunakan

- IPWho.is: https://ipwhois.io/documentation
- ipapi: https://ipapi.co/api/
