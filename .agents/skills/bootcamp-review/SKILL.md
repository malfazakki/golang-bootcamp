---
name: bootcamp-review
description: >-
  Melakukan review kode Go standar senior software engineer.
  Gunakan skill ini ketika user meminta review kode
  (kata kunci: "review kode", "code review", "review quick", "review deep", "cek kodingan").
---

# Workflow Senior Code Review Golang

Lakukan audit menyeluruh terhadap kode Go yang diberikan user dengan perspektif Senior Go Engineer.

## Mode Review
- **`quick`**: Fokus utama pada kebenaran logika (*correctness*) dan idiom Go (*Effective Go*). Ringkas dan to-the-point (maksimal 1–2 saran prioritas).
- **`deep`** *(default bila tidak disebut)*: Audit komprehensif mencakup semua aspek di bawah ini.

## Checklist Audit Code Review

1. **Correctness & Logic**
   - Apakah kode berjalan sesuai spesifikasi?
   - Apakah ada potensi *nil pointer dereference*, *index out of range*, atau unhandled zero values?

2. **Go Idiomatic & Conventions**
   - Apakah menganut prinsip *"Accept interfaces, return structs"*?
   - Penamaan package, interface, variable: ringkas, camelCase, tanpa redundansi package name (mis. `user.New` bukan `user.NewUser`).
   - Error handling: apakah error diperlakukan sebagai value, dibungkus dengan `%w`, atau malah ditelan diam-diam?

3. **Concurrency & Resource Safety** *(Jika ada)*
   - Apakah goroutine dijamin berhenti (no goroutine leaks)?
   - Apakah sinkronisasi data race-free (`sync.Mutex`, channel)?
   - Apakah `context.Context` diteruskan sebagai parameter pertama dan di-cancel tepat waktu?
   - Apakah resource yang dibuka (`defer r.Close()`, `defer file.Close()`) ditutup dengan aman?

4. **Performance & Memory Semantics**
   - Value vs Pointer receiver: apakah tepat guna dan tidak menyebabkan escape to heap yang tidak perlu?
   - Slice & Map: apakah pre-allocated (`make([]T, 0, cap)`) bila panjang data sudah diketahui?

5. **Keamanan (Security)**
   - SQL Injection: selalu parameterized queries di `database/sql`.
   - Secret hardcoding: wajib membaca dari environment variable.
   - Timing-safe comparison untuk token/kredensial (`subtle.ConstantTimeCompare`).

## Format Laporan Review
- **Ringkasan Evaluasi**: Status kelayakan produksi (Ready / Minor Refactor / Needs Rework).
- **Daftar Temuan**:
  - `[Bug/Critical]`
  - `[Non-Idiomatic / Style]`
  - `[Performa / Resource]`
- **Rekomendasi Kode**: Tunjukkan perbandingan *Before vs After* dengan penjelasan alasan teknisnya.
