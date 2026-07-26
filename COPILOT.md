# Panduan Pemasangan dan Penggunaan GitHub Copilot

## 📋 Daftar Isi
1. [Pengenalan](#pengenalan)
2. [Keperluan Sistem](#keperluan-sistem)
3. [Pemasangan](#pemasangan)
4. [Konfigurasi Awal](#konfigurasi-awal)
5. [Menggunakan Copilot](#menggunakan-copilot)
6. [Tip dan Trik](#tip-dan-trik)
7. [Penyelesaian Masalah](#penyelesaian-masalah)

---

## Pengenalan

GitHub Copilot adalah alat kecerdasan buatan yang membantu anda menulis kod dengan lebih cepat dan efisien. Ia menyediakan cadangan kod berdasarkan konteks yang anda tulis dalam editor anda.

**Faedah utama:**
- ⚡ Tulis kod lebih pantas
- 🧠 Cadangan cerdas berdasarkan konteks
- 📚 Belajar dari contoh kod berkualiti
- 🔄 Terjemahan dan penjelasan kod

---

## Keperluan Sistem

### Untuk VS Code on Windows

**Keperluan Minimum:**
- Windows 10/11
- VS Code versi 1.80.0 atau lebih baru
- Sambungan internet yang stabil
- Akaun GitHub dengan langganan Copilot aktif

**Spesifikasi Komputer:**
- RAM: Sekurang-kurangnya 4GB (disyorkan 8GB)
- Ruang Penyimpanan: 500MB ruang bebas untuk VS Code dan sambungan
- Pemprosesor: Intel/AMD prosesor moden

---

## Pemasangan

### Langkah 1: Pasang Sambungan Copilot di VS Code

1. Buka **VS Code**
2. Pergi ke **Extensions** (Ctrl+Shift+X)
3. Cari "GitHub Copilot"
4. Klik **Install** pada sambungan yang dikeluarkan oleh GitHub

```
Sambungan Resmi: GitHub Copilot (ID: GitHub.copilot)
```

### Langkah 2: Log Masuk dengan Akaun GitHub

1. Selepas pemasangan, VS Code akan meminta anda untuk log masuk
2. Klik **"Sign in to use GitHub Copilot"**
3. Pilih **"Sign in with GitHub"** di browser yang terbuka
4. Masukkan username dan password GitHub anda
5. Berikan kebenaran akses jika diminta
6. Kembali ke VS Code - anda sudah siap!

### Langkah 3: Sahkan Pemasangan

- Anda sepatutnya melihat ikon Copilot (🚀) di sudut kanan bawah VS Code
- Status harus menunjukkan "Ready" atau ikon hijau

---

## Konfigurasi Awal

### Tetapan Asas

1. Buka **File > Preferences > Settings** (atau tekan Ctrl+,)
2. Cari "Copilot" dalam kotak pencarian
3. Tetapan penting:
   - ✅ **Enable Copilot**: Pastikan ini dihidupkan
   - ✅ **Kebolehongsian**: Pilih sama ada cadangan timbul secara automatik atau atas permintaan

### Pintasan Keyboard Berguna

| Pintasan | Fungsi |
|----------|--------|
| `Alt+\` | Terima cadangan Copilot |
| `Tab` | Terima cadangan (default) |
| `Escape` | Tolak cadangan |
| `Alt+]` | Cadangan seterusnya |
| `Alt+[` | Cadangan sebelumnya |
| `Ctrl+Enter` | Buka panel cadangan berbilang |

---

## Menggunakan Copilot

### Cara Asas Menggunakan Copilot

#### 1. Cadangan Kod Automatik
```python
# Copilot akan mencadangkan melengkapkan kod
def calculate_sum(numbers):
    # Copilot cadangan: return sum(numbers)
```

Ketik kod anda dan Copilot akan menunjukkan cadangan kelabu. Tekan `Tab` untuk menerimanya.

#### 2. Menulis Dengan Ulasan (Comments)
```javascript
// Ulasan memberikan konteks kepada Copilot
// Fungsi untuk mengira purata lima nombor terbaik
function calculateTopAverage(scores) {
    // Copilot akan mencadangkan pelaksanaan
}
```

#### 3. Permintaan Copilot Chat
Tekan `Ctrl+Shift+I` (atau `Cmd+Shift+I` di macOS) untuk membuka **Copilot Chat** dan bertanya soalan:

```
Contoh pertanyaan:
- "Bagaimana cara membuat fungsi untuk memeriksa palindrom?"
- "Jelaskan kod ini dalam Bahasa Melayu"
- "Tulis unit test untuk fungsi ini"
```

---

## Tip dan Trik

### 💡 Tip 1: Gunakan Ulasan Deskriptif
Semakin jelas ulasan anda, semakin baik cadangan Copilot:

```python
# ❌ Kurang jelas
# fungsi pemprosesan

# ✅ Lebih jelas
# Fungsi untuk memproses senarai produk dan mengira jumlah harga dengan cukai 10%
def process_products(products):
    pass
```

### 💡 Tip 2: Konteks Adalah Penting
Buka fail yang berkaitan agar Copilot faham konteks:
- Buka fail model data sebelum menulis fungsi
- Buka API documentation jika membuat panggilan API

### 💡 Tip 3: Gunakan Chat untuk Penerangan
```
Pertanyaan: "Jelaskan bagaimana algoritma quicksort berfungsi"
Jawapan: Copilot akan memberikan penjelasan langkah demi langkah
```

### 💡 Tip 4: Semak Cadangan Sebelum Terima
Jangan terima cadangan tanpa menyemak:
- Pastikan sintaks betul
- Pastikan logik sesuai dengan keperluan anda
- Pastikan tiada kelemahan keselamatan

### 💡 Tip 5: Gunakan untuk Dokumentasi
```python
def calculate_fibonacci(n: int) -> int:
    """
    Copilot boleh melengkapkan dokumentasi docstring untuk anda
    """
```

---

## Penyelesaian Masalah

### ❌ Masalah: Copilot tidak menunjukkan cadangan

**Penyelesaian:**
1. Sahkan anda sudah log masuk (lihat ikon di sudut kanan bawah)
2. Periksa sambungan internet anda
3. Mula semula VS Code: `Ctrl+Shift+P` → ketik "Reload Window"
4. Periksa status Copilot di output: `View > Output` → pilih "GitHub Copilot"

### ❌ Masalah: "Copilot is not available for this repository"

**Penyelesaian:**
- Ini berlaku jika repositori terlalu besar atau tidak disokong
- Coba tambah repositori ke whitelist dalam tetapan
- Atau gunakan Copilot di fail individu yang tidak berkaitan dengan repositori

### ❌ Masalah: Cadangan yang tidak relevan atau salah

**Penyelesaian:**
1. Tolak cadangan (tekan `Escape`)
2. Tuliskan ulasan yang lebih spesifik dan jelas
3. Berikan lebih banyak konteks dalam kod
4. Gunakan Copilot Chat untuk bertanya secara langsung

### ❌ Masalah: Lambat atau terputus

**Penyelesaian:**
1. Periksa sambungan internet - pastikan stabil
2. Baca semula VS Code
3. Kurangkan bilangan fail terbuka secara serentak
4. Hubungi sokongan GitHub jika masalah berterusan

---

## Sumber Tambahan

- 📖 [Dokumentasi Rasmi GitHub Copilot](https://docs.github.com/en/copilot)
- 🎓 [Tutorial GitHub Copilot](https://github.blog/2023-06-20-how-to-write-better-prompts-for-github-copilot/)
- 💬 [GitHub Copilot Community](https://github.com/github-copilot/chat)
- 🔐 [Polisi Privasi Copilot](https://docs.github.com/en/site-policy/privacy-policies/github-copilot-for-individuals-privacy-statement)

---

## Catatan Penting

⚠️ **Keselamatan dan Etika:**
- Jangan gunakan Copilot untuk menghasilkan kod yang melanggar hak cipta
- Sentiasa semak kod yang dijana sebelum menggunakannya dalam pengeluaran
- Jangan log masuk dengan akaun organisasi di komputer awam
- Hormat privasi dan keselamatan data semasa menggunakan Copilot

---

**Versi**: 1.0  
**Terakhir dikemas kini**: Julai 2026  
**Dioptimumkan untuk**: VS Code on Windows  
**Bahasa**: Bahasa Melayu
