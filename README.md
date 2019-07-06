# Rangkuman-Modul1
Struktur Data

Variabel dan type data
Variabel adalah sebuah nama yang merepresentasikan suatu nilai dengan tipe data.
Berbagai macam tipe data dasar yang dikenal dalam bahasa pemrograman Python, seperti:

Integer =  adalah data numeric
   num = 100
   type num

Float = adalah data numeril berbentuk real
    realNum = 0.999
    type(realNum)

String = tipe data yang memuat satu karakter atau lebih karakter yang diapit oleh tanda petik tunggal (') atau tanda petik (“)
    data = "hello word"
    type (data)


Operasi data variabel biasanya dapat di lakukan pada operasi tertentu akan tetapi di bawah ini adalah contoh
kode variabel dengan type data yang sama:
    #Operasi antara variabel bertipe integer
    a=10
    b=5
    hasil=a+b
    print('hasil=',hasil)

    #Operasi antara variabel bertipe float
    a=5.5
    b=1.2
    hasil=a+b
    print('hasil=',hasil)

    #Operasi antara variabel bertipe string
    a='struktur'
    b='data'
    hasil=a+' '+b
    print('hasil=',hasil)

Setelah di atas saya menampilkan contoh kode variabel dengan type yang sama selanjutnya, di bawah ini adalah contoh kode dengan
type data yang tidak sama:
    #Operasi antara variabel bertipe integer dengn variabel bertipe float
    a=10
    b=5.5
    hasil=a+b
    print('hasil=',hasil)

    #Operasi antara variabel bertipe integer dengn variabel bertipe string
    a='struktur data'
    b=2
    hasil=a+b
    print('hasil=',hasil)


Jenis-jenis Algoritma Pemrograman:
1.	Algoritma sequential, adalah proses membandingkan setiap elemen larik satu per satu secara beruntun,
    mulai dari elemen pertama, sampai dengan elemen terakhir atau elemen yang dicari sudah ditemukan.
        # Algoritma Sequence - Konversi Kurs Mata Dollar ke Rupiah
	
		dollar=int(input('Jumlah Dollar = '))
		rupiah=dollar*15000
		print(dollar,'$ = Rp.',rupiah)
    
2.	Algoritma selection, merupakan algoritma yang didalamnya terdapat pilihan (True & False).
    Jika memenuhi kondisi True maka syntax pada percabangan True yang akan diekseskusi, begitu juga sebaliknya. 
        # Algoritma selection - Penentuan jenis bilangan
	
		num=int(input('Masukkan bilangan = '))
		if num%2==0 :
		    print(num, ' adalah bilangan genap')
		else:
		    print(num, ' adalah bilangan ganjil')
    
3.	Algoritma looping, Pada Algoritma ini, syntax akan dieksekusi secara berulang-ulang selama kondisi bernilai True. 
    Jika kondisi bernilai False maka proses iterasi akan berhenti.
        # Algoritma looping - Menampilkan sejumlah n bilangan genap
	
		num=int(input('Jumlah bilangan genap = '))
		count=1
		i=0
		while count<=num:
		    if i%2==0:
			print(count,'. ',i)
		    count=count+1 
		i=i+1


String adalah type data ayng terdiri dari beberapa karakter

	    data="Where is Waldo ?"
	    print(data[12]) # Satu karakter
	    temp=data[9:14] # lima karakter
	    print(temp)
    
List adalah struktur data yang terdiri dari beberapa elemen atau anggota list dengan berbagai tipe data

	    arrData=[1,2,'python',0.8,'numpy']
	    print (arrData)
	    print(arrData[1])
	    print(arrData[1:4])

List 2D adalah list yang berbentuk dua dimensi, yaitu bentuk data seperti halnya matriks dua dimensi, yang memiliki baris dan kolom

    #list 2D, dengan 2 baris, 3 kolom
	    arr2=[[1,2,3],[4,5,6]]
	    print(arr2)
	    print(arr2[0][2])

Tuple, sama halnya dengan list, tuple ini terdiri dari beberapa elemen, dan elemen tersebut dapat terdiri dari berbagai tipe.

    tupData=(1,2,'python',0.8,'numpy')
    print(tupData)
    print(tupData[2])
    print(tupData[1:3])
    
    
Dictionaries, pada type data ini biasanya di sebut keys ataupun index.
Jika pada list menggunakan '[...]', dan tuple menggunakan (...),
maka variabel yang berbentuk dictionaries ini dapat dilakukan dengan dua cara, yaitu
1. Menuliskan semua anggotanya secara langsung, namaVariabel={key1:data1, key2:data2,...}
2. Menuliskan satu-persatu anggotanya

#Cara-1

    studData={'001':'Ranti','002':'Diana','003':'Budi','004':'Eri'}
    print(studData)

#Cara-2

    studentData={}
    studentData['001']='Fatimah'
    studentData['002']='Sofiah'
    studentData['003']='Ahmad'
    studentData['005']='Ali'
    print(studentData)

implementasi Dictionaries ini adalah Sparse Matrix.
Sparse Matrix merupaan matrix yang memiliki banyak nilai nol, sehingga jika menggunakan list, akan banyak memori yang dibutuhkan.
Sedangkan dictionaries, hanya menyimpan yang dibutuhkan saja.
Misalkan terdapat sebuah matriks dengan ukuran 4 x 4, yang berarti terdapat 16 elemen pada matriks tersebut.

    Mat = {(0,3): 1, (2, 1): 2, (3, 3): 3}
    print(Mat)
    Mat[0,2]=4 #penambahan data baru
    print(Mat)
    #pengecekan data pada index (ind1,ind2), jika tidak terdapat data, maka return value=None, 
    #jika terdapat data maka return value=adalah data
    cek=Mat.get((0,1)) 
    print(cek)
    cek=Mat.get((2,1))
    print('(2,1)=',cek)
    cek=Mat.get((1,3))
    print('(1,3)=',cek)


semakin kompleks algoritma, maka semakin sulit untuk dibaca dan diperbaiki jika terdapat kesalahan atau penambahan syntax baru 
akan tetapi dengan function maka syntax-syntax pada program dikelompokkan berdasarkan fungsinya masing-masing.
Dengan pengelompokan ini, maka program akan lebih mudah untuk dibaca maupun diperbaiki.

Terdapat dua hal penting yang harus diperhatikan, yaitu
1. Parameter/argumen : merupakan nilai yang dikirim oleh syntax pemanggil function
2. Return Value : merupakan nilai yang dihasilkan oleh function, dan dikirim kembali ke pemanggil function

contoh:
	    # Function tanpa parameter
	    def addNumbers():
		a=int(input('Bilangan pertama = '))
		b=int(input('Bilangan kedua = '))
		print('Hasil = ',a+b)
	    #Main program
	    addNumbers()#memanggil fungsi addNumbers agar dieksekusi

	    # Function dengan parameter

	    def addNumbers(a,b):
		print('Hasil = ',a+b)
	    #Main program
	    num1=int(input('Bilangan pertama = '))
	    num2=int(input('Bilangan kedua = '))
	    addNumbers(num1,num2)#memanggil fungsi addNumbers agar dieksekusi

	    # Function dengan parameter dan return value

	    def addNumbers(a,b):
		hasil=a+b
		return hasil
	    def cekGenap(num):
		if num%2==0:
		    return True
		else:
		    return False
	    #Main program
	    num1=int(input('Bilangan pertama = '))
	    num2=int(input('Bilangan kedua = '))
	    result=addNumbers(num1,num2)#memanggil fungsi addNumbers agar dieksekusi
	    print('Hasil Penjumlahan= ', result)
	    if cekGenap(result):
		print(result,' adalah Bilangan Genap')
	    else:
		print(result,' adalah Bilangan Ganjil')



Tugas Praktikum
1. Buatlah suatu fungsi untuk menampilkan segitiga, yang memiliki dua buah parameter, yaitu karakter yang akan dicetak,
  dan tinggi segitiga (jika diperlukan, gunakan formatting string).
  Berikut adalah contoh program untuk memanggil fungsi segitiga tersebut, dan hasil output segitiga yang ditampilkan:

Jika tinggi segitiga adalah 7
printTriangle('$',7)

	       $
	      $$$
	     $$$$$
	    $$$$$$$
	   $$$$$$$$$
	  $$$$$$$$$$$
	 $$$$$$$$$$$$$
	$$$$$$$$$$$$$$$


Jika Tinggi segitiga adalah 12
printTriangle('*',12)

		   *
		  ***
		 *****
		*******
	       *********
	      ***********
	     *************
	    ***************
	   *****************
	  *******************
	 *********************
	***********************


2. Buatlah suatu modul dengan nama sparseMatrix (matriks yang memiliki banyak elemen ‘nol’) yang berisi beberapa fungsi sebagai berikut :
	a) Fungsi untuk input data dari user. Input data ini berupa ukuran matriks, dan elemen-elemen pada sparse matrix tersebut ,
     seperti contoh berikut:
	    matrik-1		          matrik-2
	    jumlah baris = 3	    	jumlah baris = 4
	    jumlah kolom = 4	    	jumlah kolom = 1
	    jumlah data = 2		jumlah data = 2
	    baris ke ?0		        baris ke ?0
	    kolom ke ?0		        kolom ke ?0
	    matrik [0,0]=2		matrik [0,0]=3
	    baris ke ?2		        baris ke ?3
	    kolom ke ?3		        kolom ke ?0
	    matrik [2,3]=4		matrik [3,0]=2


