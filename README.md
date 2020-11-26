# lab4
# program Masukkan Nilai Mahasiswa
print("==================================================================")
print("|                 PROGRAM INPUT NILAI MAHASISWA                  |")
print("==================================================================")

nilai = []
perulangan = True

while perulangan:
    nama = input("Masukkan Nama: ")
    nim = input("Masukkan NIM: ")
    nilai_tugas = int(input("Masukkan Nilai Tugas: "))
    nilai_uts = int(input("Masukkan Nilai UTS: "))
    nilai_uas = int(input("Masukkan Nilai UAS: "))
    nilai_akhir = (nilai_tugas * 30/100) + (nilai_uts * 35/100) + (nilai_uas * 35/100)

    nilai.append([nama, nim, nilai_tugas, nilai_uts, nilai_uas, int(nilai_akhir)])
    if (input("Tambah data (y/t)? ") == 't'):
        perulangan = False

print("==================================================================")
print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
print("==================================================================")
i = 0
for item in nilai:
    i += 1
    print("| {no:2d} | {nama:12s} | {nim:9s} | {nilai_tugas:5d} | {nilai_uts:5d} | {nilai_uas:5d} | {nilai_akhir:6.2f} |"
          .format(no=i, nama=item[0], nim=item[1], nilai_tugas=item[2], nilai_uts=item[3], nilai_uas=item[4], nilai_akhir=item[5]))
print("==================================================================")
