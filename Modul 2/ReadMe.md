# <h1 align="center">Laporan Praktikum Struktur Data<br> Modul 1 Pengenalan C++ </h1>
<p align="center">Salfi Ayu Ramadhani / 103112430224</p>

## Dasar Teori

C++ adalah bahasa pemrograman yang dibuat oleh Bjarne. Stroustrup, yang merupakan perkembangan dari bahasa C, dihasilkan di Bong Labs (Dennis Ritchie) pada awal tahun 1970-an. Bahasa itu berasal dari bahasa sebelumnya, yaitu B, Awalnya, bahasa tersebut dibuatsebagai bahasa pemrograman yang berfungsi di sistem Unix, Pada perkembangannya, versi ANSI (American National Standards Institute) Bahasa pemrograman C menjadi versi utama, meskipun versi tersebut sekarang tidak sering dipakai dalam pengembangan sistem dan jaringan maupun untuk sistem tertanam, pertama kali oleh Bjarne Stroustrup di laboratorium Bell mengembangkan C++ pada awal tahun 1980-an.

## Guided

### Soal 1

Sruct

```cpp
#include <iostream>
#include <string>
using namespace std;

// Definisi struct
struct Mahasiswa {
    string nama;
    string nim;
    float ipk;
};

int main() {

    Mahasiswa mhs1;

    cout << "Masukkan Nama Mahasiswa: ";
    getline(cin, mhs1.nama);
    // cin >> mhs1.nama;
    cout << "Masukkan NIM Mahasiswa : ";
    cin >> mhs1.nim;
    cout << "Masukkan IPK Mahasiswa : ";
    cin >> mhs1.ipk;

    cout << "\n=== Data Mahasiswa ===" << endl;
    cout << "Nama : " << mhs1.nama << endl;
    cout << "NIM  : " << mhs1.nim << endl;
    cout << "IPK  : " << mhs1.ipk << endl;

    return 0;
}
```

> Screenshoot 
> ![Screenshot Soal 1](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%201%20struct.png)

Program ini membuat struct Mahasiswa untuk menyimpan data nama, nim, dan ipk.
Program meminta input dari user, lalu menampilkan kembali data mahasiswa tersebut.

---

### Soal 2

Aritmatika

```cpp
#include <iostream>
using namespace std;
int main()
{
    int W, X, Y;
    float Z;
    X = 7;
    Y = 3;
    W = 1;
    Z = (X + Y) / (Y + W);
    cout << "Nilai z = " << Z << endl;
    return 0;
}
```

> Screenshoot  
> ![Screenshot Soal 2](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%202%20aritmatika.png)

Program menghitung (7+3)/(3+1) = 10/4. Karena pembagian integer, hasilnya 2, lalu ditampilkan sebagai 2.

### Soal 3

Kondisi

```cpp
#include <iostream>
using namespace std;
// int main()
// {
//     double tot_pembelian, diskon;
//     cout << "total pembelian: Rp";
//     cin >> tot_pembelian;
//     diskon = 0;
//     if (tot_pembelian >= 100000)
//         diskon = 0.05 * tot_pembelian;
//     cout << "besar diskon = Rp" << diskon;
// }



// int main()
// {
//     double tot_pembelian, diskon;
//     cout << "total pembelian: Rp";
//     cin >> tot_pembelian;
//     diskon = 0;
//     if (tot_pembelian >= 100000)
//         diskon = 0.05 * tot_pembelian;
//     else
//         diskon = 0;
//     cout << "besar diskon = Rp" << diskon;
// }



int main()
{
    int kode_hari;
    cout << "Menentukan hari kerja/libur\n"<<endl;
    cout << "1=Senin 3=Rabu 5=Jumat 7=Minggu "<<endl;
    cout << "2=Selasa 4=Kamis 6=Sabtu "<<endl;
    cin >> kode_hari;
    switch (kode_hari)
    {
    case 1:
    case 2:
    case 3:
    case 4:
    case 5:
        cout<<"Hari Kerja";
        break;
    case 6:
    case 7:
        cout<<"Hari Libur";
        break;
    default:
        cout<<"Kode masukan salah!!!";
    }
    return 0;
}
```

> Screenshoot 
> ![Screenshot Soal 3](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%203%20kondisi.png)

Program ini menghitung diskon belanja atau menentukan hari kerja/libur.

### Soal 4

Perulangan

```cpp
#include <iostream>
using namespace std;
// int main()
// {
//     int jum;
//     cout << "jumlah perulangan: ";
//     cin >> jum;
//     for (int i = 0; i < jum; i++)
//     {
//         cout << "saya sahroni\n";
//     }
//     return 1;
// }


// while
int main()
{
    int i = 1;
    int jum;
    cin >> jum;
    do
    {
        cout << "bahlil ke-" << (i + 1) << endl;
        i++;
    } while (i < jum);
    return 0;
}
```

> Screenshoot
> ![Screenshot Soal 4](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%204%20perulangan.png)

Program mencetak teks berulang sesuai jumlah yang dimasukkan.

### Soal 5

Fungsi

