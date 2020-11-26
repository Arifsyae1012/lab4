# lab4
# program Masukkan Nilai Mahasiswa
+ print("==================================================================")
+ print("|                 PROGRAM INPUT NILAI MAHASISWA                  |")
+ print("==================================================================")
+ 
+ nilai = []
+ perulangan = True

+ while perulangan:
+     nama = input("Masukkan Nama: ")
+     nim = input("Masukkan NIM: ")
+     nilai_tugas = int(input("Masukkan Nilai Tugas: "))
+     nilai_uts = int(input("Masukkan Nilai UTS: "))
+     nilai_uas = int(input("Masukkan Nilai UAS: "))
+     nilai_akhir = (nilai_tugas * 30/100) + (nilai_uts * 35/100) + (nilai_uas * 35/100)
+ 
+     nilai.append([nama, nim, nilai_tugas, nilai_uts, nilai_uas, int(nilai_akhir)])
+     if (input("Tambah data (y/t)? ") == 't'):
+         perulangan = False
+ 
+ print("==================================================================")
+ print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
+ print("==================================================================")
+ i = 0
+ for item in nilai:
+     i += 1
+     print("| {no:2d} | {nama:12s} | {nim:9s} | {nilai_tugas:5d} | {nilai_uts:5d} | {nilai_uas:5d} | {nilai_akhir:6.2f} |"
+           .format(no=i, nama=item[0], nim=item[1], nilai_tugas=item[2], nilai_uts=item[3], nilai_uas=item[4], + + + + + + nilai_akhir=item[5]))
+ print("==================================================================")


# lab5
+ # Membuat program input Nilai
+ data = {}
+ while True:
+     print("=====================================================================")
+     print("|                       Program Input Nilai                         |")
+     print("=====================================================================")
+     print("")
+     g = input("(L)ihat, (T)ambah, (U)bah, (H)apus,(C)ari, (K)eluar : ")
+     # Keluar dari program
+     if g.lower() == "k":
+         print("Keluar dari program")
+         break
+     # melihat list
+     elif g.lower() == "l":
+         if data.items():
+             print()
+             print("**********************************Daftar Nilai****************************************")
+             print()
+             print("======================================================================================")
+             print("|  No  |      NIM     |      NAMA      |   TUGAS  |   UTS   |   UAS   | AKHIR  |")
+             print("======================================================================================")
+             i = 0
+             for x in data.items():
+                 i += 1
+                 print("| {6:4} | {0:13s} | {1:13} | {2:8d} |  {3:6d} | {4:7d} | {5:12.2f} | " \
+                       .format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))
+                 print("======================================================================================")
+                 print("")
+         else:
+             print("**********************************Daftar Nilai****************************************")
+             print()
+             print("======================================================================================")
+             print("|  No  |      Nama     |      NIM      |   TUGAS  |   UTS   |   UAS   | Nilai Akhir  |")
+             print("======================================================================================")
+             print("|                                 Tidak Ada Daftar Nilai                             |")
+             print("======================================================================================")
+     # menambahkan data
+     elif g.lower() == "t":
+         print("Tambah Data")
+         nim = int(input("NIM            : "))
+         nama = input("Nama              : ")
+         uts = int(input("Nilai UTS      : "))
+         uas = int(input("Nilai UAS      : "))
+         tugas = int(input("NIlai Tugas  : "))
+         nilaiakhir = ((tugas) * 30 / 100 + (uts) * 35 / 100 + (uas) * 35 / 100)
+         data[nama] = nim, tugas, uts, uas, nilaiakhir
+     # mengubah data
+     elif g.lower() == "u":
+         print("Edit Data Nilai Mahasiswa")
+         nama = input(" Masukan Nama:")
+         if nama in data.keys():
+             nim = input("NIM               :")
+             tugas = int(input("Nilai Tugas Baru  : "))
+             uts = int(input("Nilai UTS Baru    : "))
+             uas = int(input("Nilai UAS Baru    : "))
+             nilaiakhir = ((tugas) * 30 / 100 + (uts) * 35 / 100 + (uas) * 35 / 100)
+             data[nama] = nim, tugas, uts, uas, nilaiakhir
+         else:
+             print("Data nilai{0} tidak ada ".format(nama))
+     # Menghapus data
+     elif g.lower() == "h":
+         print("Hapus Data Nilai Mahasiswa")
+         nama = input(" Masukan Nama:")
+         if nama in data.keys():
+             del data[nama]
+         else:
+             print("Data {0} tidak ada".format(nama))
+         # Mencari data
+     elif g.lower() == "c":
+         print("Cari Data Nilai Mahasiswa")
+         nama = input(" Masukan Nama: ")
+         if nama in data.keys():
+             printprint("***************************Daftar Nilai*************************")
+             print()
+             print("==================================================================")
+             print("~~~~~~~~~~~NAMA  NIM  TUGAS  UTS UAS NILAI AKHIR~~~~~~~~~~~~~~~~~~~")
+             print("| {0} | {1} | ".format(nama, data[nama]))
+             print("==================================================================")
+         else:
+             print("Datanya {0} tidak ada ".format(nama))
+     else:
+         print("\\*************************************Daftar Nilai*********************************//")
+         print("======================================================================================")
+         print("|  No  |      Nama     |      NIM      |   TUGAS  |   UTS   |   UAS   | Nilai Akhir  |")
+         print("======================================================================================")
+         print("|                                 Tidak Ada Daftar Nilai                             |")
+         print("======================================================================================")
+ 
+ else:
+     print("Pilih Menu Yang Tersedia")
