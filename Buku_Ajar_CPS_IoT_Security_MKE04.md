# BUKU AJAR
# CPS & IoT SECURITY
## MK-E-04 — Elektif Keilmuan IPTEKS Pendukung

---

**Program Studi:** Magister Terapan Forensik Digital dan Keamanan Siber  
**Departemen:** Teknik Informatika dan Komputer  
**Institusi:** Politeknik Elektronika Negeri Surabaya (PENS)  
**Semester:** 1 atau 3 (Pool Gasal / Pendalaman Tesis)  
**Bobot SKS:** T = 2, P = 1, Total = 3 SKS  
**Level Bloom:** C4–C5  
**Versi:** 1.0 — Tahun Akademik 2025/2026  

---

> *"Security in cyber-physical systems is not merely about protecting data — it is about protecting physical safety, operational continuity, and the trust embedded in critical infrastructure."*

---

## Metadata Mata Kuliah

| Item | Keterangan |
|------|-----------|
| Kode Mata Kuliah | MK-E-04 / ELEKTIF-G1-G3 |
| Nama Mata Kuliah | CPS & IoT Security |
| Rumpun Mata Kuliah | Keilmuan IPTEKS Pendukung (Cyber-Physical Systems, IoT, Hardware Security) |
| Bobot SKS | T = 2, P = 1, Total = 3 SKS |
| Semester | 1 atau 3 (Pool Gasal / Pendalaman Tesis) |
| Level Bloom | C4–C5 |
| No. Dokumen | FM.RPS.MTr.FDKS.MK-E-04.2025 |
| Tanggal Penyusunan | 28-05-2026 |

---

## Kata Pengantar

Keamanan sistem siber-fisik (Cyber-Physical Systems/CPS) dan Internet of Things (IoT) adalah salah satu tantangan keamanan siber paling kompleks di era digital. Berbeda dengan keamanan sistem informasi konvensional yang berfokus pada perlindungan data, keamanan CPS/IoT memiliki dimensi tambahan yang kritis: kegagalan keamanan dapat berdampak pada keselamatan fisik manusia, gangguan infrastruktur kritis, atau bahkan korban jiwa.

Sebuah serangan pada sistem kendali industri (ICS/SCADA) yang mengelola distribusi listrik dapat menyebabkan pemadaman massal. Serangan pada perangkat medis yang terhubung dapat membahayakan pasien. Kompromi pada sistem kendali kendaraan dapat mengancam keselamatan pengemudi. Inilah mengapa CPS/IoT Security membutuhkan pendekatan yang berbeda: menggabungkan keahlian keamanan siber dengan pemahaman mendalam tentang domain fisik, standar keselamatan, dan persyaratan operasional.

Buku ajar ini disusun untuk membekali mahasiswa Program Studi Magister Terapan Forensik Digital dan Keamanan Siber PENS dengan kemampuan menganalisis, merancang, dan mengevaluasi keamanan CPS/IoT secara komprehensif. Pendekatan yang digunakan bersifat case-based dan project-based, dengan penekanan pada praktik defensif yang legal, aman, dan berotorisasi.

Seluruh aktivitas teknis dalam buku ini — termasuk analisis firmware, pengujian protokol, dan evaluasi konfigurasi — dirancang untuk dilaksanakan dalam lingkungan lab yang terkendali, menggunakan perangkat dan dataset yang sah, tidak diarahkan untuk mengeksploitasi sistem nyata yang tidak berotorisasi.

---

## Deskripsi Mata Kuliah

Mata kuliah CPS & IoT Security (MK-E-04) membekali mahasiswa Magister Terapan FDKS dengan kemampuan menganalisis, merancang, dan mengevaluasi keamanan pada cyber-physical systems dan Internet of Things. Fokus pembelajaran mencakup:

- Arsitektur CPS/IoT, data flow, dan attack surface analysis
- Threat modelling untuk sistem siber-fisik
- Keamanan protokol IoT: MQTT, CoAP, HTTP/REST, TLS/DTLS
- Device identity, autentikasi, otorisasi, dan telemetry security
- Firmware security review: triage, konfigurasi, secrets exposure
- Hardware security: secure boot, key storage, debug interface
- Security controls: segmentation, gateway security, secure update
- Monitoring, anomaly detection, dan incident readiness
- Resilience planning untuk CPS/IoT
- Proyek capstone: desain/prototipe defensif CPS/IoT

Mata kuliah ini menggunakan pendekatan case-based dan project-based learning dengan praktik pada perangkat, firmware, dataset, atau simulasi lab yang legal, terisolasi, dan berotorisasi.

---

## Peta OBE: CPL → IK → CPMK → Sub-CPMK → Evaluasi

```mermaid
flowchart TD
    CPL1["CPL1: Etika, hukum,\nprivasi, tanggung jawab\nsosial"]
    CPL3["CPL3: Teknik, tools,\nmetode modern"]
    CPL4["CPL4: Konsep keamanan\nsiber, standar, kontrol,\nmitigasi"]
    CPL6["CPL6: Analisis ancaman,\ndeteksi, prioritasi,\nmitigasi risiko"]
    CPL7["CPL7: Solusi strategis\nberbasis data & standar"]
    CPL8["CPL8: Adaptasi teknologi\nbaru, pembelajaran mandiri"]
    CPL10["CPL10: Rancang & konfigurasi\ninfrastruktur keamanan"]

    CPMK1["CPMK-1:\nAnalisis arsitektur,\naset, ancaman CPS/IoT"]
    CPMK2["CPMK-2:\nKeamanan protokol &\nkoneksi IoT"]
    CPMK3["CPMK-3:\nEvaluasi firmware\n& hardware security"]
    CPMK4["CPMK-4:\nRancang kontrol keamanan\nCPS/IoT"]
    CPMK5["CPMK-5:\nProyek capstone\nCPS/IoT Security"]

    SubCPMK1["Sub-CPMK-1:\nArsitektur, data flow,\nthreat model, safety/ethics"]
    SubCPMK2["Sub-CPMK-2:\nProtokol IoT, TLS/DTLS,\ndevice identity, telemetry"]
    SubCPMK3["Sub-CPMK-3:\nFirmware triage,\nconfiguration review,\nsecrets exposure"]
    SubCPMK4["Sub-CPMK-4:\nRisk register, mitigasi,\nmonitoring, resilience"]
    SubCPMK5["Sub-CPMK-5:\nCapstone: desain, validasi,\nlaporan, presentasi"]

    Eval1["Eval-1 (10%):\nArchitecture map +\nThreat model +\nSafety-ethics memo"]
    Eval2["Eval-2 (20%):\nProtocol security\nanalysis report +\nSecure connection\nchecklist"]
    Eval3["Eval-3 (25%):\nFirmware/hardware\nsecurity review report +\nVulnerability note"]
    Eval4["Eval-4 (20%):\nRisk register +\nSecure architecture +\nMitigation + Resilience\nplan"]
    Eval5["Eval-5/EAS (25%):\nCapstone design/\nprototype + Validation\nreport + Presentation"]

    CPL1 & CPL4 & CPL6 & CPL7 --> CPMK1 --> SubCPMK1 --> Eval1
    CPL3 & CPL4 & CPL6 & CPL10 --> CPMK2 --> SubCPMK2 --> Eval2
    CPL1 & CPL3 & CPL6 & CPL8 --> CPMK3 --> SubCPMK3 --> Eval3
    CPL4 & CPL6 & CPL7 & CPL10 --> CPMK4 --> SubCPMK4 --> Eval4
    CPL2 & CPL7 & CPL8 & CPL10 --> CPMK5 --> SubCPMK5 --> Eval5
```

---

## Peta Kompetensi Mata Kuliah

```mermaid
flowchart TD
    CORE[CPS & IoT Security\nMK-E-04]

    CORE --> A1[Memahami Ekosistem\nCPS/IoT]
    A1 --> A1a[Arsitektur &\nlayer CPS/IoT]
    A1 --> A1b[Asset inventory &\ndata flow]
    A1 --> A1c[Attack surface\nanalysis]

    CORE --> A2[Menganalisis Ancaman]
    A2 --> A2a[Threat modelling\nSTRIDE/PASTA]
    A2 --> A2b[Safety-security\ninteraction]
    A2 --> A2c[Privacy impact\nassessment]

    CORE --> A3[Mengevaluasi Protokol\n& Koneksi]
    A3 --> A3a[MQTT/CoAP/HTTP\nanalysis]
    A3 --> A3b[TLS/DTLS &\ndevice identity]
    A3 --> A3c[Authentication &\nauthorization]

    CORE --> A4[Mengevaluasi Firmware\n& Hardware]
    A4 --> A4a[Firmware triage\n& static analysis]
    A4 --> A4b[Configuration &\nsecrets review]
    A4 --> A4c[Secure boot &\nkey storage]

    CORE --> A5[Merancang Kontrol\nKeamanan]
    A5 --> A5a[Risk register &\nmitigasi]
    A5 --> A5b[Segmentation &\ngateway security]
    A5 --> A5c[Monitoring &\nresilience]

    CORE --> A6[Proyek Capstone]
    A6 --> A6a[Desain arsitektur\nCPS/IoT aman]
    A6 --> A6b[Validasi kontrol\n& bukti]
    A6 --> A6c[Laporan teknis\n& rekomendasi]
```

---

## Tabel Pemetaan 16 Bab

| Bab | Judul | Sub-CPMK | CPMK | Materi Utama | Evaluasi |
|-----|-------|----------|------|-------------|---------|
| 1 | Arsitektur CPS/IoT dan Ekosistem Perangkat | Sub-CPMK-1 | CPMK-1 | Lapisan CPS/IoT, komponen, konteks SCADA/ICS | Eval-1 |
| 2 | Asset Inventory, Data Flow, dan Attack Surface | Sub-CPMK-1 | CPMK-1 | Aset kritis, data flow diagram, attack surface mapping | Eval-1 |
| 3 | Threat Modelling, Safety-Security Interaction, dan Etika | Sub-CPMK-1 | CPMK-1 | STRIDE CPS, safety-security tension, privacy, batasan legal | Eval-1 |
| 4 | Protokol IoT: MQTT, CoAP, HTTP/REST, dan Industrial Protocols | Sub-CPMK-2 | CPMK-2 | MQTT, CoAP, HTTP IoT, Modbus awareness | Eval-2 |
| 5 | TLS/DTLS, Kriptografi Ringan, dan Keamanan Komunikasi | Sub-CPMK-2 | CPMK-2 | TLS 1.3, DTLS, PKI untuk IoT, certificate management | Eval-2 |
| 6 | Device Identity, Authentication, Authorization, dan Telemetry | Sub-CPMK-2 | CPMK-2 | Device ID, X.509, OAuth 2.0 IoT, telemetry security | Eval-2 |
| 7 | Firmware Security: Struktur, Triage, dan Analisis Statis | Sub-CPMK-3 | CPMK-3 | Firmware format, binwalk, extraction, static analysis | Eval-3 |
| 8 | Configuration Analysis dan Secrets Exposure Review | Sub-CPMK-3 | CPMK-3 | Default credentials, hardcoded secrets, config security | Eval-3 |
| 9 | Hardware Security: Secure Boot, Key Storage, dan Debug Interface | Sub-CPMK-3 | CPMK-3 | Secure boot chain, TPM/HSM, JTAG/UART risks | Eval-3 |
| 10 | Risk Assessment dan Risk Register CPS/IoT | Sub-CPMK-4 | CPMK-4 | Risk scoring, NIST RMF, CPS-specific risk factors | Eval-4 |
| 11 | Security Controls: Segmentation, Gateway, Secure Update, Monitoring | Sub-CPMK-4 | CPMK-4 | Network segmentation, DMZ, OTA update security, anomaly detection | Eval-4 |
| 12 | Incident Readiness, Resilience, dan Recovery CPS/IoT | Sub-CPMK-5 | CPMK-5 | IRP untuk CPS, BCDR, resilience metrics | Eval-4/5 |
| 13 | Capstone: Secure CPS/IoT Architecture Design | Sub-CPMK-5 | CPMK-5 | Desain arsitektur defensif, traceability | Eval-5 |
| 14 | Capstone: Validasi Kontrol, Laporan Teknis, dan Presentasi | Sub-CPMK-5 | CPMK-5 | Validation metrics, laporan capstone, rekomendasi | Eval-5/EAS |
| 15 | OT Security, ICS/SCADA, dan Industrial IoT Convergence | Pengayaan | CPMK-1-4 | SCADA threats, IT/OT convergence, Purdue model | Pengayaan |
| 16 | Tren CPS/IoT Security: Edge, Digital Twin, Medical IoT, Smart City | Pengayaan | CPMK-1-4 | Edge security, digital twin threats, medical IoT, EV security | Pengayaan |

---

## Petunjuk Penggunaan Buku

**Untuk Mahasiswa:**
Buku ini dirancang sebagai panduan belajar mandiri dan referensi praktikum. Setiap bab memiliki 12 seksi wajib: capaian pembelajaran, peta konsep, pengantar, teori mendalam, model/arsitektur, contoh terapan, praktikum, latihan pemahaman, studi kasus, kunci jawaban, ringkasan, dan refleksi profesional.

**Urutan Belajar yang Disarankan:**
1. Baca Peta Konsep dan Capaian Pembelajaran setiap bab sebelum membaca isi
2. Kerjakan Praktikum di lingkungan lab yang disediakan instruktur
3. Jawab Latihan Pemahaman sebelum melihat kunci jawaban
4. Gunakan Studi Kasus sebagai bahan diskusi kelompok

**Catatan Keselamatan Lab:**
Semua aktivitas teknis (analisis firmware, pengujian protokol, konfigurasi perangkat) HANYA dilakukan pada lingkungan lab yang berotorisasi. Tidak ada pengujian pada sistem produksi, perangkat orang lain, atau jaringan tanpa izin.

---

# BAB-BAB BUKU AJAR

---

## Bab 1 — Arsitektur CPS/IoT dan Ekosistem Perangkat

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan arsitektur berlapis CPS/IoT dan peran setiap lapisan dalam ekosistem (C2); mengidentifikasi komponen utama CPS/IoT dan konteks operasionalnya dalam ICS/SCADA, smart city, dan sistem embedded (C4); membedakan karakteristik keamanan CPS/IoT dari keamanan IT konvensional (C4); menjelaskan batasan legal dan etik pengujian CPS/IoT (C2). *Sub-CPMK-1 / CPMK-1 / Eval-1*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    CPS_IOT[CPS & IoT:\nEkosistem dan Arsitektur]

    CPS_IOT --> DEF[Definisi & Perbedaan]
    DEF --> CPS_D[CPS: Cyber-Physical System\nIntegrasi komputasi &\nproses fisik]
    DEF --> IOT_D[IoT: Internet of Things\nMiliaran perangkat\nterhubung]
    DEF --> ICS_D[ICS/SCADA/OT:\nSistem kontrol industri]

    CPS_IOT --> LAYER[Arsitektur Berlapis]
    LAYER --> L1[Layer 1: Perception\nSensor & Aktuator]
    LAYER --> L2[Layer 2: Network\nKomunikasi & Gateway]
    LAYER --> L3[Layer 3: Processing\nEdge & Cloud]
    LAYER --> L4[Layer 4: Application\nDashboard & Control]

    CPS_IOT --> CONTEXT[Konteks Operasional]
    CONTEXT --> SMART[Smart City /\nSmart Home]
    CONTEXT --> INDUST[Industrial IoT\nManufaktur]
    CONTEXT --> MED[Medical IoT\n/ Healthcare]
    CONTEXT --> TRANS[Smart Transportation\n/ EV]

    CPS_IOT --> DIFF[Perbedaan IT vs OT/CPS]
    DIFF --> AVAIL[Availability > Security\ndi OT/ICS]
    DIFF --> RT[Real-time constraint]
    DIFF --> SAFETY_D[Safety consequence]
    DIFF --> LEGACY[Legacy system &\nlong lifecycle]
```

---

### 3. Pengantar Kontekstual

Pada Desember 2015, serangan siber terhadap jaringan listrik Ukraina — yang dikenal sebagai BlackEnergy attack — berhasil memadamkan listrik bagi sekitar 225.000 pelanggan selama beberapa jam. Ini bukan sekadar pelanggaran data: penyerang mengkompromis sistem SCADA, secara fisik membuka pemutus sirkuit dari jarak jauh, dan bahkan melumpuhkan UPS agar tim teknisi tidak dapat merespons dengan cepat.

Insiden ini mengilustrasikan fundamental CPS/IoT Security: kegagalan keamanan berdampak pada dunia fisik. Memahami arsitektur sistem ini adalah prasyarat untuk menganalisis, merancang, dan mengevaluasi keamanannya.

---

### 4. Landasan Teori

#### 4.1 Definisi dan Perbedaan Fundamental

**Cyber-Physical Systems (CPS)** adalah sistem komputasi yang terintegrasi erat dengan proses fisik. Komputer dan jaringan memantau dan mengendalikan proses fisik, dengan umpan balik loop antara dunia siber dan fisik. Contoh: sistem kendali reaktor nuklir, jaringan distribusi listrik, sistem transportasi cerdas.

**Internet of Things (IoT)** mengacu pada jaringan objek fisik ("things") yang dilengkapi sensor, software, dan konektivitas jaringan untuk bertukar data. IoT lebih luas dari CPS: tidak semua IoT devices bersifat CPS (smart speaker bukan CPS), tapi semua CPS modern umumnya memiliki elemen IoT.

**Industrial Control Systems (ICS)** mencakup: SCADA (Supervisory Control and Data Acquisition), DCS (Distributed Control Systems), dan PLC (Programmable Logic Controller). ICS/SCADA adalah jenis CPS yang digunakan dalam infrastruktur kritis.

**Perbedaan IT vs OT (Operational Technology):**

| Aspek | IT (Information Technology) | OT/CPS (Operational Technology) |
|-------|----------------------------|----------------------------------|
| Prioritas CIA | Confidentiality → Integrity → Availability | Availability → Integrity → Confidentiality |
| Update cycle | Frequent (monthly patches) | Sangat jarang (maintenance window terjadwal) |
| Lifecycle | 3–5 tahun | 15–30 tahun |
| Downtime tolerance | Menit hingga jam | Hampir nol (zero downtime) |
| Konsekuensi kegagalan | Data loss, business disruption | Physical damage, safety hazard, korban jiwa |
| Real-time requirement | Tidak kritis | Kritis (millisecond precision) |
| Protocol | TCP/IP, HTTP, TLS | Modbus, DNP3, PROFINET, OPC-UA |

#### 4.2 Arsitektur Berlapis CPS/IoT

Model arsitektur yang umum digunakan adalah **tiga hingga lima lapisan:**

**Model 3 Lapisan (IoT Klasik):**
```
Lapisan 3: Application Layer
    ↑ API, Dashboard, Business Logic, Cloud Services
Lapisan 2: Network Layer
    ↑ Gateway, Router, Protocol Translation, Communication
Lapisan 1: Perception Layer
    ↑ Sensor, Aktuator, RFID, Embedded Devices
```

**Model 5 Lapisan (CPS/IoT Enterprise):**
```
Lapisan 5: Business Layer     — Business rules, governance, reporting
Lapisan 4: Application Layer  — Applications, analytics, user interface
Lapisan 3: Processing Layer   — Edge computing, fog, cloud processing
Lapisan 2: Network Layer      — Connectivity, gateway, protocol bridge
Lapisan 1: Perception Layer   — Physical devices, sensors, actuators
```

**Purdue Reference Model (Industrial):**
Digunakan khusus untuk ICS/SCADA dengan 5 level (Level 0–4) dan zona DMZ antara IT dan OT network.

#### 4.3 Komponen Utama Ekosistem IoT/CPS

**End Device / Node:** Perangkat fisik dengan sensor dan/atau aktuator. Contoh: sensor suhu, smart meter listrik, PLC, medical device.

**Gateway / Edge Device:** Agregator dan protocol translator antara perangkat end-node dan jaringan atas. Berperan penting dalam keamanan: sering menjadi titik pertama yang dapat menerapkan kontrol keamanan.

**Network Infrastructure:** Jaringan nirkabel (WiFi, Zigbee, Z-Wave, LoRaWAN, BLE, LTE-M/NB-IoT) dan kabel (Ethernet, RS-485) yang menghubungkan semua komponen.

**Platform/Cloud:** Backend yang menerima, memproses, dan menyimpan telemetry data. Menyediakan API untuk integrasi dan dashboard untuk visualisasi.

**Management System:** OTA update server, device management platform, certificate authority untuk identitas perangkat.

#### 4.4 Mengapa CPS/IoT Security Berbeda dan Lebih Kompleks

Keamanan CPS/IoT memiliki tantangan unik yang tidak ada dalam IT konvensional:

1. **Physical safety consequence:** Serangan dapat menyebabkan kerusakan fisik, kebakaran, atau korban jiwa
2. **Resource-constrained devices:** Banyak IoT device memiliki CPU, RAM, dan daya yang sangat terbatas — tidak dapat menjalankan TLS stack penuh atau agen keamanan
3. **Heterogeneity:** Ribuan jenis perangkat dari ratusan vendor dengan berbagai OS, protokol, dan kemampuan keamanan
4. **Long lifecycle:** Perangkat industri beroperasi 20–30 tahun; vulnerability ditemukan setelah bertahun-tahun deployment
5. **Legacy protocol:** Modbus, DNP3 dirancang tanpa kemampuan kriptografi
6. **Physical access risk:** Perangkat IoT sering terpasang di lokasi yang tidak terjaga (outdoor, rumah pengguna)
7. **Scale:** Milyaran perangkat; manual security management tidak mungkin

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph INTERNET[Internet / WAN]
        CLOUD[Cloud Platform\nIoT Hub / Backend]
        MGMT[Management\nSystem\nOTA, PKI, SIEM]
    end

    subgraph EDGE_ZONE[Edge / Gateway Zone]
        GW[IoT Gateway\nProtocol Bridge\nLocal Processing]
        FIREWALL_E[Firewall /\nSecurity Gateway]
    end

    subgraph FIELD_ZONE[Field / Device Zone]
        SENSOR[Sensors\nAktuator\nEnd Nodes]
        PLC[PLC / RTU\nController]
        HMI[HMI\nLocal Control]
    end

    subgraph OT_NETWORK[OT Network — Purdue Level 0-2]
        SCADA[SCADA Server]
        DCS[DCS Controller]
    end

    CLOUD <-->|TLS/HTTPS| FIREWALL_E
    MGMT <-->|TLS| FIREWALL_E
    FIREWALL_E <-->| | GW
    GW <-->|MQTT/CoAP/Modbus| SENSOR
    GW <-->|Modbus/PROFINET| PLC
    PLC <-->|Hardwired/Serial| SENSOR
    HMI <-->|OPC-UA| SCADA
    SCADA <-->|DNP3| DCS
    DCS <-->|Fieldbus| SENSOR

    style INTERNET fill:#e3f2fd
    style EDGE_ZONE fill:#e8f5e9
    style FIELD_ZONE fill:#fff3e0
    style OT_NETWORK fill:#fce4ec
```

---

### 6. Contoh Terapan

**Kasus: Arsitektur Smart Water Treatment Plant**

Sebuah instalasi pengolahan air kota menggunakan sistem CPS/IoT dengan komponen:
- 500+ sensor (pH, klorin, tekanan, aliran) → Perception Layer
- 50 RTU/PLC yang mengendalikan pompa dan katup → Field Level
- Gateway industri di setiap area → Edge Layer
- SCADA server di ruang kontrol → Supervisory Level
- ERP dan billing system di kantor → Business Layer

**Ancaman spesifik domain:**
1. Attacker memanipulasi pembacaan sensor pH → SCADA menganggap air sudah bersih padahal belum → air berbahaya didistribusikan
2. Ransomware mengunci SCADA server → operator tidak dapat memantau atau mengendalikan proses
3. Attacker mengakses PLC melalui remote access yang tidak aman → menutup katup penting

**Implikasi desain keamanan:** Ketersediaan (Availability) adalah prioritas tertinggi, diikuti Integrity (data sensor harus akurat), baru Confidentiality.

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Pemetaan Arsitektur CPS/IoT pada Skenario Lab

**Tujuan:** Mahasiswa mampu mengidentifikasi komponen, lapisan, dan konteks operasional sistem CPS/IoT dari dokumentasi dan diagram yang disediakan.

**Lingkungan Lab:** Dataset arsitektur (PDF/gambar) yang disediakan instruktur, atau simulator IoT seperti Node-RED + MQTT broker lokal.

**Langkah Kerja:**
1. Berdasarkan skenario yang diberikan instruktur (misal: smart building, sistem irigasi cerdas), identifikasi semua komponen
2. Klasifikasikan setiap komponen ke dalam lapisan arsitektur (Perception/Network/Processing/Application)
3. Gambar Data Flow Diagram sederhana menggunakan draw.io atau Mermaid
4. Identifikasi minimal 3 trust boundary dalam arsitektur
5. Untuk setiap trust boundary: apa yang mengalir melewatinya dan apa risikonya?

**Catatan Etika:** Seluruh analisis berbasis dokumentasi dan diagram yang disediakan. Tidak ada akses ke sistem nyata.

---

### 8. Latihan Pemahaman

**Soal 1 (Konsep — C2)**
Jelaskan mengapa prioritas keamanan di OT/CPS berbeda dengan IT. Mengapa Availability menjadi prioritas tertinggi di sistem ICS, sementara dalam IT konvensional Confidentiality sering diprioritaskan?

**Soal 2 (Identifikasi — C4)**
Sebuah smart meter listrik terhubung ke gateway rumah melalui Zigbee, gateway ke cloud server melalui 4G LTE, dan cloud server dapat diakses operator melalui web browser. Identifikasi semua komponen dan klasifikasikan ke lapisan arsitektur IoT.

**Soal 3 (Analisis — C4)**
Mengapa perangkat IoT dengan lifecycle 15–20 tahun menciptakan tantangan keamanan yang jauh lebih besar dibanding server IT biasa? Jelaskan minimal tiga konsekuensi keamanannya.

**Soal 4 (Perbandingan — C4)**
Bandingkan protokol komunikasi di IT (HTTP, TLS) dengan protokol di OT/ICS (Modbus, DNP3) dari perspektif kemampuan keamanan bawaan. Apa yang membuat protocol OT lama rentan?

**Soal 5 (Analisis — C4)**
Pada insiden BlackEnergy Ukraine 2015: identifikasi lapisan arsitektur mana yang dikompromis, jenis serangan apa yang digunakan, dan mengapa dampaknya bisa fisik (pemadaman listrik).

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Arsitektur Smart Hospital (C4–C5)**

Rumah sakit modern memiliki: infusion pump cerdas yang terhubung ke WiFi, glucometer yang sync via Bluetooth ke tablet perawat, HVAC building automation system berbasis BACnet, sistem monitoring pasien ICU dengan terhubung ke nurse station, dan semua sistem ini terhubung ke EMR (Electronic Medical Record) system.

*Pertanyaan:*
1. Buat daftar semua komponen CPS/IoT yang teridentifikasi dan klasifikasikan ke lapisan arsitektur
2. Mengapa medical IoT memiliki persyaratan keamanan yang berbeda dari smart home IoT? Identifikasi minimal tiga perbedaan fundamental
3. Jika harus memilih satu sistem yang paling kritis untuk diamankan terlebih dahulu, sistem mana yang Anda pilih dan mengapa?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 1:**
Prioritas keamanan berbeda karena konsekuensi yang berbeda. Dalam IT, kehilangan ketersediaan (server down) umumnya berdampak finansial dan reputasional — serius tapi dapat pulih. Dalam OT/CPS, ketidaktersediaan dapat berarti: reaktor nuklir tanpa sistem cooling, rumah sakit tanpa sistem life support, atau pabrik kimia tanpa kendali proses — yang dapat mengakibatkan kerusakan fisik, kebakaran, atau korban jiwa. Karena itu, operator OT tidak dapat sembarangan menerapkan patch atau restart sistem; setiap maintenance harus dijadwalkan dengan sangat hati-hati.

**Jawaban Soal 5:**
Layer yang dikompromis: Network Layer (lateral movement melalui VPN) dan Application Layer (SCADA HMI software). Jenis serangan: spear phishing → credential theft → lateral movement ke network ICS → akibatnya: breaker tripped secara remote (Physical Layer terpengaruh). Dampak fisik karena sistem SCADA memiliki kendali langsung atas hardware breaker — ini adalah nature dari CPS: siber mengendalikan fisik.

**Kunci Studi Kasus:**
Medical IoT berbeda karena: (1) Patient safety directly at risk — malfunction infusion pump = overdose; (2) Regulatory compliance sangat ketat (FDA untuk AS, BPOM untuk Indonesia); (3) Device sering dalam "sterile" environment dan tidak bisa disentuh selama digunakan; (4) Denial of service bisa berarti kehilangan nyawa; (5) Data yang dikumpulkan adalah PHI (Protected Health Information) dengan persyaratan privasi sangat ketat.

Sistem paling kritis: infusion pump — karena kesalahan langsung membahayakan nyawa pasien.

---

### 11. Ringkasan Bab

CPS/IoT adalah ekosistem yang mengintegrasikan komputasi dengan proses fisik di dunia nyata. Arsitektur berlapis (Perception → Network → Processing → Application) membantu memahami aliran data dan tanggung jawab keamanan di setiap lapisan. Perbedaan fundamental IT vs OT/CPS: prioritas Availability atas Confidentiality, lifecycle panjang, real-time constraint, dan dampak fisik dari kegagalan. ICS/SCADA adalah subkategori CPS untuk infrastruktur kritis dengan model Purdue yang memisahkan OT dan IT. Memahami arsitektur ini adalah fondasi untuk analisis ancaman, evaluasi firmware, dan perancangan kontrol keamanan.

---

### 12. Refleksi Profesional

1. Serangan siber pada infrastruktur kritis (listrik, air, transportasi) semakin sering terjadi dan semakin canggih. Sebagai security professional yang bekerja di sektor ini, bagaimana Anda menyeimbangkan kewajiban untuk melindungi sistem dengan tanggung jawab kepada publik yang bergantung pada infrastruktur tersebut?

2. Banyak sistem ICS beroperasi dengan perangkat yang dibeli 20 tahun lalu dan tidak akan diganti dalam 10 tahun ke depan, meskipun diketahui rentan. Operator tidak mampu mengganti infrastruktur mahal ini setiap kali kerentanan ditemukan. Sebagai security analyst, strategi apa yang Anda rekomendasikan untuk melindungi "legacy CPS" yang tidak dapat di-patch?

3. Negara-bangsa (state actors) adalah ancaman nyata bagi infrastruktur kritis. Apakah perusahaan dan operator infrastruktur kritis bertanggung jawab untuk mempertahankan diri dari ancaman tingkat negara? Di mana batas antara tanggung jawab organisasi dan tanggung jawab pemerintah dalam melindungi infrastruktur kritis nasional?

---

---

## Bab 2 — Asset Inventory, Data Flow, dan Attack Surface Analysis

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: melakukan asset inventory pada ekosistem CPS/IoT dan mengklasifikasikan aset berdasarkan kritikalitas (C4); menyusun data flow diagram yang mencerminkan aliran data, trust boundary, dan titik eksposur (C4); menganalisis attack surface dari perspektif berbagai aktor ancaman (C4); menghubungkan aset dan data flow dengan potensi ancaman yang relevan (C5). *Sub-CPMK-1 / CPMK-1 / Eval-1*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    AS[Attack Surface Analysis\nCPS/IoT]

    AS --> INV[Asset Inventory]
    INV --> PHYS[Physical Assets:\nSensor, PLC, Gateway]
    INV --> SOFT[Software Assets:\nFirmware, OS, App]
    INV --> DATA_A[Data Assets:\nTelemetry, Config,\nCredential]
    INV --> NET[Network Assets:\nProtocol, Channel,\nTopologi]

    AS --> DFD2[Data Flow Diagram]
    DFD2 --> SOURCE[Data Source:\nSensor input]
    DFD2 --> TRANSIT[Data in Transit:\nEncrypted/Unencrypted?]
    DFD2 --> PROC2[Data Processing:\nEdge/Cloud]
    DFD2 --> STORE2[Data Storage:\nDB/Log/Cache]

    AS --> TB[Trust Boundary]
    TB --> EXT_TB[External/Internet\nboundary]
    TB --> OT_IT[OT-IT boundary]
    TB --> DEVICE[Device-Network\nboundary]

    AS --> ATK_SRF[Attack Surface Components]
    ATK_SRF --> PHYS_ATK[Physical:\nJTAG, USB, Serial]
    ATK_SRF --> NET_ATK[Network:\nOpen ports, Protocols]
    ATK_SRF --> SOFT_ATK[Software:\nAPI, Web UI, OTA]
    ATK_SRF --> SUPPLY[Supply Chain:\nFirmware, Components]
```

---

### 3. Pengantar Kontekstual

"Anda tidak dapat melindungi apa yang tidak Anda ketahui ada." Kutipan sederhana ini sangat relevan dalam ekosistem CPS/IoT yang heterogen dan tersebar. Banyak organisasi tidak memiliki inventaris perangkat IoT yang lengkap — perangkat shadow IoT (terhubung ke jaringan tanpa sepengetahuan IT) adalah masalah nyata. Pada 2020, survei Infoblox menemukan bahwa rata-rata organisasi memiliki 1.000+ perangkat IoT yang tidak terdokumentasi.

---

### 4. Landasan Teori

#### 4.1 Asset Inventory dalam CPS/IoT

Asset inventory adalah daftar komprehensif semua aset dalam ekosistem CPS/IoT, termasuk atribut yang relevan untuk keamanan. NISTIR 8259 dan ENISA menyebut asset inventory sebagai aktivitas dasar yang harus dimiliki setiap organisasi yang mengelola perangkat IoT.

**Kategori Aset CPS/IoT:**

```
1. HARDWARE/PHYSICAL ASSETS
   - End devices: sensor, aktuator, kamera, smart meter
   - Controllers: PLC, RTU, DCS
   - Gateway/Edge devices
   - Network devices: switch, router, wireless AP
   - HMI workstations dan SCADA servers

2. SOFTWARE/FIRMWARE ASSETS
   - Firmware perangkat (versi, vendor, known CVE)
   - Operating system (embedded Linux, RTOS, Windows Embedded)
   - Application software (SCADA, HMI, management console)
   - Middleware dan API

3. DATA ASSETS
   - Telemetry data (sensor readings, events)
   - Configuration files (kritis — sering mengandung credential)
   - Credential database (device certificates, passwords)
   - Log files (audit trail)
   - Intellectual property (control logic, process parameters)

4. NETWORK/COMMUNICATION ASSETS
   - Protocol yang digunakan (MQTT, Modbus, BACnet, DNP3)
   - Network topology dan segmentation
   - Wireless channels (Zigbee, WiFi, BLE, LoRa)
   - Cloud endpoints dan API
```

**Template Asset Register:**

| Asset ID | Nama | Tipe | Vendor | Firmware Version | IP/Location | Criticality | Known CVE | Owner |
|----------|------|------|--------|-----------------|-------------|-------------|-----------|-------|
| DEV-001 | Sensor Suhu A | Sensor | Vendor X | 2.1.3 | 192.168.10.5 | Medium | CVE-2023-xxxx | Tim OT |

**Criticality Classification:**
- **Critical:** Kegagalan berdampak keselamatan manusia atau pemadaman proses kritis
- **High:** Kegagalan berdampak produksi atau compliance
- **Medium:** Kegagalan berdampak efisiensi operasional
- **Low:** Kegagalan berdampak kenyamanan atau estetika

#### 4.2 Data Flow Diagram (DFD) untuk CPS/IoT

DFD dalam konteks keamanan CPS/IoT mengikuti notasi yang sama dengan threat modelling (dibahas Bab 3), tetapi berfokus pada pemahaman aliran data dan trust boundary.

**Elemen DFD:**
- **External Entity** (kotak): Sumber atau tujuan data yang berada di luar sistem kendali — user, perangkat field, cloud
- **Process** (lingkaran/oval): Komponen yang memproses data — firmware, gateway, SCADA server
- **Data Store** (garis ganda): Tempat penyimpanan data — database, file konfigurasi, log
- **Data Flow** (panah): Aliran data antara elemen
- **Trust Boundary** (garis putus-putus): Batas antara zona kepercayaan yang berbeda

**Pertanyaan yang harus dijawab oleh DFD:**
1. Data apa yang mengalir dari mana ke mana?
2. Apakah data dienkripsi saat transit?
3. Di mana data disimpan dan oleh siapa?
4. Siapa yang memiliki akses ke data di setiap titik?
5. Di mana trust boundary berada?

#### 4.3 Attack Surface Analysis

Attack surface adalah jumlah total titik masuk yang dapat digunakan attacker untuk mencoba mengakses atau mengeksploitasi sistem. Semakin kecil attack surface, semakin aman sistem.

**Dimensi Attack Surface CPS/IoT:**

**Physical Attack Surface:**
- Port debug (JTAG, UART, SWD) — sering terbuka dan tidak terlindungi
- USB port yang dapat menyuntikkan firmware
- SD card slot yang dapat menyimpan malware
- PCB yang dapat di-probe untuk side-channel analysis
- Lokasi fisik yang tidak dijaga (outdoor mounting, public space)

**Network Attack Surface:**
- Port terbuka yang tidak diperlukan (telnet, FTP, HTTP pada perangkat IoT)
- Protokol tanpa enkripsi (Modbus, MQTT tanpa TLS)
- Wireless channel yang dapat di-sniff (Zigbee, BLE)
- Default atau lemahnya konfigurasi WiFi
- Firewall rules yang terlalu permisif

**Software/Firmware Attack Surface:**
- Web UI management (sering berisi SQLi, XSS, CSRF)
- API endpoint yang tidak terautentikasi
- OTA update mechanism (dapat dimanipulasi jika tidak ada signature verification)
- Third-party library dengan CVE
- Hardcoded credential dalam firmware

**Supply Chain Attack Surface:**
- Firmware yang didownload dari vendor tanpa verifikasi
- Komponen hardware dari supplier tidak terpercaya
- Development tools yang dikompromis

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph EXTERNAL[External Zone — Internet]
        CLOUD2[Cloud IoT\nPlatform]
        VENDOR[Vendor Portal\nOTA Update]
        USER[End User\nMobile App]
    end

    subgraph DMZ2[DMZ — Demilitarized Zone]
        API_GW[API Gateway]
        FW1[Firewall 1]
        FW2[Firewall 2]
    end

    subgraph INTERNAL[Internal Network]
        MQTT_B[MQTT Broker]
        DB2[TimeSeries\nDatabase]
        SCADA2[SCADA\nServer]
    end

    subgraph FIELD2[Field Zone — OT Network]
        GW2[Field Gateway]
        SENSOR2[Sensors]
        PLC2[PLC]
    end

    USER -->|HTTPS| API_GW
    CLOUD2 -->|HTTPS| FW1
    VENDOR -->|HTTPS — OTA| FW1
    FW1 --> API_GW
    API_GW --> FW2
    FW2 --> MQTT_B
    MQTT_B --> DB2
    MQTT_B --> SCADA2
    GW2 -->|MQTT TLS| MQTT_B
    SENSOR2 -->|Zigbee/Serial| GW2
    PLC2 -->|Modbus| GW2

    TB1["Trust Boundary 1:\nInternet ↔ DMZ"]
    TB2["Trust Boundary 2:\nDMZ ↔ Internal"]
    TB3["Trust Boundary 3:\nIT ↔ OT"]

    style EXTERNAL fill:#ffcccc
    style DMZ2 fill:#ffe0cc
    style INTERNAL fill:#ccffcc
    style FIELD2 fill:#ccccff
```

