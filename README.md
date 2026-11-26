# Remike Analytics — Dashboard Game Roblox

**Demo live:** https://kirax-12.github.io/roblox-analytics/

Dashboard analytics game Roblox (front-end) dengan tema gelap profesional, dibangun sebagai
satu file HTML mandiri. Semua data adalah **data contoh** yang digenerate secara deterministik
di sisi klien — tidak ada backend dan tidak ada panggilan API.

**File:** `index.html` (±43 KB, CSS + JS inline, tanpa library chart — semua grafik digambar
manual dengan `<canvas>`).

## Cara membuka

Buka `index.html` langsung di browser, atau sajikan lewat server statis apa pun
(mis. `python3 -m http.server` di folder ini). Satu-satunya dependensi eksternal adalah
Google Fonts (Space Grotesk + Space Mono); tanpa internet, font jatuh ke fallback sistem.

## Game yang ditampilkan

| Game | Total Visits | Rating |
|---|---|---|
| Fishing Adventure | 155.000 | 88% |
| Mount Nyong | 156.000 | 87% |
| Obby Tower Fun | 48.500 | 91% |
| Tycoon Kota Mini | 23.700 | 84% |

## Fitur

- **4 tampilan dari sidebar**
  - *Ringkasan* — 4 kartu statistik (Total Visits, Rata-rata CCU, Robux Earned, Retention D1)
    dengan animasi count-up, chart area visits per hari, dan tabel ringkas.
  - *Game Saya* — tabel lengkap semua game (visits semua waktu & rentang, rating, CCU live,
    Robux, retention D1).
  - *Pendapatan* — total Robux, rata-rata harian, estimasi DevEx (kurs contoh
    US$0,0038/Robux), bar chart Robux per minggu, dan peringkat pendapatan per game.
  - *Pemain* — chart CCU per jam (pola 24 jam, puncak malam hari), kartu retention
    D1/D7/D30 dengan progress bar, CCU puncak, dan durasi sesi rata-rata.
- **Kontrol global** — dropdown pilih game (termasuk "Semua Game") + tombol rentang
  7 / 30 / 90 hari. Mengganti salah satunya memperbarui semua kartu, chart, dan tabel.
- **Tooltip hover di semua chart** — garis vertikal putus-putus, titik penanda, dan kotak
  berisi tanggal/jam + nilai.
- **Tabel interaktif** — klik baris game di tabel mana pun untuk menjadikan game itu fokus
  seluruh dashboard.
- **Data deterministik** — generator pseudo-random ter-seed dari nama game (hash FNV-1a +
  mulberry32), jadi angka konsisten di setiap render. Ada tren naik/turun ringan per game
  dan pola weekend ±32% lebih ramai.
- **Responsif** — sidebar menyusut menjadi baris navigasi di atas pada layar ≤760px,
  grid kartu menyesuaikan di tablet.

## Catatan

Dashboard konsep oleh **Remike Dev** — data contoh untuk keperluan portofolio/demo,
bukan data asli dari Roblox Creator Hub.
