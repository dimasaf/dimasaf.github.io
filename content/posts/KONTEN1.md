---
title: "Arduino Pt.1"
date: 2019-11-10
author: "Dimas Af"
comments: true
---

TIPE DATA ARDUINO

## VARIABLE
Variabel merupakan suatu pengenal (identifier) atau wadah untuk menyimpan suatu nilai. Variabel yang digunakan harus ditentukan juga tipe datanya.

+ Cara mendeklarasikan sebuah variabel
```bash
#bentuk umum
Nama_tipe nama_variabel ;
#contoh mendeklarasikan nama variable 'led' di pin 8
define led  8;
```

## STRING
String adalah tipe data yang digunakan untuk sebuah teks yang merupakan gabungan huruf, angka, whitespace (spasi), dan berbagai karakter. Fungsi ini digunakan untuk membuat identifier String/teks.

+ Cara mendeklarasikan String
```bash
#tipe data string dengan identifier coba
String coba = "Hello String";  
```

## INT
Integer digunakan untuk menyimpan angka, Tipe data ini menyimpan nilai 16-bit (2 byte) dengan rentang ukuran -32,768 sampai 32,767. 

+ Cara mendeklarasikan int
```bash
#tipe data int dengan identifier coba
int penambah = 0;
```

## UNSIGNED INT
Tipe data ini hampir sama dengan int. bedanya Unsigned int tidak menyimpan nilai negatif. Rentang ukuran 0 sampai 65,535.

+ Cara mendeklarasikan int
```bash
#tipe data unsigned int dengan identifier y
unsigned int y = 10;
```

## LONG
Long digunakan untuk menyimpan angka, mempunyai ukuran yang lebih banyak dan menyimpan 32-bit (4 byte) dari -2,147,438,648 sampai 2,147,438,647.

+ Cara mendeklarasikan long
```bash
#tipe data long dengan identifier jarak
long jarak = 222123420;
```

## FLOAT / DOUBLE
Float merupakan tipe data yang menyimpan angka yang memiliki nilai desimal.

+ Cara mendeklarasikan long
```bash
#tipe data float dengan identifier sensorSuhu
float sensorSuhu = 1.117;
```

## BOOL
Tipe data bool memiliki salah satu dari dua nilai, yaitu true atau false.

+ Cara mendeklarasikan bool
```bash
#tipe data bool dengan identifier hidup
bool hidup = falsel
```

## CHAR
Tipe data yang digunakan untuk menyimpan karakter. biasanya karakter ditulis dalam tanda kutip tunggal, seperti ini: 'A'

+ Cara mendeklarasikan char
```bash
#tipe data char dengan identifier tes
char tes = 'A'
```

## BYTE
Byte menyimpan 8-bit unsigned number, dari 0 sampai 255

+ Cara mendeklarasikan char
```bash
#tipe data byte dengan identifier terang
byte terang = 255;
```

# ARRAY
Array adalah sekumpulan variabel yang dapat diakses dengan nomor indeks


+ Cara mendeklarasikan array
```bash
#contoh penulisan array
int myInts[6];
int myPins[] = {2, 4, 8, 3, 6};
int mySensVals[6] = {2, 4, -8, 3, 2};
char message[6] = "hello";
```

untuk informasi lebih jelas https://www.arduino.cc/reference/
