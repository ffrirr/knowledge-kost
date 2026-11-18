# Functional Specification Document (FSD) — Smart Kost

## 1. Overview
Sistem Smart Kost digunakan untuk mengelola operasional properti kamar indekos / sewa bulanan, mulai dari ketersediaan kamar hingga pencatatan penyewa dan kontrak sewa.

## 2. Fitur Utama
1. **Master Kamar (`kos.room`)**:
   - Nomor Kamar (String, required, unique)
   - Lantai (Integer)
   - Tipe Kamar (Selection: Standard, Deluxe, VIP)
   - Harga Sewa Bulanan (Monetary)
   - Status (Selection: Draft, Available, Occupied, Maintenance)
2. **Kontrak Sewa (`kos.contract`)**:
   - Partner / Penyewa (`res.partner`)
   - Kamar (`kos.room`)
   - Tanggal Mulai & Selesai
   - Status Kontrak (Draft, Active, Done, Cancelled)
