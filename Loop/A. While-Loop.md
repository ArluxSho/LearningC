# Konsep Dasar Loop dengan "While"
**Loop** artinya mengulang suatu instruksi. `While` artinya selama kondisi bernilai benar, lakukan perintah. Dalam **While**, akan memeriksa kondisi terlebih dahulu untuk setelahnya menjalankan blok code.

# Syntax While
```c
while (kondisi) {
    // blok kode yang akan diulang
}
```
Kondisi ini berupa boolean (true/false). Selama kondisi bernilai **true**, blok akan dijalankan terus. Loop akan berhenti saat kondisi bernilai **false.**

# Contoh Program Sederhana
### Program untuk mencetak angka 1-5.
```c
#include <stdio.h>

int main() {
    int i = 1;            // inisialisasi
    while (i <= 5) {      // kondisi
        printf("%d\n", i);
        i++;              // update
    }
    return 0;
}
```
Output
```
1
2
3
4
5
```
### Program Kondisi Berbasis Input
```c
#include <stdio.h>

int main() {
    int angka;
    printf("Masukkan angka (0 untuk berhenti): ");
    scanf("%d", &angka);

    while (angka != 0) {
        printf("Anda memasukkan %d\n", angka);
        printf("Masukkan angka lagi (0 untuk berhenti): ");
        scanf("%d", &angka);
    }
    printf("Program selesai.");
    return 0;
}
```
# Latihan
### A. Buat program yang mencetak angka 10 sampai 1.
Output yang diharapkan:
```
10
9
8
7
6
5
4
3
2
1
```

<details>
<summary>Kunci jawaban Latihan A</summary>
  
```c
#include <stdio.h>
  
int main() {

    int i = 10;

    while ( i>0 ){
        printf ("%d ", i);
        i--;
    }
    return 0;
}
```
</details>

### B. Buat program yang menjumlahkan semua bilangan 1 sampai N input dari user dengan menggunakan perulangan While.

Misalkan input:
```
3
```

Output yang diharapkan:
```
6
```

<details>
<summary>Kunci jawaban Latihan B</summary>
  
```c
#include <stdio.h>

int main() {

    int n, sum = 0 ; //3
    int i = 1;

    printf("Masukan nilai N: ");
    scanf("%d", &n);

    while ( i <= n ){
        sum += i;
        i++;
    }

    printf ("%d", sum);

    return 0;
}
```
</details>
