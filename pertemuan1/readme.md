# Penjelasan Program Stack dalam Python

Program ini menunjukkan cara kerja struktur data Stack (tumpukan) menggunakan list di Python.
Stack mengikuti konsep LIFO (Last In, First Out), yaitu elemen terakhir yang masuk akan menjadi elemen pertama yang keluar.

## Kode Program

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

## Penjelasan Kode Program

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

## 🧩 Hasil Eksekusi

```
Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size:  2
```
