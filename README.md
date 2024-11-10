JOBSHEET 10

Nama : Febby Mathelda Silvya Mooy

Kelas : TI-3A

NIM : 2241720067

Tugas Praktikum 1: Dasar State dengan Model-View

1. Selesaikan langkah-langkah praktikum tersebut, lalu dokumentasikan berupa GIF hasil akhir praktikum beserta penjelasannya di file README.md! Jika Anda menemukan ada yang error atau tidak berjalan dengan baik, silakan diperbaiki.

Jawab:

2. Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian?

Jawab:

Langkah 4 bertujuan untuk mempermudah manajemen dan aksesibilitas kode dalam aplikasi, terutama saat aplikasi berkembang dan memiliki banyak file model. Dengan membuat file data_layer.dart yang hanya berisi perintah export
dalam kode ini membungkus beberapa model (seperti plan.dart dan task.dart) ke dalam satu file ekspor. Ini memungkinkan kode untuk mengimpor kedua model tersebut secara bersamaan hanya dengan mengimpor data_layer.dart, sehingga tidak perlu menulis beberapa perintah import untuk setiap model di file lain. Pendekatan ini membuat kode lebih ringkas, lebih terorganisir, dan lebih mudah dikelola, terutama saat jumlah file model bertambah.


3. Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta ?

Jawab:

Variabel plan di langkah 6 berfungsi sebagai model data yang merepresentasikan rencana atau daftar tugas yang akan ditampilkan dan dimodifikasi di aplikasi. Variabel ini dibuat sebagai Plan untuk menyimpan daftar tugas (tasks) yang nantinya dapat diperbarui sesuai interaksi pengguna, misalnya menambahkan atau menyelesaikan tugas.

Alasan Plan dibuat sebagai konstanta (const Plan();) adalah agar nilai awalnya tidak berubah saat pertama kali diinisialisasi. Dengan menjadikannya konstanta, kita memastikan bahwa plan dimulai dengan data default yang tidak berubah, seperti objek Plan kosong atau dengan nilai tertentu yang tidak akan diubah hingga ada tindakan dari pengguna (seperti menambahkan tugas).

Setelah diinisialisasi, variabel ini nantinya dapat diperbarui saat pengguna menambahkan tugas atau memperbarui daftar tugas, tetapi tetap dimulai sebagai nilai yang stabil dan kosong.

4. Lakukan capture hasil dari Langkah 9 berupa GIF, kemudian jelaskan apa yang telah Anda buat!

Jawab:

https://github.com/febbymathelda/master_plan/blob/main/lib/images/praktikum1.mp4

5. Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state ?

Jawab:

Pada langkah 11 dan 13, kita menggunakan dua metode penting dalam lifecycle State pada Flutter: initState() dan dispose(). Keduanya berguna untuk mengelola sumber daya atau objek yang hanya dibutuhkan saat widget aktif, sehingga membantu menjaga kinerja aplikasi tetap optimal dan mencegah kebocoran memori.

Langkah 11: initState()

initState() adalah metode lifecycle yang pertama kali dipanggil saat sebuah widget stateful diinisialisasi.
Pada langkah 11, inisialisasi ScrollController dan menambahkan Listener untuk mendeteksi pergerakan scroll. Listener ini berfungsi untuk menutup keyboard ketika pengguna mulai melakukan scroll, dengan memfokuskan kembali FocusNode ke posisi netral (tidak fokus pada input apapun).
Tujuan utamanya adalah mengelola respons aplikasi terhadap perubahan fokus, khususnya untuk menutup keyboard secara otomatis saat pengguna melakukan scroll pada layar, sehingga UI tetap bersih dan tidak tertutup oleh keyboard.


Langkah 13: dispose()
dispose() adalah metode lifecycle terakhir yang dipanggil sebelum sebuah widget dihapus dari pohon widget dan memori.
Di sini, memanggil scrollController.dispose(), yang berguna untuk membersihkan ScrollController dan membebaskan memori yang digunakan.
Menggunakan dispose() pada ScrollController (atau objek lain yang mengontrol sumber daya) sangat penting untuk menghindari kebocoran memori, karena memastikan semua sumber daya yang tidak diperlukan lagi dilepaskan ketika widget dihapus dari layar.

6. Kumpulkan laporan praktikum Anda berupa link commit atau repository GitHub ke dosen yang telah disepakati !

Tugas Praktikum 2: InheritedWidget


1. Selesaikan langkah-langkah praktikum tersebut, lalu dokumentasikan berupa GIF hasil akhir praktikum beserta penjelasannya di file README.md! Jika Anda menemukan ada yang error atau tidak berjalan dengan baik, silakan diperbaiki sesuai dengan tujuan aplikasi tersebut dibuat.

Jawab:


2. Jelaskan mana yang dimaksud InheritedWidget pada langkah 1 tersebut! Mengapa yang digunakan InheritedNotifier?

Jawab:


3. Jelaskan maksud dari method di langkah 3 pada praktikum tersebut! Mengapa dilakukan demikian?

Jawab:


4. Lakukan capture hasil dari Langkah 9 berupa GIF, kemudian jelaskan apa yang telah Anda buat!

Jawab:


5. Kumpulkan laporan praktikum Anda berupa link commit atau repository GitHub ke dosen yang telah disepakati !