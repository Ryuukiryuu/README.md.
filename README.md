LATIHAN :

1. Pembuatan List Awal:
```python
A = [15, 27, 35, 43, 50]  # Membuat list A dengan 5 elemen
```
- Ini membuat list A dengan 5 elemen berisi angka

2. Akses List:
```python
print("Element at index 3:", A[3])  # Menampilkan elemen ke-3 (indeks 3)
print("Elements from index 2 to 4:", A[2:4])  # Mengambil elemen dari indeks 2-4
print("Last Element:", A[-1])  # Mengambil elemen terakhir
```
- `A[3]` mengakses elemen ke-4 (ingat indeks dimulai dari 0)
- `A[2:4]` mengambil elemen dari indeks 2 sampai sebelum indeks 4
- `A[-1]` mengambil elemen terakhir dari list

3. Modifikasi List:
```python
A[4] = 100  # Mengubah elemen ke-4 menjadi 100
print("After changing element at index 4:", A)
A[4:] = [100]  # Mengubah dari elemen 4 sampai akhir
print("After changing elements from index 4 to end:", A)
```
- Mengubah nilai elemen pada indeks 4 menjadi 100
- Mengubah elemen dari indeks 4 sampai akhir list

4. Operasi dengan List B:
```python
B = A[:2]  # Mengambil 2 elemen pertama dari A
print("New list B from first 2 elements of A:", B)

B.append("masbro")  # Menambah string ke list B
print("After adding string to B:", B)

B.extend([400, 500, 600])  # Menambah 3 nilai ke list B
print("After adding 3 values to B:", B)
```
- Membuat list B dengan mengambil 2 elemen pertama dari list A
- Menambahkan string "masbro" ke list B menggunakan `append()`
- Menambahkan tiga nilai (400, 500, 600) ke list B menggunakan `extend()`

5. Penggabungan List:
```python
final_list = B + A  # Menggabungkan list B dan A
print("Final combined list:", final_list)
```
- Menggabungkan list B dan A menjadi satu list baru

Output dari kode menunjukkan:
1. List awal A adalah [15, 27, 35, 43, 50]
2. Setelah modifikasi, beberapa nilai berubah
3. List B dibuat dan dimodifikasi dengan penambahan string dan angka
4. Akhirnya kedua list digabungkan menjadi satu list baru

Kode ini mendemonstrasikan operasi-operasi dasar pada list Python seperti:
- Pengaksesan elemen
- Slicing (pengambilan bagian list)
- Modifikasi elemen
- Penambahan elemen baru (append)
- Penambahan multiple elemen (extend)
- Penggabungan list

PRAKTIKUM 5 :
### Penjelasan Kode:
1. **Inisialisasi List Mahasiswa**:
   ```python
   mahasiswa = []
   ```
   List kosong `mahasiswa` digunakan untuk menyimpan data mahasiswa.

2. **Fungsi `hitung_nilai_akhir`**:
   ```python
   def hitung_nilai_akhir(tugas, uts, uas):
       return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
   ```
   Fungsi ini menerima nilai `tugas`, `uts`, dan `uas` sebagai parameter, kemudian mengembalikan nilai akhir berdasarkan bobot:
   - Tugas: 30%
   - UTS: 35%
   - UAS: 35%

3. **Loop Input Data**:
   ```python
   while True:
       # Input data mahasiswa
       nama = input("Masukkan Nama: ")
       nim = input("Masukkan NIM: ")
       tugas = float(input("Nilai Tugas: "))
       uts = float(input("Nilai UTS: "))
       uas = float(input("Nilai UAS: "))
   ```
   Bagian ini menjalankan loop yang meminta pengguna untuk memasukkan data:
   - Nama
   - NIM
   - Nilai Tugas, UTS, dan UAS (dikonversi ke `float`).

4. **Menghitung Nilai Akhir**:
   ```python
   nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
   ```
   Nilai akhir dihitung dengan memanggil fungsi `hitung_nilai_akhir`.

5. **Menyimpan Data ke List**:
   ```python
   data = {
       'nama': nama,
       'nim': nim,
       'tugas': tugas,
       'uts': uts,
       'uas': uas,
       'nilai_akhir': nilai_akhir
   }
   mahasiswa.append(data)
   ```
   Data mahasiswa dimasukkan ke dalam dictionary `data` dan ditambahkan ke dalam list `mahasiswa`.

6. **Tanya untuk Menambah Data Lagi**:
   ```python
   tambah = input("Tambah data (y/t)? ")
   if tambah.lower() != 'y':
       break
   ```
   Program menanyakan apakah pengguna ingin menambahkan data lagi. Jika jawaban bukan `y`, loop akan dihentikan.

7. **Menampilkan Daftar Nilai Mahasiswa**:
   ```python
   print("\nDaftar Nilai Mahasiswa")
   print("=====================================")
   print("Nama         NIM        Tugas  UTS  UAS  Nilai Akhir")
   print("=====================================")
   for mhs in mahasiswa:
       print(f"{mhs['nama']:<12} {mhs['nim']:<10} {mhs['tugas']:<6} {mhs['uts']:<4} {mhs['uas']:<4} {mhs['nilai_akhir']:.2f}")
   print("=====================================")
   ```
   Kode ini mencetak daftar mahasiswa beserta nilai yang telah dimasukkan, menampilkan dalam format tabel.

### Output Program:
- Saat program dijalankan, pengguna diminta memasukkan nama, NIM, dan nilai (tugas, UTS, UAS).
- Program akan menghitung nilai akhir dan menampilkan data mahasiswa.
- Pengguna dapat menambahkan data lebih lanjut atau menghentikan input dengan memilih `t` (tidak).

### Hasil di Terminal:
Bagian sebelah kanan gambar menunjukkan contoh output dari program di mana data mahasiswa dengan nama "wahyu andika" dan NIM `312410182` ditampilkan lengkap dengan nilai tugas, UTS, UAS, dan nilai akhirnya.
