##  HOW TO INSTALL TestDisk & PhotoRec

## Lakukan Update dan instalasi testdisk
sudo apt update && sudo install testdisk -y

## PANDUAN RINGKAS RECOVERY DATA DENGAN PHOTOREC (UBUNTU)
======================================================

1. INSTALASI & MENJALANKAN
   - Buka Terminal (Ctrl+Alt+T).
   - Jalankan perintah instalasi:
     sudo apt update && sudo apt install testdisk -y
   - Jalankan aplikasinya:
     sudo photorec

2. PEMILIHAN DRIVE & PARTISI
   - Pilih Drive: Gunakan panah [↑/↓] untuk memilih HDD/SSD/Flashdisk berdasarkan ukurannya. Pilih [Proceed] lalu Enter.
   - Pilih Tipe Partisi: Pilih [Intel] atau [EFI GPT] (biasanya sudah otomatis terdeteksi untuk Windows/FAT32/NTFS), lalu Enter.
   - Pilih Partisi: Pilih partisi NTFS/FAT32 spesifik yang ingin di-scan.

3. FILTER EKSTENSI FILE (Opsional tapi Rekomendasi)
   - Sebelum scan, geser ke menu [File Opt] di bawah, lalu Enter.
   - Tekan tombol 's' untuk menghilangkan semua centang.
   - Cari ekstensi yang dicari (misal: jpg, mp4, docx, pdf), tekan Spasi untuk mencentang.
   - Tekan 'b' untuk menyimpan dan kembali.

4. METODE SCANNING
   - Di menu utama partisi, pilih [Search].
   - Pilih [Other] (untuk format Windows NTFS/FAT32/exFAT).
   - Pilih [Whole] untuk melakukan Deep Scan ke seluruh sektor disk.

5. MENENTUKAN WADAH / FOLDER HASIL RECOVERY
   - Masuk ke folder 'home' -> [Nama User Anda] -> 'Downloads' atau 'Documents' (Gunakan drive internal Ubuntu, JANGAN pilih drive yang sedang di-scan).
   - Jika sudah berada di folder tujuan yang aman, tekan tombol 'C' (huruf C besar) pada keyboard untuk memulai proses.
   - Hasil akan tersimpan otomatis di dalam folder bernama 'recup_dir.1', 'recup_dir.2', dst.

## PANDUAN RINGKAS RECOVERY PARTISI DENGAN TESTDISK (UBUNTU)
=========================================================

1. MENJALANKAN UTILITY
   - Buka Terminal (Ctrl+Alt+T).
   - Jalankan perintah dengan hak akses root:
     sudo testdisk

2. MEMBUAT FILE LOG
   - Pilih [Create] pada layar pertama untuk membuat file log baru, lalu tekan Enter.

3. PEMILIHAN DRIVE
   - Gunakan panah [↑/↓] untuk memilih HDD/SSD/Flashdisk yang partisinya bermasalah berdasarkan ukuran disk.
   - Pilih [Proceed] di bagian bawah, lalu tekan Enter.

4. MENENTUKAN TIPE TABEL PARTISI
   - Pilih tipe partisi yang sesuai. TestDisk biasanya otomatis menyorot pilihan yang tepat, seperti [Intel] (untuk MBR) atau [EFI GPT] (untuk partisi modern). Tekan Enter.

5. ANALISIS STRUKTUR DISK
   - Pilih menu [Analyse] untuk memeriksa struktur partisi saat ini, lalu tekan Enter.
   - Pilih [Quick Search] di layar berikutnya untuk mulai mencari partisi yang hilang/terhapus.

6. MEMERIKSA ISI FILE (PENTING!)
   - Setelah partisi ditemukan (berwarna hijau), sorot partisi tersebut.
   - Tekan tombol 'P' (huruf P kecil) untuk mengintip daftar file di dalamnya:
     * File Putih = File normal yang masih ada/sehat.
     * File Merah = File yang sudah terhapus dan bisa di-recovery.
   - Tekan 'Q' untuk keluar dari mode intip file.

7. MENULIS ULANG TABEL PARTISI
   - Tekan Enter pada partisi hijau yang ingin dikembalikan.
   - Di menu bagian bawah, geser panah ke kanan dan pilih [Write], lalu tekan Enter.
   - Konfirmasi dengan menekan tombol 'Y' pada keyboard.
   - Lepas dan colok kembali flashdisk (atau restart PC) agar perubahan terbaca oleh sistem.
