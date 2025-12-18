# Longest Increasing Subsequence (LIS) - Decision Tree Solver

Folder ini berisi implementasi algoritma untuk mencari **Longest Increasing Subsequence (LIS)** menggunakan pendekatan struktur data **Tree**.  
Program ini tidak hanya menemukan urutan angka terpanjang yang meningkat, tetapi juga memvisualisasikan seluruh kemungkinan decision tree.

---

## Alur Penggunaan Program

### 1. Input Data
Program menerima sebuah sequence (urutan angka) acak dalam bentuk list.

### 2. Pembangunan Tree
- Program membuat sebuah **Root Node (START)**.  
- Secara rekursif, program menelusuri setiap angka.  
- Jika angka di depan lebih besar dari angka saat ini, maka angka tersebut akan menjadi **child node**.

### 3. Pencarian Jalur Terpanjang
Menggunakan algoritma **Depth First Search (DFS)** untuk menelusuri pohon dari akar hingga daun guna menemukan jalur dengan jumlah node terbanyak.

### 4. Output
Program menampilkan:
- Subsequence terpanjang yang ditemukan.  
- Panjang dari subsequence tersebut.  
- Visualisasi pohon keputusan menggunakan **networkx** dan **matplotlib**.

---

## Penggunaan (Statis)

Untuk menjalankan program dengan data default (data pada soal praktikum) yang sudah disediakan, Bisa menjalankan blok kode utama (`main`).  
Berikut adalah contoh implementasi statisnya:

```python
# Contoh penggunaan di dalam file .ipynb
data = [4, 1, 13, 7, 0, 2, 8, 11, 3]

solver = LISTreeSolver(data)
solver.build_tree()

# Mencari dan menampilkan hasil
result = solver.find_longest_path()
print(f"Longest Increasing Subsequence: {result}")
print(f"Panjang Subsequence: {len(result)}")

# Visualisasi
solver.visualize_tree()
```

## Input 
```
[4, 1, 13, 7, 0, 2, 8, 11, 3]
```

## Output 
```
Longest Increasing Subsequence: [4, 7, 8, 11]
Panjang Subsequence: 4
```
## Dependencies
Sebelum menjalankan cell `main`, wajib menjalankan cell untuk install library di file `ipynb` :
* `networkx` (untuk struktur graph)
* `matpotlib` (untuk visualisasi graph)



