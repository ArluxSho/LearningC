# Array Multidimensi 
**Array multidimensi** (*multidimensional array*) adalah array yang memiliki lebih dari satu baris. Perhatikan potongan kode di bawah ini.

```c
int arr[] = { 1, 2, 3, 4, 5 };
```

Dalam memori akan direpresentasikan sebagai:

```
arr[0] -> 1
arr[1] -> 2
arr[2] -> 3
arr[3] -> 4
arr[4] -> 5
```

**Array multidimensi** dapat menjawab pertanyaan tersebut. Array multidimensi dapat dideklarasikan seperti potongan kode di bawah ini.

```c
int x[3][4];
```

Elemen-elemen dalam di atas dapat direpresentasikan sebagai:

![Representasi array 2 dimensi](https://cdn.programiz.com/sites/tutorial2program/files/two-dimensional-array_0.jpg)

Selain itu, kita juga dapat membuat array dengan dimensi yang lebih besar, seperti array tiga dimensi. Kita dapat mendeklarasikannya seperti potongan kode di bawah ini.

```c
int arr[2][3][4];
```


## Syntax
Secara umum, multidimentional array dideklarasikan dengan bentuk:

```
data_type name_of_array [size1] [size2] ... [sizeN];
```

Sebagai contoh:

```
int a [3][4];        // 2 dimentional array
int a [3][4][7];     // 3 dimentional array
```


## Menghitung size of Array

Ukuran dari multidimentional array dapat dicari dengan mengoperasikan perkalian ke seluruh dimensi. Sebagai contoh:

```
size of a [10][20] = 10 * 20 = 200
```

200 adalah jumlah elemen yang dapat disimpan dalam array 

```
size of a [2][3][4] = 2 * 3 * 4 = 24
```

Jadi, jumlah elemen yang dapat disimpan dalam array adalah 24

## Two dimentional array

### Visualisasi
Jika ada arr [4][5]; visualisasinya adalah:
```
  [0.0] [0.1] [0.2] [0.3] [0.4]    5 kolom / column
  [1.0] [1.1] [1.2] [1.3] [1.4]
  [2.0] [2.1] [2.2] [2.2] [2.4]
  [3.0] [3.1] [3.2] [3.3] [3.4]

4 row / baris
```
Jadi, 4 adalah baris (row) dan 5 adalah kolom (column).

### Inisialisasi 
**A. Method 1**
```c
int a [2][3] = {1, 2, 3, 4, 5, 6};
```
Kekurangan: terkadang masih membingungkan.

**B. Method 2**
```c
int a [2][3] = {{1, 2, 3} ,  {4, 5, 6}};
```
Paling umum digunakan saat ini.

**C. Method 3**
```c
int arr[2][3];

arr[0][0] = 1;
arr[0][1] = 2;
arr[1][0] = 3;
arr[1][1] = 4;
```
Kekurangan: membutuhkan banyak line.

**Visualisasi array akan menjadi:**
```
       0   1   2
   0  [1] [2] [3]
   1  [4] [5] [6]
```
Ingat, index dimulai dari 0;

### Cara Akses
**Menggunakan kolom dan baris**
```
       0   1   2
   0  [1] [2] [3]
   1  [4] [5] [6]
```
a [0][1] = 2

### Cara print
**A. Dengan nested loop**
```c
int a [2][3] = {{1, 2, 3} , {4, 5, 6}}

for (int i = 0; i<2; i++){
  for (int j = 0; j<3; j++) {
  printf ("%d ", a[i][j]);
  }

  printf ("\n");
}
```
Cek jika secara visualisasi
```
       0   1   2
   0  [1] [2] [3]
   1  [4] [5] [6]

iterasi 1: i=0 j=0 a[0][0]
iterasi 2: i=0 j=1 a[0][1]
iterasi 3: i=0 j=2 a[0][2]
iterasi 4: i=1 j=0 a[1][0]
iterasi 5: i=1 j=1 a[1][1]
iterasi 6: i=1 j=2 a[1][2]
```

Output yang muncul adalah:
```
1 2 3
4 5 6 
```


## Three dimentional array

### Visualisasi
Saat kita memiliki array:
```c
int arr [2][3][3]
```
Visualisasinya akan menjadi: 

```
  [] [] []          [] [] []
  [] [] []          [] [] []
  [] [] []          [] [] []
        3 x 3              3 x 3 
```

### Inisialisasi 

**A. Method 1**
```c
int a[2][2][3] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12};
```

**B. Method 2**
```c
int a[2][2][3] = {{1, 2, 3} , {4, 5, 6} , {7, 8, 9} , {10, 11, 12}};
```

Visualisasinya akan menjadi 
```
   [1] [2] [3]         [7 ] [8 ] [ 9]
   [4] [5] [6]         [10] [11] [12]
```

### Cara print
Jika array satu dimensi menggunakan single for loop, array dua dimensi menggunakan 2 for loop, maka 3 dimensi array menggunakan 3 for loop atau three nested for loops.

Jika ada array:
```c
int a[2][2][3] = {{1, 2, 3} , {4, 5, 6} , {7, 8, 9} , {10, 11, 12}};
```

Maka, souce code untuk print seluruh elemen array adalah:
```c
#include <stdio.h>

int main() {
    int a[2][2][3] = {{ {1, 2, 3}, {4, 5, 6} },{ {7, 8, 9}, {10, 11, 12} }};

    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            for (int k = 0; k < 3; k++) {
                printf("%d ", a[i][j][k]);
            }
            printf("\n"); // pindah baris per row
        }
        printf("\n"); // spasi antar layer
    }
    return 0;
}
```
