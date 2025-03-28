### Reflection Subscriber-1

1. Fungsi `Display` diterapkan pada `Notification` agar notifikasi bisa direpresentasikan sebagai teks yang mudah dipahami dan dibaca (baik untuk log atau antarmuka). Ini mempermudah kita melihat isi notifikasi dalam format manusiawi.

2. Fungsi `list_all_as_string()` digunakan untuk mengakses semua notifikasi dalam bentuk string. Fungsinya penting untuk logging atau debugging. Karena data disimpan dalam `RwLock<Vec<Notification>>`, kita tidak bisa langsung iterasi tanpa locking.

3. Fungsi ini bisa digunakan di endpoint `GET` untuk menampilkan semua notifikasi yang sudah tersimpan.
