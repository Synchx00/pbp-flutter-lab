# Tugas 7: Elemen Dasar Flutter

## *Stateful and Stateless Widget*

*Stateful Widget* adalah *widget* yang memiliki objek State yang mengandung *fields* yang dapat mempengaruhi tampilannya. Jadi, *stateful widget* dapat berubah ketika pengguna berinteraksi dengannya. 
*Stateless widget* merupakan kebalikan dari *stateful widget*. Ketika sudah dibuat, *state* dari *widget* ini tidak dapat diubah.

## *Widget* yang Digunakan

1. `Text`,
    Menampilkan sebuah *string* dengan *single style*.
2. `Icon`,
    Menampilkan sebuah ikon.
3. `Column`,
    Sebuah *widget* yang menampilkan *children*-nya secara vertikal.
4. `Row`,
    Sebuah *widget* yang menampilkan *children*-nya secara horizontal.
5. `Scaffold`,
    Menerapkan dasar dari *visual layout* Material Design.
6. `AppBar`,
    *App bar* dari Material Design
7. `Padding`,
    Memberi *padding* pada *child* yang diletakkan di dalamnya.
8. `FloatingActionButton`,
    Membuat tombol yang dapat melakukan sebuah *action*
9. `Center`,
    Sebuah *widget* yang *child*-nya akan berposisi di tengah.
10. `Visibility`,
    Menampilkan *child*-nya tergantung dengan nilai *field* `visible`.

## `setState`

Method ini digunakan jika ingin melakukan perubahan pada tampilan app secara langsung. `setState` akan menginfokan *framework* Flutter bahwa ada sesuatu yang berubah, yang mengakibatkan *method* `build` di-*rerun* sehingga menampilkan perubahan yang terjadi. Pada tugas ini, yang berubah adalah nilai dari variabel `_counter`. Namun yang berubah di tampilan tidak hanya nilai angka saja, karena `_counter` juga mempengaruhi teks yang ditampilkan. Ketika *method* `build` di-*rerun* dan nilai `_counter` sudah berubah, maka teks yang ditampilkan akan sesuai dengan kondisi *ternary* yang diberikan.

## Perbedaan `const` dan `final`

- `const` menjadikan sebuah variabel menjadi konstan ketika program di-*compile*
- `final` menyebabkan sebuah variabel tidak dapat diubah nilainya

## Implementasi

1. Membuat *function* `_decrementCounter` yang digunakan untuk mengurangi nilai `_counter`
2. Membuat *conditionals* pada *widget* `Text` yang menampilkan *EVEN* berwarna merah atau *ODD* berwarna biru
3. Membuat *function* `_setVisible` yang digunakan untuk mengubah nilai `_isVisible`
4. Memanggil *function* `_setVisible` di *function* `_incrementCounter`dan *function* `_decrementCounter`
5. Menambahkan *property*: *visible* pada *button* kurang

## Bonus

Menambahkan *property*: *visible* pada button kurang yang berguna untuk menghilangkan *button* kurang jika nilai `_counter = 0`