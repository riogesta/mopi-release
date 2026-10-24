# MockAPI Studio (Standalone Binary Release)

Repository ini berisi rilis binary standalone **MockAPI Studio (`mopi`)** untuk Linux x64. Tidak memerlukan instalasi Node.js, Bun, atau `node_modules`.

---

## 🚀 Cara Instalasi & Menjalankan

### 1. Buat folder `mopi` dan masuk ke dalamnya
```bash
mkdir -p mopi && cd mopi
```

### 2. Download binary `mopi` versi terbaru via `curl`
```bash
curl -fL https://github.com/riogesta/mopi-release/releases/latest/download/mopi -o mopi && chmod +x mopi
```

### 3. Jalankan aplikasi
```bash
./mopi
```
Secara default server berjalan di port **`3000`** (`http://localhost:3000`) dan otomatis membuat folder `./data/` untuk menyimpan database SQLite (`data/mockapi.db`) serta spesifikasi OpenAPI YAML (`data/workspaces/`).

---

## ⚙️ Konfigurasi Port (Opsional)

Jika ingin menjalankan di port lain (misalnya port `8002`):
```bash
PORT=8002 ./mopi
```

---

## 🔄 Cara Update ke Versi Terbaru

Masuk ke dalam folder `mopi`, hentikan proses yang sedang berjalan, lalu jalankan kembali perintah `curl` di atas:
```bash
curl -fL https://github.com/riogesta/mopi-release/releases/latest/download/mopi -o mopi && chmod +x mopi
```
*(Data database dan workspace di dalam folder `./data/` tetap aman dan tidak akan terhapus saat binary di-update).*