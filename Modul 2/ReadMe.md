# <h1 align="center">Laporan Praktikum Struktur Data<br> Modul 2 Pengenalan C++ Bagian 2 </h1>
<p align="center">Salfi Ayu Ramadhani / 103112430224</p>

## Dasar Teori

C++ adalah bahasa pemrograman yang dibuat oleh Bjarne. Stroustrup, yang merupakan perkembangan dari bahasa C, dihasilkan di Bong Labs (Dennis Ritchie) pada awal tahun 1970-an. Bahasa itu berasal dari bahasa sebelumnya, yaitu B, Awalnya, bahasa tersebut dibuatsebagai bahasa pemrograman yang berfungsi di sistem Unix, Pada perkembangannya, versi ANSI (American National Standards Institute) Bahasa pemrograman C menjadi versi utama, meskipun versi tersebut sekarang tidak sering dipakai dalam pengembangan sistem dan jaringan maupun untuk sistem tertanam, pertama kali oleh Bjarne Stroustrup di laboratorium Bell mengembangkan C++ pada awal tahun 1980-an.

## Guided

### Soal 1

Call By Pointer

```cpp
#include <iostream>
using namespace std;

void tukar(int *px, int *py);   
int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(&a, &b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}

void tukar(int *px, int *py)
{
    int temp = *px;
    *px = *py;
    *py = temp;
}

```

> Screenshoot 
> ![Screenshot Soal 1](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%201%20struct.png)

Program ini menukar nilai dua variabel menggunakan call by address. Nilai a dan b dikirim ke fungsi tukar dalam bentuk alamat, lalu isinya ditukar melalui pointer. Karena yang diubah adalah alamat aslinya, nilai a dan b ikut berubah setelah fungsi dipanggil.
---

### Soal 2

Call By Reference

```cpp
#include <iostream>
using namespace std;

void tukar(int &x, int &y);   

int main()
{
    int a = 10, b = 20;
    cout << "Sebelum ditukar: a = " << a << ", b = " << b << endl;
    tukar(a, b);
    cout << "Setelah ditukar: a = " << a << ", b = " << b << endl;
    return 0;
}

void tukar(int &x, int &y)
{
    int temp = x;
    x = y;
    y = temp;
}

```

> Screenshoot  
> ![Screenshot Soal 2](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/Guided%202%20aritmatika.png)

Program ini menukar nilai dua variabel menggunakan call by reference. Variabel a dan b dikirim ke fungsi tukar sebagai referensi, sehingga perubahan pada x dan y langsung mempengaruhi nilai asli a dan b. Hasilnya, setelah fungsi dipanggil, nilai a dan b tertukar.

## Unguided

### Soal 1

Buatlah sebuah program untuk melakukan transpose pada sebuah matriks persegi berukuran 3x3. Operasi transpose adalah mengubah baris menjadi kolom dan sebaliknya. Inisialisasi matriks awal di dalam kode, kemudian buat logika untuk melakukan transpose dan simpan hasilnya ke dalam matriks baru. Terakhir, tampilkan matriks awal dan matriks hasil transpose.

```cpp
#include <iostream>
using namespace std;

int main() {
    int matriks[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int transpose[3][3]; 

    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            transpose[j][i] = matriks[i][j];
        }
    }

    cout << "Matriks Awal:\n";
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << matriks[i][j] << " ";
        }
        cout << endl;
    }

    cout << "\nMatriks Hasil Transpose:\n";
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            cout << transpose[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}

```

> Screenshoot  
> ![Screenshot Soal 1](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/soal%201.png)

Program ini melakukan transpose matriks 3×3. Matriks awal disimpan dalam array matriks, lalu tiap elemen [i][j] dipindahkan ke posisi [j][i] pada array transpose. Setelah proses itu, program menampilkan matriks awal dan hasil transpose, di mana baris dan kolomnya saling bertukar.
---

### Soal 2

Buatlah program yang menunjukkan penggunaan call by reference. Buat sebuah prosedur bernama kuadratkan yang menerima satu parameter integer secara referensi (&). Prosedur ini akan mengubah nilai asli variabel yang dilewatkan dengan nilai kuadratnya. Tampilkan nilai variabel di main() sebelum dan sesudah memanggil prosedur untuk membuktikan perubahannya. 

```cpp
#include <iostream>
using namespace std;

void kuadratkan(int &x) {   
    x = x * x;
}

int main()
{
    int angka = 5;
    cout << "Nilai awal: " << angka << endl;
    kuadratkan(angka);
    cout << "Nilai setelah dikuadratkan: " << angka << endl;
    return 0;
}

```

> Sreenshoot 
> ![Screenshot Soal 2](https://github.com/salfiayu/Modul-1/blob/main/Modul%201/screenshoot/soal%202.png)

Program ini menggunakan call by reference untuk mengubah nilai variabel. Nilai angka dikirim ke fungsi kuadratkan sebagai referensi, lalu nilainya dikalikan dengan dirinya sendiri. Karena referensi mengacu langsung ke variabel asli, nilai angka di main ikut berubah menjadi hasil kuadratnya.

## Referensi

1. https://tahtamedia.co.id/index.php/issj/article/download/376/374/1410 (diakses 29-09-2025)
