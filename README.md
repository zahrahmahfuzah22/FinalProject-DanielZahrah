# **Prediksi Pembatalan Reservasi Hotel Menggunakan Model Klasifikasi Machine Learning: Studi Kasus Hotel Lonestar Oriental, Portugal**

**By:** Daniel Berzelius H. & Zahrah Mahfuzah (Alpha Group)    

**Program:** JCDSAHSR-004

---

# **A. Business Understanding**

## **Hotel Overview**

Hotel merupakan salah satu bentuk akomodasi komersial yang menyediakan layanan penginapan bagi masyarakat umum, baik untuk tujuan wisata, bisnis, maupun kebutuhan lainnya. Selain menyediakan kamar, hotel juga menawarkan berbagai fasilitas pendukung seperti restoran, ruang pertemuan, layanan kebersihan, serta fasilitas rekreasi.

Seiring berkembangnya industri pariwisata dan mobilitas masyarakat, hotel tidak lagi hanya berfungsi sebagai tempat menginap, tetapi juga menjadi bagian penting dalam mendukung aktivitas ekonomi, sosial, dan bisnis.

Namun, perkembangan sistem reservasi modern memberikan fleksibilitas tinggi kepada pelanggan, seperti:

* Pemesanan jauh hari (advance booking)
* Perubahan jadwal menginap
* Permintaan khusus
* Pembatalan reservasi (cancellation)

Fleksibilitas ini meningkatkan kenyamanan pelanggan, tetapi juga menimbulkan tantangan bagi hotel, terutama dalam:

* Manajemen ketersediaan kamar
* Ketidakpastian okupansi
* Risiko kehilangan pendapatan akibat pembatalan

---

## **Problem Statement**

Hotel Lonestar Oriental merupakan salah satu hotel terkemuka di Portugal yang menawarkan fleksibilitas tinggi dalam layanan reservasi, antara lain:

* Fleksibilitas pemesanan
* Variasi ukuran kelompok tamu
* Pilihan 10 tipe kamar
* Ketersediaan parkir luas
* Fleksibilitas waktu tunggu reservasi

Namun, tingkat pembatalan reservasi masih tergolong tinggi, yaitu sebesar **37.05%**.

Tingginya angka pembatalan ini berdampak pada:

* Penurunan pendapatan hotel
* Ketidakefisienan operasional
* Penurunan kepercayaan pelanggan dan investor

Oleh karena itu, diperlukan analisis untuk:

* Mengidentifikasi faktor utama pembatalan
* Memahami pola perilaku pelanggan
* Menyusun strategi untuk menurunkan cancellation rate

---

## **Objectives**

1. Menganalisis pola perilaku pelanggan berdasarkan data reservasi.
2. Mengidentifikasi faktor-faktor yang mempengaruhi:

   * Keberhasilan reservasi (non-cancellation)
   * Pembatalan reservasi (cancellation)
3. Memberikan rekomendasi berbasis data untuk:

   * Menurunkan tingkat pembatalan
   * Meningkatkan okupansi dan revenue hotel

---

## **Stakeholders**

1. **Manajemen Hotel**
   Menggunakan insight untuk pengambilan keputusan strategis seperti pricing, kebijakan pembatalan, dan manajemen kamar.

2. **Tim Marketing**
   Mengoptimalkan strategi pemasaran berdasarkan segmentasi pelanggan dan pola pembatalan.

3. **Front Office**
   Menggunakan insight untuk meningkatkan komunikasi dengan tamu dan mengurangi risiko pembatalan.

4. **Investor**
   Memantau performa bisnis dan stabilitas pendapatan hotel.

5. **Tim Data Scientist**
   Bertanggung jawab dalam analisis data dan pengembangan model prediktif.

---

# **B. Dataset Description**

Dataset berisi informasi terkait reservasi hotel, termasuk karakteristik tamu, detail booking, serta status reservasi.

## **Variables**

| No | Column                           | Description                                        |
| -- | -------------------------------- | -------------------------------------------------- |
| 1  | `hotel`                          | Jenis hotel (Resort / City)                        |
| 2  | `is_canceled`                    | Status pembatalan (1 = Canceled, 0 = Not Canceled) |
| 3  | `lead_time`                      | Selisih hari antara booking dan tanggal check-in   |
| 4  | `arrival_date_year`              | Tahun kedatangan                                   |
| 5  | `arrival_date_month`             | Bulan kedatangan                                   |
| 6  | `arrival_date_week_number`       | Minggu ke-berapa dalam tahun                       |
| 7  | `arrival_date_day_of_month`      | Hari kedatangan                                    |
| 8  | `stays_in_weekend_nights`        | Jumlah malam weekend                               |
| 9  | `stays_in_week_nights`           | Jumlah malam weekday                               |
| 10 | `adults`                         | Jumlah orang dewasa                                |
| 11 | `children`                       | Jumlah anak                                        |
| 12 | `babies`                         | Jumlah bayi                                        |
| 13 | `meal`                           | Tipe makanan                                       |
| 14 | `country`                        | Negara asal                                        |
| 15 | `market_segment`                 | Segmen pasar                                       |
| 16 | `distribution_channel`           | Channel booking                                    |
| 17 | `is_repeated_guest`              | Tamu repeat atau tidak                             |
| 18 | `previous_cancellations`         | Jumlah pembatalan sebelumnya                       |
| 19 | `previous_bookings_not_canceled` | Booking sebelumnya yang sukses                     |
| 20 | `reserved_room_type`             | Tipe kamar yang dipesan                            |
| 21 | `assigned_room_type`             | Tipe kamar yang diberikan                          |
| 22 | `booking_changes`                | Jumlah perubahan booking                           |
| 23 | `deposit_type`                   | Tipe deposit                                       |
| 24 | `agent`                          | ID travel agent                                    |
| 25 | `company`                        | ID perusahaan                                      |
| 26 | `days_in_waiting_list`           | Hari dalam waiting list                            |
| 27 | `customer_type`                  | Tipe pelanggan                                     |
| 28 | `adr`                            | Average Daily Rate                                 |
| 29 | `required_car_parking_spaces`    | Jumlah parkir                                      |
| 30 | `total_of_special_requests`      | Jumlah request khusus                              |
| 31 | `reservation_status`             | Status akhir reservasi                             |
| 32 | `reservation_status_date`        | Tanggal status terakhir                            |