```cpp
#include <iostream>
using namespace std;

// Prosedur: hanya menampilkan hasil, tidak mengembalikan nilai
void tampilkanHasil(double p, double l)
{
    cout << "\n=== Hasil Perhitungan ===" << endl;
    cout << "Panjang : " << p << endl;
    cout << "Lebar   : " << l << endl;
    cout << "Luas    : " << p * l << endl;
    cout << "Keliling: " << 2 * (p + l) << endl;
}

// Fungsi: mengembalikan nilai luas
double hitungLuas(double p, double l)
{
    return p * l;
}

// Fungsi: mengembalikan nilai keliling
double hitungKeliling(double p, double l)
{
    return 2 * (p + l);
}

int main()
{
    double panjang, lebar;

    cout << "Masukkan panjang: ";
    cin >> panjang;
    cout << "Masukkan lebar  : ";
    cin >> lebar;

    // Panggil fungsi
    double luas = hitungLuas(panjang, lebar);
    double keliling = hitungKeliling(panjang, lebar);

    cout << "\nDihitung dengan fungsi:" << endl;
    cout << "Luas      = " << luas << endl;
    cout << "Keliling  = " << keliling << endl;

    // Panggil prosedur
    tampilkanHasil(panjang, lebar);

    return 0;
}

```

> Screenshoot 
> ![Screenshot Soal 5](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%205%20fungsi.png)

Program menghitung luas dan keliling persegi panjang dengan fungsi lalu menampilkannya lewat prosedur.

### Soal 6

Test

```cpp
#include <iostream>
using namespace std;
int main()
{
    string ch;
    cout << "Masukkan sebuah karakter: ";
    // cin >> ch;
    ch = getchar();  //Menggunakan getchar() untuk membaca satu karakter
    cout << "Karakter yang Anda masukkan adalah: " << ch << endl;
    return 0;
}

```

> Screenshoot 
> ![Screenshot Soal 6](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%206%20test.png)

Program membaca satu karakter dengan getchar() lalu menampilkannya kembali ke layar.

## Unguided

### Soal 1

Buatlah program yang menerima input-an dua buah bilangan bertipe float, kemudian memberikan output-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

```cpp
#include <iostream>
using namespace std;

int main() {
    float a, b;
    cout << "Masukkan bilangan pertama: ";
    cin >> a;
    cout << "Masukkan bilangan kedua: ";
    cin >> b;

    cout << "Hasil Penjumlahan: " << a + b << endl;
    cout << "Hasil Pengurangan: " << a - b << endl;
    cout << "Hasil Perkalian: " << a * b << endl;
    if (b != 0)
        cout << "Hasil Pembagian: " << a / b << endl;
    else
        cout << "Pembagian tidak dapat dilakukan (b = 0)" << endl;

    return 0;
}
```

> Screenshoot  
> ![Screenshot Soal 1](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/soal%201.png)

Program ini meminta dua bilangan, lalu menampilkan hasil + , - , × , ÷. Jika bilangan kedua nol, pembagian tidak dilakukan.

---

### Soal 2

Buatlah sebuah program yang menerima masukan angka dan mengeluarkan output nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 s.d 100.  
Contoh: 79 → tujuh puluh sembilan

```cpp
#include <iostream>
#include <string>
using namespace std;

string angkaSatuan[] = {"nol", "satu", "dua", "tiga", "empat", "lima", 
                        "enam", "tujuh", "delapan", "sembilan"};
string angkaBelasan[] = {"sepuluh", "sebelas", "dua belas", "tiga belas", 
                         "empat belas", "lima belas", "enam belas", 
                         "tujuh belas", "delapan belas", "sembilan belas"};
string angkaPuluhan[] = {"", "", "dua puluh", "tiga puluh", "empat puluh", 
                         "lima puluh", "enam puluh", "tujuh puluh", 
                         "delapan puluh", "sembilan puluh"};

string terbilang(int n) {
    if (n < 10) return angkaSatuan[n];
    else if (n < 20) return angkaBelasan[n - 10];
    else if (n < 100) {
        int puluh = n / 10;
        int satuan = n % 10;
        if (satuan == 0) return angkaPuluhan[puluh];
        else return angkaPuluhan[puluh] + " " + angkaSatuan[satuan];
    } else if (n == 100) {
        return "seratus";
    }
    return "";
}

int main() {
    int n;
    cout << "Masukkan angka (0-100): ";
    cin >> n;
    if (n >= 0 && n <= 100) {
        cout << n << " : " << terbilang(n) << endl;
    } else {
        cout << "Angka di luar jangkauan!" << endl;
    }
    return 0;
}
```

> Sreenshoot 
> ![Screenshot Soal 2](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/soal%202.png)

Program ini mengubah angka 0–100 menjadi tulisan bahasa Indonesia (terbilang), lalu menampilkannya.

---

### Soal 3

Buatlah program yang dapat memberikan input dan output sebagai berikut.  
Input: 3  
Output:  
```
321 * 123
21 * 12
1 * 1
   *
```

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "input: ";
    cin >> n;
    cout << "output:\n";

    for (int i = n; i >= 1; i--) {
        for (int j = i; j >= 1; j--) {
            cout << j;
        }
        cout << " * ";
        for (int j = 1; j <= i; j++) {
            cout << j;
        }
        cout << endl;
    }

    for (int spasi = 1; spasi <= n; spasi++) {
        cout << " ";
    }
    cout << "*" << endl;

    return 0;
}
```

> Screenshoot  
> ![Screenshot Soal 3](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/soal%203%20(1).png)

Program ini meminta input n, lalu mencetak pola angka menurun dari n ke 1 dan naik kembali dari 1 ke n dengan tanda * di tengah pada setiap baris, diulang hingga angka 1, kemudian ditutup dengan satu * di bawah pola.

---

## Referensi

1. https://tahtamedia.co.id/index.php/issj/article/download/376/374/1410 (diakses 29-09-2025)
