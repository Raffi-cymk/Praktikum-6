# Praktikum-6

![](<Program Manajemen Nilai.jpeg>)

# List untuk menyimpan data mahasiswa
mahasiswa = []

# Fungsi untuk menambah data mahasiswa
def tambah(nama, nilai):
    mahasiswa.append({'nama': nama, 'nilai': nilai})
    print(f"Data {nama} berhasil ditambahkan.")

# Fungsi untuk menampilkan semua data mahasiswa
def tampilkan():
    if not mahasiswa:
        print("Tidak ada data mahasiswa.")
    else:
        print("Daftar Nilai Mahasiswa:")
        for i, mhs in enumerate(mahasiswa, start=1):
            print(f"{i}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")

# Fungsi untuk menghapus data mahasiswa berdasarkan nama
def hapus(nama):
    for mhs in mahasiswa:
        if mhs['nama'].lower() == nama.lower():
            mahasiswa.remove(mhs)
            print(f"Data {nama} berhasil dihapus.")
            return
    print(f"Data dengan nama {nama} tidak ditemukan.")

# Fungsi untuk mengubah data mahasiswa berdasarkan nama
def ubah(nama, nilai_baru):
    for mhs in mahasiswa:
        if mhs['nama'].lower() == nama.lower():
            mhs['nilai'] = nilai_baru
            print(f"Nilai {nama} berhasil diubah menjadi {nilai_baru}.")
            return
    print(f"Data dengan nama {nama} tidak ditemukan.")

# Program utama untuk mengelola data mahasiswa
while True:
    print("\nMenu:")
    print("1. Tambah Data")
    print("2. Tampilkan Data")
    print("3. Hapus Data")
    print("4. Ubah Data")
    print("5. Keluar")

    pilihan = input("Pilih menu (1-5): ")
    
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
        print("Program selesai. Terima kasih!")
        break
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")

---

Penjelasan Program

1. Fungsi tambah():

Menambahkan data mahasiswa ke dalam list mahasiswa berupa dictionary dengan kunci nama dan nilai.



2. Fungsi tampilkan():

Menampilkan seluruh data mahasiswa yang ada dalam list mahasiswa.

Jika list kosong, akan menampilkan pesan bahwa data tidak ada.



3. Fungsi hapus(nama):

Mencari data berdasarkan nama, lalu menghapusnya dari list jika ditemukan.

Jika tidak ditemukan, menampilkan pesan kesalahan.



4. Fungsi ubah(nama):

Mencari data berdasarkan nama, lalu mengubah nilai mahasiswa tersebut jika ditemukan.

Jika tidak ditemukan, menampilkan pesan kesalahan.
