# laporan praktikum 6 

## Tugas Praktikum

Buat program sederhana dengan mengaplikasikan penggunaan fungsi yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan:

* Fungsi tambah() untuk menambah data

* Fungsi täpilkan() untuk menampilkan data

* Fungsi hapus(nama) untuk menghapus data berdasarkan nama

* Fungsi ubah(nama) untuk mengubah data berdasarkan nama

Buat flowchart dan penjelasan programnya pada README.md.

* Commit dan push repository ke github.

# kode program 

``` python
# Program manajemen data mahasiswa
data_mahasiswa = {}

# Fungsi untuk menambah data mahasiswa
def tambah(nama, nilai):
    if nama in data_mahasiswa:
        print(f"Mahasiswa dengan nama {nama} sudah ada.")
    else:
        data_mahasiswa[nama] = nilai
        print(f"Data mahasiswa {nama} berhasil ditambahkan.")

# Fungsi untuk menampilkan seluruh data mahasiswa
def tampilkan():
    if not data_mahasiswa:
        print("Tidak ada data mahasiswa.")
    else:
        print("\nDaftar Nilai Mahasiswa:")
        for nama, nilai in data_mahasiswa.items():
            print(f"- Nama: {nama}, Nilai: {nilai}")
        print()

# Fungsi untuk menghapus data mahasiswa berdasarkan nama
def hapus(nama):
    if nama in data_mahasiswa:
        del data_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

# Fungsi untuk mengubah data mahasiswa berdasarkan nama
def ubah(nama, nilai_baru):
    if nama in data_mahasiswa:
        data_mahasiswa[nama] = nilai_baru
        print(f"Data mahasiswa {nama} berhasil diubah.")
    else:
        print(f"Data mahasiswa dengan nama {nama} tidak ditemukan.")

# Program utama
while True:
    print("\nMenu:")
    print("1. Tambah Data Mahasiswa")
    print("2. Tampilkan Data Mahasiswa")
    print("3. Hapus Data Mahasiswa")
    print("4. Ubah Data Mahasiswa")
    print("5. Keluar")

    pilihan = input("Pilih menu (1/2/3/4/5): ")

    if pilihan == "1":
        nama = input("Masukkan nama mahasiswa: ")
        nilai = input("Masukkan nilai mahasiswa: ")
        tambah(nama, nilai)
    elif pilihan == "2":
        tampilkan()
    elif pilihan == "3":
        nama = input("Masukkan nama mahasiswa yang akan dihapus: ")
        hapus(nama)
    elif pilihan == "4":
        nama = input("Masukkan nama mahasiswa yang akan diubah: ")
        nilai_baru = input("Masukkan nilai baru: ")
        ubah(nama, nilai_baru)
    elif pilihan == "5":
        print("Terima kasih! Program selesai.")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
```
## output kode
``` python
Menu:
1. Tambah Data Mahasiswa
2. Tampilkan Data Mahasiswa
3. Hapus Data Mahasiswa
4. Ubah Data Mahasiswa
5. Keluar
Pilih menu (1/2/3/4/5): 
```
## penjelasan kode 

Struktur Data:

Menggunakan dictionary (data_mahasiswa) untuk menyimpan data, di mana nama adalah key dan nilai adalah value.
Fungsi tambah(nama, nilai):

Mengecek apakah nama sudah ada dalam data.
Jika belum ada, data akan ditambahkan.
Jika sudah ada, akan memberi pesan bahwa nama tersebut sudah ada.
Fungsi tampilkan():

Menampilkan semua nama dan nilai dari dictionary.
Jika data kosong, akan memberi pesan bahwa tidak ada data.
Fungsi hapus(nama):

Mencari nama di dictionary.
Jika ditemukan, data akan dihapus.
Jika tidak ditemukan, menampilkan pesan kesalahan.
Fungsi ubah(nama, nilai_baru):

Mencari nama di dictionary.
Jika ditemukan, akan mengganti nilai lama dengan nilai baru.
Jika tidak ditemukan, akan memberi pesan kesalahan.
Menu Utama:

Menggunakan loop untuk memberikan opsi interaktif kepada pengguna.
Opsi mencakup tambah, tampilkan, hapus, ubah, atau keluar dari program.

## flowchart
![flowchartprak6](https://github.com/user-attachments/assets/58fb2363-5a4f-4e11-9f41-825185cfd250)