b) Fungsi untuk menampilkan sparse matrix. Contoh tampilan sparse matrix dapat dilihat sebagai berikut:
		matrik 1=	      matrik 2=
		| 2 0 0 0 |	    | 3 |
		| 0 0 0 0 |	    | 0 |
		| 0 0 0 4 |	    | 0 |
					| 2 |


c) Fungsi untuk mengalikan dua buah sparse matrix.
   Contoh hasil perkalian dua buah sparse matrix, dapat dilihat sebagai berikut :

	matrik 1=
	| 2 0 0 0 |
	| 0 0 0 0 |
	| 0 0 0 4 |

	matrik 2=
	| 3 |
	| 0 |
	| 0 |
	| 2 |

	Hasil =
	| 6 |
	| 0 |
	| 8 |

Import modul yang sudah dibuat dalam program utama (main program), dan eksekusi fungsi-fungsi yang sudah dibuat agar dapat
meminta input dari user,mengalikan dua buah sparse matrix, dan menampilkan sparse matrix-sparse matrix tersebut
(matriks yang dikalikan dan hasil perkalian)


Jawaban Tugas Praktikum

#menampilkan segitiga-nomer1

    string = ""
    x = int(input("Masukkan angka :"))
    bar = x
    while bar >= 0:
      kol = bar
      while kol > 0:
        string = string + "   "
        kol = kol - 1
      kiri = 1
      while kiri < (x - (bar-1)):
        string = string + " * "
        kiri = kiri + 1			
      kanan = 1
      while kanan < kiri -1:
        string = string + " * "
        kanan = kanan + 1	
      string = string + "\n\n"
      bar = bar - 1
    print (string)

