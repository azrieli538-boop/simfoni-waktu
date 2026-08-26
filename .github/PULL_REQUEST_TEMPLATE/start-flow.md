---
name: "Start flow: Game screen & UX fixes"
about: "Ensure single-start flow and add simple game screen with quit option"
title: "Start flow: persistent game screen"
labels: ["bug","ux","auto-merge"]
---

Perubahan ini memperbaiki masalah pengguna yang menekan tombol 'Mulai Permainan' namun terus diminta untuk memulai lagi. Perubahan utama:
- Tambah screen permainan sederhana (#game-screen) yang muncul setelah menekan Mulai
- Satu kali start bersifat persisten sampai pemain menekan 'Keluar ke Beranda'
- Hapus pointerdown handler yang memanggil click() untuk mencegah pemanggilan ganda
- Perbaikan aksesibilitas (fokus) dan tombol nonaktif saat permainan berjalan

Langkah uji singkat:
1. Buka index.html dari branch fix/start-flow
2. Tekan Mulai sekali — layar akan berubah ke "Permainan Dimulai"
3. Klik Keluar ke Beranda untuk kembali dan mengulangi
