# Praktikum 3


Pada latihan praktikum ke tiga kita akan mencoba menggunakan fungsi `end`, `sep` & `string format`.

Fungsi `end` akan menambahkan teks pada akhir perintah.\
Secara default `end` akan membuat baris baru setelah perintah print berakhir.

begitu pula dengan fungsi `sep` akan menambahkan teks sebagai separator.\
Secara default fungsi `sep` akan menambahkan sepasi sebagai separatornya.

Sedangkan untuk fungsi `string format` atau `format` adalah untuk formating style.

untuk formatting style yang kita pakai pada praktikum kali ini yaitu :
 
#### 1. Formatting dasar
 Formatting posisi kemungkinan adalah hal yang paling sering kita jumpai. Kita menggunakannya pada saat urutan dari argumen tidak ingin diubah, dan hanya ada sedikit elemen yang akan digabungkan. Metode formatting ini cocoknya adalah untuk memformat elemen yang jumlahnya sedikit.

 ```
 {} {}'.format('one', 'two')

 --------  Output  --------

 one two
 ```

 kita dapat merubah posisi dengan merubah indexing seperti ini 
  ```
 {1} {0}'.format('one', 'two')

 --------  Output  --------

 two one
 ```

#### 2. Padding atau perataan string
 Normalnya, nilai yang diformat mengambil lebar sebanyak karakter yang akan direpresentasikannya. Akan tetapi, kita bisa mengatur sendiri berapa lebar yang kita inginkan.

Rata Kanan:
```
{:>10}'.format('test')

--------  Output  --------
[][][][][][][][][][]test

```

Rata Kiri:
```
{:10}'.format('test')

--------  Output  --------
test[][][][][][][][][][]
```
> [ ] pada output diatas untuk merepresentasikan paddingnya. pada aktualnya tidak akan muncul [] tetapi akan terlihat seperti spasi atau tab.\




# Latihan 1
Code :
```
# penggunaan end
print('A', end='')
print('B', end='')
print('C', end='')

print()
print('X')
print('V')
print('Z')
# penggunaan separator

w, x, y, z = 10, 15, 20, 25
print(w, x, y, z)

print(w, x, y, z, sep=',')
print(w, x, y, z, sep='')
print(w, x, y, z, sep=':')
print(w, x, y, z, sep='-----')

# string format

print(0, 10**0)
print(1, 10 **1)
print(2, 10 **2)
print(3, 10 **3)
print(4, 10 **4)
print(5, 10 **5)
print(6, 10**6)
print(7, 10**7)
print(8, 10**8)
print(9, 10**9)
print(10, 10**10)

# string format
print('{0:>3} {1:>16}'.format(0, 10**0))
print('{0:>3} {1:>16}'.format(1, 10**1))
print('{0:>3} {1:>16}'.format(2, 10**2))
print('{0:>3} {1:>16}'.format(3, 10**3))
print('{0:>3} {1:>16}'.format(4, 10**4))
print('{0:>3} {1:>16}'.format(5, 10**5))
print('{0:>3} {1:>16}'.format(6, 10**6))
print('{0:>3} {1:>16}'.format(7, 10**7))
print('{0:>3} {1:>16}'.format(8, 10**8))
print('{0:>3} {1:>16}'.format(9, 10**9))
print('{0:>3} {1:>16}'.format(10, 10**10))

```
>`print('A', end='')`\
`print('B', end='')`\
`print('C', end='')`\
\
 kode ini akan membuat output huruf A yang pada akhir perintah fungsi end nya di ubah menjadi kosong yang secara defaultnya akan merubah baris seperti kode berikut :\
 \
`print()`\
`print('X')`\
`print('V')`\
`print('Z')`\
\
-------------------------------------------------------------------------------\
`w, x, y, z = 10, 15, 20, 25`\
Kode ini untuk mendefinisikan `w x y z` dan mengisi value dengan angka\
ketika di run akan otomatis mengisi separator dengan sepasi\
\
`print(w, x, y, z, sep=',')`\
`print(w, x, y, z, sep='')`\
`print(w, x, y, z, sep=':')`\
`print(w, x, y, z, sep='-----')`\
\
kode berikut untuk merubah separator menjadi yang kita inginkan.\
-----------------------------------------------------------------------\
`print(0, 10**0)`\
`print(1, 10 **1)`\
`print(2, 10 **2)`\
`print(3, 10 **3)`\
`print(4, 10 **4)`\
`print(5, 10 **5)`\
`print(6, 10**6)`\
`print(7, 10**7)`\
`print(8, 10**8)`\
`print(9, 10**9)`\
`print(10, 10**10)`\
\
kode diatas ini akan menampilkan angka 10 lalu dibaris selanjutnya di pangkat terus hingga pangkat 10\
dan akan menampilkan rata kiri.\
untuk membuatnya menjadi rata kanan\
kita dapat menambahkan padding.\
seperti code berikut :\
`print('{0:>3}{1:>16}')`\
lalu tambahkan format untuk menampilkan angka.\
\
`print('{0:>3} {1:>16}'.format(0, 10**0))`\
`print('{0:>3} {1:>16}'.format(1, 10**1))`\
`print('{0:>3} {1:>16}'.format(2, 10**2))`\
`print('{0:>3} {1:>16}'.format(3, 10**3))`\
`print('{0:>3} {1:>16}'.format(4, 10**4))`\
`print('{0:>3} {1:>16}'.format(5, 10**5))`\
`print('{0:>3} {1:>16}'.format(6, 10**6))`\
`print('{0:>3} {1:>16}'.format(7, 10**7))`\
`print('{0:>3} {1:>16}'.format(8, 10**8))`\
`print('{0:>3} {1:>16}'.format(9, 10**9))`\
`print('{0:>3} {1:>16}'.format(10, 10**10))`





Output :\
\
!["Output Latihan 1](/Screenshot/SS-output-Lat1.png)



## Latihan 2
Code :
```
a=input("masukkan nilai a:")

b=input("masukkan nilai b:")

print("variable a=",a)
print("variable b=",b)
print("hasil penggabungan {1}&{0}=%s".format(a,b) %(a+b))
#konversi nilai variable

a=int(a)
b=int(b)

print("hasil penjumlahan {1}+{0}=%d".format(a,b) %(a+b))
print("hasil pembagian {1}/{0}=%d".format(a,b) %(a/b))
```
Output :\
![""Output Latihan 2](/Screenshot/SS-output-Lat2.png)\
=-----------------------------------------------------------------=
## Latihan 3
Code :
```
print('{1:>15}'.format(0,"*"))
print('{1:>16}'.format(0,"***"))
print('{1:>17}'.format(0,"*****"))
print('{1:>18}'.format(0,"*******"))
print('{1:>19}'.format(0,"*********"))
print('{1:>18}'.format(0,"*******"))
print('{1:>17}'.format(0,"*****"))
print('{1:>16}'.format(0,"***"))
print('{1:>15}'.format(0,"*"))
```
Output : \
!["Output Latihan 3"](/Screenshot/SS-output-Lat3.png)