---

### 6. Contoh Terapan

**Kasus: Asset Inventory dan Attack Surface Analysis pada Smart Factory**

Sebuah perusahaan manufaktur melakukan assessment keamanan awal. Tim menemukan:
- 200 sensor IoT produksi dengan firmware yang beragam (32 vendor berbeda)
- 15 PLC dengan sistem operasi Windows Embedded yang sudah end-of-life
- MQTT broker tanpa autentikasi — semua perangkat dapat publish/subscribe ke semua topik
- Web UI manajemen gateway dapat diakses tanpa VPN dari internet
- Tidak ada catatan firmware version untuk 40% perangkat

Attack surface yang teridentifikasi:
1. **Network:** MQTT broker tanpa auth — attacker dalam jaringan yang sama dapat inject perintah palsu
2. **Software:** Windows Embedded EOL — tidak ada patch keamanan tersedia
3. **Physical:** Sensor terpasang di area produksi tanpa pengamanan fisik — JTAG port accessible
4. **Shadow IT:** 23 perangkat IoT tidak terdokumentasi yang terhubung ke jaringan

**Rekomendasi prioritas:**
1. Segera: Aktifkan autentikasi MQTT (username/password + client certificate)
2. Segera: Blokir akses web UI dari internet, wajibkan VPN
3. Jangka menengah: Mulai program patch/upgrade Windows Embedded
4. Jangka panjang: Implementasikan device management platform untuk inventori otomatis

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Asset Discovery dan Attack Surface Mapping pada Lab IoT

**Prasyarat:** Akses ke lab IoT yang disediakan instruktur (atau dataset pcap + device inventory yang disanitasi)

**Langkah Kerja:**
1. Dari topologi lab yang diberikan, buat asset register menggunakan template Lampiran D
2. Untuk setiap perangkat, identifikasi: tipe, vendor/model, versi firmware (jika tersedia), protocol yang digunakan, port terbuka
3. Buat DFD Level 1 dari sistem lab menggunakan draw.io atau Mermaid
4. Tandai semua trust boundary dalam DFD
5. Identifikasi 5 attack surface terbesar dan ranking berdasarkan risk (severity × likelihood)

**Catatan Etika:** Gunakan hanya dataset dan perangkat yang disediakan instruktur. Tidak ada scanning aktif terhadap jaringan luar.

---

### 8. Latihan Pemahaman

**Soal 1 (Identifikasi — C4)**
Sebuah smart building memiliki komponen berikut: 500 smart bulb (Zigbee), 100 door lock (BLE), 50 HVAC sensor (WiFi), building automation controller (BACnet/IP), security camera (RTSP over IP), dan cloud management platform. Buat asset inventory dengan klasifikasi criticality untuk masing-masing komponen.

**Soal 2 (Analisis — C4)**
Jelaskan mengapa "shadow IoT" (perangkat yang terhubung tanpa sepengetahuan IT/security team) merupakan risiko keamanan yang signifikan. Berikan dua contoh skenario serangan yang memanfaatkan shadow IoT.

**Soal 3 (Evaluasi — C5)**
Sebuah perangkat IoT memiliki attack surface berikut: (a) Port UART debug terbuka, (b) Web UI management tanpa HTTPS, (c) Firmware update tanpa signature verification, (d) Default password 'admin'. Ranking attack surface ini dari yang paling berbahaya ke yang paling tidak berbahaya dan jelaskan reasoning Anda.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Attack Surface Analysis Smart Grid (C4–C5)**

Sebuah perusahaan listrik memiliki 2 juta smart meter yang terdistribusi di seluruh kota. Smart meter berkomunikasi ke collector via RF mesh network, collector ke data concentrator via PLC (Power Line Communication), dan data concentrator ke head-end system via dedicated fiber. Head-end system terhubung ke billing system dan SCADA via IP network internal.

*Pertanyaan:*
1. Buat DFD tingkat tinggi untuk sistem ini dengan semua trust boundary
2. Identifikasi dan analisis attack surface dari perspektif: (a) attacker dengan akses fisik ke satu smart meter, (b) attacker yang berhasil kompromis satu data concentrator
3. Jika attacker berhasil inject perintah palsu ke 100.000 smart meter secara bersamaan (disconnect command), apa dampak fisik, operasional, dan sosialnya?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 3 (Ranking Attack Surface):**
Ranking dari paling berbahaya: (1) Firmware update tanpa signature verification — ini memungkinkan RCE (Remote Code Execution) permanen; attacker dapat flash firmware berbahaya dan mendapat kontrol penuh perangkat secara persisten; (2) Default password 'admin' — sangat mudah dieksploitasi, terutama jika manajemen interface terhubung ke internet; (3) Web UI management tanpa HTTPS — credential dan session dapat dicuri, tapi memerlukan posisi network attacker; (4) Port UART debug terbuka — memerlukan akses fisik, membatasi skala serangan, meski tetap serius untuk targeted attack.

**Kunci Studi Kasus:**
Perspektif (a) — attacker dengan satu smart meter: akses fisik ke UART/debug port, dapat ekstrak firmware dan credential untuk RF mesh network, menggunakan credential tersebut untuk berkomunikasi dengan collector, berpotensi lateral movement ke meter lain dalam jangkauan RF.

Dampak inject perintah disconnect ke 100.000 meter: (1) Fisik — 100.000 rumah/gedung tanpa listrik; (2) Operasional — emergency response system perusahaan listrik kewalahan; dispatch truck ke setiap meter karena reconnect mungkin perlu manual visit; (3) Sosial — gangguan medis untuk pengguna perangkat medis rumahan, kecelakaan akibat traffic light mati, kerugian bisnis; (4) Keuangan — biaya operasional reconnect massal.

---

### 11. Ringkasan Bab

Asset inventory adalah fondasi keamanan CPS/IoT — Anda tidak dapat melindungi apa yang tidak Anda tahu ada. Kategori aset mencakup hardware, firmware/software, data, dan jaringan, masing-masing dengan kritikalitas yang berbeda. DFD memvisualisasikan aliran data dan trust boundary — kunci untuk memahami di mana data terekspos dan siapa yang bisa mengaksesnya. Attack surface CPS/IoT memiliki dimensi fisik (debug port, physical access), network (open ports, unencrypted protocols), software (unpatched firmware, web UI), dan supply chain — jauh lebih luas dari attack surface IT konvensional.

---

### 12. Refleksi Profesional

1. Melakukan asset inventory yang komprehensif memerlukan waktu dan sumber daya yang signifikan, namun tanpanya program keamanan bersifat buta. Bagaimana Anda meyakinkan manajemen untuk berinvestasi dalam asset management program, terutama di industri di mana ROI keamanan sulit diukur?

2. Dalam ekosistem smart city dengan jutaan perangkat IoT dari berbagai vendor, tidak ada satu entitas pun yang memiliki visibilitas lengkap atas semua aset. Bagaimana Anda merancang model tata kelola keamanan yang efektif dalam ekosistem yang terfragmentasi seperti ini?

3. Ketika melakukan attack surface analysis, Anda menemukan bahwa sebuah vendor perangkat IoT yang digunakan perusahaan menyimpan telemetry data di server mereka (di luar kendali perusahaan) tanpa disebutkan dalam kontrak. Apa langkah yang harus diambil? Ini adalah masalah teknis, legal, atau keduanya?

---

---

## Bab 3 — Threat Modelling, Safety-Security Interaction, dan Etika Pengujian

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menerapkan metodologi threat modelling (STRIDE/PASTA) pada sistem CPS/IoT (C3); menganalisis interaksi antara safety dan security dalam sistem siber-fisik (C4); mengevaluasi dampak privacy dalam konteks CPS/IoT (C4); menjelaskan dan menerapkan batasan etik dan legal dalam pengujian keamanan CPS/IoT (C2). *Sub-CPMK-1 / CPMK-1 / Eval-1*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    TM_CPS[Threat Modelling\nCPS/IoT]

    TM_CPS --> METH[Metodologi]
    METH --> STRIDE_CPS[STRIDE untuk CPS/IoT\nS-T-R-I-D-E + Safety]
    METH --> PASTA2[PASTA — Process for\nAttack Simulation &\nThreat Analysis]
    METH --> TARA[TARA — Threat Analysis\n& Risk Assessment\nISO 21434 kendaraan]

    TM_CPS --> SAFETY_SEC[Safety-Security\nInteraction]
    SAFETY_SEC --> CONFLICT[Safety vs Security\nConflict Scenarios]
    SAFETY_SEC --> SYNERGY[Safety-Security Synergy\nScenarios]
    SAFETY_SEC --> SIL[Safety Integrity Level\nIEC 61508/61511]

    TM_CPS --> PRIV[Privacy dalam CPS/IoT]
    PRIV --> PIA[Privacy Impact\nAssessment]
    PRIV --> PII_IOT[PII dalam IoT:\nLocation, behavior,\nhealth data]
    PRIV --> GDPR_IOT[GDPR / UU PDP\naplikasi IoT]

    TM_CPS --> ETHICS[Etika dan Legal]
    ETHICS --> SCOPE_ETH[Scope testing:\nHanya yang diotorisasi]
    ETHICS --> RESP[Responsible disclosure]
    ETHICS --> UU_ITE2[UU ITE Indonesia\ndalam konteks CPS]
```

---

### 3. Pengantar Kontekstual

Threat modelling untuk CPS/IoT bukan sekadar mengaplikasikan STRIDE biasa. Sistem siber-fisik memiliki dimensi tambahan yang tidak ada dalam IT: ancaman terhadap safety (keselamatan fisik), interaksi antara cyber dan physical domain yang kompleks, dan implikasi privasi dari pengumpulan data sensor yang masif.

Bayangkan sebuah sistem kendali oven industri: attacker yang menaikkan suhu melebihi batas keamanan tidak hanya mencuri data — ia berpotensi menyebabkan kebakaran, ledakan, atau korban jiwa. Ini adalah "weaponized safety failure" — menggunakan kelemahan keamanan untuk memicu kegagalan keselamatan.

---

### 4. Landasan Teori

#### 4.1 STRIDE dalam Konteks CPS/IoT

STRIDE (Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege) memiliki nuansa khusus dalam CPS/IoT:

| Kategori STRIDE | Contoh CPS/IoT | Dampak Unik |
|-----------------|----------------|-------------|
| **S**poofing | Sensor palsu mengirim data suhu yang salah | Proses fisik menjadi tidak terkendali |
| **T**ampering | Modifikasi firmware PLC | Perubahan perilaku fisik yang berbahaya |
| **R**epudiation | Menghapus log kontrol dari HMI | Tidak ada audit trail untuk kecelakaan industri |
| **I**nfo Disclosure | Bocornya process parameter | Mengekspos intellectual property produksi |
| **D**enial of Service | Flooding MQTT broker | Kehilangan kendali atas proses fisik |
| **E**levation of Privilege | Dari monitoring ke kontrol | Dari "read only" menjadi mampu mengubah setpoint |

**Tambahan kategori untuk CPS: "Safety Failure":**
Ancaman yang tidak mengkompromis CIA secara langsung, tetapi memicu kegagalan keselamatan melalui manipulasi halus:
- Memanipulasi sensor dalam batas "valid" tapi di posisi yang memicu kondisi tidak aman
- Menonaktifkan alarm yang seharusnya melindungi proses
- Memanipulasi timing kontrol sehingga sekuens yang seharusnya aman menjadi berbahaya

#### 4.2 Proses Threat Modelling CPS/IoT (Step-by-Step)

```
LANGKAH 1: DEFINE SYSTEM SCOPE
  - Batas sistem (apa yang di-in scope, apa yang di-out)
  - Stakeholder yang berkepentingan
  - Data apa yang diproses

LANGKAH 2: BUILD DATA FLOW DIAGRAM
  - Semua komponen dan koneksi
  - Trust boundary
  - Aliran data kritis

LANGKAH 3: ENUMERATE THREATS (STRIDE per elemen)
  - Untuk setiap External Entity → Spoofing, Repudiation
  - Untuk setiap Process → semua 6 STRIDE
  - Untuk setiap Data Store → Tampering, Info Disclosure, DoS
  - Untuk setiap Data Flow → Tampering, Info Disclosure, DoS

LANGKAH 4: RATE THREATS (DREAD atau CVSS)
  - Severity = Likelihood × Impact
  - Pertimbangkan safety impact sebagai multiplier

LANGKAH 5: IDENTIFY MITIGATIONS
  - Untuk setiap ancaman: mitigasi teknis dan operasional

LANGKAH 6: VALIDATE
  - Apakah mitigasi sudah efektif?
  - Apakah ada ancaman yang terlewat?
```

#### 4.3 Safety-Security Interaction

Hubungan antara safety dan security dalam CPS bersifat kompleks — bisa konfliktual atau sinergis.

**Skenario Konflik Safety-Security:**

*Konteks:* Sistem kendali mesin memiliki tombol emergency stop yang harus selalu dapat ditekan operator.

- **Security requirement:** Autentikasi sebelum akses ke kontrol
- **Safety requirement:** Emergency stop harus selalu dapat diakses TANPA autentikasi (karena dalam keadaan darurat, tidak ada waktu untuk login)
- **Conflict:** Security ingin lock out unauthorized access; Safety ingin ensure immediate access

**Resolusi:** Emergency stop secara fisik tidak melalui sistem digital; tombol fisik langsung memutus daya ke aktuator (hardwired safety). Digital control system hanya untuk operasi normal.

**Skenario Sinergis Safety-Security:**

- Security monitoring yang mendeteksi serangan siber juga dapat mendeteksi kegagalan proses fisik
- Secure boot memastikan kode kontrol tidak dimanipulasi — baik untuk security dan safety
- Audit log keamanan memberikan forensic trail untuk investigasi kecelakaan industri

**Safety Integrity Level (SIL) — IEC 61508/61511:**
SIL adalah ukuran kemampuan sistem keselamatan untuk menjalankan fungsi keselamatan yang diperlukan. SIL 1–4 (SIL 4 paling kritis). Keamanan siber mempengaruhi SIL karena serangan dapat menyebabkan kegagalan fungsi keselamatan.

#### 4.4 Privacy Impact Assessment dalam IoT

IoT mengumpulkan data dalam jumlah besar yang sering mengandung informasi pribadi:

- **Location data:** Smart meter → pola kehadiran di rumah
- **Health data:** Wearable → kondisi medis, aktivitas fisik
- **Behavior data:** Smart TV/assistant → konten yang dikonsumsi
- **Industrial data:** Process parameter → IP industri, kapasitas produksi

**Privacy by Design untuk IoT:**
1. **Data minimization:** Kumpulkan hanya data yang benar-benar diperlukan
2. **Purpose limitation:** Data hanya digunakan sesuai tujuan asli pengumpulan
3. **Storage limitation:** Hapus data setelah tidak diperlukan
4. **Security by default:** Enkripsi dan akses kontrol dari awal

**UU PDP Indonesia (UU No. 27 Tahun 2022) — Implikasi IoT:**
- Pengumpulan data pribadi via IoT memerlukan consent eksplisit
- Data lokasi dan data kesehatan termasuk data sensitif (persyaratan lebih ketat)
- Wajib melaporkan pelanggaran data dalam 14 hari ke otoritas

#### 4.5 Batasan Etik dan Legal Pengujian CPS/IoT

Pengujian keamanan CPS/IoT memiliki risiko yang jauh lebih tinggi dari pengujian IT konvensional:

**Yang TIDAK boleh dilakukan tanpa otorisasi tertulis:**
- Pengujian pada perangkat IoT yang terhubung ke jaringan produksi
- Scanning aktif terhadap sistem ICS/SCADA (dapat menyebabkan gangguan proses)
- Pengiriman command ke PLC atau aktuator — bahkan dalam "read-only" mode
- Analisis firmware perangkat milik pihak ketiga (dapat melanggar DMCA/hak cipta)
- Pengujian pada jaringan kendaraan (CAN bus) yang masih terpasang di kendaraan

**Responsible Disclosure untuk CPS/IoT:**
Menemukan kerentanan pada firmware IoT publik? Proses yang benar:
1. Dokumentasikan temuan tanpa mengeksploitasinya lebih jauh
2. Hubungi vendor secara pribadi (private disclosure)
3. Beri waktu 90 hari untuk vendor memperbaiki (coordinated disclosure)
4. Jika vendor tidak merespons, pertimbangkan public disclosure dengan panduan meminimalkan risiko

---

### 5. Model atau Arsitektur

```mermaid
flowchart LR
    subgraph THREAT_MODEL_PROCESS[Proses Threat Modelling CPS/IoT]
        SCOPE2[1. Define\nSystem Scope]
        DFD3[2. Build DFD\n+ Trust Boundary]
        ENUM[3. Enumerate\nThreats STRIDE\n+ Safety Failure]
        RATE[4. Rate Threats\nSeverity × Likelihood\n× Safety Multiplier]
        MITIG2[5. Identify\nMitigations]
        VALID2[6. Validate\n& Document]
    end

    SCOPE2 --> DFD3
    DFD3 --> ENUM
    ENUM --> RATE
    RATE --> MITIG2
    MITIG2 --> VALID2
    VALID2 -->|Iterasi jika\nada perubahan| SCOPE2
```

---

### 6. Contoh Terapan

**Kasus: Threat Model SCADA Pabrik Pengolahan Bahan Kimia**

Sistem: Sensor → PLC → SCADA Server → HMI Operator

Analisis STRIDE pada data flow "SCADA Server → HMI Operator":

| ID | Ancaman | Kategori | Safety Impact | Severity | Mitigasi |
|----|---------|----------|---------------|----------|---------|
| T1 | Spoofing HMI: attacker berpura-pura menjadi HMI yang sah | S | Operator dapat menerima perintah palsu | Critical | mTLS authentication |
| T2 | Tampering nilai setpoint yang dikirim ke HMI | T | Operator diberi informasi yang salah | Critical | Data integrity check, signed messages |
| T3 | Replay attack: mengirim ulang perintah lama | T/S | Perintah yang tidak relevan dieksekusi | High | Timestamp + nonce |
| T4 | DoS pada koneksi SCADA-HMI | D | Operator kehilangan visibilitas | High | Redundant communication channel |
| T5 | Operator palsu menggunakan credential curian | E | Unauthorized control access | Critical | MFA untuk operator akses |

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Threat Modelling pada Sistem Smart Irrigation

**Prasyarat:** Pemahaman DFD dan STRIDE (Bab 2-3)

**Skenario:** Sistem irigasi cerdas pertanian yang memiliki soil moisture sensors (LoRa), central gateway (Raspberry Pi), cloud platform (AWS IoT), dan mobile app operator.

**Langkah Kerja:**
1. Buat DFD Level 1 untuk sistem ini (gunakan draw.io atau mermaid)
2. Identifikasi semua trust boundary
3. Untuk setiap elemen DFD, lakukan analisis STRIDE — gunakan worksheet Lampiran D
4. Identifikasi 3 ancaman yang paling berpotensi menyebabkan safety failure
5. Untuk setiap ancaman: tentukan severity, likelihood, dan mitigasi
6. Buat Safety-Ethics Memo (1 halaman): ancaman apa yang paling kritis dan bagaimana menguji mitigasi secara aman

---

### 8. Latihan Pemahaman

**Soal 1 (Analisis — C4)**
Jelaskan dengan contoh konkret bagaimana serangan Tampering pada sensor suhu di sistem HVAC gedung dapat menyebabkan safety failure. Mengapa ini lebih dari sekadar masalah ketersediaan atau kerahasiaan data?

**Soal 2 (Evaluasi — C5)**
Diberi dua ancaman: (a) Attacker mencuri semua data historis produksi (Information Disclosure, tidak ada safety impact), dan (b) Attacker dapat membuat sensor level cairan di tangki kimia membaca 20% lebih rendah dari nilai nyata (Tampering, safety impact tinggi). Mana yang harus diprioritaskan dan mengapa?

**Soal 3 (Analisis — C4)**
Jelaskan konflik safety-security dalam konteks perangkat medis implan (pacemaker/implanted defibrillator). Bagaimana penanganan update firmware yang aman tanpa mengancam keselamatan pasien?

**Soal 4 (Aplikasi — C3)**
Sebuah smart home hub mengumpulkan: (a) data konsumsi listrik setiap 15 menit, (b) log aktivasi sensor gerak, (c) riwayat perintah voice assistant. Lakukan Privacy Impact Assessment singkat: data apa yang sensitif, risiko privasi apa yang ada, dan mitigasi apa yang diperlukan?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Threat Model Sistem Kendali Kendaraan Listrik (C4–C5)**

Kendaraan listrik modern memiliki: battery management system (BMS), motor controller, charging controller (untuk EVSE/charger), vehicle-to-cloud connectivity (V2C), dan over-the-air update capability. Semua terhubung via CAN bus internal dan ada gateway untuk komunikasi eksternal.

*Pertanyaan:*
1. Buat threat model menggunakan STRIDE untuk komponen "OTA Update Module" — identifikasi minimal 6 ancaman
2. Untuk setiap ancaman, tentukan: apakah ada safety impact? Jika ya, jelaskan mekanismenya
3. Berikan justifikasi: apakah firmware update untuk kendaraan yang sedang beroperasi di jalan diperbolehkan? Apa batasan etis yang harus diterapkan?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 1:**
Serangan Tampering pada sensor suhu HVAC: Attacker memanipulasi sensor suhu agar melaporkan suhu 18°C padahal aktualnya 32°C → HVAC mati karena menganggap ruangan sudah dingin → suhu aktual terus naik → jika ada server room atau laboratorium dengan peralatan sensitif panas → peralatan overheat dan rusak. Lebih serius: jika ini di fasilitas medis atau industri yang memerlukan suhu terkontrol untuk proses tertentu (obat, bahan kimia reaktif), overheating dapat menyebabkan degradasi produk atau bahkan reaksi berbahaya. Ini melampaui CIA — ini adalah weaponized safety failure.

**Jawaban Soal 2:**
Ancaman (b) harus diprioritaskan meskipun (a) tampak lebih jelas sebagai pelanggaran keamanan. Alasan: (b) memiliki safety impact langsung — sensor level yang terlalu rendah dapat menyebabkan tangki dikira kosong padahal penuh → overflow bahan kimia berbahaya → kebocoran, kebakaran, korban jiwa. Ancaman dengan safety consequence selalu mendapat multiplier risiko dalam konteks CPS. (a) adalah High; (b) adalah Critical karena safety impact.

**Kunci Studi Kasus:**
OTA Update Module — ancaman STRIDE:
S: Spoofing update server → firmware berbahaya terlihat sah. Safety: firmware yang dimodifikasi dapat mengubah parameter keselamatan kendaraan.
T: Tampering dengan firmware image selama transmisi. Safety: perubahan kode kontrol rem atau akselerasi.
R: Repudiation — produsen menyangkal telah mengirim update berbahaya. Forensic challenge.
I: Info Disclosure — update mengandung IP desain kendaraan.
D: DoS pada proses update → kendaraan dengan firmware korup tidak dapat beroperasi.
E: Elevation of privilege → akses ke fungsi engineering mode melalui update mechanism.

Batasan etis update kendaraan beroperasi: dilarang. Update hanya ketika kendaraan diam, ignition off, terkoneksi ke charger (kondisi yang diketahui aman). Ini bukan hanya etika — ini adalah persyaratan keselamatan fungsional (IEC 61508).

---

### 11. Ringkasan Bab

Threat modelling CPS/IoT menggunakan STRIDE sebagai kerangka dasar dengan tambahan kategori "Safety Failure" untuk ancaman yang berdampak fisik. Proses terstruktur: define scope → DFD → enumerate threats → rate → mitigate → validate. Safety-security interaction bisa konflik (emergency access vs authentication) atau sinergis (audit log untuk forensic kecelakaan). Privacy dalam IoT mencakup data perilaku, lokasi, dan kesehatan yang memerlukan Privacy by Design. Batasan etik pengujian CPS/IoT sangat ketat: scanning aktif pada sistem ICS dapat menyebabkan gangguan proses fisik; selalu diperlukan otorisasi tertulis.

---

### 12. Refleksi Profesional

1. Dalam threat modelling, Anda menemukan bahwa sebuah sistem kontrol pabrik memiliki kerentanan kritis yang jika dieksploitasi dapat menyebabkan kecelakaan industri. Vendor menolak untuk memperbaiki dengan alasan "tidak pernah terjadi sebelumnya" dan perubahan firmware terlalu mahal. Sebagai security professional yang menemukan ini, apa kewajiban etis dan legal Anda?

2. Privacy-vs-Safety tradeoff sering muncul dalam sistem IoT kesehatan: fitness tracker yang mengumpulkan data kardiovaskular dapat mendeteksi serangan jantung lebih awal (safety benefit), tetapi juga mengekspos data kesehatan sensitif (privacy risk). Bagaimana Anda membantu organisasi navigasi tradeoff ini?

3. Coordinated disclosure untuk kerentanan IoT jauh lebih kompleks dari software biasa: kerentanan mungkin mempengaruhi jutaan perangkat dari berbagai vendor, vendor mungkin tidak memiliki tim security, dan patch mungkin sulit didistribusikan. Apakah standar "90 hari disclosure" yang umum di software security masih relevan untuk CPS/IoT? Apa modifikasi yang diperlukan?

---

---

## Bab 4 — Protokol IoT: MQTT, CoAP, HTTP/REST, dan Industrial Protocols

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan arsitektur dan mekanisme protokol IoT utama (MQTT, CoAP, HTTP/REST, Modbus, DNP3) (C2); mengidentifikasi kelemahan keamanan bawaan setiap protokol (C4); menganalisis traffic protokol IoT dari pcap/log untuk menemukan anomali dan kerentanan konfigurasi (C4); mengevaluasi konfigurasi keamanan broker dan gateway IoT (C4). *Sub-CPMK-2 / CPMK-2 / Eval-2*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    PROT[Protokol IoT &\nKeamanannya]

    PROT --> APP_LAYER[Application Layer\nProtocols]
    APP_LAYER --> MQTT2[MQTT:\nPublish-Subscribe\nPort 1883/8883]
    APP_LAYER --> COAP2[CoAP:\nRESTful untuk\nkonstrained device\nPort 5683/5684]
    APP_LAYER --> HTTP_IOT[HTTP/REST:\nCloud API\nWebhook IoT]

    PROT --> INDUST_PROT[Industrial Protocols]
    INDUST_PROT --> MODBUS2[Modbus TCP/RTU:\nLegacy, no auth,\nno encryption]
    INDUST_PROT --> DNP3_P[DNP3:\nSCADA telemetry\nlimited auth]
    INDUST_PROT --> OPCUA2[OPC-UA:\nModern, has security]

    PROT --> VULN_PROT[Kelemahan Protokol]
    VULN_PROT --> NO_ENC[Tanpa enkripsi\nbawaan]
    VULN_PROT --> NO_AUTH[Tanpa autentikasi\nbawaan / opsional]
    VULN_PROT --> REPLAY2[Rentan replay\nattack]
    VULN_PROT --> INJECT[Command injection\nvia protocol]
```

---

### 3. Pengantar Kontekstual

MQTT adalah "lingua franca" IoT — digunakan oleh miliaran perangkat dari smart home hingga pabrik industri. Namun MQTT versi awal dirancang untuk efisiensi, bukan keamanan: tidak ada enkripsi bawaan, tidak ada autentikasi wajib, dan tidak ada authorization granular. Akibatnya, pada 2023 Shodan menemukan lebih dari 50.000 MQTT broker yang terbuka di internet tanpa autentikasi — siapa saja dapat subscribe ke semua topik dan membaca data sensor dari seluruh dunia.

---

### 4. Landasan Teori

#### 4.1 MQTT (Message Queuing Telemetry Transport)

MQTT adalah protokol publish-subscribe ringan yang dirancang untuk koneksi dengan bandwidth rendah dan latency tinggi. Awalnya dikembangkan untuk memantau pipeline minyak via satelit.

**Arsitektur MQTT:**
```
Publisher (Device) → Broker (Server) → Subscriber (Application)
                         ↑
                   Mengelola Topics
                   Menyimpan Last-Value
                   Mengelola Retained Messages
```

**Quality of Service (QoS):**
- QoS 0: At most once — no acknowledgment (fire and forget)
- QoS 1: At least once — acknowledged delivery (possible duplicates)
- QoS 2: Exactly once — guaranteed exactly one delivery

**Topic Hierarchy:**
```
home/bedroom/temperature     → spesifik
home/+/temperature           → wildcard satu level
home/#                       → wildcard semua level (BERBAHAYA jika tanpa auth)
```

**Kelemahan Keamanan MQTT:**

1. **Autentikasi opsional:** Default MQTT broker (Mosquitto) menerima koneksi tanpa username/password
2. **Tidak ada enkripsi bawaan:** MQTT port 1883 plaintext; harus gunakan MQTTS (port 8883) dengan TLS
3. **Wildcard subscription:** `#` subscribe ke semua topik — dalam broker tanpa ACL, siapa pun dapat membaca semua data
4. **Topic injection:** Jika device ID sebagian dari topik dan tidak divalidasi, attacker dapat publish ke topik orang lain
5. **No message integrity:** Pesan tidak ada signature — mudah di-spoof atau di-replay

**Konfigurasi MQTT yang Aman (Mosquitto):**
```
# /etc/mosquitto/mosquitto.conf — SECURE configuration

# Enkripsi TLS wajib
listener 8883
cafile /etc/mosquitto/ca.crt
certfile /etc/mosquitto/server.crt
keyfile /etc/mosquitto/server.key
require_certificate true           # Wajibkan client certificate
tls_version tlsv1.2

# Autentikasi wajib
allow_anonymous false
password_file /etc/mosquitto/passwd

# ACL — authorization
acl_file /etc/mosquitto/acl

# Contoh ACL file:
# user device_kitchen
# topic write home/kitchen/#
# topic read home/kitchen/#
# (device kitchen hanya bisa publish/subscribe ke topiknya sendiri)
```

#### 4.2 CoAP (Constrained Application Protocol)

CoAP adalah protokol RESTful yang dirancang untuk perangkat yang sangat terbatas sumber daya (microcontroller dengan RAM <10KB). Menggunakan UDP (bukan TCP) untuk efisiensi.

**Karakteristik CoAP:**
- RESTful: GET, POST, PUT, DELETE (seperti HTTP)
- UDP-based dengan reliability opsional
- Compact binary header (minimal overhead)
- Port UDP 5683 (plaintext), 5684 (DTLS — encrypted)
- Built-in support untuk multicast

**Kelemahan Keamanan CoAP:**
- UDP amplification attack: CoAP response lebih besar dari request → DDoS amplifier
- Tanpa DTLS: communication dalam plaintext
- Multicast CoAP: sulit diterapkan keamanan
- Resource discovery (/.well-known/core) dapat mengekspos semua endpoint ke attacker

#### 4.3 HTTP/REST dalam IoT

HTTP/HTTPS semakin umum di IoT berkat proliferasi microcontroller yang lebih powerful (ESP32, Raspberry Pi). Keunggulan: ekosistem tooling yang kaya, mudah di-proxy dan dimonitor.

**Kelemahan spesifik IoT:**
- Token/API key dalam URL: `GET /api/data?token=abc123&sensor_id=1` → token terekspos dalam log
- Self-signed certificate yang di-accept tanpa validasi (tidak aman!)
- Long-lived token tanpa expiry atau revocation
- Webhook tanpa signature verification — siapa saja dapat trigger webhook

#### 4.4 Industrial Protocols: Modbus, DNP3, OPC-UA

**Modbus (1979):**
Protokol serial master-slave yang sangat sederhana. Tidak ada autentikasi, tidak ada enkripsi, tidak ada sequence number. Siapa pun yang dapat mengirim frame Modbus ke PLC dapat membaca atau menulis register — termasuk coil yang mengendalikan aktuator.

```
Modbus Read Holding Registers:
01 03 00 00 00 0A C5 CD
^  ^  ^     ^     ^
|  |  Address    CRC
|  Function (Read)
Unit ID

Response: nilai register dikembalikan — siapa pun dapat membaca
```

**Modbus Security Gap:**
- Tidak ada authentication: siapa pun di network dapat kirim command
- Tidak ada encryption: traffic plaintext
- Tidak ada integrity check: frame dapat dimanipulasi (hanya CRC untuk error detection, bukan security)
- Tidak ada authorization: semua register dapat dibaca dan ditulis

**DNP3 (1993):**
Lebih advanced dari Modbus — memiliki Secure Authentication Version 5 (SAv5) dengan HMAC, namun implementasi SAv5 tidak universal. Banyak sistem masih menggunakan DNP3 tanpa authentication.

**OPC-UA (2008):**
Protokol industri modern yang dirancang dengan security: autentikasi X.509 certificate, enkripsi AES, signing pesan, dan audit log. OPC-UA adalah standar yang direkomendasikan untuk deployment baru.

---

### 5. Model atau Arsitektur

```mermaid
sequenceDiagram
    participant DEV as IoT Device
    participant BROKER as MQTT Broker
    participant APP as Application Server
    participant ATTK as Attacker

    Note over DEV,APP: Skenario INSECURE — MQTT tanpa auth/TLS

    DEV->>BROKER: CONNECT (no username/password)
    BROKER-->>DEV: CONNACK (accepted)
    DEV->>BROKER: PUBLISH sensors/temp {value: 25.3}
    BROKER->>APP: PUBLISH sensors/temp {value: 25.3}

    ATTK->>BROKER: CONNECT (anonymous)
    BROKER-->>ATTK: CONNACK (accepted)
    ATTK->>BROKER: SUBSCRIBE # (wildcard — semua topik)
    BROKER->>ATTK: PUBLISH sensors/temp {value: 25.3}
    Note over ATTK: Attacker menerima semua data!

    ATTK->>BROKER: PUBLISH sensors/temp {value: 99.9}
    BROKER->>APP: PUBLISH sensors/temp {value: 99.9}
    Note over APP: App menerima data palsu!
```

---

### 6. Contoh Terapan

**Kasus: Analisis MQTT Traffic dari pcap File**

Dalam lab, mahasiswa diberikan file pcap (packet capture) dari sebuah deployment IoT. Analisis menggunakan Wireshark:

```
Filter Wireshark untuk MQTT: mqtt
Filter untuk melihat semua PUBLISH: mqtt.msgtype == 3

Temuan dalam pcap:
1. MQTT CONNECT tanpa UsernameFlag dan PasswordFlag → anonymous connection
2. Topic: factory/machine01/control — ada PUBLISH dengan payload {"action": "stop"}
3. Topic: factory/credentials/backup — ada pesan berisi username/password dalam plaintext!
4. QoS 0 untuk semua pesan critical control → tidak ada guaranteed delivery
```

**Rekomendasi berdasarkan analisis:**
1. Aktifkan MQTT authentication wajib
2. Enkripsi dengan TLS 1.2+
3. Implementasikan ACL: device machine01 hanya bisa publish ke topiknya sendiri, tidak ke topik control
4. Jangan pernah kirim credential via MQTT — gunakan secure channel terpisah

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Analisis Protokol IoT dari Dataset pcap

**Prasyarat:** Wireshark terinstall, dataset pcap yang disediakan instruktur

**Langkah Kerja:**
1. Buka file pcap yang diberikan di Wireshark
2. Filter traffic MQTT: `mqtt`
3. Identifikasi: (a) apakah ada koneksi anonymous? (b) apakah ada MQTT tanpa TLS (port 1883 bukan 8883)?
4. Cari topik sensitif dalam PUBLISH messages
5. Identifikasi apakah ada pola wildcard subscription
6. Buat laporan singkat: temuan keamanan, severity, dan rekomendasi
7. Bandingkan dengan Modbus traffic dalam pcap yang sama: jelaskan perbedaan model keamanan

**Catatan Etika:** Hanya gunakan dataset pcap yang disanitasi dan disediakan instruktur. Tidak ada capture dari jaringan nyata tanpa otorisasi.

---

### 8. Latihan Pemahaman

**Soal 1 (Analisis — C4)**
Mengapa Modbus tetap digunakan luas di industri meskipun tidak memiliki keamanan bawaan? Apa saja pendekatan kompensasi yang dapat diterapkan untuk mengamankan deployment Modbus yang tidak dapat diganti?

**Soal 2 (Identifikasi — C4)**
Dalam packet capture MQTT, Anda menemukan:
- Koneksi dari IP 192.168.1.50 ke broker dengan CONNECT {ClientID: "monitor", username: null}
- Setelah connect, device ini subscribe ke topik `factory/#`
Apa yang dapat Anda simpulkan tentang konfigurasi keamanan broker ini dan apa risikonya?

**Soal 3 (Evaluasi — C5)**
Bandingkan MQTT dan CoAP dari perspektif keamanan untuk deployment IoT di lingkungan industri. Faktor apa yang akan menentukan pilihan protokol?

**Soal 4 (Aplikasi — C3)**
Tulis konfigurasi ACL Mosquitto untuk skenario ini: 50 sensor (ID sensor01–sensor50) yang hanya boleh publish ke topik `plant/sensor<ID>/data`; monitoring server yang boleh subscribe ke semua topik `plant/#`; control server yang boleh publish ke `plant/+/control`.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Protocol Security Audit pada Pabrik (C4–C5)**

Sebuah pabrik tekstil memiliki sistem IoT produksi:
- 30 sensor mesin menggunakan MQTT (port 1883, no TLS, no auth)
- 5 PLC menggunakan Modbus TCP (port 502, terbuka di jaringan produksi)
- SCADA server menggunakan OPC-UA (dengan sertifikat self-signed yang tidak divalidasi)
- Gateway ke cloud menggunakan HTTP (bukan HTTPS) untuk mengirim telemetry

*Pertanyaan:*
1. Ranking kerentanan protokol dari paling kritis ke paling rendah, berikan justifikasi
2. Untuk setiap kerentanan, identifikasi: apa yang dapat dilakukan attacker? Apa dampak safety/operasional?
3. Buat Secure Connection Checklist (lihat format Lampiran B) untuk memverifikasi perbaikan setelah remediasi

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 1:**
Modbus tetap digunakan karena: (1) Legacy investment — infrastruktur industri bernilai miliaran dollar yang tidak dapat diganti setiap dekade; (2) Simplicity dan reliability — Modbus sangat sederhana dan proven reliable selama 40+ tahun; (3) Lifecycle mismatch — PLC dengan Modbus dibeli 2005 akan beroperasi sampai 2030+.

Pendekatan kompensasi: (a) Network segmentation — isolasi jaringan Modbus dari jaringan IT; (b) Unidirectional Security Gateway (data diode) — data flow hanya satu arah (dari OT ke IT, tidak sebaliknya); (c) Deep Packet Inspection (DPI) — firewall yang memahami Modbus dapat memblokir perintah write yang tidak sah; (d) Application whitelist — hanya sumber IP yang diizinkan bisa mengirim perintah Modbus; (e) Monitoring Modbus traffic untuk deteksi anomali.

**Kunci Studi Kasus:**
Ranking kerentanan: (1) MQTT tanpa TLS dan auth — paling kritis karena banyak device dan data dapat dicuri/diinjeksi; (2) HTTP (bukan HTTPS) ke cloud — credential dan data telemetry terekspos; (3) Modbus TCP terbuka — akses langsung ke PLC; (4) OPC-UA dengan self-signed — certificate spoofing mungkin.

Attack via Modbus: attacker di jaringan produksi dapat kirim Modbus Write Multiple Registers ke PLC → mengubah setpoint mesin → produk cacat atau kerusakan mesin.

---

### 11. Ringkasan Bab

