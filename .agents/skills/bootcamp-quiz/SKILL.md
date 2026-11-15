---
name: bootcamp-quiz
description: >-
  Membuat kuis dan paket soal latihan interaktif Golang berdasarkan materi yang sudah dipelajari.
  Gunakan skill ini ketika user meminta kuis, tes, atau soal latihan
  (kata kunci: "quiz", "kuis", "latihan", "soal", "uji pemahaman").
---

# Workflow Kuis Interaktif Golang

Gunakan panduan ini saat membuat kuis atau paket soal untuk menguji pemahaman user.

## Aturan Utama
1. **Dilarang keras menyertakan kunci jawaban di awal.** Kunci jawaban hanya dibahas setelah user memberikan respon jawabannya.
2. **Sertakan test case atau kriteria evaluasi** agar user dapat menguji logikanya sendiri sebelum menyerahkan jawaban.

## Format Paket Kuis

Buat 3–5 soal dengan tingkatan dan variasi berikut:

1. **Soal 1 — Easy (Prediksi Output / Konsep Dasar)**
   - Potongan kode kecil (10–15 baris).
   - Pertanyaan: Apa output kode berikut? Mengapa?

2. **Soal 2 — Medium (Lengkapi Kode / Implementasi Fungsi)**
   - Spesifikasi fungsi dengan signature jelas dan requirement idiomatis Go.
   - Contoh input dan output yang diharapkan.

3. **Soal 3 — Hard (Bug Hunting / Race Condition / Gotchas)**
   - Kode yang memiliki bug semantik, aliasing problem, goroutine leak, atau error handling tersembunyi.
   - Pertanyaan: Temukan bug-nya, jelaskan mengapa itu terjadi, dan tuliskan perbaikannya.

## Prosedur Koreksi Jawaban

Setelah user menjawab:
1. **Skor**: Berikan nilai 0–100 per soal dan total keseluruhan.
2. **Kategori Feedback**:
   - 🟢 **Correctness**: Apakah kode menghasilkan output yang benar?
   - 🔵 **Go Idiom**: Apakah cara penulisan sesuai standar Effective Go? (mis. naming, error handling, pointer usage).
   - 🟠 **Edge Cases & Performance**: Apakah ada alokasi memori berlebih, potential nil pointer dereference, dll?
3. **Pencatatan**: Jika user gagal di konsep tertentu, tandai topik tersebut agar dicatat ke `PROGRESS.md` untuk masuk jadwal Spaced Repetition.
