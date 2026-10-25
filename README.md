# Analisa Meme Coin Real-Time

Aplikasi web statis untuk menganalisis meme coin secara real-time — dalam **satu file `index.html`**, tanpa server dan tanpa dependensi eksternal.

**Demo online (GitHub Pages):** https://aguse22e.github.io/Analis_coin/

## Fitur

- **Cari token** — tempel alamat kontrak resmi (auto-detect chain: Solana, Ethereum, BSC, Base, Arbitrum, Polygon, Avalanche, Optimism) atau cari nama token.
- **Detail token live** — harga, market cap/FDV, likuiditas, volume 24j, perubahan 5m/1j/6j/24j, pair DEX, link DexScreener / explorer.
- **Keamanan kontrak (GoPlus)** — honeypot, mint, blacklist, pause, pajak beli/jual, owner, terverifikasi; untuk Solana tampilkan mint/freeze authority dan holder.
- **Top-10 holder** — dari data yang tersedia; diberi label jujur jika tidak tersedia lewat API publik, beserta tautan cek manual di Solscan / Etherscan.
- **Skor 5 pilar + vonis** — dengan Rule 1 sebagai gagal-keras; evaluasi Rule 1–8; checklist 12 poin (item otomatis dari data live, item audit/LP-lock/unlock/komunitas ditandai cek manual).
- **Sedang Ramai (Trending)** — DEX Screener boosts + CoinGecko, refresh 60 detik.
- **Pantauan Pasar** — pantau token di watchlist, refresh otomatis tiap 60 detik di halaman, catat perubahan berarti (harga ≥15%, likuiditas menyusut ≥20%, skor berubah ≥10 poin, kesimpulan berubah, volume melonjak). Tampilan natural tanpa label AI/agen/bot, ada tombol "Perbarui sekarang", "Catatan terakhir", dan "Perubahan Terakhir".
- **Saran Migrasi & Arus Whale** — token Solana pump.fun dalam dua kelompok: "Menjelang migrasi" (masih bonding curve, pair pumpfun) dan "Baru migrasi" (sudah ke PumpSwap, umur pair maks. 14 hari). Diperingkat dari dominasi beli 1 jam, rata-rata nilai transaksi 1 jam, volume, plus skor hype. Tiap kartu menampilkan harga, market cap, likuiditas, kedua skor, alasan peringkat, status mint/freeze + holder; klik kartu membuka analisa lengkap. Sinyal whale ini adalah proksi dari data perdagangan DEX, bukan pelacakan wallet tertentu, dan fase migrasi sangat berisiko.
- **Rencana Entry & Exit (Rule 6–8)** — alasan masuk, ukuran posisi, harga entry, TP bertahap +50%/+100%, stop-loss, skenario -30%/-50%, peringatan alokasi; simpan di watchlist dengan harga live.
- **Momentum** — hanya proksi momentum berlabel jelas, BUKAN RSI/MACD asli, plus tautan chart TradingView/DexScreener.

## Peringatan

Meme coin sangat spekulatif, harga bisa turun 50% atau lebih bahkan saat pasar sedang naik. Gunakan hanya dana yang siap hilang 100%. Ini alat analisa, bukan saran beli.

## Cara Pakai

### Online (GitHub Pages)

Buka https://aguse22e.github.io/Analis_coin/

### Lokal

Buka file `index.html` dengan double-click di browser, atau jalankan server statis apa pun di folder ini.

## Data

- Data live dari **DexScreener**, **GoPlus Security**, dan **CoinGecko** — semua fetch langsung dari browser ke API publik, tanpa API key.
- Data watchlist, rencana, dan pantauan tersimpan di **localStorage** browser masing-masing pengguna (key: `meme-coin-analyzer-v1`).
- Jika API gagal atau rate limit, aplikasi menampilkan pesan ramah dan data terakhir yang tersimpan tetap bisa dibaca.