MQTT (publish-subscribe, port 1883/8883) adalah protokol IoT paling umum dengan kelemahan utama: autentikasi opsional, tidak ada enkripsi bawaan, wildcard subscription berpotensi mengekspos semua data. Konfigurasi aman: MQTTS (TLS), autentikasi wajib, ACL per device. CoAP (UDP-based, RESTful) efisien untuk constrained device tetapi memerlukan DTLS untuk keamanan. Modbus dan DNP3 adalah protokol industri lama tanpa keamanan bawaan — mitigasi melalui network segmentation dan DPI. OPC-UA adalah standar industri modern dengan keamanan terintegrasi. Analisis pcap menggunakan Wireshark adalah teknik dasar untuk audit keamanan protokol IoT.

---

### 12. Refleksi Profesional

1. Ribuan sistem ICS menggunakan Modbus yang terekspos ke internet (dapat ditemukan di Shodan). Sebagai security researcher yang menemukan PLC pabrik kimia terbuka di internet, apa yang Anda lakukan? Kepada siapa Anda melaporkan jika Anda tidak tahu siapa pemiliknya?

2. Vendor router IoT sering memberikan firmware update yang berisi perubahan konfigurasi MQTT default (misalnya mengaktifkan autentikasi). Namun banyak perangkat yang sudah terdeploy tidak pernah diupdate karena operator tidak tahu atau tidak mau. Siapa yang bertanggung jawab untuk memastikan perangkat IoT yang sudah deployed mendapat update keamanan?

3. Protokol seperti MQTT sengaja dirancang dengan keamanan opsional untuk memudahkan adopsi. Ini berhasil — MQTT menjadi sangat populer. Tapi keputusan desain ini menciptakan ekosistem yang tidak aman. Apakah pendekatan "security optional, performance first" ini dapat dibenarkan dalam konteks IoT industri? Apa alternatifnya?

---

---

## Bab 5 — TLS/DTLS, Kriptografi Ringan, dan Keamanan Komunikasi IoT

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan mekanisme TLS 1.3 dan DTLS dalam konteks koneksi IoT (C2); mengidentifikasi kelemahan konfigurasi TLS/DTLS pada perangkat dan gateway IoT (C4); memilih cipher suite dan parameter kriptografi yang tepat untuk perangkat constrained (C4); menganalisis sertifikat X.509 dan infrastruktur PKI untuk IoT (C4). *Sub-CPMK-2 / CPMK-2 / Eval-2*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    TLS_IOT[TLS/DTLS dalam\nKonteks IoT]

    TLS_IOT --> TLS2[TLS 1.3\nTransport Layer Security]
    TLS2 --> HS[Handshake:\n1-RTT atau 0-RTT]
    TLS2 --> CERT[Certificate\nX.509 v3]
    TLS2 --> CIPHER[Cipher Suite:\nAES-GCM, ChaCha20]

    TLS_IOT --> DTLS2[DTLS\nDatagram TLS\nuntuk UDP/CoAP]
    DTLS2 --> RELO[Reliable delivery\ndi atas UDP]
    DTLS2 --> FLIGHT[Flight-based\nhandshake]

    TLS_IOT --> LIGHTWEIGHT[Kriptografi Ringan\nLightweight Cryptography]
    LIGHTWEIGHT --> NIST_LWC[NIST LWC:\nASCON (AEAD)]
    LIGHTWEIGHT --> ECC2[ECC P-256:\nlebih efisien dari RSA]
    LIGHTWEIGHT --> CHACHA[ChaCha20-Poly1305:\nconstrained device]

    TLS_IOT --> PKI_IOT[PKI untuk IoT]
    PKI_IOT --> ROOT_CA[Root CA\nInternal / Public]
    PKI_IOT --> DEV_CERT[Device Certificate\nX.509 per device]
    PKI_IOT --> REVOC[Certificate Revocation:\nCRL / OCSP]
    PKI_IOT --> LIFESPAN[Certificate Lifecycle\nRenewal, Rotation]
```

---

### 3. Pengantar Kontekstual

Mengamankan komunikasi IoT menggunakan TLS terdengar sederhana — tetapi kenyataannya sangat kompleks. Perangkat IoT dengan mikrocontroller 8-bit dan 32KB RAM tidak dapat menjalankan TLS handshake dengan RSA-4096 tanpa timeout. Sertifikat yang expire dan tidak diperbarui menyebabkan outage. Self-signed certificate yang di-accept tanpa validasi membuka pintu serangan MitM. Dan infrastruktur PKI untuk jutaan perangkat memerlukan solusi manajemen yang sangat berbeda dari PKI tradisional.

---

### 4. Landasan Teori

#### 4.1 TLS 1.3 — Dasar dan Peningkatan

TLS 1.3 (RFC 8446, 2018) adalah versi terbaru dengan perbaikan signifikan dibanding TLS 1.2:

| Aspek | TLS 1.2 | TLS 1.3 |
|-------|---------|---------|
| Handshake round-trips | 2-RTT | 1-RTT (atau 0-RTT untuk resumed) |
| Cipher suites | Banyak, termasuk yang lemah | Hanya 5 cipher suite yang kuat |
| Perfect Forward Secrecy | Opsional | Wajib (selalu ephemeral key) |
| Key exchange | RSA atau DHE/ECDHE | Hanya (EC)DHE |
| Authentication | RSA atau ECDSA | RSA atau ECDSA (sama) |
| Deprecated | RC4, 3DES, MD5, SHA-1 masih ada | Semua weak algorithm dihapus |

**TLS 1.3 Handshake (simplified):**
```
Client                              Server
  |--- ClientHello ----------------->|
  |    (Supported groups, key share) |
  |                                  |
  |<-- ServerHello ------------------|
  |    (Selected cipher, key share)  |
  |<-- {EncryptedExtensions} --------|
  |<-- {Certificate} ----------------|
  |<-- {CertificateVerify} ----------|
  |<-- {Finished} ------------------|
  |--- {Finished} ----------------->|
  |=== Application Data ============|
```
Perhatikan: hanya 1 round-trip sebelum data dapat dikirim.

#### 4.2 DTLS untuk IoT (CoAP over DTLS)

DTLS (Datagram TLS, RFC 9147) adalah adaptasi TLS untuk UDP. Diperlukan untuk CoAP dan protokol UDP lain.

**Tantangan DTLS:**
- UDP tidak reliable → DTLS menambahkan reliability mechanism (retransmission timer)
- UDP tidak ordered → DTLS menambahkan epoch dan sequence number
- Overhead DTLS lebih tinggi dari pure UDP → tradeoff untuk security

**DTLS Handshake Modes:**
- **Full handshake:** Seperti TLS 1.3, verifikasi certificate kedua sisi
- **Session resumption:** Menggunakan pre-shared session state → lebih cepat untuk reconect

#### 4.3 Konfigurasi TLS untuk Perangkat Constrained

Tidak semua perangkat IoT mampu menjalankan TLS dengan parameter penuh. Panduan:

**Tingkat kemampuan perangkat:**
```
TIER 1 — High-capability (ESP32, Raspberry Pi, Gateway):
  → TLS 1.3 dengan ECDHE-ECDSA-AES128-GCM-SHA256
  → Full PKI dengan X.509 certificate
  → OCSP stapling untuk revocation check

TIER 2 — Mid-range (ESP8266, STM32 with crypto accelerator):
  → TLS 1.2 minimum (TLS 1.3 jika RAM cukup)
  → ECDSA P-256 (lebih efisien dari RSA-2048)
  → ChaCha20-Poly1305 (lebih cepat dari AES di device tanpa hardware AES)
  → Pre-shared key (PSK) mode untuk eliminasi certificate overhead

TIER 3 — Highly constrained (8-bit microcontroller, <32KB RAM):
  → DTLS-PSK atau DTLS-RPK (Raw Public Key)
  → ASCON (NIST LWC standard) untuk AEAD
  → TinyDTLS library
```

#### 4.4 Kesalahan Umum TLS dalam IoT

```python
# BERBAHAYA — mematikan validasi certificate
import ssl
import urllib.request

# Ini membuat semua koneksi rentan MitM!
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE
response = urllib.request.urlopen(url, context=ctx)

# BENAR — validasi certificate dengan CA yang tepat
ctx = ssl.create_default_context(cafile='/etc/iot/ca-bundle.crt')
ctx.check_hostname = True
ctx.verify_mode = ssl.CERT_REQUIRED
# Minimum TLS version
ctx.minimum_version = ssl.TLSVersion.TLSv1_2
response = urllib.request.urlopen(url, context=ctx)
```

**Kesalahan umum lain:**
1. Self-signed cert di-accept tanpa PIN atau CA verification
2. Certificate hostname tidak divalidasi (check_hostname=False)
3. Certificate expired tidak dideteksi (produksi dengan expired cert berjalan years)
4. Private key disimpan dalam flash yang dapat dibaca (secrets exposure)
5. Menggunakan cipher suite yang deprecated (RC4, 3DES)
6. TLS 1.0/1.1 masih diaktifkan

#### 4.5 PKI untuk IoT

PKI (Public Key Infrastructure) untuk IoT memiliki tantangan skala dan lifecycle yang tidak ada dalam PKI enterprise konvensional.

**Komponen PKI IoT:**
- **Root CA:** Certificate Authority paling atas — harus sangat terlindungi (HSM)
- **Intermediate CA:** Menerbitkan device certificate — dapat dikompromis (lebih mudah di-revoke)
- **Device Certificate:** Identitas unik per perangkat, berisi device ID, public key, masa berlaku
- **CRL/OCSP:** Mekanisme revokasi untuk certificate yang dikompromis

**Lifecycle Device Certificate:**
```
Manufacturing → Provisioning → Deployment → Operation → Renewal → Decommission
      ↓               ↓             ↓           ↓          ↓           ↓
  Generate key    Issue cert    Configure    Monitor    Rotate key  Revoke cert
  in secure HSM   dari CA       device       expiry    before exp   + key destroy
```

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph PKI_ARCH[PKI Architecture untuk IoT]
        ROOT_CA2[Root CA\nOffline HSM]
        INT_CA[Intermediate CA\nOnline — Issue certs]
        MFCT_CA[Manufacturing CA\nInject cert at factory]
        CLOUD_CA[Cloud IoT CA\nFor cloud-side certs]
    end

    subgraph DEVICE_SIDE[Device Side]
        DEV_KEY[Device Private Key\nStored in Secure Element]
        DEV_CERT2[Device Certificate\nX.509: Device ID + PubKey]
    end

    subgraph SERVER_SIDE[Server Side]
        SRV_CERT[Server Certificate\nIssued by Intermediate CA]
        OCSP_SRV[OCSP Responder\nReal-time revocation check]
    end

    ROOT_CA2 -->|Signs| INT_CA
    INT_CA -->|Signs| MFCT_CA
    INT_CA -->|Signs| CLOUD_CA
    MFCT_CA -->|Issues at manufacturing| DEV_CERT2
    DEV_KEY -->|Corresponding keypair| DEV_CERT2
    INT_CA -->|Issues| SRV_CERT
    INT_CA --> OCSP_SRV
```

---

### 6. Contoh Terapan

**Kasus: Audit TLS pada Fleet IoT Gateway**

Tim security mengaudit 200 IoT gateway yang menggunakan TLS untuk koneksi ke cloud. Temuan:

```bash
# Perintah audit dengan OpenSSL (pada gateway test yang diotorisasi):
openssl s_client -connect gateway.example.com:8883 -tls1_1

# Temuan:
# 1. TLS 1.1 masih diterima (deprecated, seharusnya minimum TLS 1.2)
# 2. Certificate expire dalam 3 hari (tidak ada alerting)
# 3. Cipher: TLS_RSA_WITH_RC4_128_SHA (RC4 — sudah dilarang RFC 7465)

# Cek certificate detail:
openssl x509 -in device_cert.pem -noout -text | grep -E "Subject:|Not After:|Subject Alternative Name"
# Output:
# Subject: CN=gateway-001, O=Company, C=ID
# Not After: Jun 15 00:00:00 2024 GMT  ← SUDAH EXPIRED
```

Rekomendasi: disable TLS 1.0/1.1, disable RC4, implementasi certificate expiry alerting (30 hari sebelum expire), automated certificate renewal.

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** TLS Configuration Audit dan Certificate Analysis

**Langkah Kerja:**
1. Buat koneksi TLS test ke broker MQTT demo yang aman: `mosquitto_pub -h test.mosquitto.org -p 8883 --cafile ca.crt -t test/hello -m "hi"`
2. Gunakan `openssl s_client` untuk menganalisis TLS handshake dan melihat parameter koneksi
3. Parse certificate: `openssl x509 -in cert.pem -text -noout` — identifikasi: issuer, subject, validity, key length, SANs
4. Gunakan `testssl.sh` (jika tersedia) atau `nmap --script ssl-*` terhadap target yang diotorisasi untuk audit cipher suite
5. Dokumentasikan: cipher suite apa yang ditawarkan? Apakah ada yang deprecated? Apakah TLS 1.3 tersedia?

---

### 8. Latihan Pemahaman

**Soal 1 (Analisis — C4)**
Seorang developer IoT menggunakan kode Python dengan `ctx.verify_mode = ssl.CERT_NONE` karena "self-signed certificate susah dikonfigurasi". Jelaskan risiko konkret dari pendekatan ini dan berikan alternatif yang tepat.

**Soal 2 (Evaluasi — C5)**
Perangkat IoT dengan Cortex-M0 (ARM 32-bit, 32KB RAM, tanpa hardware AES accelerator) harus mengimplementasikan secure communication. TLS 1.3 penuh tidak mungkin karena keterbatasan resource. Rekomendasi apa yang Anda berikan?

**Soal 3 (Analisis — C4)**
Apa yang dimaksud dengan "Perfect Forward Secrecy" (PFS)? Mengapa PFS penting untuk komunikasi IoT jangka panjang, di mana perangkat mungkin beroperasi 10+ tahun?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Certificate Management Failure (C4–C5)**

Sebuah perusahaan energy memiliki 1.000 smart meter yang semuanya menggunakan sertifikat X.509 dengan masa berlaku 1 tahun. Pada tanggal 1 Januari 2024 (Tahun Baru), semua sertifikat expire secara bersamaan — karena semua dikeluarkan pada batch yang sama setahun sebelumnya. Seluruh fleet tidak dapat terhubung ke cloud platform, menyebabkan outage total selama 48 jam sementara tim melakukan emergency recertification satu per satu.

*Pertanyaan:*
1. Identifikasi semua kesalahan dalam desain PKI yang menyebabkan insiden ini
2. Bagaimana seharusnya lifecycle certificate dikelola untuk fleet besar?
3. Rancang prosedur emergency untuk situasi certificate mass expiry yang tidak dapat dihindari

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 3 (PFS):**
Perfect Forward Secrecy berarti bahwa kompromi kunci privat server di masa depan tidak dapat digunakan untuk mendekripsi komunikasi yang sudah berlalu. Dicapai dengan menggunakan kunci sesi ephemeral (ECDHE) yang berbeda untuk setiap koneksi dan tidak pernah disimpan. Penting untuk IoT jangka panjang: perangkat IoT beroperasi 10+ tahun; jika attacker merekam semua traffic dari 2024 dan di 2030 berhasil mencuri kunci privat server, tanpa PFS mereka dapat mendekripsi semua traffic 2024. Dengan PFS, kunci sesi 2024 sudah hilang — tidak ada yang dapat didekripsi.

**Kunci Studi Kasus:**
Kesalahan desain PKI: (1) Single batch issuance dengan expiry tanggal yang sama; (2) Tidak ada certificate expiry monitoring dan alerting; (3) Tidak ada automated renewal process; (4) Tidak ada staggered expiry (seharusnya berbeda-beda per device); (5) Tidak ada emergency response plan untuk mass certificate failure.

Best practice lifecycle: staggered expiry (variasikan tanggal issuance), automated renewal 30–90 hari sebelum expire, monitoring dashboard, certificate rotation per zona/grup (bukan seluruh fleet sekaligus), grace period untuk koneksi dengan cert hampir expired.

---

### 11. Ringkasan Bab

TLS 1.3 adalah standar minimum untuk komunikasi IoT yang aman — menawarkan 1-RTT handshake, PFS wajib, dan penghapusan cipher lemah. DTLS adalah adaptasi untuk UDP (CoAP). Perangkat constrained memerlukan alternatif: ECDSA (lebih efisien dari RSA), ChaCha20 (tanpa hardware AES), PSK mode (eliminasi certificate overhead), dan ASCON (NIST LWC standard). Kesalahan umum: `CERT_NONE` (matikan validasi), self-signed tanpa CA validation, certificate expired tidak terdeteksi. PKI IoT memerlukan perhatian khusus pada lifecycle: staggered expiry, automated renewal, dan emergency response plan.

---

### 12. Refleksi Profesional

1. Banyak vendor perangkat IoT menyediakan SDK dengan konfigurasi TLS yang insecure sebagai default (`CERT_NONE`) karena "kemudahan development". Perangkat yang sudah di-ship ke jutaan konsumen menggunakan konfigurasi ini. Bagaimana ekosistem keamanan IoT seharusnya menangani masalah "insecure by default" yang sudah terlanjur tersebar?

2. Certificate Authority yang dikompromis dapat membahayakan seluruh fleet IoT yang mempercayainya. Untuk infrastruktur kritis (power grid, water treatment), apakah PKI publik cukup atau diperlukan PKI internal yang sepenuhnya dikelola sendiri? Apa trade-off masing-masing pendekatan?

3. Kriptografi "quantum-resistant" (post-quantum cryptography) sudah distandarisasi NIST — CRYSTALS-Kyber untuk key exchange, CRYSTALS-Dilithium untuk signatures. Perangkat IoT yang di-deploy hari ini mungkin masih beroperasi pada era post-quantum computer. Haruskah kriptografi post-quantum diimplementasikan sekarang pada perangkat IoT baru? Apa hambatannya?

---

---

## Bab 6 — Device Identity, Authentication, Authorization, dan Telemetry Security

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan konsep device identity dan mekanisme autentikasi perangkat IoT (C2); mengidentifikasi kelemahan dalam skema autentikasi dan otorisasi IoT (C4); menganalisis keamanan aliran telemetry data dari perangkat ke cloud (C4); merancang model otorisasi berbasis peran dan atribut untuk ekosistem IoT (C4). *Sub-CPMK-2 / CPMK-2 / Eval-2*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    DID[Device Identity &\nAccess Management\nIoT IAM]

    DID --> ID[Device Identity]
    ID --> X509_ID[X.509 Certificate:\nCryptographic identity]
    ID --> DEVID[IEEE 802.1AR:\nInitial Device Identifier]
    ID --> TPM2[TPM 2.0:\nHardware-bound identity]
    ID --> SECRET_ID[Shared Secret /\nPre-provisioned Key]

    DID --> AUTHN[Authentication]
    AUTHN --> CERT_AUTH[Mutual TLS:\nClient cert auth]
    AUTHN --> PSK_AUTH[Pre-Shared Key\nLightweight auth]
    AUTHN --> TOKEN_AUTH[JWT / OAuth 2.0\nfor cloud API]
    AUTHN --> OTP_AUTH[One-time password\nfor setup/onboarding]

    DID --> AUTHZ[Authorization]
    AUTHZ --> RBAC2[RBAC:\nRole-Based\nAccess Control]
    AUTHZ --> ABAC[ABAC:\nAttribute-Based\nAccess Control]
    AUTHZ --> ACL2[ACL per resource\nper device]

    DID --> TELEM[Telemetry Security]
    TELEM --> INTEG[Data Integrity:\nSigning payload]
    TELEM --> TIMESTAMP[Timestamp &\nNonce: anti-replay]
    TELEM --> CONFID[Confidentiality:\nPayload encryption]
```

---

### 3. Pengantar Kontekstual

"Is that really the sensor talking, or is it an attacker pretending to be the sensor?" Inilah pertanyaan fundamental device identity. Dalam ekosistem IoT dengan ribuan perangkat, memastikan bahwa setiap perangkat adalah perangkat yang sah — bukan attacker yang berpura-pura — adalah tantangan yang jauh lebih kompleks dari autentikasi user konvensional.

---

### 4. Landasan Teori

#### 4.1 Device Identity

Device identity adalah mekanisme yang membuktikan bahwa sebuah perangkat adalah dirinya sendiri dan bukan entitas lain. Berbeda dari user identity, device identity harus: embedded saat manufaktur, terikat secara kriptografis ke hardware jika memungkinkan, dapat diverifikasi dari jarak jauh, dan dapat direvoke jika perangkat dikompromis.

**Tingkatan Device Identity:**

| Tingkat | Mekanisme | Kekuatan | Kapan Digunakan |
|---------|-----------|----------|-----------------|
| Level 1 | MAC Address | Sangat lemah — mudah di-spoof | Hanya untuk inventory awal |
| Level 2 | Pre-Shared Secret | Lemah jika shared, OK jika unique per device | Low-cost device, no PKI |
| Level 3 | Software X.509 Cert | Baik — dapat di-revoke | Gateway, mid-range IoT |
| Level 4 | Hardware-bound cert (TPM/SE) | Kuat — private key tidak dapat diekstrak | Kritis, industrial, medical |

**IEEE 802.1AR — Initial Device Identifier (IDevID):**
Standard industri untuk device identity yang diinjeksikan saat manufaktur dalam secure facility. IDevID digunakan untuk bootstrapping — membuktikan identitas perangkat sebelum mendapat credential operasional.

#### 4.2 Secure Device Onboarding

Onboarding adalah proses memberikan credential operasional kepada perangkat baru. Ini adalah fase paling kritis — jika onboarding dikompromis, seluruh keamanan lifecycle ikut dikompromis.

**NIST SP 800-63 / Zero Touch Provisioning:**
```
Manufacturing:
  Device mendapat IDevID (Initial Device Identifier) dari CA manufaktur
  IDevID diburn ke Secure Element/TPM

First Boot / Onboarding:
  1. Device boot → menggunakan IDevID untuk autentikasi ke onboarding server
  2. Onboarding server verifikasi IDevID (validasi cert chain ke Manufacturing CA)
  3. Onboarding server menerbitkan LDevID (Local Device Identifier)
     + credential operasional (MQTT cert, cloud credentials)
  4. Device menyimpan LDevID dan credential di secure storage
  5. Device siap beroperasi dengan identity operasional

Operasi Normal:
  Device menggunakan LDevID untuk autentikasi ke semua layanan
```

#### 4.3 Authentication untuk IoT

**Mutual TLS (mTLS) — Device Authentication:**
```
Client (Device)              Server (Gateway/Cloud)
  |-- ClientHello --------->|
  |<- ServerHello + Cert ---|  (Server membuktikan identitasnya)
  |-- Client Cert --------->|  (Client JUGA kirim certificate)
  |-- CertVerify ---------->|  (Bukti device punya private key)
  |<- Finished -------------|
  |<-- Application Data ----|
```
mTLS memastikan kedua sisi terautentikasi — server tahu siapa device-nya, device tahu siapa server-nya.

**JWT untuk IoT API:**
```json
{
  "header": {
    "alg": "ES256",
    "typ": "JWT"
  },
  "payload": {
    "device_id": "sensor-001",
    "iat": 1720000000,
    "exp": 1720003600,     ← expire 1 jam
    "scope": "telemetry:write",
    "jti": "unique-token-id"  ← prevent replay
  },
  "signature": "ECDSA_signature_dengan_device_private_key"
}
```

#### 4.4 Authorization dalam IoT

IoT memerlukan authorization granular: bukan hanya "apakah perangkat ini terautentikasi?" tetapi "apakah perangkat ini boleh melakukan aksi ini pada resource ini?"

**RBAC untuk IoT:**
```
Roles:
  - sensor_device: read_own_data, write_telemetry_own
  - gateway_device: read_all_sensors, relay_data, manage_local_network
  - cloud_platform: read_all, write_commands
  - operator: read_all, write_setpoints, view_alarms
  - admin: full_access
```

**ABAC untuk IoT (lebih granular):**
```
Policy: Aksi read_sensor_data diperbolehkan JIKA:
  AND:
    device.location == "zone_A" OR requestor.role == "admin"
    device.status == "active"
    time.hour BETWEEN 6 AND 22  (hanya jam operasional)
    request.method == "GET"
```

#### 4.5 Telemetry Security

Data telemetry (sensor readings, events, logs) harus terlindungi dalam transit dan saat diterima.

**Ancaman pada Telemetry:**
1. **Spoofing:** Data sensor palsu dari device yang berpura-pura jadi sensor sah
2. **Tampering:** Nilai sensor dimodifikasi dalam transit
3. **Replay:** Paket lama di-replay untuk menipu sistem
4. **Injection:** Perintah berbahaya disuntikkan sebagai "telemetry"

**Mitigasi:**
```json
// Telemetry message dengan proteksi lengkap
{
  "device_id": "sensor-001",
  "timestamp_utc": "2026-07-15T10:30:00Z",
  "sequence": 12345,
  "nonce": "random-32-bytes-base64",
  "readings": {
    "temperature": 25.3,
    "humidity": 65.2
  },
  "signature": "ECDSA(device_private_key, SHA256(payload))"
}
```

---

### 5. Model atau Arsitektur

```mermaid
sequenceDiagram
    participant MFG as Manufacturing\n(Secure Facility)
    participant DEV2 as Device
    participant ONBOARD as Onboarding Server
    participant CLOUD as Cloud Platform

    MFG->>DEV2: Inject IDevID Certificate\n(dalam secure manufacturing env)
    DEV2->>ONBOARD: CONNECT + IDevID cert (mTLS)
    ONBOARD->>ONBOARD: Verify IDevID cert chain\n→ Manufacturing CA
    ONBOARD-->>DEV2: Issue LDevID + Operational Credentials\n(MQTT cert, API token)
    DEV2->>DEV2: Store credentials in Secure Element
    DEV2->>CLOUD: CONNECT + LDevID cert (mTLS)
    CLOUD->>CLOUD: Verify cert → Intermediate CA
    CLOUD-->>DEV2: CONNACK — authenticated
    DEV2->>CLOUD: PUBLISH telemetry {signed payload}
    CLOUD->>CLOUD: Verify signature → device public key
    CLOUD-->>DEV2: Acknowledge (if QoS 1/2)
```

---

### 6. Contoh Terapan

**Kasus: Authorization Failure pada Platform Smart Building**

Platform smart building menggunakan OAuth 2.0 untuk akses API. Audit menemukan:
- Token memiliki scope `building:all` — terlalu broad
- Token tidak expire (no `exp` claim)
- Token sama digunakan oleh semua device di gedung — jika satu device dikompromis, semua akses terekspos
- Tidak ada per-resource authorization — token `building:all` dapat mengakses CCTV, HVAC, dan access control sekaligus

**Perbaikan desain:**
- Token per device dengan scope minimal (`sensor_003:telemetry:write` bukan `building:all`)
- Token expire 1–24 jam, wajib refresh
- RBAC atau ABAC untuk authorization per resource per device
- Audit log setiap akses API

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Device Authentication Lab dengan MQTT Client Certificate

**Langkah Kerja:**
1. Setup Mosquitto broker lokal dengan konfigurasi: TLS aktif, anonymous=false, require_certificate=true
2. Gunakan openssl untuk generate: CA cert, server cert, dan dua client cert (device-001, device-002)
3. Konfigurasi ACL: device-001 hanya bisa publish ke `sensors/device001/#`; device-002 ke `sensors/device002/#`
4. Test: device-001 mencoba subscribe ke `sensors/device002/#` → harus ditolak
5. Verifikasi bahwa koneksi tanpa certificate ditolak
6. Dokumentasikan: langkah setup, konfigurasi, dan hasil pengujian

---

### 8. Latihan Pemahaman

**Soal 1 (Analisis — C4)**
Mengapa MAC address tidak dapat dijadikan satu-satunya identifier untuk autentikasi perangkat IoT? Jelaskan minimal dua serangan yang memanfaatkan kelemahan MAC address sebagai identifier.

**Soal 2 (Evaluasi — C5)**
Sebuah sistem smart meter menggunakan shared symmetric key yang sama untuk seluruh fleet 100.000 meter. Apa implikasi keamanan jika satu meter berhasil di-reverse engineer dan kunci tersebut berhasil diekstrak?

**Soal 3 (Analisis — C4)**
Sebuah telemetry message dari sensor tidak memiliki timestamp dan nonce. Jelaskan bagaimana attacker dapat melakukan replay attack dan apa dampaknya pada sistem kontrol.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Insiden Device Identity dalam Fleet Kendaraan Terhubung (C4–C5)**

Sebuah perusahaan fleet management memiliki 5.000 kendaraan dengan IoT module untuk tracking lokasi. Semua kendaraan menggunakan credentials yang sama (username/password hardcoded dalam firmware). Seorang peneliti menemukan firmware di GitHub (diupload tidak sengaja oleh developer), mengekstrak credentials, dan berhasil inject data lokasi palsu untuk seluruh fleet selama beberapa jam sebelum terdeteksi.

*Pertanyaan:*
1. Identifikasi semua kesalahan dalam desain identity dan authentication sistem ini
2. Rancang model identity dan authentication yang tepat untuk fleet 5.000+ kendaraan
3. Jika insiden ini terjadi pada Anda: apa langkah incident response dalam 24 jam pertama?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 2:**
Shared symmetric key untuk seluruh fleet adalah "catastrophic failure mode": ekstraksi satu kunci = kompromi seluruh fleet. Tanpa kunci yang unik per device, tidak ada isolasi — satu breach menjadi breach massal. Mitigasi yang benar: unique key per device (meskipun lebih kompleks untuk dikelola), atau gunakan asymmetric PKI di mana setiap device memiliki keypair sendiri dan private key tidak perlu dibagikan ke siapa pun.

**Kunci Studi Kasus:**
Kesalahan: (1) Shared credentials untuk seluruh fleet; (2) Hardcoded credentials dalam firmware; (3) Firmware yang berisi credentials diupload ke public repository; (4) Tidak ada per-device authentication; (5) Tidak ada anomaly detection (5.000 kendaraan di lokasi aneh tidak terdeteksi selama jam).

Rancangan yang benar: setiap kendaraan memiliki X.509 certificate unik yang diinjeksikan saat manufaktur (atau activated saat pertama kali diaktivasi); mTLS untuk koneksi ke server; tidak ada credential dalam firmware; monitoring: baseline behavioral profiling per kendaraan → alert jika lokasi update dari area yang tidak mungkin dijangkau.

---

### 11. Ringkasan Bab

Device identity adalah fondasi keamanan IoT — memastikan bahwa komunikasi berasal dari perangkat yang sah, bukan attacker. Tingkatan identity dari lemah (MAC address) ke kuat (hardware-bound certificate via TPM/SE). Secure onboarding menggunakan IDevID (manufacturing identity) untuk mendapat LDevID (operational identity). Mutual TLS (mTLS) adalah standar untuk device authentication. Authorization harus granular: per device, per resource, least privilege. Telemetry security memerlukan: signature (integritas), timestamp+nonce (anti-replay), dan enkripsi (konfidensialitas). Shared credential untuk seluruh fleet adalah anti-pattern berbahaya.

---

### 12. Refleksi Profesional

1. Device provisioning pada skala jutaan perangkat IoT adalah tantangan logistik dan keamanan yang sangat besar. Proses injeksi credential di pabrik memerlukan secure manufacturing environment yang sangat ketat. Bagaimana perusahaan besar mengelola trust chain dari manufaktur ke deployment, terutama jika outsourcing manufacturing ke negara lain?

2. Device identity memerlukan private key yang tersimpan aman di perangkat. Untuk perangkat low-cost (<$5), menambahkan secure element yang menyimpan key secara aman mungkin menambah cost 50–100%. Apakah ini dapat dibenarkan? Faktor apa yang menentukan kapan hardware security diperlukan?

3. Ketika sebuah device IoT dikompromis dan perlu di-revoke identitasnya, device tersebut mungkin masih terhubung secara fisik ke sistem kritis (sensor di reaktor, infusion pump di rumah sakit). Proses revokasi memerlukan device menerima signal revokasi — tapi jika device sudah dikompromis, ia mungkin mengabaikan signal tersebut. Bagaimana Anda merancang sistem yang dapat secara andal me-revoke identitas device yang telah dikompromis?

---

---

## Bab 7 — Firmware Security: Struktur, Triage, dan Analisis Statis

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan struktur firmware embedded system dan komponen utamanya (C2); melakukan triage dan analisis statis firmware menggunakan toolset legal pada artefak yang sah (C4); mengidentifikasi kelemahan umum dalam firmware yang dapat dianalisis secara statis tanpa eksekusi (C4); merancang prosedur analisis firmware yang aman, legal, dan terdokumentasi (C5). *Sub-CPMK-3 / CPMK-3 / Eval-3*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    FW[Firmware Security Analysis]

    FW --> STRUCT[Firmware Structure]
    STRUCT --> HEADER[Magic bytes / Header]
    STRUCT --> BOOT[Bootloader section]
    STRUCT --> KERN[Kernel / OS section]
    STRUCT --> FS[Filesystem / RootFS]
    STRUCT --> CFG_FW[Config & Data sections]

    FW --> TRIAGE[Firmware Triage]
    TRIAGE --> IDENTIFY[Identify format:\nbinwalk -t]
    TRIAGE --> ENTROPY[Entropy analysis:\ncompressed/encrypted detection]
    TRIAGE --> EXTRACT[Extract filesystem:\nbinwalk -e / unblob]
    TRIAGE --> STRINGS2[String extraction:\nstrings, grep]

    FW --> STATIC[Static Analysis]
    STATIC --> HARDCODED[Hardcoded credentials\nand secrets]
    STATIC --> VULN_FUNC[Vulnerable functions:\nstrcpy, sprintf, gets]
    STATIC --> CRYPTO_FW[Crypto weakness:\nhard-coded keys, MD5]
    STATIC --> CONFIG_BIN[Configuration analysis:\ndefault creds, services]

    FW --> LEGAL[Legal & Ethical Constraints]
    LEGAL --> AUTHORIZED[Only on authorized\nlab devices / samples]
    LEGAL --> SANITIZE[Sanitize artifacts:\nno real credentials]
    LEGAL --> DOCMENT[Document chain\nof custody]
```

---

### 3. Pengantar Kontekstual

Firmware adalah "jiwa" dari perangkat IoT — kode yang menentukan semua perilaku perangkat. Ketika firmware mengandung kelemahan keamanan, seluruh perangkat terekspos, dan patch yang dikirim over-the-air (OTA) mungkin membutuhkan waktu berbulan-bulan atau bahkan tidak pernah tiba (terutama untuk device yang sudah tidak didukung). Analisis firmware memungkinkan tim keamanan untuk mengidentifikasi kelemahan *sebelum* deployment atau *setelah* insiden untuk forensik.

---

### 4. Landasan Teori

#### 4.1 Struktur Firmware

Firmware embedded system umumnya terdiri dari beberapa komponen:

**Raw Firmware Layout:**
```
[Magic/Header]   → Identifikasi format (e.g., TRX header untuk router)
[Bootloader]     → U-Boot atau proprietary — init hardware, load kernel
[Kernel]         → Linux kernel (zImage/uImage) atau RTOS
[Filesystem]     → SquashFS, JFFS2, CRAMFS, atau proprietary FS
[Config Area]    → Default configuration, certificates
[Data Partition] → User data, logs
```

**Common Filesystem Types dalam IoT Firmware:**

| Filesystem | Karakteristik | Umum Pada |
|-----------|---------------|-----------|
| SquashFS | Read-only, compressed | Router, IP camera |
| JFFS2 | Journaling Flash FS, R/W | Embedded Linux |
| CRAMFS | Compressed ROM FS | Low-memory devices |
| YAFFS2 | NAND flash optimized | Older Android, cameras |
| UBI/UBIFS | Volume management untuk NAND | Modern Linux IoT |

#### 4.2 Firmware Acquisition (pada Lab Berotorisasi)

**Metode akuisisi (semua hanya pada perangkat berotorisasi):**

1. **OTA/Update server:** Download update file resmi dari vendor — halal, tidak memerlukan akses fisik
2. **Vendor portal:** Beberapa vendor menyediakan firmware untuk download langsung
3. **Physical flash extraction:** Membaca chip flash langsung (CH341A programmer, flashrom) — hanya pada perangkat yang dimiliki sendiri atau perangkat institusi dengan otorisasi
4. **Debug interface (UART/JTAG):** Dump via serial console — hanya dengan otorisasi dan pada perangkat yang sah
5. **Network traffic capture:** Intercept OTA update dalam traffic (MITM pada lab terisolasi)

> **CATATAN ETIKA:** Semua akuisisi firmware harus dilakukan pada perangkat yang dimiliki sendiri, perangkat institusi/lab, atau perangkat yang telah mendapat persetujuan tertulis dari pemilik. Akuisisi firmware dari perangkat pihak ketiga tanpa otorisasi adalah pelanggaran hukum.

#### 4.3 Triage Firmware

**Langkah triage sistematis:**

```bash
# 1. Identifikasi file type
file firmware.bin
binwalk firmware.bin

# 2. Entropy analysis — deteksi compressed/encrypted sections
binwalk -E firmware.bin
# High entropy (~8.0) → compressed atau encrypted
# Low entropy (<6.0) → plaintext data

# 3. String extraction awal
strings firmware.bin | grep -i -E "(password|passwd|secret|key|admin|root)"
strings firmware.bin | grep -E "[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}"  # IP addresses

# 4. Extract filesystem
binwalk -e firmware.bin
# atau: unblob firmware.bin  (tool modern, lebih akurat)
```

**Interpretasi entropy:**
```
Entropy → 0.0–3.0: Sparse data (padded zeros, simple patterns)
Entropy → 4.0–6.5: Plaintext data (code, config, strings)
Entropy → 7.5–8.0: Compressed (gzip, LZMA) atau encrypted data
```

#### 4.4 Analisis Kelemahan Umum dalam Firmware

**Kategori kelemahan yang dapat diidentifikasi secara statis:**

**1. Hardcoded Credentials:**
```bash
# Cek /etc/passwd atau /etc/shadow dalam extracted filesystem
cat extracted/_firmware.bin.extracted/squashfs-root/etc/passwd
cat extracted/_firmware.bin.extracted/squashfs-root/etc/shadow

# Cek konfigurasi web server
find . -name "*.conf" | xargs grep -i "password\|passwd"
```

**2. Private Keys dan Certificates:**
```bash
find . -name "*.pem" -o -name "*.key" -o -name "*.crt" 2>/dev/null
grep -r "BEGIN PRIVATE KEY\|BEGIN RSA PRIVATE KEY" .
grep -r "BEGIN CERTIFICATE" . | head -20
```

**3. Unsafe C Functions (dalam binary analysis):**
```
Buffer overflow prone: strcpy, strcat, sprintf, gets, scanf
Format string: printf(user_input) tanpa format specifier
Integer overflow: tanpa bounds checking
```

**4. Hardcoded IP/URL:**
```bash
grep -r -E "[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}" extracted/ \
    | grep -v "127.0.0.1\|0.0.0.0\|255.255"
strings firmware.bin | grep -E "https?://"
```

**5. Debug/Test Code Artifacts:**
```bash
grep -r -i "debug\|test\|backdoor\|diagnostic\|maintenance" extracted/ \
    | grep -v "\.pyc\|Binary"
