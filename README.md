# Course-Summary 📋:
___
## 📚 Struktur Data Stack dan Queue.
### - [📖 Tipe Struktur Data.]
  Terdapat dua tipe dasar struktur data berdasarkan cara akses elemen:

- Random Access Data Structures (Struktur Data Akses Acak).
- Sequential Access Data Structures (Struktur Data Akses Sekuensial).

### - [📖 Random Access Data Structures.]

![image](https://github.com/user-attachments/assets/b696ab3b-7ae2-4f5d-806e-54b0a1d5bbbf)

- Array adalah contoh struktur data dengan akses acak. Dalam gambar ini, kita bisa melihat bagaimana setiap elemen array dapat diakses langsung menggunakan indeksnya. Misalnya, elemen '8' dapat diakses melalui indeks '1'.

- Adapun sifat-sifat dari array:
  1. **Independen** – Setiap elemen tidak bergantung pada elemen lainnya.  
  2. **Akses Fleksibel** – Elemen dapat diakses dengan berbagai cara.  
  3. **Waktu Konstan (O(1))** – Akses ke elemen sangat cepat.  
  4. **Terbatas** – Jumlah elemen ditentukan sejak awal.

### - [📖 Sequential Access Data Structures.]

- Terdiri dari stack, queue, dan linked list.

- Adapun sifat-sifat dari struktur data ini:
  1. Setiap elemen dependen (bergantung) pada elemen lainnya.
  2. Hanya dapat diakses dalam urutan tertentu.
  3. Elemen tertentu hanya dapat diperoleh melalui elemen lainnya.
  4. Tidak menyediakan akses O(1).
  5. Jumlah elemen tidak terbatas.

## 🗄️ Stack
- Definisi stack:
  - 📑 "Struktur data akses sekuensial di mana elemen ditambahkan dan dihapus berdasarkan prinsip LIFO (Last In, First Out)."
    
    ![image](https://github.com/user-attachments/assets/eb772597-c853-4683-898f-3e305a1e7f06)
    
  - Gambar di atas menggambarkan bagaimana elemen-elemen dalam stack disusun. Elemen terakhir yang masuk (dalam hal ini, "3") akan menjadi elemen pertama yang keluar. Ini adalah prinsip dasar LIFO yang mendefinisikan cara kerja stack.
  - 🗒️ Note: Stack dapat diimplementasikan menggunakan Array atau Linked list.

## 🔧 Implementasi Stack di C++ dengan OOP
  - ### 🚀 Menggunakan 'vector' dari STL
    ![image](https://github.com/user-attachments/assets/5020b699-c914-4106-82dc-29b4b218ef95)
  - ### 🚀 Menggunakan 'stack' dari STL
    ![image](https://github.com/user-attachments/assets/58a2df98-69be-407c-b12d-49ce61b0fdda)
  - ### 🚀 Menggunakan Linked List
    ![image](https://github.com/user-attachments/assets/13eefdfc-ee30-4daf-bf5b-314665a8d72d)

## 💾 Vector
  - Vector adalah array dinamis yang bisa bertambah ukurannya secara otomatis saat diperlukan.
  - Sifat-sifat vector:
    1. Disimpan secara berurutan dalam memori.
    2. Akses elemen O(1).
    3. Jika kapasitas penuh, dialokasikan ulang ke blok memori baru.
    4. Tidak menggunakan pointer untuk menyambungkan elemen.

## 📊 Perbandingan `vector<int>` vs `linked list`

  | Operasi                         | `vector<int>` (Array Dinamis)                                                | `linked list` (Node dengan Pointer)                                           |
  |---------------------------------|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
  | 📥 **Push** (`push_back` / `push`) | ✅ O(1) *(rata-rata, kecuali realokasi)*                                     | ✅ O(1)                                                                        |
  | 📤 **Pop** (`pop_back` / `pop`)   | ✅ O(1)                                                                       | ✅ O(1)                                                                        |
  | 👀 **Akses Elemen Teratas** (`back()` / `top()`) | ✅ O(1)                                                            | ✅ O(1)                                                                        |
  | 🧠 **Alokasi Memori**            | ❌ Kadang perlu realokasi *(saat kapasitas habis, O(n))*                     | ✅ Tidak butuh realokasi besar, hanya alokasi node baru                       |
  | ⚙️ **Cache Friendly** *(Akses Memori Cepat)* | ✅ Ya *(bersebelahan di memori, cepat diakses CPU)*              | ❌ Tidak *(tersebar di memori, lambat karena pointer traversal)*             |

  - Tabel di atas membandingkan operasi-operasi antara vector (array dinamis) dan linked list (node dengan pointer). Perhatikan bagaimana setiap struktur data memiliki keunggulan dan kelemahan dalam hal efisiensi operasi, alokasi memori, dan cache-friendliness.

### Kapan harus menggunakan vector❓

- Jika ukuran stack dapat diperkirakan dan tidak sering berubah.
- Jika memerlukan akses cepat ke elemen teratas dengan O(1) waktu dan 'pop()'.
- Jika ingin memanfaatkan cache CPU untuk akses cepat.
- Jika ingin menghindari overhead pointer untuk 'push()'.

### Kapan Harus Menggunakan Linked List❓

- Jika ukuran stack tidak diketahui atau sering berubah.
- Jika sering melakukan operasi 'push' dan 'pop' di awal stack (paling bawah).
- Jika ingin menghindari overhead realokasi pada vector.

### Kapan Harus Menggunakan Stack dari STL❓

- Jika menggunakan abstraksi tinggi dan tidak perlu kontrol manual atas memori.
- Jika ingin implementasi yang cepat dan sederhana tanpa harus menulis kode sendiri.
- Jika ingin memilih backend yang sesuai (deque, vector, atau list).

## Operasi Dasar Stack 📇

  1. **Push**: Menambahkan elemen ke atas Stack.
  2. **Pop**: Menghapus elemen atas pada Stack (paling atas).

     ![image](https://github.com/user-attachments/assets/febd9274-c657-4af0-a82e-f4a4a455afc2)
     
  4. **Peek**: Melihat elemen paling atas Stack tanpa menghapusnya.
  5. **Contains**: Mencari elemen dalam Stack.
  6. **isFull**: Memeriksa apakah Stack sudah penuh.
  7. **isEmpty**: Memeriksa apakah Stack kosong.
  8. **Count**: Menghitung jumlah elemen pada Stack.
  9. **Change**: Mengubah data pada posisi tertentu.
  10. **Display**: Mencetak semua elemen pada Stack.
  11. **Destroy**: Menghapus/membersihkan semua elemen pada Stack.
    
## 💡Implementasi Stack 🔧

  - Tombol Back dan Next pada browser.
  - Tombol Undo dan Redo pada aplikasi.
  - Algoritma Rekursi (contoh: menghitung Faktorial).
  - Evaluasi Ekspresi Postfix.
  - Pencarian rute labirin (Depth-First Search (DFS) dan backtracking).

## Evaluasi Notasi Postfix 📌
  
  - Evaluasi notasi postfix adalah salah satu contoh implementasi stack. Notasi postfix (atau notasi Polish terbalik) adalah cara menulis ekspresi matematika di mana operator ditulis setelah operand. Stack sangat berguna dalam mengevaluasi ekspresi semacam ini karena memungkinkan kita untuk menyimpan operand dan menerapkan operator sesuai urutan yang benar.

  - Contoh:

    **Infix** → `1 + ((2 + 3) * 4 + 5) * 6 = 151`

    **Postfix** → `1 2 3 + 4 * 5 + 6 * + = 151`

    ---

    | **Ekspresi** | 1 | 2 | 3 | + | 4 | * | 5 | + | 6 | * | + |
    |-------------|---|---|---|---|---|---|---|---|---|---|---|
    | **Stack**   | 1 | 2 | 3 |   | 4 |   | 5 |   | 6 |   |   |
    |             |   |   |   | 5 |   |20 |   |25 |   |150|   |
    |             | 1 | 2 |   |   | 1 |   | 1 |   | 1 |   |151|
    | **Aksi Stack** | push | push | push | pop | push | pop | push | pop | push | pop | pop |
    |             |       |       |       |     |       | pop |       | pop |       | pop | pop |
    |             |       |       |       |     |       | push |       | push |       | push | push |
    | **Perhitungan** |       |       |       | 3+2 |       | 5*4 |       | 5+20 |       | 6*25 | 150+1 |
    | **Hasil**   |       |       |       | 5   |       | 20  |       | 25   |       | 150  | 151  |

## DFS dan Backtracking 🔍
- Dalam konteks pencarian rute atau solusi, stack sering digunakan untuk mengimplementasikan algoritma Depth-First Search (DFS) dan backtracking. DFS adalah metode untuk menjelajahi pohon atau graf dengan pergi sedalam mungkin ke setiap cabang sebelum melakukan backtracking.

  ![image](https://github.com/user-attachments/assets/d7fafa92-da8e-4664-8d9a-3e7fe582eec0)
  
- Contoh urutan DFS: 1 2 5 6 9 3 7 10 11 8 12 4 Contoh urutan Backtracking: 4 12 8 11 10 7 3 9 6 5 2 1

## Kompleksitas Implementasi dengan Array atau Linked List

  ![image](https://github.com/user-attachments/assets/48ef3123-b0e0-411d-ab5c-2f636c5fa94c)

| **Operasi** | **`vector<int>` (Array Dinamis)** | **`linked list` (Node dengan Pointer)** |
|-------------|-----------------------------------|------------------------------------------|
| **Push** (`push_back`) | 🟢 O(1) *(rata-rata)* 🔴 O(n) *(jika realokasi terjadi)* | 🟢 O(1) |
| **Pop** (`pop_back`) | 🟢 O(1) | 🟢 O(1) |
| **Akses Elemen Teratas** (`back()` / `top()`) | 🟢 O(1) | 🟢 O(1) |
| **Akses Elemen Secara Acak** | 🟢 O(1) | 🔴 O(n) |
| **Alokasi Memori** | 🔴 O(n) *(jika realokasi terjadi)* | 🟢 O(1) *(alokasi per node)* |
| **Pembersihan Memori** *(Destructor)* | 🔴 O(1) | 🔴 O(n) *(menghapus node satu per satu)* |

## Queue
- Definisi stack:
  - 📑 "Struktur data akses sekuensial di mana elemen ditambahkan dan dihapus berdasarkan prinsip FIFO (First In, First Out)."
  - Queue dapat diimplementasikan menggunakan Array atau Linked list.

## Implementasi Queue di C++ dengan OOP
- ### Menggunakan 'vector' dari STL
  ![image](https://github.com/user-attachments/assets/7ee1a5e5-c2e4-4356-844d-a6de96605aa0)
- ### Menggunakan 'deque' dari STL
  ![image](https://github.com/user-attachments/assets/3075694f-0e8f-4cb1-bfa0-14aa8655cf1e)
- ### Menggunakan Linked List
  ![image](https://github.com/user-attachments/assets/39f8dbc1-05fc-4996-83e9-fd8a47c9a4dd)

## 📊Perbandingan Vector vs Linked List vs Deque

  | **Kebutuhan** | **Vector (`std::vector`)** | **Linked List (`std::list`)** | **Deque (`std::deque`)** |
  |---------------|-----------------------------|-------------------------------|---------------------------|
  | Akses cepat ke elemen *(random access)* | ✅ Ya (`O(1)`) | ❌ Tidak (`O(n)`) | ⚠️ Lumayan (`O(1)`, tapi lebih lambat dari vector) |
  | Tambah/hapus elemen di akhir | ✅ Ya (`O(1)`) | ✅ Ya (`O(1)`) | ✅ Ya (`O(1)`) |
  | Tambah/hapus elemen di awal | ❌ Tidak (`O(n)`) | ✅ Ya (`O(1)`) | ✅ Ya (`O(1)`) |
  | Tambah/hapus elemen di tengah | ❌ Tidak (`O(n)`) | ✅ Ya (`O(1)`) | ⚠️ Bisa, tapi tidak optimal |
  | Cache-friendly *(kontigu di memori)* | ✅ Ya | ❌ Tidak | ❌ Tidak |
  | Butuh fleksibilitas di kedua ujung | ❌ Tidak | ⚠️ Bisa, tapi ↕️ tidak optimal | ✅ Ya |

### Kapan harus menggunakan vector❓
  - Jika jumlah elemen relatif kecil.
  - Jika lebih banyak operasi 'enqueue' dibandingkan 'dequeue'.
  - Jika ingin akses elemen cepat menggunakan indeks (random access).

### Kapan harus menggunakan vector❓
  - Jika sering melakukan 'enqueue' dan 'dequeue' (kedua operasi sama-sama O(1)).
  - Jika jumlah elemen sering berubah-ubah (tidak perlu alokasi ulang seperti vector).

### Kapan harus menggunakan vector❓
  - Jika ingin performa hampir sama dengan list tetapi dengan efisiensi memori lebih baik.
  - Jika memerlukan 'enqueue' dan 'dequeue' yang cepat (O(1)) tanpa overhead pointer seperti list.
  - Jika butuh akses acak lebih cepat dibanding list.

## Operasi Dasar Queue
  1. Enqueue: Menambahkan elemen ke antrian.
  2. Dequeue: Menghapus elemen pertama pada antrian.
     
     ![image](https://github.com/user-attachments/assets/49913981-e229-45eb-8b70-1f68b57e223c)

  3. Peek: Melihat elemen paling atas pada Queue tanpa menghapusnya.
  4. Contains: Mencari elemen dalam Queue.
  5. isEmpty: Memeriksa apakah Queue kosong.

     ![image](https://github.com/user-attachments/assets/5c3db294-6682-4598-9cca-cb0ed6ec1ca0)

  6. Display: Mencetak semua elemen dalam Queue.
  7. Destroy: Menghapus atau membersihkan semua elemen dalam Queue.

     ![image](https://github.com/user-attachments/assets/bdd558d9-68d1-44f9-9d5e-0afd64b1efbb)

## 💡Implementasi Queue 🔧
  - Queue sering digunakan dalam berbagai aplikasi, termasuk:
    1. Job scheduling: Mengatur urutan eksekusi pekerjaan.
    2. Printer queueing: Mengatur urutan dokumen yang akan dicetak.

## Tambahan
### Kompleksitas dibawah ini adalah kompleksitas Linked list
![image](https://github.com/user-attachments/assets/903b2c35-f048-46a2-b28e-4491987d55ba)
