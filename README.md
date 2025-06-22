# 💧 Smart Water Tank Monitoring System

## KELOMPOK 11
## Muhammad Zacky Said, 105222046
## Rayhan Surya Destian, 105222024
## Link video demo UAS IOT: https://drive.google.com/drive/folders/1L5Lwiqkc8XPHiGux44WPvm6UZmRBBAAb

## 🎯 SDG Fokus
**SDG 6 – Clean Water and Sanitation**

## 📘 Deskripsi Singkat
Sistem ini memantau ketinggian air dalam tangki menggunakan sensor ultrasonik yang terhubung ke ESP32. Kemudian data dikirim ke aplikasi mobile melalui Blynk maupaun Firebase. Pengguna dapat mengontrol pompa air dari jarak jauh untuk mengisi ulang tangki secara otomatis atau manual.

## 🎯 Tujuan Fungsional
- Monitoring level air secara real-time
- Kontrol pompa dari aplikasi mobile
- Notifikasi saat air rendah atau tinggi

## ✅ Manfaat
- Menghindari kekurangan air
- Menghemat energi dan air
- Solusi otomatisasi rumah yang hemat biaya dan praktis

## Daftar Komponen
- ESP32
- Breadboard dan Kabel
- Modul Relay
- Sensor Ultrasonik HC-SR04
- Pompa Mini Micro DC 3V - 6V

---

## Skema Sistem
```mermaid
graph TD
  Sensor_Ultrasonik --> ESP32
  ESP32 --> WiFi
  WiFi --> Cloud[Blynk/Firebase]
  Cloud --> MobileApp[Mobile App]
  MobileApp -->|Kontrol| Cloud
  Cloud -->|Aktuasi| ESP32
  ESP32 --> Relay --> Pompa
