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
