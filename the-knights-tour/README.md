# Knight's Tour Problem - Warnsdorff's Heuristic

Program ini adalah implementasi dari masalah klasik **Knight's Tour** (Perjalanan Kuda) menggunakan **Heuristik Warnsdorff**. Tujuannya adalah untuk menentukan apakah sebuah bidak kuda dapat mengunjungi setiap kotak pada papan catur tepat satu kali.

## Alur Penggunaan Program

### 1. Cara Penggunaan
Program ini diimplementasikan dalam bahasa Python dan dirancang untuk dijalankan di lingkungan seperti Jupyter Notebook atau Google Colab.
* Jalankan sel kode yang mendefinisikan fungsi-fungsi pendukung (`get_knight_moves`, `is_safe`, `count_onward_moves`, dll).
* Eksekusi blok utama program (`if __name__ == "__main__":`) untuk memulai proses pencarian jalur.
* Anda dapat mengubah variabel `n` untuk ukuran papan atau `start_x` dan `start_y` untuk posisi awal yang berbeda.

### 2. Input
Program menerima input utama melalui parameter fungsi `knights_tour_warnsdorff`:
* **`n`**: Ukuran sisi papan catur (misalnya `8` untuk papan 8x8).
* **`start_x`**: Indeks baris awal (0 sampai n-1).
* **`start_y`**: Indeks kolom awal (0 sampai n-1).

### 3. Output
Setelah kalkulasi selesai, program akan menampilkan dua jenis output:

* **Matriks Urutan Perjalanan**: Sebuah tabel yang menampilkan angka `0` hingga `(n*n - 1)`. Angka tersebut menunjukkan urutan langkah yang ditempuh oleh kuda di setiap koordinat papan catur.
* **Visualisasi Jalur Sederhana**: Peta grafis yang memberikan tanda khusus:
    * **`S` (Start)**: Posisi awal perjalanan kuda (Langkah ke-0).
    * **`E` (End)**: Posisi akhir perjalanan kuda (Langkah ke-63 untuk papan 8x8).
    * **`·`**: Menandai kotak-kotak lain yang telah berhasil dikunjungi.

> **Catatan:** Jika program tidak menemukan jalur valid (dead-end), output akan memunculkan pesan: *"Tour gagal ditemukan. Coba posisi awal lain."*.

---

## Contoh Input & Output

**Input:**
```plaintext
n = 8
start_x = 0
start_y = 0
```

**Output:**

```plaintext 
Mencari Knight's Tour 8x8 dari posisi awal (0, 0) dengan Warnsdorff's Heuristic...

Solusi ditemukan!

Urutan perjalanan kuda:
================================
 0 33  2 17 48 31 12 15
 3 18 55 32 13 16 49 30
56  1 34 47 54 51 14 11
19  4 59 52 35 46 29 50
40 57 36 45 60 53 10 25
 5 20 41 58 37 26 63 28
42 39 22  7 44 61 24  9
21  6 43 38 23  8 27 62
================================

Visualisasi jalur (S = start, E = end):
 S · · · · · · ·
 · · · · · · · ·
 · · · · · · · ·
 · · · · · · · ·
 · · · · · · · ·
 · · · · · · E ·
 · · · · · · · ·
 · · · · · · · ·

```