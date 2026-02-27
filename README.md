# Deteksi IP Address

## 📋 Deskripsi Project

Project ini adalah aplikasi Java untuk **mendeteksi dan menganalisis IP Address** dari sebuah domain/URL. Program akan mengidentifikasi:
- **IP Address** dari domain yang diinput
- **Kelas IP** (A, B, C, D Multicast, E Eksperimental, atau Loopback)
- **Net ID dan Host ID** berdasarkan kelas IP tersebut
- **Konversi Biner** dari masing-masing oktet IP address

Project ini terdiri dari 2 file Java:
- **main.java** - File utama (entry point)
- **tugas1.java** - Program utama untuk deteksi dan analisis IP address

---

## 🚀 Cara Menjalankan Project

### Prerequisites
- Java Development Kit (JDK) sudah terinstall di sistem Anda
- Minimal Java 8 ke atas

### Langkah-langkah Running:

#### 1. **Compile kedua file Java:**
```bash
javac main.java tugas1.java
```

#### 2. **Jalankan program dengan salah satu cara:**

**Opsi A - Jalankan file main.java:**
```bash
java main
```
(Output: Hanya menampilkan hello message dan loop sederhana)

**Opsi B - Jalankan file tugas1.java (REKOMENDASI):**
```bash
java tugas1
```

### 3. **Cara Menggunakan Program:**

Setelah menjalankan `java tugas1`, ikuti langkah berikut:

```
Masukkan URL : google.com
```

Program akan menampilkan hasil analisis:
```
--- Hasil Deteksi ---
URL        : google.com
IP Address : 142.250.xxx.xxx
Class IP   : C

--- Net ID & Host ID ---
Net ID  : 142.250.xxx
Host ID : xxx

Konversi Biner per Oktet:
142 -> 10001110
250 -> 11111010
xxx -> xxxxxxxx
xxx -> xxxxxxxx
```

---

## 🔗 Hubungan main.java dan tugas1.java

- **main.java** adalah file pemula/template yang sederhana
- **tugas1.java** adalah program utama yang memiliki fungsionalitas lengkap untuk deteksi IP
- Keduanya adalah program **independent** - tidak ada dependency satu sama lain
- Kedua file dapat dikompilasi dan dijalankan secara terpisah
- Untuk menggunakan fitur lengkap deteksi IP, jalankan **tugas1.java**

---

## 📝 Contoh Input & Output

### Contoh 1: Domain (google.com)
```
Input:  google.com
Output: Menampilkan IP, Kelas, Net ID, Host ID, dan konversi biner
```

### Contoh 2: Domain Lokal (localhost)
```
Input:  localhost
Output: Class IP: Loopback (khusus)
        IP Address: 127.0.0.1
```

### Contoh 3: URL Tidak Valid
```
Input:  domain-tidak-ada-xxx.com
Output: Domain tidak valid atau IP tidak dapat ditemukan.
```

---

## 💡 Penjelasan Kelas IP

| Kelas | Range Oktet 1 | Tujuan |
|-------|---|---|
| **A** | 1 - 126 | Jaringan besar |
| **B** | 128 - 191 | Jaringan menengah |
| **C** | 192 - 223 | Jaringan kecil |
| **D** | 224 - 239 | Multicast |
| **E** | 240 - 255 | Eksperimental |
| **Loopback** | 127 | Testing/Internal |

---

## 📌 Catatan

- Program memerlukan koneksi internet untuk mengakses domain eksternal
- Input berupa URL/domain akan dikonversi menjadi IP address menggunakan `InetAddress`
- Semua proses dalam satu program tanpa memerlukan library tambahan
