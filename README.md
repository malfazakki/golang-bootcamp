# 🐹 Golang Bootcamp: Zero to Production

Repositori pembelajaran mandiri Golang intensif dengan pendekatan **1-on-1 AI Mentoring** berbasis **Google Antigravity**. Dirancang khusus untuk memperkuat fondasi bahasa Go dari nol hingga level arsitektur backend siap produksi, mengadopsi standar idiomatis (*Effective Go*), dan transisi *mental model* dari ekosistem JavaScript/TypeScript.

---

## 🎯 Metodologi Belajar

Bootcamp ini mengadopsi prinsip pembelajaran kognitif modern:
- **Socratic Method**: Pembelajaran aktif berbasis pertanyaan pemandu, bukan sekadar menyalin jawaban.
- **Cognitive Load Control**: Materi disajikan ringkas dan padat (maks. 1.200–1.500 kata per sesi) dengan contoh kode terfokus (maks. 40–50 baris).
- **Spaced Repetition**: Konsep yang lemah dijadwalkan ulang secara otomatis pada interval **H+1**, **H+3**, **H+7**, dan **H+14**.
- **Industry Engineering Standard**: Penerapan toolchain nyata sejak dini (`goimports`, `dlv`, `golangci-lint`, `go test -race`, structured logging `slog`, Docker multi-stage, dan CI).

---

## 🗺️ Silabus & Kurikulum

| Modul | Topik Utama | Cakupan Materi |
| :---: | :--- | :--- |
| **00** | **Persiapan & Tooling** | Setup Go, `go mod`, `gopls`, Delve (`dlv`), struktur dasar |
| **01** | **Fondasi Dasar** | Tipe data, zero value, control flow, function, `defer`, error dasar |
| **02** | **Struktur Data** | Array, Slice (`len`/`cap`/aliasing), Map, Struct, Pointer semantics |
| **03** | **Abstraksi** | Interface (implicit implementation), Embedding, Generics |
| **04** | **Error Handling Lanjutan** | Error wrapping (`%w`), `errors.Is`/`As`, Custom error, `panic`/`recover` |
| **05** | **Package & Tooling** | Standard project layout (`cmd/`, `internal/`), `go test`, benchmark, linter |
| **06** | **Concurrency** | Goroutine, Channel, `select`, `sync` primitives, `context`, worker pool |
| **07** | **Standard Library** | `net/http`, `encoding/json`, `io`/`bufio`, `time`, `log/slog`, `database/sql` |
| **08** | **Backend dengan Go** | REST API, middleware, migrasi DB, graceful shutdown, backend security |
| **09** | **Testing Lanjutan** | Table-driven test, interface mocking, integration test |
| **10** | **Advance Go** | Profiling (`pprof`), escape analysis, GC internals, clean architecture |
| **11** | **Capstone Project** | REST API Task Manager lengkap (PostgreSQL, Docker Compose, CI) |

Detail pelacakan pemahaman setiap topik dapat dipantau di [PROGRESS.md](PROGRESS.md).

---

## 🤖 AI Mentor Workflows (.agents/skills)

Workspace ini dilengkapi dengan modul otomasi berbasis *Antigravity Skills*:

- **`bootcamp-session`**: Mengatur alur sesi belajar, memeriksa antrean Spaced Repetition yang jatuh tempo, dan menyajikan materi baru.
  - *Trigger:* `"mulai sesi"`, `"lanjut belajar"`, `"next topic"`
- **`bootcamp-quiz`**: Membuat paket kuis bertingkat (*Easy*, *Medium*, *Hard*) tanpa kunci jawaban langsung untuk menguji pemahaman.
  - *Trigger:* `"quiz"`, `"kuis"`, `"latihan soal"`
- **`bootcamp-review`**: Melakukan audit kode standar Senior Go Engineer (koreksi, idiom Go, concurrency safety, performa alokasi memori, dan keamanan).
  - *Trigger:* `"review kode quick"`, `"review kode deep"`
- **`bootcamp-progress`**: Merekap hasil latihan, mencatat evaluasi ke `PROGRESS.md`, dan menjadwalkan Spaced Repetition untuk konsep yang masih butuh penguatan.
  - *Trigger:* `"selesai sesi"`, `"update progress"`

---

## 📁 Struktur Repositori

```text
golang-bootcamp/
├── AGENTS.md                  # Sistem instruksi operasional & peran mentor
├── PROGRESS.md                # Tracker progres kurikulum & antrean Spaced Repetition
├── README.md                  # Dokumentasi repositori
├── .agents/
│   └── skills/                # Antigravity progressive-disclosure workflows
│       ├── bootcamp-session/
│       ├── bootcamp-quiz/
│       ├── bootcamp-review/
│       └── bootcamp-progress/
└── (module folders)           # Struktur project Go (dimulai dari Modul 05+)
```

---

## 🛠️ Prasyarat & Lingkungan

- **Go**: Versi 1.22+ (Direkomendasikan versi stabil terbaru)
- **Editor**: VS Code (dengan ekstensi Go resmi) atau GoLand
- **Tools**:
  ```bash
  go install golang.org/x/tools/gopls@latest
  go install golang.org/x/tools/cmd/goimports@latest
  go install github.com/go-delve/delve/cmd/dlv@latest
  ```

---

## 📜 Lisensi

Proyek ini dibuat untuk keperluan pembelajaran pribadi dan terbuka di bawah lisensi [MIT](LICENSE).
