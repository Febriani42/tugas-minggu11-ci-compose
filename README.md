# Tugas Minggu 11: CI untuk Repo Compose

![Compose Check](https://github.com/USERNAME/tugas-minggu11-ci-compose/actions/workflows/compose-check.yml/badge.svg)

**Nama:** Ridwanika Dinda Febriani

**NIM:** 202557201011

**Mata Kuliah:** Teknologi Open Source

## Deskripsi

Workflow GitHub Actions bernama Compose Check digunakan untuk memvalidasi sintaks file docker-compose.yml secara otomatis.

Workflow berjalan setiap ada push ke branch main dan setiap ada Pull Request.

## Isi Repositori

- .github/workflows/compose-check.yml: workflow CI
- docker-compose.yml: stack WordPress + MySQL
- .env.example: contoh variabel lingkungan
- .gitignore: mengabaikan file .env
- bukti/: tangkapan layar hasil pengerjaan

## Cara Kerja Workflow

1. GitHub Actions melakukan checkout repository.
2. Menyalin .env.example menjadi .env.
3. Menjalankan docker compose config -q.
4. Jika konfigurasi benar, check berwarna hijau.
5. Jika konfigurasi salah, check berwarna merah.

## Bukti

1. Run hijau
2. Pull Request merah
3. Badge hijau

## Kendala

Kendala yang ditemukan adalah kesalahan indentasi pada file docker-compose.yml. Kesalahan tersebut menyebabkan proses validasi gagal.

## Refleksi

Dari praktikum ini saya memahami bahwa GitHub Actions dapat membantu melakukan pengecekan otomatis terhadap file konfigurasi sebelum perubahan digabungkan ke branch main.