find extracted/ -name "*.sh" | xargs grep -l "password\|secret"
```

#### 4.5 Tools Analisis Firmware

| Tool | Fungsi | Legal/Safe Use |
|------|--------|----------------|
| binwalk | Identify + extract firmware components | Ya, analisis statis |
| unblob | Modern firmware extraction | Ya, analisis statis |
| strings | Extract printable strings | Ya |
| file | Identify file type | Ya |
| hexdump/xxd | Raw hex inspection | Ya |
| Ghidra | Reverse engineering / disassembly | Ya, statis |
| radare2 | Disassembly dan analisis | Ya, statis |
| FACT | Firmware Analysis and Comparison Tool | Ya, framework |
| firmwalker | Script pencarian kelemahan umum | Ya, statis |

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    ACQUIRE[Firmware Acquisition\nOTA / Vendor / Physical\nHanya pada perangkat berotorisasi]
    TRIAGE2[Firmware Triage\nbinwalk -t\nEntropy analysis\nStrings extraction]
    EXTRACT2[Filesystem Extraction\nbinwalk -e\nunblob]
    STATIC2[Static Analysis]

    ACQUIRE --> TRIAGE2
    TRIAGE2 --> EXTRACT2
    EXTRACT2 --> STATIC2

    STATIC2 --> CRED_CHK[Credential Check\netc/passwd, shadow\nconfig files]
    STATIC2 --> KEY_CHK[Key/Cert Check\n*.pem, *.key, *.crt\nHardcoded keys]
    STATIC2 --> SRVS_CHK[Services Check\nopen ports in config\nenabled services]
    STATIC2 --> BIN_CHK[Binary Analysis\nGhidra / radare2\nunsafe functions]
    STATIC2 --> SCRIPT_CHK[Script Analysis\nstart scripts\ncron jobs]

    CRED_CHK --> FINDING[Findings Document]
    KEY_CHK --> FINDING
    SRVS_CHK --> FINDING
    BIN_CHK --> FINDING
    SCRIPT_CHK --> FINDING

    FINDING --> SEVERITY[Risk Scoring\nCVSS estimate]
    SEVERITY --> REPORT[Security Report\nto Vendor / Team]
```

---

### 6. Contoh Terapan

**Kasus: Analisis Firmware IP Camera**

Tim keamanan menerima sample firmware dari kamera IP yang sering digunakan dalam CCTV gedung perkantoran. Analisis dilakukan pada lab berotorisasi dengan firmware yang diunduh dari portal resmi vendor.

**Proses:**
```bash
# 1. Triage
binwalk firmware_camera_v2.1.bin
# → Found: TRX firmware header, SquashFS filesystem at offset 0x40000

# 2. Extract
binwalk -e firmware_camera_v2.1.bin

# 3. Cek credentials
cat _firmware_camera_v2.1.bin.extracted/squashfs-root/etc/passwd
# → root:$1$xxxxx:0:0:root:/root:/bin/sh
# → admin:$1$yyyyy:1000:1000::/home/admin:/bin/sh

# 4. Cek private keys
find . -name "*.key" -o -name "*.pem"
# → ./squashfs-root/etc/ssl/server.key  ← TEMUAN KRITIS

# 5. Verifikasi jika private key ini unik per device atau shared
cat squashfs-root/etc/ssl/server.key | head -5
```

**Temuan:**
- Private key SSL disertakan langsung dalam firmware (bukan generated saat pertama boot)
- Semua kamera dengan firmware yang sama menggunakan private key yang identik
- Jika satu kamera dikompromis, seluruh fleet terekspos (shared key)

**Rekomendasi:**
- Key generation saat first boot (setiap device memiliki keypair unik)
- Atau provisioning key melalui secure onboarding
- Atau gunakan CA infrastructure dengan device-unique certificates

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Analisis Statis Firmware pada Sample yang Disediakan Dosen

**Lingkungan:** VM Linux (Ubuntu 22.04) dengan binwalk, strings, file, dan tools analysis; firmware sample yang disediakan oleh dosen (dataset legal, bukan firmware perangkat production yang nyata)

**Langkah Kerja:**
1. Install tools: `sudo apt install binwalk strings file xxd`
2. Terima firmware sample dari dosen (file telah disanitasi dari data sensitif nyata)
3. Lakukan triage: `binwalk sample_firmware.bin` — catat komponen yang ditemukan
4. Lakukan entropy analysis: `binwalk -E sample_firmware.bin` — interpretasikan hasilnya
5. Extract: `binwalk -e sample_firmware.bin`
6. Dari extracted filesystem, cari: credentials, private keys, hardcoded IPs, debug services
7. Dokumentasikan setiap temuan dengan: lokasi file, jenis temuan, risiko, rekomendasi
8. Buat laporan ringkas menggunakan template Lampiran C

**Kriteria Keberhasilan:** Laporan berisi minimal 3 kategori temuan berbeda dengan evidence, risk level, dan rekomendasi per temuan.

---

### 8. Latihan Pemahaman

**Soal 1 (Pemahaman — C2)**
Jelaskan perbedaan antara SquashFS dan JFFS2 sebagai filesystem dalam firmware IoT. Mengapa SquashFS lebih sering digunakan pada router?

**Soal 2 (Analisis — C4)**
Entropy analysis menunjukkan nilai ~7.9 pada offset 0x100000–0x200000 dalam sebuah firmware. Apa interpretasi yang paling mungkin, dan apa implikasinya untuk proses ekstraksi dan analisis?

**Soal 3 (Evaluasi — C5)**
Sebuah vendor mengklaim firmware mereka "aman karena dienkripsi." Enkripsi firmware adalah mitigasi yang baik terhadap analisis statis, namun tidak mengubah fakta bahwa kelemahan dalam kode tetap ada. Jelaskan mengapa "security through obscurity" melalui enkripsi firmware tidak cukup sebagai satu-satunya mekanisme keamanan.

**Soal 4 (Analisis — C4)**
Sebuah perangkat IoT menggunakan shared SSL/TLS private key yang sama untuk seluruh fleet 500.000 unit (key disertakan dalam firmware). Jelaskan attack scenario bagaimana attacker dapat memanfaatkan ini untuk melakukan MITM terhadap semua perangkat dalam fleet.

**Soal 5 (Evaluasi — C5)**
Dalam analisis firmware sebuah industrial gateway, Anda menemukan binary yang memanggil `system()` dengan parameter yang berasal dari parsing MQTT message. Mengapa ini merupakan temuan kritis, dan bagaimana mitigasinya?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Firmware Triage pada Smart Meter (C4–C5)**

Sebuah utilitas listrik berencana deploy 200.000 smart meter dari vendor baru. Tim keamanan mendapat kesempatan untuk menganalisis firmware update package (v3.2.1) sebelum approval deployment. Firmware diunduh dari portal vendor yang memerlukan akun resmi.

Dari triage awal: binwalk mengidentifikasi Linux kernel (3.14), SquashFS filesystem, dan satu blok dengan entropy ~7.8. String extraction menghasilkan: beberapa URL internal, satu string "debug_mode=1", dan referensi ke `/etc/meter_key.pem`.

