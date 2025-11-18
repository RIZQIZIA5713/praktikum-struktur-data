# Penjelasan Program Stack dan Queue dalam Python

## 1. Implementasi Stack di Python
Program ini menunjukkan cara kerja struktur data Stack (tumpukan) menggunakan list di Python.
Stack mengikuti konsep LIFO (Last In, First Out), yaitu elemen terakhir yang masuk akan menjadi elemen pertama yang keluar.

### Kode Program

```python
# # stack and stack operations
stack = []

# Push
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack: ", stack)

# Pop
element = stack.pop()
print("Pop: ", element)

# Peek
topElement = stack[-1]
print("Peek: ", topElement)

# isEmpty
isEmpty = not bool(stack)
print("isEmpty: ", isEmpty)

# Size
print("Size: ", len(stack))
```

### Penjelasan Kode Program

1. **Membuat Stack**

   ```python
   stack = []
   ```

   Membuat sebuah list kosong bernama stack untuk menampung elemen-elemen.

2. **Operasi Push (Menambahkan Elemen ke Stack)**

   ```python
    stack.append('A')
    stack.append('B')
    stack.append('C')
   ```

   append() digunakan untuk menambahkan elemen di bagian paling atas stack.

3. **Operasi Pop (Mengeluarkan Elemen Teratas Stack)**

   ```python
    element = stack.pop()
   ```

   pop() akan mengambil dan menghapus elemen paling atas stack.

4. **Operasi Peek (Melihat Elemen Teratas tanpa Menghapus)**

   ```python
   topElement = stack[-1]
   ```
   
   stack[-1] mengambil elemen terakhir (teratas) tanpa menghapusnya.

5. **Cek Apakah Stack Kosong (isEmpty)**

   ```python
   isEmpty = not bool(stack)
   ```
   
   Mengecek apakah stack masih memiliki elemen

6. **Menampilkan Ukuran Stack (Size)**

   ```python
   len(stack)
   ```
   
   len(stack) mengembalikan jumlah elemen stack.

### Hasil Eksekusi Kode Program

```
Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size:  2
```

## 2. Implementasi Queue di Python
Program ini menunjukkan cara membuat dan menggunakan Queue (antrian) menggunakan list di Python.
Queue mengikuti prinsip FIFO (First In, First Out), yaitu elemen yang pertama masuk akan menjadi elemen pertama yang keluar.

### Kode Program

```python
# Creating queue and Queue Operations
queue = []

# Enqueue
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue: ", queue)

# Dequeue
element = queue.pop(0)
print("Dequeue: ", element)

# Peek
frontElement = queue[0]
print("Peek: ", frontElement)

# isEmpty
isEmpty = not bool(queue)
print("isEmpty: ", isEmpty)

# Size
print("Size: ", len(queue))
```

### Penjelasan Kode Program

1. **Membuat Queue**

   ```python
   queue = []
   ```

   Membuat sebuah list kosong bernama queue untuk menampung elemen-elemen.

2. **Enqueue (Menambahkan Elemen ke Antrian)**

   ```python
    queue.append('A')
    queue.append('B')
    queue.append('C')
   ```

   append() digunakan untuk menambahkan elemen di belakang antrian.

3. **Dequeue (Mengeluarkan Elemen Depan Antrian)**

   ```python
    element = queue.pop(0)
   ```

   pop(0) mengambil dan menghapus elemen paling depan dari queue.

4. **Peek (Melihat Elemen Depan Tanpa Menghapus)**

   ```python
   frontElement = queue[0]
   ```
   
   queue[0] mengambil elemen terdepan tanpa menghapusnya.

5. **Cek Apakah Queue Kosong (isEmpty)**

   ```python
   isEmpty = not bool(queue)
   ```
   
   Mengecek apakah queue masih memiliki elemen.

6. **Size (Mengetahui Ukuran Queue)**

   ```python
   len(queue)
   ```
   
   len(queue) menghitung jumlah elemen dalam queue.

### Hasil Eksekusi Kode Program

```
Queue:  ['A', 'B', 'C']
Dequeue:  A
Peek:  B
isEmpty:  False
Size:  2
```
