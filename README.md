# Tugas-pertemuan-ke-12
1. Class
###
    class SData():
        def __init__(self, nama='', nilai=''):
            self.nama = nama
            self.nilai = nilai
            self.Data = {
            }
2. Class - tambah()
###
    def tambah(self):
        print("=== Tambah Data ===")
        print("=== Nama dan Nilai yang akan anda masukkan akan disimpan ke dalam Data ===")
        self.nama = input("Nama : ")
        if self.nama in self.Data:
            print("=== Maaf, Nama yang anda masukkan sudah terdaftar ===")
        else:
            self.nilai = input("Nilai : ")
            self.Data[self.nama] = int(self.nilai)
        self.menu()
3. Class - cetak()
###
    def cetak(self):
        print("====== Data Universal ======")
        if len(self.Data.items()) == 0:
            print(" >Data masih belum tersedia<")
        else:
            for i in range(len(self.Data)):
                print(f'Nama : {list(self.Data.keys())[i]} | Nilai : {list(self.Data.values())[i]}')
        print("============================")
        self.menu()
4. Class - hapus()
###
    def hapus(self):
        print("=== Hapus Data ===")
        for i in range(len(self.Data)):
            print(f'( {i + 1} )', list(self.Data.keys())[i])
        print("=== Pilih salah satu nomor diatas ===")
        while True:
            try:
                m = int(input("-> "))
                del self.Data[list(self.Data.keys())[m - 1]]
                break
            except:
                print("Nomor yang Anda masukkan tidak tersedia atau salah")
        self.menu()
5. Class - ubah()
###
    def ubah(self):
        if len(self.Data.items()) == 0:
            print(" > Data masih belum tersedia <")
            self.menu()
        else:
            print("=== Ubah Data ===")
            for i in range(len(self.Data)):
                print(f'( {i + 1} )', list(self.Data.keys())[i])
            while True:
                try:
                    n = int(input("Pilih salah satu nomor diatas : "))
                    if list(self.Data.keys())[n - 1] in self.Data:
                        self.Data[list(self.Data.keys())[n - 1]] = int(input("Nilai = "))
                        break
                    else:
                        print("Tidak ditemukan")
                except:
                    print("Nomor yang Anda masukkan tidak tersedia atau salah")
            self.menu()
6. Class - menu()
###
    def menu(self):
        Choose = input("T (Tambah) | P (Tampil) | H (Hapus) | U (Ubah) | K (Keluar)")
        if Choose == 'T' or Choose == 't':
            self.tambah()
        elif Choose == 'P' or Choose == 'p':
            self.cetak()
        elif Choose == 'H' or Choose == 'h':
            self.hapus()
        elif Choose == 'U' or Choose == 'u':
            self.ubah()
        elif Choose == 'K' or Choose == 'k':
            print("Goodbye")
        else:
            print("Opsi Tidak tertera, mohon diulangi..")
            self.menu()
7. Di luar Class
###
    Mipa1 = SData()
Variable 'Mipa1', merupakan instance class dari class Person.

![image](https://user-images.githubusercontent.com/61907877/146686052-43efb365-2f94-4b89-87a7-3cb15e5693c2.png)
![image](https://user-images.githubusercontent.com/61907877/146686072-07295dbf-c30f-420f-8b5c-3f95cbf05e14.png)
