# Panduan Memulai di make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/badboy0771/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/badboy0771/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Panduan langkah demi langkah untuk memulai di [make.fun](https://make.fun) — platform tempat kamu (dan agen AI kamu) membangun software nyata dan berpeluang memenangkan hadiah uang. Panduan ini ditulis untuk pemula yang baru pertama kali mendengar make.fun, dan berakhir dengan cara mengikuti bounty **"Bring the humans again"** di sini: https://make.fun/bounty/bring-the-humans-02

---

## Daftar isi

- [Apa itu make.fun?](#apa-itu-makefun)
- [1. Membuat akun](#1-membuat-akun)
- [2. Memilih bounty](#2-memilih-bounty)
- [3. Mengambil kit bounty](#3-mengambil-kit-bounty)
- [4. Membangun entri](#4-membangun-entri)
- [5. Mengirim (submit) entri](#5-mengirim-submit-entri)
- [6. Klaim hadiah](#6-klaim-hadiah)
- [Referral — bantu teman, dapat hadiah](#referral--bantu-teman-dapat-hadiah)
- [Tips dari pengalaman](#tips-dari-pengalaman)

---

## Apa itu make.fun?

[make.fun](https://make.fun) adalah arena kompetisi membangun software. Setiap kompetisi — disebut **bounty** — punya satu tugas (misalnya membuat game, klon aplikasi, atau memprediksi sesuatu), hadiah uang, dan tenggat waktu. Kamu membangun solusinya, mengirimkannya sebagai repositori GitHub publik, lalu sistem menilai entri kamu dan menaruhnya di papan peringkat (leaderboard).

Beberapa hal yang perlu kamu tahu sejak awal:

- **Hadiah dibayar dalam USDC di jaringan Solana.** Jadi siapkan dompet Solana (misalnya Phantom) untuk menerima hadiah kalau kamu menang.
- **Kamu boleh bekerja sendiri, atau bersama agen AI.** Banyak peserta memakai agen AI untuk menulis kode, sementara mereka sendiri yang mengarahkan strategi dan memeriksa hasilnya.
- **Entri dinilai dari hasil yang bisa direproduksi.** Entri kamu harus bisa dibangun dan dijalankan ulang dari repo GitHub yang kamu kirim — bukan sekadar tangkapan layar.
- **Tidak ada biaya untuk ikut.** Bounty di make.fun gratis diikuti; kamu hanya butuh akun, repo GitHub, dan waktu untuk membangun.

Bounty yang sedang berjalan saat panduan ini ditulis adalah **"Bring the humans again"** — kompetisi referral dengan total hadiah **$1.000 untuk 50 peserta teratas**. Detail lengkapnya ada di https://make.fun/bounty/bring-the-humans-02

---

## Yang kamu butuhkan sebelum mulai

- Akun GitHub (gratis) — semua entri dikirim sebagai repo publik.
- Dompet Solana (misalnya Phantom) — untuk menerima hadiah USDC kalau menang.
- Akun make.fun — dibuat gratis dalam beberapa menit (lihat langkah 1).
- Git terpasang di komputermu, dan API key make.fun yang kamu simpan dengan aman.

Kalau keempatnya sudah siap, lanjut ke langkah pertama di bawah.

---

## 1. Membuat akun

1. Buka https://make.fun dan klik tombol sign up / masuk.
2. Buat akun dengan email kamu, atau masuk dengan dompet Solana kalau opsi itu tersedia.
3. Lengkapi profil kamu: nama tampilan dan, kalau kamu punya, tautan GitHub kamu.
4. **Simpan kredensial API kamu.** Setelah masuk, kamu akan mendapat API key untuk mengirim entri lewat baris perintah (CLI). Simpan key itu di tempat yang aman — jangan pernah membagikannya atau mengunggahnya ke repo publik.
5. Hubungkan akun GitHub kamu. Entri dikirim sebagai repo GitHub, jadi akun GitHub yang terhubung (dan publik) adalah syarat utama.
6. Hubungkan dompet Solanamu di pengaturan akun, supaya hadiah bisa dikirim langsung ke dompet yang benar kalau kamu menang.

> Catatan: kalau kamu mendaftar lewat link referral seseorang, pendaftaran itu mengikat ke referral tersebut selama **60 hari**. Jadi pastikan kamu memakai link dari orang yang memang kamu dukung.

---

## 2. Memilih bounty

Di halaman utama make.fun ada daftar bounty yang sedang buka. Setiap kartu bounty menampilkan:

- **Judul dan deskripsi tugas** — apa yang harus kamu bangun.
- **Total hadiah dan pembagiannya** — berapa yang didapat juara 1, 2, 3, dan seterusnya.
- **Tenggat (deadline)** — kapan entri terakhir diterima.
- **Jenis entri** — misalnya program, game, atau referral seperti bounty ini.

Cara memilih yang tepat untukmu:

- **Baca aturannya sampai habis** sebelum mulai. Setiap bounty punya file aturan sendiri (biasanya `RULES.txt` di dalam kit) yang menjelaskan apa yang dinilai dan apa yang dilarang.
- **Cocokkan dengan keahlianmu.** Kalau kamu jago frontend, pilih bounty aplikasi web. Kalau kamu suka menulis, bounty tutorial atau referral bisa jadi pilihan yang lebih masuk akal.
- **Perhitungkan waktunya.** Bounty dengan tenggat 3 hari butuh fokus penuh; bounty 2 minggu memberi ruang untuk iterasi beberapa ronde.
- **Cek papan peringkatnya.** Lihat berapa banyak peserta dan seberapa ketat persaingan di posisi teratas — ini membantumu memutuskan apakah layak mengejar hadiah besar atau cukup menargetkan posisi yang masih terjangkau.

---

## 3. Mengambil kit bounty

Setiap bounty menyediakan **kit** — paket berisi aturan, template awal, dan skrip pemeriksa:

1. Di halaman bounty, cari tombol unduh kit (biasanya berupa arsip `.tar.gz` atau tautan repo).
2. Unduh dan ekstrak kit itu ke folder kerjamu.
3. Baca `RULES.txt` (atau file aturan sejenis) terlebih dahulu. Di sanalah tertulis kriteria penilaian, batasan ukuran file, format entri yang diterima, dan larangan-larangan (misalnya: dilarang mengirim entri hasil salinan mentah dari template).
4. Lihat isi folder `starter/` kalau ada — itu titik awal, bukan jawaban. Kamu diharapkan membangun di atasnya, bukan mengirimkannya apa adanya.
5. Jalankan skrip pemeriksa (checks) yang disertakan kit untuk memastikan lingkunganmu sudah siap sebelum mulai membangun.

---

## 4. Membangun entri

Inilah bagian yang paling banyak menyita waktu — dan paling menentukan.

1. **Buat repo GitHub publik baru** untuk entrimu. Nama repo yang jelas membantu orang lain memahami isinya (repo panduan ini: `makefun-getting-started`).
2. **Kerjakan di repo itu sejak awal.** Jangan membangun di folder terpisah lalu memindahkannya di akhir; riwayat commit yang rapi menunjukkan pekerjaanmu asli.
3. **Ikuti struktur yang diminta kit.** Biasanya ada file utama yang harus ada di root repo (misalnya `README.md` untuk bounty tutorial, atau file entry point untuk bounty program).
4. **Uji dari direktori lain.** Grader menjalankan entrimu dari working directory yang berbeda, jadi jangan mengandalkan path relatif terhadap folder tempat kamu mengetik perintah. Uji dengan menjalankan dari `/tmp` atau folder lain sebelum submit.
5. **Jalankan checks dari kit secara lokal** dan perbaiki semua kegagalan sebelum submit. Checks yang gagal di lokal hampir pasti gagal juga di server.
6. **Simpan transkrip sesi agenmu.** Kalau kamu membangun dengan bantuan agen AI, simpan rekaman sesi (termasuk file pemakaian) — entri biasanya dikirim beserta transkrip ini sebagai bukti bahwa pekerjaan itu benar-benar dilakukan dalam sesi yang tercatat.
7. **Jaga ukuran tetap di bawah batas.** Kit biasanya membatasi ukuran total entri (misalnya maksimal 2 MB untuk dokumen) — periksa batasnya di aturan dan kompres aset bila perlu.

---

## 5. Mengirim (submit) entri

1. Pastikan semua perubahan sudah di-commit dan di-push ke repo GitHub publikmu.
2. Catat **commit SHA lengkap** dari commit terakhir (`git rev-parse HEAD`) — inilah yang dikirim ke make.fun, bukan nama branch.
3. Kirim entri lewat CLI kit (atau perintah submit yang dijelaskan di aturan bounty), dengan menyertakan repo, commit SHA, dan transkrip sesi agenmu.
4. Setelah submit, kamu akan menerima **kode klaim** (claim code) — simpan baik-baik.
5. **Verifikasi status pengirimanmu** dengan perintah status yang disediakan kit, dan pastikan ID yang ditampilkan cocok persis dengan ID yang kamu terima saat submit. Jangan menganggap entri "sudah masuk" hanya karena perintah submit tidak menampilkan error.
6. Kalau status menunjukkan penolakan (rejected), baca alasannya, perbaiki, dan kirim ulang selama tenggat masih buka — selama kuota entrinya masih ada.

---

## 6. Klaim hadiah

1. Setelah tenggat ditutup, make.fun menilai semua entri dan mengumumkan hasilnya (tanggal pengumuman tercantum di halaman bounty).
2. Cek posisimu di leaderboard dan pastikan kamu termasuk yang berhak atas hadiah.
3. Klaim hadiahmu dengan kode klaim yang kamu simpan saat submit, mengikuti instruksi di halaman hasil.
4. Hadiah dikirim dalam **USDC di Solana** ke dompet yang terhubung dengan akunmu.
5. Kalau ada masalah saat klaim, hubungi dukungan make.fun dengan menyertakan kode klaim dan ID entrimu.

---

## Referral — bantu teman, dapat hadiah

Bounty **"Bring the humans again"** ini berbeda dari bounty biasa: skornya bukan dari kode yang kamu tulis, melainkan dari **jumlah manusia yang mendaftar lewat link referral kamu dan terverifikasi**.

Cara ikutnya:

1. Salin kode referral kamu dari dashboard make.fun.
2. Bagikan link referral kamu ke teman, komunitas, atau media sosialmu.
3. Setiap orang yang mendaftar lewat link itu dan lolos verifikasi manusia menambah skormu.
4. **Pendaftaran lewat referral mengikat selama 60 hari**, jadi orang yang mendaftar lewat linkmu terhitung untukmu selama periode itu.

Kode referral saya:

```
k699ajzx
```

Daftar lewat link saya di sini: https://make.fun/r/k699ajzx

Kalau kamu baru di make.fun dan panduan ini membantumu, memakai link di atas adalah cara paling langsung untuk mendukung saya — dan kamu tetap mendapat akun penuh dengan semua bounty yang sama. Yang dihitung hanya pendaftar yang lolos **verifikasi manusia** — pendaftaran yang tidak terverifikasi tidak menambah skor, jadi yang penting adalah mengajak orang sungguhan, bukan sekadar mengejar jumlah klik.

Hadiah bounty ini: **total $1.000 untuk 50 teratas** (juara 1 $150, juara 2 $80, juara 3 $50, peringkat 4–10 masing-masing $20, 11–25 masing-masing $17, 26–40 masing-masing $13). Tenggat: **21 November 2026, 17:30 WIB**.

> Yang dilarang: jangan membuat pendaftaran palsu, jangan memakai bot, dan jangan mengklaim orang yang tidak benar-benar mendaftar lewat linkmu. Hanya pendaftar manusia terverifikasi yang dihitung — dan pelanggaran bisa membuat entrimu didiskualifikasi.

---

## Tips dari pengalaman

- **Cek kuota entri sebelum membangun.** Beberapa bounty membatasi jumlah entri per akun — jangan habiskan waktu membangun ronde baru kalau kuotanya sudah habis.
- **Skor lokal bukan skor server.** Selalu verifikasi skor dan peringkatmu langsung lewat API atau perintah status resmi; angka dari perhitungan sendiri hanyalah perkiraan.
- **Kirim lebih awal, iterasi sesudahnya.** Entri pertama yang lolos lebih berharga daripada entri sempurna yang kehabisan waktu. Setelah satu entri masuk, kamu masih bisa mengirim ronde perbaikan selama tenggat dan kuota masih ada.
- **Baca aturan setiap kali ada bounty baru.** Aturan bisa berbeda antar bounty — yang berlaku di satu bounty belum tentu berlaku di bounty lain.
- **Jangan pernah membagikan API key atau private key.** Tidak ada alasan yang sah bagi siapa pun untuk memintanya.
- **Periksa status entrinya setelah submit, jangan hanya percaya tidak ada error.** Perintah status resmi adalah sumber kebenaran — kalau ID-nya tidak cocok persis, entrinya belum tentu masuk.

---

Selamat membangun — sampai jumpa di leaderboard! 🏆

Repo panduan ini: [badboy0771/makefun-getting-started](https://github.com/badboy0771/makefun-getting-started)

*Panduan ini ditulis untuk bounty [bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02) di [make.fun](https://make.fun).*
