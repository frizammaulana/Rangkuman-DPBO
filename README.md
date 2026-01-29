# RANGKUMAN DPBO

## 📑 Daftar Isi
1. [Basic Java Programming](#basic-java-programming)
2. [Class Diagram (UML)](#class-diagram-uml)
3. [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)

---

## 🔵 BASIC JAVA PROGRAMMING

### 1. Tipe Data Primitif
```java
// Integer Types
byte    b = 100;        // 8-bit  (-128 to 127)
short   s = 10000;      // 16-bit (-32,768 to 32,767)
int     i = 100000;     // 32-bit (-2^31 to 2^31-1)
long    l = 100000L;    // 64-bit (-2^63 to 2^63-1)

// Floating Point
float   f = 10.5f;      // 32-bit
double  d = 10.5;       // 64-bit

// Others
char    c = 'A';        // 16-bit Unicode
boolean bool = true;    // true/false
```

### 2. Variabel & Konstanta
```java
// Deklarasi variabel
int umur;
String nama;
double gaji = 5000000.0;

// Konstanta (final)
final double PI = 3.14159;
final int MAX_VALUE = 100;

// Penamaan konvensi:
// - variabel: camelCase (namaVariabel)
// - konstanta: UPPER_SNAKE_CASE (NAMA_KONSTANTA)
// - class: PascalCase (NamaClass)
```

### 3. Operator

#### Operator Aritmatika
```java
int a = 10, b = 3;
int tambah = a + b;     // 13
int kurang = a - b;     // 7
int kali = a * b;       // 30
int bagi = a / b;       // 3
int modulo = a % b;     // 1
a++;                    // increment (a = 11)
b--;                    // decrement (b = 2)
```

#### Operator Relasional
```java
a > b   // lebih besar
a < b   // lebih kecil
a >= b  // lebih besar sama dengan
a <= b  // lebih kecil sama dengan
a == b  // sama dengan
a != b  // tidak sama dengan
```

#### Operator Kondisional
```java
&& // AND
|| // OR
!  // NOT

if (a > 5 && b < 10) { }  // keduanya harus true
if (a > 5 || b < 10) { }  // salah satu true
if (!(a > 5)) { }         // negasi
```

### 4. Pernyataan Kondisional

#### If-Else
```java
int nilai = 80;

if (nilai >= 90) {
    System.out.println("A");
} else if (nilai >= 80) {
    System.out.println("B");
} else if (nilai >= 70) {
    System.out.println("C");
} else {
    System.out.println("D");
}
```

#### Switch-Case
```java
int hari = 3;
String namaHari;

switch (hari) {
    case 1:
        namaHari = "Senin";
        break;
    case 2:
        namaHari = "Selasa";
        break;
    case 3:
        namaHari = "Rabu";
        break;
    default:
        namaHari = "Invalid";
        break;
}
```

#### Ternary Operator
```java
int nilai = 75;
String status = (nilai >= 70) ? "Lulus" : "Tidak Lulus";
```

### 5. Perulangan

#### For Loop
```java
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}

// Enhanced for (for-each)
int[] angka = {1, 2, 3, 4, 5};
for (int num : angka) {
    System.out.println(num);
}
```

#### While Loop
```java
int i = 0;
while (i < 10) {
    System.out.println(i);
    i++;
}
```

#### Do-While Loop
```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 10);
```

#### Break & Continue
```java
for (int i = 0; i < 10; i++) {
    if (i == 5) break;      // keluar dari loop
    if (i == 3) continue;   // skip iterasi ini
    System.out.println(i);
}
```

### 6. Array

#### Array 1 Dimensi
```java
// Deklarasi
int[] angka = new int[5];
String[] nama = {"Ali", "Budi", "Citra"};

// Akses elemen
angka[0] = 10;
String pertama = nama[0];  // "Ali"

// Length
int panjang = nama.length;  // 3
```

#### Array 2 Dimensi
```java
// Rectangular Array
int[][] matrix = new int[3][4];
matrix[0][0] = 1;

// Inisialisasi langsung
int[][] matrix2 = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Non-Rectangular Array
int[][] jagged = new int[3][];
jagged[0] = new int[2];
jagged[1] = new int[3];
jagged[2] = new int[4];
```

#### Array Bertipe Object
```java
Mahasiswa[] mahasiswa = new Mahasiswa[3];
for (int i = 0; i < mahasiswa.length; i++) {
    mahasiswa[i] = new Mahasiswa();
}
```

### 7. String
```java
String str1 = "Hello";
String str2 = new String("World");

// Concatenation
String gabung = str1 + " " + str2;  // "Hello World"

// Method penting
str1.length();              // panjang string
str1.charAt(0);            // karakter di index 0
str1.substring(0, 3);      // "Hel"
str1.toUpperCase();        // "HELLO"
str1.toLowerCase();        // "hello"
str1.equals(str2);         // perbandingan isi
str1.contains("ell");      // true
str1.replace("H", "Y");    // "Yello"
```

### 8. Input/Output

#### Output
```java
System.out.print("Tanpa newline");
System.out.println("Dengan newline");
System.out.printf("Format: %s, %d, %.2f", "text", 10, 3.14);
```

#### Input (Scanner)
```java
import java.util.Scanner;

Scanner input = new Scanner(System.in);

String nama = input.nextLine();
int umur = input.nextInt();
double gaji = input.nextDouble();

input.close();
```

---

## 🔶 CLASS DIAGRAM (UML)

### 1. Struktur Class Diagram
```
┌─────────────────────┐
│   NamaClass         │  ← Class Name
├─────────────────────┤
│ - atribut1: tipe    │  ← Attributes (Fields)
│ # atribut2: tipe    │
│ + atribut3: tipe    │
├─────────────────────┤
│ + method1(): void   │  ← Methods
│ - method2(): int    │
│ # method3(): String │
└─────────────────────┘
```

### 2. Visibility/Access Modifier
```
+ public       → dapat diakses dari mana saja
- private      → hanya dalam class tersebut
# protected    → dalam class dan subclass
~ package      → dalam package yang sama
```

### 2.1 CARA MENGGAMBAR CLASS DIAGRAM YANG BENAR

#### Langkah-langkah Menggambar Class Diagram:

**STEP 1: Identifikasi Entitas/Class**
```
Cari kata benda (noun) dalam studi kasus
Contoh: Mahasiswa, Dosen, Matakuliah, Buku, Perpustakaan
```

**STEP 2: Tentukan Atribut**
```
Cari properti dari setiap class
Contoh class Mahasiswa:
- nim (String)
- nama (String)
- tanggalLahir (Date)
- ipk (double)
```

**STEP 3: Tentukan Method**
```
Cari aksi/behavior yang bisa dilakukan
Contoh class Mahasiswa:
- daftar()
- ambilMatakuliah()
- hitungIPK()
- tampilkanInfo()
```

**STEP 4: Tentukan Relasi**
```
Cari hubungan antar class:
- Association (punya/has)
- Inheritance (adalah/is-a)
- Aggregation (bagian dari - weak)
- Composition (terdiri dari - strong)
- Dependency (menggunakan)
```

**STEP 5: Tentukan Multiplicity**
```
Berapa banyak objek yang terlibat:
1, 0..1, 1..*, 0..*, *, 2..5
```

#### Contoh Lengkap Class Diagram Mahasiswa:

```
┌─────────────────────────────────┐
│         Mahasiswa               │
├─────────────────────────────────┤
│ - nim: String                   │
│ - nama: String                  │
│ - tanggalLahir: Date            │
│ - alamat: String                │
│ - ipk: double                   │
├─────────────────────────────────┤
│ + Mahasiswa(nim, nama)          │  ← Constructor
│ + setNim(nim: String): void     │
│ + getNim(): String              │
│ + setNama(nama: String): void   │
│ + getNama(): String             │
│ + hitungIPK(): double           │
│ + tampilInfo(): void            │
└─────────────────────────────────┘
```

#### Detail Penulisan Method dalam Class Diagram:

```
Format Method:
[visibility] namaMethod(parameter: tipe): returnType

Contoh:
+ hitungLuas(): double
+ setNama(nama: String): void
+ getNilai(matkul: String): int
- validateData(data: String): boolean
# calculateBonus(gaji: double): double

Constructor (nama sama dengan class):
+ Mahasiswa()
+ Mahasiswa(nim: String, nama: String)

Static method (underline):
+ getTotalMahasiswa(): int
  ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲ ̲
```

#### Cara Menggambar Berbagai Jenis Class:

**1. Class Biasa**
```
┌──────────────────┐
│   Mahasiswa      │
├──────────────────┤
│ - nim: String    │
├──────────────────┤
│ + getNim()       │
└──────────────────┘
```

**2. Abstract Class**
```
┌──────────────────────┐
│   <<abstract>>       │
│   Kendaraan          │  atau tulis nama class italic
├──────────────────────┤
│ # merk: String       │
├──────────────────────┤
│ + bergerak()         │  ← abstract method (italic)
│ + berhenti()         │
└──────────────────────┘
```

**3. Interface**
```
┌──────────────────────┐
│   <<interface>>      │
│   Drawable           │
├──────────────────────┤
│                      │  ← biasanya kosong (no attributes)
├──────────────────────┤
│ + draw(): void       │
│ + resize(): void     │
└──────────────────────┘
```

**4. Enum**
```
┌──────────────────────┐
│     <<enum>>         │
│   StatusMahasiswa    │
├──────────────────────┤
│ AKTIF                │
│ CUTI                 │
│ LULUS                │
│ DROP_OUT             │
└──────────────────────┘
```

### 2.2 CARA TRANSLATE STUDY CASE KE CLASS DIAGRAM

#### 🎯 STUDY CASE 1: Sistem Perpustakaan

**📝 Study Case:**
```
Sebuah perpustakaan memiliki banyak buku. Setiap buku memiliki 
judul, pengarang, ISBN, dan tahun terbit. Perpustakaan juga 
memiliki anggota. Setiap anggota memiliki ID anggota, nama, 
alamat, dan nomor telepon. Seorang anggota dapat meminjam 
beberapa buku. Setiap peminjaman dicatat dengan tanggal pinjam 
dan tanggal kembali.
```

**🔍 STEP 1: Identifikasi Class (kata benda)**
```
Class yang ditemukan:
1. Perpustakaan
2. Buku
3. Anggota
4. Peminjaman
```

**🔍 STEP 2: Identifikasi Atribut**
```
Buku:
- judul (String)
- pengarang (String)
- isbn (String)
- tahunTerbit (int)

Anggota:
- idAnggota (String)
- nama (String)
- alamat (String)
- noTelepon (String)

Peminjaman:
- tanggalPinjam (Date)
- tanggalKembali (Date)
- status (String)
```

**🔍 STEP 3: Identifikasi Method**
```
Buku:
+ getJudul(): String
+ getPengarang(): String
+ tampilInfo(): void

Anggota:
+ pinjamBuku(buku: Buku): void
+ kembalikanBuku(buku: Buku): void
+ tampilInfo(): void

Peminjaman:
+ hitungDenda(): double
+ perpanjang(): void
```

**🔍 STEP 4: Identifikasi Relasi**
```
- Perpustakaan HAS-MANY Buku (Aggregation 1 → 0..*)
- Perpustakaan HAS-MANY Anggota (Aggregation 1 → 0..*)
- Anggota MELAKUKAN-MANY Peminjaman (Association 1 → 0..*)
- Peminjaman UNTUK Buku (Association * → 1)
```

**✅ HASIL CLASS DIAGRAM:**
```
┌──────────────────┐
│  Perpustakaan    │
├──────────────────┤
│ - nama: String   │
│ - alamat: String │
├──────────────────┤
│ + tambahBuku()   │
│ + tambahAnggota()│
└────────┬─────────┘
         │ 1
         │ has
         │
    ┌────┴───┐
    │        │
    │ 0..*   │ 0..*
    ▽        ▽
┌────────┐  ┌────────────┐
│  Buku  │  │  Anggota   │
├────────┤  ├────────────┤
│-judul  │  │-idAnggota  │
│-isbn   │  │-nama       │
├────────┤  ├────────────┤
│+getInfo│  │+pinjamBuku │
└───┬────┘  └─────┬──────┘
    │             │
    │ 1           │ 1
    │             │
    │   ┌─────────┴──────┐
    │   │  Peminjaman    │
    └───┤ ───────────────┤
      * │-tanggalPinjam  │
        │-tanggalKembali │
        ├────────────────┤
        │+hitungDenda()  │
        └────────────────┘
```

#### 🎯 STUDY CASE 2: Sistem Akademik

**📝 Study Case:**
```
Universitas memiliki dosen dan mahasiswa. Dosen mengajar 
mata kuliah, mahasiswa mengambil mata kuliah. Setiap orang 
(dosen dan mahasiswa) memiliki nama, NIK, dan tanggal lahir. 
Dosen memiliki NIP dan gelar, sedangkan mahasiswa memiliki 
NIM dan IPK. Mata kuliah memiliki kode, nama, dan SKS.
```

**🔍 Analisis:**
```
Class:
1. Person (superclass) ← dosen dan mahasiswa = orang
2. Dosen (extends Person)
3. Mahasiswa (extends Person)
4. MataKuliah

Relasi:
- Dosen IS-A Person (Inheritance)
- Mahasiswa IS-A Person (Inheritance)
- Dosen MENGAJAR MataKuliah (Association 1 → 1..*)
- Mahasiswa MENGAMBIL MataKuliah (Association * → *)
```

**✅ HASIL CLASS DIAGRAM:**
```
         ┌─────────────────┐
         │     Person      │ ← Superclass
         ├─────────────────┤
         │ - nama: String  │
         │ - nik: String   │
         │ - tglLahir: Date│
         ├─────────────────┤
         │ + getNama()     │
         └────────△────────┘
                  │
         ┌────────┴────────┐
         │ extends         │ extends
         │                 │
 ┌───────┴────────┐  ┌────┴──────────┐
 │     Dosen      │  │   Mahasiswa   │
 ├────────────────┤  ├───────────────┤
 │ - nip: String  │  │ - nim: String │
 │ - gelar: String│  │ - ipk: double │
 ├────────────────┤  ├───────────────┤
 │ + mengajar()   │  │ + daftar()    │
 └────────┬───────┘  └───────┬───────┘
          │                  │
          │ 1                │ *
          │ mengajar   ambil │
          │                  │
          │      ┌───────────┴────┐
          │      │  MataKuliah    │
          └──────┤ ───────────────┤
             1..*│ - kode: String │
                 │ - nama: String │
                 │ - sks: int     │
                 ├────────────────┤
                 │ + getInfo()    │
                 └────────────────┘
```

#### 🎯 STUDY CASE 3: Sistem E-Commerce

**📝 Study Case:**
```
Sebuah toko online menjual produk. Produk dapat berupa 
Elektronik atau Pakaian. Setiap produk punya nama, harga, 
dan stok. Elektronik punya garansi, Pakaian punya ukuran. 
Customer dapat membuat pesanan yang berisi beberapa produk. 
Setiap pesanan punya status dan total harga.
```

**🔍 Analisis:**
```
Class:
1. Produk (abstract/parent)
2. Elektronik (extends Produk)
3. Pakaian (extends Produk)
4. Customer
5. Pesanan
6. ItemPesanan (class penghubung)

Relasi:
- Elektronik IS-A Produk
- Pakaian IS-A Produk
- Customer HAS-MANY Pesanan (1 → 0..*)
- Pesanan HAS-MANY ItemPesanan (1 → 1..*)
- ItemPesanan FOR Produk (* → 1)
```

**✅ HASIL CLASS DIAGRAM:**
```
        ┌──────────────────────┐
        │   <<abstract>>       │
        │      Produk          │
        ├──────────────────────┤
        │ - id: String         │
        │ - nama: String       │
        │ - harga: double      │
        │ - stok: int          │
        ├──────────────────────┤
        │ + getHarga(): double │
        │ + kurangiStok(): void│
        └──────────△───────────┘
                   │
          ┌────────┴────────┐
          │                 │
 ┌────────┴────────┐  ┌────┴──────────┐
 │   Elektronik    │  │    Pakaian    │
 ├─────────────────┤  ├───────────────┤
 │ - garansi: int  │  │ - ukuran: Str │
 ├─────────────────┤  ├───────────────┤
 │ + getGaransi()  │  │ + getUkuran() │
 └─────────────────┘  └───────────────┘


 ┌──────────────┐         ┌─────────────────┐
 │   Customer   │ 1    0..*│    Pesanan      │
 ├──────────────┤◇─────────├─────────────────┤
 │ - id         │  membuat │ - noPesanan     │
 │ - nama       │          │ - tanggal       │
 │ - email      │          │ - status        │
 ├──────────────┤          ├─────────────────┤
 │ + buatPesanan│          │ + hitungTotal() │
 └──────────────┘          └────────┬────────┘
                                    │ 1
                                    │ berisi
                                    │
                               ┌────┴──────────┐
                               │ ItemPesanan   │ *
                               ├───────────────┤◇───┐
                               │ - jumlah: int │    │
                               │ - subtotal    │    │
                               ├───────────────┤    │ 1
                               │+ hitungSubtot │    │
                               └───────────────┘    │
                                                    │
                                             ┌──────▽──────┐
                                             │   Produk    │
                                             └─────────────┘
```

#### 🎯 STUDY CASE 4: Sistem Parkir

**📝 Study Case:**
```
Sistem parkir untuk kendaraan. Kendaraan bisa motor atau mobil.
Motor bayar Rp2000/jam, Mobil Rp5000/jam. Setiap kendaraan 
punya plat nomor dan waktu masuk. Parkir punya kapasitas 
maksimal dan bisa cek ketersediaan tempat.
```

**🔍 Analisis & Class Diagram:**
```
          ┌──────────────────┐
          │  <<abstract>>    │
          │   Kendaraan      │
          ├──────────────────┤
          │ # platNomor: Str │
          │ # waktuMasuk: Dt │
          ├──────────────────┤
          │ + hitungBiaya()  │ ← abstract method
          │ + getPlat()      │
          └────────△─────────┘
                   │
          ┌────────┴────────┐
          │                 │
  ┌───────┴──────┐  ┌──────┴────────┐
  │    Motor     │  │     Mobil     │
  ├──────────────┤  ├───────────────┤
  │ - TARIF=2000 │  │ - TARIF=5000  │
  ├──────────────┤  ├───────────────┤
  │ +hitungBiaya│  │ +hitungBiaya  │
  └──────────────┘  └───────────────┘


  ┌────────────────────┐
  │      Parkir        │
  ├────────────────────┤
  │ - kapasitas: int   │
  │ - terisi: int      │
  ├────────────────────┤
  │ + masukKendaraan() │
  │ + keluarKendaraan()│
  │ + cekKetersediaan()│
  └──────────┬─────────┘
             │ 1
             │ mengelola
             │
             │ 0..*
             ▽
       ┌────────────┐
       │ Kendaraan  │
       └────────────┘
```

### 2.3 TEKNIK TRANSLATE STUDY CASE - CHECKLIST

#### 📋 Checklist Langkah-langkah:

**✅ 1. Baca Study Case dengan Teliti**
- Highlight kata-kata penting
- Identifikasi entitas utama
- Cari hubungan antar entitas

**✅ 2. Identifikasi Noun (Kata Benda) → CLASS**
```
Kata benda = Class kandidat
Contoh: mahasiswa, buku, dosen, mobil, pesanan
```

**✅ 3. Identifikasi Adjective (Kata Sifat) → ATTRIBUTE**
```
Kata sifat/properti = Atribut
Contoh: nama, warna, harga, jumlah, status
```

**✅ 4. Identifikasi Verb (Kata Kerja) → METHOD**
```
Kata kerja = Method
Contoh: membeli, mengajar, menghitung, menyimpan
```

**✅ 5. Identifikasi Relationship (Hubungan)**
```
Kata hubungan:
- "memiliki" → Association/Aggregation
- "terdiri dari" → Composition
- "adalah" → Inheritance
- "dapat" → Method
```

**✅ 6. Tentukan Multiplicity**
```
Kata petunjuk:
- "satu" → 1
- "banyak/beberapa" → *
- "minimal/maksimal" → range (1..*, 2..5)
```

#### 🎯 STUDY CASE 5: Sistem Rumah Sakit

**📝 Study Case:**
```
Rumah sakit memiliki dokter dan pasien. Dokter memiliki 
spesialisasi. Pasien bisa berobat jalan atau rawat inap.
Setiap kunjungan pasien dicatat dengan diagnosa dan resep obat.
Dokter bisa menangani banyak pasien. Pasien bisa ditangani 
banyak dokter. Kamar rawat inap memiliki nomor, tipe (VIP, 
kelas 1, kelas 2), dan tarif per hari.
```

**🔍 Analisis Lengkap:**

**STEP 1: Identifikasi Class (Noun)**
```
✓ RumahSakit
✓ Dokter
✓ Pasien
✓ PasienRawatJalan (subclass Pasien)
✓ PasienRawatInap (subclass Pasien)
✓ Kunjungan
✓ Kamar
```

**STEP 2: Identifikasi Atribut**
```
Dokter:
- id, nama, spesialisasi, noTelepon

Pasien (parent):
- id, nama, alamat, tanggalLahir

PasienRawatInap (child):
- tanggalMasuk, tanggalKeluar

Kunjungan:
- tanggal, diagnosa, resep

Kamar:
- nomor, tipe, tarifPerHari, status (tersedia/terisi)
```

**STEP 3: Identifikasi Method**
```
Dokter:
+ menanganiPasien()
+ getSpesialisasi()

Pasien:
+ daftar()
+ getInfo()

PasienRawatInap:
+ hitungBiayaKamar()

Kunjungan:
+ tambahDiagnosa()
+ tambahResep()
```

**STEP 4: Identifikasi Relasi & Multiplicity**
```
- Dokter MENANGANI Pasien (* → *)
  → Many-to-Many → butuh class Kunjungan sebagai penghubung
  
- Dokter HAS-MANY Kunjungan (1 → 0..*)
- Pasien HAS-MANY Kunjungan (1 → 0..*)
- PasienRawatInap MENEMPATI Kamar (* → 1)
- PasienRawatJalan IS-A Pasien (inheritance)
- PasienRawatInap IS-A Pasien (inheritance)
```

**✅ HASIL CLASS DIAGRAM:**
```
                    ┌──────────────────┐
                    │     Pasien       │
                    ├──────────────────┤
                    │ - id: String     │
                    │ - nama: String   │
                    │ - alamat: String │
                    ├──────────────────┤
                    │ + daftar()       │
                    │ + getInfo()      │
                    └────────△─────────┘
                             │
                    ┌────────┴────────┐
                    │                 │
        ┌───────────┴────────┐  ┌────┴──────────────┐
        │ PasienRawatJalan   │  │ PasienRawatInap   │
        ├────────────────────┤  ├───────────────────┤
        │                    │  │ - tglMasuk: Date  │
        ├────────────────────┤  │ - tglKeluar: Date │
        │ + getTagihan()     │  ├───────────────────┤
        └────────────────────┘  │ + hitungBiaya()   │
                                └─────────┬─────────┘
                                          │ *
                                          │ menempati
                                          │
                                          │ 1
                                   ┌──────▽──────────┐
                                   │     Kamar       │
                                   ├─────────────────┤
                                   │ - nomor: String │
                                   │ - tipe: String  │
                                   │ - tarif: double │
                                   ├─────────────────┤
                                   │ + getInfo()     │
                                   └─────────────────┘

┌──────────────┐         ┌──────────────┐         ┌──────────────┐
│    Dokter    │ 1    *  │  Kunjungan   │  *   1  │    Pasien    │
├──────────────┤◇────────├──────────────┤─────────├──────────────┤
│ - id         │menangani│ - tanggal    │ditangani│              │
│ - nama       │         │ - diagnosa   │         │              │
│ - spesialis  │         │ - resep      │         │              │
├──────────────┤         ├──────────────┤         │              │
│ + menangani()│         │ + getInfo()  │         │              │
└──────────────┘         └──────────────┘         └──────────────┘
```

#### 🎯 LATIHAN: Translate Study Case Sendiri

**📝 LATIHAN 1: Bank**
```
Bank memiliki nasabah. Nasabah bisa membuka rekening tabungan
atau deposito. Setiap rekening punya nomor rekening, saldo,
dan pemilik. Tabungan bisa diambil kapan saja, deposito tidak
bisa diambil sebelum jatuh tempo. Nasabah bisa transfer, tarik,
dan setor uang.
```

**💡 Hint:**
```
Class: Bank, Nasabah, Rekening (abstract), Tabungan, Deposito
Relasi: Inheritance (Tabungan/Deposito → Rekening)
        Association (Nasabah ←→ Rekening)
```

**📝 LATIHAN 2: Rental Mobil**
```
Perusahaan rental mobil menyewakan berbagai jenis mobil (sedan,
SUV, MPV). Setiap mobil punya plat nomor, warna, dan tarif sewa
per hari. Customer bisa menyewa mobil dengan mencatat tanggal
sewa dan tanggal kembali. Hitung total biaya berdasarkan durasi
dan tarif mobil.
```

**💡 Hint:**
```
Class: RentalMobil, Mobil (parent), Sedan, SUV, MPV, Customer, Transaksi
Relasi: Inheritance, Association
Method: hitungBiaya() di Transaksi
```

### 2.4 TIPS MENGGAMBAR CLASS DIAGRAM

**✅ DO'S:**
1. **Nama Class:** PascalCase, singular (Mahasiswa, bukan Mahasiswas)
2. **Nama Atribut:** camelCase (namaMahasiswa, tanggalLahir)
3. **Nama Method:** camelCase + kata kerja (hitungGaji, setNama)
4. **Tipe Data:** Tulis tipe dengan jelas (String, int, double, Date)
5. **Constructor:** Sama dengan nama class
6. **Getter/Setter:** Tulis jika penting untuk diagram
7. **Abstract:** Gunakan italic atau <<abstract>>
8. **Interface:** Gunakan <<interface>>

**❌ DON'T:**
1. Jangan terlalu detail (tidak perlu semua getter/setter)
2. Jangan lupa visibility modifier
3. Jangan salah relasi (composition vs aggregation)
4. Jangan lupa multiplicity
5. Jangan buat class yang tidak perlu

**🎨 Tools untuk Menggambar:**
- **Online:** draw.io, Lucidchart, PlantUML
- **Desktop:** StarUML, Visual Paradigm, ArgoUML
- **Code-based:** PlantUML (pakai text)

### 2.5 CHEAT SHEET RELASI

```
INHERITANCE (Generalization)
  │
  △     Anak IS-A Parent
  │     Contoh: Mobil is a Kendaraan
  
REALIZATION (Interface)
  ┆
  △     Class implements Interface
  ┆     Contoh: Lingkaran implements Drawable

ASSOCIATION
  ────►  Class uses/has Class
         Contoh: Mahasiswa ambil MataKuliah
         
AGGREGATION (weak has-a)
  ◇───►  Has-a relationship, tapi bisa exist sendiri
         Contoh: Kelas has Students (student bisa pindah kelas)

COMPOSITION (strong has-a)
  ◆───►  Has-a relationship, tidak bisa exist tanpa parent
         Contoh: Rumah has Kamar (kamar tidak exist tanpa rumah)

DEPENDENCY
  ┄┄┄►  Class uses Class temporarily
         Contoh: Class A use Class B as parameter
```

**Contoh Kasus Relasi:**

```
INHERITANCE:
  Animal ← Dog, Cat
  Kendaraan ← Motor, Mobil
  Pegawai ← Manager, Staff

AGGREGATION:
  Universitas ◇──► Mahasiswa (mahasiswa bisa pindah kampus)
  Perusahaan ◇──► Karyawan (karyawan bisa resign)

COMPOSITION:
  Rumah ◆──► Kamar (kamar hancur jika rumah hancur)
  Mobil ◆──► Mesin (mesin tidak berguna tanpa mobil)
  
ASSOCIATION:
  Dokter ──► Pasien
  Mahasiswa ──► MataKuliah
  Customer ──► Produk
```

#### Association (Asosiasi)
```
┌─────────┐              ┌─────────┐
│ Student │ ───────────> │ Course  │
└─────────┘   takes      └─────────┘
```

#### Aggregation (Agregasi) - "has-a" (lemah)
```
┌─────────┐              ┌─────────┐
│ Class   │ ◇───────────>│ Student │
└─────────┘   contains   └─────────┘
```

#### Composition (Komposisi) - "has-a" (kuat)
```
┌─────────┐              ┌─────────┐
│ House   │ ◆───────────>│  Room   │
└─────────┘   composed   └─────────┘
```

#### Inheritance (Pewarisan) - "is-a"
```
┌─────────┐
│ Animal  │
└────△────┘
     │
     │ extends
     │
┌────┴────┐
│   Dog   │
└─────────┘
```

#### Realization/Implementation (Interface)
```
┌──────────────┐
│ <<interface>>│
│   Payable    │
└──────△───────┘
       │
       │ implements
       ┆
┌──────┴───────┐
│   Invoice    │
└──────────────┘
```

### 4. Multiplicity (Kardinalitas)
```
0..1  → nol atau satu
1     → tepat satu
0..*  → nol atau lebih
*     → nol atau lebih (sama dengan 0..*)
1..*  → satu atau lebih
2..5  → dua sampai lima
```

### 5. Abstract Class & Method
```
┌─────────────────────┐
│   <<abstract>>      │
│   Employee          │  ← Abstract class (italic/<<abstract>>)
├─────────────────────┤
│ - name: String      │
├─────────────────────┤
│ + getName(): String │
│ + calculatePay()    │  ← Abstract method (italic)
└─────────────────────┘
```

### 6. Interface
```
┌─────────────────────┐
│   <<interface>>     │
│   Drawable          │
├─────────────────────┤
│ + draw(): void      │
└─────────────────────┘
```

### 7. Contoh Class Diagram Lengkap
```
        ┌──────────────┐
        │   Manusia    │
        ├──────────────┤
        │ - nama       │
        │ - umur       │
        ├──────────────┤
        │ + setNama()  │
        │ + getNama()  │
        └──────△───────┘
               │
        ┌──────┴──────┐
        │             │
  ┌─────┴────┐  ┌────┴─────┐
  │   Pria   │  │  Wanita  │
  └──────────┘  └──────────┘
```

---

## 🔴 OBJECT-ORIENTED PROGRAMMING (OOP)

### 1. Empat Pilar OOP

#### 1.1 ABSTRAKSI
Menyembunyikan detail implementasi dan hanya menampilkan fungsionalitas.
```java
// Contoh abstraksi
abstract class Kendaraan {
    abstract void bergerak();  // method abstrak
}
```

#### 1.2 ENKAPSULASI
Menyembunyikan data dan hanya mengaksesnya melalui method.
```java
public class Mahasiswa {
    // Data hiding
    private String nama;
    private int umur;
    
    // Getter
    public String getNama() {
        return nama;
    }
    
    // Setter
    public void setNama(String nama) {
        this.nama = nama;
    }
}
```

#### 1.3 INHERITANCE (Pewarisan)
Kelas child mewarisi properti dan method dari kelas parent.
```java
// Superclass
class Animal {
    protected String nama;
    
    public void makan() {
        System.out.println("Hewan sedang makan");
    }
}

// Subclass
class Dog extends Animal {
    public void gonggong() {
        System.out.println("Woof woof!");
    }
}
```

#### 1.4 POLYMORPHISM
Kemampuan objek untuk mengambil banyak bentuk.
```java
class Animal {
    public void suara() {
        System.out.println("Hewan bersuara");
    }
}

class Dog extends Animal {
    @Override
    public void suara() {
        System.out.println("Guk guk!");
    }
}

class Cat extends Animal {
    @Override
    public void suara() {
        System.out.println("Meong!");
    }
}
```

### 2. Class & Object

#### Definisi Class
```java
public class Mahasiswa {
    // Atribut/Field
    private String nama;
    private String nim;
    private int umur;
    
    // Constructor
    public Mahasiswa() {
        // default constructor
    }
    
    public Mahasiswa(String nama, String nim) {
        this.nama = nama;
        this.nim = nim;
    }
    
    // Method
    public void belajar() {
        System.out.println(nama + " sedang belajar");
    }
    
    // Getter & Setter
    public String getNama() {
        return nama;
    }
    
    public void setNama(String nama) {
        this.nama = nama;
    }
}
```

#### Membuat Object
```java
// Menggunakan default constructor
Mahasiswa mhs1 = new Mahasiswa();
mhs1.setNama("Ali");

// Menggunakan parameterized constructor
Mahasiswa mhs2 = new Mahasiswa("Budi", "12345");

// Memanggil method
mhs2.belajar();
```

### 3. Constructor

#### Jenis-jenis Constructor
```java
public class Person {
    private String name;
    private int age;
    
    // 1. Default Constructor
    public Person() {
        this.name = "Unknown";
        this.age = 0;
    }
    
    // 2. Parameterized Constructor
    public Person(String name) {
        this.name = name;
        this.age = 0;
    }
    
    // 3. Fully Parameterized Constructor
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

#### Constructor Chaining
```java
public class Book {
    private String title;
    private String author;
    
    public Book() {
        this("Unknown Title", "Unknown Author");
    }
    
    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }
}
```

### 4. Keyword "this"

```java
public class Student {
    private String name;
    
    // Membedakan parameter dan field
    public void setName(String name) {
        this.name = name;  // this.name = field, name = parameter
    }
    
    // Memanggil constructor lain
    public Student() {
        this("Default Name");  // memanggil constructor berparameter
    }
    
    public Student(String name) {
        this.name = name;
    }
    
    // Return object saat ini
    public Student getThis() {
        return this;
    }
}
```

### 5. Keyword "super"

```java
class Employee {
    protected String name;
    
    public Employee(String name) {
        this.name = name;
    }
    
    public void work() {
        System.out.println(name + " is working");
    }
}

class Manager extends Employee {
    private String department;
    
    public Manager(String name, String dept) {
        super(name);  // memanggil constructor parent
        this.department = dept;
    }
    
    @Override
    public void work() {
        super.work();  // memanggil method parent
        System.out.println("Managing " + department);
    }
}
```

### 6. Method Overloading

Method dengan nama sama tapi parameter berbeda.
```java
public class Calculator {
    // Overload berdasarkan jumlah parameter
    public int add(int a, int b) {
        return a + b;
    }
    
    public int add(int a, int b, int c) {
        return a + b + c;
    }
    
    // Overload berdasarkan tipe parameter
    public double add(double a, double b) {
        return a + b;
    }
    
    // Overload berdasarkan urutan parameter
    public String add(String a, int b) {
        return a + b;
    }
    
    public String add(int a, String b) {
        return a + b;
    }
}
```

### 7. Method Overriding

Method di subclass mengganti implementasi method parent.
```java
class Shape {
    public void draw() {
        System.out.println("Drawing shape");
    }
}

class Circle extends Shape {
    @Override
    public void draw() {
        System.out.println("Drawing circle");
    }
}

class Rectangle extends Shape {
    @Override
    public void draw() {
        System.out.println("Drawing rectangle");
    }
}
```

### 8. Access Modifier

```java
public class ModifierExample {
    // PUBLIC - dapat diakses dari mana saja
    public String publicVar = "Public";
    
    // PRIVATE - hanya dalam class ini
    private String privateVar = "Private";
    
    // PROTECTED - class ini, subclass, dan package yang sama
    protected String protectedVar = "Protected";
    
    // DEFAULT (package-private) - hanya dalam package yang sama
    String defaultVar = "Default";
    
    // STATIC - milik class, bukan object
    public static int count = 0;
    
    // FINAL - tidak bisa diubah (konstanta)
    public final double PI = 3.14159;
    
    // STATIC FINAL - konstanta class
    public static final String APP_NAME = "MyApp";
}
```

### 9. Abstract Class

```java
// Abstract class tidak bisa diinstansiasi
abstract class Employee {
    protected String name;
    protected double baseSalary;
    
    public Employee(String name, double baseSalary) {
        this.name = name;
        this.baseSalary = baseSalary;
    }
    
    // Abstract method - wajib diimplementasi di subclass
    public abstract double calculatePay();
    
    // Concrete method - bisa langsung dipakai
    public void displayInfo() {
        System.out.println("Name: " + name);
    }
}

class SalariedEmployee extends Employee {
    public SalariedEmployee(String name, double salary) {
        super(name, salary);
    }
    
    @Override
    public double calculatePay() {
        return baseSalary;
    }
}

class HourlyEmployee extends Employee {
    private int hoursWorked;
    
    public HourlyEmployee(String name, double hourlyRate, int hours) {
        super(name, hourlyRate);
        this.hoursWorked = hours;
    }
    
    @Override
    public double calculatePay() {
        return baseSalary * hoursWorked;
    }
}
```

### 10. Interface

```java
// Interface - kontrak yang harus dipenuhi
interface Drawable {
    // Method abstract (implisit public abstract)
    void draw();
    
    // Default method (Java 8+)
    default void display() {
        System.out.println("Displaying...");
    }
    
    // Static method (Java 8+)
    static void info() {
        System.out.println("Drawable interface");
    }
    
    // Konstanta (implisit public static final)
    int MAX_SIZE = 100;
}

interface Resizable {
    void resize(int width, int height);
}

// Multiple inheritance dengan interface
class Rectangle implements Drawable, Resizable {
    private int width, height;
    
    @Override
    public void draw() {
        System.out.println("Drawing rectangle");
    }
    
    @Override
    public void resize(int w, int h) {
        this.width = w;
        this.height = h;
    }
}
```

### 11. Polymorphism (Lanjutan)

#### Dynamic Binding
```java
Animal animal1 = new Dog();  // Upcasting
Animal animal2 = new Cat();  // Upcasting

animal1.suara();  // Output: Guk guk! (runtime binding)
animal2.suara();  // Output: Meong! (runtime binding)
```

#### Upcasting & Downcasting
```java
// Upcasting (implisit)
Animal animal = new Dog();  // OK

// Downcasting (eksplisit)
Dog dog = (Dog) animal;  // OK
dog.gonggong();

// Runtime error jika salah cast
Cat cat = (Cat) animal;  // ClassCastException!

// Cek tipe sebelum cast
if (animal instanceof Dog) {
    Dog d = (Dog) animal;
    d.gonggong();
}
```

### 12. Package

#### Apa itu Package?
Package adalah cara untuk mengelompokkan class-class yang berkaitan dalam satu folder/direktori. Package membantu:
- **Menghindari konflik nama** class yang sama
- **Mengorganisir** project yang besar
- **Kontrol akses** dengan access modifier
- **Memudahkan maintenance** code

#### Struktur Penamaan Package
```
Konvensi: huruf kecil semua, biasanya reverse domain
Contoh:
- com.telkom.dpbo
- org.apache.commons
- id.ac.telkomuniversity.project
```

#### Cara Membuat Package yang Benar

**Langkah 1: Buat Struktur Folder**
```
MyProject/
├── src/
│   ├── main/
│   │   └── Main.java
│   ├── model/
│   │   ├── Mahasiswa.java
│   │   └── Dosen.java
│   ├── controller/
│   │   └── MahasiswaController.java
│   └── util/
│       └── Helper.java
```

**Langkah 2: Deklarasikan Package di Setiap File**

```java
// File: src/model/Mahasiswa.java
package model;  // ← HARUS baris pertama (sebelum import)

public class Mahasiswa {
    private String nama;
    private String nim;
    
    public Mahasiswa(String nama, String nim) {
        this.nama = nama;
        this.nim = nim;
    }
    
    public String getNama() { return nama; }
    public String getNim() { return nim; }
}
```

```java
// File: src/model/Dosen.java
package model;

public class Dosen {
    private String nama;
    private String nip;
    
    public Dosen(String nama, String nip) {
        this.nama = nama;
        this.nip = nip;
    }
    
    public String getNama() { return nama; }
    public String getNip() { return nip; }
}
```

```java
// File: src/controller/MahasiswaController.java
package controller;

import model.Mahasiswa;  // ← Import class dari package lain

public class MahasiswaController {
    public void tampilkanMahasiswa(Mahasiswa mhs) {
        System.out.println("Nama: " + mhs.getNama());
        System.out.println("NIM: " + mhs.getNim());
    }
}
```

```java
// File: src/main/Main.java
package main;

import model.Mahasiswa;
import model.Dosen;
import controller.MahasiswaController;

public class Main {
    public static void main(String[] args) {
        // Membuat objek
        Mahasiswa mhs = new Mahasiswa("Budi", "12345");
        Dosen dsn = new Dosen("Dr. Ali", "19870001");
        
        // Menggunakan controller
        MahasiswaController ctrl = new MahasiswaController();
        ctrl.tampilkanMahasiswa(mhs);
    }
}
```

#### Cara Import Package

**1. Import Specific Class (Recommended)**
```java
import model.Mahasiswa;
import model.Dosen;
```

**2. Import Semua Class di Package**
```java
import model.*;  // import semua class di package model
```

**3. Import Nested Package**
```java
import com.telkom.dpbo.model.Mahasiswa;
import com.telkom.dpbo.util.*;
```

**4. Fully Qualified Name (Tanpa Import)**
```java
public class Main {
    public static void main(String[] args) {
        // Tanpa import, tulis full path
        model.Mahasiswa mhs = new model.Mahasiswa("Budi", "12345");
        controller.MahasiswaController ctrl = new controller.MahasiswaController();
    }
}
```

#### Package dengan Sub-package

```
MyProject/
├── src/
│   └── com/
│       └── telkom/
│           └── dpbo/
│               ├── Main.java
│               ├── model/
│               │   ├── student/
│               │   │   └── Mahasiswa.java
│               │   └── lecturer/
│               │       └── Dosen.java
│               └── util/
│                   └── Helper.java
```

```java
// File: com/telkom/dpbo/model/student/Mahasiswa.java
package com.telkom.dpbo.model.student;

public class Mahasiswa {
    private String nama;
    // ...
}
```

```java
// File: com/telkom/dpbo/Main.java
package com.telkom.dpbo;

import com.telkom.dpbo.model.student.Mahasiswa;
import com.telkom.dpbo.model.lecturer.Dosen;

public class Main {
    // ...
}
```

#### Compile & Run Program dengan Package

**Di Command Line / Terminal:**

```bash
# Struktur folder:
# MyProject/
# └── src/
#     ├── main/Main.java
#     ├── model/Mahasiswa.java
#     └── controller/MahasiswaController.java

# 1. Masuk ke folder project
cd MyProject/src

# 2. Compile semua file (dari folder src)
javac main/Main.java model/*.java controller/*.java

# Atau compile sekaligus:
javac main/Main.java

# 3. Run program (dari folder src, tanpa ekstensi .java)
java main.Main
```

**Untuk Sub-package:**
```bash
# Compile
javac com/telkom/dpbo/Main.java

# Run
java com.telkom.dpbo.Main
```

#### Di NetBeans / IDE

**Cara Membuat Package di NetBeans:**

1. **Klik kanan pada Source Packages** → New → Java Package
2. **Isi Package Name**: misalnya `model`, `controller`, `view`
3. **Klik Finish**
4. **Klik kanan pada package** → New → Java Class
5. **Buat class** di dalam package tersebut

```
NetBeans akan otomatis:
- Membuat folder sesuai nama package
- Menambahkan "package namapackage;" di baris pertama
- Mengatur classpath dengan benar
```

#### Contoh Project Lengkap dengan Package

```
TokoOnline/
├── src/
│   ├── main/
│   │   └── Main.java
│   ├── model/
│   │   ├── Product.java
│   │   ├── Customer.java
│   │   └── Order.java
│   ├── service/
│   │   ├── ProductService.java
│   │   └── OrderService.java
│   └── util/
│       ├── Validator.java
│       └── Formatter.java
```

**Product.java**
```java
package model;

public class Product {
    private String id;
    private String name;
    private double price;
    
    public Product(String id, String name, double price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }
    
    // Getter & Setter
    public String getId() { return id; }
    public String getName() { return name; }
    public double getPrice() { return price; }
}
```

**ProductService.java**
```java
package service;

import model.Product;
import java.util.ArrayList;

public class ProductService {
    private ArrayList<Product> products = new ArrayList<>();
    
    public void addProduct(Product product) {
        products.add(product);
    }
    
    public void displayProducts() {
        for (Product p : products) {
            System.out.println(p.getName() + ": Rp" + p.getPrice());
        }
    }
}
```

**Validator.java**
```java
package util;

public class Validator {
    public static boolean isValidEmail(String email) {
        return email.contains("@");
    }
    
    public static boolean isValidPrice(double price) {
        return price > 0;
    }
}
```

**Main.java**
```java
package main;

import model.Product;
import service.ProductService;
import util.Validator;

public class Main {
    public static void main(String[] args) {
        // Membuat service
        ProductService ps = new ProductService();
        
        // Membuat produk
        Product p1 = new Product("P001", "Laptop", 5000000);
        Product p2 = new Product("P002", "Mouse", 50000);
        
        // Validasi harga
        if (Validator.isValidPrice(p1.getPrice())) {
            ps.addProduct(p1);
        }
        if (Validator.isValidPrice(p2.getPrice())) {
            ps.addProduct(p2);
        }
        
        // Tampilkan produk
        ps.displayProducts();
    }
}
```

#### Access Modifier dalam Package

```java
// File: model/Mahasiswa.java
package model;

public class Mahasiswa {
    public String nama;        // ✅ Accessible dari mana saja
    protected String nim;      // ✅ Accessible di package & subclass
    String alamat;             // ✅ Accessible hanya di package yang sama
    private double ipk;        // ❌ Hanya accessible di class ini
    
    public void methodPublic() { }      // ✅ Dari mana saja
    protected void methodProtected() { } // ✅ Package & subclass
    void methodDefault() { }             // ✅ Hanya package yang sama
    private void methodPrivate() { }     // ❌ Hanya class ini
}
```

```java
// File: controller/MahasiswaController.java
package controller;

import model.Mahasiswa;

public class MahasiswaController {
    public void test() {
        Mahasiswa mhs = new Mahasiswa();
        
        mhs.nama = "Budi";      // ✅ OK (public)
        mhs.nim = "12345";      // ❌ ERROR (protected, beda package)
        mhs.alamat = "Jakarta"; // ❌ ERROR (default, beda package)
        // mhs.ipk = 3.5;       // ❌ ERROR (private)
        
        mhs.methodPublic();     // ✅ OK
        // mhs.methodProtected(); // ❌ ERROR (beda package)
        // mhs.methodDefault();   // ❌ ERROR (beda package)
        // mhs.methodPrivate();   // ❌ ERROR (private)
    }
}
```

#### Package Built-in Java yang Sering Dipakai

```java
// Otomatis di-import (tidak perlu import)
java.lang.*  // String, Math, System, Integer, dll

// Perlu import
import java.util.*;           // ArrayList, HashMap, Scanner
import java.io.*;             // File, BufferedReader, FileWriter
import java.text.*;           // SimpleDateFormat, NumberFormat
import java.sql.*;            // Connection, Statement, ResultSet
import javax.swing.*;         // JFrame, JButton, JPanel (GUI)
```

#### Contoh Penggunaan Package Built-in

```java
import java.util.ArrayList;
import java.util.Scanner;
import java.text.SimpleDateFormat;
import java.util.Date;

public class Example {
    public static void main(String[] args) {
        // java.util.ArrayList
        ArrayList<String> list = new ArrayList<>();
        list.add("Item 1");
        
        // java.util.Scanner
        Scanner input = new Scanner(System.in);
        String text = input.nextLine();
        
        // java.text.SimpleDateFormat & java.util.Date
        SimpleDateFormat sdf = new SimpleDateFormat("dd-MM-yyyy");
        String tanggal = sdf.format(new Date());
        
        System.out.println(tanggal);
    }
}
```

#### Tips & Best Practices

✅ **DO:**
- Gunakan nama package yang deskriptif (model, controller, view, util)
- Selalu tulis package di baris pertama file
- Gunakan huruf kecil untuk nama package
- Organisir class berdasarkan fungsinya

❌ **DON'T:**
- Jangan gunakan nama package yang bertabrakan dengan built-in (java, javax)
- Jangan taruh banyak class tidak related dalam 1 package
- Jangan lupa deklarasi package di setiap file

#### Troubleshooting Package

**Error: package does not exist**
```
Penyebab: 
- File tidak ada di folder yang sesuai
- Salah nama package
- Tidak compile file yang di-import terlebih dahulu

Solusi:
- Pastikan struktur folder = nama package
- Cek typo di nama package
- Compile semua file yang terkait
```

**Error: class is not public in package**
```
Penyebab: Class yang di-import tidak public

Solusi:
- Pastikan class dideklarasi dengan "public class NamaClass"
```

**Error: cannot find symbol**
```
Penyebab: Lupa import atau salah nama class

Solusi:
- Tambahkan import statement
- Cek nama class sudah benar
```

### 13. Object Class Methods

Semua class di Java mewarisi dari class Object.
```java
public class Person {
    private String name;
    private int age;
    
    // Override toString()
    @Override
    public String toString() {
        return "Person[name=" + name + ", age=" + age + "]";
    }
    
    // Override equals()
    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (obj == null || getClass() != obj.getClass()) return false;
        Person person = (Person) obj;
        return age == person.age && 
               name.equals(person.name);
    }
    
    // Override hashCode()
    @Override
    public int hashCode() {
        return Objects.hash(name, age);
    }
}
```

### 14. Collection Framework

#### ArrayList
```java
import java.util.ArrayList;

ArrayList<String> list = new ArrayList<>();

// Menambah element
list.add("Apple");
list.add("Banana");
list.add(0, "Mango");  // insert di index 0

// Akses element
String item = list.get(0);

// Ubah element
list.set(1, "Orange");

// Hapus element
list.remove(2);
list.remove("Apple");

// Size
int size = list.size();

// Loop
for (String fruit : list) {
    System.out.println(fruit);
}

// Lambda
list.forEach(fruit -> System.out.println(fruit));
```

#### HashMap
```java
import java.util.HashMap;

HashMap<Integer, String> map = new HashMap<>();

// Menambah pasangan key-value
map.put(101, "Alice");
map.put(102, "Bob");
map.put(103, "Charlie");

// Akses value
String name = map.get(102);  // "Bob"

// Cek key/value
boolean hasKey = map.containsKey(101);
boolean hasValue = map.containsValue("Alice");

// Hapus
map.remove(101);

// Size
int size = map.size();

// Loop through keys
for (Integer id : map.keySet()) {
    System.out.println(id + ": " + map.get(id));
}

// Loop through values
for (String value : map.values()) {
    System.out.println(value);
}

// Loop through entries
for (HashMap.Entry<Integer, String> entry : map.entrySet()) {
    System.out.println(entry.getKey() + ": " + entry.getValue());
}
```

---

## 📝 TIPS PERSIAPAN TES

### Teori
1. **Pahami konsep 4 pilar OOP** (Abstraksi, Enkapsulasi, Inheritance, Polymorphism)
2. **Kuasai access modifier** (public, private, protected, default)
3. **Pahami perbedaan**:
   - Class vs Object
   - Overloading vs Overriding
   - Abstract Class vs Interface
   - Upcasting vs Downcasting
4. **Hapal UML notation** (visibility, relasi, multiplicity)

### Praktikum
1. **Latihan coding**:
   - Buat class sederhana dengan constructor, getter/setter
   - Implementasi inheritance (1 parent, 2+ child)
   - Buat abstract class atau interface
   - Gunakan ArrayList/HashMap
2. **Debugging**: Latih membaca error dan memperbaiki code
3. **Speed coding**: Latih menulis code dengan cepat tapi benar

### Hal yang Sering Ditanyakan
1. Jelaskan perbedaan overloading dan overriding
2. Kapan menggunakan abstract class vs interface?
3. Apa itu polymorphism? Berikan contoh
4. Buat class diagram dari soal cerita
5. Implementasi inheritance dengan 3 level
6. Bedakan composition dan aggregation
7. Jelaskan keyword this dan super
8. Apa fungsi constructor?

---

## 🎯 CONTOH SOAL & JAWABAN

### Soal 1: Buat Class Sederhana
**Soal**: Buat class Mahasiswa dengan atribut nama, nim, dan ipk. Buat getter/setter dan method tampilInfo().

**Jawaban**:
```java
public class Mahasiswa {
    private String nama;
    private String nim;
    private double ipk;
    
    public Mahasiswa(String nama, String nim, double ipk) {
        this.nama = nama;
        this.nim = nim;
        this.ipk = ipk;
    }
    
    public String getNama() { return nama; }
    public void setNama(String nama) { this.nama = nama; }
    
    public String getNim() { return nim; }
    public void setNim(String nim) { this.nim = nim; }
    
    public double getIpk() { return ipk; }
    public void setIpk(double ipk) { this.ipk = ipk; }
    
    public void tampilInfo() {
        System.out.println("Nama: " + nama);
        System.out.println("NIM: " + nim);
        System.out.println("IPK: " + ipk);
    }
}
```

### Soal 2: Inheritance
**Soal**: Buat class Kendaraan (parent) dengan atribut merk dan method bergerak(). Buat class Motor dan Mobil sebagai child dengan method tambahan.

**Jawaban**:
```java
// Parent class
class Kendaraan {
    protected String merk;
    
    public Kendaraan(String merk) {
        this.merk = merk;
    }
    
    public void bergerak() {
        System.out.println(merk + " sedang bergerak");
    }
}

// Child class 1
class Motor extends Kendaraan {
    private int cc;
    
    public Motor(String merk, int cc) {
        super(merk);
        this.cc = cc;
    }
    
    public void wheelie() {
        System.out.println("Motor melakukan wheelie!");
    }
}

// Child class 2
class Mobil extends Kendaraan {
    private int pintu;
    
    public Mobil(String merk, int pintu) {
        super(merk);
        this.pintu = pintu;
    }
    
    public void bukaPintu() {
        System.out.println("Membuka " + pintu + " pintu");
    }
}
```

### Soal 3: Polymorphism
**Soal**: Demonstrasikan polymorphism dengan class Shape dan turunannya.

**Jawaban**:
```java
abstract class Shape {
    protected String color;
    
    public Shape(String color) {
        this.color = color;
    }
    
    public abstract double hitungLuas();
    
    public void displayColor() {
        System.out.println("Warna: " + color);
    }
}

class Circle extends Shape {
    private double radius;
    
    public Circle(String color, double radius) {
        super(color);
        this.radius = radius;
    }
    
    @Override
    public double hitungLuas() {
        return Math.PI * radius * radius;
    }
}

class Rectangle extends Shape {
    private double panjang, lebar;
    
    public Rectangle(String color, double p, double l) {
        super(color);
        this.panjang = p;
        this.lebar = l;
    }
    
    @Override
    public double hitungLuas() {
        return panjang * lebar;
    }
}

// Penggunaan polymorphism
public class Main {
    public static void main(String[] args) {
        Shape s1 = new Circle("Merah", 5);
        Shape s2 = new Rectangle("Biru", 4, 6);
        
        // Polymorphic behavior
        System.out.println("Luas lingkaran: " + s1.hitungLuas());
        System.out.println("Luas persegi: " + s2.hitungLuas());
    }
}
```

---

## ⚡ QUICK REFERENCE

### Reserved Keywords Java
```
abstract    continue    for          new         switch
assert      default     goto*        package     synchronized
boolean     do          if           private     this
break       double      implements   protected   throw
byte        else        import       public      throws
case        enum        instanceof   return      transient
catch       extends     int          short       try
char        final       interface    static      void
class       finally     long         strictfp    volatile
const*      float       native       super       while
```
*tidak digunakan

### Naming Conventions
- **Class**: PascalCase (Mahasiswa, KendaraanBermotor)
- **Method**: camelCase (hitungLuas, getNama)
- **Variable**: camelCase (namaMahasiswa, totalHarga)
- **Constant**: UPPER_SNAKE_CASE (MAX_VALUE, PI)
- **Package**: lowercase (com.example.myapp)

### Common Exceptions
```java
NullPointerException        // object null
ArrayIndexOutOfBoundsException  // index array invalid
ClassCastException          // casting salah
NumberFormatException       // konversi string ke number gagal
IllegalArgumentException    // argumen invalid
```

---

## 🚀 Semoga Sukses!

**Tips Terakhir**:
1. Baca soal dengan teliti
2. Pikirkan class diagram terlebih dahulu
3. Tulis code yang clean dan rapi
4. Comment code jika perlu
5. Test code sebelum submit
6. Jangan panik, tetap tenang!

**Good luck dengan tes asisten praktikum DPBO! 💪**
