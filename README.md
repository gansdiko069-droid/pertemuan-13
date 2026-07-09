# Profile Card App - Pertemuan 13 (Sistem Informasi)

Aplikasi mobile berbasis React Native (Expo) yang mendemonstrasikan integrasi fitur-fitur native perangkat (*hardware access*) seperti kamera, galeri foto, dan pelacakan lokasi berbasis GPS, serta penyimpanan data lokal secara persisten.

---

## 🚀 Deskripsi & Fitur Aplikasi

Aplikasi ini dirancang untuk memenuhi tugas Pertemuan 13, berfokus pada implementasi *Device Features* (Kamera & GPS). Aplikasi dikembangkan menggunakan Expo SDK 54 agar sepenuhnya kompatibel dengan ekosistem Expo Go.

### 🟢 Level 1 — Fitur Wajib (Core)
* **Akses Fitur Native:** Mengintegrasikan modul Kamera (`expo-image-picker`), Galeri Foto, dan koordinat GPS (`expo-location`).
* **Alur Perizinan (Permission Flow) yang Benar:** Meminta izin akses terlebih dahulu, memvalidasi status `granted`, baru kemudian mengeksekusi fungsi perangkat.
* **Penanganan Penolakan Izin:** Menampilkan pesan edukatif yang ramah menggunakan `Alert` jika pengguna menolak memberikan izin, sehingga aplikasi tidak *crash*.
* **Penanganan Pembatalan (Canceled State):** Memvalidasi kondisi `result.canceled` sebelum memproses data URI foto.
* **Antarmuka (UI) Rapi:** Tampilan berbentuk *Card Profile* yang bersih, estetik, dan responsif.

### 🟡 Level 2 — Pengembangan (Fitur Pilihan)
* **[Level 2] Kombinasi Kamera + Galeri:** Menyediakan dialog pilihan sumber foto (*Kamera* atau *Galeri*) menggunakan komponen `Alert` yang interaktif sebelum mengakses perangkat.
* **[Level 2] Persistensi Data (AsyncStorage):** Menyimpan URI foto profil dan koordinat lokasi terakhir ke penyimpanan lokal menggunakan `@react-native-async-storage/async-storage`. Data otomatis dimuat kembali saat aplikasi ditutup dan dibuka ulang.

### 🔴 Level 3 — Tantangan Bonus
* **[Bonus] Hapus Foto:** Menyediakan tombol hapus untuk membersihkan data koordinat dan mengembalikan foto profil ke gambar *placeholder* default.

---

## 🛠️ Tech Stack & Dependencies

* **Framework:** React Native (Expo SDK 54 - Optimized for Expo Go)
* **Bahasa Pemrograman:** JavaScript (ES6+)
* **Dependencies Utama:**
  * `expo-image-picker` (Akses Kamera & Galeri)
  * `expo-location` (Akses GPS & Koordinat)
  * `@react-native-async-storage/async-storage` (Persistensi Data Lokal)

---

## 📸 Dokumentasi & Screenshot

| 1. Dialog Izin & Pilihan | 2. Hasil Foto & Lokasi | 3. Penanganan Penolakan |
| :-: | :-: | :-: |
| ![Dialog Izin & Pilihan](./screenshots/dialog_izin.png) | ![Hasil Foto Lokasi](./screenshots/hasil_foto.png) | ![Penanganan Penolakan](./screenshots/penolakan_izin.png) |
| *Meminta izin akses & menampilkan opsi Kamera/Galeri.* | *Foto profil berubah dan koordinat GPS berhasil didapatkan.* | *Pesan edukatif ramah saat pengguna menolak memberikan izin.* |

> 💡 **Catatan Pengumpulan:** Pastikan Anda telah mengambil 3 screenshot tersebut dari HP Anda, buat folder bernama `screenshots` di proyek Anda, lalu simpan file fotonya dengan nama `dialog_izin.png`, `hasil_foto.png`, dan `penolakan_izin.png`.

---

## 💻 Cara Menjalankan Proyek

### 1. Kloning Repositori
```bash
git clone [https://github.com/gansdiko069-droid/pertemuan-13.git](https://github.com/gansdiko069-droid/pertemuan-13.git)
cd pertemuan-13