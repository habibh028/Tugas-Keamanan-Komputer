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
   - Scan satu Alamat/IP address:
   <img width="417" alt="Screen Shot 2024-09-17 at 23 27 04" src="https://github.com/user-attachments/assets/6b6ea388-2336-4ee5-99f9-0f4b07ef994b">

   - Melakukan scan port tertentu:
   <img width="409" alt="Screen Shot 2024-09-17 at 23 29 36" src="https://github.com/user-attachments/assets/e00c32d9-26f5-489e-a936-3aeaef3c9664">

   - Scan lebih mendalam (service version):
   <img width="413" alt="Screen Shot 2024-09-17 at 23 31 01" src="https://github.com/user-attachments/assets/18b5d649-ddea-4d41-b98e-06be3dc7f263">

   
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
   <img width="400" alt="Screen Shot 2024-09-18 at 00 00 45" src="https://github.com/user-attachments/assets/0965f0f0-7753-408d-b669-c5340eeb3699">

---

## Perbandingan Singkat

| Tool             | Kelebihan                              | Kekurangan                             | Penggunaan Terbaik                   |
|------------------|----------------------------------------|----------------------------------------|---------------------------------------|
| **Nmap**         | Sangat komprehensif, scripting support  | Sulit bagi pemula, proses lebih lambat | Audit keamanan dan scanning mendalam |
| **Zenmap**       | Antarmuka GUI, visualisasi hasil scan   | Tidak sefleksibel Nmap command-line    | Pengguna yang butuh Nmap dalam GUI   |
| **Angry IP Scan**| Cepat, ringan, dan mudah digunakan     | Fitur terbatas, tidak mendalam         | Scanning cepat di jaringan lokal     |



