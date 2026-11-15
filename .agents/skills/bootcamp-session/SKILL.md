---
name: bootcamp-session
description: >-
  Mengelola alur sesi belajar bootcamp Golang sesuai kurikulum AGENTS.md.
  Gunakan skill ini ketika user ingin memulai sesi baru, melanjutkan belajar, atau berpindah ke topik berikutnya
  (kata kunci: "mulai sesi", "lanjut", "next topic", "belajar", "sesi baru").
---

# Workflow Sesi Belajar Bootcamp Golang

Ikuti alur terstruktur ini setiap kali sesi belajar baru dimulai:

## Prosedur Sesi

### 1. Pre-Session Check (Spaced Repetition & Status)
1. Buka dan baca file `PROGRESS.md`. Jika file belum ada tetapi terdapat `PROGRESS.template.md`, otomatis salin `PROGRESS.template.md` menjadi `PROGRESS.md`.
2. Cek tabel **Antrean Spaced Repetition**:
   - Apakah ada topik yang jatuh tempo review (H+1, H+3, H+7, atau H+14)?
   - **Jika ADA**: Alokasikan 5–10 menit pertama untuk review topik tersebut dengan 1–3 soal cepat. Jangan lanjut ke materi baru sebelum review selesai atau user meminta skip.
   - **Jika TIDAK ADA**: Langsung masuk ke topik kurikulum berikutnya sesuai status modul aktif di `PROGRESS.md`.

### 2. Penyampaian Materi (§5 AGENTS.md)
Sajikan materi dengan format wajib:
1. **Tujuan Belajar**: 2–3 poin spesifik.
2. **Mental Model & Analogi**: 1–2 kalimat analogi konkret di awal.
3. **Tabel Komparasi JS/TS** (jika ada padanan langsung):
   `Konsep Go | Padanan JS/TS | Beda utama`
4. **Penjelasan Konsep**: Lugas, padat, mendalam.
5. **Contoh Kode**:
   - Maksimal 40–50 baris kode yang runnable dan lolos format `gofmt`.
   - Beri komentar di baris-baris krusial.
6. **Gotchas / Jebakan Umum**: Kesalahan yang sering dialami pemula atau developer eks-JS/TS.
7. **Rangkuman Cheat Sheet**: 3–5 poin intisari konsep.

> **PENTING**: Patuhi batas densitas: maksimal 1.200–1.500 kata per sesi. Jika topik terlalu luas, pecah menjadi sesi bertahap (mis. Sesi 1a, Sesi 1b).

### 3. Latihan Terpandu (§6 AGENTS.md)
Berikan 3 soal bertingkat:
- **Easy**: Pemahaman konsep / prediksi output.
- **Medium**: Penerapan / lengkapi kode / tulis fungsi kecil.
- **Hard**: Analisis bug / debugging / edge case.

> **ATURAN PEMBERIAN SOAL (SCAFFOLDING)**:
> 1. **Berikan soal SATU PER SATU** (mulai dari Easy). Jangan memberikan semua soal sekaligus.
> 2. Soal berikutnya baru diberikan setelah jawaban soal sebelumnya dievaluasi dan dipahami tuntas oleh user.
> 3. Jangan sertakan kunci jawaban bersamaan dengan soal. Tunggu user menjawab. Sertakan kriteria sukses / test cases agar user dapat memvalidasi sendiri.

### 4. Koreksi Jawaban (§7 AGENTS.md)
- Berikan penilaian objektif (Benar / Sebagian / Salah, skor 0–100).
- Bedakan antara: Bug vs Non-Idiomatic vs Performa/Keamanan.
- Gunakan pendekatan **Socratic**: jika ada error, tanyakan hipotesis user terlebih dahulu sebelum membocorkan solusi.
