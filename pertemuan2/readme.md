# **Implementasi Singly Linked List Menggunakan Python**

Program ini merupakan implementasi dasar struktur data Singly Linked List menggunakan bahasa Python.
Di dalamnya terdapat operasi untuk menambah, menghapus, menampilkan, dan menghitung jumlah elemen dalam list.
Kode ini dibuat untuk membantu memahami cara kerja pointer antar node serta bagaimana operasi dasar list dilakukan tanpa menggunakan struktur data bawaan Python.

---

## **1. Node Sebagai Penyimpan Data**

```python
class Node:
    def __init__(self, data=None, pointer=None):
        self.data = data
        self.next = pointer
```

Node digunakan untuk menyimpan nilai dan pointer ke node berikutnya sehingga setiap elemen dapat terhubung membentuk rantai data.

## **2. Inisialisasi Linked List**


```python
class LinkedList:
    def __init__(self):
        self.head = None
```

Kelas LinkedList memiliki pointer `head` sebagai penanda node pertama dan menjadi pusat dari semua operasi list.

## **3 Menambah Elemen di Awal (insert_at_first)**

```python
def insert_at_first(self, data):
    node = Node(data, self.head)
    self.head = node
```

Node baru ditempatkan di depan list dengan mengarahkannya ke head lama lalu menjadikannya sebagai head yang baru.

## **4 Menambah Elemen di Akhir (insert_at_last)**

```python
def insert_at_last(self, data):
    if self.head is None:
        self.head = Node(data)
    else:
        node_sekarang = self.head
        while node_sekarang.next:
            node_sekarang = node_sekarang.next

        node = Node(data)
        node_sekarang.next = node
```

Node baru ditambahkan di bagian akhir dengan menelusuri list hingga node terakhir lalu menautkan node baru di posisi tersebut.

## **5 Menambah Elemen pada Posisi Tertentu (insert_at)**

```python
def insert_at(self, index, data):
    if index < 0 or index > self.length() - 1:
        print("indeks tidak valid")
    elif index == 0:
        self.insert_at_first(data)
    else:
        urutan = 0
        node_sekarang = self.head

        while urutan < index - 1:
            urutan += 1
            node_sekarang = node_sekarang.next

        node = Node(data, node_sekarang.next)
        node_sekarang.next = node
```

Node disisipkan pada index tertentu dengan menemukan node sebelumnya lalu mengatur pointer agar node baru masuk di posisi yang diinginkan.

## **6 Menghapus Elemen Pertama (remove_first)**

```python
def remove_first(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
    else:
        self.head = self.head.next
```

Elemen pertama dihapus dengan menggeser head ke node berikutnya.

## **7 Menghapus Elemen Terakhir (remove_last)**

```python
def remove_last(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
    elif self.head.next is None:
        self.head = None
    else:
        node_sebelumnya = None
        node_sekarang = self.head

        while node_sekarang.next:
            node_sebelumnya = node_sekarang
            node_sekarang = node_sekarang.next

        node_sebelumnya.next = None
```

Proses ini menelusuri list hingga node paling akhir lalu memutus kaitan node sebelum terakhir sehingga node terakhir terhapus.

## **8 Menghapus Elemen Berdasarkan Posisi (remove_at)**

```python
def remove_at(self, index):
    if index < 0 or index >= self.length():
        print("index invalid")
    elif index == 0:
        self.remove_first()
    else:
        urutan = 0
        node_sekarang = self.head

        while urutan < index - 1:
            node_sekarang = node_sekarang.next
            urutan += 1

        node_sekarang.next = node_sekarang.next.next
```

Node pada index tertentu dihapus dengan menelusuri node sebelumnya lalu menghubungkan pointer ke node setelah target.

## **9 Menampilkan Isi Linked List (print)**

```python
def print(self):
    if self.head is None:
        print("data kosong")
    else:
        text_print = ''
        node_sekarang = self.head

        while node_sekarang:
            text_print += str(node_sekarang.data) + " → "
            node_sekarang = node_sekarang.next

        print(text_print)
```

Memperlihatkan seluruh data dalam list dengan menelusuri node dari head hingga node terakhir dan mencetak nilainya secara berurutan.

## **10 Menghitung Jumlah Elemen (length)**

```python
def length(self):
    urutan = 0
    data_sekarang = self.head

    while data_sekarang:
        data_sekarang = data_sekarang.next
        urutan += 1

    return urutan
```

Menghitung total node dengan menelusuri semua elemen dari head sambil menambah hitungan hingga mencapai node terakhir.

## **11. Contoh Penggunaan Semua Operasi**

```python
ll = LinkedList()

# insert
ll.insert_at_first("jeruk")
ll.insert_at_first("mangga")
ll.insert_at_first("manggis")
ll.insert_at_last("apel")
ll.insert_at(2, "anggur")

# remove
ll.remove_first()
ll.remove_last()
ll.remove_at(1)
ll.remove_at(1)

# print
ll.print()
print(ll.length())
```

Bagian ini menjalankan operasi insert, remove, cetak, dan hitung jumlah elemen untuk memperlihatkan cara kerja seluruh fungsi di dalam LinkedList.

---
