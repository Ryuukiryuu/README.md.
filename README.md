Kode Python pada gambar tersebut adalah program sederhana untuk input data mahasiswa dan menghitung nilai akhir berdasarkan bobot nilai tugas, UTS, dan UAS. Berikut penjelasan kode tersebut:

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