*Pertanyaan:*
1. Susun rencana analisis statis lengkap untuk firmware ini, termasuk tool yang digunakan dan artifact yang dicari
2. Apa arti dari entropy ~7.8 dan bagaimana pendekatan Anda untuk bagian tersebut?
3. Temukan "debug_mode=1" dan referensi ke `meter_key.pem` — bagaimana Anda menilai risiko masing-masing dan apa rekomendasi Anda kepada vendor?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 3 (Enkripsi Firmware):**
Enkripsi firmware mempersulit analisis statis, tetapi memiliki beberapa kelemahan fatal sebagai sole security measure: (1) Decryption key harus ada di perangkat — jika perangkat dikompromis secara fisik, key dapat diekstrak dan firmware didekripsi; (2) Kelemahan dalam kode (buffer overflow, hardcoded credentials) tetap ada setelah dekripsi — enkripsi hanya menyembunyikan, bukan memperbaiki; (3) "Security through obscurity" adalah prinsip yang ditolak dalam keamanan modern (Kerckhoffs's principle); (4) Attacker yang berhasil mendapat satu perangkat fisik dapat mendekripsi firmware dan mengekstrak seluruh struktur dan kelemahan. Mitigasi yang benar adalah: perbaiki kelemahan dalam kode + gunakan enkripsi firmware sebagai defence-in-depth, bukan sebagai sole protection.

**Kunci Studi Kasus:**
Rencana analisis: (1) strings extraction untuk cari credentials dan hardcoded data; (2) extract filesystem dengan binwalk -e; (3) cek /etc/passwd, /etc/shadow; (4) cek file meter_key.pem — apakah unique per device atau shared?; (5) analisis start scripts untuk debug_mode; (6) analisis network services yang diaktifkan; (7) cek update mechanism. Entropy ~7.8 → compressed atau encrypted, coba binwalk -e dan lihat apakah berhasil diextract (compressed) atau gagal (encrypted). debug_mode=1 dalam production firmware adalah risiko tinggi — kemungkinan membuka port debug atau mengurangi security checks; rekomendasi: wajib disabled di production build. meter_key.pem: cek apakah key ini di-generated per device atau shared — jika shared, risiko sangat tinggi; rekomendasi: device-unique key generation.

---

### 11. Ringkasan Bab

Firmware adalah komponen paling kritis namun sering paling terabaikan dalam keamanan IoT. Analisis firmware dimulai dari triage (identifikasi format, entropy analysis, string extraction), diikuti ekstraksi filesystem, kemudian analisis statis untuk mencari credentials, private keys, debug artifacts, dan unsafe code patterns. Tools utama: binwalk, strings, Ghidra untuk binary analysis. Kelemahan paling umum: hardcoded credentials, shared private keys, debug mode tidak di-disabled, dan penggunaan unsafe C functions. Semua analisis harus dilakukan secara legal (firmware resmi/diotorisasi), dengan dokumentasi chain of custody, dan artifact harus disanitasi sebelum diserahkan sebagai laporan. Enkripsi firmware bukan substitusi untuk secure coding — ia hanya memperlambat analisis, tidak menghilangkan kelemahan.

---

### 12. Refleksi Profesional

1. Analisis firmware sering menemukan credential dan private key yang "tersembunyi" dalam firmware. Sebagai security analyst, Anda memiliki kewajiban untuk melaporkan temuan ini ke vendor. Bagaimana Anda mengelola responsible disclosure — ke siapa, dalam format apa, dengan tenggat waktu berapa — terutama jika kelemahan tersebut sudah di-exploit di alam liar?

2. Reverse engineering firmware tanpa otorisasi tertulis melanggar hukum di berbagai yurisdiksi (Computer Fraud and Abuse Act di AS, Pasal 30 UU ITE di Indonesia). Namun, peneliti keamanan yang menemukan kelemahan kritis dalam firmware perangkat medis mungkin menghadapi dilema: melaporkan memerlukan analisis yang secara teknis merupakan reverse engineering. Bagaimana komunitas keamanan seharusnya menyeimbangkan kebutuhan keamanan publik dengan batasan hukum?

3. Sebuah perangkat IoT yang sudah end-of-life (tidak lagi dapat menerima patch) ditemukan memiliki kelemahan kritis dalam firmware. Perangkat ini masih dioperasikan oleh ribuan pengguna. Apa tanggung jawab vendor, operator, regulator, dan komunitas keamanan dalam situasi ini?

---

---

## Bab 8 — Configuration Analysis dan Secrets Exposure Review

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: mengidentifikasi kelemahan konfigurasi dalam perangkat IoT dan komponen CPS (C4); melakukan review sistematis terhadap konfigurasi layanan, network, dan autentikasi (C4); mendeteksi secrets exposure (API key, password, token) dalam konfigurasi dan kode (C4); merancang baseline konfigurasi aman untuk deployment IoT (C5). *Sub-CPMK-3 / CPMK-3 / Eval-3*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    CONF[Configuration Security\nReview]

    CONF --> SCOPE[Scope of Review]
    SCOPE --> NET_CONF[Network Configuration:\nports, firewall, protocols]
    SCOPE --> AUTH_CONF[Authentication Config:\ncredentials, session, MFA]
    SCOPE --> CRYPTO_CONF[Crypto Config:\nTLS version, ciphers, cert]
    SCOPE --> SVC_CONF[Service Config:\nenabled services, defaults]
    SCOPE --> OS_CONF[OS Hardening:\npermissions, users, cron]

    CONF --> SECRETS[Secrets Exposure]
    SECRETS --> HARDCODED_S[Hardcoded in code/config]
    SECRETS --> ENV_S[Environment variables\nnot properly scoped]
    SECRETS --> LOG_S[Secrets in logs]
    SECRETS --> REPO_S[Committed to repository]
    SECRETS --> TRANS_S[Secrets in transit\nunencrypted]

    CONF --> TOOL_CONF[Analysis Tools]
    TOOL_CONF --> GREP_CONF[grep / semgrep\nfor pattern matching]
    TOOL_CONF --> GITLEAKS2[gitleaks / trufflehog\nfor repo scanning]
    TOOL_CONF --> LYNIS[lynis / CIS-CAT\nOS hardening check]
    TOOL_CONF --> NMAP2[nmap\nopen port verification]

    CONF --> BASELINE[Secure Baseline]
    BASELINE --> CIS_IOT[CIS Benchmarks for IoT]
    BASELINE --> NIST_GUIDE[NISTIR 8259A\nDevice Cybersecurity]
    BASELINE --> ENISA_GUIDE[ENISA Baseline Security]
```

---

### 3. Pengantar Kontekstual

"Misconfiguration adalah penyebab breach terbesar pada cloud, dan hal yang sama berlaku untuk IoT." Studi berulang dari vendor keamanan (Armis, Forescout, Claroty) konsisten menunjukkan bahwa sebagian besar insiden IoT bukan disebabkan oleh zero-day vulnerability, melainkan oleh: default password yang tidak diubah, port yang tidak perlu dibuka, TLS yang tidak dikonfigurasi, dan secrets yang tersimpan dalam plaintext. Configuration review adalah metode paling cost-effective untuk meningkatkan postur keamanan secara dramatis.

---

### 4. Landasan Teori

#### 4.1 Default Configuration Problem

Perangkat IoT sering dikirim dengan konfigurasi default yang dioptimalkan untuk kemudahan setup, bukan keamanan:

**Anti-patterns yang sangat umum:**
```
Username: admin   Password: admin
Username: admin   Password: 1234
Username: root    Password: (kosong)
Telnet aktif pada port 23
Web interface pada port 80 (tanpa HTTPS)
SSH aktif dengan password authentication enabled
SNMP community string: "public"
```

**NISTIR 8259A — Device Cybersecurity Core Baseline:**
NIST mendefinisikan elemen baseline minimum untuk perangkat IoT:
1. Device Identification
2. Device Configuration (ability to configure, document changes)
3. Data Protection (encryption, integrity)
4. Logical Access to Interfaces (authentication, least privilege)
5. Software Update (secure update mechanism)
6. Cybersecurity State Awareness (logging, monitoring)

#### 4.2 Network Configuration Analysis

**Port Exposure Assessment:**
```bash
# Pada lab/simulasi — verifikasi open ports pada device lab
nmap -sV -p- 192.168.100.50  # Full port scan
nmap -sU -p 161,162 192.168.100.50  # UDP — SNMP check

# Interpretasi umum:
# Port 23 (Telnet): kritis — unencrypted, harus disabled
# Port 22 (SSH): perlu cek apakah password auth enabled atau key-only
# Port 80 (HTTP): web admin tanpa HTTPS — harus redirect ke 443
# Port 161 (SNMP v1/v2): lemah — gunakan SNMPv3 atau disable
# Port 8080, 8443: alternate web ports — perlu review
```

**Firewall dan ACL Validation:**
```
Prinsip: default deny, explicit allow
Inbound: hanya izinkan port yang diperlukan, dari source yang diotorisasi
Outbound: batasi — device seharusnya hanya berkomunikasi ke layanan yang dikenal
```

#### 4.3 Authentication Configuration Review

**Checklist autentikasi:**
```
□ Default credentials telah diubah
□ Password policy: minimum length 12+, complexity, no dictionary words
□ Brute-force protection: rate limiting, account lockout
□ SSH: PasswordAuthentication no (key-only)
□ MFA aktif untuk admin interface
□ Session timeout: idle timeout 15–30 menit
□ Session tokens: HttpOnly, Secure, SameSite
□ API keys: expire, tidak hardcoded, per-client
```

#### 4.4 TLS/Cryptographic Configuration Review

```bash
# Test TLS config (terhadap lab device)
testssl.sh --fast https://192.168.100.50

# Yang dicari:
# - TLS version minimum: TLSv1.2 (idealnya TLSv1.3 only)
# - Weak ciphers: RC4, DES, 3DES, NULL → harus disabled
# - Cert validity: tidak expired, chain lengkap
# - HSTS: Strict-Transport-Security header ada
# - SWEET32, POODLE, BEAST, ROBOT vulnerabilities
```

**Cipher suite baseline untuk IoT (IETF RFC 8446 / NIST SP 800-52r2):**
```
# Diperbolehkan (TLS 1.3):
TLS_AES_128_GCM_SHA256
TLS_AES_256_GCM_SHA384
TLS_CHACHA20_POLY1305_SHA256

# Dilarang (harus disabled):
TLS_RSA_WITH_RC4_128_SHA        ← RC4 broken
TLS_RSA_WITH_DES_CBC_SHA        ← DES broken
SSL_CK_DES_192_EDE3_CBC_WITH_MD5 ← 3DES + MD5
*_EXPORT_* ciphers              ← export-grade, broken
*_NULL_* ciphers                ← no encryption
```

#### 4.5 Secrets Detection

**Kategori secrets yang perlu dideteksi:**

| Kategori | Pattern | Risiko |
|----------|---------|--------|
| API Key | `AIza[0-9A-Za-z-_]{35}` (Google) | Account takeover |
| AWS Secret Key | `AKIA[0-9A-Z]{16}` | Cloud resource access |
| Private Key | `-----BEGIN RSA PRIVATE KEY-----` | Impersonation |
| Password in config | `password\s*=\s*\S+` | Auth bypass |
| JWT secret | Hardcoded JWT signing key | Token forgery |
| DB connection string | `postgres://user:pass@host` | DB access |

**Tools Deteksi:**
```bash
# Gitleaks — untuk repository scanning
gitleaks detect --source=./firmware_extracted/

# truffleHog — entropy-based + regex detection
trufflehog filesystem ./firmware_extracted/

# semgrep — custom rules untuk secrets
semgrep --config=p/secrets ./

# Manual grep (cepat, untuk spot check)
grep -r -E "(password|passwd|secret|api_key|token)\s*[=:]\s*['\"]?\S+" \
    firmware_extracted/ --include="*.conf" --include="*.sh" --include="*.env"
```

#### 4.6 OS dan Service Hardening

**Prinsip minimal footprint:**
```
Aktifkan hanya layanan yang diperlukan → attack surface minimal
Remove atau disable:
  - Telnet (ganti SSH)
  - FTP (ganti SFTP/SCP)
  - TFTP
  - Finger, rsh, rlogin, rexec
  - Unnecessary cron jobs
  - Test/debug endpoints
  - Development tools (compiler, interpreter) yang tidak diperlukan di production
```

**File permission review:**
```bash
# World-writable files → ancaman privilege escalation
find / -type f -perm -o+w 2>/dev/null | grep -v /proc

# SUID/SGID binaries → potential privilege escalation
find / -type f \( -perm -4000 -o -perm -2000 \) 2>/dev/null

# Crontab — pastikan tidak ada script yang dapat dimodifikasi oleh non-root
cat /etc/crontab
crontab -l
```

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    START_CONF[Configuration Review\nInitiation]
    START_CONF --> SCOPE_DEF[Define Scope:\nDevice / System / Network]
    SCOPE_DEF --> COLLECT[Collect Configuration Artifacts\nConfig files, network maps,\nfirmware extracts, scan results]
    COLLECT --> PARALLEL_REVIEW[Parallel Review Streams]

    PARALLEL_REVIEW --> NET_REVIEW[Network Review\nnmap scan, firewall rules,\nopen port analysis]
    PARALLEL_REVIEW --> AUTH_REVIEW[Auth Review\npassword policy,\ndefault creds check]
    PARALLEL_REVIEW --> CRYPTO_REVIEW[Crypto Review\ntestssl.sh, cipher check,\ncert validity]
    PARALLEL_REVIEW --> SECRET_REVIEW[Secrets Review\ngitleaks, trufflehog,\nmanual grep]
    PARALLEL_REVIEW --> OS_REVIEW[OS Hardening Review\nlynis, permission check,\nservice audit]

    NET_REVIEW --> FINDINGS2[Consolidated Findings]
    AUTH_REVIEW --> FINDINGS2
    CRYPTO_REVIEW --> FINDINGS2
    SECRET_REVIEW --> FINDINGS2
    OS_REVIEW --> FINDINGS2

    FINDINGS2 --> SCORE[Risk Scoring per Finding\nCritical / High / Medium / Low]
    SCORE --> REPORT2[Configuration Security Report]
    REPORT2 --> REMEDIATION[Remediation Plan\nwith priority queue]
    REMEDIATION --> VERIFY[Verification after fix\nre-test & re-scan]
```

---

### 6. Contoh Terapan

**Kasus: Configuration Audit pada Industrial IoT Gateway**

Gateway industri menghubungkan sensor shop floor ke cloud SCADA. Audit konfigurasi menemukan:

| Temuan | Severity | Detail |
|--------|----------|--------|
| Telnet aktif (port 23) | Kritis | Semua credential dalam plaintext |
| Default admin:admin | Kritis | Credential tidak diubah sejak install |
| SSH password auth enabled | Tinggi | Brute-force possible |
| TLS 1.0 enabled | Tinggi | Rentan POODLE, BEAST |
| SNMP v1 community "public" | Tinggi | Read/write SNMP tanpa auth |
| `/etc/config/db.conf` berisi DB password | Tinggi | Secrets exposure |
| Logging ke /tmp tanpa rotation | Medium | Log loss jika disk penuh |
| Tidak ada idle timeout | Medium | Session hijacking risk |

**Remediation priority:**
1. Segera: disable Telnet, ubah default credentials, disable SNMP v1
2. Dalam 24 jam: disable SSH password auth (key-only), fix TLS minimum 1.2
3. Dalam 1 minggu: rotate DB password, implementasikan session timeout, pindahkan log ke persistent storage

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Configuration Audit pada Lab IoT Device

**Lingkungan:** VM dengan Mosquitto MQTT broker, simple web admin interface (DVWA atau lab yang disediakan dosen), dan network scanner di jaringan lab terisolasi

**Langkah Kerja:**
1. Lakukan network scan dengan nmap pada subnet lab: identifikasi open ports
2. Review konfigurasi Mosquitto: cek apakah anonymous=true, TLS, ACL
3. Review konfigurasi SSH jika ada: PasswordAuthentication, PermitRootLogin
4. Jalankan gitleaks atau grep pada direktori konfigurasi yang disediakan untuk mencari secrets
5. Review permission file konfigurasi: apakah world-readable?
6. Buat daftar temuan dengan severity dan rekomendasi menggunakan template Lampiran B

---

### 8. Latihan Pemahaman

**Soal 1 (Pemahaman — C2)**
Jelaskan mengapa "security through obscurity" (mengubah port SSH dari 22 ke 2222) tidak dianggap sebagai kontrol keamanan yang efektif, meskipun dapat mengurangi volume scan otomatis.

**Soal 2 (Analisis — C4)**
Sebuah konfigurasi Mosquitto memiliki `allow_anonymous true` dan tidak ada ACL. Jelaskan semua potensi ancaman yang dihasilkan oleh konfigurasi ini dalam konteks sistem smart building.

**Soal 3 (Evaluasi — C5)**
Environment variable `DB_PASSWORD=P@ssw0rd123` disimpan dalam file `.env` yang di-commit ke repository GitHub. Jelaskan: (a) mengapa ini masalah meskipun repository bersifat private, dan (b) apa langkah mitigasi yang benar.

**Soal 4 (Analisis — C4)**
Audit menemukan bahwa sebuah gateway IoT menggunakan TLS 1.0 dengan cipher suite `TLS_RSA_WITH_3DES_EDE_CBC_SHA`. Jelaskan kelemahan spesifik dari kombinasi ini dan rekomendasi perbaikannya.

**Soal 5 (Aplikasi — C3)**
Tulis regex pattern (untuk digunakan dengan grep) yang dapat mendeteksi: (a) hardcoded password dalam file konfigurasi format `key = value`, (b) private key PEM dalam file apapun.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Configuration Review pada Fleet Smart Meter (C4–C5)**

Sebuah perusahaan utilitas akan deploy 10.000 smart meter. Sebelum deployment, tim keamanan melakukan configuration audit pada 5 unit sample. Temuan: (1) semua meter memiliki password admin yang sama, (2) web management interface tersedia via HTTP (bukan HTTPS), (3) SNMP v2c aktif dengan community string "meter2024", (4) NTP server dikonfigurasi ke IP publik tanpa otentikasi, (5) firmware update mechanism menggunakan HTTP tanpa signature verification.

*Pertanyaan:*
1. Lakukan risk scoring pada setiap temuan (Critical/High/Medium/Low) dengan justifikasi berbasis dampak dan kemungkinan eksploitasi
2. Rancang baseline konfigurasi aman untuk fleet ini, mencakup semua aspek yang ditemukan bermasalah
3. Bagaimana Anda merancang proses verifikasi konfigurasi yang dapat dijalankan secara otomatis pada 10.000 perangkat?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 3 (Git Secrets):**
(a) Repository private tidak berarti aman: (1) access token atau akun developer dapat dikompromis; (2) developer mungkin fork ke repository publik; (3) GitHub dapat mengalami breach; (4) git history tidak bisa di-delete — bahkan jika file dihapus, credential tetap ada dalam commit history dan dapat diambil dengan `git log -p`; (5) akses employee yang resign atau dikontrak tidak langsung dicabut.
(b) Mitigasi benar: (1) segera rotate credential yang terekspos; (2) hapus dari git history menggunakan `git filter-branch` atau BFG Repo-Cleaner; (3) gunakan secret management (HashiCorp Vault, AWS Secrets Manager, environment injection dari CI/CD); (4) tambahkan pre-commit hook (gitleaks) untuk mencegah commit credential; (5) file `.env` harus masuk `.gitignore`.

**Kunci Studi Kasus:**
Risk scoring: (1) same password → Kritis (compromise satu = compromise semua); (2) HTTP web UI → Tinggi (credential sniffing); (3) SNMP v2c community string → Tinggi (read/write SNMP = full config access); (4) NTP tanpa auth → Medium (time manipulation → certificate validation bypass, replay attack); (5) HTTP update tanpa signature → Kritis (supply chain attack, malicious firmware injection).
Baseline: unique password per device (provisioned during deployment), HTTPS only, SNMP v3 atau disabled, NTP dengan authentication (NTPsec dengan MAC), firmware update HTTPS + signature verification (vendor public key hardcoded dalam device).
Otomatisasi verifikasi: configuration compliance script yang dijalankan saat provisioning dan secara periodik; hasil dikomparasi terhadap golden baseline config; alert jika ada deviasi.

---

### 11. Ringkasan Bab

Configuration security adalah fondasi keamanan operasional IoT. Sebagian besar insiden IoT bukan disebabkan zero-day, melainkan misconfiguration yang dapat diperbaiki tanpa code changes. Area utama review: network (port terbuka, firewall), authentication (default creds, password policy), cryptography (TLS version, cipher suite), secrets exposure (hardcoded credential, git commit), dan OS hardening (minimal services, proper permissions). Tools utama: nmap, testssl.sh, gitleaks/trufflehog, lynis. Baseline keamanan mengacu pada NISTIR 8259A, CIS Benchmarks, dan ENISA Baseline. Remediation harus diprioritaskan berdasarkan risk score, dan verifikasi ulang dilakukan setelah setiap perbaikan.

---

### 12. Refleksi Profesional

1. Configuration management dalam fleet IoT berskala besar adalah masalah operasional yang kompleks: bagaimana memastikan bahwa konfigurasi aman tetap konsisten setelah update, penambahan perangkat baru, atau perubahan infrastruktur? Alat Infrastructure-as-Code (Ansible, Puppet, Chef) yang umum di server tidak selalu tersedia di embedded IoT. Apa pendekatan yang realistis?

2. Audit konfigurasi dapat menemukan bahwa sistem yang sudah berjalan selama bertahun-tahun memiliki kelemahan serius. Mengubah konfigurasi perangkat yang sedang beroperasi dalam infrastruktur kritis (pembangkit listrik, rumah sakit) memiliki risiko downtime. Bagaimana Anda menyeimbangkan urgensi perbaikan keamanan dengan risiko operasional perubahan konfigurasi?

3. SNMP v1/v2c masih banyak digunakan di industri karena kompatibilitas dengan peralatan lama. SNMPv3 menawarkan autentikasi dan enkripsi tetapi memerlukan migrasi. Dalam konteks infrastruktur kritis dengan peralatan berusia 10–20 tahun, bagaimana Anda merekomendasikan transisi ke SNMPv3 secara bertahap tanpa mengorbankan availability?

---

---

## Bab 9 — Hardware Security: Secure Boot, Key Storage, dan Debug Interface

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan mekanisme Secure Boot dan chain-of-trust dalam sistem embedded (C2); mengidentifikasi risiko pada debug interface (JTAG, UART, USB) dan storage media (C4); membandingkan opsi penyimpanan kriptografis (TPM, Secure Element, TrustZone) beserta trade-off masing-masing (C4); merancang kontrol keamanan hardware yang proporsional dengan risiko aplikasi (C5). *Sub-CPMK-3 / CPMK-3 / Eval-3*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    HW[Hardware Security]

    HW --> SECBOOT[Secure Boot]
    SECBOOT --> ROM_BOOT[ROM Bootloader\nimmutable root of trust]
    SECBOOT --> SIG_VERIFY[Signature Verification\nper boot stage]
    SECBOOT --> CHAIN[Chain of Trust:\nROM → BL1 → BL2 → OS → App]

    HW --> KEY_STORE[Key Storage]
    KEY_STORE --> TPM3[TPM 2.0\nDedicated security chip]
    KEY_STORE --> SE[Secure Element\nTamper-resistant enclave]
    KEY_STORE --> TEE[TrustZone / TEE\nSoftware isolation]
    KEY_STORE --> SW_STORE[Software keystore\nWeakest — avoid for critical]

    HW --> DEBUG_IF[Debug Interfaces]
    DEBUG_IF --> JTAG2[JTAG\nFull processor access]
    DEBUG_IF --> UART2[UART/Serial Console\nShell access]
    DEBUG_IF --> USB3[USB\nStorage, DFU, debugging]
    DEBUG_IF --> SWD[SWD\nARM debug port]

    HW --> COUNTERMEASURES[Countermeasures]
    COUNTERMEASURES --> DISABLE_DEBUG[Disable debug in production]
    COUNTERMEASURES --> FUSE[Blow efuses\nto lock debug]
    COUNTERMEASURES --> TAMPER[Tamper detection\nmesh, voltage, temp]
    COUNTERMEASURES --> EPOXY[Physical potting/epoxy\nboard protection]
```

---

### 3. Pengantar Kontekstual

Hardware security adalah lapisan paling dalam dalam pertahanan IoT. Jika seorang attacker mendapat akses fisik ke sebuah perangkat, semua keamanan software dapat di-bypass tanpa hardware security yang memadai. Debug interface yang tidak di-disable dapat memberikan akses shell penuh. Key yang tidak tersimpan dalam hardware security module dapat diekstrak dari memori. Boot sequence yang tidak dilindungi memungkinkan modifikasi firmware tanpa deteksi.

---

### 4. Landasan Teori

#### 4.1 Secure Boot

Secure Boot adalah mekanisme yang memastikan bahwa perangkat hanya menjalankan firmware yang telah diotorisasi oleh vendor atau pemilik. Tanpa Secure Boot, attacker yang berhasil memodifikasi flash storage dapat mengganti seluruh firmware tanpa perangkat mendeteksinya.

**Chain of Trust:**
```
[ROM Bootloader]           ← Immutable, dalam silicon, trusted by design
      |
      | verify signature
      v
[Bootloader Stage 1 (BL1)] ← Signed oleh manufacturer key
      |
      | verify signature
      v
[Bootloader Stage 2 (BL2)] ← Signed oleh manufacturer key
      |
      | verify signature
      v
[Operating System Kernel]  ← Signed oleh OS vendor key
      |
      | verify signature (optional)
      v
[User Applications]        ← Optional signing
```

Jika salah satu stage gagal verifikasi → boot dihentikan atau fallback ke recovery mode.

**Teknologi Implementasi:**
- **ARM TrustZone + ARM Trusted Firmware:** Untuk SoC berbasis ARM
- **UEFI Secure Boot:** Untuk x86/x64 industrial PC
- **HAB (High Assurance Boot) — NXP i.MX:** SoC populer dalam IoT industrial
- **AVB (Android Verified Boot):** Perangkat Android IoT

#### 4.2 Root of Trust Hardware

| Komponen | Fungsi | Keunggulan | Keterbatasan |
|----------|--------|------------|--------------|
| TPM 2.0 | Crypto operations, PCR measurement, sealed storage | Standar industri, cross-platform | Cost, hanya tersedia di platform tertentu |
| Secure Element (SE) | Tamper-resistant, smart card-grade | Sangat aman, fisik tamper-evident | Cost lebih tinggi, interface terbatas |
| ARM TrustZone | TEE (Trusted Execution Environment) | Tidak perlu chip tambahan | Software-based isolation, side-channel risk |
| SRAM PUF | Unclonable device fingerprint | Unik per device, tidak perlu provisioning | Teknologi relatif baru |

**TPM 2.0 — Key Operations:**
```
Key Generation: TPM generate keypair, private key TIDAK pernah keluar dari TPM
Sealing: Encrypt data dengan kondisi bahwa TPM state tertentu (PCR values)
Attestation: Buktikan bahwa system boot dalam kondisi tertentu (measured boot)
Signing: Sign data dengan key yang tersimpan dalam TPM
```

#### 4.3 Debug Interface Risks

**JTAG (Joint Test Action Group):**
JTAG adalah boundary-scan interface yang memberikan akses mendalam ke prosesor, memori, dan peripheral. Dalam production:
- Tanpa proteksi: attacker dengan physical access dapat dump entire flash/RAM, attach debugger, dan full control
- Proteksi: disable JTAG via efuse blow (irreversible), atau JTAG authentication (via password atau certificate)

**UART/Serial Console:**
```
Banyak perangkat IoT memiliki UART test points pada PCB.
Akses UART sering memberikan: boot log lengkap, U-Boot prompt,
shell access jika authentication tidak dikonfigurasi.

Contoh U-Boot prompt yang berbahaya:
  Hit any key to stop autoboot: 2
  > setenv bootargs "single"   ← boot ke single-user mode
  > boot                       ← full root access tanpa password
```

**Proteksi UART:**
- Remove atau depopulate UART test points pada production board
- Disable U-Boot console atau set U-Boot password
- Disable shell access via serial pada production firmware

**USB:**
- DFU (Device Firmware Update) mode dapat digunakan untuk reflash firmware
- USB mass storage mode dapat mengekspos filesystem
- Proteksi: disable DFU pada production, atau require signature untuk update via USB

#### 4.4 Flash Memory dan Storage Security

**Unencrypted Flash Storage:**
Jika flash chip dapat diakses secara fisik (desoldering atau in-circuit via SPI/I2C/eMMC interface), attacker dapat dump seluruh isi tanpa proteksi software.

**Full Disk Encryption untuk IoT:**
- Storage encryption (dm-crypt/LUKS pada Linux, atau custom block cipher)
- Key harus tersimpan dalam TPM atau SE, bukan dalam flash yang sama
- Sealed key (TPM PCR binding): key hanya tersedia jika boot state dalam kondisi yang diharapkan (belum dimodifikasi)

---

### 5. Model atau Arsitektur

```mermaid
sequenceDiagram
    participant ROM as ROM Bootloader\n(Silicon, Immutable)
    participant TPM4 as TPM 2.0
    participant BL as Bootloader (BL1/BL2)
    participant OS as OS Kernel
    participant APP as Application

    ROM->>TPM4: Request public key for verification
    TPM4-->>ROM: Vendor public key
    ROM->>BL: Verify BL signature
    BL-->>ROM: Signature valid ✓
    ROM->>TPM4: Extend PCR[0] with BL measurement
    BL->>BL: Verify kernel signature
    BL-->>BL: Signature valid ✓
    BL->>TPM4: Extend PCR[1] with kernel measurement
    BL->>OS: Boot kernel
    OS->>TPM4: Request sealed storage key
    TPM4->>TPM4: Check PCR[0], PCR[1] match expected\n(verified boot state)
    TPM4-->>OS: Release sealed storage key ✓
    OS->>APP: Provide decrypted storage access
    Note over TPM4: Jika PCR values mismatch\n(boot modified), key TIDAK dirilis
```

---

### 6. Contoh Terapan

**Kasus: Hardware Assessment pada Industrial Controller**

Tim keamanan melakukan hardware assessment pada PLC klon yang digunakan dalam sistem conveyor pabrik. Prosedur dilakukan pada unit spare (bukan unit yang sedang berproduksi) dalam lab yang berotorisasi.

**Temuan hardware:**
```
1. JTAG header 10-pin depopulated pada production unit — BAIK
   Tetapi: masih ada via/pad yang dapat disolder kembali — RISIKO MEDIUM

2. UART test points (4 pin: VCC, TX, RX, GND) tersedia di PCB
   → Baudrate: 115200 8N1
   → U-Boot console aktif dengan countdown 3 detik
   → Tanpa password U-Boot
   Risiko: KRITIS — akses ke bootloader dan shell

3. Flash chip (SPI NOR 8MB) langsung accessible
   → Tidak ada TSOP-48 socket untuk quick removal
   → Tetapi in-circuit SPI dumping via test points memungkinkan

4. Tidak ada TPM atau Secure Element teridentifikasi
   → Key material disimpan dalam flash yang tidak terenkripsi
```

**Rekomendasi bertahap (untuk vendor):**
- Immediate: Tambahkan U-Boot password atau disable U-Boot console
- Short-term: Enable flash encryption menggunakan key yang di-sealed ke boot state
- Long-term: Tambahkan SE chip pada PCB revision berikutnya untuk proper key storage

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Analisis Hardware Security pada Perangkat Lab (Dataset + Simulasi)

**Lingkungan:** Dataset foto PCB perangkat IoT yang disediakan dosen (telah disanitasi), dokumentasi datasheet chipset terkait, dan simulator QEMU untuk Secure Boot chain

**Langkah Kerja:**
1. Identifikasi komponen pada foto PCB: SoC, flash chip, test points JTAG/UART, Secure Element (jika ada)
2. Cari datasheet SoC yang digunakan: apakah mendukung Secure Boot? Apakah mendukung eFuse lock untuk debug?
3. Buat penilaian risiko: komponen mana yang dapat diakses secara fisik dan apa implikasinya?
4. Rancang rekomendasi hardware security: apa yang harus ditambah/dimodifikasi untuk meningkatkan keamanan?
5. Simulasi Secure Boot (opsional): jalankan QEMU dengan verifikasi signature sederhana dan dokumentasikan hasilnya

---

### 8. Latihan Pemahaman

**Soal 1 (Pemahaman — C2)**
Jelaskan konsep "chain of trust" dalam Secure Boot. Mengapa setiap stage harus memverifikasi stage berikutnya, dan bukan hanya tahap pertama yang memverifikasi semua?

**Soal 2 (Analisis — C4)**
Sebuah perangkat memiliki Secure Boot yang diimplementasikan dengan baik, tetapi flash storage tidak dienkripsi. Seorang attacker dengan akses fisik menggunakan in-circuit SPI reader untuk dump flash. Apa yang dapat dan tidak dapat dilakukan attacker dengan dump tersebut?

**Soal 3 (Evaluasi — C5)**
ARM TrustZone menyediakan Trusted Execution Environment (TEE) tanpa memerlukan chip hardware tambahan. Dibandingkan dengan Secure Element fisik, apa kelebihan dan keterbatasan TrustZone untuk penyimpanan kunci kriptografis?

**Soal 4 (Analisis — C4)**
Sebuah router IoT memiliki UART console yang menampilkan seluruh boot log termasuk pesan kernel, lalu memberikan login prompt. Attacker tidak dapat login karena tidak tahu password. Apakah UART console ini masih merupakan risiko keamanan? Jelaskan informasi apa yang dapat diperoleh attacker dari boot log saja.

**Soal 5 (Aplikasi — C3)**
Jelaskan perbedaan antara "disable debug interface via software" versus "blow efuse untuk lock debug interface secara permanen." Dalam konteks apa masing-masing pendekatan lebih tepat?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Hardware Security Review pada Medical IoT Device (C4–C5)**

Sebuah perangkat patient monitoring yang terhubung ke jaringan rumah sakit sedang menjalani security review sebelum deployment. Spesifikasi: SoC ARM Cortex-A53, Linux 5.4, TPM 2.0 terpasang, flash 16GB eMMC. Dokumen menunjukkan bahwa Secure Boot dikonfigurasi, tetapi developer mengakui bahwa JTAG masih aktif "untuk maintenance."

*Pertanyaan:*
1. Evaluasi trade-off mempertahankan JTAG aktif "untuk maintenance" pada perangkat medical yang terhubung ke jaringan rumah sakit — apa risiko spesifiknya dan dalam kondisi apa JTAG maintenance mungkin dibenarkan?
2. Dengan kehadiran TPM 2.0, rancang skema: (a) key storage untuk data pasien, (b) verifikasi boot integrity, dan (c) remote attestation agar rumah sakit dapat memverifikasi integritas perangkat sebelum mengizinkan akses ke jaringan
3. Apa implikasi hukum dan etika jika perangkat medical ini mengalami breach akibat JTAG yang dibiarkan aktif?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 2 (Secure Boot + Unencrypted Flash):**
Yang DAPAT dilakukan attacker: (1) baca seluruh filesystem — konfigurasi, data, credentials tersimpan di plaintext; (2) ekstrak binary untuk analisis offline; (3) modifikasi isi filesystem dan tulis kembali ke flash — tetapi bootloader akan MENOLAK boot (Secure Boot). Yang TIDAK DAPAT dilakukan: menjalankan firmware yang dimodifikasi (Secure Boot akan gagal). Namun: attacker tetap dapat membaca semua data yang tidak terenkripsi — ini masih merupakan data breach. Kesimpulan: Secure Boot melindungi integritas eksekusi tetapi tidak melindungi confidentiality data. Storage encryption diperlukan untuk proteksi penuh.

**Kunci Studi Kasus Medical IoT:**
JTAG untuk maintenance adalah risiko tidak proporsional untuk perangkat medical: physical access saat maintenance memang diperlukan, tetapi JTAG memberikan akses jauh lebih luas dari yang diperlukan untuk diagnosis rutin. Alternatif: (1) JTAG dilindungi dengan authentication hardware (password-protected); (2) log diagnostic dari TPM PCR values tanpa akses JTAG penuh; (3) sediakan debug port terbatas yang hanya mengekspose diagnostic read-only. TPM scheme: patient data key = sealed dengan PCR[0-3] (boot chain); remote attestation = TPM quote dikirim ke hospital NAC sebelum network join; hospital verifikasi PCR values terhadap known-good baseline. Implikasi hukum: regulasi medical device (FDA 21 CFR, EU MDR) mensyaratkan cybersecurity sebagai bagian dari device design; breach akibat JTAG yang dibiarkan aktif → potensi liability; jika data pasien bocor → pelanggaran HIPAA (di AS) atau UU PDP (di Indonesia).

---

### 11. Ringkasan Bab

Hardware security adalah lapisan pertahanan terdalam dalam IoT — melindungi semua layer di atasnya. Secure Boot memastikan chain-of-trust dari ROM hingga aplikasi, mencegah modifikasi firmware tidak sah. Key storage dalam TPM/SE/TrustZone jauh lebih aman daripada software-only — private key tidak dapat diekstrak dari hardware yang proper. Debug interface (JTAG, UART, USB) merupakan attack surface fisik yang signifikan dan harus di-disable atau dilindungi pada production device. Flash encryption dengan TPM-sealed key memastikan data tidak dapat dibaca meski flash chip diangkat secara fisik. Hardware security decisions memiliki lifecycle implications — retrofit sulit atau impossible setelah production.

---

### 12. Refleksi Profesional

1. Secure Boot memerlukan key management yang ketat: vendor private key harus dijaga dengan sangat aman. Jika vendor private key bocor, seluruh fleet perangkat yang menggunakan key tersebut dapat diflash dengan firmware berbahaya. Bagaimana vendor IoT seharusnya mengelola signing key untuk fleet jutaan perangkat, termasuk key rotation jika key dikompromis?

2. Hardware security features (TPM, Secure Element) menambah cost Bill of Materials. Dalam segmen perangkat IoT konsumer yang price-sensitive (<$10–$20), hardware security sering menjadi korban pertama pengurangan cost. Siapa yang seharusnya menanggung cost ini: vendor, konsumen, atau regulator melalui standar wajib?

3. Ketika sebuah perangkat IoT dengan Secure Boot mengalami malfungsi firmware dan perlu di-reflash di lapangan oleh teknisi, prosedur recovery harus tersedia tetapi tidak boleh disalahgunakan. Rancang sebuah kebijakan yang menyeimbangkan: kemampuan recovery yang legitimate untuk teknisi terlatih, versus pencegahan penyalahgunaan recovery mode oleh attacker yang menyamar sebagai teknisi.

---

---

## Bab 10 — Risk Assessment dan Risk Register CPS/IoT

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menerapkan metodologi risk assessment yang relevan untuk sistem CPS/IoT (C3); mengembangkan risk register komprehensif yang mencakup aset, ancaman, kelemahan, dan kontrol (C4); menghitung dan memprioritaskan risiko menggunakan kualitatif maupun semi-kuantitatif scoring (C4); merumuskan rekomendasi mitigasi berbasis risk-based prioritization (C5). *Sub-CPMK-4 / CPMK-4 / Eval-4*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    RA[Risk Assessment\nCPS/IoT]

    RA --> FRAME[Risk Framing\nScope, context, assumptions]
    FRAME --> ASSET_ID2[Asset Inventory\nHW, SW, data, process]
    ASSET_ID2 --> THREAT_ID[Threat Identification\nThreat actors, STRIDE]
    THREAT_ID --> VULN_ID[Vulnerability Identification\nHW, FW, Config, Protocol]
    VULN_ID --> RISK_CALC[Risk Calculation\nLikelihood × Impact]
    RISK_CALC --> RISK_REG[Risk Register\nDocumentation]
    RISK_REG --> RISK_TREAT[Risk Treatment\nMitigate, Accept, Transfer, Avoid]
    RISK_TREAT --> MONITOR_R[Monitoring & Review\nPeriodic reassessment]

    RA --> METHODS[Methodologies]
    METHODS --> NIST_RMF[NIST RMF\nSP 800-30 / SP 800-82]
    METHODS --> IEC62443[IEC 62443\nISA/IEC for Industrial]
    METHODS --> ISO27005[ISO/IEC 27005\nGeneral IT risk]
    METHODS --> OCTAVE[OCTAVE\nOrganizational focus]
```

---

### 3. Pengantar Kontekstual

Risk Assessment adalah jantung dari program keamanan berbasis bukti. Tanpa risk assessment yang sistematis, organisasi tidak dapat memprioritaskan investasi keamanan, membuktikan kepada manajemen mengapa perlu budget untuk kontrol tertentu, atau menunjukkan kepada regulator bahwa risiko telah diidentifikasi dan dikelola. Dalam CPS/IoT, risk assessment lebih kompleks dari IT biasa karena mencakup: safety impact, operational technology, physical consequences, dan device lifecycle yang panjang.

---

### 4. Landasan Teori

#### 4.1 Risk Terminology

| Term | Definisi | Contoh IoT |
|------|----------|-----------|
| **Aset** | Sesuatu yang bernilai dan perlu dilindungi | Sensor, PLC, data telemetry, jaringan OT |
| **Ancaman (Threat)** | Kemungkinan penyebab kerugian | Ransomware, insider threat, supply chain attack |
| **Kelemahan (Vulnerability)** | Celah yang dapat dieksploitasi | Default password, unpatched firmware, open UART |
| **Risiko (Risk)** | Probabilitas ancaman mengeksploitasi kelemahan × dampak | Tinggi jika exploit mudah dan dampak besar |
| **Kontrol** | Mekanisme untuk mitigasi risiko | MFA, network segmentation, patch management |

**Rumus Risiko:**
```
Risk = Likelihood × Impact

Likelihood (kemungkinan eksploitasi):
  Faktor: kompleksitas exploit, motivasi threat actor,
          ketersediaan tools, aksesibilitas sistem

Impact (dampak jika eksploitasi berhasil):
  Faktor: safety impact, financial loss,
          operational disruption, reputation damage,
          privacy breach, regulatory penalty
```

#### 4.2 Risk Assessment Frameworks untuk CPS/IoT

**NIST SP 800-30 Rev. 1 — Guide for Conducting Risk Assessments:**
Framework komprehensif dari NIST yang mencakup seluruh siklus: prepare, conduct, communicate, maintain. Digunakan oleh Federal agencies AS tetapi diadopsi secara luas.

**IEC 62443-3-2 — Security Risk Assessment for IACS:**
Standard internasional khusus untuk Industrial Automation and Control Systems (IACS). Mendefinisikan proses "Target Security Level" (SL-T) berdasarkan risk assessment, lalu menentukan kontrol yang diperlukan untuk mencapai SL-T.

**Security Level dalam IEC 62443:**
```
SL 0: No specific requirements
SL 1: Protection against casual/coincidental violation
SL 2: Protection against intentional violation by low sophistication attacker
SL 3: Protection against sophisticated attacker with IACS-specific knowledge
SL 4: Protection against state-sponsored attacker with extended resources
```

#### 4.3 Risk Scoring

**Matriks Risiko 5×5 (Semi-Kuantitatif):**

| | Impact 1 | Impact 2 | Impact 3 | Impact 4 | Impact 5 |
|-|----------|----------|----------|----------|----------|
| **Likelihood 5** | 5 | 10 | 15 | 20 | 25 |
| **Likelihood 4** | 4 | 8 | 12 | 16 | 20 |
| **Likelihood 3** | 3 | 6 | 9 | 12 | 15 |
| **Likelihood 2** | 2 | 4 | 6 | 8 | 10 |
| **Likelihood 1** | 1 | 2 | 3 | 4 | 5 |

```
Score 20–25: KRITIS — immediate action required
Score 12–19: TINGGI — address within 30 days
Score 6–11:  SEDANG — address within 90 days
Score 1–5:   RENDAH — accept or monitor
```

**CVSS (Common Vulnerability Scoring System) untuk kelemahan teknis:**
```
CVSS v3.1 Base Score = f(AV, AC, PR, UI, S, C, I, A)

AV = Attack Vector (Network=N, Adjacent=A, Local=L, Physical=P)
AC = Attack Complexity (Low=L, High=H)
PR = Privileges Required (None=N, Low=L, High=H)
UI = User Interaction (None=N, Required=R)
S  = Scope (Unchanged=U, Changed=C)
C  = Confidentiality Impact (None=N, Low=L, High=H)
I  = Integrity Impact
A  = Availability Impact
```

#### 4.4 Threat Actors dalam CPS/IoT

| Threat Actor | Motivasi | Kapabilitas | Typical Targets |
|-------------|----------|-------------|-----------------|
| Script kiddie | Notoriety, fun | Rendah, tool-based | Consumer IoT, CCTV |
| Cybercriminal | Financial gain | Sedang | Smart meter, payment, ransomware |
| Insider | Sabotage, data theft | Tinggi (akses privilege) | Industrial, utility |
| Hacktivist | Political, ideology | Sedang | Utility, transportation |
| Nation-state | Espionage, disruption | Sangat tinggi | Critical infra, defense |
| Competitor | IP theft | Sedang | Manufacturing, R&D |

#### 4.5 Risk Register Format

Risk register adalah dokumen hidup yang mencatat semua risiko yang teridentifikasi beserta statusnya.

**Kolom standar Risk Register CPS/IoT:**
```
ID | Aset | Ancaman | Kelemahan | Likelihood | Impact | Risk Score |
   Kategori Risiko | Kontrol Existing | Kontrol Usulan |
   Owner | Due Date | Status | Residual Risk
```

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    SCOPE2[1. Define Scope\nSystem boundary, stakeholders,\nregulatory context]
    ASSET_MAP[2. Asset Inventory\nHW, SW, data, network,\ncriticality rating]
    THREAT_ENUM[3. Threat Enumeration\nSTRIDE + ICS-specific threats\nThreat actor profiling]
    VULN_ENUM[4. Vulnerability Enumeration\nFW scan, config review,\nhardware assessment, protocol]
    RISK_SCORE2[5. Risk Scoring\nLikelihood × Impact\nCVSS for technical vulns]
    RISK_REGFILL[6. Risk Register\nDocument all risks\nwith evidence]
    TREAT[7. Risk Treatment\nfor each risk:\nMitigate / Accept / Transfer / Avoid]
    MITIGATE[8. Control Selection\nProportional to risk score\nCost-effective]
    RESIDUAL[9. Residual Risk\nRisk remaining after\ncontrol implementation]
    ACCEPT[10. Risk Acceptance\nSign-off by risk owner\n+ management]
    REVIEW[11. Periodic Review\nTrigger: incident, change,\nperiodic schedule]

    SCOPE2 --> ASSET_MAP --> THREAT_ENUM --> VULN_ENUM --> RISK_SCORE2
    RISK_SCORE2 --> RISK_REGFILL --> TREAT --> MITIGATE --> RESIDUAL
    RESIDUAL --> ACCEPT --> REVIEW --> THREAT_ENUM
```

---

### 6. Contoh Terapan

**Kasus: Risk Assessment pada Sistem SCADA Water Treatment**

**Aset Kritis yang Diidentifikasi:**
- HMI (Human-Machine Interface) workstation
- PLC yang mengontrol dosing pump (klorinasi)
- Historian server (database data proses)
- OT network (jaringan SCADA)
- Data setpoint dan alarms

**Tabel Risk Register (sebagian):**

| ID | Aset | Ancaman | Kelemahan | L | I | Score | Prioritas |
|----|------|---------|-----------|---|---|-------|-----------|
| R-01 | HMI Workstation | Ransomware via internet | Windows tidak patch, RDP open | 4 | 5 | 20 | KRITIS |
| R-02 | PLC Dosing Pump | Unauthorized command | Modbus tanpa auth, no segmentation | 3 | 5 | 15 | TINGGI |
| R-03 | Historian Server | Data exfiltration | Default credentials, no MFA | 3 | 4 | 12 | TINGGI |
| R-04 | OT Network | Lateral movement | Flat network, no VLAN | 4 | 4 | 16 | TINGGI |
| R-05 | Remote Access | MitM / credential theft | VPN dengan shared creds | 3 | 4 | 12 | TINGGI |

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Menyusun Risk Register untuk Sistem IoT Fiktif

**Lingkungan:** Dokumen spesifikasi sistem IoT yang disediakan dosen (skenario fiktif smart building), template risk register (Lampiran E), dan referensi NIST SP 800-30

**Langkah Kerja:**
1. Baca spesifikasi sistem smart building (komponen, topologi, protokol, data)
2. Identifikasi minimal 5 aset berbeda dengan criticality rating
3. Untuk setiap aset, identifikasi minimal 2 ancaman menggunakan STRIDE
4. Identifikasi kelemahan yang relevan untuk setiap ancaman
5. Score setiap risiko (Likelihood 1–5, Impact 1–5, Risk Score = L×I)
6. Rekomendasikan kontrol mitigasi untuk setiap risiko
7. Isi template Risk Register (Lampiran E) secara lengkap

---

### 8. Latihan Pemahaman

**Soal 1 (Pemahaman — C2)**
Jelaskan perbedaan antara "risk appetite" dan "risk tolerance" dalam konteks manajemen risiko CPS/IoT. Berikan contoh konkret untuk masing-masing dalam konteks operator infrastruktur kritis.

**Soal 2 (Analisis — C4)**
Sebuah vulnerability ditemukan dalam firmware PLC yang digunakan di 50 fasilitas manufaktur. CVSS Base Score = 9.8. Namun, sistem tidak terhubung ke internet dan akses fisik sangat terbatas. Bagaimana Anda menyesuaikan penilaian risiko untuk mempertimbangkan faktor lingkungan ini? Apakah risk score masih 9.8?

**Soal 3 (Evaluasi — C5)**
Dua risiko memiliki risk score yang sama (15 = 5×3). Risiko A: Likelihood=5, Impact=3 (ancaman sangat umum, dampak sedang). Risiko B: Likelihood=3, Impact=5 (ancaman lebih jarang, tapi dampak sangat besar). Bagaimana Anda memprioritaskan keduanya? Apakah pendekatan L×I saja cukup?

**Soal 4 (Analisis — C4)**
Dalam skenario risk treatment, sebuah organisasi memilih untuk "menerima" risiko ransomware pada sistem OT karena biaya mitigasi dianggap terlalu tinggi. Kondisi apa yang harus terpenuhi agar "risk acceptance" ini dapat dibenarkan secara profesional dan etika?

**Soal 5 (Aplikasi — C3)**
Jelaskan bagaimana IEC 62443 Security Level (SL 0–4) dapat membantu dalam menentukan target keamanan untuk sistem SCADA pembangkit listrik. Apa SL yang appropriate dan mengapa?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Risk Register untuk Smart Grid Substation (C4–C5)**

Sebuah perusahaan distribusi listrik berencana modernisasi 20 gardu listrik dengan sistem SCADA berbasis IP. Komponen: RTU (Remote Terminal Unit) yang berkomunikasi via DNP3/IP ke control center, maintenance access via VPN, historian server, dan HMI lokal di setiap gardu. Regulatory requirement: IEC 62351 untuk keamanan komunikasi, NERC CIP untuk compliance.

*Pertanyaan:*
1. Lakukan asset identification dan criticality assessment untuk sistem ini
2. Buat risk register dengan minimal 6 risiko berbeda, mencakup: ancaman siber, ancaman insider, ancaman supply chain, dan ancaman fisik
3. Untuk setiap risiko, rekomendasikan treatment (mitigate/accept/transfer/avoid) dengan justifikasi
4. Bagaimana NERC CIP requirements mempengaruhi risk treatment options yang tersedia?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 3 (Risk Prioritization):**
L×I saja tidak cukup sebagai satu-satunya kriteria prioritisasi. Risiko dengan Impact=5 (catastrophic) harus mendapat perhatian lebih, bahkan jika Likelihood lebih rendah — terutama dalam CPS di mana catastrophic impact dapat berarti kehilangan jiwa atau kerusakan infrastruktur yang tidak reversible. Pendekatan yang lebih baik: (1) pisahkan risiko catastrophic ke dalam "priority queue" terlepas dari score; (2) pertimbangkan "worst-case scenario" selain expected value; (3) pertimbangkan reversibility — dampak yang reversible lebih dapat ditoleransi daripada yang irreversible; (4) dalam safety-critical system, risiko dengan Impact=5 (safety failure) harus selalu diprioritaskan atas risiko lain dengan score yang sama.

**Kunci Studi Kasus:**
Asset identification: RTU (kritis — kontrol langsung distribusi), communication link DNP3/IP (kritis — integrity), VPN endpoint (tinggi — remote access vector), historian (sedang — data, tidak kontrol langsung), HMI lokal (tinggi — fisik di substation). Risk register: (1) ransomware via VPN → R-01 Tinggi; (2) DNP3 command injection → R-02 Kritis (integrity sistem distribusi); (3) insider sabotage via HMI → R-03 Kritis (safety impact); (4) supply chain attack pada RTU firmware → R-04 Tinggi; (5) data manipulation historian → R-05 Sedang; (6) physical intrusion substation → R-06 Tinggi. NERC CIP: membatasi beberapa risk treatment options — misalnya, tidak dapat "accept" risiko terhadap BES Cyber System tanpa formal exception process; beberapa kontrol adalah mandatory (CIP-005 ESP, CIP-007 system security management, CIP-010 config management).

---

### 11. Ringkasan Bab

Risk Assessment adalah proses sistematis untuk mengidentifikasi, menganalisis, dan memprioritaskan risiko keamanan CPS/IoT. Framework utama: NIST SP 800-30 (umum), IEC 62443 (industrial), ISO 27005 (organisasional). Risk scoring menggunakan Likelihood × Impact sebagai pendekatan dasar, dengan CVSS untuk kelemahan teknis. Risk Register mendokumentasikan seluruh risiko beserta kontrol dan status. Risk Treatment menyediakan empat opsi: mitigate, accept, transfer, avoid — dengan setiap pilihan memerlukan justifikasi berbasis evidence. Dalam CPS/IoT, safety impact dan availability impact sering lebih kritis daripada confidentiality. Risk assessment bukan one-time activity — harus diperbarui periodik atau setelah perubahan signifikan.

---

### 12. Refleksi Profesional

1. Risk assessment adalah dasar dari keputusan investasi keamanan. Namun, dalam praktik, banyak organisasi menjalankan risk assessment hanya untuk memenuhi audit atau compliance, bukan sebagai alat pengambilan keputusan yang genuine. Bagaimana Anda memastikan bahwa risk assessment yang Anda fasilitasi menghasilkan keputusan yang bermakna, bukan sekadar "checkbox exercise"?

2. Dalam infrastruktur kritis, "accepting" risiko keamanan yang berdampak pada keselamatan publik merupakan keputusan yang memiliki implikasi hukum dan etika. Siapa yang berwenang untuk menyetujui "risk acceptance" untuk risiko yang dapat berpotensi mengakibatkan korban jiwa? Apakah ada kategori risiko yang tidak boleh di-"accept" dalam domain CPS/IoT?

3. Risk Register yang akurat memerlukan transparansi tentang kelemahan sistem. Di banyak organisasi, pengungkapan kelemahan di hadapan manajemen dapat menyebabkan ketidaknyamanan politis atau ketakutan akan investigasi. Bagaimana seorang security professional dapat mendorong budaya "honest risk disclosure" tanpa menciptakan iklim ketakutan atau blame?

---

---

## Bab 11 — Security Controls: Segmentation, Gateway, Secure Update, dan Monitoring

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: merancang arsitektur segmentasi jaringan untuk ekosistem CPS/IoT (C5); mengevaluasi dan memilih kontrol keamanan yang proporsional terhadap risiko yang teridentifikasi (C5); menjelaskan mekanisme secure over-the-air (OTA) update dan kondisi kritis dalam prosesnya (C4); merancang strategi monitoring dan anomaly detection untuk lingkungan OT/IoT (C5). *Sub-CPMK-4 / CPMK-4 / Eval-4*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    CTRL[Security Controls\nCPS/IoT]

    CTRL --> SEG[Network Segmentation]
    SEG --> PURDUE2[Purdue Model Implementation]
    SEG --> VLAN_SEG[VLAN separation\nIT vs OT vs IoT]
    SEG --> DMZONE[DMZ for data exchange\nbetween IT and OT]
    SEG --> FIREWALL2[Industrial firewall /\ndata diode]

    CTRL --> GW[Gateway Controls]
    GW --> PROTOCOL_GW[Protocol gateway:\nModbus → OPC-UA → REST]
    GW --> AUTHZ_GW[Authorization at gateway:\nwho can send what command]
    GW --> RATE_LIMIT[Rate limiting:\nprevent resource exhaustion]
    GW --> INSPECTION[Deep packet inspection\nfor ICS protocols]

    CTRL --> OTA[Secure OTA Update]
    OTA --> PKG_SIGN[Package signing:\nvendor signature verification]
    OTA --> HTTPS_OTA[HTTPS delivery:\nencrypted channel]
    OTA --> ROLLBACK[Rollback capability:\nif update fails]
    OTA --> STAGED[Staged rollout:\nlimited fleet first]

    CTRL --> MON[Monitoring]
    MON --> SIEM2[SIEM / Log aggregation]
    MON --> IDS_OT[IDS/IPS for OT:\nClaroty, Dragos, Nozomi]
    MON --> ANOMALY[Behavioral anomaly:\nbaseline + deviation]
    MON --> ALERT[Alert & Response\nrunbook]
```

---

### 3. Pengantar Kontekstual

Kontrol keamanan adalah implementasi konkret dari risk treatment yang direncanakan dalam risk assessment. Prinsip dasar pemilihan kontrol: proporsional terhadap risiko — kontrol yang too expensive atau too complex relatif terhadap risiko yang dimitigasi adalah penggunaan sumber daya yang tidak efisien; kontrol yang too weak terhadap risiko kritis adalah kelalaian. Dalam CPS/IoT, kontrol keamanan juga harus dipertimbangkan terhadap dampaknya pada availability dan safety.

---

### 4. Landasan Teori

#### 4.1 Network Segmentation

**Implementasi Purdue Reference Model:**
```
Level 4/5: Enterprise Network (ERP, email, internet access)
           ↕ Firewall + DMZ (perimeter between enterprise and OT)
Level 3: OT Management (Historian, OT engineering workstation,
          vulnerability scanning, patch management)
           ↕ Industrial firewall (deep packet inspection)
Level 2: Control Supervisory (SCADA, HMI, DCS)
           ↕ Industrial firewall (stateful inspection)
Level 1: Basic Control (PLC, DCS controller, RTU)
           ↕ Data diode atau strict firewall (unidirectional jika memungkinkan)
Level 0: Field devices (sensor, actuator, smart meter)
```

**VLAN Architecture:**
```
VLAN 10: IT Corporate
VLAN 20: OT Level 3 (Historian, OT management)
VLAN 30: OT Level 2 (SCADA, HMI)
VLAN 40: OT Level 1 (PLC, controller)
VLAN 50: IoT devices (sensor, actuator, smart devices)
VLAN 99: Management (out-of-band, access for authorized admin only)

Inter-VLAN routing: hanya melalui firewall dengan ACL ketat
```

#### 4.2 Data Diode dan Unidirectional Gateway

Data diode adalah solusi hardware yang memungkinkan data mengalir hanya satu arah — dari OT ke IT, tidak pernah sebaliknya. Digunakan untuk melindungi lingkungan kritis yang tidak boleh menerima koneksi dari luar apapun.

```
Historian (OT) → [Data Diode] → Reporting Server (IT)
                   (hardware enforced, unidirectional)
                   ← (tidak ada jalur balik)
```

Vendor: Waterfall Security Solutions, Owl Cyber Defense, Fox DataDiode.

#### 4.3 Security Gateway / Industrial Firewall

Industrial firewall berbeda dari IT firewall karena:
- Memahami protokol ICS (Modbus, DNP3, EtherNet/IP, OPC-UA)
- Deep packet inspection di level application layer untuk protokol OT
- Dapat enforce: fungsi code apa yang diizinkan, register mana yang dapat dibaca/ditulis

**Contoh aturan industrial firewall:**
```
Rule 1: ALLOW source=SCADA_HMI, dst=PLC_001, protocol=Modbus TCP,
        function_code=3 (Read Holding Registers), register=0-99
Rule 2: ALLOW source=SCADA_HMI, dst=PLC_001, protocol=Modbus TCP,
        function_code=16 (Write Multiple Registers), register=10-19
Rule 3: DENY ALL OTHER Modbus traffic to PLC_001
```

#### 4.4 Secure OTA Update

Firmware update adalah salah satu vektor serangan supply chain paling berbahaya — jika proses update dicompromise, attacker dapat mendistribusikan malware ke seluruh fleet.

**Komponen Secure OTA:**
```
1. Package Preparation (di server vendor):
   - Firmware dikompilasi dalam secure build environment
   - Signed dengan vendor private key (HSM-protected)
   - Metadata: version, target device model, checksum, timestamp

2. Distribusi:
   - HTTPS/TLS 1.3 dari update server yang diautentikasi
   - Certificate pinning pada device (verifikasi update server cert)
   - Delta updates untuk efisiensi bandwidth (hanya diff)

3. Verification on Device:
   - Verifikasi HTTPS certificate update server
   - Verifikasi signature paket dengan vendor public key (embedded dalam device)
   - Verifikasi SHA-256/512 checksum
   - Verifikasi version (anti-downgrade: tidak bisa install versi lebih lama)

4. Installation:
   - Flash ke slot/partition cadangan (A/B partition scheme)
   - Reboot ke firmware baru
   - Health check: jika gagal → automatic rollback ke firmware lama

5. Konfirmasi:
   - Device report success ke update server
   - Update server catat completion
```

**Anti-rollback protection:**
Version counter yang di-increment dalam eFuse (irreversible) — mencegah downgrade ke firmware yang memiliki kelemahan diketahui.

#### 4.5 Monitoring dan Anomaly Detection

**Pendekatan monitoring CPS/IoT:**

1. **Network-based monitoring:** Analisis traffic tanpa mengganggu device (passive tap atau SPAN port)
2. **Log aggregation:** Kirim log dari gateway, historian, dan aplikasi ke SIEM
3. **Behavioral baseline:** Pelajari pola normal → deteksi anomali

**Behavioral baseline untuk IoT:**
```
Contoh baseline untuk sensor suhu industri:
- Normal: mengirim telemetry setiap 30 detik
- Normal: nilai suhu antara 20°C–150°C
- Normal: berkomunikasi hanya dengan gateway 192.168.10.1
- Normal: tidak pernah memulai koneksi keluar

Anomali → Alert:
- Telemetry interval berubah drastis
- Nilai diluar range (sensor failure atau data manipulation)
- Koneksi ke IP yang tidak dikenal
- Volume traffic tiba-tiba meningkat 10×
```

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    INTERNET[Internet / Enterprise]
    PERIM_FW[Perimeter Firewall\n+ IPS]
    DMZ2[DMZ\nUpdate Server, Remote Access\nForensic Jump Host]
    OT_FW[OT Boundary Firewall\nDeep Packet Inspection]
    SCADA_NET[SCADA / Level 2 Network\nHMI, Engineering WS]
    CTRL_FW[Control Network Firewall\nStrict ACL]
    PLC_NET[PLC / Level 1 Network\nPLC, RTU, DCS]
    FIELD_SEG[Field Device Network\nSensor, Actuator]

    DATA_DIODE[Data Diode →\nHistorian → Reporting]
    SIEM3[SIEM + OT-IDS\nNozomi / Claroty / Dragos]

    INTERNET <--> PERIM_FW
    PERIM_FW <--> DMZ2
    DMZ2 <--> OT_FW
    OT_FW <--> SCADA_NET
    SCADA_NET <--> CTRL_FW
    CTRL_FW <--> PLC_NET
    PLC_NET <--> FIELD_SEG

    SCADA_NET --> DATA_DIODE

    PERIM_FW -.->|logs| SIEM3
    OT_FW -.->|logs| SIEM3
    CTRL_FW -.->|logs| SIEM3
    SCADA_NET -.->|logs| SIEM3
    PLC_NET -.->|traffic mirror| SIEM3
```

---

### 6. Contoh Terapan

**Kasus: Implementasi Defense-in-Depth pada Smart Factory**

Setelah risk assessment mengidentifikasi R-01 (ransomware via internet, Kritis) dan R-02 (unauthorized PLC command, Kritis):

**Kontrol untuk R-01 (Ransomware):**
- Network segmentation: HMI dan engineering workstation di VLAN OT terpisah
- Perimeter firewall: hanya mengizinkan koneksi dari specific IP ke VPN
- OT-spesifik: disable RDP ke HMI, enable application whitelisting
- Offline backup: historian backup ke media offline yang tidak terhubung ke OT network

**Kontrol untuk R-02 (Unauthorized PLC Command):**
- Industrial firewall dengan DPI Modbus: hanya SCADA HMI dapat kirim command ke PLC
- Whitelist function codes: hanya function code 3 (read) dan 16 (write setpoint) yang diizinkan
- Command logging: semua command ke PLC di-log untuk audit
- Behavioral monitoring: alert jika command dari sumber yang tidak dikenal

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Perancangan Arsitektur Segmentasi untuk Smart Building

**Lingkungan:** Kertas/simulasi atau network diagram tool (draw.io, Lucidchart); tidak memerlukan akses ke network production

**Langkah Kerja:**
1. Diberikan spesifikasi sistem smart building (HVAC, CCTV, access control, energy management, IT corporate)
2. Identifikasi semua perangkat dan kelompokkan berdasarkan Purdue level
3. Rancang VLAN architecture dengan justifikasi setiap segmentasi
4. Tentukan firewall rules antar VLAN (minimum 5 rules per interface)
5. Rancang strategi monitoring: di mana menempatkan sensor/tap dan jenis alerting apa
6. Evaluasi apakah data diode tepat digunakan di titik manapun dalam arsitektur

---

### 8. Latihan Pemahaman

**Soal 1 (Pemahaman — C2)**
Jelaskan perbedaan antara data diode dan industrial firewall. Dalam kondisi apa data diode lebih tepat daripada firewall, dan apa trade-off yang ditanggung?

**Soal 2 (Analisis — C4)**
Sebuah proses OTA update tidak mengimplementasikan anti-downgrade protection. Jelaskan skenario serangan di mana attacker dapat mengeksploitasi kelemahan ini, dan apa dampaknya.

**Soal 3 (Evaluasi — C5)**
Sebuah operator utilitas mempertimbangkan untuk menerapkan behavioral anomaly detection pada jaringan PLC mereka. Mereka khawatir bahwa sistem akan menghasilkan terlalu banyak false positive selama perubahan operasional normal (maintenance, seasonal changes). Bagaimana Anda mendesain sistem monitoring yang meminimalkan false positive sambil tetap mendeteksi ancaman nyata?

**Soal 4 (Analisis — C4)**
Sebuah IoT device menggunakan "certificate pinning" untuk memverifikasi update server, tetapi certificate update server expired dan tidak diperbarui tepat waktu. Apa yang terjadi, dan bagaimana desain yang lebih baik untuk menghindari situasi ini?

**Soal 5 (Evaluasi — C5)**
Mengapa A/B partition scheme dalam OTA update dianggap critical requirement, bukan nice-to-have? Jelaskan skenario kegagalan tanpa A/B partition dan dengan A/B partition.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Defense-in-Depth untuk Sistem Manajemen Gedung (C4–C5)**

Sebuah gedung perkantoran 40 lantai memiliki Building Management System (BMS) yang terintegrasi: HVAC, lift, akses kontrol, CCTV IP, smart meter listrik, dan jaringan tenant. Semua terhubung ke satu network. Insiden terakhir: seorang karyawan tenant mengakses panel kontrol HVAC melalui laptop yang terinfeksi malware, menyebabkan sistem pendingin mati selama 4 jam di tengah cuaca panas ekstrem.

*Pertanyaan:*
1. Identifikasi semua kelemahan arsitektur yang memungkinkan insiden ini terjadi
2. Rancang arsitektur segmentasi yang mencegah recurrence — berikan diagram dengan VLAN, firewall, dan data flow
3. Tentukan kontrol monitoring yang harus diimplementasikan untuk mendeteksi insiden serupa lebih awal
4. Rancang prosedur OTA update yang aman untuk komponen BMS yang tersebar di 40 lantai

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 5 (A/B Partition):**
Tanpa A/B partition: satu-satunya firmware yang ada mulai di-overwrite selama update. Jika update gagal di tengah jalan (power failure, network drop, corrupt package), device bisa boot ke firmware yang rusak dan tidak berfungsi (brick). Satu-satunya recovery: intervensi fisik atau factory reset. Untuk device di lokasi remote atau device yang tidak dapat diakses secara fisik dengan mudah, ini adalah bencana operasional. Dengan A/B partition: firmware baru di-write ke slot B (tidak mengganggu slot A yang sedang berjalan); setelah write selesai dan checksum verified, device reboot ke slot B; jika boot ke slot B gagal (health check failure), device otomatis reboot ke slot A (known-good firmware). Result: update failure tidak mengakibatkan brick device. Ini adalah critical requirement terutama untuk device remote, device yang tidak dapat diakses secara fisik, dan device dalam infrastruktur kritis.

**Kunci Studi Kasus BMS:**
Kelemahan: (1) flat network — tenant dan BMS terhubung langsung; (2) tidak ada segmentasi antara HVAC, lift, akses kontrol, CCTV; (3) laptop tenant dapat mengakses langsung panel kontrol HVAC; (4) tidak ada monitoring untuk mendeteksi anomali. Arsitektur: VLAN Tenant (10.1.0.0/24), VLAN CCTV (10.2.0.0/24), VLAN Akses Kontrol (10.3.0.0/24), VLAN HVAC/BMS (10.4.0.0/24), VLAN Manajemen (10.5.0.0/24); firewall antara semua VLAN; tenant TIDAK dapat berkomunikasi ke VLAN BMS apapun; BMS management hanya dari VLAN Manajemen dengan MFA. Monitoring: IDS pada BMS VLAN, alert untuk setiap koneksi dari luar VLAN Manajemen ke BMS, logging semua command ke HVAC controller. OTA update: update server di VLAN Manajemen, device tarik update (pull model) bukan server push ke device, signature verification mandatory, update dilakukan di luar jam kerja dengan change management approval.

---

### 11. Ringkasan Bab

Security controls dalam CPS/IoT harus proporsional dengan risiko dan tidak mengorbankan availability. Network segmentation menggunakan Purdue Model sebagai referensi, dengan VLAN, industrial firewall, dan data diode sebagai implementasi. Industrial firewall mampu deep packet inspection pada protokol OT (Modbus, DNP3, EtherNet/IP). Secure OTA update memerlukan: package signing, HTTPS delivery, anti-downgrade, A/B partition untuk rollback, dan staged rollout. Monitoring efektif menggunakan kombinasi: SIEM, OT-specific IDS (Claroty, Nozomi, Dragos), dan behavioral baseline. Defense-in-depth berarti lapisan kontrol saling melengkapi — tidak ada single point of failure dalam pertahanan.

---

### 12. Refleksi Profesional

1. Segmentasi jaringan dalam lingkungan OT sering menghadapi resistensi dari tim operasional yang khawatir bahwa segmentasi akan mengganggu aliran data operasional atau menyulitkan troubleshooting. Sebagai security professional, bagaimana Anda membangun kasus bisnis untuk segmentasi yang meyakinkan tim OT — bukan hanya manajemen — bahwa ini adalah investasi yang tepat?

2. OTA update dalam infrastruktur kritis menghadapi dilema timing: update segera setelah kelemahan ditemukan (mengurangi exposure window) versus testing extensive sebelum deploy (mengurangi risiko update-induced failure). Dalam industri yang mengoperasikan pipeline gas atau reaktor nuklir, kegagalan sistem akibat update yang buruk bisa sama berbahayanya dengan serangan siber. Bagaimana industri mengelola dilema ini?

3. Behavioral anomaly detection untuk ICS/OT memerlukan baseline yang akurat tentang "operasi normal." Dalam fasilitas yang memiliki banyak variasi produk, perubahan shift, maintenance windows, dan seasonal variation, membangun baseline yang akurat sangat challenging. Bagaimana Anda mendekati pembangunan baseline yang robust untuk lingkungan seperti ini, tanpa false positive yang berlebihan namun tetap efektif?

---

---

## Bab 12 — Incident Readiness, Resilience, dan Recovery CPS/IoT

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: merancang incident response plan yang disesuaikan untuk lingkungan CPS/IoT (C5); menjelaskan perbedaan mendasar antara IR pada IT dan OT/CPS dalam hal prioritas dan prosedur (C4); menganalisis skenario insiden CPS/IoT dan menentukan langkah respons yang tepat (C4); merancang strategi resilience dan recovery yang mempertahankan operational continuity (C5). *Sub-CPMK-5 / CPMK-5 / Eval-4/5*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    IRP[Incident Response\nCPS/IoT]

    IRP --> PREPARE[Preparation]
    PREPARE --> IRP_PLAN[IR Plan document]
    PREPARE --> TEAM[IR Team:\nOT + IT + Safety]
    PREPARE --> RUNBOOK2[Runbooks per scenario]
    PREPARE --> CONTACT[Vendor contacts\nRegulator contacts]

    IRP --> DETECT2[Detection]
    DETECT2 --> SIEM_ALERT[SIEM / OT-IDS alert]
    DETECT2 --> HUMAN[Human observation:\noperator report]
    DETECT2 --> SAFETY_TRIP[Safety system trip\nas indicator]

    IRP --> CONTAIN[Containment]
    CONTAIN --> ISOLATE[Network isolation:\nlogical or physical]
    CONTAIN --> SAFE_STATE[Drive to safe state:\nbefore isolation]
    CONTAIN --> PRESERVE[Evidence preservation]

    IRP --> ERADICATE[Eradication]
    ERADICATE --> ROOT_CAUSE[Root cause analysis]
    ERADICATE --> CLEAN[Clean / re-image]
    ERADICATE --> PATCH2[Patch vulnerability]

    IRP --> RECOVER[Recovery]
    RECOVER --> RESTORE[Restore from\nknown-good backup]
    RECOVER --> VERIFY[Verify integrity\nbefore production]
    RECOVER --> STAGED_R[Staged return\nto service]

    IRP --> LESSONS[Post-Incident Review]
    LESSONS --> PIR[Post-Incident Report]
    LESSONS --> IMPROVE[Improve controls\nand procedures]
```

---

### 3. Pengantar Kontekstual

Incident response dalam CPS/IoT adalah disiplin yang sangat berbeda dari IR dalam lingkungan IT konvensional. Dalam IT, "isolasi system" adalah langkah standar awal — sistem di-shutdown dan diisolasi dari jaringan. Dalam OT/CPS, tindakan yang sama dapat mematikan conveyor belt pabrik, menyebabkan proses kimia kehilangan kontrol, atau memadamkan listrik bagi ribuan pelanggan. Keputusan isolasi dalam OT harus selalu diawali oleh pertanyaan: "Apa kondisi proses yang aman sebelum kita melakukan ini?"

---

### 4. Landasan Teori

#### 4.1 Perbedaan IT vs OT Incident Response

| Aspek | IT IR | OT/CPS IR |
|-------|-------|-----------|
| Prioritas pertama | Confidentiality & Integrity | Safety & Availability |
| Isolasi sistem | Segera, standar | Hanya setelah process safe state |
| Shutdown terduga | Umumnya aman | Dapat menyebabkan safety hazard |
| Evidence preservation | Forensic image dulu | Safety first, forensic second |
| Waktu recovery | Hours–days dapat diterima | Minutes–hours (production loss) |
| Koordinasi | IT team | IT + OT + Safety + Management |
| Backup/restore | Relatif straightforward | Memerlukan recalibration, re-validation |

#### 4.2 Fase Incident Response CPS/IoT

**Fase 1: Preparation**
- Incident Response Plan (IRP) terdokumentasi dan dilatih
- IR Team dengan jelas mendefinisikan: siapa yang menghubungi siapa, eskalasi kepada siapa
- Pre-approved isolated network segment untuk forensic investigation
- Backup verified dan tested — termasuk restoration procedure
- Kontak vendor PLC/SCADA untuk emergency support
- Kontak regulator (jika critical infrastructure: BSSN, PLN, regulator sektoral)
- Tabletop exercise minimal setahun sekali

**Fase 2: Detection & Analysis**
```
Indikator insiden dalam CPS/IoT:
- SIEM/OT-IDS alert (unusual traffic, protocol anomaly)
- Operator melaporkan perilaku HMI yang tidak normal
- Setpoint berubah tanpa perintah operator
- Safety Instrumented System (SIS) trip yang tidak terduga
- Alarm yang terlalu banyak atau terlalu sedikit
- Komunikasi antara level yang tidak seharusnya (IT → PLC direct)
- Performa jaringan degradasi tiba-tiba
```

**Fase 3: Containment — CPS-Specific**
```
Pra-kondisi WAJIB sebelum isolasi OT:
1. Identifikasi current process state
2. Konsultasi operator dan engineer OT: apakah aman untuk isolasi?
3. Jika proses berbahaya (kimia, tekanan tinggi, dll.):
   → Drive process ke safe state terlebih dahulu
   → Dokumentasikan state sebelum isolasi
4. Pastikan Safety Instrumented System (SIS) tetap berfungsi
5. Jangan pernah isolasi SIS bersamaan dengan SCADA sebelum ada clearance safety

Setelah safe state confirmed:
- Isolasi segment yang terdampak dari network OT yang lebih luas
- Jangan shutdown device yang terdampak dulu (preserve volatile evidence)
- Jika perlu shutdown: catat semua state terlebih dahulu
```

**Fase 4: Evidence Preservation**
```
OT/ICS forensic priorities:
1. Network captures (SPAN port, taps) — sebelum isolasi jika memungkinkan
2. Log dari SIEM, historian, firewall
3. Volatile memory dari workstation HMI (jika memungkinkan dan aman)
4. Konfigurasi snapshot dari PLC/RTU (bukan interrupt operasi aktif)
5. Foto fisik perangkat dan koneksi (chain of custody)
6. Wawancara operator (catat apa yang dilihat, kapan, sequence of events)
```

**Fase 5: Eradication & Recovery**
```
Jangan terburu-buru ke recovery — eradikasi yang tidak tuntas
menyebabkan re-infection.

1. Root cause analysis: bagaimana attacker masuk? Apa yang dilakukan?
2. Identifikasi semua sistem yang terkompromi
3. Re-image atau restore dari clean backup yang diverifikasi
4. Patch vulnerability yang dieksploitasi
5. Change semua credentials yang mungkin terekspos

Recovery tahapan:
1. Lab/isolated environment: test sistem yang di-restore
2. Staging: operasikan dalam mode terbatas sebelum production
3. Production: only after verification + management sign-off
```

#### 4.3 Resilience dan Business Continuity

**Recovery Time Objective (RTO) dan Recovery Point Objective (RPO):**
```
RTO: Berapa lama sistem boleh down? (untuk OT, sering <1 jam atau bahkan menit)
RPO: Berapa banyak data boleh hilang? (untuk proses industri, sering near-zero)

→ RTO dan RPO menentukan frekuensi backup dan kompleksitas recovery procedure
```

**Redundancy untuk CPS/ICS:**
- Active-active: dua PLC berjalan paralel, failover otomatis
- Hot standby: backup PLC siap dalam milidetik
- Warm standby: backup PLC perlu 1–5 menit untuk aktif
- Cold standby: backup PLC memerlukan manual intervention untuk aktif

**Cyber-Physical Recovery Challenges:**
- Re-kalibrasi sensor setelah replacement
- Re-validation prosedur after firmware restore
- Process restart yang aman setelah shutdown (urutan startup dapat kritis)
- Verifikasi bahwa setpoint dan konfigurasi kembali ke nilai yang benar

---

### 5. Model atau Arsitektur

```mermaid
sequenceDiagram
    participant OPS as Operator/OT Team
    participant SOC2 as SOC/Security Team
    participant MGMT as Management
    participant VENDOR as Vendor Support

    OPS->>SOC2: Report: anomalous HMI behavior
    SOC2->>SOC2: Triage: classify incident severity
    SOC2->>OPS: Request: current process state assessment
    OPS-->>SOC2: Process state: pressure nominal, safe to investigate
    SOC2->>MGMT: Escalate: potential cyber incident in OT
    MGMT-->>SOC2: Authorize: containment actions
    SOC2->>OPS: Coordinate: isolate affected VLAN
    OPS->>OPS: Drive process to safe state
    OPS-->>SOC2: Safe state confirmed
    SOC2->>SOC2: Isolate network segment
    SOC2->>VENDOR: Engage: OT vendor emergency support
    VENDOR-->>SOC2: Provide: forensic guidance for PLC
    SOC2->>SOC2: Collect evidence (logs, network captures)
    SOC2->>SOC2: Root cause analysis
    SOC2->>OPS: Provide: clean system for verification
    OPS->>OPS: Verify system integrity in isolated env
    OPS-->>MGMT: Ready for staged recovery
    MGMT-->>OPS: Authorize: production recovery
```

---

### 6. Contoh Terapan

**Kasus: Ransomware pada Jaringan OT Fasilitas Air**

Sebuah PDAM mendeteksi enkripsi massal file di workstation HMI pada pukul 02.00. Sistem SCADA mengalami gangguan, tetapi PLC yang mengontrol pompa dan dosing kimia masih beroperasi secara otomatis menggunakan setpoint terakhir.

**Respons yang dilakukan:**
1. **Detection (02.05):** SOC menerima alert ransomware dari endpoint protection di workstation HMI
2. **Assessment (02.10):** OT engineer konfirmasi: PLC masih berjalan, proses air dalam batas normal, tidak ada bahaya immediat
3. **Containment (02.20):** Isolasi VLAN level 2 (SCADA/HMI) dari level 1 (PLC) — PLC tetap berjalan dalam mode autonomous dengan setpoint sebelumnya
4. **Evidence (02.30–04.00):** Capture log SIEM, historis koneksi, image HMI workstation
5. **Eradication (04.00–08.00):** Identifikasi entry point (VPN dengan credential yang dikompromis), reset semua credentials, re-image workstation dari backup
6. **Recovery (08.00–10.00):** Restore HMI dalam isolated environment, verify, staged reconnect ke PLC, verify monitoring, production recovery
7. **Post-Incident:** Implementasi MFA untuk VPN, segmentasi tambahan, training operator

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Tabletop Exercise — Insiden CPS/IoT

**Lingkungan:** Skenario tertulis yang disediakan dosen; tidak memerlukan sistem nyata

**Langkah Kerja:**
1. Dosen membagikan skenario insiden (pilihan: ransomware, insider sabotage, sensor manipulation, supply chain)
2. Mahasiswa dalam kelompok (5–6 orang) berperan sebagai: SOC analyst, OT engineer, safety officer, management, legal/compliance
3. Jalankan tabletop exercise mengikuti fase IR: detection → containment → eradication → recovery
4. Setiap keputusan harus dijustifikasi dan dampaknya pada safety/operations dipertimbangkan
5. Dokumentasikan seluruh keputusan dan alasannya dalam format incident timeline
6. Post-exercise: presentasikan lessons learned dan improvement yang direkomendasikan

---

### 8. Latihan Pemahaman

**Soal 1 (Pemahaman — C2)**
Jelaskan mengapa "isolasi segera" yang merupakan langkah standar dalam IT incident response tidak dapat diterapkan secara langsung dalam OT/CPS. Apa pra-kondisi yang harus dipenuhi sebelum isolasi dilakukan?

**Soal 2 (Analisis — C4)**
Seorang attacker berhasil mengakses SCADA system dan mengubah setpoint pompa dosing kimia di fasilitas pengolahan air. Operator tidak menyadari karena HMI masih menampilkan nilai normal (spoofed display). Identifikasi indicator of compromise apa yang seharusnya dapat mendeteksi serangan ini bahkan ketika HMI di-spoof.

**Soal 3 (Evaluasi — C5)**
Setelah insiden ransomware, management meminta recovery "secepat mungkin" karena setiap jam downtime mengakibatkan kerugian finansial signifikan. Security team ingin melakukan forensic investigation lengkap sebelum recovery. Bagaimana Anda mengelola ketegangan ini, dan argumen apa yang Anda berikan kepada management?

**Soal 4 (Analisis — C4)**
Jelaskan perbedaan antara RTO (Recovery Time Objective) dan RPO (Recovery Point Objective). Untuk sistem kontrol pembangkit listrik, nilai RTO dan RPO yang realistis adalah berapa, dan bagaimana ini mempengaruhi desain backup strategy?

**Soal 5 (Aplikasi — C3)**
Sebuah PLC yang terkompromi perlu di-restore. Firmware backup tersedia, tetapi backup configuration (setpoint, ladder logic) terakhir adalah 3 bulan lalu. Langkah-langkah apa yang diperlukan sebelum me-restore backup ke PLC production?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — IR pada Insiden Manipulasi Data Sensor (C4–C5)**

Sistem monitoring kualitas udara di kawasan industri mengirimkan data ke platform cloud pemerintah. Sebuah insiden terdeteksi: data PM2.5 dari 15 sensor menunjukkan nilai normal (30 µg/m³) selama 6 jam, sementara sensor referensi manual menunjukkan nilai berbahaya (250 µg/m³). Investigasi awal menunjukkan bahwa gateway IoT yang menggabungkan data sensor sebelum dikirim ke cloud mengalami unauthorized access.

*Pertanyaan:*
1. Buat timeline respons insiden dari detection hingga recovery dengan justifikasi setiap tindakan
2. Identifikasi evidence apa yang harus dikumpulkan dan bagaimana chain-of-custody dikelola (khususnya jika data ini relevan secara hukum karena terkait regulasi kualitas udara)
3. Selain recovery teknis, identifikasi implikasi hukum, regulasi, dan reputasi dari insiden ini, serta langkah non-teknis yang diperlukan

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 3 (Recovery vs Forensics Tension):**
Argumen kunci untuk manajemen: (1) Recovery tanpa mengetahui root cause adalah recovery yang tidak aman — jika attacker masih memiliki akses, sistem akan dikompromise kembali dalam hitungan jam, menyebabkan downtime yang lebih panjang; (2) Minimum forensics diperlukan: cukup untuk mengidentifikasi entry point dan memastikan semua persistence mechanism dihapus — tidak perlu full forensics dulu; (3) Paralel approach: sebagian tim mulai persiapan recovery (restore environment, prepare clean systems) sementara tim lain melakukan forensic investigation; (4) Staged recovery: mulai dengan fungsi paling kritis dulu — tidak harus full recovery sekaligus; (5) Legal consideration: jika insiden melibatkan infrastruktur kritis, regulasi mungkin mewajibkan investigation sebelum recovery (NERC CIP, NIS2, etc.). Kesimpulan: propose "minimum viable forensics" (4–8 jam) sebelum recovery, dengan paralel persiapan recovery, untuk menyeimbangkan kebutuhan bisnis dan kebutuhan keamanan.

**Kunci Studi Kasus:**
Timeline: T+0 deteksi anomali (sensor vs manual reference), T+30min SOC dilibatkan, T+1h isolasi gateway dari pengiriman ke platform cloud (hentikan pengiriman data palsu), T+1.5h preserve evidence gateway (memory dump, log, konfigurasi), T+2h notifikasi regulator (kewajiban hukum jika critical infrastructure), T+4h root cause: unauthorized access via unpatched web interface gateway, T+8h re-image gateway dari clean backup, T+10h verify data dengan manual reference, T+12h resume reporting dengan monitoring ketat. Evidence: log akses gateway, network captures, konfigurasi sebelum dan sesudah, data sensor asli vs yang dikirim. Chain of custody: hash semua evidence, tandatangani setiap transfer. Implikasi non-teknis: kemungkinan pelanggaran regulasi environmental reporting; notifikasi kepada instansi lingkungan hidup; investigasi apakah ada pihak yang diuntungkan dari data palsu (misalnya fasilitas yang seharusnya membayar denda emisi).

---

### 11. Ringkasan Bab

Incident response dalam CPS/IoT berbeda fundamental dari IT IR — safety dan availability mendahului confidentiality. Pra-kondisi isolasi OT: sistem harus dalam safe state terlebih dahulu. Fase IR: Preparation → Detection → Containment (safe-state first) → Evidence Preservation → Eradication → Recovery (staged) → Post-Incident. Forensics CPS/IoT mencakup log historian, network captures, PLC configuration snapshot, dan wawancara operator. Recovery memerlukan: restore dari clean backup, re-kalibrasi, re-validasi, dan staged return to service. Tabletop exercise adalah investasi yang sangat cost-effective untuk kesiapan IR. Insiden yang tidak ditangani dengan benar (root cause tidak ditemukan) sering berakhir dengan reinfection.

---

### 12. Refleksi Profesional

1. Dalam insiden CPS yang berdampak pada keselamatan publik (misalnya: manipulasi data sensor kualitas udara, gangguan distribusi air), ada kewajiban hukum dan etika untuk menotifikasi pihak berwenang dan publik. Kapan dan bagaimana notification harus dilakukan, mengingat ketegangan antara: kebutuhan investigasi (yang mungkin memerlukan kerahasiaan), kebutuhan publik untuk tahu, dan risiko reputasi organisasi?

2. Tabletop exercise sering dianggap sebagai formalitas — dilakukan setahun sekali untuk memenuhi compliance, bukan untuk truly test kesiapan. Bagaimana Anda merancang tabletop exercise yang benar-benar mengungkap gap dalam kesiapan IR, bukan sekadar menjalankan skenario yang sudah familiar kepada peserta?

3. Industri CPS/OT sering memiliki ketergantungan pada vendor tunggal untuk komponen kritis (satu vendor PLC, satu vendor SCADA). Ketika terjadi insiden yang memerlukan emergency vendor support, organisasi sepenuhnya bergantung pada responsiveness vendor. Bagaimana organisasi mengelola risiko ini dalam kontrak vendor dan rencana kontinuitas bisnis?

---

---

## Bab 13 — Capstone: Secure CPS/IoT Architecture Design

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: merancang arsitektur CPS/IoT yang aman secara end-to-end berdasarkan prinsip defense-in-depth (C5); mengintegrasikan semua domain keamanan (device, komunikasi, cloud, OT network) dalam satu rancangan kohesif (C5); mengevaluasi arsitektur yang ada terhadap standar dan framework industri (C5); mendokumentasikan keputusan arsitektur keamanan dengan justifikasi berbasis risk (C5). *Sub-CPMK-5 / CPMK-5 / Eval-5*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    CAP[Secure CPS/IoT\nArchitecture Design\nCapstone]

    CAP --> REQ[Requirements Analysis]
    REQ --> FUNC[Functional requirements:\nwhat system must do]
    REQ --> SEC_REQ[Security requirements:\nwhat risks must be mitigated]
    REQ --> REG_REQ[Regulatory requirements:\ncompliance obligations]
    REQ --> OPS_REQ[Operational requirements:\navailability, maintainability]

    CAP --> DESIGN[Architecture Design]
    DESIGN --> DEVICE_LAYER[Device Layer:\nidentity, secure boot, firmware]
    DESIGN --> COMM_LAYER[Communication Layer:\nprotocol, TLS, segmentation]
    DESIGN --> PLATFORM[Platform/Cloud Layer:\nAPI security, IAM, logging]
    DESIGN --> OT_LAYER[OT Layer:\nPurdue model, industrial FW]

    CAP --> VALIDATE[Validation]
    VALIDATE --> THREAT_VAL[Threat model vs architecture]
    VALIDATE --> CONTROL_MAP[Control mapping:\neach risk has mitigation]
    VALIDATE --> GAP[Gap analysis:\nunmitigated risks]
    VALIDATE --> RESIDUAL2[Residual risk acceptance]

    CAP --> DOC[Documentation]
    DOC --> ARCH_DOC[Architecture Document]
    DOC --> DECISION[Architecture Decision Records]
    DOC --> RATIONALE[Security rationale per decision]
```

---

### 3. Pengantar Kontekstual

Capstone ini mengintegrasikan seluruh materi yang telah dipelajari: dari threat modelling (Bab 3), protokol keamanan (Bab 4–5), device identity (Bab 6), firmware dan hardware security (Bab 7–9), risk assessment (Bab 10), security controls (Bab 11), hingga incident readiness (Bab 12). Kemampuan untuk merancang arsitektur yang aman dari awal adalah kompetensi tertinggi yang diuji — ini adalah pekerjaan nyata seorang security architect dalam industri.

---

### 4. Landasan Teori

#### 4.1 Prinsip Desain Arsitektur Keamanan CPS/IoT

**Security by Design (SbD):**
Keamanan harus dipertimbangkan dari fase desain, bukan di-boleh setelah sistem selesai dibangun. "Security by design" bukan sekadar slogan — ia memiliki implikasi teknis konkret: keputusan yang dibuat di fase desain (pemilihan SoC, protokol komunikasi, cloud provider) menentukan batas atas keamanan yang dapat dicapai.

**Defense-in-Depth:**
```
Tidak ada single control yang cukup. Setiap layer harus memiliki pertahanan sendiri,
sehingga jika satu layer dikompromis, layer lain masih melindungi.

Layer pertahanan dalam CPS/IoT:
1. Physical: akses kontrol fisik ke perangkat
2. Hardware: Secure Boot, SE/TPM, debug port disabled
3. Firmware: secure coding, minimal footprint, update mechanism
4. Network device: mTLS, device identity, certificate
5. Protocol: TLS, signed messages, anti-replay
6. Gateway/Edge: auth, authz, rate limiting, protocol validation
7. OT Network: segmentation, industrial firewall, monitoring
8. Cloud/Platform: API security, IAM, logging, SIEM
9. Process: secure development, change management, IR readiness
```

**Zero Trust untuk CPS/IoT:**
```
"Never trust, always verify" — bahkan device yang terhubung ke internal network
harus diautentikasi dan diotorisasi untuk setiap aksi.

Implikasi Zero Trust untuk IoT:
- Setiap device harus memiliki identity yang unik dan dapat diverifikasi
- Device tidak secara otomatis mendapat akses ke semua resource dalam network yang sama
- Micro-segmentation: isolasi per device atau per device group
- Continuous monitoring: anomali → revoke akses
```

#### 4.2 Architecture Decision Records (ADR)

ADR adalah dokumen yang mencatat keputusan arsitektur beserta konteks, alternatif yang dipertimbangkan, dan alasan pemilihan. Dalam security architecture, ADR sangat penting untuk auditability.

**Format ADR:**
```
ADR-001: Pemilihan protokol komunikasi untuk sensor ke gateway

Konteks: Sensor dengan MCU 32-bit, battery-powered, bandwidth terbatas,
         komunikasi jarak 50-200m, environment industri

Keputusan: MQTT over TLS 1.3 dengan mTLS authentication

Alternatif yang dipertimbangkan:
- CoAP + DTLS: lebih ringan untuk UDP, tetapi implementasi DTLS pada MCU target
  masih immature, library kurang tested
- HTTP/REST: terlalu berat untuk MCU target, overhead besar
- LoRaWAN: range lebih lebar, tetapi enkripsi per standard lebih lemah (AES-128 shared)

Konsekuensi:
- (+) MQTT well-supported, library matang untuk MCU target (ESP-IDF, STM32Cube)
- (+) TLS 1.3 memberikan PFS, mengurangi session overhead vs TLS 1.2
- (-) MQTT over TLS memerlukan lebih banyak resource dibanding CoAP/DTLS
- (-) Perlu CA infrastructure untuk device certificates
```

#### 4.3 Threat Model vs Architecture Mapping

Setelah arsitektur dirancang, setiap ancaman dalam threat model harus dipetakan ke kontrol yang memitigasinya:

```
| Ancaman (STRIDE) | Kontrol Arsitektur | Status |
|-----------------|-------------------|--------|
| S: Device spoofing | mTLS client cert | MITIGATED |
| T: Payload tampering | Message signing (ECDSA) | MITIGATED |
| R: Replay attack | Timestamp + nonce | MITIGATED |
| I: Protocol analysis | TLS 1.3 enkripsi | MITIGATED |
| D: Gateway overload | Rate limiting | MITIGATED |
| E: Unauthorized command | RBAC per device | MITIGATED |
| Safety: Actuator misuse | Setpoint validation at controller | PARTIALLY MITIGATED |
| S: OTA server spoofing | Certificate pinning | MITIGATED |
```

Ancaman yang "UNMITIGATED" memerlukan risk acceptance atau desain ulang.

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    FIELD_D[Field Devices\nSensor, Actuator\nSecure Boot + Device Cert]
    EDGE[Edge / IoT Gateway\nProtocol translation\nmTLS termination\nCommand auth + rate limit]
    OT_CTRL[OT Control Layer\nPLC, RTU, DCS\nIndustrial FW + DPI\nAudit logging]
    IT_OT_DMZ[IT/OT DMZ\nHistorian\nOT Jump Host\nPatch + vulnerability mgmt]
    CLOUD[Cloud Platform\nIoT Hub / MQTT Broker\nAPI Gateway\nIAM + RBAC\nSIEM + Monitoring]
    MGMT_C[Management Plane\nOut-of-band\nMFA + PAM\nAll access logged]

    FIELD_D <-->|MQTT + TLS 1.3\nmTLS auth| EDGE
    EDGE <-->|Segmented\nIndustrial FW| OT_CTRL
    OT_CTRL <-->|Strict ACL\nData diode for\nhistorian feed| IT_OT_DMZ
    IT_OT_DMZ <-->|HTTPS + token\nvia internet breakout| CLOUD
    MGMT_C -.->|Manages all layers\nout-of-band| EDGE
    MGMT_C -.-> OT_CTRL
    MGMT_C -.-> CLOUD

    CLOUD --> SIEM_CLOUD[SIEM\nLog all layers\nAnomaly detection]
    SIEM_CLOUD --> ALERT2[Alert → IR Team]
```

---

### 6. Contoh Terapan

**Kasus: Rancangan Arsitektur Secure Smart Metering**

**Konteks:** Utilitas gas merancang smart meter deployment untuk 500.000 pelanggan. Meter akan mengirim telemetry konsumsi setiap 15 menit ke platform cloud.

**Keputusan arsitektur utama:**

| Komponen | Keputusan | Justifikasi Keamanan |
|----------|-----------|---------------------|
| Device identity | X.509 cert per meter, injected at manufacturing | Unique identity, revocable, chain of trust |
| Komunikasi meter-gateway | DLMS/COSEM + TLS 1.2, mTLS | Protocol standar smart meter, mutual auth |
| Komunikasi gateway-cloud | HTTPS + MQTT over TLS 1.3 | End-to-end encryption |
| OTA update | Signed package, HTTPS, A/B partition | Integrity, availability, rollback |
| Command authorization | RBAC: utility operator can send setpoint, tidak dapat remote disconnect tanpa second approval | Least privilege, prevent unauthorized disconnect |
| Monitoring | Behavioral baseline per meter, alert untuk abnormal consumption patterns | Detect meter tampering dan cyberattack |

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Merancang Secure Architecture untuk Sistem IoT Pilihan

**Lingkungan:** Kertas dan diagram tool (draw.io, Lucidchart, atau kertas milimeter), referensi framework (NISTIR 8259, IEC 62443, OWASP ISVS)

**Langkah Kerja:**
1. Pilih satu skenario: (a) Smart hospital asset tracking, (b) Industrial cold chain monitoring, (c) Smart city parking management
2. Lakukan requirements analysis: functional, security, regulatory, operational
3. Identifikasi semua komponen sistem dan rancang arsitektur high-level
4. Untuk setiap layer, tentukan kontrol keamanan dengan justifikasi ADR
5. Buat threat model dan petakan setiap ancaman ke kontrol arsitektur
6. Identifikasi gap atau risiko residual yang tidak dapat dihilangkan
7. Dokumentasikan dalam format Architecture Document (menggunakan template Lampiran A)

---

### 8. Latihan Pemahaman

**Soal 1 (Sintesis — C6)**
Jelaskan mengapa arsitektur "flat network" (semua IoT device dalam satu network segment) adalah anti-pattern yang tidak dapat diterima dalam environment CPS/IoT kelas enterprise. Gunakan argument berbasis threat model, bukan hanya best practice generic.

**Soal 2 (Evaluasi — C5)**
Sebuah desainer mengusulkan menggunakan VPN sebagai satu-satunya kontrol keamanan untuk akses remote ke SCADA system. Evaluasi proposal ini: apa yang VPN berikan dan tidak berikan dalam konteks keamanan CPS?

**Soal 3 (Analisis — C4)**
Sebuah arsitektur menggunakan TLS 1.3 untuk semua komunikasi, Secure Boot pada semua device, dan network segmentation. Namun, tidak ada mekanisme revokasi credential yang diimplementasikan. Jelaskan skenario di mana ketiadaan revokasi credential menjadi titik kegagalan kritis.

**Soal 4 (Evaluasi — C5)**
Bandingkan dua pendekatan untuk command authorization: (1) Semua command divalidasi di gateway, (2) Command divalidasi di gateway DAN di controller/PLC. Mana yang lebih aman dan mengapa? Dalam kondisi apa pendekatan (1) mungkin tidak cukup?

**Soal 5 (Sintesis — C6)**
Sebuah sistem CPS memiliki 10.000 sensor yang masing-masing memiliki X.509 certificate dengan masa berlaku 2 tahun. Rancang strategy untuk mengelola lifecycle certificate ini: kapan di-renew, bagaimana direnew, apa yang terjadi jika renewal gagal, dan bagaimana handle device yang offline saat renewal.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Evaluate dan Improve Arsitektur Existing (C5)**

Sebuah perusahaan logistik memiliki sistem cold chain monitoring untuk pengiriman farmasi. Arsitektur saat ini: sensor suhu Bluetooth Low Energy (BLE) → smartphone kurir (sebagai gateway) → API cloud via internet. Semua komunikasi tanpa enkripsi. API cloud hanya diamankan dengan API key statik yang sama untuk semua kurir. Tidak ada monitoring anomali.

*Pertanyaan:*
1. Lakukan threat model pada arsitektur yang ada: identifikasi semua ancaman signifikan
2. Rancang arsitektur yang diperbaiki yang mengatasi semua ancaman yang diidentifikasi
3. Buat ADR untuk tiga keputusan arsitektur terpenting dalam desain baru Anda
4. Identifikasi risiko residual yang tetap ada setelah perbaikan dan bagaimana Anda me-manage-nya

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 5 (Certificate Lifecycle):**
Strategy certificate renewal untuk 10.000 sensor: (1) Staggered expiry — jangan semua expire pada waktu yang sama; saat provisioning, randomize expiry date dalam window 18–24 bulan; (2) Renewal threshold — mulai proses renewal saat 30 hari sebelum expiry (bukan saat sudah expired); (3) Automated renewal — device memulai renewal request secara otomatis ke CA; CA memverifikasi device identity dengan current certificate sebelum issue yang baru; (4) Offline device — jika device tidak terhubung saat renewal: certificate yang expired → device tidak dapat authenticate → alert operator untuk manual intervention atau physical replacement; prevent certificate cliff: operational planning untuk ensure most devices can renew before expiry; (5) Failure handling — jika renewal gagal (CA unreachable): retry dengan exponential backoff; grace period (misal 7 hari) agar certificate expired tetap diterima sementara renewal dicoba; tanpa grace period, 10.000 device bisa serentak offline.

**Kunci Studi Kasus:**
Threat model: (1) BLE sniffing/replay: suhu data dapat diintersep/dimanipulasi; (2) Smartphone sebagai untrusted gateway: kurir dapat memodifikasi data sebelum kirim; (3) API key statik shared: compromise satu kurir → compromise semua; (4) Tidak ada integrity check: tidak dapat membuktikan data tidak dimanipulasi; (5) No monitoring: manipulasi data tidak terdeteksi. Arsitektur baru: BLE dengan enkripsi (BLE 4.2+ dengan LE Secure Connections); gateway app di smartphone dengan device certificate unik per kurir; API per-courier certificate (tidak shared key); signed telemetry dari sensor; cloud verifikasi signature; monitoring untuk anomali suhu dan behavioral baseline. ADR kunci: (1) BLE encryption vs plaintext; (2) per-device cert vs shared API key; (3) signed vs unsigned payload.

---

### 11. Ringkasan Bab

Security architecture adalah sintesis dari semua domain keamanan CPS/IoT dalam satu rancangan kohesif. Prinsip utama: security by design, defense-in-depth, zero trust. Architecture Decision Records mendokumentasikan setiap keputusan dengan konteks, alternatif, dan justifikasi — penting untuk auditability. Threat model vs architecture mapping memastikan setiap ancaman memiliki kontrol yang memitigasinya. Gap analysis mengidentifikasi risiko residual yang perlu risk acceptance. Arsitektur yang baik tidak hanya "secure" tetapi juga maintainable, scalable, dan operable — keamanan yang tidak dapat dioperasikan dengan benar justru menciptakan risiko baru.

---

### 12. Refleksi Profesional

1. Security architecture seringkali dibuat dalam kondisi keterbatasan: budget terbatas, timeline ketat, komponen legacy yang tidak dapat diganti, vendor yang tidak kooperatif. Bagaimana Anda memprioritaskan keputusan arsitektur ketika tidak semua risiko dapat dimitigasi karena constraint? Kriteria apa yang menentukan trade-off antara keamanan ideal dan keamanan yang dapat diimplementasikan?

2. Architecture Decision Records adalah alat untuk akuntabilitas dan pembelajaran. Namun, dalam praktik, ADR sering tidak dibuat atau tidak di-update. Ketika sistem yang dirancang 5 tahun lalu mengalami insiden, keputusan arsitektur asli tidak terdokumentasi sehingga sulit untuk belajar dari insiden. Bagaimana organisasi menciptakan budaya dokumentasi arsitektur yang berkelanjutan?

3. Seorang security architect yang bertanggung jawab atas rancangan sistem CPS yang kemudian mengalami breach — apakah ia memiliki tanggung jawab hukum atau profesional? Di mana batas antara "keputusan arsitektur yang wajar dalam konteks yang ada" versus "kelalaian profesional"? Bagaimana standar profesi (CISSP, CEH, dll.) menetapkan ekspektasi tanggung jawab ini?

---

---

## Bab 14 — Capstone: Validasi Kontrol, Laporan Teknis, dan Presentasi

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: merancang dan menjalankan prosedur validasi kontrol keamanan pada sistem CPS/IoT (C5); menyusun laporan teknis keamanan yang komprehensif, evidence-based, dan dapat diaudit (C5); mengkomunikasikan temuan keamanan kepada audiens teknis dan non-teknis (C5); mengevaluasi kekuatan dan keterbatasan penilaian keamanan yang dilakukan (C5). *Sub-CPMK-5 / CPMK-5 / Eval-5/EAS*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    VALID[Control Validation\n& Technical Reporting]

    VALID --> PLAN_V[Validation Planning]
    PLAN_V --> SCOPE_V[Scope: apa yang divalidasi]
    PLAN_V --> METHOD_V[Methodology: bagaimana]
    PLAN_V --> CRITERIA[Success criteria:\napa yang dianggap "berhasil"]
    PLAN_V --> SAFETY_V[Safety constraints:\napa yang tidak boleh dilakukan]

    VALID --> EXECUTE[Validation Execution]
    EXECUTE --> CONFIG_V[Configuration verification]
    EXECUTE --> DOC_REVIEW[Documentation review]
    EXECUTE --> FUNCTIONAL[Functional testing\ndalam lab berotorisasi]
    EXECUTE --> LOG_REVIEW[Log review & analysis]
    EXECUTE --> INTERVIEW[Interview operator\nand engineers]

    VALID --> REPORT3[Technical Report]
    REPORT3 --> EXEC_SUM[Executive Summary]
    REPORT3 --> FINDINGS3[Findings per control]
    REPORT3 --> EVIDENCE[Evidence artifacts]
    REPORT3 --> REC[Recommendations]
    REPORT3 --> RISK_SUM[Residual risk summary]

    VALID --> PRESENT[Presentation]
    PRESENT --> TECH_AUD[Technical audience:\ndetail dan evidence]
    PRESENT --> MGMT_AUD[Management audience:\nrisk dan business impact]
    PRESENT --> LIMIT[Acknowledge limitations\nof assessment]
```

---

### 3. Pengantar Kontekstual

Merancang kontrol adalah setengah pekerjaan — memvalidasi bahwa kontrol benar-benar berfungsi seperti yang dimaksud adalah setengah lainnya. Security theatre — kontrol yang ada di atas kertas tetapi tidak berfungsi dalam praktik — adalah masalah nyata dalam industri. Laporan teknis yang baik adalah alat komunikasi yang menjembatani antara temuan teknis dan keputusan bisnis. Kemampuan ini — validasi, dokumentasi, dan komunikasi — adalah kompetensi yang membedakan security professional dari junior ke senior.

---

### 4. Landasan Teori

#### 4.1 Control Validation Methodology

**Control Validation vs Penetration Testing:**

| Aspek | Control Validation | Penetration Testing |
|-------|-------------------|---------------------|
| Tujuan | Verifikasi kontrol berfungsi sesuai desain | Temukan apa yang dapat dieksploitasi |
| Pendekatan | Evidence-based review + functional testing | Adversarial simulation |
| Dokumen yang dibutuhkan | Diperlukan (architecture doc, config) | Tidak wajib (black-box) |
| Scope | Spesifik per kontrol | Broad attack surface |
| Output | Pass/Fail per kontrol | List vulnerabilities + exploit paths |
| Akibat pada system | Minimal | Mungkin disruption |
| Untuk CPS/OT | Lebih appropriate | Perlu sangat hati-hati di OT |

**Metode Validasi Kontrol:**

1. **Documentation review:** Apakah kebijakan, prosedur, dan konfigurasi terdokumentasi dan konsisten?
2. **Configuration inspection:** Apakah konfigurasi aktif (yang berjalan) sesuai dengan konfigurasi yang didokumentasikan?
3. **Functional verification:** Apakah kontrol berfungsi sesuai intended purpose? (dalam lab/isolated environment)
4. **Log review:** Apakah kontrol menghasilkan log yang diperlukan? Apakah log tersebut actually dimonitor?
5. **Interview:** Apakah personel yang bertanggung jawab memahami dan dapat mengoperasikan kontrol?

#### 4.2 Evidence Collection dan Chain of Custody

Setiap klaim dalam laporan teknis harus didukung oleh evidence yang dapat diverifikasi.

**Jenis Evidence:**
```
1. Screenshot/screen recording: tampilkan konfigurasi, hasil testing
2. Configuration files: export actual running configuration
3. Log excerpts: tunjukkan log yang membuktikan kontrol berjalan
4. Network captures: packet capture yang menunjukkan enkripsi aktif
5. Command output: output tool validasi (nmap, testssl.sh, nessus)
6. Interview notes: pernyataan dari personel yang diinterview (dengan persetujuan)
```

**Chain of Custody:**
```
Untuk setiap evidence:
- Hash (SHA-256) evidence file saat dikumpulkan
- Catat: siapa yang mengumpulkan, kapan, bagaimana, dari mana
- Simpan di lokasi aman dengan akses terbatas
- Transfer evidence ke penyimpanan akhir: verifikasi hash kembali
```

#### 4.3 Struktur Laporan Teknis Keamanan

```
1. COVER PAGE
   Judul, subjek sistem, tanggal, klasifikasi kerahasiaan, versi

2. EXECUTIVE SUMMARY (1–2 halaman)
   - Tujuan assessment
   - Ringkasan temuan (overall risk rating)
   - Top 3 rekomendasi prioritas
   - Statement bahwa assessment memiliki keterbatasan (scope, waktu)

3. SCOPE DAN METODOLOGI
   - Sistem/komponen yang dinilai
   - Metode validasi yang digunakan
   - Periode assessment
   - Tim assessor
   - Batasan dan asumsi

4. TEMUAN (FINDINGS)
   Untuk setiap temuan:
   - ID (F-001, F-002, ...)
   - Judul
   - Severity (Kritis/Tinggi/Sedang/Rendah)
   - Deskripsi teknis
   - Evidence (dengan referensi ke lampiran)
   - Impact jika tidak dimitigasi
   - Rekomendasi

5. RINGKASAN RISIKO RESIDUAL
   - Tabel semua temuan dengan severity dan status
   - Risk posture statement

6. REKOMENDASI PRIORITAS
   - Prioritas 1: immediate action (Kritis)
   - Prioritas 2: short-term (Tinggi, <30 hari)
   - Prioritas 3: medium-term (Sedang, 30–90 hari)

7. LAMPIRAN
   - Evidence artifacts
   - Tool output
   - Configuration excerpts
   - Daftar referensi standar
```

#### 4.4 Komunikasi kepada Audiens Berbeda

**Kepada tim teknis (engineer, developer, OT specialist):**
- Jelaskan detail teknis secara lengkap
- Berikan command, konfigurasi, tool output
- Hubungkan dengan standar teknis spesifik (RFC, IEC, NIST SP)
- Hormati keahlian mereka — jangan oversimplify

**Kepada manajemen dan non-teknis:**
- Fokus pada business impact dan risiko
- Hindari jargon teknis atau beri penjelasan singkat
- Gunakan analogi yang relatable (rumah, kunci, brankas)
- Sediakan action items yang jelas dengan accountability dan timeline
- Sertakan estimasi cost of inaction vs cost of mitigation

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    KICK[Kickoff Meeting\nScope, rules of engagement,\ncontact persons]
    DOC_COL[Document Collection\nArchitecture, config, policies,\nincident history]
    DOC_REV[Documentation Review\nGap vs stated architecture]
    CONFIG_INS[Configuration Inspection\nActual running config\nvs documented]
    FUNC_TEST[Functional Verification\nin lab / authorized env\nNOT on production live]
    LOG_AUD[Log & Evidence Audit\nAre logs generated?\nAre they monitored?]
    INTERVIEW2[Stakeholder Interviews\nOT engineer, SOC, ops]
    FINDINGS_AGG[Findings Aggregation\nDeduplicate, classify,\nevidence link]
    DRAFT[Draft Report\nInternal review]
    FINDINGS_BRIEF[Findings Briefing\nto client / system owner\nbefore final report]
    FINAL_REP[Final Report\nIncorporating feedback]
    PRESENT2[Presentation\nExec + Technical]
    FOLLOWUP[Follow-up plan\nRemediation tracking]

    KICK --> DOC_COL --> DOC_REV --> CONFIG_INS
    CONFIG_INS --> FUNC_TEST --> LOG_AUD --> INTERVIEW2
    INTERVIEW2 --> FINDINGS_AGG --> DRAFT --> FINDINGS_BRIEF
    FINDINGS_BRIEF --> FINAL_REP --> PRESENT2 --> FOLLOWUP
```

---

### 6. Contoh Terapan

**Kasus: Validasi Kontrol pada Gateway IoT Rumah Sakit**

**Finding F-001 — TLS Configuration (Severity: Tinggi)**

*Deskripsi:* Gateway IoT di RSUD X menggunakan TLS 1.0 dan mengizinkan cipher suite `TLS_RSA_WITH_3DES_EDE_CBC_SHA`. Konfigurasi ini rentan terhadap POODLE (CVE-2014-3566) dan SWEET32 (CVE-2016-2183).

*Evidence:* Lihat Lampiran A — output testssl.sh pada gateway 192.168.10.50 (tanggal 2026-07-10, jam 14:22 WIB, oleh assessor: [nama], hash SHA-256 capture: [hash]).

*Impact:* Data telemetry pasien (heart rate, SpO2) dapat diintersep dan didekripsi oleh attacker dalam network yang sama. Potensi pelanggaran privasi data medis pasien sesuai UU PDP No. 27 Tahun 2022.

*Rekomendasi:* Konfigurasi minimum TLS versi 1.2 (preferably TLS 1.3 only), disable semua cipher suite yang menggunakan DES, 3DES, RC4, dan NULL. Rujuk konfigurasi yang direkomendasikan dalam Lampiran B.

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Penyusunan Laporan Validasi Kontrol

**Lingkungan:** Hasil dari praktikum Bab 7, 8, 9, 10, dan 11; template laporan teknis (Lampiran C dan F); tidak memerlukan sistem tambahan

**Langkah Kerja:**
1. Kumpulkan semua evidence dari praktikum sebelumnya
2. Tulis satu laporan teknis komprehensif yang mencakup semua temuan dari praktikum Bab 7–11
3. Buat Executive Summary maksimal 1 halaman untuk audiens manajemen
4. Buat tabel prioritas remediasi dengan estimasi effort dan impact
5. Siapkan presentasi 10 menit: 5 menit versi teknis, 5 menit versi manajemen (untuk audiens yang berbeda)
6. Peer review: tukar laporan dengan kelompok lain dan berikan feedback menggunakan rubrik di Lampiran F

---

### 8. Latihan Pemahaman

**Soal 1 (Evaluasi — C5)**
Sebuah laporan keamanan menyatakan: "Tidak ditemukan kelemahan kritis." Evaluasi pernyataan ini — apa yang diperlukan untuk memvalidasi klaim ini, dan apa keterbatasan yang harus selalu disebutkan dalam pernyataan seperti ini?

**Soal 2 (Analisis — C4)**
Seorang assessor menemukan bahwa firewall rules yang terdokumentasi berbeda dari firewall rules yang aktual (running configuration). Apa implikasi dari discrepancy ini, dan bagaimana ini harus dilaporkan?

**Soal 3 (Evaluasi — C5)**
Executive summary laporan keamanan mencantumkan 27 findings. Seorang CISO meminta Anda merangkumnya menjadi 3 poin untuk presentasi board. Bagaimana Anda memilih 3 poin tersebut, dan informasi apa yang tidak boleh dihilangkan meskipun diringkas?

**Soal 4 (Analisis — C4)**
Seorang engineer OT menolak salah satu rekomendasi laporan Anda dengan argumen bahwa perubahan tersebut akan mengharuskan downtime 8 jam pada sistem produksi yang beroperasi 24/7. Bagaimana Anda merespons penolakan ini secara profesional?

**Soal 5 (Sintesis — C6)**
Jelaskan mengapa "functional testing" dalam control validation harus dilakukan di lingkungan lab atau isolated environment, bukan langsung pada sistem production CPS/OT. Apa risiko spesifik dari testing pada production system?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — EAS (Evaluasi Akhir Semester): Security Assessment CPS/IoT Komprehensif**

*Konteks:* Anda adalah tim security consultant yang diminta oleh sebuah perusahaan logistik untuk melakukan security assessment terhadap sistem manajemen cold chain mereka. Sistem mencakup: 2.000 sensor suhu BLE, 50 gateway Raspberry Pi, cloud platform AWS IoT Core, API management, dan monitoring dashboard untuk tim QA.

*Tugas:*
1. **Asset Inventory & Architecture** (20%): Buat architecture diagram dan asset inventory dengan criticality rating
2. **Threat Model** (20%): Lakukan STRIDE threat modelling, identifikasi minimal 10 ancaman signifikan
3. **Risk Register** (20%): Buat risk register lengkap dengan scoring dan prioritasi
4. **Control Design** (20%): Rancang kontrol untuk semua risiko kritis dan tinggi
5. **Validation Plan** (10%): Rancang rencana validasi kontrol (tidak perlu dieksekusi, cukup rancangan)
6. **Technical Report** (10%): Susun laporan teknis dengan executive summary dan findings

*Deliverable:* Laporan tertulis (maksimal 30 halaman) + presentasi 20 menit

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 1 (Evaluasi Klaim "No Critical Findings"):**
Klaim "tidak ditemukan kelemahan kritis" harus selalu disertai dengan: (1) Definisi "kritis" yang jelas (berdasarkan scoring framework apa?); (2) Scope yang jelas: sistem apa, komponen apa, metode apa yang digunakan; (3) Keterbatasan: "temuan berlaku untuk kondisi pada waktu assessment, dalam scope yang didefinisikan; kemungkinan terdapat kelemahan yang tidak teridentifikasi karena keterbatasan waktu, akses, dan metodologi"; (4) Evidence: apa yang diuji, tool apa yang digunakan, periode testing; (5) Perbedaan antara "not found" dan "not present" — absence of evidence ≠ evidence of absence. Klaim tanpa caveat ini adalah misleading dan dapat menciptakan false sense of security.

**Kunci Soal 4 (Menangani Penolakan Rekomendasi):**
Langkah profesional: (1) Akui legitimasi concern operasional — 8 jam downtime adalah concern nyata, bukan alasan yang tidak valid; (2) Explore alternative mitigations yang tidak memerlukan downtime: apakah ada compensating control? (misalnya: tambahkan monitoring khusus untuk ancaman yang dimitigasi rekomendasi tersebut); (3) Quantify risk: bantu engineer memahami probability dan impact insiden jika rekomendasi tidak diimplementasikan; (4) Propose scheduling: apakah dapat dilakukan selama planned maintenance window?; (5) Escalate jika perlu: jika risiko terlalu tinggi untuk dibiarkan, eskalasi ke manajemen dengan informasi yang objektif — bukan untuk memenangkan argumen, tetapi untuk memastikan risk acceptance dilakukan secara sadar oleh pihak yang berwenang; (6) Dokumentasikan: catat dalam laporan bahwa rekomendasi ini ditolak oleh system owner, beserta alasannya.

---

### 11. Ringkasan Bab

Control validation memastikan kontrol yang dirancang benar-benar berfungsi — bukan sekadar ada di atas kertas. Metodologi validasi mencakup: documentation review, configuration inspection, functional verification (lab/isolated), log review, dan stakeholder interview. Setiap klaim dalam laporan harus didukung evidence dengan chain of custody yang jelas. Laporan teknis yang efektif memiliki struktur yang jelas: executive summary, findings dengan evidence, dan rekomendasi prioritas. Komunikasi kepada audiens teknis vs manajemen memerlukan adaptasi pesan — keduanya sama pentingnya. Keterbatasan assessment harus selalu diakui secara eksplisit — laporan yang mengklaim "comprehensive" tanpa caveat adalah laporan yang misleading.

---

### 12. Refleksi Profesional

1. Sebuah laporan keamanan yang menemukan banyak kelemahan kritis dapat mempermalukan tim OT dan manajemen yang selama ini percaya sistem mereka aman. Bagaimana Anda menyampaikan temuan yang keras dengan cara yang konstruktif dan mendorong perbaikan, bukan defensiveness dan blame?

2. Sebagai external assessor, Anda mungkin menemukan kelemahan yang sudah diketahui oleh internal team tetapi tidak pernah diatasi karena berbagai alasan (budget, prioritas, politik). Apakah Anda berkewajiban untuk melaporkan temuan ini dengan cara yang "memaksa" tindakan, atau cukup mendokumentasikan dan menyerahkan keputusan kepada manajemen?

3. Laporan keamanan yang tidak di-followup (rekomendasi tidak diimplementasikan) adalah situasi yang umum. Sebagai konsultan atau internal security team, apa kewajiban Anda jika rekomendasi Anda diabaikan dan kemudian terjadi insiden yang dapat diprediksi? Bagaimana dokumentasi yang benar melindungi Anda secara profesional dan hukum?

---

---

## Bab 15 — OT Security, ICS/SCADA, dan Industrial IoT Convergence

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: menjelaskan karakteristik khusus keamanan OT/ICS/SCADA yang membedakannya dari IT security (C2); menganalisis ancaman dan insiden historis pada infrastruktur kritis OT (C4); mengevaluasi framework standar OT security (IEC 62443, NERC CIP, NIST SP 800-82) dan relevansinya (C5); merancang pendekatan security assessment untuk lingkungan ICS yang mempertimbangkan safety dan availability (C5). *Pengayaan — tanpa evaluasi formal*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    OT_SEC[OT/ICS/SCADA Security]

    OT_SEC --> CHAR[OT Characteristics]
    CHAR --> LONGLIFE[Long lifecycle:\n20-30 tahun]
    CHAR --> AVAIL_FIRST[Availability first:\nuptime > patch]
    CHAR --> LEGACY[Legacy protocols:\nModbus, DNP3, Profibus]
    CHAR --> SAFETY2[Safety systems:\nSIS, SIL requirements]

    OT_SEC --> INCIDENTS[Historical Incidents]
    INCIDENTS --> STUXNET[Stuxnet 2010:\nIranian centrifuges]
    INCIDENTS --> UKRAINE[Ukraine Power Grid\n2015-2016]
    INCIDENTS --> TRITON[TRITON/TRISIS 2017:\nSafety system attack]
    INCIDENTS --> COLONIAL[Colonial Pipeline 2021:\nRansomware IT → OT]

    OT_SEC --> FRAMEWORKS2[Frameworks]
    FRAMEWORKS2 --> IEC62443B[IEC 62443:\nISA/IEC IACS]
    FRAMEWORKS2 --> NERCCIP[NERC CIP:\nElectric grid]
    FRAMEWORKS2 --> NIST80082[NIST SP 800-82:\nICS security guide]
    FRAMEWORKS2 --> CISA_GUIDE[CISA ICS advisories\nand guidelines]

    OT_SEC --> IIoT[Industrial IoT\nConvergence]
    IIoT --> EDGE2[Edge computing\nin OT environment]
    IIoT --> DIGITAL_TWIN2[Digital twin\nsecurity implications]
    IIoT --> PREDICTIVE[Predictive maintenance\ndata exposure risk]
```

---

### 3. Pengantar Kontekstual

OT security adalah domain yang selama puluhan tahun beroperasi dalam paradigma "air-gapped and safe" — sistem industri yang tidak terhubung ke internet dianggap aman dari ancaman siber. Paradigma ini runtuh secara dramatis pada 2010 dengan Stuxnet, yang menunjukkan bahwa air gap dapat ditembus melalui USB. Sejak itu, digitalisasi industri (Industri 4.0, IIoT) semakin menghubungkan OT ke IT dan internet, menciptakan attack surface yang sebelumnya tidak ada.

---

### 4. Landasan Teori

#### 4.1 Karakteristik Khusus OT/ICS

**Perbedaan fundamental OT vs IT:**

| Karakteristik | IT | OT/ICS |
|--------------|-----|--------|
| Prioritas keamanan | CIA (Confidentiality first) | AIC (Availability first) |
| Lifecycle perangkat | 3–5 tahun | 15–30 tahun |
| Patch cadence | Reguler (bulanan/mingguan) | Sangat lambat atau tidak pernah |
| Testing sebelum patch | Minimal | Extensive (takut downtime) |
| Waktu response terhadap insiden | Toleran terhadap downtime sementara | Setiap menit downtime = kerugian besar atau bahaya |
| Real-time requirements | Tidak kritis | Sangat kritis (microsecond untuk safety) |
| Antivirus/EDR | Standar | Sering tidak kompatibel dengan OT system |
| OS | Modern, regularly updated | Windows XP, Windows CE, RTOS proprietary |

#### 4.2 Insiden Historis Kritis — Pelajaran dari Lapangan

**Stuxnet (2010) — Serangan terhadap Sentrifus Pengayaan Uranium Iran:**
- Metode penyebaran: USB drive, jaringan Windows
- Target spesifik: PLC Siemens S7-315 yang mengontrol frekuensi inverter
- Efek: mengubah kecepatan sentrifus di luar parameter normal sambil menampilkan data normal ke operator
- Pelajaran: air gap tidak absolute; serangan dapat sangat targeted; OT dapat diserang tanpa kerusakan fisik langsung yang segera terlihat

**Ukraine Power Grid (Desember 2015 & 2016):**
- 2015: Spear-phishing → SCADA compromise → remote disconnection 30 substations → 225.000 pelanggan tanpa listrik
- 2016: Industroyer/CRASHOVERRIDE malware → serangan lebih sophisticated, protokol IEC 104, IEC 61850
- Pelajaran: attacker mempelajari protokol ICS; remote access yang tidak aman adalah vector utama; operational procedures (manual override) penting sebagai fallback

**TRITON/TRISIS (2017) — Serangan terhadap Safety Instrumented System:**
- Target: Schneider Electric Triconex Safety Instrumented System (SIS) di fasilitas petrokimia Timur Tengah
- Tujuan: disable SIS agar jika sabotage terjadi, sistem safety tidak merespons → potensi ledakan/katastrofe
- Dampak aktual: SIS masuk ke fail-safe mode (inadvertent), mencegah produksi → insiden terdeteksi
- Pelajaran: attacker mulai menarget safety systems, bukan hanya SCADA; ini adalah eskalasi sangat serius

**Colonial Pipeline (Mei 2021):**
- Entry: VPN account dengan credential yang dikompromis, tanpa MFA
- Serangan: ransomware DarkSide pada jaringan IT billing
- Keputusan: Colonial Pipeline secara proaktif shutdown OT (pipeline) karena tidak dapat mengkonfirmasi apakah OT juga terinfeksi
- Dampak: 5.500 mil pipeline berhenti selama 6 hari; shortage BBM di East Coast AS
- Pelajaran: insiden IT dapat menyebabkan shutdown OT; IT-OT convergence menciptakan risk baru; MFA adalah kontrol dasar yang non-negotiable

#### 4.3 Framework OT Security

**IEC 62443 — Kerangka IACS:**
```
IEC 62443 terdiri dari series dokumen:
- 62443-1-x: General (konsep, terminologi)
- 62443-2-x: Policies & procedures (untuk operator dan integrator)
- 62443-3-x: System level (security risk assessment, system design)
- 62443-4-x: Component level (product development requirements)

Security Level (SL):
SL 1: Casual attacker (script kiddie)
SL 2: Intentional violation, simple means
SL 3: Sophisticated attacker, ICS knowledge
SL 4: State-sponsored, extended resources
```

**NERC CIP (Critical Infrastructure Protection) — Electric Grid:**
NERC CIP adalah standar wajib untuk grid listrik di Amerika Utara. Mencakup:
- CIP-002: BES Cyber System Categorization
- CIP-005: Electronic Security Perimeters
- CIP-007: System Security Management
- CIP-010: Configuration Management and Vulnerability Management

**NIST SP 800-82 Rev. 3 (2023) — Guide to OT Security:**
Panduan komprehensif NIST untuk OT security, mencakup: threat landscape, architecture, controls, dan incident response untuk ICS/SCADA.

#### 4.4 Industrial IoT Convergence — Security Implications

**Edge Computing dalam OT:**
```
Traditional OT: data processing di controller lokal atau historian
IIoT + Edge: data processing di edge nodes yang lebih powerful,
             terhubung ke cloud untuk analytics

Security implication:
- Edge nodes memiliki lebih banyak software → lebih besar attack surface
- Edge nodes terhubung ke cloud → jika kompromis, bridge antara OT dan cloud
- Edge container orchestration (K3s, edge Kubernetes) → new attack vectors
```

**Predictive Maintenance dan Data Exposure:**
Sensor data yang dikumpulkan untuk predictive maintenance dapat mengungkapkan informasi sensitif:
- Production volumes dan schedule
- Machine utilization (competitive intelligence)
- Quality issues (reputational)
- Jika data ini dikirim ke cloud vendor pihak ketiga → supply chain risk

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    CORP_NET[Corporate Network\nIT: ERP, Email, Office]
    CORP_FW[Corporate Firewall]
    HIST_DMZ[Historian DMZ\nData aggregation\nRemote access jump host]
    OT_FW2[OT Boundary Firewall\nDeep Packet Inspection\nIEC 62443 zona]
    CTRL_ROOM[Control Room Network\nHMI, Engineering WS\nOT Management]
    SAFETY[Safety Layer\nSIS — Safety Instrumented\nSystem: AIR GAPPED\nfrom SCADA]
    PLC_LEVEL[Process Control\nPLC, DCS, RTU\nSegmented per zone]
    FIELD2[Field Devices\nSensor, Actuator\nValve, Motor]
    EDGE_NODE[Edge Node\nIIoT Analytics\nPredictive Maintenance]
    CLOUD2[Cloud Platform\nAnalytics, Monitoring\nRemote diagnostics]

    CORP_NET <-->|Controlled exchange| CORP_FW
    CORP_FW <-->|Historian only\nData diode for read| HIST_DMZ
    HIST_DMZ <-->|Strictly controlled| OT_FW2
    OT_FW2 <-->|OT management\nauthorized personnel| CTRL_ROOM
    CTRL_ROOM <-->|Approved protocols\nDNP3, OPC-UA| PLC_LEVEL
    PLC_LEVEL <-->| | FIELD2
    SAFETY -.->|Physically isolated\nfrom SCADA| PLC_LEVEL

    FIELD2 --> EDGE_NODE
    EDGE_NODE -->|Encrypted, authenticated\ntelemetry only| CLOUD2
```

---

### 6. Contoh Terapan

**Kasus: IIoT Deployment di Fasilitas Manufaktur — Risk Assessment**

Sebuah pabrik otomotif mengimplementasikan predictive maintenance menggunakan vibration sensor pada 500 mesin CNC. Data dikirim ke cloud AI platform vendor.

**Risiko yang diidentifikasi:**
1. **Data sovereignty:** Data produksi dikirim ke vendor cloud di luar negeri — implikasi regulasi dan competitive
2. **Vendor access:** Vendor platform memerlukan akses untuk debugging → potential backdoor
3. **OT-cloud bridge:** Edge node yang menghubungkan OT dan cloud menjadi target kritis
4. **Data manipulation:** Jika attacker mengkompromis edge node, dapat inject false sensor data → predictive maintenance salah → unplanned downtime atau kerusakan mesin

**Kontrol yang diterapkan:**
- Data aggregation dan anonymization di edge sebelum dikirim ke cloud
- Vendor contractually prohibited dari mengakses raw production data
- Edge node dalam VLAN terpisah, tidak dapat berkomunikasi langsung ke PLC
- Monitoring: behavioral baseline untuk edge node traffic

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Analisis Insiden Historis OT dan Lesson Learned

**Lingkungan:** Laporan insiden publik (ICS-CERT advisories, CISA reports, akademik paper tentang Stuxnet, Ukraine, TRITON); tidak memerlukan akses sistem nyata

**Langkah Kerja:**
1. Pilih satu insiden OT historis dari daftar yang disediakan dosen
2. Analisis: entry point, attack path, dampak, dan response
3. Petakan setiap tahap serangan ke MITRE ATT&CK for ICS framework
4. Identifikasi: kontrol keamanan apa yang, jika ada, dapat mencegah atau mendeteksi insiden ini lebih awal?
5. Buat laporan lessons learned dengan rekomendasi untuk sistem serupa di Indonesia

---

### 8. Latihan Pemahaman

**Soal 1 (Analisis — C4)**
Jelaskan mengapa patch management yang rutin (patch setiap bulan seperti di IT) tidak dapat langsung diterapkan pada sistem OT/ICS. Faktor teknis dan operasional apa yang membuat patch OT sangat kompleks?

**Soal 2 (Evaluasi — C5)**
Insiden Colonial Pipeline (2021) menunjukkan bahwa keputusan untuk shutdown OT dibuat secara proaktif oleh perusahaan, bukan karena OT sendiri diserang. Evaluasi keputusan ini: apakah ini merupakan respons yang tepat? Apa alternatif yang mungkin?

**Soal 3 (Analisis — C4)**
TRITON/TRISIS menarget Safety Instrumented System (SIS), bukan SCADA atau PLC. Mengapa menarget SIS dianggap sebagai eskalasi yang sangat serius dibandingkan menarget SCADA?

**Soal 4 (Evaluasi — C5)**
Sebuah operator utilitas mengklaim bahwa sistem SCADA mereka "aman karena tidak terhubung ke internet." Berikan minimal tiga skenario serangan yang dapat terjadi bahkan pada sistem SCADA yang benar-benar air-gapped.

**Soal 5 (Sintesis — C6)**
IEC 62443 mendefinisikan Security Level 4 sebagai proteksi terhadap "state-sponsored attacker with extended resources." Apakah SL 4 realistic untuk dicapai oleh operator infrastruktur kritis skala menengah? Apa trade-off yang harus dipertimbangkan?

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Security Assessment Plan untuk ICS Pembangkit Listrik (C4–C5)**

Sebuah pembangkit listrik tenaga gas berencana melakukan security assessment menyeluruh terhadap sistem SCADA mereka sebelum program modernisasi. Sistem saat ini: DCS dari vendor tunggal (berusia 12 tahun), Modbus TCP untuk komunikasi internal, HMI berbasis Windows 7 (end-of-life), koneksi remote access via modem dial-up, dan SIS yang terpisah secara fisik dari DCS.

*Pertanyaan:*
1. Rancang assessment plan yang mempertimbangkan safety dan availability — metode apa yang dapat dan tidak dapat digunakan?
2. Identifikasi risiko tertinggi berdasarkan deskripsi sistem, sebelum assessment dimulai
3. Bagaimana Anda akan menyesuaikan rekomendasi Anda mengingat OS end-of-life (Windows 7) yang tidak dapat di-upgrade karena ketergantungan pada DCS software?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 4 (Air-Gapped SCADA Attack Vectors):**
(1) USB/removable media: Stuxnet adalah contoh klasik — malware disebarkan via USB drive yang dibawa oleh insinyur/vendor; (2) Supply chain attack: vendor firmware atau software update yang dikompromis sebelum sampai ke fasilitas; (3) Insider threat: operator atau kontraktor dengan akses fisik dapat membawa perangkat berbahaya atau secara langsung memodifikasi konfigurasi; (4) Engineering workstation: laptop insinyur yang membawa virus dari jaringan rumah/kantor dan dihubungkan ke SCADA saat maintenance; (5) Radio frequency attack: beberapa sistem SCADA menggunakan komunikasi radio (Radio Serial Protocol) yang dapat diintersep atau di-jam; (6) Social engineering: menipu operator untuk menjalankan tindakan berbahaya yang tampak legitimate. Kesimpulan: air gap tidak pernah absolute — physical vectors tetap ada dan sering dieksploitasi.

**Kunci Studi Kasus:**
Assessment methods yang aman: documentation review, configuration inspection (export, tidak live), interview operator, network diagram review, log review. Yang TIDAK boleh dilakukan: active scanning pada DCS (dapat menyebabkan malfunction), functional testing pada production system. Risiko tertinggi pra-assessment: Windows 7 EoL (unpatched vulnerabilities), modem dial-up (unencrypted, brute-force, potential legacy vulnerability), Modbus tanpa auth (semua perangkat dalam network dapat kirim command), single-vendor dependency (supply chain risk). Windows 7 mitigation tanpa upgrade: application whitelisting (hanya jalankan approved executables), network isolation ketat (HMI tidak dapat akses internet sama sekali), tambahkan monitoring host-based (EDR yang kompatibel dengan WinXP/7), backup lebih sering, rencana migrasi jangka menengah.

---

### 11. Ringkasan Bab

OT/ICS security berbeda fundamental dari IT security: availability mendahului confidentiality, lifecycle sangat panjang, patch sangat sulit, dan dampak fisik nyata. Insiden historis (Stuxnet, Ukraine, TRITON, Colonial Pipeline) mengajarkan bahwa: air gap tidak absolute, safety systems adalah target, dan IT-OT convergence menciptakan risiko baru. Framework utama: IEC 62443 (universal IACS), NERC CIP (electric grid), NIST SP 800-82. IIoT convergence membawa manfaat (predictive maintenance, efficiency) sekaligus risiko baru (edge as OT-cloud bridge, data exposure). Assessment OT memerlukan pendekatan khusus yang mengedepankan safety — tidak semua metode IT assessment dapat diterapkan langsung pada OT.

---

### 12. Refleksi Profesional

1. Industri manufaktur dan energi di Indonesia semakin mengadopsi IIoT untuk efisiensi. Namun, sebagian besar insinyur OT Indonesia belum terekspos pada konsep cybersecurity ICS. Sebagai security professional dengan keahlian di bidang ini, apa peran Anda dalam membangun kapasitas keamanan OT di Indonesia — melampaui sekadar audit dan consulting?

2. Insiden TRITON menunjukkan bahwa attacker bersedia menghabiskan waktu bertahun-tahun untuk mempelajari sistem safety industri sebelum menyerang. Ini bukan lagi domain hacker biasa — ini adalah ancaman setara nation-state. Apakah operator infrastruktur kritis swasta memiliki kemampuan dan sumber daya yang memadai untuk menghadapi ancaman ini, atau apakah ini harus menjadi tanggung jawab negara?

3. Standar keamanan OT (IEC 62443, NERC CIP) sangat detail dan memerlukan investasi signifikan untuk implementasi. Banyak operator infrastruktur kritis di negara berkembang tidak memiliki resources untuk compliance penuh. Bagaimana regulator dan industri harus mendekati prioritasi standar keamanan dalam konteks keterbatasan resources ini?

---

---

## Bab 16 — Tren CPS/IoT Security: Edge, Digital Twin, Medical IoT, dan Smart City

### 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu: mengidentifikasi tren teknologi CPS/IoT yang membawa implikasi keamanan signifikan (C4); menganalisis tantangan keamanan khusus pada domain Medical IoT, Smart City, dan Edge Computing (C4); mengevaluasi pendekatan keamanan untuk Digital Twin dan sistem AI-enabled CPS (C5); merumuskan agenda penelitian dan pengembangan keamanan CPS/IoT yang relevan (C5). *Pengayaan — tanpa evaluasi formal*

---

### 2. Peta Konsep Bab

```mermaid
flowchart TD
    TRENDS[Emerging Trends\nCPS/IoT Security]

    TRENDS --> EDGE3[Edge & Fog Computing]
    EDGE3 --> EDGE_ATTACK[Edge as attack pivot]
    EDGE3 --> CONTAINER_OT[Container security\nin OT edge]
    EDGE3 --> PRIVACY_EDGE[Privacy at edge:\ndata minimization]

    TRENDS --> DT[Digital Twin Security]
    DT --> DT_SYNC[Sync integrity:\ntwin vs physical]
    DT --> DT_ATTACK[Attack via twin:\nsimulation manipulation]
    DT --> DT_DATA[Sensitive operational\ndata in twin]

    TRENDS --> MEDICAL[Medical IoT\nIoMT]
    MEDICAL --> FDA_GUIDE[FDA cybersecurity\nguidance 2023]
    MEDICAL --> PATIENT[Patient safety\nas primary concern]
    MEDICAL --> LEGACY_MED[Legacy medical device\nsecurity challenges]

    TRENDS --> SMARTCITY[Smart City]
    SMARTCITY --> INFRA_CONV[Infrastructure convergence:\ntransport, energy, water]
    SMARTCITY --> PRIVACY3[Mass surveillance\nprivacy concerns]
    SMARTCITY --> CASCADE[Cascade failure risk\nacross domains]

    TRENDS --> PQC[Post-Quantum\nCryptography]
    PQC --> NIST_PQC[NIST PQC standards:\nML-KEM, ML-DSA]
    PQC --> HARVEST[Harvest now,\ndecrypt later threat]
    PQC --> MIGRATION[Migration timeline\nfor IoT devices]
```

---

### 3. Pengantar Kontekstual

Keamanan CPS/IoT bukan bidang yang statis. Teknologi terus berevolusi — edge computing membawa komputasi lebih dekat ke perangkat, digital twin menciptakan representasi virtual sistem fisik, medical devices semakin terhubung, dan kota-kota membangun infrastruktur smart yang terintegrasi. Setiap tren ini membawa opportunity sekaligus risiko baru yang memerlukan pemikiran keamanan yang adaptif. Bab ini mempersiapkan mahasiswa untuk menghadapi lanskap CPS/IoT security yang akan mereka temui dalam 5–10 tahun ke depan.

---

### 4. Landasan Teori

#### 4.1 Edge Computing Security

**Edge Computing dalam CPS/IoT:**
Edge computing memindahkan komputasi dari cloud ke node yang lebih dekat dengan sumber data. Untuk IoT: ini berarti pemrosesan data di gateway, edge server di fasilitas, atau bahkan di device itu sendiri.

**Implikasi Keamanan Edge:**
```
Tantangan:
1. Edge node sering di lingkungan fisik yang kurang aman (outdoor, unmanned facility)
2. Edge node memiliki lebih banyak software dan attack surface vs sensor sederhana
3. Edge node menjadi "bridge" antara OT/field dan cloud — jika dikompromis,
   menjadi pivot untuk lateral movement ke kedua arah
4. Container orchestration di edge (K3s, MicroK8s) = new attack surface
5. Edge software update management = tantangan tersendiri

Kontrol:
- Physical security: tamper detection, secure enclosure
- Software hardening: minimal footprint, container scanning
- Network: mTLS untuk semua koneksi edge, micro-segmentation
- Monitoring: behavioral baseline untuk edge traffic
- Update: signed container images, automated patching
```

**Privacy at the Edge:**
Edge computing memungkinkan "privacy by design" yang lebih baik:
```
Traditional: sensor data → cloud → analytics
Edge: sensor data → local analytics → only insights to cloud
                    (raw data tidak pernah meninggalkan fasilitas)

Manfaat: raw data sensitif (biometrik, aktivitas operasional) tidak dikirim ke cloud
Tantangan: ensures edge analytics tidak dapat di-bypass atau dimanipulasi
```

#### 4.2 Digital Twin Security

**Apa itu Digital Twin dalam CPS:**
Digital twin adalah representasi virtual dari sistem fisik yang terus diperbarui dengan data real-time dari sistem nyata. Digunakan untuk: monitoring, simulasi, predictive analytics, dan desain.

**Ancaman Khusus Digital Twin:**
```
1. Twin data manipulation:
   Jika attacker dapat memanipulasi data yang masuk ke twin,
   simulasi dan keputusan berbasis twin akan salah.
   Contoh: memalsukan sensor data → twin menunjukkan semua normal
           → kondisi berbahaya tidak terdeteksi

2. Sensitive operational data:
   Digital twin mengandung data sangat sensitif tentang sistem nyata:
   topologi, kapasitas, parameter operasional, vulnerabilities.
   Jika bocor → roadmap serangan untuk attacker.

3. Reverse engineering via twin:
   Attacker dapat mempelajari perilaku sistem nyata melalui twin
   tanpa perlu akses fisik ke sistem.

4. Attack simulation:
   Twin dapat digunakan untuk simulate attack scenario sebelum
   melancarkannya ke sistem nyata.
```

**Mitigasi:**
- Akses twin sangat terbatas (zero trust, need-to-know)
- Data integrity: twin harus memverifikasi authenticity sensor data
- Air-gap antara production twin dan non-production twin
- Monitoring akses ke twin

#### 4.3 Medical IoT (IoMT) Security

**Karakteristik khusus Medical IoT:**
```
Perangkat: infusion pump, pacemaker, ventilator, patient monitor,
           MRI, CT scanner, surgical robot, glucometer

Karakteristik keamanan unik:
1. Patient safety adalah paramount — kesalahan dapat berakibat fatal
2. FDA regulatory: pre-market dan post-market cybersecurity requirements
3. Lifecycle sangat panjang: perangkat medical sering digunakan 10–20 tahun
4. Patch sangat sulit: memerlukan FDA re-clearance untuk perubahan software
5. Availability kritis: device sedang digunakan untuk pasien — tidak bisa
   reboot sembarangan
6. HIPAA (AS) / UU PDP (Indonesia): data pasien sangat sensitif
```

**FDA Cybersecurity Guidance (2023):**
Untuk perangkat medical baru yang submit FDA clearance, wajib:
- Cybersecurity plan yang komprehensif (Software Bill of Materials)
- Patches dan updates yang dapat diberikan post-market
- Disclosure dan transparency tentang known vulnerabilities

**Serangan nyata pada Medical IoT:**
- 2019: FDA advisory pada Medtronic insulin pump — remotely controllable, no auth
- 2020: ransomware pada Universal Health Services (US) — 400 rumah sakit terdampak
- Pacemaker vulnerabilities: demonstrasi akses unauthorized oleh peneliti (Barnaby Jack, 2012)

#### 4.4 Smart City Security

**Konvergensi infrastruktur dalam Smart City:**
```
Smart City mengintegrasikan:
- Transportasi: traffic light, smart parking, autonomous vehicle infra
- Energi: smart grid, EV charging, distributed energy
- Air: smart water management, flood monitoring
- Keamanan publik: CCTV, emergency services, gunshot detection
- Lingkungan: air quality, waste management
- Komunikasi: LoRaWAN, NB-IoT, 5G URLLC
```

**Risiko Cascade Failure:**
```
Dalam smart city yang highly integrated:
- Serangan pada satu domain dapat cascade ke domain lain
Contoh:
  - Serangan traffic management → kemacetan → ambulans terlambat
  - Serangan grid listrik → charging station EV down → transportasi disrupted
  - Serangan water management → kualitas air tidak terpantau → kesehatan publik

Defense: domain isolation adalah krusial — sistem yang terpengaruh
         tidak boleh menarik sistem lain ke bawah bersamanya
```

**Privasi Massal dan Surveillance:**
Smart city mengumpulkan data dalam skala masif: CCTV dengan facial recognition, lokasi kendaraan, pola pergerakan individu. Ini menciptakan risiko:
- Data breach pada sistem smart city → privacy breach massal
- Potential misuse oleh pemerintah atau korporasi (mass surveillance)
- UU PDP Indonesia No. 27 Tahun 2022: pengumpulan data personal harus berdasar consent, proportional, dan purpose-limited

#### 4.5 Post-Quantum Cryptography (PQC) untuk IoT

**Ancaman Quantum Computing:**
Komputer quantum dengan cukup qubit dapat memecahkan RSA dan ECC — algoritma kriptografi yang digunakan hampir semua sistem keamanan saat ini. "Harvest now, decrypt later": attacker mengumpulkan encrypted traffic hari ini dan akan mendekripsinya ketika quantum computer tersedia.

**NIST PQC Standards (2024):**
```
NIST telah menetapkan standar PQC:
- ML-KEM (CRYSTALS-Kyber): Key Encapsulation Mechanism
- ML-DSA (CRYSTALS-Dilithium): Digital Signature
- SLH-DSA (SPHINCS+): Stateless Hash-based Signature

Untuk IoT:
- ML-KEM dan ML-DSA memerlukan lebih banyak resources dari RSA/ECC
- Lightweight PQC sedang dalam penelitian
- Timeline: mulai migrasi bertahap, terutama untuk data dengan sensitivity tinggi
  dan perangkat dengan lifecycle panjang (medical, industrial)
```

**Implikasi untuk CPS/IoT:**
Perangkat IoT yang di-deploy hari ini dengan lifecycle 15-20 tahun mungkin beroperasi saat quantum computing threats menjadi nyata. Perencanaan crypto agility diperlukan sekarang.

---

### 5. Model atau Arsitektur

```mermaid
flowchart TD
    SMART_CITY_ARCH[Smart City\nSecurity Architecture]

    SMART_CITY_ARCH --> DOMAIN_ISOLATION[Domain Isolation\nTransport / Energy / Water\nindependent networks]
    SMART_CITY_ARCH --> SHARED_SOC[Shared City SOC\nCross-domain monitoring]
    SMART_CITY_ARCH --> DATA_GOV[Data Governance\nPDP compliance, consent,\npurpose limitation]

    DOMAIN_ISOLATION --> TRANSPORT_D[Transport Network\nTraffic, Parking, EV]
    DOMAIN_ISOLATION --> ENERGY_D[Energy Network\nSmart Grid, Renewables]
    DOMAIN_ISOLATION --> WATER_D[Water Network\nDistribution, Quality]
    DOMAIN_ISOLATION --> SAFETY_D[Public Safety\nEmergency services]

    SHARED_SOC -->|Read-only\ncross-domain telemetry| TRANSPORT_D
    SHARED_SOC -->|Read-only| ENERGY_D
    SHARED_SOC -->|Read-only| WATER_D
    SHARED_SOC -->|Read-only| SAFETY_D

    SHARED_SOC --> CORRELATION[Cross-domain\ncorrelation\nDetect cascade threats]
    CORRELATION --> ALERT3[Alert &\nCity IR Team]
```

---

### 6. Contoh Terapan

**Kasus: Security Assessment untuk Infrastruktur Smart City**

Sebuah kota besar berencana mengintegrasikan: 10.000 CCTV dengan AI analytics, 5.000 sensor lingkungan (udara, suara, cuaca), smart traffic light di 500 persimpangan, dan sistem manajemen parkir. Semua terhubung ke City Operations Center via 5G dan fiber.

**Isu keamanan utama yang diidentifikasi:**

| Domain | Risiko | Severity |
|--------|--------|----------|
| CCTV dengan AI | Facial recognition data breach → privasi massal | Kritis |
| CCTV dengan AI | AI poisoning: membutakan kamera tertentu | Tinggi |
| Traffic light | Unauthorized command → kemacetan atau kecelakaan | Kritis |
| Sensor lingkungan | Data manipulation → salah informasi publik | Tinggi |
| Integrasi 5G | 5G network slice compromise → all systems affected | Kritis |
| City Operations Center | Single point of compromise | Kritis |

**Rekomendasi arsitektur:**
- Domain separation: traffic, CCTV, sensor, dan parkir dalam network terpisah
- City Operations Center: read-only access ke semua domain, tidak dapat control langsung
- Data governance board: oversight penggunaan data warga
- Privacy Impact Assessment sebelum setiap deployment CCTV/AI baru
- Resilient design: setiap domain harus berfungsi secara autonomous jika City Center down

---

### 7. Praktikum atau Aktivitas Terarah

**Judul:** Analisis Implikasi Keamanan Tren CPS/IoT Terpilih

**Langkah Kerja:**
1. Pilih satu tren: (a) Digital Twin untuk industri, (b) Medical IoT deployment baru, (c) Smart City komponen terpilih
2. Lakukan literature review: cari minimum 3 sumber tentang security challenges domain tersebut
3. Buat threat model spesifik untuk tren yang dipilih
4. Identifikasi regulasi dan standar yang berlaku (FDA, UU PDP, IEC 62443, dll.)
5. Rancang security requirements yang seharusnya dipenuhi oleh implementasi domain tersebut
6. Presentasikan temuan dalam format makalah singkat (3–5 halaman) atau presentasi 10 menit

---

### 8. Latihan Pemahaman

**Soal 1 (Analisis — C4)**
Digital twin yang menggunakan data real-time dari sistem fisik menciptakan "information goldmine" bagi attacker. Identifikasi tiga kategori informasi sensitif yang dapat diekstrak dari digital twin manufaktur, dan jelaskan bagaimana masing-masing dapat dieksploitasi.

**Soal 2 (Evaluasi — C5)**
Sebuah perangkat pacemaker memiliki fitur wireless monitoring — dokter dapat memantau ritme jantung pasien dari jarak jauh. Evaluasi trade-off keamanan vs keselamatan: apa risiko keamanan dari konektivitas wireless ini, dan apakah manfaatnya membenarkan risiko tersebut?

**Soal 3 (Analisis — C4)**
Smart city mengumpulkan data pergerakan kendaraan dan pejalan kaki secara real-time. Jelaskan bagaimana data ini dapat: (a) digunakan secara legitimate untuk keamanan publik, dan (b) disalahgunakan untuk mass surveillance atau profiling warga.

**Soal 4 (Evaluasi — C5)**
Post-quantum cryptography (PQC) algorithms umumnya memerlukan computational resources lebih besar dari RSA/ECC. Untuk perangkat IoT dengan microcontroller 32-bit yang sudah deployed, apa opsi migrasi ke PQC yang realistis? Apakah semua perangkat existing dapat dimigrasi?

**Soal 5 (Sintesis — C6)**
Rancang security requirements untuk sebuah autonomous vehicle yang beroperasi dalam ekosistem smart city. Pertimbangkan: vehicle-to-infrastructure communication, over-the-air update, sensor data integrity, dan decision algorithm security.

---

### 9. Latihan Terapan / Studi Kasus

**Studi Kasus 1 — Medical IoT Security Strategy (C4–C5)**

Sebuah rumah sakit swasta berencana deploy sistem monitoring pasien berbasis IoT untuk 200 tempat tidur ICU: vital sign monitor, infusion pump connected, dan ventilator dengan remote monitoring. Semua device terhubung ke clinical information system. Beberapa device menggunakan OS proprietary (firmware closed-source), beberapa sudah 8 tahun beroperasi dan tidak lagi menerima update dari vendor.

*Pertanyaan:*
1. Lakukan risk assessment untuk deployment ini, prioritaskan berdasarkan potensi patient safety impact
2. Rancang network segmentation khusus untuk medical IoT yang menyeimbangkan keamanan dan aksesibilitas klinis
3. Untuk device dengan firmware end-of-life, apa pilihan mitigasi yang tersedia? Evaluasi setiap opsi
4. Bagaimana Anda memastikan bahwa incident response untuk medical IoT mempertimbangkan patient safety sebagai prioritas tertinggi?

---

### 10. Kunci Jawaban dan Pembahasan

**Jawaban Soal 4 (PQC Migration untuk IoT):**
Migrasi PQC untuk perangkat existing sangat challenging: (1) Perangkat dengan OTA update capability: dapat diupdate firmware dengan PQC libraries, tetapi perlu verifikasi bahwa resources (CPU, RAM, flash) cukup untuk PQC algorithms; (2) Perangkat tanpa OTA atau dengan resources sangat terbatas: migrasi PQC pada device level tidak feasible. Options: (a) isolasi perangkat ini dari jaringan yang memerlukan long-term confidentiality; (b) enkripsi ulang semua komunikasi di gateway level (gateway yang lebih powerful melakukan PQC, device tetap menggunakan legacy crypto ke gateway); (c) rencana replacement jangka panjang. (3) Tidak semua data perlu PQC saat ini: data dengan short sensitivity period (kurang dari 10 tahun) tidak urgent untuk PQC migrasi. Data dengan sensitivity jangka panjang (rahasia state, medical records, industrial IP) harus diprioritaskan. Kesimpulan: crypto agility — kemampuan untuk mengganti algoritma kriptografi tanpa mengganti seluruh sistem — adalah design requirement yang harus dipertimbangkan untuk perangkat baru yang di-deploy hari ini.

**Kunci Studi Kasus Medical IoT:**
Risk assessment priority: (1) Infusion pump remote compromise → wrong dosage → patient death (Kritis); (2) Ventilator manipulation → respiratory failure (Kritis); (3) Vital sign monitor spoofing → delayed clinical response (Kritis); (4) Data breach → HIPAA/PDP violation (Tinggi); (5) Ransomware → system unavailability (Tinggi). Network segmentation: Clinical IoT VLAN (terpisah dari corporate dan internet), clinical systems (CIS, EHR) dalam VLAN terpisah dengan akses ketat dari IoT VLAN, tidak ada akses internet langsung dari medical device, maintenance laptop hanya digunakan di VLAN khusus, clinical workstation hanya dapat akses baca data dari IoT VLAN. EoL device mitigation: (1) network isolation (tidak ada koneksi ke seluruh hospital network, hanya ke dedicated gateway); (2) application whitelisting di gateway; (3) kompensasi dengan enhanced monitoring; (4) vendor engagement untuk extended support atau replacement program; (5) risk acceptance yang terdokumentasi dan ditandatangani oleh risk owner.

---

### 11. Ringkasan Bab

Tren CPS/IoT menciptakan frontiers keamanan baru yang memerlukan pendekatan adaptif. Edge computing membawa risiko "bridge" antara OT dan cloud. Digital twin mengandung informasi sangat sensitif dan memerlukan perlindungan setara dengan sistem fisiknya. Medical IoT (IoMT) menempatkan patient safety sebagai prioritas pertama — keamanan tidak boleh mengorbankan akses medis kritis. Smart city menciptakan risiko cascade failure antara domain infrastruktur yang semakin terintegrasi. Post-quantum cryptography menjadi concern nyata untuk sistem dengan lifecycle panjang — crypto agility harus menjadi design principle mulai hari ini. Semua tren ini memerlukan kolaborasi antara security professional, domain expert (medis, energi, transportasi), regulator, dan pembuat kebijakan.

---

### 12. Refleksi Profesional

1. Teknologi Digital Twin dapat meningkatkan efisiensi operasional secara dramatis, tetapi juga menciptakan aset informasi yang sangat bernilai dan berpotensi sangat berbahaya jika disalahgunakan. Bagaimana organisasi menyeimbangkan nilai operasional dari digital twin dengan kebutuhan untuk melindungi informasi sensitif yang terkandung di dalamnya — terutama ketika twin mungkin dioperasikan oleh vendor third-party?

2. Medical IoT menghadapi dilema unik: keamanan yang terlalu ketat (misalnya, memerlukan multi-step authentication untuk mengubah dosis infusion pump) dapat menghambat respons klinis dalam emergensi. Siapa yang berwenang membuat keputusan tentang trade-off ini — engineer keamanan, dokter, regulator, atau pasien? Bagaimana proses pengambilan keputusan yang tepat terlihat?

3. Smart city yang mengumpulkan data warga dalam skala masif menciptakan tanggung jawab yang sangat besar kepada masyarakat. Sebuah breach pada sistem CCTV smart city yang memaparkan data pergerakan jutaan warga selama bertahun-tahun adalah insiden yang belum pernah terjadi sebelumnya dalam skala tersebut. Bagaimana kota-kota di Indonesia seharusnya mempersiapkan diri — regulasi, teknis, dan respons insiden — untuk skenario seperti ini?

---

---

# LAMPIRAN

## Lampiran A — Template Architecture Map dan Data Flow Diagram

### A.1 Template Architecture Map CPS/IoT

```
ARCHITECTURE MAP — [Nama Sistem]
Versi: ____  Tanggal: ____  Dibuat oleh: ____  Klasifikasi: ____

═══════════════════════════════════════════════════════════════════
LAYER 1: FIELD DEVICES
═══════════════════════════════════════════════════════════════════
[Daftar semua perangkat field]

ID Perangkat | Nama/Model | Fungsi | OS/Firmware | Protokol | Lokasi Fisik | Criticality
-------------|------------|--------|-------------|----------|--------------|------------
D-001        |            |        |             |          |              | Kritis/Tinggi/Sedang/Rendah
D-002        |            |        |             |          |              |

═══════════════════════════════════════════════════════════════════
LAYER 2: COMMUNICATION / GATEWAY
═══════════════════════════════════════════════════════════════════
[Gateway, edge node, protocol converter]

ID | Nama/Model | Fungsi | Protokol In | Protokol Out | Autentikasi | Enkripsi
---|------------|--------|-------------|--------------|-------------|--------

═══════════════════════════════════════════════════════════════════
LAYER 3: CONTROL / OT
═══════════════════════════════════════════════════════════════════
[PLC, DCS, RTU, SCADA, HMI]

ID | Nama/Model | Vendor | OS | Versi Firmware | Protokol | Patch Level
---|------------|--------|----|----|---------|----------

═══════════════════════════════════════════════════════════════════
LAYER 4: PLATFORM / CLOUD
═══════════════════════════════════════════════════════════════════
[IoT Hub, API Gateway, Database, Analytics]

ID | Layanan | Provider | Region | Autentikasi | Enkripsi at-rest | Logging
---|---------|----------|--------|-------------|-----------------|--------

═══════════════════════════════════════════════════════════════════
NETWORK ZONES
═══════════════════════════════════════════════════════════════════
Zone | VLAN | Subnet | Devices | Traffic Rules | Monitoring
-----|------|--------|---------|---------------|----------
```

---

### A.2 Template Data Flow Diagram (DFD)

```
DATA FLOW DIAGRAM — [Nama Sistem]
Level: L0 (Context) / L1 (System) / L2 (Process Detail)

KOMPONEN DAN DATA FLOW:

[Sumber Data]          Data yang dikirim          [Tujuan]
Perangkat D-001  →→→  {suhu, kelembaban, ts}  →→→  Gateway G-001
Gateway G-001    →→→  {payload terenkripsi}    →→→  Cloud MQTT Broker
MQTT Broker      →→→  {telemetry message}      →→→  Analytics Engine
Analytics Engine →→→  {alert, report}          →→→  Operator Dashboard

TRUST BOUNDARIES:
[ TB-1: Field ↔ Gateway ]       Crossing: mTLS, cert auth
[ TB-2: Gateway ↔ Cloud ]       Crossing: HTTPS, JWT
[ TB-3: Cloud ↔ Operator ]      Crossing: HTTPS, MFA

DATA CLASSIFICATION:
Type                  | Classification | Retention | Encryption
---------------------|----------------|-----------|----------
Raw sensor readings  | Internal       | 90 hari   | TLS in-transit
Alarm events         | Confidential   | 1 tahun   | AES-256 at rest
User commands        | Confidential   | 2 tahun   | AES-256 at rest
Audit logs           | Restricted     | 5 tahun   | AES-256 at rest
```

---

## Lampiran B — Template Protocol Security Analysis Report dan Secure Connection Checklist

### B.1 Protocol Security Analysis Report

```
PROTOCOL SECURITY ANALYSIS REPORT
Sistem: ________________  Protokol: ________________
Tanggal: ____  Assessor: ____  Versi Dokumen: ____

1. PROTOKOL OVERVIEW
   Nama Protokol: ________________________________
   Standar/RFC: __________________________________
   Transport: [ ] TCP  [ ] UDP  [ ] Serial  [ ] Bluetooth  [ ] Lainnya
   Port default: _____  Port yang digunakan: _____

2. SECURITY FEATURES NATIVE
   [ ] Enkripsi: Metode: ________________________
   [ ] Autentikasi: Metode: _____________________
   [ ] Integritas pesan: Metode: ________________
   [ ] Anti-replay: Metode: _____________________
   [ ] Authorization: Metode: ___________________

3. KELEMAHAN YANG DIKETAHUI
   ID    | Deskripsi                    | CVSS | Mitigation
   ------|------------------------------|------|----------
         |                              |      |
   
4. KONFIGURASI AKTUAL (dari inspeksi)
   Versi protokol yang digunakan: ______________
   Konfigurasi TLS (jika berlaku):
     - Min TLS version: ______________
     - Cipher suites aktif: __________
     - Certificate validation: [ ] Ya  [ ] Tidak
     - mTLS (mutual): [ ] Ya  [ ] Tidak
   Konfigurasi autentikasi:
     - Method: ______________
     - Credential type: ______________
   
5. TEMUAN
   ID     | Severity | Deskripsi | Evidence | Rekomendasi
   -------|----------|-----------|----------|------------
   P-001  |          |           |          |

6. KESIMPULAN
   Risk Level Keseluruhan: [ ] Kritis  [ ] Tinggi  [ ] Sedang  [ ] Rendah
   Rekomendasi Utama:
   1. _______________________________________________
   2. _______________________________________________
```

### B.2 Secure Connection Checklist

```
SECURE CONNECTION CHECKLIST — CPS/IoT

Device-to-Gateway:
  [ ] mTLS dengan device certificate (X.509) aktif
  [ ] TLS versi minimum 1.2 (idealnya 1.3)
  [ ] Cipher suite: no RC4, no DES, no NULL
  [ ] Certificate validation: CA chain, expiry, revocation
  [ ] Anonymous connection diblokir
  [ ] Protocol-level authentication aktif (MQTT username, CoAP DTLS)
  [ ] ACL: device hanya dapat akses topic/resource yang diotorisasi

Gateway-to-Cloud:
  [ ] HTTPS/TLS 1.3 untuk semua API calls
  [ ] API key atau OAuth 2.0 token dengan scope terbatas
  [ ] Token expiry dikonfigurasi (max 24 jam)
  [ ] HSTS aktif pada cloud endpoint
  [ ] Certificate pinning pada gateway (opsional tapi direkomendasikan)

MQTT Specific:
  [ ] Port 8883 (MQTT over TLS), bukan 1883 (plaintext)
  [ ] allow_anonymous false
  [ ] password_file aktif
  [ ] ACL file dikonfigurasi dengan prinsip least privilege
  [ ] TLS versi minimal dikonfigurasi

General:
  [ ] Semua koneksi keluar dan masuk di-log
  [ ] Failed authentication di-alert
  [ ] Rate limiting aktif untuk koneksi baru
  [ ] Network traffic di-monitor untuk anomali
```

---

## Lampiran C — Template Firmware/Hardware Security Review Report

```
FIRMWARE / HARDWARE SECURITY REVIEW REPORT
Perangkat: ________________  Firmware Versi: ________
Tanggal: ____  Metode akuisisi: ____  Assessor: ____
Hash SHA-256 firmware file: ___________________________

KETENTUAN: Review ini dilakukan pada firmware sample yang diperoleh secara
legal (dari portal vendor / perangkat lab berotorisasi / dokumen resmi).
Tidak ada pengujian pada perangkat production atau sistem pihak ketiga.

1. TRIAGE SUMMARY
   File size: ________  Format: ________
   Komponen teridentifikasi (binwalk):
   - Bootloader: ___________
   - Kernel: _______________
   - Filesystem: ___________
   - Enkripsi/Kompresi: [ ] Ada  [ ] Tidak
   Entropy range: ______ (Bagian terenkripsi: [ ] Ada  [ ] Tidak)

2. FIRMWARE COMPOSITION
   OS: ________________  Versi: ______
   Libraries teridentifikasi:
   Library       | Versi  | Known CVE? | Notes
   --------------|--------|------------|------
   OpenSSL       |        |            |
   BusyBox       |        |            |
   uClibc        |        |            |

3. FINDINGS

   F-FW-001: HARDCODED CREDENTIALS
   Status: [ ] Ditemukan  [ ] Tidak Ditemukan
   Detail: _______________________________________________
   Lokasi: _______________________________________________
   Severity: [ ] Kritis  [ ] Tinggi  [ ] Sedang  [ ] Rendah
   Rekomendasi: __________________________________________

   F-FW-002: PRIVATE KEYS / CERTIFICATES
   Status: [ ] Ditemukan  [ ] Tidak Ditemukan
   Detail: _______________________________________________
   Unik per device: [ ] Ya  [ ] Tidak  [ ] Tidak dapat ditentukan
   Severity: _____________________________________________
   Rekomendasi: __________________________________________

   F-FW-003: DEBUG ARTIFACTS
   Status: [ ] Ditemukan  [ ] Tidak Ditemukan
   Detail (debug mode, test endpoints, shell access): ____
   Severity: _____________________________________________

   F-FW-004: SERVICES DAN PORTS
   Service       | Port  | Diperlukan? | Rekomendasi
   --------------|-------|-------------|-------------
   Telnet        | 23    | [ ] Ya/Tidak| Disable
   SSH           | 22    |             |
   HTTP          | 80    |             |

   F-HW-001: DEBUG INTERFACES
   JTAG: [ ] Ada  [ ] Disabled  [ ] Protected
   UART: [ ] Ada  [ ] Accessible  [ ] Protected
   USB DFU: [ ] Ada  [ ] Enabled  [ ] Auth required
   Detail: _______________________________________________

4. RISK SUMMARY
   | Finding   | Severity | Rekomendasi         | Priority |
   |-----------|----------|---------------------|----------|
   | F-FW-001  |          |                     |          |

5. OVERALL ASSESSMENT
   Risk Level: [ ] Kritis  [ ] Tinggi  [ ] Sedang  [ ] Rendah
   Siap untuk deployment: [ ] Ya  [ ] Tidak  [ ] Bersyarat
   Syarat (jika bersyarat): ______________________________
```

---

## Lampiran D — Template Asset Register dan Threat Model Worksheet

### D.1 Asset Register CPS/IoT

```
ASSET REGISTER — [Nama Sistem / Organisasi]
Versi: ____  Tanggal: ____  Pemilik: ____

ID    | Nama Aset     | Tipe   | Lokasi  | Owner | Criticality | Value | Dependencies
------|---------------|--------|---------|-------|-------------|-------|-------------
A-001 | PLC Line 1    | HW/OT  | Area A  |       | Kritis      |       | A-002, A-005
A-002 | SCADA Server  | SW/OT  | Server  |       | Kritis      |       | A-003
A-003 | HMI Workstat. | HW/SW  | CtrlRm  |       | Tinggi      |       |
A-004 | Sensor Suhu   | HW     | Line 1  |       | Sedang      |       | A-001

Criticality Rating:
  Kritis: Kegagalan menyebabkan safety incident atau downtime sistem kritis
  Tinggi: Kegagalan menyebabkan gangguan produksi signifikan atau data breach
  Sedang: Kegagalan menyebabkan degradasi layanan, tidak immediate safety
  Rendah: Kegagalan memiliki dampak minimal
```

### D.2 Threat Model Worksheet (STRIDE + Safety)

```
THREAT MODEL WORKSHEET
Sistem: ________________  Tanggal: ____  Fasilitator: ____

KOMPONEN YANG DIANALISIS:
[Daftar komponen dalam scope threat model]

THREAT TABLE:

ID    | Komponen | Kategori STRIDE | Deskripsi Ancaman              | Likelihood | Impact | Mitigasi
------|----------|-----------------|--------------------------------|------------|--------|--------
T-001 | Gateway  | S - Spoofing    | Attacker impersonate device    | 3          | 4      | mTLS client cert
T-002 | PLC      | T - Tampering   | Unauthorized write setpoint    | 3          | 5      | DPI + auth
T-003 | MQTT     | R - Repudiation | No logging, deniable actions   | 2          | 3      | Audit log
T-004 | Network  | I - Info Disc   | Protocol plaintext interception| 4          | 4      | TLS encryption
T-005 | SCADA    | D - DoS         | Flood → SCADA unresponsive     | 3          | 4      | Rate limiting
T-006 | PLC      | E - Privilege   | Escalate from operator to admin| 2          | 5      | RBAC enforcement
T-007 | Safety   | SF - Safety Fail| SIS disabled during attack     | 1          | 5      | SIS isolation
      |          |                 |                                |            |        |

UNMITIGATED THREATS (Risk Acceptance Required):
ID    | Ancaman | Alasan tidak dapat dimitigasi | Risk Owner | Tanggal Accept
------|---------|-------------------------------|------------|---------------

DIAGRAM TRUST BOUNDARY:
[Sisipkan diagram DFD dengan trust boundary]
```

---

## Lampiran E — Template Risk Register dan Secure Architecture Design

### E.1 Risk Register CPS/IoT

```
RISK REGISTER — [Nama Sistem / Organisasi]
Versi: ____  Tanggal: ____  Risk Owner: ____  Review Date: ____

ID    | Aset     | Ancaman          | Kelemahan        | L | I | Score | Kategori
------|----------|-----------------|-----------------|---|---|-------|--------
R-001 |          |                 |                 |   |   |       | Kritis
R-002 |          |                 |                 |   |   |       | Tinggi

Kolom lengkap:
ID | Aset | Ancaman | Kelemahan | Likelihood(1-5) | Impact(1-5) | Score | Kategori Risk |
   Kontrol Existing | Kontrol Usulan | Effort | Risk Owner | Due Date | Status | Residual Risk

Keterangan Likelihood:
  1 = Sangat tidak mungkin (<5% dalam setahun)
  2 = Tidak mungkin (5–15%)
  3 = Mungkin (15–40%)
  4 = Kemungkinan besar (40–75%)
  5 = Hampir pasti (>75%)

Keterangan Impact:
  1 = Trascendental (dampak minimal)
  2 = Kecil (gangguan terbatas)
  3 = Sedang (gangguan signifikan, tidak ada safety)
  4 = Besar (gangguan serius, data breach, atau safety minor)
  5 = Katastrofik (safety incident, infrastruktur kritis, reputasi besar)

Risk Treatment:
  MITIGATE: Implementasikan kontrol tambahan
  ACCEPT: Terima risiko dengan dokumentasi
  TRANSFER: Asuransi atau transfer ke pihak ketiga
  AVOID: Hentikan atau modifikasi aktivitas yang menghasilkan risiko
```

### E.2 Secure Architecture Design Checklist

```
SECURE ARCHITECTURE DESIGN CHECKLIST — CPS/IoT

DEVICE LAYER:
  [ ] Setiap device memiliki unique identity (X.509 cert atau equal)
  [ ] Secure Boot dikonfigurasi atau direncanakan
  [ ] Debug interface disabled atau protected pada production
  [ ] Firmware update mechanism: signed, HTTPS, anti-downgrade, rollback
  [ ] Key material tersimpan dalam secure storage (SE/TPM) jika critical

COMMUNICATION LAYER:
  [ ] Semua komunikasi dienkripsi (TLS 1.2+ atau equivalent)
  [ ] Mutual authentication (mTLS atau equivalent) untuk device-gateway
  [ ] Anti-replay mechanism (timestamp + nonce atau sequence number)
  [ ] Message integrity (signing atau HMAC)
  [ ] Certificate pinning pada critical connections

NETWORK LAYER:
  [ ] Segmentasi: IT, OT, dan IoT dalam zone terpisah
  [ ] Default-deny firewall policy
  [ ] Industrial firewall untuk OT zone (DPI)
  [ ] Data diode untuk unidirectional data flow kritis
  [ ] Out-of-band management network

PLATFORM / CLOUD LAYER:
  [ ] API authentication (OAuth 2.0, API key dengan expiry)
  [ ] RBAC atau ABAC untuk authorization
  [ ] Rate limiting pada semua endpoint
  [ ] Logging semua akses dan perubahan
  [ ] Encryption at-rest untuk data sensitif

MONITORING:
  [ ] SIEM atau log aggregation dari semua layer
  [ ] Behavioral baseline per device atau device group
  [ ] Alert untuk koneksi unusual, volume traffic anomali
  [ ] IR runbook untuk skenario umum

GOVERNANCE:
  [ ] Asset inventory terkini
  [ ] Risk register aktif dan di-review periodik
  [ ] Vulnerability management: scan dan patch process
  [ ] Incident response plan terdokumentasi dan dilatih
  [ ] Vendor security requirements dalam kontrak
```

---

## Lampiran F — Rubrik Penilaian

### F.1 Rubrik Penilaian Praktikum

| Kriteria | Tidak Memenuhi (0–59) | Memenuhi (60–74) | Baik (75–84) | Sangat Baik (85–100) |
|----------|----------------------|------------------|--------------|---------------------|
| **Metodologi** | Tidak mengikuti prosedur yang ditentukan; langkah-langkah tidak terstruktur | Mengikuti prosedur dengan beberapa deviasi; alasan tidak selalu jelas | Mengikuti prosedur dengan baik; deviasi minor disertai alasan | Metodologi sangat sistematis; adaptasi yang justified terhadap situasi spesifik |
| **Identifikasi Temuan** | Temuan kurang dari yang diharapkan; banyak yang terlewat | Mengidentifikasi temuan utama tetapi melewatkan beberapa yang penting | Mengidentifikasi sebagian besar temuan; categorization tepat | Identifikasi temuan lengkap dan akurat; tidak ada false positive signifikan |
| **Evidence** | Tidak ada evidence atau evidence tidak terkait klaim | Evidence ada tetapi tidak adequat mendukung klaim | Evidence jelas dan mendukung klaim; hash/dokumentasi ada | Evidence sangat kuat; chain of custody terdokumentasi sempurna |
| **Analisis Risiko** | Tidak ada risk assessment atau tidak relevant | Risk assessment ada tetapi scoring tidak justified | Risk scoring logis dengan justifikasi yang cukup | Risk scoring sangat tepat dengan justifikasi berbasis framework dan evidence |
| **Rekomendasi** | Tidak ada rekomendasi atau tidak practical | Rekomendasi generic dan tidak spesifik untuk konteks | Rekomendasi spesifik dan dapat diimplementasikan | Rekomendasi sangat spesifik, diprioritaskan, dan disertai effort estimate |
| **Etika dan Kepatuhan** | Melanggar batasan ethical/legal yang ditetapkan | Mematuhi batasan tetapi tidak mendokumentasikan | Mematuhi dan mendokumentasikan dengan baik | Mematuhi, mendokumentasikan, dan menunjukkan pemahaman mendalam tentang implikasi etika |
| **Laporan** | Laporan tidak terstruktur, banyak kesalahan faktual | Laporan terstruktur dasar; beberapa kesalahan faktual | Laporan profesional; akurat dan jelas | Laporan setara publikasi industri; sangat jelas, akurat, dan komprehensif |

### F.2 Rubrik Penilaian Capstone (Tugas Besar)

| Kriteria | Bobot | Deskripsi |
|----------|-------|-----------|
| **Asset Inventory & Architecture** | 20% | Kelengkapan inventory, akurasi architecture diagram, identifikasi trust boundary |
| **Threat Model** | 20% | Kelengkapan STRIDE analysis, identifikasi ancaman unik konteks sistem, quality DFD |
| **Risk Register** | 20% | Akurasi risk scoring, kelengkapan register, justifikasi setiap risk item |
| **Control Design** | 20% | Kesesuaian kontrol dengan risiko, proporsionalitas, feasibility implementasi |
| **Technical Report** | 10% | Struktur, kejelasan, evidence, profesionalisme laporan |
| **Presentation** | 10% | Kemampuan menjelaskan kepada audiens teknis dan non-teknis; menjawab pertanyaan |

---

## Lampiran G — Pernyataan Etika Praktikum

```
PERNYATAAN ETIKA PRAKTIKUM
Program Studi Magister Terapan Forensik Digital dan Keamanan Siber
PENS — Politeknik Elektronika Negeri Surabaya

Mata Kuliah: CPS and IoT Security (MK-E-04)

Saya yang bertanda tangan di bawah ini:

Nama    : _________________________________
NIM     : _________________________________
Kelas   : _________________________________

Dengan ini menyatakan bahwa selama mengikuti praktikum mata kuliah ini:

1. LINGKUP KERJA LEGAL:
   Seluruh pengujian, analisis, dan eksperimen hanya dilakukan pada:
   a. Lingkungan lab yang disediakan oleh institusi
   b. Perangkat milik pribadi yang sah
   c. Dataset, firmware, log, dan artefak legal yang disediakan oleh dosen
   d. Simulator dan emulator yang diotorisasi
   
   Saya TIDAK AKAN melakukan pengujian pada sistem, jaringan, perangkat,
   infrastruktur, atau layanan pihak ketiga tanpa otorisasi tertulis.

2. SANITASI ARTEFAK:
   Setiap artefak yang dikumpulkan dan diserahkan sebagai bukti praktikum
   telah disanitasi dari: kredensial asli, data pribadi, data operasional
   sensitif, dan informasi pihak ketiga.

3. KERAHASIAAN INFORMASI:
   Informasi dan teknik yang dipelajari dalam praktikum ini tidak akan
   digunakan untuk tujuan yang merugikan individu, organisasi, atau
   infrastruktur manapun.

4. PELAPORAN BERTANGGUNG JAWAB:
   Jika dalam proses pembelajaran saya menemukan kelemahan keamanan pada
   sistem nyata (secara tidak sengaja), saya akan segera melaporkan kepada
   dosen dan tidak akan mengeksploitasi atau mempublikasikan temuan tersebut
   sebelum mendapat arahan resmi.

5. INTEGRITAS AKADEMIK:
   Semua laporan praktikum mencerminkan pekerjaan saya sendiri. Saya tidak
   akan melakukan fabrikasi data atau menyalin laporan orang lain.

6. KEPATUHAN HUKUM:
   Saya memahami bahwa akses tidak sah ke sistem komputer adalah pelanggaran
   Pasal 30 UU ITE No. 11 Tahun 2008 sebagaimana diubah dengan UU No. 19
   Tahun 2016, dan dapat dikenai sanksi pidana.

Demikian pernyataan ini saya buat dengan sadar dan tanpa paksaan.

Surabaya, _________________ 20____

Tanda tangan mahasiswa                    Tanda tangan Dosen Pengampu

_______________________                   _______________________
(Nama Mahasiswa)                          (Nama Dosen)
NIM: ___________                          NIP/NIK: ______________
```

---

# DAFTAR PUSTAKA

## Pustaka Utama

1. NIST. (2023). *NISTIR 8259: Foundational Cybersecurity Activities for IoT Device Manufacturers*. National Institute of Standards and Technology. https://doi.org/10.6028/NIST.IR.8259

2. NIST. (2023). *NISTIR 8259A: IoT Device Cybersecurity Capability Core Baseline*. National Institute of Standards and Technology. https://doi.org/10.6028/NIST.IR.8259A

3. NIST. (2023). *NIST SP 800-82 Rev. 3: Guide to Operational Technology (OT) Security*. National Institute of Standards and Technology. https://doi.org/10.6028/NIST.SP.800-82r3

4. NIST. (2012). *NIST SP 800-30 Rev. 1: Guide for Conducting Risk Assessments*. National Institute of Standards and Technology. https://doi.org/10.6028/NIST.SP.800-30r1

5. IEC. (2018). *IEC 62443-3-2: Industrial Automation and Control Systems Security — Security Risk Assessment for System Design*. International Electrotechnical Commission.

6. IEC. (2019). *IEC 62443-4-2: Industrial Automation and Control Systems Security — Technical Security Requirements for IACS Components*. International Electrotechnical Commission.

7. ENISA. (2023). *Baseline Security Recommendations for IoT in the Context of Critical Information Infrastructures*. European Union Agency for Cybersecurity.

8. OWASP Foundation. (2023). *OWASP IoT Security Verification Standard (ISVS) v1.0*. OWASP Foundation. https://github.com/OWASP/IoT-Security-Verification-Standard-ISVS

9. OWASP Foundation. (2023). *OWASP Firmware Security Testing Methodology (FSTM)*. OWASP Foundation. https://github.com/scriptingxss/owasp-fstm

10. Stallings, W. (2022). *Cryptography and Network Security: Principles and Practice* (8th ed.). Pearson.

## Pustaka Pendukung

11. Pfleeger, C. P., Pfleeger, S. L., & Margulies, J. (2015). *Security in Computing* (5th ed.). Prentice Hall.

12. MITRE. (2023). *ATT&CK for ICS Matrix*. MITRE Corporation. https://attack.mitre.org/matrices/ics/

13. CISA. (2023). *ICS Security Best Practices*. Cybersecurity and Infrastructure Security Agency. https://www.cisa.gov/ics

14. ISA. (2018). *ISA-62443-3-3: System Security Requirements and Security Levels*. International Society of Automation.

15. OWASP Foundation. (2023). *OWASP Top 10 IoT Vulnerabilities*. OWASP Foundation. https://owasp.org/www-project-internet-of-things/

16. NIST. (2020). *NIST SP 800-63B: Digital Identity Guidelines — Authentication and Lifecycle Management*. National Institute of Standards and Technology.

17. IETF. (2018). *RFC 8446: The Transport Layer Security (TLS) Protocol Version 1.3*. Internet Engineering Task Force.

18. IETF. (2012). *RFC 6347: Datagram Transport Layer Security Version 1.2 (DTLS 1.2)*. Internet Engineering Task Force.

19. IETF. (2014). *RFC 7252: The Constrained Application Protocol (CoAP)*. Internet Engineering Task Force.

20. OASIS. (2019). *MQTT Version 5.0*. OASIS Standard. https://docs.oasis-open.org/mqtt/mqtt/v5.0/mqtt-v5.0.html

21. ISO/IEC. (2022). *ISO/IEC 27001:2022: Information Security, Cybersecurity and Privacy Protection — Information Security Management Systems — Requirements*. International Organization for Standardization.

22. ISO/IEC. (2022). *ISO/IEC 27005:2022: Information Security, Cybersecurity and Privacy Protection — Guidance on Managing Information Security Risks*. International Organization for Standardization.

23. Lee, E. A., & Seshia, S. A. (2017). *Introduction to Embedded Systems: A Cyber-Physical Systems Approach* (2nd ed.). MIT Press.

24. Kim, D. & Solomon, M. G. (2018). *Fundamentals of Information Systems Security* (3rd ed.). Jones & Bartlett Learning.

25. Dragos Inc. (2023). *Year in Review: ICS/OT Cybersecurity Report 2023*. Dragos Inc.

26. Claroty. (2023). *Biannual ICS Risk & Vulnerability Report*. Claroty Team82.

27. NIST. (2023). *NIST SP 1800-10: Protecting Information and System Integrity in Industrial Control System Environments*. National Institute of Standards and Technology.

28. ARM. (2021). *PSA Certified IoT Security Framework*. ARM Holdings. https://www.psacertified.org

29. IETF. (2023). *RFC 9202: Datagram Transport Layer Security (DTLS) Profile for Authentication and Authorization for Constrained Environments (ACE)*. Internet Engineering Task Force.

30. Kohnfelder, L., & Garg, P. (1999). *The Threats to Our Products*. Microsoft Interface (foundational paper for STRIDE threat modeling).

31. Bodeau, D., & Graubart, R. (2021). *Cyber Resiliency Engineering Framework*. MITRE Technical Report MTR-110236.

32. IEC. (2003). *IEC 61508: Functional Safety of E/E/PE Safety-related Systems (Parts 1-7)*. International Electrotechnical Commission.

33. Papp, D., Ma, Z., & Buttyan, L. (2015). Embedded Systems Security: Threats, Vulnerabilities, and Attack Taxonomy. *Proceedings of the 13th Annual Conference on Privacy, Security and Trust (PST)*. IEEE.

34. McLaughlin, S., Konstantinou, C., Wang, X., Davi, L., Sadeghi, A.-R., Maniatakos, M., & Karri, R. (2016). The Cybersecurity Landscape in Industrial Control Systems. *Proceedings of the IEEE*, 104(5), 1039–1057.

35. Langner, R. (2011). Stuxnet: Dissecting a Cyberweapon. *IEEE Security & Privacy*, 9(3), 49–51.

36. Dragos. (2017). *TRISIS/TRITON Malware Analysis*. Dragos Research. https://www.dragos.com/blog/trisis-analyzing-safety-system-targeted-malware/

37. E-ISAC & SANS ICS. (2016). *Analysis of the Cyber Attack on the Ukrainian Power Grid*. Electricity Information Sharing and Analysis Center.

38. NIST. (2024). *NIST SP 800-227 (Draft): Recommendations for Key-Encapsulation Mechanisms*. National Institute of Standards and Technology.

39. Pernul, G., & Ryan, P. Y. A. (Eds.). (2023). *Computer Security — ESORICS 2023: Selected Papers*. Springer.

40. Peraturan Perundang-undangan Indonesia:
    - UU No. 27 Tahun 2022 tentang Pelindungan Data Pribadi (UU PDP)
    - UU No. 11 Tahun 2008 jo. UU No. 19 Tahun 2016 tentang Informasi dan Transaksi Elektronik (UU ITE)
    - Peraturan Presiden No. 82 Tahun 2022 tentang Perlindungan Infrastruktur Informasi Vital
    - BSSN. (2023). *Panduan Keamanan Siber untuk Sistem Kontrol Industri*. Badan Siber dan Sandi Negara.

---

*Buku ajar ini disusun berdasarkan Rencana Pembelajaran Semester (RPS) MK-E-04 CPS and IoT Security, Program Studi Magister Terapan Forensik Digital dan Keamanan Siber, Politeknik Elektronika Negeri Surabaya (PENS), Tahun Akademik 2025/2026.*

*Seluruh contoh teknis, konfigurasi, dan praktikum dalam buku ini dirancang untuk tujuan pendidikan dalam lingkungan yang legal, aman, terisolasi, dan berotorisasi. Tidak ada instruksi yang ditujukan untuk eksploitasi sistem nyata atau pihak ketiga.*

*Versi: 1.0 | Juli 2026*
