---
name: bootcamp-progress
description: >-
  Menganalisis hasil sesi belajar, mencatat evaluasi, dan memperbarui file PROGRESS.md.
  Gunakan skill ini saat sesi selesai atau user meminta mencatat progres
  (kata kunci: "selesai sesi", "update progress", "catat progres", "akhiri sesi", "rekap progres").
---

# Workflow Pencatatan Progres Bootcamp

Gunakan alur ini setiap kali sebuah sesi belajar atau pengerjaan latihan selesai.

## Langkah Eksekusi

### 1. Evaluasi & Ekstraksi Data Sesi
Identifikasi dari riwayat obrolan sesi terakhir:
- **Modul & Topik**: Materi apa saja yang dibahas hari ini.
- **Topik Dikuasai**: Konsep yang dijawab/diterapkan user dengan lancar (skor >= 85).
- **Topik Lemah / Perlu Diperkuat**: Konsep yang mengalami salah paham, error logika berulang, atau skor latihan < 75.

### 2. Jadwalkan Spaced Repetition untuk Topik Lemah
Hitung tanggal review berdasarkan tanggal hari ini:
- **Tahap 1 (H+1)**: Besok hari (review 3 soal cepat).
- **Tahap 2 (H+3)**: 3 hari ke depan (1 soal Medium + rangkuman).
- **Tahap 3 (H+7)**: 7 hari ke depan (1 soal Hard + debug).
- **Tahap 4 (H+14)**: 14 hari ke depan (integrasi project).

Masukkan jadwal ini ke tabel **Antrean Spaced Repetition** di `PROGRESS.md`.

### 3. Update File `PROGRESS.md`
Edit `PROGRESS.md` dengan:
1. Update **Status Terkini** (Modul aktif, Topik terakhir, Tanggal diperbarui).
2. Centang `[x]` pada materi yang sudah tuntas dan dikuasai.
3. Tambahkan ringkasan ke bagian **Catatan Sesi Historis**:
   ```markdown
   ### [YYYY-MM-DD] - Modul X: <Nama Topik>
   - **Hasil Latihan**: Skor rata-rata X/100
   - **Kekuatan**: <Poin yang dikuasai>
   - **Area Perbaikan**: <Poin yang perlu diulang>
   - **Rekomendasi Sesi Berikutnya**: <Topik selanjutnya>
   ```

### 4. Konfirmasi ke User
Tampilkan ringkasan singkat hasil evaluasi hari ini ke chat dan ingatkan topik apa yang akan dipelajari di sesi berikutnya.
