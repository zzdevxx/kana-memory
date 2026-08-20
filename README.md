# 🎴 Kana Memory

> Belajar huruf Jepang (Hiragana, Katakana, Kanji N5, Kosakata) lewat **Memory Game**, **Quiz**, dan **Flashcard**. Single-file offline web app — buka di browser, langsung pakai.

![Status](https://img.shields.io/badge/status-stable-a78bfa?style=flat-square)
![Stack](https://img.shields.io/badge/stack-vanilla_JS-fbbf24?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![Offline](https://img.shields.io/badge/100%25-offline-34d399?style=flat-square)
![Mobile](https://img.shields.io/badge/mobile--first-f472b6?style=flat-square)

---

## 📖 Tentang

**Kana Memory** adalah aplikasi web ringan untuk belajar bahasa Jepang level **JLPT N5** dengan pendekatan **gamifikasi**. Tidak ada server, tidak ada build step, tidak ada instalasi — cukup buka `index.html` di browser (HP, tablet, laptop) dan langsung main.

Cocok untuk pemula yang baru mulai belajar:
- **Hiragana** (46 karakter dasar)
- **Katakana** (46 karakter dasar)
- **Kanji N5** (35 karakter dasar)
- **Kosakata** (salam, angka, hari, warna, keluarga)

---

## ✨ Fitur

### 🎮 Memory Game (4 mode)
Pasangkan kartu kiri-kanan: karakter Jepang dengan romaji/arti-nya.
- **Hiragana Memory** — あ ↔ a
- **Katakana Memory** — ア ↔ a
- **Kosakata N5** — 水 ↔ air
- **Campuran** — hira + kata + kosakata digabung

Difficulty: 4 / 6 / 8 / 10 / 12 pasang (atur via **Pengaturan → Pasangan Kartu**). Best time tersimpan per mode.

### 📝 Quiz (5 mode)
Kuis pilihan ganda 10 soal dengan feedback instan + weighted random (soal yang sering salah lebih sering muncul).
- **Tebak Hiragana** — romaji → pilih karakter
- **Tebak Katakana** — romaji → pilih karakter
- **Tebak Arti Kosakata** — karakter → pilih artinya
- **Pilihan Ganda N5** — campuran kosakata & kanji
- **Kuis Acak Harian** — random dari semua kategori

Setelah kuis selesai: rating bintang (1–3), review jawaban salah, hadiah XP + koin, confetti animation.

### 📚 Belajar (Flashcard)
Browse + tap untuk lihat detail karakter. Tap 🔊 untuk dengar pelafalan (TTS bahasa Jepang / Indonesia).
- Hiragana · Katakana · Kanji N5
- Salam · Angka · Hari · Warna · Keluarga

Karakter yang sudah dipelajari ditandai ✓ dan menambah XP.

### 🏆 Gamifikasi
- **Level** — naik dari N5 Beginner → Student → Master → Sensei
- **XP** — earned dari game, kuis, belajar
- **Koin** 💰 — earned dari tantangan harian, dipakai beli tema
- **Streak** 🔥 — hari berturut-turut belajar
- **13 Achievement** — First Win, Perfect Score, 5/10/30 Streak, Quiz Master, Kanji 10/30, Master Hiragana/Katakana, Daily Hero, Collector
- **Tantangan Harian** — 3 task random per hari (main game, selesaikan kuis, hafalkan 5 karakter baru, dll)
- **Confetti animation** saat menang

### 🎨 4 Tema
- **Aurora** (default, gratis) — ungu + pink
- **Sakura** (100 koin) — rose + sakura
- **Matcha** (150 koin) — hijau matcha
- **Ocean** (200 koin) — cyan + teal

Tema bisa diganti kapan saja di **Profil → Tema & Hadiah**.

### 🔊 Audio (TTS)
Pelafalan karakter Jepang & kosakata Indonesia via **Web Speech API**. Tidak butuh file audio tambahan.

### 📱 Mobile-First
- Bottom nav dengan 5 tab (Home / Game / Kuis / Belajar / Profil)
- Sticky header dengan brand "Kana Memory"
- Touch-optimized cards (min 44px tap target)
- Safe-area inset untuk notch HP
- Dark mode (default) + light mode via tema

### 💾 100% Offline
Semua data tersimpan di **localStorage** — progress, settings, achievement, streak, best time. Tidak ada tracking, tidak ada API call (kecuali Google Fonts CDN untuk typography).

### ⚙️ Pengaturan
Menu Pengaturan berisi:
1. **🎴 Pasangan Kartu** — popup untuk pilih jumlah pasangan (4/6/8/10/12)
2. **ℹ️ Tentang Aplikasi** — info app, fitur, stack
3. **👨‍💻 Tentang Saya** — info developer (nama, NIM, prodi)
4. **Reset & Mulai Ulang** — hapus semua progress

---

## 👨‍💻 Developer

| Field    | Value                              |
|----------|------------------------------------|
| Nama     | Yureike Christiani Ismawan Bendon  |
| NIM      | 2302070004                         |
| Prodi    | Pendidikan Bahasa Jepang           |

Akses via **Pengaturan → Tentang Saya**.

---

## 🚀 Cara Menjalankan

### Opsi 1 — Buka langsung (paling simpel)
1. Download / clone repo ini
2. Double-click `index.html`
3. Browser terbuka → app jalan ✨

### Opsi 2 — Local server (opsional, untuk development)
```powershell
# Pakai Python
python -m http.server 8000

# Atau pakai Node
npx serve .

# Lalu buka http://localhost:8000
```

### Opsi 3 — Deploy ke hosting
Upload / push ke:
- **GitHub Pages** — commit, push, enable Pages
- **Netlify / Vercel** — drag & drop file
- **Cloudflare Pages** — connect repo, deploy

Tidak perlu build step. Tidak perlu config. Single file jalan di mana saja.

---

## 📂 Struktur File

```
KanaMemory/
├── index.html       ← Seluruh app (HTML + CSS + JS inlined)
├── README.md        ← Dokumentasi lengkap
└── LICENSE          ← Lisensi MIT
```

Yep, **cuma 1 file utama** untuk menjalankan seluruh aplikasi. 100% self-contained.

---

## 🛠️ Tech Stack

| Layer        | Technology                                   |
|--------------|----------------------------------------------|
| Markup       | HTML5                                        |
| Styling      | Vanilla CSS (CSS variables, grid, flex)      |
| Logic        | Vanilla JavaScript (ES2020+)                 |
| Storage      | `localStorage` (no backend)                  |
| Audio        | Web Speech API (`speechSynthesis`)           |
| Font         | Google Fonts: Inter, Shippori Mincho, Noto Sans JP |

**No frameworks. No bundler. No dependencies. No build step.**

---

## 🎯 Cara Pakai

### First-time setup
1. Buka `index.html`
2. Splash screen → tap **Mulai**
3. Masukkan nama kamu → tap **Ayo Mulai 🚀**
4. Mulai dari tab **Belajar** untuk hafal karakter, atau langsung ke **Game** / **Kuis**

### Daily routine (5-10 menit)
1. Buka app → otomatis dapat tantangan harian (3 task)
2. Main 1 memory game (~2 menit)
3. Selesaikan 1 kuis (~2 menit)
4. Hafal 5 karakter baru (~3 menit)
5. Cek achievement progress di **Profil**

### Tips belajar
- 🔥 **Streak** — buka app setiap hari, jangan putus
- 💰 **Koin** — selesaikan tantangan harian, jangan skip
- 📚 **Belajar dulu, baru main** — pahami karakter sebelum quiz
- 🎯 **Pakai TTS** — tap tombol 🔊 di detail karakter untuk dengar pelafalan

---

## 🗺️ Arsitektur Aplikasi

```
┌─────────────────────────────────────────────────┐
│                  Splash Screen                  │
│  (hanya untuk first-time visitor)               │
└────────────────────┬────────────────────────────┘
                     │
                     ▼
┌─────────────────────────────────────────────────┐
│            Onboarding (Nama input)              │
└────────────────────┬────────────────────────────┘
                     │
        ┌────────────┼────────────┬─────────────┐
        ▼            ▼            ▼             ▼
   ┌────────┐  ┌────────┐  ┌─────────┐   ┌──────────┐
   │  Home  │  │  Game  │  │  Kuis   │   │ Belajar  │
   │(Beranda)│  │ (4 mode)│  │(5 mode) │   │(8 tab)   │
   └────┬───┘  └────┬───┘  └────┬────┘   └────┬─────┘
        │           │           │             │
        │           ▼           ▼             ▼
        │      Game Play    Quiz Play    Learn Detail
        │     (board)       (soal)       (modal)
        │           │           │             │
        │           ▼           ▼             │
        │       Finish       Finish          │
        │       Modal        Modal           │
        │           │           │             │
        └───────────┴───────────┴─────────────┘
                     │
                     ▼
        ┌────────────┬─────────────┐
        ▼            ▼             ▼
   ┌─────────┐  ┌─────────┐  ┌──────────┐
   │ Profile │  │Settings │  │ Achievements│
   │ (stats) │  │ (config)│  │  (badges) │
   └─────────┘  └─────────┘  └──────────┘
```

Routing berbasis hash (`#/home`, `#/game`, dll) — tidak butuh server-side routing.

---

## 💾 Data & Privacy

Semua data disimpan **lokal di browser** (`localStorage`). Tidak ada server, tidak ada analytics, tidak ada tracking.

Keys yang disimpan:
- `kmc_user` — nama, XP, level, koin, tema
- `kmc_settings` — difficulty, theme mode
- `kmc_stats` — per-karakter correct/wrong count
- `kmc_best` — best time per game mode
- `kmc_achievements` — unlocked badge IDs
- `kmc_daily` — tantangan harian
- `kmc_visited_dates` — streak history
- `kmc_learned_chars` — karakter yang sudah ditandai dipelajari
- `kmc_last_screen` — last visited screen (untuk resume)
- `kmc_has_visited` — flag first-time visit

**Reset progress:** buka **Pengaturan → Reset & Mulai Ulang**, atau manual via DevTools → Application → Local Storage → hapus key `kmc_*` → refresh.

---

## 🎨 Kustomisasi

Mau ganti warna tema default? Edit CSS variables di bagian `:root` di `index.html`:
```css
:root {
  --primary: #a78bfa;       /* ungu */
  --primary-strong: #8b5cf6;
  --accent: #f472b6;        /* pink */
  --bg: #07061a;            /* dark background */
  --text: #f4f1ff;
}
```

Mau tambah kosakata? Edit konstanta `KOSAKATA` di dalam `<script>`:
```js
const KOSAKATA = {
  salam: [['こんにちは','halo'], ...],
  angka: [['一','satu'], ...],
  // tambah kategori baru di sini
  makanan: [['寿司','sushi'], ['味噌汁','sup miso'], ...]
};
```

Lalu tambahkan ke `LEARN_TABS`:
```js
const LEARN_TABS = [
  ...,
  { id: 'makanan', label: 'Makanan', data: KOSAKATA.makanan, color: '#fbbf24' }
];
```

---

## 🐛 Bug Fixes (Changelog)

### v3.1 (Juni 2026)
- **Fix:** Tombol "Lihat Hasil" kuis tidak bereaksi (crash `Daily.complete` saat data null)
- **Fix:** Outline 1px di kartu mode Game/Kuis/Belajar (border default jadi transparent)
- **New:** Menu **"Tentang Saya"** di Pengaturan — info developer (nama, NIM, prodi)
- **Update:** Pengaturan lebih simpel — "Default Game" dihapus (sudah ada di "Pasangan Kartu" popup)
- **Rename:** "Menu Pair" → "Pasangan Kartu"
- **Remove:** "Tentang Game Kartu" dari Pengaturan (redundan)

### v3.0
- Single-file app (HTML + CSS + JS inlined)
- 4 mode Memory Game, 5 mode Kuis, 8 tab Belajar
- Gamifikasi (level, XP, koin, streak, 13 achievement, tantangan harian)
- 4 tema (Aurora, Sakura, Matcha, Ocean)
- TTS audio (Web Speech API)
- Mobile-first bottom nav, dark/light mode

---

## 🐛 Browser Support

Tested on:
- ✅ Chrome / Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+ (iOS & macOS)
- ✅ Chrome Android 90+

Butuh browser modern yang support:
- CSS Grid & Custom Properties
- ES2020 (optional chaining, nullish coalescing)
- `speechSynthesis` API (audio — gracefully degrades)
- `localStorage` API

---

## 📜 Lisensi
 
Proyek ini dilisensikan di bawah [MIT License](LICENSE). Bebas digunakan, dimodifikasi, dan didistribusikan.

---

## 🙏 Credits

- **Hiragana & Katakana** — Unicode standard
- **Kanji N5** — JLPT official list
- **Fonts** — Google Fonts (Inter, Shippori Mincho, Noto Sans JP)
- **Inspirasi** — Duolingo, Anki, Genshin (aurora theme)

---

<div align="center">

**楽しく学ぼう！** *(Mari belajar dengan menyenangkan!)* 🌸

⭐ Star repo ini kalau bermanfaat.

</div>
