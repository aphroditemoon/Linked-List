<div align="center">

# 🔗 Linked List in C

### Implementasi **Doubly Linked List** sederhana menggunakan bahasa C  
Program ini mendemonstrasikan proses **insert**, **delete**, **print**, dan **clear data** pada struktur data linked list.

<br>

![C](https://img.shields.io/badge/Language-C-blue?style=for-the-badge&logo=c)
![Data Structure](https://img.shields.io/badge/Data%20Structure-Doubly%20Linked%20List-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

</div>

---

## 📌 Deskripsi Project

Project ini dibuat untuk memahami konsep dasar **Doubly Linked List** dalam bahasa C.  
Linked list yang digunakan memiliki pointer **next** dan **prev**, sehingga setiap node dapat terhubung ke node setelahnya dan node sebelumnya.

Program ini menggunakan tiga pointer utama:

| Pointer | Fungsi |
|---|---|
| `head` | Menunjuk node pertama dalam list |
| `tail` | Menunjuk node terakhir dalam list |
| `curr` | Pointer bantu untuk proses traversal atau pencarian data |

---

## ✨ Fitur Utama

✅ Menambahkan data di depan list  
✅ Menambahkan data di belakang list  
✅ Menambahkan data setelah nilai tertentu  
✅ Menghapus data dari depan list  
✅ Menghapus data dari belakang list  
✅ Menghapus data berdasarkan nilai tertentu  
✅ Menghapus seluruh data dari list  
✅ Menampilkan isi linked list dari depan ke belakang  

---

## 🧠 Konsep yang Digunakan

Project ini mencakup beberapa konsep penting dalam bahasa C dan struktur data:

- `struct` untuk membuat node
- Pointer `next` dan `prev`
- Alokasi memori dinamis menggunakan `malloc()`
- Penghapusan memori menggunakan `free()`
- Traversal linked list
- Kondisi khusus saat list kosong
- Kondisi khusus saat hanya ada satu node
- Operasi insert dan delete pada doubly linked list

---

## 🏗️ Struktur Node

Setiap node pada program ini memiliki tiga bagian utama:

```c
struct tnode
{
    int x;
    struct tnode *next;
    struct tnode *prev;
};
```

Penjelasan:

| Bagian | Keterangan |
|---|---|
| `x` | Menyimpan nilai integer |
| `next` | Menunjuk node berikutnya |
| `prev` | Menunjuk node sebelumnya |

---

## ⚙️ Daftar Function

| Function | Deskripsi |
|---|---|
| `push_front(int value)` | Menambahkan data ke bagian depan list |
| `push_back(int value)` | Menambahkan data ke bagian belakang list |
| `push_mid(int value, int searchKey)` | Menambahkan data setelah nilai tertentu |
| `delete_front()` | Menghapus data paling depan |
| `delete_back()` | Menghapus data paling belakang |
| `delete_mid(int searchKey)` | Menghapus data berdasarkan nilai tertentu |
| `clearData()` | Menghapus semua data dalam list |
| `printList()` | Menampilkan semua data dalam list |

---

## 🔄 Alur Program

Program menjalankan beberapa operasi linked list secara berurutan:

```c
push_front(11);
push_back(90);
push_front(78);
push_back(50);
```

Hasil awal list:

```text
78 11 90 50
```

Kemudian program melakukan insert dan delete:

```text
Insert after 90  -> 78 11 90 22 50
Insert after 78  -> 78 18 11 90 22 50
Delete front     -> 18 11 90 22 50
Delete back      -> 18 11 90 22
Delete 90        -> 18 11 22
Delete all       -> There is No Data
```

---

## 🖥️ Contoh Output Program

```text
PUSH DATA
List: 78 11 90 50

Insert after 90
List: 78 11 90 22 50

Insert after 78
List: 78 18 11 90 22 50

Delete front
List: 18 11 90 22 50

Delete back
List: 18 11 90 22

Delete 90
List: 18 11 22

Delete all
There is No Data
```

---

## 🚀 Cara Menjalankan Program

### 1. Clone repository

```bash
git clone https://github.com/aphroditemoon/Linked-List.git
cd Linked-List
```

### 2. Compile program

Jika file kamu menggunakan ekstensi `.c`, gunakan:

```bash
gcc Tugas.c -o linkedlist
```

Jika file kamu bernama `Tugas` atau `Tugas.txt`, gunakan:

```bash
gcc -x c Tugas -o linkedlist
```

atau:

```bash
gcc -x c Tugas.txt -o linkedlist
```

### 3. Jalankan program

Untuk Windows:

```bash
linkedlist
```

Untuk Linux atau macOS:

```bash
./linkedlist
```

---

## 📂 Struktur Repository

```text
Linked-List/
│
├── Tugas
└── README.md
```

---

## 📊 Visualisasi Sederhana

Contoh bentuk doubly linked list:

```text
NULL <- [78] <-> [11] <-> [90] <-> [50] -> NULL
```

Setelah menjalankan:

```c
push_mid(22, 90);
```

Maka list menjadi:

```text
NULL <- [78] <-> [11] <-> [90] <-> [22] <-> [50] -> NULL
```

---

## 🎯 Tujuan Project

Project ini bertujuan untuk melatih pemahaman mengenai cara kerja linked list, terutama pada operasi dasar seperti penambahan data, penghapusan data, dan pengelolaan pointer di dalam bahasa C.

Dengan memahami project ini, pengguna dapat lebih mudah mempelajari struktur data lanjutan seperti:

- Stack
- Queue
- Tree
- Graph
- Hash Table

---

## 📝 Catatan Pengembangan

Beberapa ide pengembangan yang dapat ditambahkan ke depannya:

- Menambahkan menu interaktif untuk input dari user
- Menambahkan fitur pencarian data
- Menampilkan list dari belakang ke depan menggunakan pointer `prev`
- Menambahkan validasi alokasi memori setelah `malloc()`
- Membuat tampilan output lebih rapi dan informatif

---

## 👨‍💻 Author

**Erlangga Putra Mahardika**  
Repository: `Linked-List`

---

<div align="center">

### ⭐ Terima kasih sudah membaca project ini!

Jika project ini membantu, jangan lupa beri ⭐ pada repository ini.

</div>
