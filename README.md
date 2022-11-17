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

# Tugas 8: Flutter Form


##  Perbedaan `Navigator.push` dan `Navigator.pushReplacement`
`Navigator.push` menambahkan `Route` ke *top of stack* dari `Navigator`. Sedangkan `Navigator.pushReplacement`, selain menambahkannya ke *top of stack* juga menghilangkan `Route` yang sebelumnya.

##  *Widget* yang Digunakan
1. `Text`,
    Menampilkan sebuah *string* dengan *single style*.
2. `Column`,
    Sebuah *widget* yang menampilkan *children*-nya secara vertikal.
3. `Row`,
    Sebuah *widget* yang menampilkan *children*-nya secara horizontal.
4. `Scaffold`,
    Menerapkan dasar dari *visual layout* Material Design.
5. `AppBar`,
    *App bar* dari Material Design
6. `Padding`,
    Memberi *padding* pada *child* yang diletakkan di dalamnya.
7. `Center`,
    Sebuah *widget* yang *child*-nya akan berposisi di tengah.
8. `Drawer`,
    Panel yang berdiri secara horizontal di pinggir `Scaffold` yang menampilkan tautan navigasi dalam aplikasi.
9. `ListTile`,
    Sebuah baris yang biasanya mengandung teks dan ikon.
10. `Navigator`,
    Mengelola *child widgets* menggunakan prinsip *stack*.
11. `MaterialPageRoute`,
    Rute modal yang menggantikan seluruh layar dengan transisi platform-adaptif.
12. `SingleChildScrollView`,
    Digunakan agar *child*-nya bisa di-*scroll*.
13. `Container`,
    *Widget* yang menggabungkan *widget* umum untuk *painting*, *positioning*, dan *sizing*.
14. `Card`,
    Sebuah panel yang bisa digunakan untuk menampilkan informasi di dalamnya. Memiliki *style* dimana sudutnya sedikit bulat dan terdapat bayangan elevasi.
15. `CustomScrollView`,
    Kurang lebih sama dengan `SingleChildScrollView` namun lebih fleksibel.
16. `SliverFillRemainingFill`,
    Sebuah *sliver* yang mengandung sebuah *box child* yang mengisi sisa ruang pada *viewport*.
17. `Form`,
    *Containter* untuk melakukan *grouping* terhadap beberapa *form field widget*.
18. `TextFormField`,
    *Field* teks yang bisa digunakan untuk melakukan *input*.
19. `InputDecoration`,
    Melakukan dekorasi pada sebuah *input field*.
20. `DropdownButtonFormField`,
    Menu *dropdown*.
21. `Expanded`,
    Melebarkan *child* dari `Row`, `Column`, atau `Flex` agar mengisi ruang yang masih tersedia.
22. `Align`,
    Melakukan *aligining* terhadap *child*-nya.
23. `TextButton`,
    Tombol yang berisi teks.

##  Jenis-jenis *event* pada FLutter 
1.  `onPressed`
2.  `onLongPress`
3.  `onSaved`
4.  `onTap`

##  Cara kerja `Navigator`
`Navigator` menggunakan prinsip *stack* dalam mengganti halaman. Halaman yang ditampilkan adalah yang berada pada *top of stack*.

##  Implementasi
* Membuat *form*
* Membuat *input field* yang dinginkan mengacu pada soal
* Menyimpan Data-data yang di-input ke dalam sebuah `List`
* Menyimpan data dalam bentuk `Card`
* Menampilkan data pada halaman Data Budget sesuai dengan yang sudah ditambahkan dengan memanfaatkan `List` yang sudah dibuat tadi