#sparse matriks-nomer2

    def MatriksInput():
        baris=input("Jumlah Baris : ")
        kolom=input("Jumlah Kolom  : ")
        JumlahData=int(input("Jumlah Data : "))
        matrixData={}

        for i in range (0,JumlahData):
            tempbaris=int(input("Baris ke ? "))
            tempkolom=int(input("Kolom ke ? "))
            temp="Matriks [" + str(tempbaris) + "," + " " + str(tempkolom) + "]" + " : "
            data=input(temp)
            matrixData[tempbaris,tempkolom]=data
        return (matrixData,baris,kolom)

    def displayData(matrixData,baris,kolom):
        matrix={}
        for i in range(0,int(baris)):
            temp=''
            for j in range(0,int(kolom)):
                if matrixData.get((i+1,j+1),0)==0:
                    temp=temp+' '+str(0)
                else:
                    temp=temp+' '+str(matrixData[i+1,j+1])
            print(temp)

    def multMatrix(a,b,baris,kolom):
        c={}
        for i in range(0,int(baris)):
            for j in range(0, int(kolom)):
                temp=0
                for k in range(0,int(baris)):
                    if ((a.get((i+0,k+1),0)!=0) and (b.get((k+1,j+1),0)!=0)):

                        temp=temp+int(a[i+0,k+1])*int(b[k+1,j+1])

                    else:
                        temp=temp+0

                c[i+1,j+1]=temp
        return(c)

    print("matriks-1")
    (a,baris_a,kolom_a)=MatriksInput()
    print("_________________________________________________\n")
    print("matriks-2")
    (b,baris_b,kolom_b)=MatriksInput()
    if (kolom_a==baris_b):
        c=multMatrix(a,b,baris_a,kolom_a)
        print("_________________________________________________\n \n~ PERKALIAN MATRIKS 1 & MATRIKS 2 ~\n")
        print("matriks 1 = ")
        displayData(a,baris_a,kolom_a)
        print("matriks 2 = ")
        displayData(b,baris_b,kolom_b)
        print("Hasil = ")
        displayData(c,baris_a,kolom_b)
    else:
        print("_________________________________________________\n \nUkuran Matriks yang Anda Masukkan Tidak Sesuai")
