# Golang Bootcamp - Progress Tracker

> File ini melacak progres pembelajaran dan jadwal Spaced Repetition Anda.  
> Diperbarui secara otomatis di akhir setiap sesi oleh AI Mentor (workflow `bootcamp-progress`).

---

## 📌 Status Terkini
- **Modul Aktif**: Modul 0 — Persiapan
- **Topik Terakhir**: Belum dimulai
- **Terakhir Diperbarui**: -

---

## 🔄 Antrean Spaced Repetition (Review Topik Lemah)
> Jadwal pengulangan otomatis: H+1 (3 soal cepat), H+3 (1 soal Medium + rangkuman), H+7 (1 soal Hard + debug), H+14 (integrasi)

| Tanggal Target | Topik | Tahap | Status | Catatan / Fokus |
| :--- | :--- | :--- | :--- | :--- |
| *Contoh: YYYY-MM-DD* | *Pointer vs Value Semantics* | *H+1* | *Menunggu* | *Review mutasi struct* |

---

## 📊 Ringkasan Pemahaman Materi

### Modul 0 — Persiapan
- [ ] Instalasi Go, GOPATH vs Go Modules, `go mod init`
- [ ] Tooling dasar: `go run`, `go build`, `go fmt`, `go vet`
- [ ] Development tools: `goimports`, `gopls`, Delve debugger (`dlv`)
- [ ] "Hello World" & struktur dasar

### Modul 1 — Fondasi
- [ ] Variabel, tipe data, zero value, konstanta
- [ ] Control flow (`if`, `for`, `switch`)
- [ ] Function, multiple return, defer
- [ ] Error handling dasar (error as value)

### Modul 2 — Struktur Data
- [ ] Array vs Slice (`len`, `cap`, aliasing, memory layout)
- [ ] Map (baca, tulis, delete, zero value check)
- [ ] Struct, method receiver (value vs pointer)
- [ ] Pointer semantics & memory allocation

### Modul 3 — Abstraksi
- [ ] Interface (implicit implementation, nil interface gotchas)
- [ ] Struct embedding & composition
- [ ] Generics dasar (type constraints, `any`, `comparable`)

### Modul 4 — Error Handling Lanjutan
- [ ] Error wrapping (`%w`, `errors.Is`, `errors.As`)
- [ ] Custom error types
- [ ] `panic` & `recover` (kapan dipakai, kapan dihindari)

### Modul 5 — Package & Tooling
- [ ] Go modules & standard project layout (`cmd/`, `internal/`, `pkg/`)
- [ ] Testing dasar (`go test`, `go test -cover`)
- [ ] Benchmark & `golangci-lint`

### Modul 6 — Concurrency
- [ ] Goroutine & Go scheduler
- [ ] Channel (buffered, unbuffered, direction)
- [ ] `select` & multiplexing
- [ ] `sync` (`Mutex`, `RWMutex`, `WaitGroup`, `Once`)
- [ ] `context` (cancellation, timeout, values)
- [ ] Worker pool & pipeline pattern
- [ ] Race condition & `go test -race`

### Modul 7 — Standard Library Penting
- [ ] `io` & `bufio`
- [ ] `encoding/json`
- [ ] `net/http` (client & server)
- [ ] `time`
- [ ] `log/slog` (structured logging)
- [ ] `database/sql`

### Modul 8 — Backend dengan Go
- [ ] REST API architecture & routing
- [ ] Middleware pattern
- [ ] Validasi input & response format
- [ ] Database migration (`golang-migrate`) & parameterized queries
- [ ] Graceful shutdown
- [ ] Security fundamentals (CORS, token timing, safe SQL)

### Modul 9 — Testing Lanjutan
- [ ] Table-driven tests
- [ ] Mocking via interface
- [ ] Integration testing dengan Testcontainers

### Modul 10 — Advance
- [ ] Profiling dengan `pprof`
- [ ] Escape analysis & memory layout
- [ ] Garbage Collection tuning
- [ ] Clean architecture ala Go

### Modul 11 — Capstone Project (Task Manager API)
- [ ] Core REST API & Data Model
- [ ] PostgreSQL integration & migrations
- [ ] Structured logging & middleware
- [ ] Dockerfile multi-stage & Docker Compose
- [ ] GitHub Actions CI (lint + test)
- [ ] Senior Engineer Code Review (Lulus >= 75)

---

## 📝 Catatan Sesi Historis
*(Log setiap sesi belajar akan dicatat otomatis di sini)*
