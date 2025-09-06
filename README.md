# TUGAS PM
#  Flutter Shopping Cart (Simple)

Aplikasi Flutter sederhana dengan tema **Keranjang Belanja**.
Tujuan utama: memahami perbedaan Stateless vs Stateful widget, state management, dan navigasi antar layar.

---

##  Tujuan
- Memahami perbedaan Stateless vs Stateful widget.
- Menerapkan state management menggunakan **setState**.
- Menggunakan widget tree yang rapi.
- Navigasi antar 2 layar dengan **MaterialApp + Navigator**.

---

##  Fitur
- Tambah barang ke keranjang.
- Hapus barang dari keranjang.
- Dark mode modern + animasi smooth.
- 2 Halaman ( Home & Cart ).
- Validasi input ( tidak bisa tambah item kosong ).

---

##  Widget Tree (Diagram Sederhana)

 ```bash
 MaterialApp
└── HomeScreen (StatelessWidget)
└── Button → Navigator.push → CartScreen
└── CartScreen (StatefulWidget)
├── AppBar
├── Column
│ ├── TextField + Button (Tambah Item)
│ └── ListView (Daftar Barang)
└── FloatingActionButton
 ```


---

##  State Management
- **Pendekatan:** `setState` ( ephemeral/widget-local state ).  
- **Alasan:**  
  - Sederhana dan bawaan Flutter.  
  - Cocok untuk aplikasi kecil.  
  - Sesuai requirement tugas.  

Jika aplikasi berkembang lebih kompleks, bisa pakai **Provider** atau **Riverpod**.

---

##  Struktur Folder
```bash
lib/
├── main.dart
├── models/
│ └── cart_item.dart # model data item
├── screens/
│ ├── home_screen.dart # layar awal
│ └── cart_screen.dart # layar keranjang belanja
└── widgets/
└── cart_item_tile.dart # widget custom untuk 1 item
```


---


##  Cara Menjalankan
1. Clone repo ini:
   ```bash
   git clone https://github.com/username/flutter-cart-simple.git
   cd flutter-cart-simple
   ```
2. Jalankan flutter pub get.
3. Run di terminal:
   ```bash
   flutter run



