### Reflection Subscriber-1

1. Fungsi `Display` diterapkan pada `Notification` agar notifikasi bisa direpresentasikan sebagai teks yang mudah dipahami dan dibaca (baik untuk log atau antarmuka). Ini mempermudah kita melihat isi notifikasi dalam format manusiawi.

2. Fungsi `list_all_as_string()` digunakan untuk mengakses semua notifikasi dalam bentuk string. Fungsinya penting untuk logging atau debugging. Karena data disimpan dalam `RwLock<Vec<Notification>>`, kita tidak bisa langsung iterasi tanpa locking.

3. Fungsi ini bisa digunakan di endpoint `GET` untuk menampilkan semua notifikasi yang sudah tersimpan.

### Reflection Subscriber-2

1. Have you explored things outside of the steps in the tutorial, for example: src/lib.rs? If not, explain why you did not do so. If yes, explain things that you have learned from those other parts of code.

I have not explored beyond the provided tutorial, such as the src/lib.rs file. My current focus was to ensure all primary features worked correctly according to the instructions. However, I acknowledge the file contains essential setups, including Rocket's initialization and module integrations, and intend to review it later to better understand how Rocket manages the application’s configuration.

2. Since you have completed the tutorial by now and have tried to test your notification system by spawning multiple instances of Receiver, explain how the Observer pattern eases you to plug in more subscribers. How about spawning more than one instance of Main app, will it still be easy enough to add to the system?

The Observer pattern significantly simplifies the process of adding subscribers. It allows multiple Receiver instances to subscribe seamlessly, requiring no additional modifications to the Main app. However, spawning multiple Main app instances would introduce complexity, particularly regarding synchronization and data consistency across instances. Additional mechanisms, such as load balancing or state synchronization, would need to be implemented.

3. Have you tried to make your own Tests or enhance documentation in your Postman collection? If you have tried those features, tell us whether it is useful for your work (it can be your tutorial work or your Group Project).

I have explored creating custom Tests in Postman, and it has proven highly useful, especially when working on the NutriBoost project. The testing features in Postman, including automated request validation and environment management, made it easy to test various scenarios quickly. Additionally, enhanced documentation through Postman collections allowed smoother team collaboration and improved clarity of the application's API design.