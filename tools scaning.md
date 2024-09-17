# Laporan Perbandingan Tools Scanning di Kali Linux

## 1. Nmap (Network Mapper)

**Nmap** adalah salah satu tool open-source yang sangat populer untuk scanning jaringan dan audit keamanan. Tool ini berbasis command-line, dan dapat digunakan untuk menemukan host, layanan, port, serta informasi versi di jaringan.

### Kelebihan:
- **Komprehensif**: Mampu melakukan scanning mendalam dengan berbagai jenis scan (TCP, UDP, ping, dll.).
- **Kustomisasi Tinggi**: Mendukung scripting dengan Nmap Scripting Engine (NSE).
- **Akurasi Tinggi**: Memberikan informasi yang sangat detail.
- **Cross-Platform**: Tersedia di banyak sistem operasi.

### Kekurangan:
- **Tidak Ramah Pemula**: Memiliki antarmuka command-line yang membutuhkan pemahaman lebih dalam.
- **Lambat**: Karena scanning yang mendalam, waktu pemrosesan bisa lebih lama.

### Cara Menggunakan:
1. **Instalasi Nmap:**
   ```bash
   sudo apt-get install nmap
   ```

2. **Perintah Dasar:**
   - Scan satu IP address:
     ```bash
     nmap 192.168.1.1
     ```
   - Scan seluruh jaringan:
     ```bash
     nmap 192.168.1.0/24
     ```

---

## 2. Zenmap

**Zenmap** adalah antarmuka grafis (GUI) untuk Nmap. Ini memungkinkan pengguna untuk melakukan scan tanpa harus menggunakan command-line.

### Kelebihan:
- **Mudah Digunakan**: GUI memudahkan pengguna dalam melakukan scanning.
- **Visualisasi Data**: Menyediakan grafik untuk memudahkan interpretasi hasil scan.
  
### Kekurangan:
- **Terbatas dalam Kustomisasi**: Tidak sefleksibel menggunakan Nmap secara langsung.
- **Performanya Lebih Lambat**: Penggunaan GUI kadang membuat proses lebih lambat.

### Cara Menggunakan:
1. **Instalasi Zenmap:**
   ```bash
   sudo apt-get install zenmap
   ```

2. **Langkah-Langkah**:
   - Jalankan Zenmap dengan perintah:
     ```bash
     sudo zenmap
     ```
   - Masukkan alamat IP atau range yang ingin di-scan dan pilih profil scan, lalu klik "Scan".

---

## 3. Angry IP Scanner

**Angry IP Scanner** adalah tool scanning jaringan ringan dan cepat. Ini cocok untuk scanning IP address range dan menampilkan informasi dasar.

### Kelebihan:
- **Cepat dan Ringan**: Sangat cepat dan tidak memerlukan banyak sumber daya.
- **Mudah Digunakan**: Antarmuka sangat sederhana.
- **Cross-Platform**: Tersedia untuk berbagai sistem operasi.

### Kekurangan:
- **Fitur Terbatas**: Tidak menyediakan informasi mendalam seperti Nmap.
  
### Cara Menggunakan:
1. **Instalasi Angry IP Scanner:**
   - Unduh dari situs resminya: [Angry IP Scanner](https://angryip.org/download/#linux).
   - Install paket `.deb` dengan perintah:
     ```bash
     sudo dpkg -i ipscan_3.x.x_amd64.deb
     sudo apt-get install -f
     ```

2. **Langkah-Langkah**:
   - Buka aplikasi dengan perintah:
     ```bash
     ipscan
     ```
   - Masukkan range IP, lalu klik "Start" untuk memulai scanning.

---

## Perbandingan Singkat

| Tool             | Kelebihan                              | Kekurangan                             | Penggunaan Terbaik                   |
|------------------|----------------------------------------|----------------------------------------|---------------------------------------|
| **Nmap**         | Sangat komprehensif, scripting support  | Sulit bagi pemula, proses lebih lambat | Audit keamanan dan scanning mendalam |
| **Zenmap**       | Antarmuka GUI, visualisasi hasil scan   | Tidak sefleksibel Nmap command-line    | Pengguna yang butuh Nmap dalam GUI   |
| **Angry IP Scan**| Cepat, ringan, dan mudah digunakan     | Fitur terbatas, tidak mendalam         | Scanning cepat di jaringan lokal     |



