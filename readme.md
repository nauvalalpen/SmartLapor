# 🏙️ SmartLapor (LaporJalan AI)

**Enterprise-Grade Public Facility Reporting System powered by Agentic AI, MCP, & Event-Driven Architecture.**

![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-Message_Queue-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Schema_Less-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-In_Memory_Cache-DC382D?style=flat-square&logo=redis&logoColor=white)
![AI](https://img.shields.io/badge/Agentic_AI-MCP_Enabled-6B5B95?style=flat-square&logo=openai&logoColor=white)

---

## 📌 Project Overview

Repository ini berisi rancangan **Infrastruktur dan Arsitektur Sistem** untuk "SmartLapor", sebuah solusi digital guna memecahkan masalah sistem pelaporan fasilitas publik (seperti jalan rusak) yang sering mengalami _server down_, lambat, dan kewalahan dalam proses verifikasi data.

Proyek ini disusun sebagai pemenuhan Tugas UTS Mata Kuliah **Topik Khusus** (Teknik Informatika / RPL).

## 🚀 Key Features & Solutions

1. **Asynchronous Upload (Zero-Downtime):** Mencegah server _timeout_ saat warga upload foto masal menggunakan **RabbitMQ**.
2. **Auto-Verification Agent:** Filtrasi laporan palsu dan penentuan prioritas secara otonom menggunakan **Agentic AI** yang terhubung via **Model Context Protocol (MCP)**.
3. **Ultra-Fast GeoMap:** Peta sebaran lokasi jalan rusak dimuat dalam waktu 0 milidetik berkat **Redis Cache** dan query Geospatial dari **MongoDB**.
4. **Ultimate Portability:** Seluruh infrastruktur di- _containerize_ menggunakan **Docker**, siap di-_deploy_ di server Pemda mana pun secara _On-Premise_.

---

## 🏗️ System Architecture

Diagram arsitektur di bawah ini menggambarkan topologi _Event-Driven Microservices_ yang memisahkan proses _Read/Write_ dan mendelegasikan tugas berat ke _background worker_.

![Arsitektur Sistem SmartLapor](docs/Arsitektur%20Sistem.png)

## 🛠️ Infrastructure as Code (How to Run)

Proyek ini mengadopsi prinsip _Infrastructure as Code_ (IaC). Anda dapat menjalankan seluruh ekosistem database dan message broker (_MongoDB, RabbitMQ, Redis_) secara lokal menggunakan Docker Compose.

1. Pastikan **Docker** dan **Docker Compose** sudah terinstal di sistem Anda.
2. Clone repository ini:
   ```bash
   git clone https://github.com/[USERNAME_GITHUB_ANDA]/SmartLapor-Architecture.git
   ```
3. Masuk ke direktori proyek dan jalankan _container_:
   ```bash
   cd SmartLapor-Architecture
   docker-compose up -d
   ```
4. Akses Dashboard RabbitMQ Management di browser: `http://localhost:15672`

---

## 🤖 Prompt Engineering Logbook

Pengembangan arsitektur ini didampingi oleh _Agentic AI_ sebagai _Technical Co-founder_. Sebanyak **60 prompt iteratif** telah dirancang mencakup fase Eksplorasi, Validasi Solusi, Analisis Kompetitor, dan Inovasi.

👉 **[Lihat Logbook 60 Prompt Lengkap di Sini](prompt-log.md)**

---

## 📂 Project Documentation

Dokumen lengkap terkait analisis bisnis, _Pitch Deck_, dan _Technical Whitepaper_ dapat diakses pada folder `/docs` di repository ini:

- [Laporan (PDF)](docs/Laporan%20UTS%20Topik%20Khusus%20-%20Nauval%20Alpen%20Perdana.pdf)
- [PPT (PDF)](docs/PPT%20Topik%20Khusus%20-%20Nauval%20Alpen%20Perdana.pdf)

---
