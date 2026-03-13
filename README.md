# Parking Management System Dashboard

**Parking Management System Dashboard** adalah aplikasi web untuk mengelola sistem parkir kendaraan.  
Website ini digunakan untuk mencatat kendaraan yang masuk, kendaraan yang sedang parkir, serta kendaraan yang keluar beserta biaya parkirnya.

Aplikasi ini terintegrasi dengan **Firebase** untuk autentikasi pengguna dan penyimpanan data **real-time**.

---

#  Fitur Utama

##  Autentikasi Pengguna
- **Register & Login**  
  Pengguna harus mendaftar dan login menggunakan **Email dan Password** sebelum dapat mengakses dashboard.

- **Route Protection**  
  Halaman dashboard hanya bisa diakses oleh pengguna yang sudah login.

- **Logout**  
  Pengguna dapat keluar dari sesi dengan aman.

---

##  Check-In Kendaraan
- Menginput **plat nomor kendaraan**.
- Memilih **area parkir** dan **paket parkir**.
- Menampilkan **indikator kapasitas area parkir secara real-time**  
  Contoh: `(0/10)` menunjukkan jumlah slot yang masih tersedia.

---

##  Check-Out & Struk Digital
- Memproses kendaraan yang keluar dari area parkir.
- Status kendaraan akan diperbarui di database.
- Sistem otomatis menghitung **biaya parkir berdasarkan durasi atau paket parkir**.
- Setelah checkout, sistem menampilkan **Struk Parkir Digital** berisi:
  - Plat nomor
  - Slot parkir
  - Durasi parkir
  - Total biaya

---

## Riwayat Parkir
- Halaman tabel untuk melihat **riwayat kendaraan yang sudah selesai parkir**.
- Fitur yang tersedia:
  - Hapus riwayat per item
  - Hapus seluruh riwayat parkir

---

# Alat yang digunakan
- HTML5  
- CSS3  
- JavaScript 

### BaaS
Menggunakan **Firebase** sebagai Backend as a Service.

- **Firebase Authentication**  
  Untuk sistem login menggunakan email dan password.

- **Firebase Realtime Database**  
  Untuk menyimpan dan mengelola data parkir secara real-time.

---

# Struktur Database

Data disimpan di **Firebase Realtime Database** dalam node `transactions`.

Contoh struktur JSON:

```json
{
  "transactions": {
    "unique_id_1": {
      "plate": "B 1234 XYZ",
      "slot": "A1",
      "type": "harian",
      "status": "active",
      "checkInTime": 1715678900000
    },
    "unique_id_2": {
      "plate": "AB 1234 AF",
      "slot": "A1",
      "type": "harian",
      "status": "completed",
      "checkInTime": 1773130586585,
      "checkOutTime": 1773130597961,
      "totalCost": 5000
    }
  }
}
```
Screenshot Aplikasi

- 1.	Input Plat nomor kendaraan
  <img width="921" height="238" alt="image" src="https://github.com/user-attachments/assets/eab0a1ea-0eff-4b27-aa25-e9f4b1cca47c" />
 
- 2.	Data
  <img width="921" height="335" alt="image" src="https://github.com/user-attachments/assets/37725e1d-ac80-40ae-ad42-a9859c84d008" />

- 3.	Kendaraan keluar
  <img width="637" height="272" alt="image" src="https://github.com/user-attachments/assets/39f0c2ab-6b19-45b5-987c-7ec2fac025cd" />

- 4.	Riwayat kendaraan masuk
  <img width="921" height="352" alt="image" src="https://github.com/user-attachments/assets/007acf15-51be-4e2f-a90e-d05f9876fffe" />

- 5.	Firebase Realtime Database Console
  <img width="839" height="498" alt="image" src="https://github.com/user-attachments/assets/c32d7563-a164-4043-9f27-3a3d8256273f" />

- 6.  Login Page
<img width="909" height="740" alt="image" src="https://github.com/user-attachments/assets/77df81e3-81a5-4392-af85-f8a3261161e5" />

- 7.  Sign Up
  <img width="755" height="743" alt="image" src="https://github.com/user-attachments/assets/74153ba3-537f-492f-a75b-0a280f819abf" />
  
