# BUKU AJAR

# VIRTUALIZATION & CLOUD SECURITY

## MK-E-05

---

**Program Studi:** Magister Terapan Forensik Digital dan Keamanan Siber
**Departemen:** Teknik Informatika dan Komputer
**Institusi:** Politeknik Elektronika Negeri Surabaya (PENS)
**Kode Mata Kuliah:** MK-E-05 / ELEKTIF-G1-G3
**Bobot SKS:** T=2, P=1, Total=3
**Semester:** 1 atau 3 (Pool Gasal / Pendalaman Tesis)
**Level Bloom:** C4-C5

---

*"Security is not a product, but a process — and in the cloud, that process must be continuous, automated, and evidence-based."*

---

## KATA PENGANTAR

Transformasi digital telah mendorong hampir seluruh organisasi untuk bermigrasi ke lingkungan virtualisasi dan cloud. Namun, kecepatan adopsi teknologi ini sering kali melampaui pemahaman tentang implikasi keamanannya. Hypervisor, container, Kubernetes, dan layanan cloud managed membawa efisiensi luar biasa — sekaligus membuka attack surface yang sama sekali berbeda dari infrastruktur fisik konvensional. Kesalahan dalam konfigurasi IAM, network security group yang terlalu permisif, image container yang mengandung vulnerability, atau secret yang tidak terkelola dengan baik menjadi penyebab utama insiden cloud dewasa ini.

Buku ajar ini disusun untuk membekali mahasiswa Magister Terapan Forensik Digital dan Keamanan Siber PENS dengan kemampuan teknis dan konseptual yang dibutuhkan untuk menganalisis, merancang, mengimplementasikan, dan memvalidasi keamanan lingkungan virtualisasi, cloud, container, dan distributed systems. Seluruh materi diorientasikan pada praktik defensif: bukan eksploitasi, melainkan penilaian, perancangan kontrol, validasi, dan dokumentasi yang dapat diaudit.

**Komitmen keselamatan yang tidak dapat dikompromis:** Seluruh kegiatan praktikum dan evaluasi dalam mata kuliah ini hanya boleh dilakukan pada lingkungan yang telah diotorisasi — akun cloud institusi, sandbox, local cluster, atau private cloud PENS. Pengujian terhadap infrastruktur cloud pihak ketiga tanpa izin tertulis merupakan pelanggaran hukum (UU ITE) dan pelanggaran etika profesi.

Buku ini diselaraskan sepenuhnya dengan Rencana Pembelajaran Semester (RPS) MK-E-05 Tahun Akademik 2025/2026.

---

## DESKRIPSI MATA KULIAH

Mata kuliah Virtualization & Cloud Security membekali mahasiswa dengan kemampuan menganalisis, merancang, mengonfigurasi, mengevaluasi, dan memvalidasi kontrol keamanan pada lingkungan virtualisasi, cloud, container, dan distributed systems. Fokus pembelajaran mencakup:

- Shared responsibility model dan cloud architecture (IaaS/PaaS/SaaS/FaaS)
- Identity and Access Management (IAM), RBAC, dan least privilege
- Cloud network segmentation, security groups, dan private connectivity
- Workload isolation, secrets management, dan secure baseline configuration
- Container image security, registry security, dan software supply chain
- Kubernetes/cluster security baseline dan admission control
- Logging, observability, forensic readiness, dan evidence integrity
- Policy-as-code, compliance mapping, backup/recovery, dan resilience
- Secure cloud/container architecture design dan capstone project

Pembelajaran dilakukan melalui case-based dan project-based learning pada lab legal, terisolasi, dan berotorisasi.

---

## PETA OBE: CPL → IK → CPMK → SUB-CPMK → EVALUASI

| CPMK | Sub-CPMK | Materi Utama | Evaluasi | Bobot |
|---|---|---|---|---|
| CPMK-1: Analisis arsitektur virtualisasi/cloud/container | Sub-CPMK-1: Arsitektur, shared responsibility, trust boundary, risk scenario | Virtualization, cloud models, containers, trust boundary | Eval-1: Architecture map + risk memo | 10% |
| CPMK-2: Evaluasi IAM, network, workload, secrets, baseline | Sub-CPMK-2: IAM, network segmentation, workload isolation, secrets, baseline | IAM/RBAC, VPC, security groups, Pod Security, secrets | Eval-2: Security assessment report | 20% |
| CPMK-3: Posture assessment container/Kubernetes/cloud | Sub-CPMK-3: Container image, registry, K8s baseline, logging, forensic readiness | Trivy, kube-bench, Falco, audit logs, evidence pack | Eval-3: Posture review + evidence pack | 25% |
| CPMK-4: Rancangan secure cloud/container architecture | Sub-CPMK-4: Secure architecture, risk register, compliance, monitoring, resilience | Policy-as-code, CIS Controls, ZTA, backup/recovery | Eval-4: Architecture + resilience plan | 20% |
| CPMK-5: Capstone proyek defensif cloud/container | Sub-CPMK-5: Integrasi desain, implementasi, validasi, evidence, rekomendasi | End-to-end secure cloud/container project | Eval-5/EAS: Capstone report + presentasi | 25% |
| Pengayaan | — | Cloud SOC, CNAPP, CSPM, DevSecOps | Reflective note | 0% |

---

## PETA KOMPETENSI MATA KULIAH

```mermaid
flowchart TD
    A[Virtualization & Cloud Security] --> B[Fondasi]
    B --> B1["Arsitektur virtualisasi:\nhypervisor Type 1/2, VM isolation"]
    B --> B2["Cloud architecture:\nIaaS/PaaS/SaaS, multi-tenancy"]
    B --> B3["Container:\nnamespace, cgroup, OCI image"]
    B --> B4["Shared responsibility model:\nsiapa bertanggung jawab atas apa"]
    A --> C[Kontrol Keamanan]
    C --> C1["IAM & RBAC:\nleast privilege, credential management"]
    C --> C2["Network security:\nVPC, security group, segmentation"]
    C --> C3["Workload isolation:\nPod Security, resource limits"]
    C --> C4["Secrets management:\nVault, K8s secrets, rotation"]
    C --> C5["Secure baseline:\nCIS Benchmarks, hardening"]
    A --> D[Posture Assessment]
    D --> D1["Container image scanning:\nTrivy, Grype"]
    D --> D2["Kubernetes audit:\nkube-bench, admission control"]
    D --> D3["Logging & observability:\nFalco, audit logs, SIEM"]
    D --> D4["Forensic readiness:\nevidence integrity, reproducibility"]
    A --> E[Architecture & Resilience]
    E --> E1["Secure architecture design:\ndefense-in-depth, ZTA"]
    E --> E2["Policy-as-code:\nOPA, Conftest, Checkov"]
    E --> E3["Compliance mapping:\nCSA CCM, CIS Controls"]
    E --> E4["Backup/recovery:\nRTO/RPO, snapshot, DR"]
    A --> F[Capstone Project]
    F --> F1["Secure cloud/container design"]
    F --> F2["Validation & evidence pack"]
    F --> F3["Executive recommendation"]
```

---

## PETUNJUK PENGGUNAAN BUKU

Buku ini dirancang untuk digunakan dalam tiga mode: (1) **Studi Mandiri** — setiap bab lengkap dengan teori, contoh, dan latihan sehingga dapat dipelajari sendiri; (2) **Pembelajaran Tatap Muka/Daring** — setiap bab sesuai dengan 1-3 pertemuan dalam RPS; (3) **Referensi Praktikum** — setiap bab memiliki aktivitas terarah yang dapat dijalankan dalam lab berotorisasi.

**Prasyarat:** Pemahaman dasar jaringan komputer, sistem operasi Linux, dan scripting dasar. Disarankan sudah menyelesaikan MK Networks and Security (MK-E-02).

**Keselamatan Lab:** Sebelum setiap praktikum, bacalah catatan keselamatan dan pastikan Anda bekerja dalam environment yang telah diotorisasi.

---

## DAFTAR BAB

| Bab | Judul | Pertemuan | Sub-CPMK | Evaluasi |
|---|---|---|---|---|
| 1 | Arsitektur Virtualisasi: Hypervisor, VM, dan Keamanan | P1 | Sub-CPMK-1 | Eval-1 |
| 2 | Cloud Architecture, Shared Responsibility, dan Trust Boundary | P2 | Sub-CPMK-1 | Eval-1 |
| 3 | Container, Orchestration, dan Risk Scenario Analysis | P3 | Sub-CPMK-1 | Eval-1 |
| 4 | Identity and Access Management di Cloud | P4 | Sub-CPMK-2 | Eval-2 |
| 5 | Cloud Network Security: VPC, Segmentasi, dan Isolasi | P5 | Sub-CPMK-2 | Eval-2 |
| 6 | Workload Isolation, Secrets Management, dan Secure Baseline | P6 | Sub-CPMK-2 | Eval-2 |
| 7 | Container Image Security dan Software Supply Chain | P7 | Sub-CPMK-3 | Eval-3 |
| 8 | Kubernetes Security Baseline dan Admission Control | P8 | Sub-CPMK-3 | Eval-3 |
| 9 | Logging, Observability, dan Forensic Readiness di Cloud | P9 | Sub-CPMK-3 | Eval-3 |
| 10 | Secure Cloud/Container Architecture Design | P10 | Sub-CPMK-4 | Eval-4 |
| 11 | Monitoring, Backup/Recovery, Incident Readiness, dan Resilience | P11 | Sub-CPMK-4 | Eval-4 |
| 12 | Capstone Fase 1: Security Architecture & Asset Mapping | P12 | Sub-CPMK-5 | Eval-5 |
| 13 | Capstone Fase 2: Implementasi Kontrol & Validasi | P13 | Sub-CPMK-5 | Eval-5 |
| 14 | Capstone Fase 3: Laporan, Evidence Pack & Rekomendasi | P14 | Sub-CPMK-5 | EAS |
| 15 | Pengayaan: Cloud SOC, CNAPP, CSPM, dan Runtime Detection | P15 | — | — |
| 16 | Pengayaan: DevSecOps, Cloud IR, dan Jalur Karir | P16 | — | — |

---

# BAB 1 — ARSITEKTUR VIRTUALISASI: HYPERVISOR, VM, DAN KEAMANAN

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menjelaskan arsitektur virtualisasi dan jenis-jenis hypervisor
- Mengidentifikasi attack surface virtualisasi dan VM isolation boundaries
- Menganalisis risiko keamanan yang bersifat unik pada environment virtualisasi
- Memetakan aset dan data flow dalam infrastruktur virtual

*Berkaitan dengan Sub-CPMK-1, Eval-1 (10%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Virtualization Architecture] --> B[Hypervisor Types]
    B --> B1["Type 1 Bare-metal:\nESXi, Hyper-V, KVM\nLangsung di hardware"]
    B --> B2["Type 2 Hosted:\nVMware Workstation, VirtualBox\nDi atas OS host"]
    A --> C[VM Security Boundaries]
    C --> C1["VM-to-VM isolation:\nnamespace terpisah di hardware"]
    C --> C2["Guest-to-host boundary:\nhypervisor sebagai trust boundary"]
    C --> C3["VM escape:\nhypervisor vulnerability → akses host"]
    A --> D[Attack Surface]
    D --> D1["Hypervisor vulnerabilities:\nCVE dalam hypervisor"]
    D --> D2["VM management API:\nvSphere API, libvirt"]
    D --> D3["Shared resources:\nCPU side-channel, memory"]
    D --> D4["Virtual network:\nVLAN, vSwitch vulnerability"]
    A --> E[Key Security Controls]
    E --> E1["Hypervisor patching:\nkritis, bukan opsional"]
    E --> E2["VM isolation:\nnetwork + storage separation"]
    E --> E3["Minimal hypervisor:\nsmall attack surface"]
    E --> E4["Secure management:\nMFA, encrypted API, audit log"]
```

## 3. Pengantar Kontekstual

Virtualisasi adalah teknologi yang memungkinkan satu mesin fisik menjalankan banyak mesin virtual (VM) secara bersamaan dengan isolasi yang terjamin. Dari perspektif keamanan, virtualisasi menghadirkan manfaat sekaligus tantangan. Manfaatnya: isolasi beban kerja yang berbeda, kemudahan snapshot dan recovery, dan kemampuan segmentasi. Tantangannya: hypervisor menjadi "single point of trust" yang jika dikompromis, seluruh VM yang berjalan di atasnya berpotensi terekspos. Serangan "VM escape" — di mana proses dalam guest VM berhasil keluar ke hypervisor atau VM lain — mewakili salah satu skenario ancaman paling serius dalam infrastruktur virtual.

## 4. Landasan Teori

### 4.1 Hypervisor: Definisi, Tipe, dan Implikasi Keamanan

**Hypervisor** (juga disebut Virtual Machine Monitor/VMM) adalah software, firmware, atau hardware yang menciptakan dan mengelola virtual machines dengan memvirtualisasikan sumber daya fisik (CPU, memori, storage, network).

**Type 1 (Bare-metal Hypervisor):**
Berjalan langsung di atas hardware fisik tanpa OS host di antaranya. Contoh: VMware ESXi, Microsoft Hyper-V (dalam mode server), KVM (Kernel-based Virtual Machine — terintegrasi ke Linux kernel), Xen. Karakteristik keamanan: (a) attack surface lebih kecil karena tidak ada OS host yang dapat dikompromis; (b) performa lebih baik; (c) digunakan dalam produksi enterprise dan cloud provider (AWS Nitro, Azure Hyper-V, GCP KVM).

**Type 2 (Hosted Hypervisor):**
Berjalan sebagai aplikasi di atas OS host. Contoh: VMware Workstation, Oracle VirtualBox, Parallels. Karakteristik keamanan: (a) attack surface lebih besar — kerentanan OS host dapat mempengaruhi seluruh VM; (b) digunakan terutama untuk development, testing, dan lab — tidak direkomendasikan untuk produksi.

### 4.2 VM Isolation dan Attack Surface

**Mekanisme isolasi VM:**
Hypervisor menggunakan kombinasi fitur hardware (Intel VT-x/VT-d, AMD-V/AMD-Vi) dan software untuk memastikan setiap VM memiliki:
- CPU virtual yang terisolasi: proses dalam VM tidak dapat mengakses memori VM lain secara langsung
- Memori tervirtualisasi: setiap VM memiliki address space terpisah, dijaga oleh MMU (Memory Management Unit) virtual
- Storage virtual: disk image terpisah per VM
- Network virtual: interface jaringan yang terisolasi

**Attack surface utama pada virtualisasi:**

1. **Hypervisor vulnerabilities:** CVE dalam hypervisor adalah sangat kritis karena dapat memungkinkan VM escape. Contoh historis: CVE-2018-3646 (L1TF/Foreshadow — Intel CPU side-channel yang mempengaruhi hypervisor), VENOM (CVE-2015-3456, vulnerability dalam virtual floppy disk controller).

2. **VM management interface:** API management seperti VMware vSphere API, libvirt, atau Proxmox API harus diamankan dengan ketat — kompromi pada management plane memberikan kontrol penuh atas semua VM.

3. **Shared CPU resources — side-channel attacks:** Prosesor modern berbagi cache antara VM. Serangan seperti Spectre/Meltdown dan L1TF mengeksploitasi fitur microarchitectural yang dibagi ini untuk "membaca" memori VM lain.

4. **Virtual networking:** Virtual switch (vSwitch) yang tidak terkonfigurasi dengan benar dapat memungkinkan traffic antar VM yang seharusnya terisolasi.

### 4.3 Keamanan Hypervisor — NIST SP 800-125 Guidance

NIST SP 800-125 memberikan panduan keamanan untuk lingkungan full virtualization:

**Rekomendasi utama:**
1. **Minimal hypervisor installation:** Instal hanya komponen yang diperlukan; setiap layanan tambahan memperluas attack surface
2. **Hypervisor patching:** Patch hypervisor secepat patch OS — jangan anggap hypervisor lebih stabil dan kurang memerlukan update
3. **Secure management network:** Management traffic (vSphere, Hyper-V Manager, libvirt) harus di-isolasi dalam network terpisah, tidak dapat diakses dari VM guest
4. **VM isolation enforcement:** Pastikan VM tidak dapat berkomunikasi satu sama lain kecuali melalui path yang explicitly defined dan monitored
5. **Audit logging:** Semua operasi management (start/stop VM, snapshot, network change) harus dicatat

```
NIST SP 800-125 Security Principles untuk Virtualization:
┌─────────────────────────────────────────┐
│  Physical Hardware                       │
├─────────────────────────────────────────┤
│  Hypervisor (Trust Anchor — KRITIS)     │
├────────────┬────────────┬───────────────┤
│  VM 1      │  VM 2      │  VM 3         │
│ (Web)      │ (DB)       │ (Dev/Test)    │
│            │            │               │
│ vNIC-1     │ vNIC-2     │ vNIC-3        │
├────────────┴────────────┴───────────────┤
│  Virtual Switch (vSwitch)               │
│  [Traffic antara VM dikontrol di sini]  │
└─────────────────────────────────────────┘

Management Network (TERPISAH dari guest VM network):
Administrator → Management API → Hypervisor (authenticated, encrypted, audited)
```

### 4.4 Asset Mapping dalam Infrastruktur Virtual

Pemetaan aset dalam infrastruktur virtual harus mencakup:

| Kategori Aset | Contoh | Pemilik | Klasifikasi Data | Trust Level |
|---|---|---|---|---|
| Hypervisor | ESXi host, KVM node | Infrastructure Team | N/A (software) | Highest Trust |
| Management API | vCenter, Proxmox API | Infrastructure Team | Akses istimewa | Restricted |
| VM — Production | web-01, db-01 | App Teams | Varies | Per-VM policy |
| VM — Management | jumpbox, monitoring | Security Team | Moderate | Trusted |
| Virtual Network | vSwitch, VLAN 100-200 | Network Team | N/A (infra) | Per-VLAN |
| VM Disk Images | .vmdk, .qcow2 files | Storage Admin | Sesuai isi VM | Protected |
| VM Snapshots | Backup snapshots | Backup Admin | Sesuai isi VM | Protected |

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph PHYSICAL["Physical Layer"]
        HW["Server Hardware:\nCPU, RAM, NIC, Storage"]
    end
    
    subgraph HYPERVISOR["Hypervisor Layer (Trust Boundary)"]
        HV["Type 1 Hypervisor\n(ESXi / KVM / Hyper-V)"]
        MGMT_API["Management API\n(vSphere API / libvirt)"]
        VSWITCH["Virtual Switch\n(vSwitch / OVS)"]
    end
    
    subgraph VMs["Guest VMs (Isolated)"]
        VM1["VM 1 - Web\nOS: Ubuntu 22.04\nvNIC: VLAN 100"]
        VM2["VM 2 - Database\nOS: Rocky Linux\nvNIC: VLAN 200"]
        VM3["VM 3 - Dev/Test\nOS: Windows 10\nvNIC: VLAN 300"]
    end
    
    subgraph MGMT["Management Network (Isolated)"]
        ADMIN["Admin Workstation\n(MFA, VPN required)"]
    end
    
    HW --> HV
    HV --> VM1
    HV --> VM2
    HV --> VM3
    VM1 & VM2 & VM3 --> VSWITCH
    HV --> MGMT_API
    MGMT_API --> ADMIN
    
    classDef critical fill:#ff6b6b,color:#fff
    classDef vm fill:#74b9ff
    classDef mgmt fill:#55efc4
    class HV,MGMT_API critical
    class VM1,VM2,VM3 vm
    class ADMIN mgmt
```

## 6. Contoh Terapan

**Skenario: Organisasi menjalankan 50 VM di atas 3 host ESXi tanpa dedicated management network**

Masalah yang teridentifikasi:
- Management traffic (vSphere API) berjalan di network yang sama dengan VM produksi
- Snapshot disimpan di storage yang sama dengan VM disk (tidak ada isolasi)
- Hypervisor tidak dipatch dalam 8 bulan terakhir (3 CVE high severity pending)
- Tidak ada audit logging untuk operasi management

Rekomendasi berdasarkan NIST SP 800-125:
1. Pisahkan management network ke VLAN dedicated (misalnya VLAN 999, tidak routable dari VM network)
2. Implementasikan MFA untuk akses vSphere
3. Segera patch hypervisor: prioritaskan CVE dengan CVSS ≥ 7.0
4. Aktifkan audit logging di vCenter: log semua event ke SIEM
5. Pisahkan storage backup/snapshot ke datastore terpisah dengan akses restricted

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Mengidentifikasi attack surface dan memetakan aset dalam environment virtualisasi.

**Environment:** Local VM menggunakan VirtualBox atau QEMU/KVM yang diinstal pada laptop lab (diotorisasi).

**Langkah:**
1. Identifikasi hypervisor yang digunakan di lab: versi, tipe, status patch.
2. Buat asset map: daftar semua VM yang berjalan, network yang digunakan, data apa yang ada di dalamnya.
3. Evaluasi: apakah management API terisolasi dari VM network?
4. Cek konfigurasi vSwitch: apakah ada VM yang seharusnya tidak bisa berkomunikasi tapi bisa?
5. Dokumen dalam format: Architecture Map dengan trust boundary yang jelas.

**Output:** Draft Architecture Map — bagian pertama dari Eval-1.

**Catatan etika:** Semua analisis dilakukan hanya pada lab environment milik sendiri atau yang diotorisasi dosen.

## 8. Latihan Pemahaman

1. **(C2)** Jelaskan perbedaan fundamental antara hypervisor Type 1 dan Type 2 dari perspektif attack surface. Mana yang lebih aman untuk deployment produksi dan mengapa?

2. **(C4)** Sebuah organisasi memiliki VM produksi dan VM development yang berjalan di hypervisor yang sama. VM development digunakan oleh tim yang tidak memiliki akses ke sistem produksi. Identifikasi 3 risiko keamanan dari skenario ini dan rekomendasi mitigasinya.

3. **(C3)** Mengapa "hypervisor patching" diperlakukan lebih mendesak daripada patching OS biasa dalam konteks keamanan enterprise?

## 9. Latihan Terapan / Studi Kasus

Sebuah perusahaan fintech menjalankan semua sistem (produksi, staging, development, testing) di atas 2 host KVM. Anda diminta melakukan review awal. Berdasarkan prinsip-prinsip NIST SP 800-125: (a) buatlah daftar pertanyaan yang harus dijawab untuk menilai keamanan environment ini; (b) identifikasi risiko tertinggi yang kemungkinan ada; (c) rekomendasikan arsitektur yang lebih aman dengan justifikasi.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Type 1 (bare-metal): berjalan langsung di hardware tanpa OS host → attack surface lebih kecil (tidak ada OS host yang bisa dikompromis), performa lebih baik, digunakan dalam produksi. Type 2 (hosted): berjalan di atas OS host → attack surface lebih besar (kerentanan OS host + hypervisor), lebih mudah di-install dan cocok untuk lab/development. Untuk produksi, Type 1 lebih aman karena: (a) tidak ada layer OS host yang bisa menjadi attack vector; (b) vendor menjaga minimal footprint; (c) management tools terpisah dari workload.

**Soal 2:** Tiga risiko: (a) **VM escape dari development ke production** — jika terdapat vulnerability dalam hypervisor, proses di VM development berpotensi mengakses memori VM produksi; mitigasi: separasi ke host fisik berbeda untuk workload produksi dan non-produksi. (b) **Side-channel attack** — developer dengan akses ke VM development dapat berpotensi mengekstrak informasi dari CPU cache yang dibagi dengan VM produksi; mitigasi: aktifkan CPU scheduling isolation, pertimbangkan dedicated NUMA node. (c) **Management plane cross-contamination** — jika management API dapat diakses dari VM development, developer berpotensi mempengaruhi VM produksi melalui API; mitigasi: isolasi management network.

**Soal 3:** Karena hypervisor adalah "trust anchor" untuk semua VM yang berjalan di atasnya. Sebuah CVE kritis dalam hypervisor (seperti VM escape vulnerability) berpotensi mengekspos SEMUA VM sekaligus, tidak hanya satu sistem. Selain itu, hypervisor patch seringkali memerlukan downtime yang direncanakan (karena harus me-live migrate VM dulu) — sehingga penundaan patching lebih berisiko. Dibandingkan OS biasa di mana kompromi hanya mempengaruhi satu sistem, kompromi hypervisor memiliki "blast radius" yang jauh lebih besar.

**Studi Kasus:** (a) Pertanyaan kunci: Versi KVM berapa? Ada CVE pending? Apakah management API terisolasi? Bagaimana VM produksi dan development dipisahkan secara network? Apakah ada VLAN separation? Bagaimana akses ke host KVM dikontrol (SSH, MFA)? Apakah ada audit log untuk operasi VM? (b) Risiko tertinggi: tidak ada isolasi antara lingkungan produksi dan non-produksi — ini adalah single biggest risk. Jika developer VM dikompromis, ada potensi pivot ke produksi melalui shared hypervisor. (c) Arsitektur yang direkomendasikan: setidaknya 1 host KVM dedicated untuk produksi saja (dengan akses management sangat restricted), 1 host KVM untuk staging + testing, dan environment development di laptop masing-masing developer atau cloud sandbox terisolasi. Seluruh management traffic melalui VLAN dedicated yang hanya accessible dari admin workstation dengan MFA.

## 11. Ringkasan Bab

Virtualisasi menggunakan hypervisor (Type 1 atau Type 2) untuk menjalankan multiple VM dengan isolasi dari hardware yang sama. Attack surface virtualisasi mencakup hypervisor vulnerabilities, VM escape, side-channel attacks, management API, dan virtual networking. NIST SP 800-125 merekomendasikan: minimal hypervisor installation, dedicated management network, aggressive patching, VM network isolation, dan audit logging. Asset mapping harus mencakup semua komponen: hypervisor, management API, VM, virtual network, dan storage.

## 12. Refleksi Profesional

1. Dalam industri, sering terjadi trade-off antara keamanan virtualisasi (yang mungkin menuntut separasi fisik untuk workload kritis) dan efisiensi (yang mendorong konsolidasi sebanyak mungkin VM ke satu host). Sebagai seorang arsitek keamanan, bagaimana Anda meyakinkan stakeholder bisnis bahwa investasi dalam isolasi fisik yang lebih ketat, meskipun lebih mahal, justified dari perspektif risk management?


---

# BAB 2 — CLOUD ARCHITECTURE, SHARED RESPONSIBILITY, DAN TRUST BOUNDARY

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menjelaskan model layanan cloud (IaaS/PaaS/SaaS/FaaS) dan implikasi keamanannya
- Menganalisis shared responsibility model untuk setiap model layanan
- Memetakan trust boundary dan data flow dalam arsitektur cloud
- Mengidentifikasi risiko multi-tenancy

*Berkaitan dengan Sub-CPMK-1, Eval-1 (10%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud Architecture] --> B[Service Models]
    B --> B1["IaaS: VM, Network, Storage\nCustomer mengatur OS ke atas"]
    B --> B2["PaaS: Runtime, DB, Platform\nCustomer hanya manage aplikasi"]
    B --> B3["SaaS: Aplikasi lengkap\nCustomer hanya manage data + akses"]
    B --> B4["FaaS/Serverless: Functions\nCustomer hanya manage kode"]
    A --> C[Shared Responsibility Model]
    C --> C1["Provider responsible:\nphysical, hypervisor, network fabric"]
    C --> C2["Customer responsible:\nOS config, IAM, data encryption,\nnetwork config, app security"]
    C --> C3["Shared:\nOS (IaaS), encryption-in-transit,\nidentity (PaaS)"]
    A --> D[Trust Boundary]
    D --> D1["Where provider trust ends:\nAPI boundary, management plane"]
    D --> D2["Where customer trust begins:\nVM OS, application, data"]
    D --> D3["Multi-tenancy risk:\nneighbor tenant via shared infra"]
    A --> E[Cloud Deployment Models]
    E --> E1["Public: AWS, Azure, GCP"]
    E --> E2["Private: on-prem cloud"]
    E --> E3["Hybrid: kombinasi"]
    E --> E4["Community: shared sector"]
```

## 3. Pengantar Kontekstual

Cloud computing merevolusi cara infrastruktur dikelola — dari kepemilikan fisik menuju konsumsi layanan. Namun, transisi ini membawa perubahan fundamental pada model keamanan: batas tanggung jawab menjadi tidak lagi jelas secara fisik. Kesalahpahaman tentang shared responsibility model adalah penyebab utama misconfiguration keamanan cloud. Organisasi yang mengasumsikan "cloud provider yang bertanggung jawab atas keamanan" tanpa memahami di mana batas itu berada, akan meninggalkan celah signifikan yang dapat dieksploitasi.

## 4. Landasan Teori

### 4.1 Model Layanan Cloud dan Implikasi Keamanan

**Infrastructure as a Service (IaaS):**
Customer mendapatkan akses ke infrastruktur virtual: VM, virtual network, storage. Customer bertanggung jawab atas segalanya mulai dari OS ke atas. Contoh: AWS EC2, Azure Virtual Machines, GCP Compute Engine.

Tanggung jawab keamanan customer di IaaS:
- OS patching dan hardening
- Network security group / firewall rules
- Data encryption at rest dan in transit
- IAM dan credential management
- Application security

**Platform as a Service (PaaS):**
Customer mendapatkan platform untuk menjalankan aplikasi — runtime, database, middleware. Provider mengelola OS, hypervisor, dan hardware. Contoh: AWS Elastic Beanstalk, Azure App Service, Google App Engine, Heroku.

Tanggung jawab keamanan customer di PaaS berkurang (tidak perlu patch OS), tapi area baru muncul:
- Application security
- Data classification dan encryption
- Identity management (API keys, service accounts)
- Dependency/library security (software supply chain)

**Software as a Service (SaaS):**
Provider menyediakan aplikasi lengkap. Customer hanya mengkonfigurasi dan menggunakannya. Contoh: Microsoft 365, Google Workspace, Salesforce.

Tanggung jawab keamanan customer di SaaS sangat terbatas tapi tetap penting:
- **Data governance:** apa yang disimpan di aplikasi, berapa lama
- **Access control:** siapa yang boleh akses, dengan hak apa
- **Account security:** MFA, password policy, privileged account management
- **Integration security:** bagaimana data mengalir antara SaaS dan sistem internal

**Function as a Service (FaaS/Serverless):**
Customer hanya mendeploy kode (functions). Provider mengelola execution environment, scaling, dan infrastruktur. Contoh: AWS Lambda, Azure Functions, Google Cloud Functions.

Implikasi keamanan serverless yang unik:
- Tidak ada OS untuk di-patch, tapi runtime dependencies perlu dimonitor
- Setiap function berjalan dalam isolated container (ephemeral) — forensic lebih sulit
- IAM untuk functions: permissions ke AWS services harus mengikuti least privilege
- Cold start timing dapat bocorkan informasi tentang function activity

### 4.2 Shared Responsibility Model

```
SHARED RESPONSIBILITY MODEL (AWS Analogy):

CUSTOMER RESPONSIBLE ("Security IN the Cloud"):
┌─────────────────────────────────────────────────────┐
│  Customer Data                                       │
│  Platform, Applications, Identity & Access Mgmt     │
│  OS, Network Configuration, Firewall               │  IaaS
│  Client-side Encryption, Server-side Encryption    │
└─────────────────────────────────────────────────────┘

AWS RESPONSIBLE ("Security OF the Cloud"):
┌─────────────────────────────────────────────────────┐
│  Compute │ Storage │ Database │ Networking          │
│  (Hardware/Infrastructure)                          │
├─────────────────────────────────────────────────────┤
│  Regions │ Availability Zones │ Edge Locations      │
└─────────────────────────────────────────────────────┘

CATATAN PENTING:
- IaaS: customer bertanggung jawab paling banyak
- PaaS: tanggung jawab dibagi lebih banyak ke provider
- SaaS: provider bertanggung jawab hampir semua infrastruktur,
        tapi customer tetap bertanggung jawab atas data dan akses
```

**Jebakan umum yang menyebabkan insiden cloud:**

1. **S3 bucket public secara tidak sengaja:** AWS tidak "default-protect" bucket — ini tanggung jawab customer. Ribuan data breach terjadi karena misconfiguration ini.

2. **EC2 instance tanpa security group restrictive:** Instance dengan port 22/3389 terbuka ke 0.0.0.0/0 adalah customer's responsibility — bukan AWS.

3. **Root account tanpa MFA:** Tanggung jawab penuh customer.

4. **Unencrypted EBS volumes:** Customer harus mengaktifkan enkripsi secara eksplisit.

### 4.3 Trust Boundary dalam Cloud Architecture

**Trust boundary** adalah garis demarkasi yang memisahkan komponen sistem yang memiliki tingkat kepercayaan berbeda. Dalam cloud architecture:

```mermaid
flowchart LR
    subgraph PROVIDER["Cloud Provider Trust Zone"]
        HW["Physical Hardware"]
        NET["Network Fabric"]
        HV["Hypervisor"]
        MGMT["Provider Management Plane"]
    end
    
    subgraph BOUNDARY["Trust Boundary (API)"]
        API["Cloud API Endpoint\n(IAM-controlled)"]
    end
    
    subgraph CUSTOMER["Customer Trust Zone"]
        VM_OS["VM OS"]
        APP["Application"]
        DATA["Customer Data"]
        IAM_C["Customer IAM\n(Access Control)"]
    end
    
    subgraph EXTERNAL["External (Untrusted)"]
        INTERNET["Internet / Users"]
        PARTNER["Partner APIs"]
    end
    
    HV --> API
    API --> VM_OS
    VM_OS --> APP
    APP --> DATA
    INTERNET --> APP
    PARTNER --> APP
    
    classDef provider fill:#74b9ff
    classDef customer fill:#55efc4
    classDef external fill:#ff6b6b,color:#fff
    class HW,NET,HV,MGMT provider
    class VM_OS,APP,DATA,IAM_C customer
    class INTERNET,PARTNER external
```

### 4.4 Multi-Tenancy Risk

Public cloud adalah infrastruktur yang dibagi antara ribuan customer ("tenants"). Risiko multi-tenancy:

1. **Noisy neighbor:** Tenant lain mengkonsumsi resource berlebihan, mempengaruhi performa. Bukan risiko keamanan murni, tapi dapat digunakan sebagai denial-of-service.

2. **Side-channel attacks:** Secara teori, tenant berbagi hardware yang sama. Side-channel attacks seperti Spectre/Meltdown dapat (secara sangat terbatas) mengekspos informasi lintas tenant. Cloud provider secara aktif memitigasi ini melalui hypervisor patching dan CPU microupdate.

3. **Management plane leakage:** Jika terdapat bug dalam cloud provider's management plane, data konfigurasi satu tenant mungkin terekspos ke tenant lain. Sangat jarang terjadi dan merupakan tanggung jawab cloud provider untuk memperbaiki.

**Mitigasi risiko multi-tenancy (dari perspektif customer):**
- Enkripsi semua data sensitif dengan kunci yang dikontrol customer (CMK — Customer Managed Keys)
- Jangan bergantung hanya pada cloud provider's isolation — tambahkan enkripsi layer
- Untuk workload yang sangat sensitif: pertimbangkan dedicated instances (physical isolation)

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph DATA_FLOW["Data Flow Diagram — Cloud Architecture"]
        USER["End User\n(Browser/Mobile)"]
        CDN["CDN\n(CloudFront/Fastly)"]
        LB["Load Balancer\n(ALB/Azure LB)"]
        
        subgraph APP_TIER["Application Tier (Customer Zone)"]
            APP1["App Server 1\n(EC2/VM)"]
            APP2["App Server 2\n(EC2/VM)"]
        end
        
        subgraph DATA_TIER["Data Tier (Customer Zone)"]
            DB["Database\n(RDS/Azure SQL)"]
            CACHE["Cache\n(ElastiCache/Redis)"]
            STORAGE["Object Storage\n(S3/Blob)"]
        end
        
        subgraph MGMT_PLANE["Management Plane (API — Trust Boundary)"]
            IAM["IAM Service"]
            LOGGING["CloudTrail/Log"]
            KMS["Key Management\nService (KMS)"]
        end
        
        USER --> CDN --> LB
        LB --> APP1 & APP2
        APP1 & APP2 --> DB & CACHE & STORAGE
        APP1 & APP2 --> IAM & LOGGING & KMS
    end
    
    TRUST_BOUNDARY(["Trust Boundary:\nCustomer manages everything inside\nProvider manages physical infra"])
```

## 6. Contoh Terapan

**Analisis Shared Responsibility untuk Perusahaan Perbankan yang Menggunakan AWS IaaS:**

| Komponen | AWS Bertanggung Jawab | Bank Bertanggung Jawab |
|---|---|---|
| Keamanan fisik data center | ✓ | |
| Hypervisor patching | ✓ | |
| Network fabric AWS | ✓ | |
| OS di EC2 instance | | ✓ OS patching, hardening |
| Security Group rules | | ✓ Harus restrictive |
| Data encryption di RDS | | ✓ Harus aktifkan encryption |
| IAM user management | | ✓ MFA, least privilege |
| Kepatuhan regulasi data | | ✓ OJK compliance |
| Backup data nasabah | | ✓ Backup policy |
| DDoS protection (Shield Standard) | ✓ | |
| DDoS protection lanjutan (Shield Advanced) | Layanan opsional | ✓ Harus berlangganan dan konfigurasi |

**Kesimpulan:** Bank yang salah mengasumsikan "cloud provider yang urus keamanan" akan meninggalkan seluruh baris kanan tabel di atas tanpa proteksi yang memadai.

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Membuat shared responsibility analysis dan data flow diagram untuk skenario cloud organisasi.

**Aktivitas (berbasis skenario yang diberikan dosen — tidak perlu akun cloud nyata untuk bagian ini):**
1. Diberikan skenario: Startup e-commerce menggunakan AWS IaaS (EC2, RDS, S3) dan satu layanan SaaS (Gmail/Google Workspace untuk email). 
2. Buat tabel shared responsibility analysis untuk setiap layanan yang digunakan.
3. Buat data flow diagram yang menunjukkan alur data dari pelanggan ke database, dengan trust boundary yang jelas.
4. Identifikasi 3 trust boundary yang paling kritis dan jelaskan kontrol yang harus ada.

**Output:** Shared Responsibility Analysis + Data Flow Diagram — bagian dari Eval-1.

## 8. Latihan Pemahaman

1. **(C2)** Sebuah organisasi menggunakan SaaS untuk menyimpan data HR sensitif. Manajer IT menyatakan "keamanan sudah tanggungjawab vendor SaaS." Apa yang salah dengan pernyataan ini? Apa yang tetap menjadi tanggung jawab organisasi?

2. **(C4)** Mengapa model FaaS/serverless menghadirkan tantangan forensik yang unik dibandingkan IaaS? Apa implikasinya untuk incident response?

## 9. Latihan Terapan / Studi Kasus

Sebuah perusahaan manufaktur Indonesia akan memindahkan ERP mereka dari on-premises ke cloud. Data ERP mencakup data keuangan, data produksi, dan data karyawan (nama, gaji, NIK). Mereka mempertimbangkan tiga opsi: (a) IaaS — migrasi ERP ke EC2/VM cloud; (b) PaaS — gunakan managed database dan container service; (c) SaaS ERP — gunakan produk ERP cloud seperti SAP S/4HANA Cloud. Analisis implikasi shared responsibility, risiko data, dan rekomendasi untuk masing-masing opsi, dengan mempertimbangkan UU PDP No. 27/2022.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Pernyataan manajer IT salah karena shared responsibility SaaS masih menempatkan beberapa tanggung jawab pada customer: (a) **Access control** — siapa yang memiliki akun, hak apa yang mereka miliki, apakah ada akun yang tidak aktif; (b) **Data governance** — data apa yang boleh disimpan di SaaS ini, apakah SaaS ini sudah diotorisasi untuk menyimpan data HR, apakah sesuai UU PDP; (c) **Account security** — MFA untuk semua pengguna, terutama admin; (d) **Data retention** — berapa lama data disimpan, bagaimana jika ada karyawan resign; (e) **Integration security** — jika SaaS terintegrasi dengan sistem internal, bagaimana keamanan integrasi tersebut.

**Soal 2:** FaaS menghadirkan tantangan forensik: (a) **Ephemeral execution environment** — setiap invocation berjalan dalam container yang dimusnahkan setelah selesai, tidak ada "disk" yang bisa diimaging untuk forensik; (b) **Minimal logging by default** — tanpa konfigurasi eksplisit, sangat sedikit yang dicatat; (c) **Tidak ada persistent state** — state di memori hilang setelah invocation; (d) **Multi-layered execution** — function mungkin trigger function lain, membuat trace execution lebih kompleks. Implikasi untuk IR: (a) harus mengaktifkan comprehensive logging (CloudWatch Logs dengan log retention yang cukup) SEBELUM insiden terjadi; (b) forensic readiness harus dimulai dari desain, bukan reaktif; (c) korrelasi log dari berbagai sumber lebih kritis daripada di VM tradisional.

**Studi Kasus:** (a) IaaS: Tanggung jawab customer tertinggi — perlu tim yang capable untuk manage OS, patching, network security. Risiko: misconfiguration tinggi jika tim tidak berpengalaman. Untuk UU PDP: wajib enkripsi data karyawan, kontrol akses, dan mekanisme notifikasi breach. (b) PaaS: Reduced operational burden — tidak perlu patch OS. Risiko berkurang pada level infra tapi dependency/library security menjadi lebih kritis. (c) SaaS ERP: Vendor mengelola hampir semua. Kekhawatiran UU PDP: pastikan vendor memiliki sertifikasi yang relevan, DPA (Data Processing Agreement) yang jelas, dan data residency di Indonesia atau yurisdiksi yang diakui. Rekomendasi: untuk perusahaan manufaktur menengah tanpa tim security cloud yang matang, PaaS atau SaaS lebih aman operasionalnya, tapi harus dipastikan bahwa vendor memiliki komitmen hukum terhadap data protection sesuai UU PDP.

## 11. Ringkasan Bab

Cloud service models (IaaS/PaaS/SaaS/FaaS) mendefinisikan pembagian tanggung jawab keamanan antara provider dan customer. Semakin managed modelnya, semakin banyak tanggung jawab infrastruktur yang diambil alih provider — tapi tanggung jawab data, akses, dan aplikasi tetap pada customer. Trust boundary dalam cloud berada pada API layer. Multi-tenancy menghadirkan risiko teoretis yang dimitigasi oleh provider, tapi customer harus menambahkan enkripsi layer sendiri untuk data paling sensitif.

## 12. Refleksi Profesional

1. Beberapa regulasi Indonesia (seperti regulasi Bank Indonesia atau OJK untuk sektor keuangan) mewajibkan data tertentu disimpan di dalam wilayah Indonesia ("data localization"). Bagaimana hal ini mempengaruhi keputusan arsitektur cloud sebuah bank? Apakah solusi cloud publik internasional dapat memenuhi persyaratan ini, dan bagaimana memvalidasinya?

---

# BAB 3 — CONTAINER, ORCHESTRATION, DAN RISK SCENARIO ANALYSIS

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menjelaskan arsitektur container (namespace, cgroup, OCI image) dan perbedaannya dengan VM
- Memahami ekosistem orchestration Kubernetes dan komponen keamanannya
- Mengidentifikasi trust boundary dan attack surface spesifik container
- Menyusun risk scenario analysis untuk lingkungan container

*Berkaitan dengan Sub-CPMK-1, Eval-1 (10%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Container Architecture] --> B[Core Concepts]
    B --> B1["Namespace isolation:\nPID, Network, Mount, UTS, IPC, User"]
    B --> B2["cgroup resource control:\nCPU, Memory, Block I/O limits"]
    B --> B3["OCI Image:\nlayers, manifest, digest\nimmutable dan distributable"]
    A --> C[Container vs VM]
    C --> C1["VM: hardware-level isolation\nhypervisor, full OS"]
    C --> C2["Container: OS-level isolation\nshared kernel = smaller footprint\nbut larger blast radius"]
    A --> D[Kubernetes Architecture]
    D --> D1["Control Plane:\nAPI Server, Scheduler,\netcd, Controller Manager"]
    D --> D2["Worker Nodes:\nkubelet, kube-proxy,\nContainer Runtime"]
    D --> D3["Kubernetes Objects:\nPod, Deployment, Service,\nNetworkPolicy, RBAC"]
    A --> E[Container Security Threats]
    E --> E1["Vulnerable base image:\nCVE dalam OS packages"]
    E --> E2["Container escape:\nprivileged container,\nhostPath mount"]
    E --> E3["Lateral movement:\ndalam cluster via ServiceAccount"]
    E --> E4["Supply chain:\nmalicious image dari registry"]
```

## 3. Pengantar Kontekstual

Container merevolusi deployment software dengan menyediakan portabilitas dan efisiensi yang jauh melampaui VM. Namun, arsitektur container menghadirkan model isolasi yang fundamental berbeda dari VM — container berbagi kernel host OS, sehingga isolasi lebih tipis dan serangan "container escape" lebih mudah jika container tidak dikonfigurasi dengan benar. Kubernetes sebagai orchestrator de facto menambah kompleksitas: cluster Kubernetes yang besar dapat memiliki ratusan Pod, RBAC yang kompleks, dan banyak titik konfigurasi yang jika salah dapat menjadi entry point bagi attacker.

## 4. Landasan Teori

### 4.1 Arsitektur Container — Mekanisme Isolasi

**Linux Namespaces:**
Container menggunakan Linux namespaces untuk mengisolasi setiap container ke dalam "view" tersendiri dari sistem:

| Namespace | Yang Diisolasi | Implikasi Keamanan |
|---|---|---|
| PID | Process IDs — container hanya melihat proses-nya sendiri | Proses di luar container tidak visible |
| Network | Interface jaringan, routing table, firewall rules | Container memiliki network stack terpisah |
| Mount | Filesystem mounts | Container tidak bisa melihat host filesystem secara default |
| UTS | Hostname dan domain name | Container dapat memiliki hostname sendiri |
| IPC | IPC objects (shared memory, semaphores) | Isolasi shared memory antar container |
| User | UID/GID mapping | Root dalam container ≠ root di host (jika user namespace aktif) |

**cgroups (Control Groups):**
Membatasi resources yang dapat dikonsumsi oleh setiap container. Ini adalah mekanisme untuk:
- Mencegah "noisy neighbor" — satu container yang mengkonsumsi semua CPU/RAM
- Mencegah DoS melalui resource exhaustion
- Menetapkan resource limits yang enforceable

```yaml
# Contoh resource limits dalam Kubernetes Pod spec:
resources:
  requests:        # minimum yang dijamin
    memory: "64Mi"
    cpu: "250m"    # 250 millicores = 0.25 CPU
  limits:          # maksimum yang boleh dikonsumsi
    memory: "128Mi"
    cpu: "500m"
# PENTING: tanpa limits, container bisa mengkonsumsi semua resource node!
```

**OCI Image Architecture:**
OCI (Open Container Initiative) mendefinisikan standar image format:

```
Image Layer Architecture:
┌──────────────────────────────────┐
│  Application Layer (R/W)         │ ← Dibuat saat container run
├──────────────────────────────────┤
│  App Dependencies (R/O)          │ ← Image layer
├──────────────────────────────────┤
│  Runtime Libraries (R/O)         │ ← Image layer
├──────────────────────────────────┤
│  Base OS Image (R/O)             │ ← Image layer (Ubuntu, Alpine, dll)
└──────────────────────────────────┘

Setiap layer diidentifikasi dengan SHA256 digest — immutable!
Perubahan dalam image = layer baru dengan digest berbeda
```

### 4.2 Container vs VM — Implikasi Keamanan

| Aspek | Virtual Machine | Container |
|---|---|---|
| Isolasi level | Hardware (hypervisor) | OS (shared kernel) |
| Attack surface escape | VM escape (sangat sulit) | Container escape (lebih mudah jika misconfigured) |
| Overhead | Lebih besar (full OS per VM) | Minimal (shared kernel) |
| Boot time | Menit | Detik |
| Blast radius jika escape | 1 host, semua VM di atasnya | 1 host, semua container di atasnya |
| Forensic artifacts | Disk image, memory dump | Ephemeral — harus konfigurasi logging eksplisit |

**Container escape scenarios yang harus dipahami (untuk defensive purposes):**
- **Privileged container:** Container yang dijalankan dengan `--privileged` flag mendapatkan akses hampir penuh ke host system call interface. Ini adalah misconfiguration paling umum dan paling berbahaya.
- **hostPath mount:** Jika container di-mount direktori host (`/` atau `/etc`), container dapat memodifikasi host filesystem.
- **Exposed Docker socket:** Jika `/var/run/docker.sock` di-mount ke dalam container, proses dalam container dapat mengontrol Docker daemon di host.

### 4.3 Kubernetes Architecture dan Security Components

**Control Plane (Brain of Kubernetes):**
```
kube-apiserver: Pintu masuk semua operasi. SEMUA komunikasi ke cluster
               melalui API server. Security: TLS mutual auth, RBAC, Admission Control.

etcd:          Key-value store yang menyimpan seluruh cluster state.
               JIKA etcd dikompromis: seluruh cluster state diketahui attacker.
               Security: enkripsi at rest, mutual TLS, akses hanya dari API server.

kube-scheduler: Menentukan di node mana Pod akan berjalan.
               Security: bisa dipengaruhi oleh Pod affinity/taint yang berbahaya.

controller-manager: Menjalankan controller loops (Deployment, ReplicaSet, dll).
```

**Worker Nodes (Where workloads run):**
```
kubelet:       Agent yang berjalan di setiap node. Menerima instruksi dari API server
               dan mengeksekusi Pods. Security: TLS, RBAC, Node Authorization.

kube-proxy:   Mengelola iptables/ipvs untuk Service routing.

Container Runtime: Docker, containerd, CRI-O — menjalankan container actual.
```

**Kubernetes Objects yang kritis untuk keamanan:**

```yaml
# NetworkPolicy — mengontrol traffic antar Pod
# Default Kubernetes: semua Pod bisa berkomunikasi dengan semua Pod (BERBAHAYA!)
# Network Policy mengubah ini:
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: deny-all-default
  namespace: production
spec:
  podSelector: {}    # Berlaku untuk semua Pod di namespace ini
  policyTypes:
  - Ingress
  - Egress
  # Tidak ada rules = deny all ingress dan egress
  # Harus tambahkan rules secara eksplisit untuk traffic yang diizinkan
```

### 4.4 Risk Scenario Analysis untuk Container Environment

**Threat Model — Container/Kubernetes:**

Menggunakan STRIDE untuk container threats:

| Threat | Contoh dalam Container Context | Kontrol |
|---|---|---|
| Spoofing | Impersonasi ServiceAccount dengan token curian | RBAC minimum, token projection, rotation |
| Tampering | Modifikasi image di registry setelah build | Image signing (Cosign), digest pinning |
| Repudiation | Tidak ada audit log untuk API calls | Audit logging di kube-apiserver |
| Information Disclosure | Secret dalam environment variable atau log | Secrets management (Vault), scan untuk secret exposure |
| Denial of Service | Container tanpa resource limits mengkonsumsi semua CPU/RAM | LimitRange, ResourceQuota |
| Elevation of Privilege | Container dengan hostPID atau privileged flag | Pod Security Standards (Restricted profile) |

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph K8S_CLUSTER["Kubernetes Cluster"]
        subgraph CONTROL_PLANE["Control Plane"]
            API["kube-apiserver\n(TLS + RBAC + Admission Control)"]
            ETCD["etcd\n(Encrypted at rest)"]
            SCHED["kube-scheduler"]
            CM["controller-manager"]
        end
        
        subgraph NODE1["Worker Node 1"]
            KUBELET1["kubelet"]
            subgraph NS_PROD["Namespace: production"]
                POD1["Pod: web-app\n(Restricted PSS)"]
                POD2["Pod: api-server\n(Restricted PSS)"]
            end
        end
        
        subgraph NODE2["Worker Node 2"]
            KUBELET2["kubelet"]
            subgraph NS_DATA["Namespace: data"]
                POD3["Pod: database\n(Baseline PSS)"]
            end
        end
        
        NP["NetworkPolicy:\nProduction ↔ Data\nhanya TCP 5432"]
        RBAC["RBAC:\nEach NS has dedicated ServiceAccount\nwith minimal permissions"]
    end
    
    DEV["Developer\n(kubectl)"] --> API
    API --> ETCD & SCHED & CM
    API --> KUBELET1 & KUBELET2
    KUBELET1 --> POD1 & POD2
    KUBELET2 --> POD3
```

## 6. Contoh Terapan

**Risk Scenario: Privilege Escalation via Misconfigured Kubernetes ServiceAccount**

```yaml
# Skenario: ServiceAccount dengan ClusterAdmin yang terlalu luas
# (ini adalah CONTOH apa yang JANGAN dilakukan)
apiVersion: v1
kind: ServiceAccount
metadata:
  name: my-app-sa
  namespace: production
---
# BERBAHAYA: ClusterRoleBinding memberikan cluster-admin ke app SA!
apiVersion: rbac.authorization.k8s.io/v1
kind: ClusterRoleBinding
metadata:
  name: my-app-admin  # Nama yang menyesatkan
roleRef:
  apiGroup: rbac.authorization.k8s.io
  kind: ClusterRole
  name: cluster-admin  # Hak tertinggi dalam Kubernetes!
subjects:
- kind: ServiceAccount
  name: my-app-sa
  namespace: production
```

**Risiko:** Jika container yang menggunakan `my-app-sa` dikompromis, attacker mendapatkan cluster-admin — dapat membuat/menghapus Pod di semua namespace, membaca Secrets, mengubah NetworkPolicy, dll.

**Mitigasi (yang seharusnya dilakukan):**

```yaml
# Buat Role yang hanya memberikan akses minimal yang diperlukan
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  name: my-app-role
  namespace: production
rules:
- apiGroups: [""]
  resources: ["configmaps"]
  verbs: ["get", "list"]  # Hanya baca ConfigMap yang diperlukan
# Tidak lebih, tidak kurang!
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menyusun risk scenario analysis untuk environment container/Kubernetes.

**Aktivitas (berbasis skenario, tidak memerlukan cluster nyata untuk bagian ini):**
1. Diberikan deskripsi arsitektur: aplikasi microservices dengan 5 services di Kubernetes, menggunakan 2 namespace (frontend, backend), dengan external API gateway.
2. Buat threat model menggunakan STRIDE untuk environment ini.
3. Identifikasi 5 risk scenario terburuk (berdasarkan likelihood × impact).
4. Untuk setiap risk scenario: identifikasi kontrol yang harus ada, dan apakah kontrol tersebut bersifat preventif, detektif, atau korektif.

**Output:** Risk Scenario Analysis — bagian terakhir dari Eval-1.

## 8. Latihan Pemahaman

1. **(C2)** Mengapa menjalankan container sebagai `privileged` dianggap sebagai misconfiguration yang sangat berbahaya? Apa perbedaannya dengan menjalankan container sebagai root user (UID 0)?

2. **(C4)** Sebuah developer ingin me-mount direktori `~/.kube/config` dari host ke dalam container untuk memudahkan debugging. Identifikasi risiko dari tindakan ini dan alternatif yang lebih aman.

3. **(C3)** Jelaskan peran `etcd` dalam Kubernetes dan mengapa keamanannya sangat kritis. Apa yang harus diproteksi?

## 9. Latihan Terapan / Studi Kasus

Anda diminta mereview arsitektur Kubernetes dari tim DevOps sebuah startup. Anda menemukan: (a) semua Pod berjalan sebagai root; (b) default ServiceAccount tidak di-disable, dan beberapa Pod menggunakannya; (c) tidak ada NetworkPolicy yang terdefinisi; (d) secret database disimpan sebagai plaintext dalam environment variables; (e) registry image tidak menggunakan image signing. Untuk setiap temuan: klasifikasikan severity (Critical/High/Medium), jelaskan implikasi keamanan konkret, dan berikan rekomendasi perbaikan spesifik yang dapat langsung diimplementasikan.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Perbedaan `privileged` vs root user: (a) Container yang berjalan sebagai **root user (UID 0)** di dalam container: ini sudah berbahaya — jika terdapat path escape, attacker memiliki akses root ke host. Namun, masih ada beberapa isolation dari namespaces. (b) Container dengan flag `--privileged` (atau `securityContext.privileged: true` di K8s): ini menghilangkan hampir semua namespace isolation. Container mendapatkan akses penuh ke host's device filesystem (`/dev`), semua Linux capabilities, dan dapat memodifikasi iptables rules, mount filesystems, dll. Ini secara efektif adalah akses root ke host system. `privileged` jauh lebih berbahaya dari sekadar root user karena namespaces yang seharusnya melindungi tidak aktif.

**Soal 2:** Mount `~/.kube/config` ke dalam container memberikan container akses penuh ke cluster Kubernetes dengan credential pengguna yang bersangkutan. Jika aplikasi dalam container dikompromis, attacker mendapatkan akses kubectl ke cluster. Alternatif yang lebih aman: (a) gunakan **ServiceAccount** dengan hak minimal yang spesifik untuk kebutuhan debugging; (b) gunakan **kubectl port-forward** dari luar container untuk akses sementara; (c) gunakan **ephemeral containers** (kubectl debug) untuk debugging tanpa memodifikasi Pod utama.

**Soal 3:** `etcd` menyimpan seluruh state cluster Kubernetes: semua Pod definitions, ServiceAccount tokens, Secret objects (termasuk service account tokens, TLS certificates), ConfigMaps, NetworkPolicy, RBAC definitions. Jika etcd dikompromis: (a) attacker dapat membaca semua Secrets; (b) dapat memodifikasi cluster state (tambah Pod, ubah RBAC); (c) memiliki informasi lengkap tentang seluruh infrastruktur. Proteksi yang diperlukan: (a) enkripsi Secrets at rest dalam etcd; (b) TLS mutual authentication antara API server dan etcd; (c) etcd hanya accessible dari kube-apiserver, tidak dari node lain atau eksternal; (d) backup etcd secara regular dengan enkripsi backup.

**Studi Kasus:** (a) Semua Pod sebagai root: **CRITICAL** — container sebagai root memperluas blast radius jika terjadi container escape; mitigasi: `runAsNonRoot: true`, `runAsUser: 1000+` dalam PodSecurityContext. (b) Default ServiceAccount: **HIGH** — default SA memiliki token yang di-mount secara otomatis, memberikan minimal cluster access yang tidak diperlukan; mitigasi: `automountServiceAccountToken: false` untuk Pod yang tidak perlu API access, buat SA khusus per aplikasi. (c) Tidak ada NetworkPolicy: **HIGH** — semua Pod bisa berkomunikasi dengan semua Pod (east-west traffic unrestricted); mitigasi: mulai dengan default-deny, kemudian allow-list yang specific. (d) Secret sebagai env variable: **HIGH** — env variables muncul dalam logs, crash reports, dan dapat dibaca oleh proses anak; mitigasi: gunakan Kubernetes Secrets dengan volume mount (bukan env var), atau gunakan eksternal secret manager (HashiCorp Vault). (e) Tidak ada image signing: **MEDIUM** — tidak ada jaminan bahwa image yang dijalankan adalah image yang sama yang di-build; mitigasi: implementasikan Cosign + Policy controller untuk enforce image signature verification.

## 11. Ringkasan Bab

Container menggunakan Linux namespaces dan cgroups untuk isolasi yang lebih ringan dari VM, dengan shared kernel sebagai konsekuensinya. OCI image menggunakan layer yang immutable dan identifiable via digest. Kubernetes mengelola container orchestration dengan control plane (API server, etcd) dan worker nodes (kubelet). Risk scenario analysis untuk container mencakup: container escape via privileged/hostPath, ServiceAccount token abuse, lateral movement dalam cluster, supply chain compromise melalui malicious image.

## 12. Refleksi Profesional

1. Model container ephemeral (container dimusnahkan dan dibuat baru setiap deployment) menghadirkan tantangan fundamental untuk forensic investigation — saat insiden terjadi, evidence mungkin sudah hilang. Sebagai seorang profesional keamanan siber, bagaimana Anda merancang "forensic readiness" untuk environment Kubernetes bahkan sebelum insiden terjadi? Apa kontrol minimal yang harus ada?


---

# BAB 4 — IDENTITY AND ACCESS MANAGEMENT DI CLOUD

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menganalisis model IAM cloud provider (AWS IAM, Azure AD, GCP IAM)
- Menerapkan prinsip least privilege dalam desain IAM cloud
- Mengidentifikasi IAM misconfigurations yang umum dan risikonya
- Merancang IAM baseline yang aman dan dapat diaudit

*Berkaitan dengan Sub-CPMK-2, Eval-2 (20%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud IAM] --> B[Identity Types]
    B --> B1["Human Identity:\nuser, admin, developer\n→ MFA required"]
    B --> B2["Machine Identity:\nservice account, instance role,\nworkload identity\n→ short-lived credentials"]
    B --> B3["Federated Identity:\nSSO, SAML, OIDC\n→ centralized IdP"]
    A --> C[IAM Concepts]
    C --> C1["Authentication:\nWho are you? (credentials, MFA)"]
    C --> C2["Authorization:\nWhat can you do? (policies, roles)"]
    C --> C3["Principal:\nEntity yang melakukan action"]
    C --> C4["Resource:\nCloud resource yang diakses"]
    C --> C5["Condition:\nKonteks (IP, time, MFA required)"]
    A --> D[Principle of Least Privilege]
    D --> D1["Minimum permissions\nuntuk task yang diperlukan"]
    D --> D2["Just-in-time access:\ntemporary elevation"]
    D --> D3["Role separation:\ndev ≠ prod access"]
    D --> D4["Regular access review:\nrevoke yang tidak terpakai"]
    A --> E[Common Misconfigurations]
    E --> E1["AdministratorAccess\nuntuk semua developer"]
    E --> E2["Access key tidak dirotasi\natau tidak dibutuhkan"]
    E --> E3["Tidak ada MFA\nuntuk root/admin"]
    E --> E4["Wildcard * resources\ndalam policy"]
```

## 3. Pengantar Kontekstual

Jika ada satu kontrol keamanan cloud yang paling sering gagal, itu adalah IAM. Menurut laporan Verizon DBIR dan Gartner, mayoritas data breach di cloud melibatkan credential yang dikompromis atau IAM yang terlalu permisif. Ini bukan karena cloud provider tidak menyediakan tools IAM yang baik — AWS IAM, Azure AD, dan GCP IAM adalah sangat capable. Masalahnya adalah kompleksitas: IAM di cloud jauh lebih granular dari IAM on-premises, dan konfigurasi yang salah sangat mudah dibuat tanpa disadari.

## 4. Landasan Teori

### 4.1 Model IAM Cloud — Konsep Fundamental

**Principal:** Entity yang melakukan tindakan — user, role, service account, atau AWS service.

**Policy:** Dokumen JSON (atau YAML) yang mendefinisikan apa yang boleh dilakukan principal terhadap resource. Terdiri dari: Effect (Allow/Deny), Action (apa yang boleh dilakukan), Resource (pada resource apa), Condition (kondisi tambahan).

**AWS IAM Policy Example:**
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowS3ReadProductionBucket",
      "Effect": "Allow",
      "Action": [
        "s3:GetObject",
        "s3:ListBucket"
      ],
      "Resource": [
        "arn:aws:s3:::company-production-data",
        "arn:aws:s3:::company-production-data/*"
      ],
      "Condition": {
        "Bool": {
          "aws:MultiFactorAuthPresent": "true"
        }
      }
    }
  ]
}
```

**Apa yang benar dari policy di atas:**
- Spesifik: hanya `GetObject` dan `ListBucket` — bukan `*`
- Spesifik resource: hanya bucket production tertentu — bukan `*`
- Kondisi MFA: hanya berlaku jika pengguna sudah melakukan MFA

**Apa yang harus dihindari:**
```json
// JANGAN LAKUKAN INI — policy yang terlalu luas:
{
  "Effect": "Allow",
  "Action": "*",           // Semua action!
  "Resource": "*"          // Semua resource!
}
// Ini sama dengan memberikan AdministratorAccess — prinsip least privilege dilanggar
```

### 4.2 Human Identity vs Machine Identity

**Human Identity:**
- User manusia yang mengakses cloud console atau CLI
- Harus menggunakan MFA — terutama untuk privileged accounts
- Credential: password + MFA untuk console, access key untuk CLI (disarankan menggunakan SSO/role assumption, bukan long-lived access key)
- Root account AWS: hanya untuk billing dan account-level tasks, jangan digunakan untuk operasi sehari-hari

**Machine Identity (Service Account / Instance Role):**
- Aplikasi atau service yang mengakses cloud resources programmatically
- Harus menggunakan short-lived credentials (role assumption, workload identity) — bukan long-lived access keys yang di-embed dalam kode
- Contoh yang benar: EC2 instance menggunakan IAM Instance Role (credential dirotasi otomatis oleh AWS) → tidak perlu access key dalam aplikasi
- Contoh yang salah: access key di-hardcode dalam kode atau environment variable → ini adalah common cause of breach

```python
# CARA YANG SALAH — hardcoded credentials:
import boto3
client = boto3.client('s3',
    aws_access_key_id='AKIAIOSFODNN7EXAMPLE',       # JANGAN LAKUKAN INI!
    aws_secret_access_key='wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY'  # BAHAYA!
)

# CARA YANG BENAR — gunakan Instance Role atau environment credentials:
import boto3
client = boto3.client('s3')  # Secara otomatis menggunakan Instance Role
# Boto3 akan otomatis mengambil credentials dari Instance Metadata Service
# Credential ini short-lived dan di-rotasi otomatis oleh AWS
```

### 4.3 Prinsip Least Privilege dalam Cloud IAM

**Least Privilege** berarti memberikan hak akses minimum yang diperlukan untuk menyelesaikan tugas yang dimaksud — tidak lebih, tidak kurang.

**Praktik least privilege:**

1. **Start restrictive, add as needed:** Mulai dengan no permissions, tambahkan hanya yang diperlukan saat ada kebutuhan nyata yang terdokumentasi.

2. **Role separation:** Developer tidak boleh memiliki akses langsung ke production. Gunakan role yang berbeda untuk dev/staging/production environments.

3. **Just-in-time (JIT) access:** Untuk tindakan privileged (seperti emergency access ke produksi), gunakan mekanisme JIT yang memberikan akses sementara dengan batas waktu dan audit trail.

4. **Access key rotation:** Access key jangka panjang harus dirotasi secara regular (maksimal 90 hari). Lebih baik lagi: ganti dengan role-based credentials yang short-lived.

5. **Regular access review:** Audit permissions secara berkala. IAM credential reports (AWS) dan Access Advisor dapat menunjukkan permission mana yang tidak pernah digunakan.

```bash
# AWS CLI: Lihat last used date untuk IAM user access keys
aws iam get-access-key-last-used --access-key-id AKIAIOSFODNN7EXAMPLE

# AWS CLI: Generate credential report untuk semua IAM users
aws iam generate-credential-report
aws iam get-credential-report --output text --query Content | base64 -d

# AWS CLI: Access Advisor - lihat service yang TIDAK pernah diakses (kandidat untuk revoke)
aws iam list-policies-granting-service-access \
  --arn arn:aws:iam::123456789012:user/alice \
  --service-namespaces s3 ec2
```

### 4.4 IAM Misconfigurations yang Umum

| Misconfiguration | Risiko | Deteksi | Mitigasi |
|---|---|---|---|
| Root account tanpa MFA | Akun paling powerful tanpa perlindungan ekstra | AWS Security Hub: root-mfa check | Enable MFA segera, disable root access key |
| AdministratorAccess untuk developer | Kelebihan privilege — developer bisa modifikasi/hapus apa saja | AWS IAM Access Analyzer | Ganti dengan role yang spesifik per task |
| Long-lived access key tanpa rotasi | Jika key bocor (GitHub, dll), attacker punya akses permanen | AWS Config: access-keys-rotated rule | Rotasi setiap 90 hari, atau gunakan role assumption |
| S3 bucket policy `Principal: "*"` | Bucket accessible oleh siapapun di internet | AWS Trusted Advisor, S3 Block Public Access | Hapus public access, gunakan bucket policy yang specific |
| IAM wildcard `Action: "*"` | Equivalent dengan admin access | AWS IAM Access Analyzer | Review dan batasi ke action yang diperlukan |
| No MFA untuk privileged user | Credential phishing langsung memberikan akses | AWS Config: mfa-enabled-for-iam-console-access | Enforce MFA via SCP/IAM policy condition |

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph IAM_FLOW["Cloud IAM Authorization Flow"]
        PRINCIPAL["Principal:\nUser / ServiceAccount / Role"]
        REQUEST["API Request:\nAction + Resource"]
        AUTHN["Authentication:\nCredential Verification + MFA Check"]
        POLICY_EVAL["Policy Evaluation Engine"]
        
        subgraph POLICIES["Applicable Policies"]
            SCP["SCP\n(Org-level max boundary)"]
            PERMISSION_BOUNDARY["Permission Boundary\n(per-entity max)"]
            IDENTITY_POLICY["Identity Policy\n(attached to principal)"]
            RESOURCE_POLICY["Resource Policy\n(attached to resource)"]
        end
        
        DECISION{"Decision:\nAllow / Deny?"}
        ACTION_EXEC["Action Executed"]
        DENY_RESP["AccessDenied Error"]
        CLOUDTRAIL["CloudTrail Log\n(semua request dicatat)"]
        
        PRINCIPAL --> REQUEST --> AUTHN
        AUTHN --> POLICY_EVAL
        SCP & PERMISSION_BOUNDARY & IDENTITY_POLICY & RESOURCE_POLICY --> POLICY_EVAL
        POLICY_EVAL --> DECISION
        DECISION -->|Allow| ACTION_EXEC
        DECISION -->|Deny| DENY_RESP
        REQUEST --> CLOUDTRAIL
        ACTION_EXEC & DENY_RESP --> CLOUDTRAIL
    end
```

## 6. Contoh Terapan

**IAM Assessment Checklist untuk EC2-based Application:**

```bash
# 1. Cek apakah instance menggunakan Instance Role (bukan hardcoded credentials)
aws ec2 describe-instances --query \
  'Reservations[*].Instances[*].[InstanceId,IamInstanceProfile]' \
  --output table
# Output: semua instance harus memiliki IamInstanceProfile (bukan null)

# 2. Cek permissions dari Instance Role
aws iam get-instance-profile --instance-profile-name my-app-profile
# Kemudian periksa policies yang attached

# 3. Identifikasi overprivileged permissions menggunakan IAM Access Analyzer
aws accessanalyzer list-analyzers
# Jika belum ada analyzer, buat:
aws accessanalyzer create-analyzer \
  --analyzer-name my-account-analyzer \
  --type ACCOUNT

# 4. Cek last used dates untuk semua access keys
aws iam generate-credential-report
# Review report untuk keys yang tidak digunakan > 90 hari

# 5. Verifikasi MFA status
aws iam list-virtual-mfa-devices
aws iam list-users --query 'Users[*].UserName' --output text | \
  xargs -I{} aws iam list-mfa-devices --user-name {} --query 'MFADevices[*].SerialNumber'
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Melakukan IAM assessment pada lab environment yang disediakan dosen.

**Environment:** AWS sandbox account yang disediakan institusi (BUKAN akun produksi atau akun pribadi).

**Langkah:**
1. Login ke AWS sandbox menggunakan credential yang diberikan dosen.
2. Jalankan credential report dan identifikasi: user tanpa MFA, access key yang tidak dirotasi, user dengan AdministratorAccess.
3. Review IAM policies: cari wildcard Action atau Resource.
4. Cek apakah ada S3 bucket yang public.
5. Dokumentasikan temuan dalam format assessment report.

**Output:** IAM security findings — bagian dari Eval-2.

**Catatan etika:** Semua aktivitas dilakukan di akun sandbox yang diotorisasi. Tidak ada perubahan konfigurasi tanpa izin dosen.

## 8. Latihan Pemahaman

1. **(C4)** Seorang developer meminta akses `AmazonS3FullAccess` untuk membaca data dari satu S3 bucket tertentu. Mengapa ini melanggar least privilege? Tuliskan policy yang benar.

2. **(C4)** Sebuah aplikasi web di EC2 perlu mengakses DynamoDB dan S3. Developer membuatkan IAM user dengan access key dan meng-embed key tersebut dalam environment variable. Identifikasi masalah keamanan dan berikan solusi yang benar.

## 9. Latihan Terapan / Studi Kasus

Anda melakukan IAM assessment pada AWS account sebuah startup dan menemukan: 15 IAM users dengan AdministratorAccess, 3 access key yang tidak dirotasi selama 1 tahun, root account tanpa MFA, 2 Lambda function menggunakan access key yang sama, dan tidak ada SCP (Service Control Policy) di level organisasi. Susun: (a) prioritas remediasi (Critical/High/Medium) untuk setiap temuan; (b) rencana remediasi step-by-step yang dapat dilakukan tanpa mengganggu operasional; (c) IAM governance model yang direkomendasikan untuk jangka panjang.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** `AmazonS3FullAccess` memberikan s3:* (semua action) pada * (semua bucket di account) — jauh melampaui kebutuhan "membaca satu bucket". Policy yang benar:

```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": ["s3:GetObject", "s3:ListBucket"],
    "Resource": [
      "arn:aws:s3:::specific-bucket-name",
      "arn:aws:s3:::specific-bucket-name/*"
    ]
  }]
}
```

**Soal 2:** Masalah: (a) access key long-lived — jika bocor (misal push ke Git), attacker punya akses permanent; (b) env variable mudah terbaca dari logs, crash reports, atau proses anak; (c) satu key untuk 2 layanan berbeda — jika key bocor, keduanya terkena. Solusi: gunakan IAM Instance Role dengan policy minimal:

```json
{
  "Effect": "Allow",
  "Action": ["dynamodb:GetItem", "dynamodb:PutItem", "dynamodb:Query"],
  "Resource": "arn:aws:dynamodb:ap-southeast-1:123456789:table/specific-table"
},
{
  "Effect": "Allow",
  "Action": ["s3:GetObject"],
  "Resource": "arn:aws:s3:::specific-bucket/*"
}
```

Attach role ke EC2 instance. Tidak ada access key yang perlu disimpan dalam kode atau env.

**Studi Kasus:** (a) Prioritas: CRITICAL — root tanpa MFA (immediate fix, 5 menit), CRITICAL — 15 user AdministratorAccess (review dan revoke semua yang tidak perlu); HIGH — access key tidak dirotasi 1 tahun (kemungkinan bocor sudah lama); HIGH — 2 Lambda menggunakan shared access key (harus diganti dengan execution role); MEDIUM — tidak ada SCP (governance gap tapi tidak urgent). (b) Remediasi: Hari 1: enable MFA untuk root; revoke root access key; identify 15 admin user — siapa yang benar-benar perlu admin? (c) IAM governance jangka panjang: gunakan AWS Organizations dengan SCP; gunakan SSO (AWS SSO/Identity Center) dengan federasi ke IdP corporate; gunakan permission boundaries; implement IAM Access Analyzer; automated rotation; quarterly access review.

## 11. Ringkasan Bab

Cloud IAM mengontrol siapa (principal) dapat melakukan apa (action) pada resource apa (resource) dalam kondisi apa (condition). Human identity memerlukan MFA; machine identity harus menggunakan short-lived credentials via role assumption. Least privilege berarti minimum permissions yang diperlukan — tidak ada wildcard. Misconfiguration IAM yang umum mencakup root tanpa MFA, AdministratorAccess yang terlalu luas, dan hardcoded credentials.

## 12. Refleksi Profesional

1. Banyak organisasi memberikan akses luas kepada developer "karena lebih mudah dan cepat untuk development." Trade-off ini memiliki implikasi jika credential developer dikompromis. Bagaimana Anda merancang developer access model yang tetap produktif (developer dapat bekerja efisien) namun tetap aman (blast radius minimal jika dikompromis)? Pertimbangkan: sandbox accounts, role assumption, JIT access, dan audit logging.

---

# BAB 5 — CLOUD NETWORK SECURITY: VPC, SEGMENTASI, DAN ISOLASI

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Merancang arsitektur VPC yang aman dengan segmentasi yang tepat
- Mengkonfigurasi Security Groups dan Network ACL untuk least-privilege network access
- Menganalisis risiko network dari konfigurasi cloud yang tidak tepat
- Memahami konsep private connectivity dan perannya dalam cloud security

*Berkaitan dengan Sub-CPMK-2, Eval-2 (20%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud Network Security] --> B[VPC Architecture]
    B --> B1["Subnets: public vs private\nAZ distribution"]
    B --> B2["Route tables:\nkontrol traffic routing"]
    B --> B3["Internet Gateway:\nhanya untuk subnet yang perlu"]
    B --> B4["NAT Gateway:\noutbound-only internet untuk private subnet"]
    A --> C[Access Control]
    C --> C1["Security Groups:\nstateful, instance-level firewall\ndefault: deny all inbound"]
    C --> C2["Network ACL:\nstateless, subnet-level\neksplisit allow+deny"]
    C --> C3["WAF:\nLayer 7 HTTP protection\nOWASP rules"]
    A --> D[Private Connectivity]
    D --> D1["VPC Peering:\npoint-to-point, no transitive routing"]
    D --> D2["PrivateLink / VPC Endpoints:\nakses cloud services tanpa internet"]
    D --> D3["VPN / Direct Connect:\nhubungi on-premises secara aman"]
    A --> E[Network Monitoring]
    E --> E1["VPC Flow Logs:\nrecord IP traffic metadata"]
    E --> E2["DNS query logging:\nidentifikasi C2 atau data exfil"]
    E --> E3["Traffic Mirroring:\ndeep packet inspection (selective)"]
```

## 3. Pengantar Kontekstual

Network security di cloud berbeda dari on-premises dalam cara yang fundamental. Tidak ada "network perimeter" fisik — setiap resource dapat dikonfigurasi untuk accessible dari internet dalam hitungan menit. Ini berarti security group dan network policy menjadi "perimeter" baru. Konsep seperti VPC (Virtual Private Cloud), subnet segmentation, dan private endpoints memungkinkan arsitektur yang sama amannya dengan on-premises — bahkan lebih fleksibel — jika dikonfigurasi dengan benar.

## 4. Landasan Teori

### 4.1 VPC Architecture dan Subnet Segmentation

**VPC (Virtual Private Cloud)** adalah isolated network environment dalam cloud. Setiap VPC memiliki CIDR block sendiri, subnet, routing table, dan security controls.

**Prinsip desain VPC yang aman:**

```
VPC ARCHITECTURE BEST PRACTICE (AWS Example):

VPC: 10.0.0.0/16

┌────────────────────────────────────────────────────┐
│  Public Subnet 10.0.1.0/24 (AZ-a)                 │
│  Public Subnet 10.0.2.0/24 (AZ-b)                 │
│  [Load Balancer, NAT Gateway, Bastion Host]        │
│  Route: 0.0.0.0/0 → Internet Gateway               │
├────────────────────────────────────────────────────┤
│  Private Subnet 10.0.10.0/24 (AZ-a)               │
│  Private Subnet 10.0.11.0/24 (AZ-b)               │
│  [Application Servers, ECS/EKS nodes]              │
│  Route: 0.0.0.0/0 → NAT Gateway (outbound only)   │
├────────────────────────────────────────────────────┤
│  Data Subnet 10.0.20.0/24 (AZ-a)                  │
│  Data Subnet 10.0.21.0/24 (AZ-b)                  │
│  [RDS, ElastiCache, Elasticsearch]                 │
│  Route: NO internet routing (isolated)             │
└────────────────────────────────────────────────────┘

Prinsip:
- Database tidak boleh di public subnet — pernah dan tidak akan pernah
- Application servers di private subnet — akses via Load Balancer saja
- Internet Gateway hanya dibutuhkan di public subnet
- NAT Gateway: memberikan internet access outbound ke private subnet,
  tapi tidak mengizinkan inbound connection dari internet
```

### 4.2 Security Groups — Cloud Firewall

**Security Group** adalah stateful, instance-level firewall di cloud. "Stateful" berarti jika koneksi inbound diizinkan, reply traffic-nya otomatis diizinkan (tidak perlu explicit outbound rule untuk established connections).

**Best Practices Security Group:**

```terraform
# Terraform — Security Group untuk Application Server (contoh best practice)
resource "aws_security_group" "app_server" {
  name        = "app-server-sg"
  description = "Security group for application servers"
  vpc_id      = aws_vpc.main.id

  # Inbound: hanya dari Load Balancer Security Group
  ingress {
    description     = "HTTP from Load Balancer only"
    from_port       = 8080
    to_port         = 8080
    protocol        = "tcp"
    security_groups = [aws_security_group.load_balancer.id]
    # TIDAK menggunakan cidr_blocks = ["0.0.0.0/0"]!
    # Referensi ke SG lain lebih aman dan maintainable
  }

  # Outbound: hanya ke database security group pada port database
  egress {
    description     = "Database access"
    from_port       = 5432
    to_port         = 5432
    protocol        = "tcp"
    security_groups = [aws_security_group.database.id]
  }

  egress {
    description = "HTTPS for package updates via NAT"
    from_port   = 443
    to_port     = 443
    protocol    = "tcp"
    cidr_blocks = ["0.0.0.0/0"]  # NAT akan filter ini ke internet saja
  }
  
  tags = {
    Name        = "app-server-sg"
    Environment = "production"
    ManagedBy   = "Terraform"
  }
}

# JANGAN BUAT Security Group seperti ini:
# ingress { from_port = 0, to_port = 0, protocol = "-1", cidr_blocks = ["0.0.0.0/0"] }
# Ini membuka SEMUA port ke SEMUA IP — sangat berbahaya!
```

### 4.3 Network ACL vs Security Group

| Aspek | Security Group | Network ACL |
|---|---|---|
| Level | Instance (ENI) | Subnet |
| Stateful/less | Stateful (reply otomatis diizinkan) | Stateless (must explicit allow both directions) |
| Rules | Allow only | Allow dan Deny |
| Evaluation | Semua rules dievaluasi | Rules dievaluasi berurutan (number order) |
| Default | Deny all inbound, Allow all outbound | Allow all inbound dan outbound |
| Use case | Primary instance-level control | Additional subnet-level defense-in-depth |

**Kapan menggunakan Network ACL:**
- Sebagai defense-in-depth tambahan di level subnet
- Untuk eksplisit DENY (Security Group tidak bisa deny — hanya bisa tidak-allow)
- Misalnya: blacklist IP address yang sudah diketahui berbahaya

### 4.4 VPC Endpoints — Akses Service Tanpa Internet

**VPC Endpoint** memungkinkan EC2 instance atau Lambda mengakses AWS services (S3, DynamoDB, SQS, dll.) **tanpa traffic melewati internet** — traffic tetap dalam AWS network backbone.

```
Tanpa VPC Endpoint:
EC2 (private subnet) → NAT Gateway → Internet → S3
[Traffic keluar ke internet, lebih mahal, lebih exposed]

Dengan Gateway VPC Endpoint (S3/DynamoDB):
EC2 (private subnet) → VPC Endpoint → S3
[Traffic tetap dalam AWS network, tidak keluar ke internet]
```

Ini penting untuk keamanan karena:
- Data sensitif tidak melewati internet publik
- Dapat membuat S3 bucket policy yang hanya mengizinkan access dari VPC (bukan dari internet sama sekali)
- Mengurangi attack surface

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    INTERNET["Internet\n(Untrusted)"]
    IGW["Internet Gateway"]
    WAF["WAF\n(Layer 7 Protection)"]
    ALB["Application Load Balancer\n(Public Subnet)"]
    
    subgraph VPC["VPC 10.0.0.0/16"]
        subgraph PUBLIC["Public Subnet (10.0.1-2.0/24)"]
            NAT["NAT Gateway\n(outbound only)"]
        end
        
        subgraph PRIVATE["Private Subnet (10.0.10-11.0/24)"]
            APP1["App Server 1\nSG: allow from ALB:8080"]
            APP2["App Server 2\nSG: allow from ALB:8080"]
        end
        
        subgraph DATA["Data Subnet (10.0.20-21.0/24)"]
            DB["RDS Database\nSG: allow from App SG:5432"]
        end
        
        VPC_EP["VPC Endpoint\n(S3, SQS, SecretsManager)"]
    end
    
    S3["S3 Bucket\n(Bucket Policy: allow only from VPC)"]
    
    INTERNET --> IGW --> WAF --> ALB
    ALB --> APP1 & APP2
    APP1 & APP2 --> DB
    APP1 & APP2 --> NAT
    APP1 & APP2 --> VPC_EP --> S3
    NAT --> INTERNET
```

## 6. Contoh Terapan

**Audit Security Group menggunakan AWS CLI:**

```bash
# Temukan Security Groups dengan port 0.0.0.0/0 yang exposed (risiko tinggi)
aws ec2 describe-security-groups \
  --query 'SecurityGroups[?IpPermissions[?IpRanges[?CidrIp==`0.0.0.0/0`]]].[GroupId,GroupName,IpPermissions]' \
  --output table

# Temukan Security Groups yang mengizinkan SSH (port 22) dari mana saja
aws ec2 describe-security-groups \
  --filters "Name=ip-permission.from-port,Values=22" \
             "Name=ip-permission.cidr,Values=0.0.0.0/0" \
  --query 'SecurityGroups[*].[GroupId,GroupName]' \
  --output table

# Cek VPC Flow Logs (apakah sudah diaktifkan untuk semua VPC?)
aws ec2 describe-vpcs --query 'Vpcs[*].VpcId' --output text | \
  xargs -I{} aws ec2 describe-flow-logs \
    --filter "Name=resource-id,Values={}" \
    --query 'FlowLogs[*].[FlowLogId,ResourceId,TrafficType]'
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menganalisis konfigurasi network security cloud menggunakan dataset yang disanitasi.

**Aktivitas:**
1. Dosen menyediakan output export dari `describe-security-groups` dan `describe-vpcs` (sudah di-anonimisasi).
2. Analisis: identifikasi Security Groups yang bermasalah (port 22/3389 ke 0.0.0.0/0, overly permissive egress).
3. Cek apakah VPC menggunakan subnet segmentation (public/private/data).
4. Identifikasi apakah VPC Flow Logs aktif.
5. Rekomendasikan perbaikan dalam format: temuan, severity, rekomendasi spesifik.

**Output:** Network security findings — bagian dari Eval-2.

## 8. Latihan Pemahaman

1. **(C4)** Mengapa database RDS TIDAK boleh ditempatkan di public subnet, bahkan jika Security Group dikonfigurasi untuk hanya menerima traffic dari Application Server tertentu?

2. **(C3)** Jelaskan perbedaan fungsi Security Group dan Network ACL. Dalam skenario apa keduanya harus digunakan bersama-sama?

## 9. Latihan Terapan / Studi Kasus

Tim developer telah mendeply arsitektur berikut di AWS: semua EC2 di public subnet, RDS di public subnet, Security Group database mengizinkan port 3306 dari 0.0.0.0/0 "sementara untuk testing", tidak ada VPC Flow Logs, dan tidak ada WAF. Developer berargumen "kami akan fix sebelum production." Sebagai security architect: (a) identifikasi minimal 5 risiko konkret dari arsitektur ini; (b) jelaskan mengapa "fix sebelum production" adalah argumentasi yang berbahaya dalam konteks ini; (c) buat rencana remediasi yang bisa diterapkan tanpa downtime.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Defense-in-depth dan reduce attack surface: (a) Meskipun Security Group membatasi akses, menempatkan database di public subnet berarti database memiliki public IP (atau dapat diberikan public IP) dan dapat discoverability dari internet. (b) Jika terjadi Security Group misconfiguration (bahkan sementara), database langsung exposed ke internet; (c) Attacker yang melakukan network scanning akan menemukan bahwa IP tersebut mendengarkan pada port database; (d) Compliance (PCI-DSS, SOC2) umumnya mensyaratkan database tidak di public subnet; (e) VPC Flow Logs untuk data subnet menunjukkan traffic lebih bersih dan lebih mudah dianalisis ketika tidak ada traffic internet.

**Soal 2:** Security Group: stateful, instance-level, hanya Allow (tidak bisa Deny eksplisit), primary control. Network ACL: stateless (explicit allow untuk both directions), subnet-level, dapat Allow dan Deny. Digunakan bersama dalam skenario: (a) defense-in-depth — SG sebagai primary control, NACL sebagai secondary; (b) blacklisting IP — SG tidak bisa deny spesific IP, tapi NACL bisa; (c) regulatory compliance yang mensyaratkan multiple layers of network control.

**Studi Kasus:** (a) Risiko: 1) RDS di public subnet dengan port 3306 ke 0.0.0.0/0 — database dapat diakses oleh siapapun di internet; 2) Semua EC2 di public subnet — semua instance memiliki public IP, attack surface sangat luas; 3) Tidak ada VPC Flow Logs — tidak ada visibility network traffic, tidak ada audit trail; 4) Tidak ada WAF — layer 7 attacks (SQLi, XSS) tidak terfilter; 5) Arsitektur "testing" sering menjadi production secara tidak sengaja sebelum "fix" dilakukan. (b) "Fix sebelum production" berbahaya karena: data breach dapat terjadi saat "testing" (test data mungkin real); "testing" environment sering tidak di-off-kan dan secara tidak sengaja menjadi production; jadwal "fix" sering diundur karena time pressure. (c) Remediasi tanpa downtime: 1) Ubah Security Group RDS: hapus 0.0.0.0/0, izinkan hanya SG App Server; 2) Aktifkan VPC Flow Logs segera (tanpa downtime); 3) Buat private subnet dan migrasi RDS (dapat dilakukan dengan snapshot + restore); 4) Migrasi EC2 ke private subnet bertahap; 5) Deploy WAF di depan Load Balancer.

## 11. Ringkasan Bab

VPC menyediakan isolated network environment dengan kontrol penuh atas routing, subnetting, dan access control. Segmentasi subnet (public/private/data) mengimplementasikan defense-in-depth di level network. Security Groups adalah primary instance-level firewall (stateful, allow-only); Network ACL adalah secondary subnet-level control (stateless, allow + deny). VPC Endpoints memungkinkan akses private ke cloud services tanpa melewati internet.

## 12. Refleksi Profesional

1. Security Group yang terlalu permisif sering dibuat oleh developer karena "lebih mudah" dan sering tidak pernah diperketat kembali. Bagaimana Anda, sebagai security architect, merancang proses (bukan hanya kebijakan) yang secara sistemik mencegah Security Group permisif masuk ke production? Pertimbangkan: Infrastructure as Code review, CI/CD security gates, dan automated compliance checking.

---

# BAB 6 — WORKLOAD ISOLATION, SECRETS MANAGEMENT, DAN SECURE BASELINE

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menerapkan workload isolation dalam environment cloud dan container
- Merancang secrets management yang aman menggunakan best practices
- Mengimplementasikan secure baseline configuration berdasarkan CIS Benchmarks
- Memvalidasi konfigurasi baseline dengan tools otomatis

*Berkaitan dengan Sub-CPMK-2, Eval-2 (20%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Workload Security] --> B[Workload Isolation]
    B --> B1["Kubernetes Namespace:\nlogical isolation"]
    B --> B2["Pod Security Standards:\nPrivileged/Baseline/Restricted"]
    B --> B3["Resource Quotas:\nprevent noisy neighbor + DoS"]
    B --> B4["Node isolation:\ntaint + toleration\nuntuk dedicated workloads"]
    A --> C[Secrets Management]
    C --> C1["Kubernetes Secrets:\nbase64, bukan enkripsi!\nperlu enkripsi at rest"]
    C --> C2["External Vault:\nHashiCorp Vault, AWS Secrets Manager\nGCP Secret Manager"]
    C --> C3["Secret rotation:\notomatis, tidak manual"]
    C --> C4["Tidak boleh di:\nGit, env var, log, image"]
    A --> D[Secure Baseline]
    D --> D1["CIS Benchmarks:\nDocker, Kubernetes, Cloud Provider"]
    D --> D2["Automated assessment:\nkube-bench, Trivy config scan\nCheckov"]
    D --> D3["Drift detection:\nalert jika konfigurasi berubah\ndari baseline"]
```

## 3. Pengantar Kontekstual

Setelah mengamankan identity dan network, lapisan berikutnya adalah workload itu sendiri. Sebuah aplikasi yang berjalan dengan hak berlebihan, menggunakan secrets yang tidak terkelola, atau tidak memenuhi baseline hardening adalah aplikasi yang rentan meskipun IAM dan network sudah dikonfigurasi dengan benar. Bab ini menutup troika kontrol keamanan fundamental: identity, network, dan workload.

## 4. Landasan Teori

### 4.1 Workload Isolation dalam Kubernetes

**Kubernetes Namespaces:**
Namespace memberikan isolasi logical untuk resource dalam cluster. Best practice: gunakan namespace terpisah untuk setiap environment (production, staging, development) dan setiap tim/aplikasi.

```yaml
# Buat namespace dengan labels yang jelas
apiVersion: v1
kind: Namespace
metadata:
  name: production
  labels:
    environment: production
    team: backend
    security-tier: critical
---
# ResourceQuota — batasi resource usage per namespace
apiVersion: v1
kind: ResourceQuota
metadata:
  name: production-quota
  namespace: production
spec:
  hard:
    requests.cpu: "10"          # Total CPU yang bisa di-request oleh semua Pod
    requests.memory: "20Gi"     # Total Memory yang bisa di-request
    limits.cpu: "20"            # Total CPU limit
    limits.memory: "40Gi"       # Total Memory limit
    pods: "50"                  # Maksimal 50 Pod dalam namespace ini
    services: "20"              # Maksimal 20 Services
    secrets: "100"              # Maksimal 100 Secrets
```

**Pod Security Standards (PSS) — Pengganti PodSecurityPolicy:**
PSS mendefinisikan tiga profil keamanan:

1. **Privileged:** Tidak ada batasan keamanan (untuk system components seperti Calico, monitoring agents). Jangan gunakan untuk workload aplikasi.

2. **Baseline:** Mencegah privilege escalation yang paling berbahaya:
   - Tidak mengizinkan `hostPID`, `hostIPC`, `hostNetwork`
   - Tidak mengizinkan `privileged: true`
   - Membatasi `hostPath` volumes ke path yang aman
   - Membatasi `capabilities`

3. **Restricted (Target untuk semua aplikasi):** Mengimplementasikan current best practices:
   - Semua yang di Baseline, PLUS:
   - Harus `runAsNonRoot: true`
   - Harus `seccompProfile` (RuntimeDefault atau spesifik)
   - Drop semua Linux capabilities, boleh add specific yang diperlukan
   - Volume types dibatasi (no hostPath)

```yaml
# Mengaktifkan Pod Security Standards untuk namespace
apiVersion: v1
kind: Namespace
metadata:
  name: production
  labels:
    pod-security.kubernetes.io/enforce: restricted    # Block Pod yang tidak conform
    pod-security.kubernetes.io/warn: restricted       # Warning untuk admission
    pod-security.kubernetes.io/audit: restricted      # Audit non-conforming pods
```

**Pod spec yang memenuhi Restricted PSS:**
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: secure-app
spec:
  securityContext:
    runAsNonRoot: true            # Tidak boleh run sebagai root
    runAsUser: 1000              # UID non-root
    fsGroup: 2000                 # Group untuk mounted volumes
    seccompProfile:
      type: RuntimeDefault        # Syscall filtering default
  containers:
  - name: app
    image: myapp:v1.2.3@sha256:abc123...  # Pin ke digest! Bukan tag saja
    securityContext:
      allowPrivilegeEscalation: false  # Tidak boleh escalate privilege
      readOnlyRootFilesystem: true     # Filesystem read-only
      capabilities:
        drop:
        - ALL                          # Drop semua Linux capabilities
        add:
        - NET_BIND_SERVICE             # Hanya add yang diperlukan (jika perlu)
    resources:
      requests:
        cpu: "100m"
        memory: "128Mi"
      limits:
        cpu: "200m"
        memory: "256Mi"
```

### 4.2 Secrets Management

**Masalah dengan secrets yang tidak dikelola:**
- Hardcoded dalam kode atau Dockerfile → terekspos di Git history
- Dalam environment variable → muncul dalam `docker inspect`, logs, crash dumps
- Kubernetes Secrets default hanya base64-encoded (BUKAN encrypted) → siapapun dengan akses etcd atau `kubectl get secret` dapat membaca
- Tidak pernah dirotasi → jika bocor, exposure window tidak terbatas

**Arsitektur Secrets Management yang benar:**

```
Tingkatan Secrets Management:

LEVEL 1 (Minimum): Kubernetes Secrets dengan enkripsi at rest
├── Aktifkan enkripsi etcd (EncryptionConfiguration)
├── RBAC ketat: tidak semua orang boleh get/list secrets
└── Tetap butuh rotasi manual

LEVEL 2 (Recommended): External Secret Manager
├── AWS Secrets Manager / GCP Secret Manager / Azure Key Vault
├── Automatic rotation (misalnya database password dirotasi otomatis setiap 30 hari)
├── Audit trail setiap kali secret diakses
└── External Secrets Operator: sync secret dari Vault ke Kubernetes Secret

LEVEL 3 (Advanced): HashiCorp Vault dengan dynamic secrets
├── Secret di-generate on-demand (tidak disimpan statik)
├── Database password dibuat saat container start, dihapus saat selesai
└── Zero standing secrets
```

**External Secrets Operator — menjembatani Vault/AWS SM dengan Kubernetes:**
```yaml
# ExternalSecret: definisi bagaimana secret dari AWS Secrets Manager
# disync ke Kubernetes Secret
apiVersion: external-secrets.io/v1beta1
kind: ExternalSecret
metadata:
  name: database-credentials
  namespace: production
spec:
  refreshInterval: 1h              # Cek update setiap 1 jam
  secretStoreRef:
    name: aws-secrets-manager
    kind: ClusterSecretStore
  target:
    name: db-password              # Nama Kubernetes Secret yang akan dibuat
  data:
  - secretKey: password            # Key dalam Kubernetes Secret
    remoteRef:
      key: production/db-password  # Key dalam AWS Secrets Manager
```

### 4.3 Secure Baseline dengan CIS Benchmarks

**CIS (Center for Internet Security) Benchmarks** menyediakan panduan konfigurasi hardening yang diakui secara industri untuk berbagai platform.

**CIS Benchmarks yang relevan:**
- CIS Docker Benchmark (Level 1 & 2)
- CIS Kubernetes Benchmark (Level 1 & 2)
- CIS Amazon Web Services Foundations Benchmark
- CIS Red Hat Linux Benchmark (untuk node OS)

**kube-bench — automated Kubernetes benchmark:**
```bash
# Jalankan kube-bench di cluster Kubernetes (dalam lab yang diotorisasi)
# kube-bench secara otomatis mendeteksi versi Kubernetes dan menjalankan
# CIS Kubernetes Benchmark yang sesuai

# Jalankan sebagai Job di cluster:
kubectl apply -f https://raw.githubusercontent.com/aquasecurity/kube-bench/main/job.yaml
kubectl logs job/kube-bench | head -100

# Output contoh:
# [INFO] 1 Master Node Security Configuration
# [INFO] 1.2 API Server
# [PASS] 1.2.1 Ensure that the --anonymous-auth argument is set to false
# [FAIL] 1.2.2 Ensure that the --basic-auth-file argument is not set
#        Remediation: Edit the API server pod specification file...
# [WARN] 1.2.3 Ensure that the --token-auth-file parameter is not set
# ...
# == Summary ==
# 42 checks PASS
# 11 checks FAIL
# 9 checks WARN
# 1 checks INFO
```

**Trivy untuk container image dan config scan:**
```bash
# Scan Kubernetes manifest files untuk security misconfigurations
trivy config kubernetes_manifests/

# Output:
# deployment.yaml (kubernetes)
# Tests: 120 (UNKNOWN: 0, LOW: 5, MEDIUM: 8, HIGH: 4, CRITICAL: 2)
# 
# HIGH: Container should not run as root
#   Namespace: production
#   Resource: Deployment/my-app
#   Remediation: Set runAsNonRoot: true
#
# CRITICAL: Container has read/write root filesystem
#   Remediation: Set readOnlyRootFilesystem: true
```

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph SECRET_FLOW["Secure Secret Delivery Flow"]
        DEV["Developer\n(tidak lihat secret produksi)"]
        CI_CD["CI/CD Pipeline\n(GitOps)"]
        VAULT["HashiCorp Vault /\nAWS Secrets Manager\n(Source of Truth)"]
        ESO["External Secrets Operator\n(Kubernetes)"]
        K8S_SECRET["Kubernetes Secret\n(encrypted at rest)"]
        POD["Pod / Container\n(mounted sebagai file)"]
        
        DEV -->|"Define ExternalSecret manifest\n(tidak mengandung nilai secret)"| CI_CD
        CI_CD --> ESO
        ESO -->|"Fetch secret via\nVault/SM API"| VAULT
        VAULT -->|"Return encrypted secret"| ESO
        ESO -->|"Create/Update"| K8S_SECRET
        K8S_SECRET -->|"Mount sebagai volume\n(file, bukan env var)"| POD
        
        AUDIT["Audit Log:\nsiapa mengakses secret, kapan"]
        VAULT --> AUDIT
        K8S_SECRET --> AUDIT
    end
```

## 6. Contoh Terapan

**Remediation: Mengamankan database credential yang sebelumnya hardcoded:**

```python
# SEBELUM (berbahaya — credential hardcoded):
import psycopg2
conn = psycopg2.connect(
    host="db.example.com",
    database="production",
    user="admin",
    password="SuperSecret123!"  # BERBAHAYA!
)

# SESUDAH (menggunakan mounted secret file):
import psycopg2
import os

# Secret di-mount sebagai file dalam /etc/secrets/ (bukan env var)
with open('/etc/secrets/db-password', 'r') as f:
    db_password = f.read().strip()

# db_password sekarang dibaca dari file yang di-mount dari Kubernetes Secret
# File ini tidak terekspos dalam env, logs, atau container inspect
conn = psycopg2.connect(
    host=os.getenv('DB_HOST'),  # Non-sensitive config: env var OK
    database=os.getenv('DB_NAME'),
    user=os.getenv('DB_USER'),
    password=db_password
)
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Mengevaluasi workload security posture menggunakan tools assessment.

**Aktivitas (dalam lab Kubernetes yang diotorisasi):**
1. Deploy Kubernetes cluster lokal (Minikube/Kind dalam lab).
2. Jalankan kube-bench dan dokumentasikan semua temuan FAIL.
3. Jalankan Trivy config scan pada deployment manifest.
4. Identifikasi top 5 temuan berdasarkan severity.
5. Implementasikan fix untuk satu temuan HIGH dan verifikasi dengan re-scan.

**Output:** Posture review notes — bagian dari Eval-2.

## 8. Latihan Pemahaman

1. **(C4)** Kubernetes Secret menyimpan data dalam base64. Seorang anggota tim menyatakan "sudah aman karena di-encode." Apa yang salah dengan pernyataan ini? Apa yang harus dilakukan untuk benar-benar mengamankan Secret di etcd?

2. **(C5)** Bandingkan tiga pendekatan secrets management: (a) hardcoded dalam kode; (b) Kubernetes Secret default; (c) External Secret Manager dengan auto-rotation. Evaluasi setiap pendekatan dari perspektif: keamanan, operasional complexity, dan auditability.

## 9. Latihan Terapan / Studi Kasus

Tim backend ingin mendeploy microservice baru yang memerlukan: koneksi ke database PostgreSQL, API key untuk payment gateway, dan TLS certificate untuk komunikasi internal. Rancang secret management strategy yang: (a) menentukan jenis secret mana yang disimpan di mana; (b) menjelaskan bagaimana secret di-deliver ke container; (c) menjelaskan rotation policy untuk setiap tipe secret; (d) menjelaskan siapa yang boleh membaca secret ini dalam pipeline CI/CD dan production.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Base64 adalah encoding, bukan enkripsi — siapapun dapat menjalankan `base64 -d` untuk mendekode nilai tersebut. Ini bukan proteksi apapun. Yang harus dilakukan untuk mengamankan Secret di etcd: (a) aktifkan **Encryption at Rest** dalam etcd melalui EncryptionConfiguration di kube-apiserver — ini menggunakan AES-256 untuk mengenkripsi secret sebelum disimpan ke disk etcd; (b) batasi akses ke etcd hanya dari kube-apiserver; (c) gunakan RBAC untuk membatasi siapa yang bisa `get/list/watch` secrets; (d) pertimbangkan External Secret Manager untuk secret yang paling sensitif.

**Soal 2:** (a) Hardcoded dalam kode: SANGAT TIDAK AMAN — mudah bocor via Git, log, crash report; tidak bisa dirotasi tanpa redeploy; tidak ada audit trail; TIDAK BOLEH digunakan. (b) Kubernetes Secret default: security sedang — lebih baik dari hardcoded, tapi base64 bukan enkripsi, perlu manual rotation, memerlukan enkripsi at rest eksplisit, audit trail terbatas pada API audit log. Operasional: sederhana, sudah built-in. (c) External Secret Manager: BEST PRACTICE — auto-rotation, audit trail lengkap per-access, enkripsi kuat, integrasi dengan IAM; lebih kompleks operasionalnya tapi trade-off yang worth it untuk production.

**Studi Kasus Strategy:** (a) Penyimpanan: Database password → AWS Secrets Manager (auto-rotation by RDS integration); API key payment gateway → AWS Secrets Manager (rotation via Lambda function); TLS certificate → AWS ACM (auto-renewal) atau cert-manager dalam Kubernetes. (b) Delivery: External Secrets Operator sync dari Secrets Manager ke Kubernetes Secret; mount sebagai file ke container (bukan env var); untuk TLS, mount sebagai Kubernetes TLS secret. (c) Rotation: database password setiap 30 hari (otomatis via Secrets Manager + Lambda); API key payment gateway setiap 90 hari (dengan koordinasi payment provider); TLS cert otomatis via cert-manager 30 hari sebelum expiry. (d) Akses: CI/CD pipeline hanya boleh deploy ExternalSecret manifest (tidak mengakses nilai secret); hanya ESO service account yang bisa akses Secrets Manager; developer TIDAK BOLEH get/list Kubernetes secrets di production namespace; production admin akses via JIT dengan approval.

## 11. Ringkasan Bab

Workload isolation menggunakan Kubernetes namespaces dengan Pod Security Standards (Restricted profile sebagai target untuk semua aplikasi). Resource Quotas mencegah noisy neighbor dan DoS. Secrets management harus menghindari hardcoded secrets dan menggunakan External Secret Manager dengan auto-rotation. CIS Benchmarks (divalidasi dengan kube-bench dan Trivy config scan) memberikan baseline konfigurasi yang terstandar dan dapat diaudit.

## 12. Refleksi Profesional

1. Secret rotation otomatis idealnya dilakukan tanpa downtime — aplikasi harus dapat menggunakan credential baru sementara credential lama masih valid untuk jangka waktu singkat ("rotation overlap"). Namun, implementasi ini memerlukan investasi engineering yang signifikan. Bagaimana Anda meyakinkan tim engineering untuk mengalokasikan waktu untuk fitur "tidak terlihat" (tidak menambah fitur bisnis) namun kritis dari perspektif keamanan?


---

# BAB 7 — CONTAINER IMAGE SECURITY DAN SOFTWARE SUPPLY CHAIN

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menganalisis keamanan container image dari base image hingga runtime
- Menggunakan tools scanning untuk mendeteksi kerentanan dalam image
- Memahami konsep software supply chain dan risikonya
- Menerapkan image signing dan policy enforcement

*Berkaitan dengan Sub-CPMK-3, Eval-3 (25%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Container Image Security] --> B[Image Composition]
    B --> B1["Base image:\nOS layer — pilih minimal\nAlpine, Distroless"]
    B --> B2["Dependencies:\nnpm, pip, apt packages\n→ scan untuk CVE"]
    B --> B3["Application code:\nscanning SAST + secrets"]
    B --> B4["Image layers:\ntiap layer diidentifikasi\ndengan SHA256 digest"]
    A --> C[Vulnerability Scanning]
    C --> C1["Trivy: comprehensive scanner\nOS packages + library CVE"]
    C --> C2["Grype: Anchore image scanner"]
    C --> C3["Scan di CI/CD:\nblock build jika CRITICAL CVE"]
    C --> C4["Scan di registry:\ncontinuous monitoring"]
    A --> D[Supply Chain Security]
    D --> D1["Dockerfile best practices:\nnon-root, minimal, pinned versions"]
    D --> D2["SBOM: Software Bill of Materials\nSPDX atau CycloneDX format"]
    D --> D3["Image signing:\nCosign + Sigstore"]
    D --> D4["Admission control:\nverify signature sebelum run"]
    A --> E[Registry Security]
    E --> E1["Private registry:\nhanya image yang approved"]
    E --> E2["Image tag pinning:\ngunakan digest, bukan :latest"]
    E --> E3["Registry access control:\nsiapa bisa push/pull image"]
```

## 3. Pengantar Kontekstual

Container image adalah "paket" yang berisi seluruh dependencies aplikasi — dari OS base layer hingga kode aplikasi itu sendiri. Kerentanan dalam image dapat berasal dari mana saja dalam stack ini: kernel library yang outdated dalam base image, library npm yang mengandung CVE, atau bahkan image dari public registry yang sudah tersusupi (supply chain attack). Insiden seperti SolarWinds (supply chain attack pada software build pipeline) menunjukkan bahwa kepercayaan pada software yang kita gunakan harus diverifikasi, bukan diasumsikan.

## 4. Landasan Teori

### 4.1 Dockerfile Best Practices untuk Keamanan

**Prinsip 1: Gunakan base image yang minimal**
```dockerfile
# KURANG BAIK: Base image yang besar, banyak packages tidak diperlukan
FROM ubuntu:22.04
RUN apt-get install -y python3 python3-pip curl wget vim git

# LEBIH BAIK: Base image minimal
FROM python:3.11-alpine
# Alpine = ~5MB, minimal attack surface

# TERBAIK untuk production: Distroless (tidak ada shell, tidak ada package manager)
FROM gcr.io/distroless/python3
# Hanya runtime yang diperlukan, tidak ada shell
# Attacker yang masuk container tidak bisa menjalankan bash, apt, curl, dll.
```

**Prinsip 2: Jangan jalankan sebagai root**
```dockerfile
# Buat user non-root dan group
RUN addgroup --system --gid 1001 appgroup && \
    adduser --system --uid 1001 --ingroup appgroup appuser

# Salin dan set ownership
COPY --chown=appuser:appgroup . /app

# Switch ke user non-root
USER appuser

# Sekarang semua proses dalam container berjalan sebagai appuser (UID 1001)
```

**Prinsip 3: Multi-stage build untuk minimal final image**
```dockerfile
# Stage 1: Build environment (boleh lebih besar karena tidak di-deploy)
FROM golang:1.21 AS builder
WORKDIR /app
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN CGO_ENABLED=0 GOOS=linux go build -o myapp .

# Stage 2: Production image — minimal, hanya binary yang dikompilasi
FROM gcr.io/distroless/static-debian12
COPY --from=builder /app/myapp /
USER nonroot:nonroot
EXPOSE 8080
ENTRYPOINT ["/myapp"]
# Final image: hanya binary, tidak ada Go compiler, tidak ada source code
```

**Prinsip 4: Pin versi dependencies**
```dockerfile
# JANGAN: Tag floating yang berubah tanpa sepengetahuan kita
FROM python:3.11
# Atau bahkan:
FROM python:latest  # SANGAT BERBAHAYA — bisa berubah kapan saja!

# HARUS: Pin ke specific digest untuk reprodusibilitas
FROM python:3.11.9-alpine3.19@sha256:a3b4c5d6e7f8...
# Dengan sha256 digest, image yang sama persis dijamin digunakan setiap build
```

### 4.2 Vulnerability Scanning dengan Trivy

```bash
# Scan image untuk CVE (dalam lab atau CI/CD pipeline)
trivy image python:3.11-alpine

# Output contoh:
# python:3.11-alpine (alpine 3.18.4)
# =====================================================
# Total: 3 (UNKNOWN: 0, LOW: 1, MEDIUM: 1, HIGH: 1, CRITICAL: 0)
# 
# ┌──────────────────────────┬────────────────┬──────────┬───────────────────┐
# │ Library                  │ Vulnerability  │ Severity │ Installed / Fixed │
# ├──────────────────────────┼────────────────┼──────────┼───────────────────┤
# │ libssl3                  │ CVE-2023-XXXX  │ HIGH     │ 3.1.3-r0 / 3.1.4  │
# └──────────────────────────┴────────────────┴──────────┴───────────────────┘

# Scan dengan exit code — berguna untuk CI/CD gate
trivy image --exit-code 1 --severity CRITICAL,HIGH myapp:v1.2.3
# Return code 1 jika ada CRITICAL atau HIGH CVE → CI/CD pipeline fails → image tidak di-push

# Scan Dockerfile untuk misconfigurations
trivy config Dockerfile

# Scan filesystem directory
trivy fs /path/to/source/code

# Generate SBOM dalam format SPDX
trivy image --format spdx-json --output sbom.json myapp:v1.2.3
```

### 4.3 Software Bill of Materials (SBOM)

SBOM adalah daftar inventaris dari semua komponen yang ada dalam software (OS packages, libraries, dependencies). Analoginya: daftar bahan makanan pada kemasan produk.

**Mengapa SBOM penting:**
- Ketika CVE baru ditemukan (misalnya Log4Shell), dengan SBOM kita bisa langsung mengetahui apakah kita menggunakan library yang terpengaruh — tanpa harus scan semua image satu per satu
- Compliance dan audit: regulasi tertentu mulai mensyaratkan SBOM (terutama untuk software pemerintah)
- Supply chain transparency: membuktikan bahwa software yang kita gunakan adalah apa yang kita klaim

**SBOM formats:**
- **SPDX (Software Package Data Exchange):** Standar ISO/IEC 5962, dikembangkan oleh Linux Foundation
- **CycloneDX:** OWASP standard, lebih fokus pada security use cases

### 4.4 Image Signing dengan Cosign

**Cosign** (bagian dari Sigstore project) memungkinkan signing dan verifikasi container images, memastikan bahwa image yang berjalan di cluster adalah image yang sama yang di-build dan divalidasi dalam CI/CD pipeline.

```bash
# Generate keypair (simpan private key dengan aman!)
cosign generate-key-pair
# Menghasilkan: cosign.key (private, JANGAN commit ke Git!) dan cosign.pub

# Sign image setelah build dan push ke registry
cosign sign --key cosign.key myregistry.io/myapp:v1.2.3@sha256:abc123...
# Signature disimpan di registry bersama image

# Verify signature sebelum deployment
cosign verify --key cosign.pub myregistry.io/myapp:v1.2.3@sha256:abc123...
# Exit 0 = valid, exit non-0 = invalid/unsigned → jangan deploy!
```

**Policy enforcement menggunakan Kyverno atau OPA Gatekeeper:**
```yaml
# Kyverno Policy: hanya izinkan image dari registry yang approved dan sudah di-sign
apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: require-signed-images
spec:
  validationFailureAction: Enforce
  rules:
  - name: check-image-signature
    match:
      any:
      - resources:
          kinds: ["Pod"]
    verifyImages:
    - imageReferences:
      - "myregistry.io/*"  # Hanya izinkan image dari registry kita
      attestors:
      - count: 1
        entries:
        - keys:
            publicKeys: |-
              -----BEGIN PUBLIC KEY-----
              [cosign public key di sini]
              -----END PUBLIC KEY-----
    # Jika image tidak dari registry kita atau tidak ada signature valid,
    # Pod akan ditolak oleh admission controller
```

## 5. Model atau Arsitektur

```mermaid
flowchart LR
    subgraph CI_CD["CI/CD Pipeline (Secure Build Pipeline)"]
        CODE["Source Code\n(Git)"]
        BUILD["Build Stage:\ndocker build"]
        SAST["SAST Scan:\ncode quality + secrets detection"]
        IMG_SCAN["Image Scan:\nTrivy — block if CRITICAL"]
        SBOM_GEN["SBOM Generation:\nSPDX/CycloneDX"]
        SIGN["Image Signing:\nCosign"]
        PUSH["Push to Registry\n(only if all gates pass)"]
    end
    
    subgraph REGISTRY["Private Container Registry"]
        APPROVED["Approved Images:\n• signed\n• no CRITICAL CVE\n• from known sources"]
        CONT_SCAN["Continuous Scanning:\nnew CVE detection"]
    end
    
    subgraph K8S["Kubernetes Cluster"]
        AC["Admission Controller:\n(Kyverno/OPA Gatekeeper)\nverify signature before admit"]
        PODS["Running Pods:\nhanya image approved"]
    end
    
    CODE --> BUILD --> SAST --> IMG_SCAN --> SBOM_GEN --> SIGN --> PUSH
    PUSH --> APPROVED
    APPROVED --> AC --> PODS
    CONT_SCAN --> APPROVED
```

## 6. Contoh Terapan

**CI/CD Security Gate menggunakan GitHub Actions (konsep):**
```yaml
# .github/workflows/secure-build.yml
name: Secure Container Build

on:
  push:
    branches: [main]

jobs:
  build-and-scan:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    
    - name: Build image
      run: docker build -t myapp:${{ github.sha }} .
    
    - name: Scan for CVEs
      uses: aquasecurity/trivy-action@master
      with:
        image-ref: myapp:${{ github.sha }}
        exit-code: '1'              # Fail pipeline jika ada CVE
        severity: 'CRITICAL,HIGH'  # Block pada severity ini
        format: 'sarif'
        output: 'trivy-results.sarif'
    
    - name: Generate SBOM
      run: trivy image --format spdx-json --output sbom.json myapp:${{ github.sha }}
    
    - name: Push to registry
      # Hanya dieksekusi jika semua steps sebelumnya berhasil
      run: |
        docker tag myapp:${{ github.sha }} myregistry.io/myapp:${{ github.sha }}
        docker push myregistry.io/myapp:${{ github.sha }}
    
    - name: Sign image
      run: cosign sign --key ${{ secrets.COSIGN_PRIVATE_KEY }} myregistry.io/myapp:${{ github.sha }}
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Melakukan container image security assessment menggunakan Trivy.

**Aktivitas (dalam lab berotorisasi menggunakan image publik untuk scanning):**
1. Pull beberapa image publik dari Docker Hub yang diberikan dosen (image yang sudah diketahui memiliki CVE untuk tujuan belajar).
2. Scan setiap image menggunakan Trivy.
3. Buat tabel perbandingan: nama image, jumlah CVE per severity, packages paling bermasalah.
4. Identifikasi: apakah ada CRITICAL CVE? Apa packagenya? Apakah ada versi yang sudah di-patch?
5. Rekomendasikan: gunakan image ini atau cari alternatif yang lebih aman?

**Output:** Image security assessment notes — bagian dari Eval-3.

## 8. Latihan Pemahaman

1. **(C4)** Seorang developer menggunakan tag `:latest` untuk base image dalam Dockerfile. "Nanti kita update Dockerfile-nya," katanya. Identifikasi 3 risiko keamanan dan operasional dari penggunaan `:latest`.

2. **(C3)** Apa perbedaan antara image *vulnerability* (CVE dalam OS package atau library) dan image *misconfiguration* (seperti running as root)? Mengapa keduanya perlu di-address dan dengan tools yang berbeda?

## 9. Latihan Terapan / Studi Kasus

Tim DevOps ingin mengimplementasikan "secure image pipeline" dari nol. Mereka saat ini menggunakan image dari Docker Hub langsung, tanpa scanning, tanpa private registry, dan deployment langsung via `kubectl apply`. Rancang implementasi bertahap (3 fase) yang meningkatkan keamanan secara progresif: (a) Fase 1: quick wins yang bisa diimplementasikan dalam minggu pertama; (b) Fase 2: kontrol intermediate (1 bulan); (c) Fase 3: mature pipeline (3 bulan). Untuk setiap fase, sebutkan: apa yang diimplementasikan, alat yang digunakan, dan metrik sukses.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Tiga risiko `:latest`: (a) **Tidak reproducible** — `:latest` hari ini mungkin berbeda dari `:latest` besok (image baru di-push ke registry); build yang "berhasil" hari ini mungkin gagal besok karena breaking change; (b) **Kerentanan tidak terprediksi** — pembaruan `:latest` mungkin memperkenalkan CVE baru atau perubahan behavior tanpa sepengetahuan tim; (c) **Tidak dapat diaudit** — tidak bisa menentukan dengan pasti versi mana yang berjalan di production, membuat incident response dan forensic lebih sulit. Solusi: pin ke specific digest (`@sha256:...`) atau ke tag yang tidak berubah (semantic versioning: `3.11.9-alpine3.19`).

**Soal 2:** Vulnerability (CVE) = kerentanan yang ada dalam kode library atau OS package yang bisa dieksploitasi. Tool: Trivy, Grype (scan terhadap CVE database). Misconfiguration = konfigurasi yang salah yang meningkatkan attack surface. Tool: Trivy config scan, Hadolint (Dockerfile linter), kube-bench. Keduanya harus di-address karena: CVE yang unpatch bisa dieksploitasi oleh attacker yang berhasil masuk ke container; misconfiguration menentukan apa yang bisa attacker lakukan setelah masuk (misalnya: container running as root dengan readWriteRootFilesystem → attacker bisa memodifikasi container filesystem dan bahkan escape ke host).

**Studi Kasus Fase Implementasi:** (a) Fase 1 (minggu pertama, zero disruption): setup Trivy CLI di developer laptop — scan image sebelum push (tidak blocking dulu, hanya awareness); buat private registry (Harbor atau AWS ECR); stop menggunakan `:latest`, mulai gunakan semantic version tags; (b) Fase 2 (1 bulan): integrasikan Trivy ke CI/CD sebagai gate yang WARN (belum block) untuk CRITICAL; migrate semua Dockerfile ke non-root user; buat registry policy: semua image harus dari private registry; (c) Fase 3 (3 bulan): Trivy CI/CD gate blocking untuk CRITICAL, warning untuk HIGH; implementasi Cosign image signing; implementasi Kyverno policy enforcement di cluster; generate SBOM untuk semua images; implementasi continuous scanning di registry untuk new CVE detection.

## 11. Ringkasan Bab

Container image security mencakup: pemilihan base image yang minimal (Alpine, Distroless), running as non-root, multi-stage build, dan pinning ke specific digest. Vulnerability scanning (Trivy, Grype) harus diintegrasikan dalam CI/CD pipeline sebagai blocking gate. SBOM memberikan inventaris komponen untuk rapid response terhadap CVE baru. Image signing (Cosign) memastikan image yang dijalankan di cluster adalah image yang telah divalidasi.

## 12. Refleksi Profesional

1. Log4Shell (CVE-2021-44228) adalah kerentanan kritis yang mempengaruhi jutaan aplikasi Java yang menggunakan Log4j. Organisasi yang memiliki SBOM dapat mengidentifikasi dalam hitungan jam apakah mereka menggunakan Log4j; organisasi tanpa SBOM membutuhkan berhari-hari atau berminggu-minggu. Berdasarkan pengalaman ini, bagaimana Anda meyakinkan manajemen untuk mengalokasikan resources dalam membangun SBOM infrastructure — bahkan sebelum insiden besar terjadi?

---

# BAB 8 — KUBERNETES SECURITY BASELINE DAN ADMISSION CONTROL

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Mengevaluasi keamanan konfigurasi Kubernetes cluster menggunakan CIS Benchmark
- Mengkonfigurasi RBAC Kubernetes dengan prinsip least privilege
- Memahami Admission Control sebagai garis pertahanan terakhir sebelum workload berjalan
- Mengidentifikasi dan memitigasi common Kubernetes security misconfigurations

*Berkaitan dengan Sub-CPMK-3, Eval-3 (25%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Kubernetes Security Baseline] --> B[API Server Security]
    B --> B1["Authentication:\nkubeconfig, OIDC, certificates"]
    B --> B2["Authorization:\nRBAC — Role, ClusterRole,\nRoleBinding, ClusterRoleBinding"]
    B --> B3["Audit logging:\nlog semua API requests"]
    A --> C[Admission Control]
    C --> C1["Built-in: LimitRanger,\nResourceQuota, PodSecurity"]
    C --> C2["Dynamic: Validating Webhook\n(Kyverno, OPA Gatekeeper)"]
    C --> C3["Mutating Webhook:\nauto-inject sidecar, labels"]
    A --> D[Node Security]
    D --> D1["Node OS hardening:\nCIS Linux Benchmark"]
    D --> D2["kubelet security:\nauthentication, authorization"]
    D --> D3["etcd encryption at rest"]
    A --> E[Network Security]
    E --> E1["NetworkPolicy:\ndefault-deny, whitelist approach"]
    E --> E2["Service mesh awareness:\nmTLS antar service"]
    E --> E3["Egress control:\nbatasi call keluar dari Pod"]
```

## 3. Pengantar Kontekstual

Kubernetes adalah platform yang sangat powerful — dan dengan kekuatan besar datang tanggung jawab konfigurasi yang besar. Cluster Kubernetes yang tidak dikonfigurasi dengan benar dapat memberikan attacker akses yang sangat luas jika satu komponen dikompromis. RBAC yang terlalu permisif, API server yang accessible tanpa autentikasi, atau tidak adanya Admission Control adalah jenis kesalahan yang menyebabkan "cloud-native breaches" yang semakin sering terjadi.

## 4. Landasan Teori

### 4.1 Kubernetes RBAC — Implementasi Least Privilege

**Objek RBAC Kubernetes:**
- **Role:** permissions dalam satu namespace
- **ClusterRole:** permissions cluster-wide atau lintas namespace
- **RoleBinding:** bind Role ke principal dalam namespace
- **ClusterRoleBinding:** bind ClusterRole ke principal (cluster-wide)

```yaml
# Contoh RBAC yang baik: Role minimal untuk backend service
# Hanya boleh read ConfigMap dan write ke specific resource
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  name: backend-service-role
  namespace: production
rules:
- apiGroups: [""]
  resources: ["configmaps"]
  resourceNames: ["app-config"]  # Hanya ConfigMap bernama "app-config"!
  verbs: ["get", "watch"]
- apiGroups: [""]
  resources: ["endpoints"]
  verbs: ["get", "list", "watch"]
# TIDAK ADA: secrets (tidak perlu), pods (tidak perlu), * (tidak boleh)

---
apiVersion: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  name: backend-service-binding
  namespace: production
subjects:
- kind: ServiceAccount
  name: backend-sa
  namespace: production
roleRef:
  kind: Role
  name: backend-service-role
  apiGroup: rbac.authorization.k8s.io
```

**RBAC Anti-patterns yang harus dihindari:**
```yaml
# ANTI-PATTERN 1: Wildcard verbs dan resources (sama dengan admin)
rules:
- apiGroups: ["*"]
  resources: ["*"]
  verbs: ["*"]

# ANTI-PATTERN 2: cluster-admin untuk ServiceAccount aplikasi
kind: ClusterRoleBinding
roleRef:
  kind: ClusterRole
  name: cluster-admin  # JANGAN!

# ANTI-PATTERN 3: Default ServiceAccount dibiarkan dengan default token
# Selalu set:
automountServiceAccountToken: false
# Di Pod spec, jika tidak perlu akses API server
```

### 4.2 Audit Logging di Kubernetes API Server

Kubernetes API server dapat dikonfigurasi untuk mencatat semua request yang masuk — ini adalah equivalent dari "Windows Event Log" untuk Kubernetes:

```yaml
# Audit policy — simpan sebagai /etc/kubernetes/audit-policy.yaml
# di control plane node
apiVersion: audit.k8s.io/v1
kind: Policy
rules:
# Catat semua request ke secrets (untuk detect unauthorized secret access)
- level: Metadata
  resources:
  - group: ""
    resources: ["secrets"]
  
# Catat exec ke Pod (kubectl exec — perlu dimonitor ketat)
- level: Request
  resources:
  - group: ""
    resources: ["pods/exec", "pods/portforward"]

# Catat perubahan RBAC
- level: RequestResponse
  resources:
  - group: "rbac.authorization.k8s.io"
    resources: ["clusterroles", "clusterrolebindings", "roles", "rolebindings"]

# Tidak perlu catat health checks (terlalu noisy)
- level: None
  users: ["system:kube-probe-*"]
  verbs: ["get"]
  resources:
  - group: ""
    resources: ["healthz", "readyz", "livez"]

# Default: catat metadata dari semua request lain
- level: Metadata
```

### 4.3 Admission Controllers

Admission Controller adalah plugin yang mengintersept request ke Kubernetes API server sebelum objek disimpan. Ada dua jenis:
1. **Validating:** Menerima atau menolak request berdasarkan rules
2. **Mutating:** Memodifikasi request sebelum diterima (misalnya auto-inject sidecar)

**PodSecurity Admission Controller (built-in):**
```yaml
# Namespace label untuk enforce Pod Security Standards
apiVersion: v1
kind: Namespace
metadata:
  name: production
  labels:
    pod-security.kubernetes.io/enforce: restricted
    pod-security.kubernetes.io/enforce-version: v1.27
```

**Kyverno Policy — Dynamic Admission Controller:**
```yaml
# Policy: wajibkan label owner pada semua Deployment
apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: require-labels
spec:
  validationFailureAction: Enforce
  rules:
  - name: check-for-labels
    match:
      any:
      - resources:
          kinds: ["Deployment"]
    validate:
      message: "Label 'owner' diperlukan pada semua Deployment"
      pattern:
        metadata:
          labels:
            owner: "?*"  # Harus ada, nilai apapun

---
# Policy: larang latest tag
apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: disallow-latest-tag
spec:
  validationFailureAction: Enforce
  rules:
  - name: check-image-tag
    match:
      any:
      - resources:
          kinds: ["Pod"]
    validate:
      message: "Image tag ':latest' dilarang. Gunakan specific version tag atau digest."
      pattern:
        spec:
          containers:
          - image: "!*:latest"  # Tidak boleh berakhiran :latest
```

### 4.4 NetworkPolicy untuk Micro-segmentation

```yaml
# Default deny all: tidak ada komunikasi kecuali yang explicitly diizinkan
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: default-deny-all
  namespace: production
spec:
  podSelector: {}        # Berlaku untuk semua Pod
  policyTypes:
  - Ingress
  - Egress
  # Tidak ada ingress/egress rules = deny all

---
# Allow: frontend bisa akses backend pada port 8080
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: allow-frontend-to-backend
  namespace: production
spec:
  podSelector:
    matchLabels:
      app: backend
  ingress:
  - from:
    - podSelector:
        matchLabels:
          app: frontend
    ports:
    - protocol: TCP
      port: 8080

---
# Allow: backend bisa akses database pada port 5432
# Dan bisa akses internet untuk updates (via egress)
apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: backend-egress-policy
  namespace: production
spec:
  podSelector:
    matchLabels:
      app: backend
  egress:
  - to:
    - podSelector:
        matchLabels:
          app: database
    ports:
    - protocol: TCP
      port: 5432
  - to:
    - namespaceSelector:
        matchLabels:
          kubernetes.io/metadata.name: kube-system  # DNS
    ports:
    - protocol: UDP
      port: 53
```

## 5. Model atau Arsitektur

```mermaid
sequenceDiagram
    participant DEV as Developer<br/>(kubectl)
    participant API as kube-apiserver
    participant AUTHN as Authentication
    participant AUTHZ as RBAC Authorization
    participant ADMIT as Admission Controllers<br/>(Kyverno, PodSecurity)
    participant ETCD as etcd
    participant AUDIT as Audit Log
    
    DEV->>API: kubectl apply -f pod.yaml
    API->>AUDIT: Log: request received
    API->>AUTHN: Verify credentials (kubeconfig cert/token)
    AUTHN-->>API: Identity: developer@company.com
    API->>AUTHZ: Can developer create Pod in production?
    AUTHZ-->>API: Denied (no create pod permission)
    API->>AUDIT: Log: DENY - insufficient permissions
    API-->>DEV: Error: Forbidden
    
    Note over DEV,ETCD: Jika credentials adalah CI/CD service account:
    
    DEV->>API: kubectl apply -f pod.yaml (sebagai ci-sa)
    API->>AUTHN: Verify ci-sa token
    AUTHN-->>API: Identity: ci-sa (ServiceAccount)
    API->>AUTHZ: Can ci-sa create Pod?
    AUTHZ-->>API: Allowed (has create pod permission)
    API->>ADMIT: Validate: does Pod meet security requirements?
    ADMIT-->>API: Denied: image using :latest tag (Kyverno policy)
    API->>AUDIT: Log: DENY - admission webhook rejection
    API-->>DEV: Error: image tag policy violation
```

## 6. Contoh Terapan

**kube-bench remediation untuk common findings:**

```bash
# CIS Check 1.2.1: Ensure anonymous auth is disabled (FAIL)
# Verifikasi current state:
ps aux | grep kube-apiserver | grep anonymous-auth
# Jika tidak ada flag → default adalah enabled!

# Remediation (dalam kubeadm-managed cluster):
# Edit /etc/kubernetes/manifests/kube-apiserver.yaml
# Tambahkan:
# - --anonymous-auth=false

# CIS Check 1.2.22: Ensure audit logging is enabled (FAIL)
# Tambahkan ke kube-apiserver.yaml:
# - --audit-log-path=/var/log/kubernetes/audit.log
# - --audit-policy-file=/etc/kubernetes/audit-policy.yaml
# - --audit-log-maxage=30
# - --audit-log-maxbackup=10
# - --audit-log-maxsize=100

# Verifikasi setelah remediation:
kubectl get pods -n kube-system kube-apiserver-<node-name> -o yaml | grep -A 50 containers
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menjalankan kube-bench dan menganalisis hasil untuk cluster Kubernetes lokal.

**Aktivitas (dalam lab Minikube/Kind yang diotorisasi):**
1. Setup Minikube atau Kind cluster di lab.
2. Deploy kube-bench sebagai Job.
3. Kumpulkan hasil (kubectl logs).
4. Kategorikan temuan: PASS, FAIL, WARN.
5. Untuk 3 FAIL tertinggi, tulis: deskripsi risiko, langkah remediation, dan verifikasi setelah remediation.
6. Implementasikan satu NetworkPolicy default-deny dan verifikasi efeknya.

**Output:** Kubernetes posture review notes — bagian dari Eval-3.

## 8. Latihan Pemahaman

1. **(C4)** Mengapa `automountServiceAccountToken: false` harus menjadi default untuk Pod yang tidak perlu mengakses Kubernetes API? Apa risiko jika dibiarkan default?

2. **(C5)** Evaluasi trade-off antara menggunakan PSS (Pod Security Standards, built-in) vs Dynamic Admission Controllers seperti Kyverno. Dalam skenario apa Anda akan merekomendasikan masing-masing atau kombinasi keduanya?

## 9. Latihan Terapan / Studi Kasus

Anda menemukan konfigurasi berikut di cluster production: (a) kube-apiserver dengan `--anonymous-auth=true` dan tidak ada audit logging; (b) beberapa Pod dengan `serviceAccountName: default` yang tidak diubah; (c) tidak ada NetworkPolicy di semua namespace; (d) ada ClusterRoleBinding yang memberikan `cluster-admin` ke ServiceAccount `monitoring-sa`. Untuk setiap temuan: (a) jelaskan skenario attack yang memungkinkan; (b) berikan remediation yang spesifik; (c) berikan cara verifikasi bahwa remediation telah berhasil.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Default ServiceAccount dalam Kubernetes secara otomatis me-mount token (JWT) ke dalam setiap Pod yang menggunakannya (di `/var/run/secrets/kubernetes.io/serviceaccount/token`). Risiko: (a) jika Pod dikompromis, attacker mendapatkan token yang bisa digunakan untuk mengakses Kubernetes API dengan hak default SA (yang mungkin memiliki lebih banyak permission daripada yang terlihat); (b) token ini valid selama Pod berjalan; (c) pada cluster yang tidak menggunakan RBAC ketat, default SA mungkin memiliki lebih banyak permissions dari yang seharusnya. `automountServiceAccountToken: false` mencegah token di-mount, sehingga bahkan jika Pod dikompromis, attacker tidak mendapatkan token untuk mengakses API server.

**Soal 2:** PSS (built-in): lebih sederhana, tidak memerlukan additional components, cocok untuk enforce standar Pod security profiles (Restricted/Baseline/Privileged). Kyverno: lebih fleksibel, dapat membuat custom policies (contoh: require labels, disallow :latest, verify image signatures), dapat mutating (auto-add labels, sidecars). Rekomendasi: gunakan PSS sebagai baseline enforcement (terpadu dengan K8s), tambahkan Kyverno untuk custom policies yang specific ke organisasi. Keduanya dapat berjalan bersama dan saling melengkapi.

**Studi Kasus:** (a) Anonymous auth: attacker tanpa credential dapat query API server, discover cluster topology, namespace, resource; remediation: `--anonymous-auth=false` di kube-apiserver; verifikasi: `curl https://[api-server]:6443/api/v1/pods` tanpa token → harus dapat `Unauthorized`. (b) Default SA: setiap Pod dapat coba query API dengan default SA token; audit: `kubectl auth can-i --list --as=system:serviceaccount:production:default`; remediation: `automountServiceAccountToken: false` di semua Pod yang tidak perlu API access; buat SA dedicated per workload. (c) Tidak ada NetworkPolicy: lateral movement bebas antar Pod; skenario: attacker di Pod frontend dapat mengakses langsung Pod database; remediation: deploy default-deny NetworkPolicy ke semua namespace, kemudian allow-list yang diperlukan; verifikasi: dari Pod frontend `curl backend-service:8080` → harus gagal sampai NetworkPolicy izinkan. (d) monitoring-sa dengan cluster-admin: jika monitoring Pod dikompromis, attacker mendapat full cluster access; remediation: create Role/ClusterRole dengan hanya permissions yang diperlukan monitoring (biasanya hanya get/list/watch metrics); verifikasi: `kubectl auth can-i create pods --as=system:serviceaccount:monitoring:monitoring-sa` → harus mengembalikan `no`.

## 11. Ringkasan Bab

Kubernetes RBAC harus mengimplementasikan least privilege: Role/ClusterRole dengan verbs dan resources spesifik, tidak ada wildcard. Audit logging pada API server mencatat semua request untuk forensic dan compliance. Admission Controllers (PSS built-in + Kyverno/OPA) adalah garis pertahanan terakhir yang memblokir workload tidak aman sebelum berjalan. NetworkPolicy dengan default-deny mengimplementasikan micro-segmentation dalam cluster.

## 12. Refleksi Profesional

1. Banyak organisasi menghindari mengaktifkan Admission Controllers yang ketat karena khawatir "mengganggu deployment yang sudah ada." Ini menciptakan technical debt keamanan yang terus bertambah. Bagaimana strategi Anda untuk memperkenalkan Admission Controls ke cluster production yang sudah berjalan — tanpa menyebabkan disruption besar — sambil memastikan deployment pipeline tidak tiba-tiba gagal?

---

# BAB 9 — LOGGING, OBSERVABILITY, DAN FORENSIC READINESS DI CLOUD

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Merancang logging architecture yang mendukung security investigation
- Mengkonfigurasi audit logging di cloud dan Kubernetes
- Memahami konsep forensic readiness dalam environment cloud/container
- Memastikan integritas dan reproducibility evidence dari cloud artifacts

*Berkaitan dengan Sub-CPMK-3, Eval-3 (25%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud/Container Observability] --> B[Log Sources]
    B --> B1["Cloud Provider:\nCloudTrail, Activity Log,\nVPC Flow Logs"]
    B --> B2["Kubernetes:\nAPI Audit Log, kubelet log"]
    B --> B3["Container/Application:\nstdout/stderr → logging stack"]
    B --> B4["Runtime Security:\nFalco alerts — syscall monitoring"]
    A --> C[Logging Architecture]
    C --> C1["Centralized: ELK/EFK Stack\nElasticsearch + Kibana"]
    C --> C2["Cloud-native: CloudWatch,\nAzure Monitor, GCP Logging"]
    C --> C3["Retention policy:\nsesuai compliance requirement"]
    C --> C4["SIEM integration:\nkorelasi event security"]
    A --> D[Forensic Readiness]
    D --> D1["Log preservation:\nimmutable storage, WORM"]
    D --> D2["Evidence integrity:\nhash log archives"]
    D --> D3["Reproducibility:\ncatat semua tool+config yang digunakan"]
    D --> D4["Container forensics:\nephemeral nature challenge"]
    A --> E[Detection — Falco]
    E --> E1["Runtime rules:\ndeteksi anomaly saat runtime"]
    E --> E2["Alert on:\nshell spawn, sensitive file access,\nnetwork anomaly"]
```

## 3. Pengantar Kontekstual

Cloud dan container environments menghasilkan volume log yang jauh lebih besar dari on-premises, namun juga menghadirkan tantangan yang unik: container yang ephemeral menghilangkan bukti begitu container dimatikan, cloud API calls tersebar di berbagai services dengan format berbeda, dan tanpa centralized logging, investigasi insiden menjadi sangat sulit. Forensic readiness harus direncanakan SEBELUM insiden terjadi — bukan setelah.

## 4. Landasan Teori

### 4.1 Log Sources dalam Cloud/Kubernetes Environment

**Cloud Provider Audit Logs:**

AWS CloudTrail mencatat semua API calls ke AWS services:
```json
// Contoh CloudTrail event — GetObject dari S3
{
  "eventVersion": "1.08",
  "userIdentity": {
    "type": "IAMUser",
    "userName": "alice",
    "arn": "arn:aws:iam::123456789:user/alice"
  },
  "eventTime": "2025-10-15T03:42:00Z",
  "eventSource": "s3.amazonaws.com",
  "eventName": "GetObject",
  "sourceIPAddress": "203.0.113.45",
  "requestParameters": {
    "bucketName": "company-production-data",
    "key": "customer-records/2025/records.csv"
  },
  "responseElements": null,
  "errorCode": null  // null = success
}

// Red flag: DeleteTrail event — attacker mencoba menghapus audit trail!
{
  "eventName": "DeleteTrail",
  "userIdentity": { "userName": "compromised-admin" },
  "eventTime": "2025-10-15T04:01:00Z"
  // ALERT: ini harus memicu immediate alert ke SOC
}
```

**Kubernetes API Audit Logs:**
```json
// Format Kubernetes audit log
{
  "kind": "Event",
  "apiVersion": "audit.k8s.io/v1",
  "level": "Request",
  "auditID": "abc-123",
  "stage": "ResponseComplete",
  "requestURI": "/api/v1/namespaces/production/secrets/db-credentials",
  "verb": "get",
  "user": {
    "username": "system:serviceaccount:default:compromised-sa"
  },
  "sourceIPs": ["10.0.10.5"],
  "responseStatus": {
    "code": 200  // Berhasil membaca secret!
  },
  "requestReceivedTimestamp": "2025-10-15T03:45:00Z"
}
```

### 4.2 Falco — Runtime Security Monitoring

**Falco** adalah Cloud Native Runtime Security tool yang memonitor syscalls dan API events untuk mendeteksi anomaly behavior saat runtime:

```yaml
# Contoh Falco rules untuk Kubernetes
# (untuk dipelajari dan dipahami, bukan dieksekusi di luar lab)

# Rule: Deteksi shell yang di-spawn dalam container
- rule: Terminal Shell in Container
  desc: A shell was used as the entrypoint/exec point into a container
  condition: >
    spawned_process and container
    and shell_procs and proc.tty != 0
    and container_entrypoint
  output: >
    A shell was spawned in a container
    (user=%user.name container=%container.name
     image=%container.image.repository
     shell=%proc.name parent=%proc.pname cmdline=%proc.cmdline)
  priority: WARNING
  tags: [container, shell]

# Rule: Deteksi akses ke file sensitive dalam container
- rule: Read Sensitive File Untrusted
  desc: An attempt to read a sensitive file by a process not trusted
  condition: >
    open_read and sensitive_files
    and not trusted_processes
    and container
  output: >
    Sensitive file opened for reading
    (user=%user.name command=%proc.cmdline file=%fd.name
     container=%container.name image=%container.image.repository)
  priority: WARNING
```

### 4.3 Centralized Logging Architecture

**EFK Stack (Elasticsearch, Fluentd, Kibana) untuk Kubernetes:**
```yaml
# Fluentd DaemonSet: agent yang berjalan di setiap node untuk collect logs
# (konsep deployment, bukan implementasi lengkap)
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: fluentd
  namespace: kube-system
spec:
  selector:
    matchLabels:
      app: fluentd
  template:
    spec:
      tolerations:
      - key: node-role.kubernetes.io/control-plane
        effect: NoSchedule
      containers:
      - name: fluentd
        image: fluent/fluentd-kubernetes-daemonset:v1.16-debian-elasticsearch8
        env:
        - name: FLUENT_ELASTICSEARCH_HOST
          value: "elasticsearch.logging.svc.cluster.local"
        volumeMounts:
        - name: varlog
          mountPath: /var/log             # Log dari node
        - name: containerlog
          mountPath: /var/lib/docker/containers  # Log dari container
          readOnly: true
      volumes:
      - name: varlog
        hostPath:
          path: /var/log
      - name: containerlog
        hostPath:
          path: /var/lib/docker/containers
```

### 4.4 Forensic Readiness di Cloud/Container Environment

**Prinsip forensic readiness untuk cloud/container:**

1. **Log sebelum insiden terjadi:** Aktifkan CloudTrail, VPC Flow Logs, Kubernetes audit logging, dan container logging SEBELUM ada insiden. Log yang tidak ada tidak dapat dipulihkan.

2. **Immutable log storage:** Simpan log ke S3 dengan Object Lock (WORM — Write Once Read Many) agar log tidak dapat dihapus atau dimodifikasi, bahkan oleh admin.

3. **Log retention yang sesuai compliance:** Minimum 90 hari online, 1 tahun archival (sesuaikan dengan regulasi industri). Untuk PCI-DSS: minimum 12 bulan.

4. **Evidence integrity:** Hash log archives (SHA-256) dan simpan hash di tempat terpisah. Ini membuktikan log tidak dimodifikasi sejak dikumpulkan.

5. **Container-specific challenges:**
   - Container ephemeral: log dari container yang sudah dihentikan hilang jika tidak di-stream ke centralized logging
   - **Solusi:** konfigurasi logging driver untuk semua container (Fluentd DaemonSet, CloudWatch agent)
   - Untuk forensic mendalam: jangan langsung hapus Pod — buat snapshot atau preserve container filesystem jika diperlukan untuk investigasi

```bash
# Preserve container filesystem untuk forensic (dalam lab/emergency response)
# Jalankan hanya dalam context IR yang diotorisasi

# Export container filesystem ke tar archive
docker export <container_id> > container_fs_$(date +%Y%m%d_%H%M%S).tar
sha256sum container_fs_$(date +%Y%m%d_%H%M%S).tar > container_fs.sha256

# Dalam Kubernetes: hentikan Pod (bukan delete) untuk preservasi
kubectl scale deployment <deployment> --replicas=0
# Jangan delete Pod — cari Pod yang masih ada
kubectl get pods -n production

# Describe Pod sebelum delete untuk capture state
kubectl describe pod <pod-name> -n production > pod_state_$(date +%Y%m%d).txt
kubectl get pod <pod-name> -n production -o yaml > pod_manifest.yaml
```

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph SOURCES["Log Sources"]
        CLOUDTRAIL["AWS CloudTrail\n(API calls)"]
        VPC_FL["VPC Flow Logs\n(network metadata)"]
        K8S_AUDIT["K8s API Audit Log\n(API server)"]
        CONTAINER_LOG["Container stdout/stderr\n(application logs)"]
        FALCO["Falco Alerts\n(runtime anomalies)"]
    end
    
    subgraph COLLECT["Collection Layer"]
        FLUENTD["Fluentd/Fluent Bit\n(DaemonSet per node)"]
        CW_AGENT["CloudWatch Agent"]
    end
    
    subgraph STORAGE["Centralized Storage"]
        ES["Elasticsearch\n(hot — 90 days)"]
        S3_WORM["S3 with Object Lock\n(cold — 1+ year, WORM)"]
    end
    
    subgraph ANALYSIS["Analysis Layer"]
        KIBANA["Kibana Dashboard\n(visualization)"]
        SIEM["SIEM\n(correlation rules, alerts)"]
    end
    
    CLOUDTRAIL & VPC_FL --> CW_AGENT
    K8S_AUDIT & CONTAINER_LOG & FALCO --> FLUENTD
    CW_AGENT & FLUENTD --> ES
    ES --> S3_WORM
    ES --> KIBANA & SIEM
```

## 6. Contoh Terapan

**Log analysis untuk mendeteksi credential abuse di AWS:**

```python
"""
Analisis CloudTrail log untuk detect unusual access pattern.
Script ini dijalankan pada log export yang sudah di-download — tidak memodifikasi sistem.
"""
import json
from collections import defaultdict
from datetime import datetime

def analyze_cloudtrail_logs(log_file_path):
    unusual_patterns = []
    
    with open(log_file_path, 'r') as f:
        logs = json.load(f)
    
    for record in logs.get('Records', []):
        user = record.get('userIdentity', {}).get('userName', 'Unknown')
        event_name = record.get('eventName', '')
        source_ip = record.get('sourceIPAddress', '')
        event_time = record.get('eventTime', '')
        
        # Flag 1: StopLogging — attacker mencoba menghapus trail
        if event_name in ['DeleteTrail', 'StopLogging', 'UpdateTrail']:
            unusual_patterns.append({
                'severity': 'CRITICAL',
                'type': 'Audit Trail Modification',
                'user': user,
                'event': event_name,
                'time': event_time,
                'ip': source_ip
            })
        
        # Flag 2: IAM privilege escalation
        if event_name in ['AttachUserPolicy', 'AttachRolePolicy'] and \
           'AdministratorAccess' in str(record.get('requestParameters', {})):
            unusual_patterns.append({
                'severity': 'CRITICAL',
                'type': 'Privilege Escalation',
                'user': user,
                'event': event_name,
                'time': event_time,
                'ip': source_ip
            })
        
        # Flag 3: CreateAccessKey (backdoor creation)
        if event_name == 'CreateAccessKey':
            unusual_patterns.append({
                'severity': 'HIGH',
                'type': 'New Access Key Created',
                'user': user,
                'event': event_name,
                'time': event_time,
                'ip': source_ip
            })
    
    return unusual_patterns

# Panggil dengan log export dari lab (bukan produksi)
results = analyze_cloudtrail_logs('cloudtrail_sample.json')
for finding in sorted(results, key=lambda x: x['severity']):
    print(f"[{finding['severity']}] {finding['type']}: {finding['user']} - {finding['time']}")
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menganalisis log dataset untuk mendeteksi security anomalies.

**Aktivitas (berbasis dataset yang disanitasi dari dosen):**
1. Dosen menyediakan CloudTrail log export (JSON, sudah di-anonimisasi) dan Kubernetes audit log extract.
2. Analisis CloudTrail: identifikasi event-event yang mencurigakan (DeleteTrail, CreateUser, AttachPolicy).
3. Analisis K8s audit log: identifikasi akses ke secrets, exec ke Pod, perubahan RBAC.
4. Buat timeline event yang mencurigakan.
5. Dokumentasikan dalam format evidence pack: daftar log yang dianalisis, hash file log, temuan, timestamp.

**Output:** Log analysis + evidence pack — bagian dari Eval-3.

## 8. Latihan Pemahaman

1. **(C4)** Mengapa S3 Object Lock (WORM) penting untuk log storage dalam konteks forensic? Apa yang terjadi jika attacker yang dikompromis memiliki akses S3 dan bisa menghapus log?

2. **(C4)** VPC Flow Logs hanya merekam metadata jaringan (IP, port, protocol, bytes, action) — tidak merekam payload. Apa keterbatasan ini untuk investigasi, dan bagaimana cara mengatasinya?

## 9. Latihan Terapan / Studi Kasus

Organisasi Anda tidak memiliki logging yang terpusat. Setelah insiden terdeteksi, tim IR menemukan bahwa: log container sudah hilang (Pod di-restart), CloudTrail tidak diaktifkan (hemat biaya), dan VPC Flow Logs tidak dikonfigurasi. Tim tidak bisa menentukan scope insiden, initial access vector, atau apakah data exfiltration terjadi. (a) Apa pelajaran utama dari skenario ini tentang forensic readiness? (b) Jika Anda diminta membangun logging strategy dari nol pasca-insiden ini, apa prioritas pertama dalam 48 jam, satu minggu, dan satu bulan? (c) Bagaimana Anda meyakinkan manajemen bahwa biaya logging adalah investasi, bukan pengeluaran?

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** S3 Object Lock (WORM) mencegah penghapusan atau modifikasi objek yang sudah disimpan, bahkan oleh IAM user dengan hak admin. Tanpa WORM: attacker yang berhasil mendapatkan hak S3 admin dapat menghapus log audit, menghilangkan jejak aksi mereka. Ini adalah taktik anti-forensik yang umum digunakan. Dengan WORM: log tidak dapat dihapus sampai retention period habis, memberikan jaminan bahwa log yang ada adalah log yang asli dan lengkap. Ini juga memenuhi persyaratan compliance (PCI-DSS, SOC2, ISO 27001) yang mensyaratkan log tidak dapat dimodifikasi.

**Soal 2:** Keterbatasan VPC Flow Logs: (a) Tidak bisa melihat isi data yang ditransfer — tidak tahu apakah yang ditransfer adalah data sensitif atau traffic normal; (b) Tidak bisa decode protocol-specific content; (c) Tidak bisa lihat HTTP headers atau request body. Cara mengatasi: (a) Untuk investigation yang lebih dalam: gunakan Traffic Mirroring (AWS) untuk mengambil full packet capture pada traffic specific — ini lebih mahal dan harus selective; (b) Gunakan proxy logs (jika ada) yang mencatat HTTP request/response headers; (c) Gunakan Application Load Balancer access logs yang mencatat HTTP request details; (d) Correlate VPC Flow Logs dengan application logs dari SIEM untuk mendapatkan gambaran yang lebih lengkap.

**Studi Kasus:** (a) Pelajaran utama: forensic readiness tidak bisa dimulai saat insiden terjadi — harus dibangun sebelumnya. Log yang tidak ada tidak bisa dipulihkan. Cost of logging jauh lebih murah dari cost of not knowing. (b) Prioritas: 48 jam pertama — aktifkan CloudTrail segera (global, all regions, S3 + Object Lock); aktifkan VPC Flow Logs untuk semua VPC; aktifkan Kubernetes audit logging (jika ada K8s). Satu minggu — deploy centralized logging (Fluentd/CloudWatch agent ke semua EC2/Pods); set retention policy; alert untuk critical events (DeleteTrail, CreateUser). Satu bulan — SIEM integration; Falco untuk runtime detection; log review baseline (berapa normal volume per hari?); forensic runbook. (c) ROI argument: tanpa logging, scope insiden tidak diketahui → harus treat seluruh infrastruktur sebagai potentially compromised → biaya remediation jauh lebih besar dari biaya logging. Regulasi (UU PDP, POJK, PCI-DSS) mensyaratkan logging dan audit trail — non-compliance berisiko denda. Cyber insurance semakin mensyaratkan logging sebagai baseline security control.

## 11. Ringkasan Bab

Logging di cloud memerlukan konfigurasi eksplisit dari berbagai sumber: CloudTrail (API calls), VPC Flow Logs (network), Kubernetes audit log (API server), dan container logs (stdout/stderr). Falco menyediakan runtime anomaly detection berdasarkan syscall monitoring. Forensic readiness mensyaratkan: log sebelum insiden, immutable storage (WORM), retention yang sesuai, dan evidence integrity (hash). Container forensics menghadapi tantangan ephemeral namun dapat dimitigasi dengan centralized logging dan container state preservation saat IR.

## 12. Refleksi Profesional

1. Ada dilema dalam logging cloud: semakin banyak log yang dikumpulkan, semakin baik untuk forensic, namun juga semakin banyak data pribadi pengguna yang mungkin ter-log (IP addresses, request parameters yang mengandung data). Bagaimana Anda menyeimbangkan kebutuhan forensic readiness dengan kewajiban privasi pengguna di bawah UU PDP No. 27/2022? Log apa yang harus disimpan, dan apa yang harus di-redact atau tidak di-log?


---

# BAB 10 — SECURE CLOUD ARCHITECTURE DAN POLICY-AS-CODE

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Merancang arsitektur cloud yang menerapkan defense-in-depth
- Memahami prinsip policy-as-code dan implementasinya
- Menggunakan tools IaC security scanning (Checkov, Conftest)
- Membuat rekomendasi arsitektur berbasis threat model

*Berkaitan dengan Sub-CPMK-4, Eval-4 (20%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Secure Cloud Architecture] --> B[Defense-in-Depth Layers]
    B --> B1["Layer 1: Identity\n(IAM, MFA, OIDC)"]
    B --> B2["Layer 2: Network\n(VPC, SG, NACL, WAF)"]
    B --> B3["Layer 3: Compute\n(hardened image, no SSH,\nIMDS v2 only)"]
    B --> B4["Layer 4: Data\n(encryption at rest + transit,\nbackup, WORM)"]
    B --> B5["Layer 5: Monitoring\n(CloudTrail, GuardDuty, SIEM)"]
    A --> C[Policy-as-Code]
    C --> C1["OPA/Conftest:\nvalidasi IaC sebelum apply"]
    C --> C2["Checkov:\nscan Terraform, CloudFormation\nuntuk security misconfigs"]
    C --> C3["Sentinel (Terraform Enterprise):\ncomercial grade policy enforcement"]
    C --> C4["CI/CD integration:\ngates di pipeline build"]
    A --> D[Secure IaC Practices]
    D --> D1["Terraform: state encryption,\nremote backend"]
    D --> D2["Least privilege:\nterraform apply role — minimal rights"]
    D --> D3["Secret handling:\nnever hardcode, gunakan Vault/SSM"]
    D --> D4["Drift detection:\nterraform plan in CI — detect manual changes"]
```

## 3. Pengantar Kontekstual

Infrastruktur cloud yang dibuat secara manual (melalui web console) rentan terhadap inkonsistensi, human error, dan tidak dapat diaudit dengan mudah. Infrastructure-as-Code (IaC) mengatasi masalah ini — namun IaC yang ditulis tanpa kontrol keamanan dapat menyebarkan misconfiguration secara masif dan konsisten. Policy-as-Code mengotomatiskan verifikasi bahwa IaC memenuhi standar keamanan sebelum deployed.

## 4. Landasan Teori

### 4.1 Defense-in-Depth dalam Cloud Architecture

Defense-in-depth di cloud bukan berarti memasang banyak produk keamanan — melainkan memastikan bahwa tidak ada single point of failure dalam posture keamanan:

```
Jika IAM dikompromis → Network controls mencegah lateral movement
Jika network bypassed → Compute hardening mencegah code execution
Jika compute dikompromis → Data encryption mencegah exfiltration yang berguna
Jika data diakses → Monitoring mendeteksi dan memungkinkan response
```

### 4.2 Terraform Security Best Practices

```hcl
# Terraform remote state — enkripsi dan akses terkontrol
terraform {
  backend "s3" {
    bucket         = "company-terraform-state"
    key            = "production/terraform.tfstate"
    region         = "ap-southeast-1"
    encrypt        = true                    # Enkripsi state file di S3
    dynamodb_table = "terraform-state-lock"  # Prevent concurrent apply
    
    # State bucket harus memiliki:
    # - Versioning enabled (recovery jika state corrupt)
    # - Object Lock (prevent state deletion)
    # - Access log (audit siapa yang akses state)
  }
}

# JANGAN simpan sensitive values dalam terraform variables langsung
# BAIK: gunakan data source dari Secret Manager
data "aws_secretsmanager_secret_version" "db_password" {
  secret_id = "production/database/password"
}

resource "aws_db_instance" "main" {
  identifier = "production-db"
  # Gunakan value dari Secret Manager, bukan hardcoded
  password   = data.aws_secretsmanager_secret_version.db_password.secret_string
}
```

### 4.3 Checkov — IaC Security Scanner

```bash
# Scan Terraform code dalam direktori saat ini
checkov -d .

# Scan dengan output detail dan fail fast pada HIGH severity
checkov -d . --severity HIGH --compact

# Contoh output Checkov:
# Check: CKV_AWS_20: "Ensure that S3 Buckets are encrypted"
# PASSED for resource: aws_s3_bucket.logs
# 
# Check: CKV_AWS_24: "Ensure that RDS database is not publicly accessible"  
# FAILED for resource: aws_db_instance.main
# File: /terraform/main.tf:45-60
#   45 | resource "aws_db_instance" "main" {
#   ...
#   52 |   publicly_accessible = true  # <-- MISCONFIGURATION
#
# Passed checks: 23, Failed checks: 2, Skipped checks: 0

# Scan dengan output SARIF untuk CI/CD integration
checkov -d . --output sarif --output-file-path checkov-results.sarif
```

### 4.4 OPA (Open Policy Agent) dan Conftest

```rego
# Policy: semua S3 bucket harus memiliki versioning diaktifkan
# Simpan sebagai policy/s3-versioning.rego

package main

deny[msg] {
  # Iterasi semua resource dalam Terraform plan
  resource := input.resource_changes[_]
  resource.type == "aws_s3_bucket"
  resource.change.after.versioning[_].enabled != true
  msg := sprintf(
    "S3 bucket '%v' harus mengaktifkan versioning untuk recovery dan audit",
    [resource.address]
  )
}

deny[msg] {
  resource := input.resource_changes[_]
  resource.type == "aws_s3_bucket"
  resource.change.after.server_side_encryption_configuration == []
  msg := sprintf(
    "S3 bucket '%v' harus mengaktifkan server-side encryption",
    [resource.address]
  )
}
```

```bash
# Jalankan Conftest dengan policy di atas
terraform plan -out plan.tfplan
terraform show -json plan.tfplan > plan.json
conftest test plan.json --policy policy/

# Output:
# FAIL - plan.json - main - S3 bucket 'aws_s3_bucket.logs' harus mengaktifkan versioning
# 1 tests, 0 passed, 0 warnings, 1 failure, 0 exceptions
```

## 5. Model atau Arsitektur

```mermaid
flowchart LR
    subgraph IaC_Pipeline["IaC Security Pipeline"]
        WRITE["Developer\nWrite Terraform"]
        TFLINT["tflint:\nstyle + syntax check"]
        CHECKOV["Checkov:\nsecurity scan"]
        CONFTEST["Conftest + OPA:\ncustom policy check"]
        PLAN["terraform plan:\nreview planned changes"]
        APPLY["terraform apply:\ndeploy jika semua gate pass"]
    end
    
    subgraph RUNTIME_CHECKS["Runtime Drift Detection"]
        SCHED_PLAN["Scheduled terraform plan\n(nightly)"]
        DRIFT_ALERT["Alert if drift detected\n(someone made manual change!)"]
    end
    
    WRITE --> TFLINT --> CHECKOV --> CONFTEST --> PLAN --> APPLY
    APPLY --> SCHED_PLAN --> DRIFT_ALERT
```

## 6. Contoh Terapan

**Secure three-tier architecture di AWS menggunakan Terraform (framework, bukan full implementation):**

```hcl
# Tier 1: Web (public subnet) — hanya menerima traffic dari internet pada port 443
# Tier 2: Application (private subnet) — hanya dari web tier
# Tier 3: Data (data subnet) — hanya dari application tier

module "vpc" {
  source  = "terraform-aws-modules/vpc/aws"
  version = "5.1.2"
  
  name = "production-vpc"
  cidr = "10.0.0.0/16"
  
  azs              = ["ap-southeast-1a", "ap-southeast-1b"]
  public_subnets   = ["10.0.1.0/24", "10.0.2.0/24"]   # Web tier
  private_subnets  = ["10.0.10.0/24", "10.0.11.0/24"] # App tier
  database_subnets = ["10.0.20.0/24", "10.0.21.0/24"] # Data tier
  
  enable_nat_gateway     = true    # App tier bisa outbound ke internet
  single_nat_gateway     = false   # HA: satu NAT per AZ
  enable_vpn_gateway     = false   # Tidak perlu untuk cloud-native
  
  enable_flow_log                   = true   # VPC Flow Logs wajib
  create_flow_log_cloudwatch_log_group = true
  create_flow_log_cloudwatch_iam_role  = true
  flow_log_max_aggregation_interval    = 60
}
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menjalankan Checkov pada Terraform code yang sengaja memiliki misconfigurations.

**Aktivitas (dalam lab lingkungan terisolasi):**
1. Dosen menyediakan Terraform code dengan 5–10 misconfiguration yang sengaja dimasukkan.
2. Jalankan Checkov: `checkov -d . --output json > results.json`.
3. Analisis setiap FAIL: apa misconfiguration-nya, apa risikonya, bagaimana memperbaikinya?
4. Perbaiki Terraform code.
5. Jalankan ulang Checkov dan verifikasi semua gate PASS.
6. Dokumentasikan dalam format: misconfiguration, risk, remediation.

**Output:** IaC security review + remediation report — bagian dari Eval-4.

## 8. Latihan Pemahaman

1. **(C4)** Mengapa "terraform state" adalah target menarik bagi attacker? State file berisi informasi apa? Apa kontrol keamanan yang harus diterapkan pada S3 bucket yang menyimpan state file?

2. **(C4)** Apa perbedaan antara IaC security scanning (Checkov) dan runtime cloud posture assessment (AWS Config)? Kapan masing-masing paling berguna?

## 9. Latihan Terapan / Studi Kasus

Organisasi memiliki tim developer yang menggunakan Terraform untuk deploy infrastruktur. Saat ini tidak ada IaC security gate — developer bisa `terraform apply` langsung ke production dengan credential admin. Audit menemukan: 3 S3 bucket dengan public access, 2 RDS instance publicly accessible, tidak ada encryption di beberapa EBS volumes, dan security group dengan 0.0.0.0/0 untuk SSH. Rancang: (a) Immediate remediation plan untuk menutup eksposur yang ada; (b) IaC security pipeline yang mencegah ini terulang; (c) Access model: siapa yang boleh menjalankan `terraform apply` ke production, dan dengan credential seperti apa (hint: pertimbangkan short-lived credentials, CI/CD role, manual approval gate).

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Terraform state file berisi: semua resource IDs, IP addresses, passwords (jika hardcoded — yang tidak boleh terjadi namun sering terjadi), ARNs, security group IDs, subnet IDs, dan essentially peta lengkap infrastruktur. Bagi attacker, ini adalah reconnaissance yang sudah selesai dilakukan — mereka tidak perlu scan infrastruktur karena state file sudah memberikan gambaran lengkap. Kontrol keamanan: (a) enkripsi S3 bucket (SSE-KMS dengan CMK); (b) akses S3 bucket hanya untuk Terraform IAM role, bukan developer secara individual; (c) S3 versioning untuk recovery; (d) S3 access logging untuk audit; (e) jangan simpan sensitive values dalam state (gunakan data sources dari Secret Manager).

**Soal 2:** Checkov (IaC scanning) = preventive control — memeriksa konfigurasi sebelum diapply; mendeteksi misconfiguration sebelum menjadi masalah di environment; berguna di CI/CD pipeline. AWS Config (runtime posture) = detective control — memonitor konfigurasi resource yang sudah berjalan; mendeteksi drift dari baseline (misalnya S3 bucket yang semula private tiba-tiba public karena manual change); berguna untuk ongoing compliance monitoring. Keduanya diperlukan: Checkov mencegah misconfiguration baru; AWS Config mendeteksi perubahan tidak sah pada resource yang sudah ada.

**Studi Kasus:** (a) Immediate remediation: disable public access di semua S3 bucket (AWS S3 Block Public Access setting); ubah RDS instance publicly_accessible=false (perlu maintenance window); encrypt EBS volumes (perlu snapshot+restore); ubah security group SSH dari 0.0.0.0/0 ke IP specific atau VPN endpoint. (b) IaC pipeline: tambahkan tflint → Checkov → Conftest → terraform plan → manual approval (untuk production) → terraform apply; set Checkov minimum severity HIGH dengan exit code 1 (gagalkan pipeline); custom OPA policy untuk org-specific rules. (c) Access model: developer tidak punya AWS credential production langsung; CI/CD pipeline menggunakan IAM role dengan permission minimal (hanya resource yang perlu); untuk emergency, gunakan break-glass procedure dengan MFA dan audit trail; terraform apply ke production harus melalui PR review + automated gate pass + manual approval dari security owner.

## 11. Ringkasan Bab

Policy-as-code mengotomatiskan enforcement standar keamanan dalam IaC. Checkov memvalidasi Terraform/CloudFormation terhadap ratusan security checks; OPA/Conftest memungkinkan custom policy yang spesifik untuk organisasi. Defense-in-depth di cloud melibatkan kontrol berlapis: identity, network, compute, data, dan monitoring. Terraform state harus dilindungi dengan enkripsi dan akses terkontrol karena berisi peta lengkap infrastruktur.

## 12. Refleksi Profesional

1. Policy-as-code membuat keputusan keamanan menjadi eksplisit dan dapat diaudit — setiap policy adalah pernyataan tertulis tentang apa yang diizinkan dan tidak. Namun, siapa yang berwenang menulis dan mengubah policy tersebut? Bagaimana Anda mengelola governance dari policy-as-code itu sendiri — agar tidak ada yang bisa melemahkan policy tanpa review?

---

# BAB 11 — MONITORING, BACKUP-RECOVERY, DAN RESILIENSI CLOUD

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Merancang monitoring strategy untuk cloud environment
- Mendefinisikan dan memvalidasi RTO/RPO untuk cloud workloads
- Merancang backup dan disaster recovery plan untuk cloud
- Menghubungkan konsep resiliensi dengan Zero Trust Architecture

*Berkaitan dengan Sub-CPMK-4, Eval-4 (20%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud Resilience Strategy] --> B[Monitoring]
    B --> B1["SIEM integration:\nkorelasi event lintas service"]
    B --> B2["Alerting:\nthreshold, anomaly-based"]
    B --> B3["Dashboard:\nvisibilitas real-time posture"]
    B --> B4["Runbook automation:\nplaybook otomatis untuk alert umum"]
    A --> C[Backup dan Recovery]
    C --> C1["RTO: Recovery Time Objective\nberapa lama boleh downtime?"]
    C --> C2["RPO: Recovery Point Objective\nberapa banyak data boleh hilang?"]
    C --> C3["3-2-1 rule:\n3 kopian, 2 media, 1 offsite"]
    C --> C4["Immutable backup:\nProtection dari ransomware"]
    A --> D[Disaster Recovery Patterns]
    D --> D1["Backup & Restore:\nslow, murah — RTO: hours/days"]
    D --> D2["Pilot Light:\ninfrastruktur minimal always-on"]
    D --> D3["Warm Standby:\nscaled-down version always running"]
    D --> D4["Multi-site Active/Active:\nmahal, RTO: seconds/zero"]
    A --> E[Zero Trust dalam Cloud Resilience]
    E --> E1["Never trust, always verify:\nbahkan setelah recovery, re-verify identitas"]
    E --> E2["Microsegmentation:\nbatasi blast radius insiden"]
    E --> E3["Continuous validation:\nposture dinilai terus-menerus"]
```

## 3. Pengantar Kontekstual

Insiden cloud tidak selalu berarti breach — bisa juga availability failure, data corruption, atau kesalahan operasional. Resiliensi adalah kemampuan sistem untuk bertahan dari gangguan dan pulih kembali. Dalam konteks keamanan, resiliensi juga berarti: jika satu kontrol gagal, sistem masih bisa berfungsi dan pulih; jika terjadi compromise, dampaknya terbatas dan recovery dapat dilakukan dengan cepat.

## 4. Landasan Teori

### 4.1 RTO dan RPO: Mendefinisikan dan Memvalidasi

**Recovery Time Objective (RTO):** Berapa lama maksimum sistem boleh tidak tersedia (downtime)? RTO menentukan kecepatan recovery yang diperlukan.

**Recovery Point Objective (RPO):** Berapa banyak data yang boleh hilang (diukur dalam waktu)? RPO menentukan frekuensi backup yang diperlukan.

```
Contoh:
RTO = 4 jam → sistem harus pulih dalam 4 jam setelah insiden
RPO = 1 jam → kita tidak boleh kehilangan lebih dari 1 jam data
                → backup harus dilakukan minimal setiap 1 jam
```

**Matrix DR strategy vs RTO/RPO:**

| DR Pattern | RTO | RPO | Biaya Relatif |
|---|---|---|---|
| Backup & Restore | Hours–Days | Hours–Days | Rendah |
| Pilot Light | 10s of minutes | Minutes | Sedang |
| Warm Standby | Minutes | Seconds–Minutes | Sedang-Tinggi |
| Multi-site Active/Active | Near-zero | Near-zero | Tinggi |

### 4.2 Immutable Backup sebagai Defense terhadap Ransomware

Ransomware sering menyerang backup sebelum mengenkripsi data utama. Immutable backup memastikan backup tidak dapat dimodifikasi atau dihapus:

```bash
# AWS S3 Object Lock untuk backup immutable
# Konfigurasi saat pembuatan bucket (tidak bisa diubah setelah dibuat)
aws s3api create-bucket \
    --bucket company-immutable-backup \
    --region ap-southeast-1 \
    --create-bucket-configuration LocationConstraint=ap-southeast-1

aws s3api put-object-lock-configuration \
    --bucket company-immutable-backup \
    --object-lock-configuration '{
        "ObjectLockEnabled": "Enabled",
        "Rule": {
            "DefaultRetention": {
                "Mode": "COMPLIANCE",  # Tidak bisa diubah bahkan oleh admin!
                "Days": 90
            }
        }
    }'

# Mode COMPLIANCE = tidak ada yang bisa menghapus object sampai retention period habis
# Mode GOVERNANCE = dapat di-override oleh user dengan s3:BypassGovernanceRetention permission
# Untuk proteksi ransomware, gunakan COMPLIANCE mode
```

### 4.3 Multi-AZ vs Multi-Region

```hcl
# Terraform: RDS dengan Multi-AZ untuk high availability
resource "aws_db_instance" "main" {
  identifier           = "production-db"
  engine               = "postgres"
  engine_version       = "15.4"
  instance_class       = "db.t3.medium"
  allocated_storage    = 100
  
  multi_az             = true  # Standby di AZ lain, failover otomatis (2-3 menit)
  
  backup_retention_period = 30  # Simpan point-in-time recovery 30 hari
  backup_window           = "02:00-03:00"  # Backup saat traffic rendah
  
  deletion_protection  = true   # Tidak bisa dihapus tanpa disable ini dulu
  
  storage_encrypted    = true   # Enkripsi data at rest
  kms_key_id          = aws_kms_key.rds_key.arn
}
```

### 4.4 Zero Trust dalam Konteks Resiliensi

Zero Trust Architecture (ZTA, NIST SP 800-207) relevan dengan resiliensi cloud:

- **Microsegmentation mengurangi blast radius:** Jika satu workload dikompromis, ZTA mencegah attacker bergerak ke workload lain.
- **Continuous verification membantu detect anomaly:** Dalam ZTA, setiap request diverifikasi ulang — perilaku tidak normal terdeteksi lebih cepat.
- **Identity-based access control lebih resilient:** Jika network perimeter dikompromis (misalnya VPN breach), ZTA berbasis identity masih memberikan layer kontrol yang valid.
- **Post-recovery re-verification:** Setelah disaster recovery, semua credential dan access harus di-review — tidak bisa diasumsikan bahwa credential yang ada sebelum insiden masih valid dan belum dikompromis.

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph PROD["Production Region (ap-southeast-1)"]
        AZ1["AZ-1a:\nWeb + App + DB Primary"]
        AZ2["AZ-1b:\nWeb + App + DB Standby"]
        AZ1 <--"Multi-AZ Sync Replication"--> AZ2
    end
    
    subgraph DR["DR Region (ap-southeast-3 — Jakarta)"]
        DR_WARM["Warm Standby:\nScaled-down infrastructure"]
        DR_BACKUP["Immutable Backup\n(S3 WORM + Object Lock)"]
    end
    
    subgraph MONITOR["Monitoring Layer"]
        CW["CloudWatch Metrics + Alarms"]
        GUARDDUTY["GuardDuty: Threat Detection"]
        SIEM_BOX["SIEM: Event Correlation"]
    end
    
    PROD -->|"Async Replication\n(cross-region)"| DR_WARM
    PROD -->|"Backup\n(RTO: 1h, RPO: 1h)"| DR_BACKUP
    
    CW & GUARDDUTY --> SIEM_BOX
    SIEM_BOX -->|"Alert: Failover Trigger"| DR_WARM
    
    DR_WARM -->|"Failover:\n10-30 minutes"| RECOVERY["Recovery Site\nLive Traffic"]
    DR_BACKUP -->|"Restore:\n2-4 hours"| RECOVERY
```

## 6. Contoh Terapan

**Backup testing procedure (wajib untuk validasi RPO/RTO):**

```bash
# Backup tidak berguna jika tidak pernah ditest restore-nya
# Prosedur test restore (dalam environment test, BUKAN production):

# 1. Identifikasi backup yang akan di-restore (backup kemarin)
aws rds describe-db-snapshots \
    --db-instance-identifier production-db \
    --query 'DBSnapshots[?Status==`available`] | sort_by(@, &SnapshotCreateTime) | [-1]'

# 2. Restore ke instance test (bukan production!)
aws rds restore-db-instance-from-db-snapshot \
    --db-instance-identifier restore-test-$(date +%Y%m%d) \
    --db-snapshot-identifier rds:production-db-2025-10-15-02-00 \
    --db-instance-class db.t3.small \
    --no-multi-az \
    --no-publicly-accessible

# 3. Catat waktu restore selesai → bandingkan dengan RTO target

# 4. Verifikasi data integrity
# - Periksa record count
# - Spot check beberapa data kritikal
# - Jalankan application smoke test terhadap DB restore

# 5. Dokumentasikan hasil: berapa lama? Data lengkap? Aplikasi bisa connect?

# 6. Hapus instance test setelah selesai
aws rds delete-db-instance \
    --db-instance-identifier restore-test-$(date +%Y%m%d) \
    --skip-final-snapshot
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Merancang disaster recovery plan untuk skenario cloud outage.

**Aktivitas (desktop-based, tidak memerlukan cloud account):**
1. Dosen memberikan skenario: sebuah aplikasi e-commerce dengan komponen web server (EC2), application server, database (RDS), dan object storage (S3).
2. Mahasiswa mendefinisikan: (a) business criticality dari setiap komponen; (b) RTO dan RPO yang realistis untuk setiap komponen; (c) DR strategy yang sesuai (backup/restore, pilot light, warm standby, active-active).
3. Buat diagram arsitektur DR (menggunakan Mermaid atau draw.io sesuai petunjuk dosen).
4. Identifikasi: apa yang harus ditest sebelum insiden terjadi? Buat checklist DR drill.

**Output:** DR architecture design + runbook — bagian dari Eval-4.

## 8. Latihan Pemahaman

1. **(C4)** Jelaskan mengapa backup ke bucket S3 yang berada di account yang sama dengan production — tanpa Object Lock — tidak memberikan perlindungan yang memadai terhadap ransomware. Bagaimana solusinya?

2. **(C5)** Sebuah organisasi memiliki RTO = 15 menit dan RPO = 5 menit untuk aplikasi core banking. Evaluasi apakah Warm Standby memenuhi requirement ini, dan jika tidak, apa yang diperlukan?

## 9. Latihan Terapan / Studi Kasus

Sebuah perusahaan fintech memiliki database PostgreSQL di AWS RDS dengan backup retention 7 hari. Pada hari Jumat sore, ditemukan bahwa data customer di-corrupt oleh bug yang di-deploy hari Rabu. Business requirement: (a) harus bisa restore ke state sebelum bug di-deploy (Rabu pagi); (b) recovery harus selesai sebelum Senin pagi (untuk operasional weekly batch). Analisis: (a) apakah backup strategy saat ini mendukung requirement tersebut? (b) Apa proses teknis restore ke point-in-time spesifik? (c) Apa risiko recovery dan bagaimana mitigasinya? (d) Data transaksi yang terjadi antara Rabu deploy hingga Jumat deteksi — bagaimana dihandle?

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Jika backup S3 bucket berada di AWS account yang sama, IAM role yang dikompromis oleh attacker/ransomware mungkin juga memiliki akses ke bucket backup tersebut. Attacker ransomware modern pertama-tama menghapus backup sebelum mengenkripsi data utama — ini membuat korban tidak punya pilihan selain membayar. Solusi berlapis: (a) Simpan backup di AWS account terpisah yang terisolasi (dedicated backup account dalam AWS Organizations); (b) Gunakan S3 Object Lock dalam COMPLIANCE mode — bahkan admin account tidak bisa menghapus sebelum retention period; (c) Cross-region replication: backup di region berbeda; (d) Gunakan IAM role untuk backup yang hanya memiliki hak write (put) ke backup bucket, tidak punya hak delete.

**Soal 2:** Warm Standby untuk RTO 15 menit: Warm Standby dengan failover otomatis dan health check yang sudah dikonfigurasi dengan baik kemungkinan bisa mencapai 10–15 menit. Ini borderline — bergantung pada kompleksitas DNS failover, health check intervals, dan waktu untuk redirect traffic. Untuk RPO 5 menit, Warm Standby memerlukan async replication dengan lag maksimum 5 menit, yang bisa dicapai dengan RDS Multi-AZ synchronous (lag sangat kecil, tetapi hanya dalam satu region) atau async replication dengan monitoring lag secara ketat. Kesimpulan: untuk RTO 15 menit yang ketat dan RPO 5 menit, diperlukan Multi-AZ (untuk RPO) plus infrastruktur warm standby yang sudah fully scaled (bukan scaled-down) agar failover cepat. Active/Active adalah pilihan lebih aman untuk requirement seketat ini.

**Studi Kasus:** (a) 7 hari backup retention = cukup (insiden Rabu, masih dalam window 7 hari). RDS mendukung Point-in-Time Recovery (PITR) ke titik mana pun dalam retention window. (b) Proses PITR: `aws rds restore-db-instance-to-point-in-time` dengan target time = Selasa malam atau sebelum deployment Rabu pagi — restore ke instance terpisah (jangan timpa production!). (c) Risiko: waktu restore bisa 2–4 jam untuk database besar; data transaksi antara Rabu-Jumat hilang; validasi bahwa hasil restore benar membutuhkan waktu; jika ada data baru yang "benar" yang dibuat setelah bug (yang tidak corrupt), harus di-merge manual. Mitigasi: mulai restore segera Jumat malam; siapkan tim untuk validasi; komunikasikan ke bisnis bahwa ada downtime dan data gap. (d) Transaksi Rabu–Jumat: audit log dan application log bisa digunakan untuk merekonstruksi transaksi yang valid; transaksi yang corrupt perlu diidentifikasi dan di-reject; beberapa transaksi mungkin harus di-re-input manual; inform customer tentang status transaksi mereka; ini adalah proses yang intensif labor.

## 11. Ringkasan Bab

RTO dan RPO mendefinisikan requirement recovery; DR strategy (backup/restore, pilot light, warm standby, active-active) dipilih berdasarkan requirement dan budget. Immutable backup (S3 Object Lock COMPLIANCE mode) melindungi dari ransomware yang menyerang backup. Zero Trust relevan dalam resiliensi: microsegmentation membatasi blast radius; post-recovery re-verification memastikan bahwa infrastruktur yang pulih tidak masih dikompromis.

## 12. Refleksi Profesional

1. Backup testing (DR drill) adalah aktivitas yang sering dilewati karena "tidak ada waktu" atau "nanti kalau ada insiden baru dicoba." Namun DR yang tidak pernah ditest sama dengan tidak punya DR. Bagaimana Anda menyusun argumen bisnis dan teknis untuk menjadikan DR drill sebagai kegiatan regular (misalnya bulanan atau kuartalan)?


---

# BAB 12 — CAPSTONE FASE 1: SECURITY ARCHITECTURE DAN ASSET MAPPING

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Melakukan asset discovery dan inventarisasi lingkungan cloud/container
- Mengidentifikasi trust boundary dan attack surface dari arsitektur yang ada
- Menyusun threat model menggunakan metodologi STRIDE untuk sistem cloud
- Mendokumentasikan temuan dalam format yang dapat diaudit

*Berkaitan dengan Sub-CPMK-5, Eval-5/EAS (30%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Capstone Fase 1:\nSecurity Architecture Review] --> B[Asset Discovery]
    B --> B1["Cloud Resources:\nEC2, RDS, S3, Lambda,\nEKS Cluster"]
    B --> B2["Network Topology:\nVPC, Subnets, SG, NACL,\npeering, VPN"]
    B --> B3["Identity:\nIAM users, roles, policies,\nservice accounts"]
    B --> B4["Data Assets:\nklasifikasi: public/internal/\nconfidential/restricted"]
    A --> C[Architecture Review]
    C --> C1["Review terhadap CIS Benchmark"]
    C --> C2["Review terhadap NIST CSF"]
    C --> C3["Identifikasi trust boundaries"]
    C --> C4["Identifikasi attack surface"]
    A --> D[Threat Modelling]
    D --> D1["STRIDE per komponen:\nSpoofing, Tampering,\nRepudiation, Info Disc,\nDoS, Elevation of Privilege"]
    D --> D2["Risk rating:\nLikelihood × Impact"]
    D --> D3["Prioritisasi threats:\nHigh/Medium/Low"]
    A --> E[Documentation]
    E --> E1["Architecture diagram:\nstate yang ada (as-is)"]
    E --> E2["Asset inventory table"]
    E --> E3["Threat model matrix"]
    E --> E4["Gap analysis awal"]
```

## 3. Pengantar Kontekstual

Capstone proyek mensimulasikan skenario nyata: tim keamanan baru masuk dan harus melakukan security review menyeluruh terhadap lingkungan cloud yang sudah berjalan. Fase pertama adalah memahami apa yang ada, siapa yang dapat mengakses apa, dan di mana ancaman paling signifikan berada — sebelum merekomendasikan atau mengimplementasikan kontrol apa pun. Tanpa pemahaman yang solid tentang arsitektur dan asset, kontrol yang diimplementasikan akan tidak tepat sasaran.

## 4. Landasan Teori

### 4.1 Asset Discovery dan Klasifikasi

**Asset inventory untuk lingkungan cloud:**

```markdown
## Cloud Asset Inventory Template

### Compute Resources
| ID | Type | Region | OS/Runtime | Purpose | Owner | Data Classification |
|---|---|---|---|---|---|---|
| i-abc123 | EC2 t3.medium | ap-southeast-1a | Ubuntu 22.04 | Web server | team-web | Internal |
| eks-cluster-prod | EKS 1.27 | ap-southeast-1 | K8s | App orchestration | team-platform | Internal |

### Storage Resources
| ID | Type | Region | Encryption | Public? | Versioning | Data Classification |
|---|---|---|---|---|---|---|
| company-prod-data | S3 | ap-southeast-1 | SSE-S3 | No | Yes | Confidential |
| company-static-assets | S3 | ap-southeast-1 | None | Yes | No | Public |

### Network Resources
| Resource | CIDR/ID | AZ | Purpose | Notes |
|---|---|---|---|---|
| vpc-abc | 10.0.0.0/16 | all | Main VPC | |
| subnet-pub-1 | 10.0.1.0/24 | 1a | Public (Web) | NAT Gateway |
| subnet-priv-1 | 10.0.10.0/24 | 1a | Private (App) | Via NAT |

### IAM Assets
| Principal | Type | Policies Attached | Last Used | MFA? | Risk Level |
|---|---|---|---|---|---|
| admin-alice | IAM User | AdministratorAccess | 2025-10-01 | Yes | High |
| ci-deploy-role | IAM Role | Custom deploy policy | Daily | N/A (role) | Medium |
```

### 4.2 STRIDE Threat Modelling untuk Komponen Cloud

```markdown
## STRIDE Analysis: EKS Cluster Endpoint

Komponen: Kubernetes API Server (kube-apiserver)
Trust level: High — central control plane

| Threat Category | Threat | Mitigasi yang Ada | Gap |
|---|---|---|---|
| Spoofing | Attacker menyamar sebagai valid kubectl user | OIDC auth, client certs | Tidak ada MFA untuk kubectl |
| Tampering | Modifikasi manifest Pod secara unauthorized | RBAC, Admission Controller | Belum ada Kyverno/OPA |
| Repudiation | User menyangkal telah delete resource | Kubernetes Audit Log | Audit log belum aktif |
| Info Disclosure | API endpoint dapat diakses dari internet | Private endpoint | Endpoint masih public |
| DoS | Flood API server dengan requests | Rate limiting default | Tidak ada custom rate limit |
| EoP | Container breakout ke host | PSS Restricted | Sebagian pod masih Privileged |
```

### 4.3 Trust Boundary Mapping

Trust boundary adalah garis yang memisahkan area dengan tingkat kepercayaan berbeda. Setiap request yang melintas trust boundary harus divalidasi.

```mermaid
flowchart LR
    INTERNET["Internet\n(Trust: Zero)"] -->|"HTTPS/443"| WAF["WAF\n(Trust Boundary 1)"]
    WAF -->|"Filtered traffic"| ALB["ALB\n(Trust: Low)"]
    ALB -->|"Trust Boundary 2\n(auth required)"| WEB["Web Pods\nPublic Subnet"]
    WEB -->|"Trust Boundary 3\n(service token)"| APP["App Pods\nPrivate Subnet"]
    APP -->|"Trust Boundary 4\n(mTLS + auth)"| DB["RDS Database\nData Subnet"]
    
    subgraph CROSS_BOUNDARY["Setiap Boundary = Validasi Eksplisit"]
        note1["TB1: WAF rules block OWASP Top 10"]
        note2["TB2: JWT validation by ALB"]
        note3["TB3: NetworkPolicy + ServiceAccount RBAC"]
        note4["TB4: DB credentials from Secrets Manager + TLS"]
    end
```

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph PHASE1["Capstone Fase 1: Deliverable"]
        A1["1. Asset Inventory\n(complete spreadsheet)"]
        A2["2. Architecture Diagram\n(as-is current state)"]
        A3["3. Trust Boundary Map"]
        A4["4. STRIDE Threat Model\n(per komponen kritis)"]
        A5["5. Risk Matrix\n(likelihood × impact)"]
        A6["6. Gap Analysis Awal\n(kontrol yang ada vs yang seharusnya)"]
    end
    
    A1 --> A2 --> A3 --> A4 --> A5 --> A6
    
    subgraph INPUT["Input untuk Fase 1"]
        I1["RPS Lab Scenario:\ndesain cloud yang diberikan dosen"]
        I2["CIS Cloud Benchmark\nsebagai referensi"]
        I3["NIST CSF Framework\n(Identify function)"]
    end
    
    INPUT --> PHASE1
```

## 6. Contoh Terapan

**Scenario yang digunakan dalam Capstone:** Dosen menyediakan skenario fiktif "PT. CloudNusa" — perusahaan e-commerce dengan infrastruktur AWS yang terdiri dari: EKS cluster (5 nodes), RDS PostgreSQL, ElastiCache Redis, 3 S3 buckets, dan beberapa EC2 instances. Dokumen skenario berisi: diagram arsitektur awal, snippet IAM policy, security group rules, dan daftar misconfigurations yang disengaja. Mahasiswa bertugas melakukan security review terhadap skenario ini.

**Metodologi pendekatan:**
1. Baca semua dokumentasi skenario.
2. Buat asset inventory dari informasi yang tersedia.
3. Gambar ulang arsitektur dengan trust boundary yang jelas.
4. Lakukan STRIDE analysis untuk 3 komponen paling kritis.
5. Buat risk matrix.
6. Identifikasi gap utama yang perlu di-address di Fase 2.

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menghasilkan deliverable Fase 1 Capstone berdasarkan skenario yang diberikan.

**Aktivitas:** Mahasiswa bekerja secara individual atau dalam kelompok kecil (sesuai petunjuk dosen) menggunakan skenario "PT. CloudNusa." Output yang dinilai:
- Kelengkapan asset inventory
- Akurasi arsitektur diagram dan trust boundary
- Kedalaman STRIDE analysis
- Ketepatan risk rating dan prioritisasi
- Kualitas gap analysis

**Catatan etika:** Semua analisis dilakukan terhadap skenario fiktif yang disediakan dosen — bukan terhadap infrastruktur nyata pihak ketiga.

## 8. Latihan Pemahaman

1. **(C4)** Mengapa asset discovery harus mendahului threat modelling? Apa risiko melakukan threat modelling tanpa inventory asset yang lengkap?

2. **(C3)** Apa perbedaan antara "attack surface" dan "threat"? Berikan contoh untuk masing-masing dalam konteks Kubernetes cluster.

## 9. Latihan Terapan / Studi Kasus

Anda menemukan bahwa dalam skenario "PT. CloudNusa," IAM user untuk developer memiliki `AdministratorAccess` policy. Lakukan mini-STRIDE analysis untuk komponen IAM ini: (a) Identifikasi minimal 4 threats berbeda (dari kategori STRIDE yang berbeda); (b) Untuk setiap threat, berikan: likelihood, impact, risk level, dan rekomendasi mitigasi; (c) Tulis justifikasi mengapa IAM adalah komponen paling kritikal untuk di-address di Fase 2.

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Asset discovery mendahului threat modelling karena: threat modelling memerlukan pemahaman tentang apa yang dilindungi dan dari siapa. Tanpa inventory yang lengkap: (a) ada aset yang terlewat dari analisis dan menjadi blind spot; (b) threat model yang dibuat tidak akurat karena tidak tahu topology dan trust boundaries yang sebenarnya; (c) prioritisasi tidak tepat karena tidak tahu data apa yang ada di setiap komponen; (d) rekomendasi mungkin tidak applicable karena tidak memahami arsitektur yang sesungguhnya.

**Soal 2:** Attack surface = semua titik di mana sistem dapat diakses atau diinteraksikan (baik secara legitimate maupun tidak). Threat = aksi spesifik oleh threat actor yang mengeksploitasi attack surface. Contoh K8s: Attack surface = kube-apiserver port 6443 yang accessible dari internet; Threat = Spoofing: attacker menggunakan credential yang di-phish untuk authenticate ke API server.

**Studi Kasus IAM AdministratorAccess:** (a) Threats: Spoofing — attacker yang mencuri session token developer dapat menyamar sebagai developer dan memiliki full admin access; Tampering — developer dengan AdministratorAccess dapat memodifikasi IAM policies, security groups, atau bahkan menghapus audit logs; Info Disclosure — developer dapat membaca seluruh secret di Secrets Manager, konten semua S3 bucket, database credentials; EoP — developer yang awalnya hanya memiliki akses ke satu service kini dapat escalate ke seluruh account karena AdministratorAccess memungkinkan `iam:*` dan `sts:AssumeRole`. (b) Risk rating: semuanya High likelihood × High impact = Critical. (c) Justifikasi: IAM adalah "master key" dari seluruh AWS account — compromise pada identity adalah compromise pada semua layer keamanan lainnya; network controls, encryption, dan monitoring semuanya dapat dibypass oleh principal dengan AdministratorAccess.

## 11. Ringkasan Bab

Fase 1 Capstone adalah fondasi dari seluruh security assessment: tanpa pemahaman arsitektur yang akurat, kontrol yang diimplementasikan di Fase 2 tidak akan tepat sasaran. Asset inventory yang lengkap, trust boundary yang jelas, dan STRIDE threat model yang sistematis menghasilkan risk matrix yang menjadi dasar prioritisasi perbaikan.

## 12. Refleksi Profesional

1. Dalam engagement security review nyata, klien sering memberikan informasi yang tidak lengkap atau tidak akurat tentang infrastruktur mereka ("seharusnya begini" vs "kenyataannya begini"). Bagaimana Anda memvalidasi bahwa dokumentasi yang diberikan mencerminkan keadaan yang sebenarnya? Tools atau teknik apa yang Anda gunakan untuk cloud infrastructure discovery?

---

# BAB 13 — CAPSTONE FASE 2: IMPLEMENTASI KONTROL DAN VALIDASI

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Memilih dan memprioritasikan kontrol keamanan berdasarkan risk matrix dari Fase 1
- Mengimplementasikan kontrol dalam bentuk konfigurasi atau kode (IaC, RBAC, policy)
- Memvalidasi efektivitas kontrol yang diimplementasikan
- Mendokumentasikan evidence implementasi

*Berkaitan dengan Sub-CPMK-5, Eval-5/EAS (30%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Capstone Fase 2:\nControl Implementation] --> B[Prioritisasi Kontrol]
    B --> B1["Dari risk matrix Fase 1:\naddress Critical dan High dulu"]
    B --> B2["Quick wins:\nlow effort, high impact"]
    B --> B3["Sequencing:\nkontrol yang saling bergantung"]
    A --> C[Implementation Categories]
    C --> C1["IAM Remediation:\nKurangi privilege, enable MFA,\ncreate role per workload"]
    C --> C2["Network Hardening:\nNetworkPolicy default-deny,\nSG refinement, WAF rules"]
    C --> C3["Workload Security:\nPSS enforce, Kyverno policy,\nimage signing"]
    C --> C4["Logging & Detection:\naktifkan audit log, Falco,\nCloudTrail → SIEM"]
    A --> D[Validation]
    D --> D1["Functional test:\napakah kontrol bekerja sebagaimana dimaksud?"]
    D --> D2["Negative test:\napakah blocked traffic benar-benar blocked?"]
    D --> D3["Evidence collection:\nscreenshot, log, command output"]
    A --> E[Evidence Pack]
    E --> E1["Setiap kontrol: before/after"]
    E --> E2["Hash evidence files"]
    E --> E3["Timeline implementasi"]
```

## 3. Pengantar Kontekstual

Implementasi kontrol keamanan tanpa validasi adalah security theater — kita tidak tahu apakah kontrol benar-benar bekerja sampai diuji. Fase 2 Capstone menekankan: setiap kontrol yang diimplementasikan harus divalidasi dengan bukti yang dapat diaudit. Ini mencerminkan praktik nyata di mana auditor atau regulator akan meminta evidence bahwa kontrol yang diklaim benar-benar efektif.

## 4. Landasan Teori

### 4.1 Control Selection Framework

Pemilihan kontrol berdasarkan NIST CSF Functions:

```markdown
## Control Selection Matrix

### Prioritas 1 — Critical Risk (implement dalam 48 jam pertama)
| Risk | Kontrol | Framework Reference | Effort |
|---|---|---|---|
| IAM AdministratorAccess untuk developer | Replace dengan role-based least privilege | CIS AWS 1.16, NIST CSF PR.AC-6 | Medium |
| K8s API server public | Enable private endpoint, restrict public | CIS EKS 3.2.1 | Low |
| Audit logging tidak aktif | Enable CloudTrail all-regions, K8s audit | CIS AWS 3.1, NIST CSF DE.CM-1 | Low |

### Prioritas 2 — High Risk (implement dalam 1 minggu)
| Risk | Kontrol | Framework Reference | Effort |
|---|---|---|---|
| Tidak ada NetworkPolicy | Default-deny + whitelist per service | NIST CSF PR.AC-5 | Medium |
| Pod berjalan sebagai root | PSS Restricted enforcement per namespace | CIS EKS 5.2.6 | Medium |
| Image tanpa signing | Cosign + Kyverno verification | NIST SSDF | High |
```

### 4.2 Implementasi dan Validasi — Pola Before/After

```bash
# KONTROL: Restrict kube-apiserver public access
# 
# BEFORE: Verifikasi kondisi awal
kubectl get endpoints kubernetes
# kubernetes   10.100.0.1:443   7d

# Jika cluster menggunakan EKS, cek public endpoint:
aws eks describe-cluster --name production-cluster \
    --query 'cluster.resourcesVpcConfig.endpointPublicAccess'
# true  <-- ini yang akan kita ubah

# IMPLEMENTASI
aws eks update-cluster-config \
    --name production-cluster \
    --resources-vpc-config endpointPublicAccess=false,endpointPrivateAccess=true

# AFTER: Validasi perubahan berhasil
aws eks describe-cluster --name production-cluster \
    --query 'cluster.resourcesVpcConfig'
# {
#   "endpointPublicAccess": false,  <-- berhasil!
#   "endpointPrivateAccess": true
# }

# NEGATIVE TEST: Dari luar VPC, kubectl seharusnya gagal
kubectl get nodes
# E0101 error: couldn't get current server API group list:
# dial tcp: connection refused  <-- BAIK! public access berhasil di-block
```

### 4.3 Evidence Collection untuk Audit

Setiap kontrol yang diimplementasikan harus memiliki evidence pack:

```markdown
## Evidence Pack Template — Per Kontrol

### Kontrol ID: CTL-001
**Deskripsi:** Disable EKS API Server public endpoint
**Framework:** CIS EKS Benchmark v1.4, Check 3.2.1
**Risk yang di-address:** Info Disclosure, EoP (dari STRIDE Fase 1)

**Pre-implementation state:**
- Screenshot/command output yang membuktikan kondisi sebelumnya
- Tanggal/waktu pengambilan evidence
- SHA256 hash file evidence

**Implementasi:**
- Command/konfigurasi yang digunakan (verbatim)
- Waktu implementasi
- Siapa yang mengimplementasikan

**Post-implementation validation:**
- Command output yang membuktikan perubahan berhasil
- Negative test result (blocked traffic)
- Waktu validasi

**Residual risk:**
- Apakah kontrol ini fully mitigates risk, atau ada residual risk?
```

## 5. Model atau Arsitektur

```mermaid
flowchart LR
    subgraph FASE1_OUTPUT["Output Fase 1"]
        RISK["Risk Matrix\n(Critical/High/Medium/Low)"]
    end
    
    subgraph FASE2["Fase 2: Implementasi Terstruktur"]
        SEL["Control Selection\n(prioritas berdasarkan risk)"]
        PLAN["Implementation Plan\n(sequence, dependencies, effort)"]
        IMPL["Implementasi\n(IaC, RBAC, policy config)"]
        VAL["Validasi\n(functional + negative test)"]
        EVID["Evidence Collection\n(before/after, hash)"]
        RETEST["Re-assessment\n(risk matrix update)"]
    end
    
    RISK --> SEL --> PLAN --> IMPL --> VAL --> EVID --> RETEST
```

## 6. Contoh Terapan

**Implementasi Kyverno policy untuk skenario PT. CloudNusa:**

```bash
# Verifikasi tidak ada Kyverno terinstall (before state)
kubectl get pods -n kyverno 2>&1
# Error from server (NotFound): namespaces "kyverno" not found

# Install Kyverno (dalam lab cluster)
kubectl create -f https://github.com/kyverno/kyverno/releases/download/v1.11.0/install.yaml

# Apply policy: larang container running as root
cat <<'EOF' | kubectl apply -f -
apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: disallow-root-user
spec:
  validationFailureAction: Enforce
  rules:
  - name: check-runAsNonRoot
    match:
      any:
      - resources:
          kinds: ["Pod"]
    validate:
      message: "Container tidak boleh berjalan sebagai root (runAsNonRoot: true diperlukan)"
      pattern:
        spec:
          containers:
          - securityContext:
              runAsNonRoot: true
EOF

# Validasi: coba deploy Pod yang run as root
cat <<'EOF' | kubectl apply -f - 2>&1
apiVersion: v1
kind: Pod
metadata:
  name: test-root-pod
  namespace: default
spec:
  containers:
  - name: test
    image: alpine:3.18
    securityContext:
      runAsUser: 0  # root!
EOF
# Error from server: admission webhook "validate.kyverno.svc-fail" denied the request:
# Container tidak boleh berjalan sebagai root (runAsNonRoot: true diperlukan)
# <-- BERHASIL! Policy berfungsi.

# Kumpulkan evidence: timestamp, screenshot output, policy YAML
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Mengimplementasikan minimal 5 kontrol dari risk matrix Fase 1 dan mendokumentasikan evidence.

**Aktivitas (dalam lab Minikube/Kind yang diotorisasi):**
1. Pilih 5 kontrol dari risk matrix berdasarkan prioritas.
2. Untuk setiap kontrol: dokumentasikan before state, implementasikan, validasi, dokumentasikan after state.
3. Buat evidence pack yang terstruktur.
4. Update risk matrix untuk mencerminkan risk yang sudah di-mitigasi.
5. Identifikasi residual risk.

**Output:** Evidence pack implementasi kontrol — bagian dari Eval-5/EAS.

## 8. Latihan Pemahaman

1. **(C5)** Apa perbedaan antara "functional test" dan "negative test" untuk validasi kontrol keamanan? Mengapa negative test sama pentingnya?

2. **(C4)** Mengapa evidence harus di-hash (SHA-256)? Apa yang dibuktikan oleh hash dari file evidence?

## 9. Latihan Terapan / Studi Kasus

Setelah implementasi NetworkPolicy default-deny di namespace `production`, tim developer melaporkan bahwa beberapa service tidak dapat berkomunikasi satu sama lain. (a) Jelaskan mengapa hal ini terjadi secara teknis. (b) Apa prosedur troubleshooting yang benar — bagaimana Anda mendiagnosis service mana yang terdampak tanpa melemahkan posture keamanan? (c) Bagaimana Anda memperbaikinya dengan tetap mempertahankan default-deny? (d) Apa yang harus didokumentasikan dari insiden ini?

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Functional test memverifikasi bahwa kontrol bekerja sesuai maksud (misalnya: NetworkPolicy diapply, Pod yang authorized bisa berkomunikasi). Negative test memverifikasi bahwa kontrol memblokir apa yang seharusnya diblokir (misalnya: Pod yang tidak authorized tidak bisa berkomunikasi). Negative test sama pentingnya karena: kontrol keamanan yang salah konfigurasi mungkin lolos functional test (karena dia tidak menolak traffic yang seharusnya diizinkan) namun gagal menjadi security control yang efektif (karena dia juga tidak menolak traffic yang seharusnya di-block); hanya dengan negative test kita membuktikan bahwa kontrol benar-benar memblokir.

**Soal 2:** Hash SHA-256 dari file evidence membuktikan bahwa file tersebut tidak dimodifikasi sejak hash dibuat. Dalam konteks audit atau legal: hash membuktikan integrity evidence; jika hash yang disimpan (di tempat terpisah) cocok dengan hash file yang ada, file tersebut otentik dan tidak dimanipulasi. Ini relevan karena auditor atau pengadilan dapat mempertanyakan apakah evidence telah dimanipulasi untuk mendukung kesimpulan tertentu.

**Studi Kasus NetworkPolicy:** (a) Default-deny NetworkPolicy memblokir SEMUA traffic ingress dan egress di namespace, termasuk yang sebelumnya berfungsi. Sebelum default-deny, komunikasi antar Pod berfungsi karena tidak ada pembatasan. Setelah default-deny, setiap komunikasi antar Pod harus secara eksplisit diizinkan. (b) Troubleshooting tanpa melemahkan posture: `kubectl logs` dari Pod yang gagal untuk lihat error; `kubectl describe networkpolicy -n production` untuk review semua policy; uji konektivitas dari Pod secara targeted: `kubectl exec -n production <pod> -- nc -zv <target-service> <port>`; jangan langsung ubah policy — identifikasi dulu semua dependency yang ada. (c) Perbaikan: buat NetworkPolicy yang explicitly mengizinkan traffic yang diperlukan (seperti yang ditunjukkan di Bab 8); gunakan pendekatan whitelist dari documentation arsitektur yang ada dan komunikasi dengan developer tentang service dependencies. (d) Dokumentasikan: waktu policy diapply; service yang terdampak dan berapa lama; root cause (komunikasi implicit yang tidak terdokumentasi); NetworkPolicy yang ditambahkan sebagai fix; lesson learned: komunikasi dengan developer tim sebelum apply default-deny policy.

## 11. Ringkasan Bab

Fase 2 Capstone menterjemahkan risk matrix menjadi tindakan nyata: select kontrol berdasarkan prioritas, implementasikan, dan validasi dengan functional + negative test. Evidence pack yang tersusun rapi dengan before/after state dan hash file adalah deliverable yang dapat diaudit. Residual risk yang tersisa harus didokumentasikan secara transparan.

## 12. Refleksi Profesional

1. Dalam skenario nyata, implementasi beberapa kontrol (seperti default-deny NetworkPolicy) dapat menyebabkan disruption pada sistem yang berjalan. Bagaimana Anda menyeimbangkan urgensi untuk mengimplementasikan kontrol dengan kebutuhan untuk tidak mengganggu operasional bisnis? Apakah ada urutan implementasi yang lebih "aman"?

---

# BAB 14 — CAPSTONE FASE 3: LAPORAN, EVIDENCE PACK, DAN REKOMENDASI

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa mampu:
- Menyusun laporan keamanan cloud yang komprehensif dan dapat diaudit
- Mengorganisasikan evidence pack yang membuktikan temuan dan implementasi
- Menyampaikan rekomendasi yang actionable dan berbasis risiko
- Memahami standar komunikasi keamanan kepada audience teknis dan manajemen

*Berkaitan dengan Sub-CPMK-5, Eval-5/EAS (30%)*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Capstone Fase 3:\nReporting] --> B[Report Structure]
    B --> B1["Executive Summary:\nnon-teknis, risk-based,\nbusiness impact"]
    B --> B2["Technical Findings:\ndetail per temuan,\nevidence, CVSS-like rating"]
    B --> B3["Implemented Controls:\nbefore/after, evidence pack"]
    B --> B4["Residual Risk:\napa yang belum teratasi"]
    B --> B5["Recommendations:\nprioritized roadmap"]
    A --> C[Evidence Pack]
    C --> C1["Organized per kontrol:\nC001, C002, ..."]
    C --> C2["Hash manifest:\nSHA256 semua file evidence"]
    C --> C3["Timeline lengkap:\nkapan setiap action dilakukan"]
    A --> D[Quality Criteria]
    D --> D1["Reproducible:\norang lain bisa verifikasi temuan"]
    D --> D2["Accurate:\ntemuan didukung evidence"]
    D --> D3["Actionable:\nrekomendasi bisa diimplementasikan"]
    D --> D4["Proportional:\nrating risk sesuai konteks"]
```

## 3. Pengantar Kontekstual

Laporan keamanan adalah output utama dari pekerjaan security assessment. Temuan teknis yang brilian tidak berguna jika tidak dikomunikasikan dengan baik — kepada auditor yang membutuhkan evidence, kepada developer yang akan melakukan perbaikan, atau kepada manajemen yang mengambil keputusan anggaran. Fase 3 mensintesis semua pekerjaan dari Fase 1 dan 2 menjadi dokumen yang dapat digunakan.

## 4. Landasan Teori

### 4.1 Struktur Laporan Security Assessment Cloud

```markdown
# Security Assessment Report: PT. CloudNusa AWS Environment
**Klasifikasi:** Confidential — Internal Use Only
**Tanggal:** [Tanggal laporan]
**Versi:** 1.0
**Assessor:** [Nama / Tim]

---

## 1. Executive Summary

Penilaian keamanan terhadap lingkungan AWS PT. CloudNusa dilaksanakan pada
[periode]. Tujuan penilaian adalah mengidentifikasi risiko keamanan pada
infrastruktur cloud dan Kubernetes cluster, serta memvalidasi implementasi kontrol.

**Ringkasan Risiko:**
| Level | Jumlah Temuan | Sudah Dimitigasi | Residual |
|---|---|---|---|
| Critical | 2 | 2 | 0 |
| High | 5 | 3 | 2 |
| Medium | 8 | 4 | 4 |
| Low | 6 | 2 | 4 |

**Business Impact (jika tidak di-address):** [1-2 paragraf tentang dampak bisnis,
bukan teknis — sesuai audience manajemen]

---

## 2. Metodologi

- Fase 1: Asset discovery, architecture review, threat modelling (STRIDE)
- Fase 2: Control implementation dan validasi
- Framework referensi: CIS AWS Benchmark v1.5, CIS EKS Benchmark v1.4,
  NIST SP 800-190, NIST CSF

---

## 3. Technical Findings

### Finding-001: IAM AdministratorAccess untuk Developer Accounts
**Severity:** Critical
**CVSS-equivalent:** 9.1 (AV:N/AC:L/PR:L/UI:N/S:C/C:H/I:H/A:H)
**Status:** Remediated

**Deskripsi:** [Teknis detail]
**Evidence:** File: evidence/F001-iam-admin-before.txt (SHA256: abc123...)
**Remediation:** [Apa yang dilakukan]
**Validation:** File: evidence/F001-iam-admin-after.txt (SHA256: def456...)
**Residual Risk:** [Jika ada]

---

## 4. Residual Risk Register

[Temuan yang belum dimitigasi, dengan justifikasi dan rencana]

---

## 5. Recommendations Roadmap

### Immediate (0–30 hari):
1. [Rekomendasi 1] — Priority: Critical

### Short-term (30–90 hari):
1. [Rekomendasi 2] — Priority: High

### Long-term (90+ hari):
1. [Rekomendasi 3] — Priority: Medium / Strategic
```

### 4.2 Evidence Pack Organization

```bash
# Struktur direktori evidence pack
capstone-evidence/
├── README.md                 # Deskripsi setiap file
├── HASH_MANIFEST.txt         # SHA256 dari semua file
├── phase1/
│   ├── asset-inventory.xlsx
│   ├── architecture-diagram.png
│   ├── threat-model-stride.xlsx
│   └── risk-matrix-initial.xlsx
├── phase2/
│   ├── C001-iam-remediation/
│   │   ├── before-state.txt
│   │   ├── implementation-commands.sh
│   │   ├── after-state.txt
│   │   └── negative-test-result.txt
│   ├── C002-network-policy/
│   │   ├── before-state.txt
│   │   ├── networkpolicy-applied.yaml
│   │   ├── after-state-positive.txt
│   │   └── after-state-negative.txt
│   └── [C003-C00N]...
└── phase3/
    ├── final-report.pdf
    └── risk-matrix-updated.xlsx

# Buat hash manifest:
find capstone-evidence/ -type f -exec sha256sum {} \; > HASH_MANIFEST.txt
# Simpan HASH_MANIFEST.txt di tempat yang berbeda dari evidence
# Ini membuktikan bahwa file tidak dimodifikasi sejak assessment selesai
```

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph SYNTHESIS["Fase 3: Sintesis"]
        F1_OUT["Output Fase 1:\nAsset Inventory,\nRisk Matrix,\nThreat Model"]
        F2_OUT["Output Fase 2:\nEvidence Pack\n(before/after),\nUpdated Risk Matrix"]
        
        F1_OUT & F2_OUT --> REPORT["Final Report"]
        
        REPORT --> EXEC["Executive Summary\n(C-Level, non-teknis)"]
        REPORT --> TECH["Technical Findings\n(security team, developer)"]
        REPORT --> ROADMAP["Remediation Roadmap\n(project manager, CISO)"]
        REPORT --> EVID_PACK["Evidence Pack\n(auditor, regulator)"]
    end
```

## 6. Contoh Terapan

**Komunikasi temuan kepada manajemen:**

```markdown
## Untuk: Direktur Teknologi PT. CloudNusa
## Dari: Tim Keamanan Siber
## Hal: Ringkasan Risiko Kritis — Perlu Persetujuan Tindakan Segera

Bapak/Ibu,

Kami telah menyelesaikan penilaian keamanan lingkungan cloud AWS perusahaan.
Ditemukan 2 risiko dengan tingkat KRITIS yang memerlukan perhatian segera:

**Risiko 1: Akses Admin Tanpa Batas untuk 5 Akun Developer**
Dampak Bisnis: Jika satu akun developer dikompromis (misalnya melalui phishing),
penyerang dapat menghapus seluruh infrastruktur, mengakses data pelanggan, atau
menyebarkan ransomware ke seluruh environment.
Estimasi Biaya Insiden: [berdasarkan data industri] Rp 2–10 miliar untuk recovery
dan reputational damage.
Biaya Perbaikan: < 2 hari kerja, tanpa biaya lisensi tambahan.
Status: Siap diimplementasikan — menunggu persetujuan.

Diperlukan: Persetujuan untuk melanjutkan implementasi dalam 48 jam ke depan.
```

## 7. Praktikum atau Aktivitas Terarah

**Tujuan:** Menghasilkan laporan Capstone final yang lengkap.

**Aktivitas:** Sintesiskan semua output Fase 1 dan 2 menjadi:
1. Final report (sesuai template).
2. Evidence pack yang terorganisir dengan hash manifest.
3. Presentasi executive summary (5 menit) kepada "panel manajemen" (dosen/panel reviewer).

**Output:** Laporan final + evidence pack — ini adalah deliverable utama EAS.

## 8. Latihan Pemahaman

1. **(C5)** Mengapa laporan keamanan untuk manajemen dan untuk tim teknis harus berbeda dalam bahasa dan fokus? Apa yang salah jika Anda memberikan laporan teknis lengkap kepada manajemen?

2. **(C4)** Apa yang dimaksud dengan "residual risk" dalam konteks security assessment? Mengapa penting untuk mendokumentasikannya secara eksplisit daripada hanya mendokumentasikan temuan yang sudah di-remediated?

## 9. Latihan Terapan / Studi Kasus

Anda menemukan bahwa S3 bucket yang berisi data backup PostgreSQL memiliki public access diaktifkan. Backup terakhir berisi nama, email, dan nomor telepon seluruh customer (500.000 records). Bucket sudah ada selama 6 bulan. (a) Bagaimana Anda menentukan apakah data sudah pernah diakses secara tidak sah? (b) Tulis "finding" untuk laporan teknis (1 paragraph). (c) Tulis "ringkasan risiko" untuk manajemen dalam bahasa non-teknis (1 paragraph). (d) Apa kewajiban legal organisasi di Indonesia berdasarkan UU PDP No. 27/2022 jika terbukti ada akses tidak sah?

## 10. Kunci Jawaban dan Pembahasan

**Soal 1:** Manajemen memerlukan informasi yang terkait dengan dampak bisnis, biaya, dan keputusan investasi — bukan detail teknis seperti CVE IDs atau kubectl commands. Laporan teknis lengkap kepada manajemen: (a) terlalu detail sehingga tidak efektif dalam komunikasi risiko; (b) fokus pada "apa yang ditemukan" bukan "mengapa ini penting bagi bisnis"; (c) dapat menyebabkan keputusan yang salah karena manajemen mungkin misinterpret severity tanpa konteks bisnis; (d) laporan teknis juga mengandung informasi yang bisa menjadi "roadmap" bagi attacker jika bocor — distribusinya perlu dibatasi.

**Soal 2:** Residual risk = risiko yang tersisa setelah kontrol diimplementasikan. Penting didokumentasikan karena: (a) tidak ada kontrol yang perfect — setiap kontrol memiliki batas dan kemungkinan bypass; (b) manajemen atau auditor harus tahu risiko apa yang masih ada agar bisa membuat keputusan yang informed (misalnya: "apakah residual risk ini acceptable atau perlu tambahan kontrol?"); (c) dari perspektif accountability: mendokumentasikan residual risk membuktikan bahwa assessor jujur dan tidak menyembunyikan kelemahan; (d) residual risk menjadi input untuk siklus assessment berikutnya.

**Studi Kasus S3 Public Bucket:** (a) Cara menentukan akses tidak sah: aktifkan S3 server access logging (jika sudah aktif, review log); cek AWS CloudTrail untuk GetObject events pada bucket tersebut selama 6 bulan ke belakang; analisis: apakah ada GetObject dari IP di luar network organisasi? Apakah ada akses di waktu yang tidak biasa? Volume akses yang tidak wajar? (b) Technical finding: "S3 bucket 'company-backup-prod' telah dikonfigurasi dengan public access selama estimasi 6 bulan. Bucket berisi backup database PostgreSQL yang mengandung PII 500.000 customer (nama, email, nomor telepon). S3 access log dan CloudTrail menunjukkan [X] akses dari IP eksternal selama periode tersebut. Risk: CRITICAL. Potensi data breach regulatori." (c) Manajemen: "Kami menemukan bahwa file backup yang berisi data pribadi 500.000 pelanggan dapat diakses oleh siapa saja melalui internet tanpa kata sandi selama kurang lebih 6 bulan. Situasi ini perlu ditangani segera untuk menentukan apakah data pelanggan telah diakses secara tidak sah, dan untuk memenuhi kewajiban hukum yang berlaku." (d) Kewajiban UU PDP No. 27/2022: Pasal 46 — kewajiban notifikasi kepada Menkominfo dan subjek data dalam waktu 14 hari setelah mengetahui adanya kebocoran data; harus dilampirkan informasi tentang data yang bocor, dampak yang mungkin terjadi, dan langkah penanganan; kegagalan notifikasi dapat berimplikasi sanksi administratif.

## 11. Ringkasan Bab

Laporan security assessment yang efektif memiliki tiga lapisan: executive summary berbasis dampak bisnis, technical findings dengan evidence yang verifiable, dan recommendations roadmap yang prioritized. Evidence pack yang terorganisasi dengan hash manifest membuktikan integritas assessment. Residual risk harus didokumentasikan secara transparan. Komunikasi kepada manajemen menggunakan bahasa bisnis, bukan bahasa teknis.

## 12. Refleksi Profesional

1. Laporan security assessment mengandung informasi yang sangat sensitif — daftar kerentanan dan bagaimana cara mengeksploitasinya. Bagaimana Anda memastikan laporan ini hanya sampai ke pihak yang berwenang? Apa prosedur yang Anda rekomendasikan untuk distribusi, penyimpanan, dan akhirnya penghapusan laporan assessment?


---

# BAB 15 — PENGAYAAN: CLOUD SOC, CNAPP, DAN RUNTIME DETECTION

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa memahami:
- Peran Cloud Security Operations Center (Cloud SOC) dan bedanya dari SOC tradisional
- Konsep CNAPP (Cloud-Native Application Protection Platform)
- Postur CSPM dan perlindungan workload CWPP
- Runtime detection dan respons dalam lingkungan cloud/container

*Bab Pengayaan — materi referensi dan wawasan industri*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud SOC Landscape] --> B[Detection Stack]
    B --> B1["CSPM: Cloud Security\nPosture Management\n— konfigurasi, compliance"]
    B --> B2["CWPP: Cloud Workload\nProtection Platform\n— runtime, VM/container/serverless"]
    B --> B3["CIEM: Cloud Infrastructure\nEntitlement Management\n— IAM analysis, over-privilege"]
    B --> B4["CNAPP: gabungan\nCSPM + CWPP + CIEM\ndi satu platform"]
    A --> C[Tools Kategori]
    C --> C1["Open Source:\nFalco (runtime),\nTrivy (scan),\nkube-bench (CIS)"]
    C --> C2["Cloud Native:\nAWS GuardDuty,\nAzure Defender for Cloud,\nGCP Security Command Center"]
    C --> C3["Commercial CNAPP:\nWiz, Orca, Prisma Cloud,\nLacework, Aqua Security"]
    A --> D[Cloud SOC Workflow]
    D --> D1["Alert ingestion:\nGuardDuty/CNAPP → SIEM"]
    D --> D2["Triage:\nfalse positive filter,\ncontextual enrichment"]
    D --> D3["Investigation:\ncloud-native IR tools"]
    D --> D4["Remediation:\nautomated playbook / manual IR"]
```

## 3. Pengantar Kontekstual

Seiring organisasi bermigrasi ke cloud, SOC tradisional yang fokus pada firewall logs dan endpoint EDR tidak cukup. Cloud environments menghasilkan jenis telemetri yang berbeda — API calls, resource configuration changes, container runtime events — yang memerlukan tooling dan skill yang berbeda. Cloud SOC dan CNAPP muncul sebagai respons terhadap kebutuhan ini.

## 4. Landasan Teori

### 4.1 CSPM vs CWPP vs CIEM

**CSPM (Cloud Security Posture Management):**
- Fokus: apakah konfigurasi cloud resource sudah sesuai standar?
- Contoh pertanyaan: "Apakah S3 bucket ini public? Apakah CloudTrail aktif? Apakah semua RDS encrypted?"
- Bekerja pada data konfigurasi, bukan traffic
- Deteksi: misconfiguration, compliance gap, benchmark drift

**CWPP (Cloud Workload Protection Platform):**
- Fokus: apa yang terjadi pada workload saat runtime?
- Contoh pertanyaan: "Apakah ada proses anomali berjalan dalam container ini? Apakah ada koneksi jaringan yang tidak biasa?"
- Bekerja pada runtime events (syscalls, network, process)
- Deteksi: malware, exploit, anomaly behavior, container escape

**CIEM (Cloud Infrastructure Entitlement Management):**
- Fokus: siapa yang bisa melakukan apa di cloud?
- Contoh pertanyaan: "IAM role ini memiliki S3:* permission, tapi hanya pernah menggunakan S3:GetObject — apakah permission lain bisa di-remove?"
- Bekerja pada IAM policy analysis dan usage data
- Deteksi: over-privileged accounts, unused permissions, toxic combinations

**CNAPP** = CSPM + CWPP + CIEM dalam satu platform — memberikan visibility end-to-end dari konfigurasi hingga runtime.

### 4.2 AWS GuardDuty sebagai Cloud-Native Threat Detection

AWS GuardDuty adalah layanan managed threat detection yang menganalisis CloudTrail, VPC Flow Logs, dan DNS logs secara otomatis menggunakan ML dan threat intelligence:

```json
// Contoh GuardDuty finding
{
  "type": "UnauthorizedAccess:IAMUser/ConsoleLoginSuccess.B",
  "severity": 7.0,
  "title": "API GenerateDataKey was invoked from a known Tor exit node",
  "description": "API activity has been identified using credentials belonging to 
                   user alice@company.com from known Tor IP 198.51.100.5",
  "detail": {
    "userType": "IAMUser",
    "userName": "alice",
    "eventSource": "kms.amazonaws.com",
    "eventName": "GenerateDataKey",
    "sourceIPAddress": "198.51.100.5",
    "country": "Tor Node"
  }
}
```

Kategori GuardDuty findings yang relevan untuk Cloud SOC:
- `CryptoCurrency:EC2/BitcoinTool` — EC2 melakukan mining crypto
- `Backdoor:EC2/C&CActivity` — EC2 berkomunikasi dengan C&C server
- `Exfiltration:S3/AnomalousBehavior` — S3 access yang tidak normal
- `CredentialAccess:IAMUser/AnomalousBehavior` — penggunaan IAM yang mencurigakan
- `Impact:S3/AnomalousBehavior` — S3 delete yang tidak biasa (ransomware?)

### 4.3 Container Runtime Incident Response

```bash
# Ketika Falco alert terdeteksi (shell spawned dalam container):
# Tindakan yang diotorisasi dalam environment yang berotorisasi:

# 1. Identify container yang bermasalah
kubectl get pods -A | grep <suspicious-pod-name>

# 2. Preserve state sebelum kill (forensic readiness)
kubectl describe pod <pod-name> -n <namespace> > pod-forensic-state.txt
kubectl get pod <pod-name> -n <namespace> -o yaml >> pod-forensic-state.txt

# 3. Ambil logs sebelum container dimatikan
kubectl logs <pod-name> -n <namespace> --previous > pod-logs.txt 2>&1 || true
kubectl logs <pod-name> -n <namespace> > pod-logs-current.txt 2>&1

# 4. Scale down deployment untuk isolasi (tapi jangan delete dulu)
kubectl scale deployment <deployment-name> -n <namespace> --replicas=0

# 5. Investigasi: apa yang terjadi?
# Review Falco alerts, K8s audit log, dan aplikasi logs
# Identifikasi: kapan, siapa/apa yang memicu, apa yang dilakukan

# 6. Remediation: patch, redeploy dari clean image
# 7. Incident report
```

## 5. Model atau Arsitektur

```mermaid
flowchart TD
    subgraph CLOUD_ENV["Cloud/Container Environment"]
        CONFIG["Resource Configs\n(IAM, S3, SG, ...)"]
        RUNTIME["Runtime Events\n(syscalls, network, process)"]
        IAM_USAGE["IAM Usage Data\n(who used what permission)"]
    end
    
    subgraph CNAPP["CNAPP Platform"]
        CSPM_MOD["CSPM Module\n(config analysis)"]
        CWPP_MOD["CWPP Module\n(runtime protection)"]
        CIEM_MOD["CIEM Module\n(entitlement analysis)"]
        CORRELATION["Risk Correlation Engine:\ngabungkan data lintas modul"]
    end
    
    CONFIG --> CSPM_MOD
    RUNTIME --> CWPP_MOD
    IAM_USAGE --> CIEM_MOD
    
    CSPM_MOD & CWPP_MOD & CIEM_MOD --> CORRELATION
    
    CORRELATION --> SIEM_CLOUD["Cloud SIEM\n(prioritized alerts)"]
    SIEM_CLOUD --> SOC_ANALYST["Cloud SOC Analyst:\ntriage + investigate + respond"]
```

## 6. Latihan Pemahaman

1. **(C4)** Jelaskan mengapa CNAPP lebih efektif daripada menggunakan CSPM dan CWPP secara terpisah dan tidak terintegrasi. Berikan contoh konkret di mana correlasi lintas modul menghasilkan detection yang lebih akurat.

2. **(C3)** AWS GuardDuty mendeteksi "S3 GetObject dari TOR exit node." Sebagai Cloud SOC analyst, apa langkah triage Anda dalam 15 menit pertama setelah menerima alert ini?

## 7. Ringkasan Bab

Cloud SOC memerlukan tooling yang berbeda dari SOC tradisional: CSPM memantau konfigurasi, CWPP melindungi runtime workload, dan CIEM menganalisis entitlement. CNAPP mengintegrasikan ketiganya dalam satu platform dengan risk correlation. Cloud-native detection (GuardDuty, Security Command Center) dan open-source tools (Falco, kube-bench) melengkapi stack. Container runtime IR menghadapi tantangan ephemeral — forensic preservation harus dilakukan sebelum container dihapus.

## 12. Refleksi Profesional

1. CNAPP commercial tools (Wiz, Orca, Prisma Cloud) menawarkan visibility komprehensif namun memerlukan investasi signifikan. Open-source tools (Falco, Trivy, kube-bench) memerlukan lebih banyak expertise namun lebih fleksibel dan tanpa biaya lisensi. Dalam konteks organisasi pemerintah atau institusi pendidikan di Indonesia dengan anggaran terbatas, bagaimana Anda membangun Cloud SOC capability yang efektif dengan resource yang ada?

---

# BAB 16 — PENGAYAAN: DEVSECOPS, CLOUD IR, DAN JALUR SERTIFIKASI

## 1. Capaian Pembelajaran Bab

Setelah mempelajari bab ini, mahasiswa memahami:
- Integrasi keamanan dalam DevOps pipeline (DevSecOps)
- Incident response yang spesifik untuk cloud environments
- Jalur sertifikasi yang relevan untuk cloud security professional

*Bab Pengayaan — wawasan karir dan industri*

## 2. Peta Konsep Bab

```mermaid
flowchart TD
    A[Cloud Security Career Path] --> B[DevSecOps]
    B --> B1["Shift-left security:\nkeamanan dari awal pipeline"]
    B --> B2["SAST/DAST dalam CI/CD"]
    B --> B3["IaC security scan:\nCheckov, tfsec"]
    B --> B4["Secret scanning:\ngit-secrets, trufflehog"]
    A --> C[Cloud IR]
    C --> C1["IR di cloud berbeda:\nAPI-first, ephemeral,\nshared responsibility"]
    C --> C2["Cloud-native IR tools:\nCloudTrail + Athena,\nVPC Traffic Mirroring"]
    C --> C3["Container IR:\npreserve sebelum delete"]
    A --> D[Certification Pathway]
    D --> D1["Cloud fundamentals:\nAWS SAA, AZ-900, GCP ACE"]
    D --> D2["Cloud security:\nAWS Security Specialty,\nAZ-500, CCSP (ISC2)"]
    D --> D3["Container/K8s:\nCKA, CKAD, CKS"]
    D --> D4["General security:\nCISSP, CEH, CompTIA Security+"]
```

## 3. Pengantar Kontekstual

Cloud security bukan hanya tentang teknologi — ini juga tentang people dan process. DevSecOps mengintegrasikan keamanan ke dalam alur kerja development sehingga developer menjadi bagian dari tim keamanan, bukan musuhnya. Cloud IR memerlukan adaptasi metodologi IR tradisional untuk realitas cloud: ephemeral resources, API-based access, dan shared responsibility model.

## 4. Landasan Teori

### 4.1 DevSecOps — Shift-Left Security

"Shift-left" berarti memindahkan security checks lebih awal dalam software development lifecycle — dari "setelah deployment" (kanan) ke "sebelum/saat development" (kiri):

```
Traditional: DEV → BUILD → TEST → DEPLOY → [Security Review]
DevSecOps:   [Secret Scan] → DEV → [SAST] → BUILD → [Image Scan] → TEST → [IaC Scan] → DEPLOY → [CSPM + CWPP]
```

**Tools DevSecOps pipeline:**

```yaml
# Contoh GitLab CI/CD pipeline dengan security gates
stages:
  - code_quality
  - security_scan
  - build
  - image_scan
  - deploy

# 1. Secret scanning — sebelum commit masuk (pre-commit hook)
# Developer menginstall: pre-commit hook dengan gitleaks
# Setiap commit di-scan untuk hardcoded secrets (API key, password)

sast_scan:
  stage: security_scan
  image: semgrep/semgrep
  script:
    - semgrep --config=p/owasp-top-ten --config=p/python .
  # Gagalkan jika ditemukan HIGH severity finding

iac_scan:
  stage: security_scan
  image: bridgecrew/checkov
  script:
    - checkov -d terraform/ --severity HIGH --exit-code 1
  # Gagalkan jika ada misconfiguration HIGH atau CRITICAL

build_image:
  stage: build
  script:
    - docker build -t myapp:$CI_COMMIT_SHA .
    - docker push registry.company.com/myapp:$CI_COMMIT_SHA

image_vulnerability_scan:
  stage: image_scan
  image: aquasec/trivy
  script:
    - trivy image --exit-code 1 --severity CRITICAL registry.company.com/myapp:$CI_COMMIT_SHA
  # Gagalkan jika ada CVE CRITICAL dalam image
```

### 4.2 Cloud-Specific Incident Response

Cloud IR memiliki tantangan unik:

**1. Ephemeral resources:** EC2 instance yang di-autoscale bisa terminate sebelum forensic selesai. Solusi: enable VPC Flow Logs dan CloudTrail sebelum insiden; gunakan memory capture tools jika ada.

**2. API-centric investigation:** Di cloud, hampir semua aksi meninggalkan jejak di CloudTrail — API calls adalah "digital fingerprint" attacker.

**3. Shared responsibility:** Provider cloud bertanggung jawab untuk infrastruktur; customer bertanggung jawab untuk konfigurasi, data, dan akses. Dalam IR: tidak bisa "ambil harddisk server" untuk forensic — harus gunakan cloud-native snapshot.

```bash
# Cloud IR — preserve evidence EC2 (dalam environment yang berotorisasi)

# 1. Isolate instance (buat Security Group yang block semua traffic)
aws ec2 create-security-group \
    --group-name "ir-isolation-$(date +%Y%m%d)" \
    --description "Isolation SG for IR" \
    --vpc-id vpc-abc123

# 2. Apply isolation SG ke instance yang dikompromis
aws ec2 modify-instance-attribute \
    --instance-id i-compromised123 \
    --groups sg-isolation123

# 3. Create snapshot untuk forensic (SEBELUM terminate instance)
aws ec2 create-snapshot \
    --volume-id vol-abc123 \
    --description "IR Snapshot $(date +%Y%m%d) - i-compromised123"

# 4. Export CloudTrail logs untuk periode insiden
aws cloudtrail lookup-events \
    --lookup-attributes AttributeKey=Username,AttributeValue=compromised-user \
    --start-time "2025-10-15T00:00:00Z" \
    --end-time "2025-10-16T00:00:00Z" \
    > cloudtrail-ir-evidence.json

# 5. Hitung hash evidence
sha256sum cloudtrail-ir-evidence.json > cloudtrail-ir-evidence.json.sha256
```

### 4.3 Jalur Sertifikasi Cloud Security

**Tingkat Foundational:**
- AWS Certified Cloud Practitioner (CLF-C02)
- Microsoft AZ-900: Azure Fundamentals
- Google ACE (Associate Cloud Engineer)

**Tingkat Associate/Professional:**
- AWS Certified Solutions Architect – Associate (SAA-C03)
- AWS Certified Security – Specialty (SCS-C02) ← paling relevan untuk cloud security
- Microsoft AZ-500: Microsoft Azure Security Technologies
- Google Professional Cloud Security Engineer

**Container dan Kubernetes:**
- CKA: Certified Kubernetes Administrator
- CKAD: Certified Kubernetes Application Developer
- CKS: Certified Kubernetes Security Specialist ← paling relevan untuk K8s security

**Vendor-Agnostic:**
- CCSP (Certified Cloud Security Professional) — (ISC)² ← gold standard untuk cloud security
- CCSK (Certificate of Cloud Security Knowledge) — Cloud Security Alliance
- CompTIA Cloud+

**Rekomendasi learning path untuk mahasiswa program ini:**
1. AWS SAA-C03 (fondasi cloud)
2. CKA (Kubernetes)
3. AWS Security Specialty atau CKS (security focus)
4. Jangka panjang: CCSP (ISC)²

## 5. Model atau Arsitektur

```mermaid
flowchart LR
    subgraph DEV["Development Phase"]
        IDE["Developer IDE:\nreal-time SAST feedback\n(plugin: SonarLint, Snyk)"]
        PRE_COMMIT["Pre-commit hooks:\n• gitleaks (secret scan)\n• tflint (terraform lint)"]
    end
    
    subgraph CICD["CI/CD Pipeline"]
        SAST["SAST:\nSemgrep, Bandit (Python),\nSpotBugs (Java)"]
        IaC_SCAN["IaC Scan:\nCheckov, tfsec"]
        BUILD["Build: docker build"]
        IMG_SCAN["Image Scan:\nTrivy, Grype"]
        SIGN["Sign: Cosign"]
        SBOM["SBOM: Syft/Trivy"]
    end
    
    subgraph DEPLOY["Deployment + Runtime"]
        ADMC["Admission Control:\nKyverno (verify signature)"]
        CSPM_RT["CSPM:\nnew resource compliance"]
        CWPP_RT["CWPP/Falco:\nruntime anomaly detection"]
    end
    
    IDE --> PRE_COMMIT --> SAST --> IaC_SCAN --> BUILD --> IMG_SCAN --> SIGN --> SBOM --> ADMC --> CSPM_RT & CWPP_RT
```

## 6. Latihan Pemahaman

1. **(C4)** Apa yang dimaksud dengan "cloud blast radius" dalam konteks insiden keamanan, dan bagaimana microsegmentation melalui VPC dan NetworkPolicy menguranginya?

2. **(C4)** Dalam DevSecOps, developer sering mengeluh bahwa security gates "memperlambat delivery." Bagaimana Anda merespons keluhan ini secara konstruktif, dengan argumen yang mengakui kekhawatiran mereka namun tetap mempertahankan posisi bahwa security gates diperlukan?

## 7. Ringkasan Bab

DevSecOps mengintegrasikan keamanan ke setiap tahap pipeline: secret scanning (pre-commit), SAST (code phase), IaC scan (build phase), image scan (container build phase), dan CSPM/CWPP (runtime phase). Cloud IR berbeda dari traditional IR: API-centric, ephemeral resources, shared responsibility — memerlukan adaptasi tools dan prosedur. Jalur sertifikasi untuk cloud security profesional mencakup cloud platform certs (AWS, Azure, GCP), K8s security (CKS), dan vendor-agnostic (CCSP).

## 12. Refleksi Profesional

1. Di Indonesia, adopsi cloud computing di sektor pemerintah dan BUMN masih relatif awal. Sebagai profesional keamanan siber yang akan lulus dari program magister ini, bagaimana Anda dapat berkontribusi dalam membangun kapabilitas keamanan cloud di organisasi tempat Anda berkarir? Apa gap terbesar yang Anda lihat antara "best practice cloud security" yang dipelajari dalam program ini dengan realitas praktis di lapangan?


---

# LAMPIRAN

---

## Lampiran A — Template Laporan Capstone Security Assessment

```
====================================================================
LAPORAN SECURITY ASSESSMENT CLOUD/CONTAINER
Mata Kuliah: Virtualization and Cloud Security (MK-E-05)
Program Studi: Magister Terapan Forensik Digital dan Keamanan Siber
====================================================================

Nama Mahasiswa   : _____________________________________________
NIM              : _____________________________________________
Skenario         : PT. CloudNusa AWS Environment
Periode Asesmen  : _______________ s/d _______________
Tanggal Laporan  : _______________
Versi            : 1.0
Klasifikasi      : Confidential — Lab Use Only

====================================================================
BAGIAN I — EXECUTIVE SUMMARY
====================================================================

1.1 Ringkasan Temuan
----------------------------------------------------------------------
Total Temuan:
  Critical : ___
  High     : ___
  Medium   : ___
  Low      : ___
  
Sudah Dimitigasi  : ___
Residual Risk     : ___

1.2 Dampak Bisnis (narasi 2-3 paragraf non-teknis)
----------------------------------------------------------------------
[Tulis dampak bisnis dari temuan paling signifikan, dalam bahasa
yang dapat dipahami manajemen non-teknis]

1.3 Rekomendasi Utama
----------------------------------------------------------------------
1. [Rekomendasi terpenting] — Prioritas: Critical
2. [Rekomendasi kedua] — Prioritas: High
3. [Rekomendasi ketiga] — Prioritas: High

====================================================================
BAGIAN II — METODOLOGI
====================================================================

2.1 Scope
----------------------------------------------------------------------
In-scope  : [list komponen yang diases]
Out-scope : [list yang tidak diases]

2.2 Framework Referensi
----------------------------------------------------------------------
□ CIS AWS Foundations Benchmark v1.5
□ CIS EKS Benchmark v1.4
□ NIST SP 800-190 (Container Security)
□ NIST CSF v1.1
□ NIST SP 800-125 (Virtualization Security)

2.3 Metodologi yang Digunakan
----------------------------------------------------------------------
□ Asset Discovery dan Inventory
□ Architecture Review
□ Trust Boundary Mapping
□ STRIDE Threat Modelling
□ CIS Benchmark Assessment
□ Control Implementation dan Validasi

====================================================================
BAGIAN III — ASSET INVENTORY
====================================================================

3.1 Compute Resources
----------------------------------------------------------------------
| ID | Type | Region | OS/Runtime | Purpose | Data Classification |
|____|______|________|____________|_________|_____________________|
|    |      |        |            |         |                     |

3.2 Network Resources
----------------------------------------------------------------------
| Resource | CIDR/ID | Purpose | Trust Level |
|__________|________|_________|_____________|
|          |        |         |             |

3.3 Identity Resources (IAM)
----------------------------------------------------------------------
| Principal | Type | Policies | MFA | Last Used | Risk |
|___________|______|__________|_____|___________|______|
|           |      |          |     |           |      |

====================================================================
BAGIAN IV — ARCHITECTURE REVIEW
====================================================================

4.1 Architecture Diagram (As-Is)
----------------------------------------------------------------------
[Sertakan diagram arsitektur menggunakan Mermaid atau gambar]

4.2 Trust Boundary Map
----------------------------------------------------------------------
[Sertakan trust boundary diagram]

4.3 Attack Surface Analysis
----------------------------------------------------------------------
| Entry Point | Exposure | Kontrol Ada | Gap |
|_____________|__________|_____________|_____|
|             |          |             |     |

====================================================================
BAGIAN V — THREAT MODEL (STRIDE)
====================================================================

5.1 Komponen yang Dianalisis: ____________________________

| Threat Category | Threat | Likelihood | Impact | Risk | Mitigasi |
|_________________|________|____________|________|______|__________|
| Spoofing        |        |            |        |      |          |
| Tampering       |        |            |        |      |          |
| Repudiation     |        |            |        |      |          |
| Info Disclosure |        |            |        |      |          |
| Denial of Svc   |        |            |        |      |          |
| EoP             |        |            |        |      |          |

====================================================================
BAGIAN VI — TECHNICAL FINDINGS
====================================================================

[TEMPLATE PER FINDING]

Finding ID : F-00X
Judul      : ________________________________________________
Severity   : □ Critical  □ High  □ Medium  □ Low
Status     : □ Open  □ Remediated  □ Accepted Risk
Framework  : [CIS/NIST reference]

Deskripsi  :
[Jelaskan misconfiguration atau kerentanan yang ditemukan]

Evidence   :
File: [evidence/FX-xxx.txt]
SHA256: ________________

Dampak     :
[Jelaskan dampak jika dieksploitasi]

Remediation:
[Apa yang harus dilakukan]

Validasi   :
[Bagaimana memverifikasi remediation berhasil]

Residual Risk:
[Risk yang masih ada setelah mitigasi, jika ada]

====================================================================
BAGIAN VII — IMPLEMENTED CONTROLS
====================================================================

| Control ID | Deskripsi | Finding Addressed | Before | After | Evidence |
|____________|___________|__________________|________|_______|__________|
|            |           |                  |        |       |          |

====================================================================
BAGIAN VIII — RESIDUAL RISK REGISTER
====================================================================

| Risk ID | Deskripsi | Severity | Alasan Belum Dimitigasi | Rencana |
|_________|___________|__________|_________________________|_________|
|         |           |          |                         |         |

====================================================================
BAGIAN IX — REKOMENDASI ROADMAP
====================================================================

Immediate (0–30 hari):
1.
2.

Short-term (30–90 hari):
1.
2.

Long-term (90+ hari):
1.
2.

====================================================================
BAGIAN X — HASH MANIFEST EVIDENCE
====================================================================

[Output dari: sha256sum evidence/* > HASH_MANIFEST.txt]

====================================================================
PERNYATAAN ASSESSOR
====================================================================

Saya menyatakan bahwa assessment ini dilakukan dalam lingkungan
lab yang diotorisasi terhadap skenario fiktif yang disediakan
oleh dosen. Tidak ada sistem nyata pihak ketiga yang diakses
tanpa otorisasi selama proses assessment ini.

Nama      : _____________________________________________
NIM       : _____________________________________________
Tanggal   : _____________________________________________
Tanda Tangan : _____________________________________________
```

---

## Lampiran B — Template Secure Cloud Architecture Design

```
====================================================================
SECURE CLOUD ARCHITECTURE DESIGN DOCUMENT
====================================================================

Nama Mahasiswa   : _____________________________________________
Mata Kuliah      : MK-E-05 Virtualization and Cloud Security
Judul Desain     : _____________________________________________
Tanggal          : _______________

====================================================================
1. BUSINESS CONTEXT DAN REQUIREMENTS
====================================================================

1.1 Deskripsi Aplikasi/Sistem
----------------------------------------------------------------------
[Jelaskan apa yang akan di-deploy: aplikasi web, microservices, dll.]

1.2 Data Classification
----------------------------------------------------------------------
Jenis data yang diproses: □ Public  □ Internal  □ Confidential  □ Restricted
Regulasi yang berlaku   : □ UU PDP  □ PCI-DSS  □ HIPAA  □ Lainnya: _______

1.3 Availability Requirements
----------------------------------------------------------------------
RTO (Recovery Time Objective) : _____________
RPO (Recovery Point Objective): _____________
Target uptime                 : ___% (setara ___ jam downtime/tahun)

====================================================================
2. ARCHITECTURE DESIGN
====================================================================

2.1 Network Architecture
----------------------------------------------------------------------
[Mermaid diagram — VPC, subnet layout, security boundaries]

VPC CIDR          : _____________
Public Subnets    : _____________ (untuk: _____________)
Private Subnets   : _____________ (untuk: _____________)
Data Subnets      : _____________ (untuk: _____________)

2.2 Compute Design
----------------------------------------------------------------------
| Component | Type | Subnet | OS/Runtime | Justification |
|___________|______|________|____________|_______________|
|           |      |        |            |               |

2.3 Security Controls per Layer
----------------------------------------------------------------------
Layer 1 — Identity    : [IAM strategy, MFA, federation]
Layer 2 — Network     : [VPC, SG rules, NACL, WAF]
Layer 3 — Compute     : [hardening, patching, no-SSH policy]
Layer 4 — Application : [container security, PSS, RBAC]
Layer 5 — Data        : [encryption at rest, in-transit, backup]
Layer 6 — Monitoring  : [logging, alerting, SIEM integration]

2.4 IAM Design
----------------------------------------------------------------------
| Role/User | Purpose | Permissions | Conditions |
|___________|_________|_____________|____________|
|           |         |             |            |

====================================================================
3. THREAT MODEL RINGKASAN
====================================================================

| Threat | Control | Residual Risk |
|________|_________|_______________|
|        |         |               |

====================================================================
4. COMPLIANCE MAPPING
====================================================================

| Control | CIS Ref | NIST Ref | NIST SP 800-190 | Implemented? |
|_________|_________|__________|_________________|______________|
|         |         |          |                  |              |

====================================================================
5. IaC SECURITY GATES
====================================================================

Pipeline Security Checks:
□ Secret scanning (gitleaks/trufflehog)
□ SAST (semgrep)
□ IaC scan (checkov)
□ Image vulnerability scan (trivy)
□ Image signing (cosign)
□ Admission control (kyverno/OPA)
□ Runtime detection (falco/guardduty)

====================================================================
6. DISASTER RECOVERY PLAN
====================================================================

DR Strategy: □ Backup & Restore  □ Pilot Light  □ Warm Standby  □ Active-Active
DR Region   : _____________________________________________
Backup Frequency: ________________
Backup Retention: ________________
Last DR Test Date: ________________
DR Test Results  : ________________
```

---

## Lampiran C — Template Risk Register Cloud

```
====================================================================
CLOUD SECURITY RISK REGISTER
====================================================================

Organisasi   : _____________________________________________
Environment  : □ AWS  □ Azure  □ GCP  □ On-Premises  □ Hybrid
Tanggal      : _______________
Versi        : _______________

====================================================================
RISK REGISTER
====================================================================

Risk ID  : R-001
Kategori : □ IAM  □ Network  □ Compute  □ Data  □ Monitoring  □ Supply Chain
Deskripsi: ________________________________________________
Threat Actor: ________________________________________________
Attack Vector: ________________________________________________

Penilaian Risiko Inherent:
Likelihood : □ Low (1)  □ Medium (2)  □ High (3)  □ Critical (4)
Impact     : □ Low (1)  □ Medium (2)  □ High (3)  □ Critical (4)
Risk Score : ___ (Likelihood × Impact)

Kontrol yang Ada:
1. ________________________________________________
2. ________________________________________________

Penilaian Risiko Residual (setelah kontrol):
Likelihood : □ Low (1)  □ Medium (2)  □ High (3)  □ Critical (4)
Impact     : □ Low (1)  □ Medium (2)  □ High (3)  □ Critical (4)
Risk Score : ___ (Likelihood × Impact)

Keputusan: □ Accept  □ Mitigate  □ Transfer  □ Avoid
Rencana Mitigasi (jika mitigate):
________________________________________________

Pemilik Risk   : ________________________________________________
Target Tanggal : ________________________________________________
Review Berikutnya: ______________

Framework Reference:
CIS  : ________________________________________________
NIST : ________________________________________________
```

---

## Lampiran D — Template Evidence Pack Capstone

```
====================================================================
EVIDENCE PACK MANIFEST
Capstone Security Assessment — MK-E-05
====================================================================

Nama Mahasiswa : _____________________________________________
NIM            : _____________________________________________
Skenario       : _____________________________________________

====================================================================
STRUKTUR EVIDENCE PACK
====================================================================

capstone-evidence/
├── README.md                 (file ini)
├── HASH_MANIFEST.txt         (SHA256 semua file)
├── phase1/
│   ├── P1-01-asset-inventory.[xlsx/md]
│   ├── P1-02-architecture-diagram.[png/mermaid]
│   ├── P1-03-trust-boundary-map.[png/mermaid]
│   ├── P1-04-stride-threat-model.[xlsx/md]
│   ├── P1-05-risk-matrix-initial.[xlsx/md]
│   └── P1-06-gap-analysis.[md]
├── phase2/
│   ├── C001-[nama-kontrol]/
│   │   ├── before-state.txt
│   │   ├── implementation.sh  (atau .yaml, .tf, dll)
│   │   ├── after-state-positive.txt
│   │   ├── after-state-negative.txt (negative test)
│   │   └── notes.md
│   ├── C002-[nama-kontrol]/
│   │   └── [sama seperti di atas]
│   └── [C003-C00N]/
└── phase3/
    ├── final-report.pdf (atau .md)
    └── risk-matrix-updated.[xlsx/md]

====================================================================
EVIDENCE LOG
====================================================================

| File | Deskripsi | Dibuat Tanggal | Dibuat Oleh | SHA256 |
|______|___________|_______________|_____________|________|
|      |           |               |             |        |

====================================================================
CARA MEMBUAT HASH MANIFEST
====================================================================

Jalankan command berikut dari direktori capstone-evidence/:

    find . -type f -not -name "HASH_MANIFEST.txt" \
        -exec sha256sum {} \; | sort > HASH_MANIFEST.txt

Simpan HASH_MANIFEST.txt juga di lokasi terpisah (misalnya submit
ke LMS) untuk verifikasi integritas di kemudian hari.

====================================================================
CATATAN INTEGRITAS
====================================================================

Evidence ini dikumpulkan dalam lingkungan lab berotorisasi.
Tidak ada modifikasi yang dilakukan terhadap file evidence
setelah hash digenerate.

Pernyataan Assessor: ______________________ Tanggal: ____________
```

---

## Lampiran E — Template Compliance Mapping CIS/NIST

```
====================================================================
COMPLIANCE MAPPING — MK-E-05 Capstone
====================================================================

Environment     : □ AWS  □ EKS  □ Docker  □ Hybrid
Framework Utama : CIS Benchmark + NIST SP 800-190

====================================================================
CIS AWS FOUNDATIONS BENCHMARK
====================================================================

| Check ID | Deskripsi | Status | Evidence | Catatan |
|----------|-----------|--------|----------|---------|
| 1.1  | Root account hardware MFA | □ PASS □ FAIL □ N/A | | |
| 1.4  | No access key for root | □ PASS □ FAIL □ N/A | | |
| 1.14 | MFA enabled for all IAM users | □ PASS □ FAIL □ N/A | | |
| 1.16 | No AdministratorAccess policy | □ PASS □ FAIL □ N/A | | |
| 2.1  | CloudTrail enabled all regions | □ PASS □ FAIL □ N/A | | |
| 2.4  | CloudTrail S3 server access log | □ PASS □ FAIL □ N/A | | |
| 2.7  | CloudTrail log encryption | □ PASS □ FAIL □ N/A | | |
| 3.1  | Unauthorized API call alerts | □ PASS □ FAIL □ N/A | | |
| 4.1  | No SG allows 0.0.0.0/0 SSH | □ PASS □ FAIL □ N/A | | |
| 4.2  | No SG allows 0.0.0.0/0 RDP | □ PASS □ FAIL □ N/A | | |
| 5.1  | Default VPC no SG open | □ PASS □ FAIL □ N/A | | |

====================================================================
CIS EKS BENCHMARK (jika berlaku)
====================================================================

| Check ID | Deskripsi | Status | Evidence |
|----------|-----------|--------|----------|
| 3.2.1 | API server not publicly accessible | □ PASS □ FAIL | |
| 4.1.1 | Default ServiceAccount no auto-mount | □ PASS □ FAIL | |
| 4.2.1 | Minimize admins in cluster | □ PASS □ FAIL | |
| 5.1.1 | RBAC authorization enabled | □ PASS □ FAIL | |
| 5.2.1 | PSA: restrict privileged containers | □ PASS □ FAIL | |
| 5.4.1 | Secrets not stored in env vars | □ PASS □ FAIL | |
| 5.7.1 | NetworkPolicy default-deny | □ PASS □ FAIL | |

====================================================================
NIST SP 800-190 MAPPING
====================================================================

| Control Area | Requirement | Implemented? | How |
|--------------|-------------|--------------|-----|
| Image Security | Scan for known vulnerabilities | □ Ya □ Tidak | |
| Image Security | Use minimal base images | □ Ya □ Tidak | |
| Image Security | Do not run as root | □ Ya □ Tidak | |
| Registry Security | Restrict write access | □ Ya □ Tidak | |
| Registry Security | Enable vulnerability scanning | □ Ya □ Tidak | |
| Orchestrator Security | RBAC enabled | □ Ya □ Tidak | |
| Orchestrator Security | Network segmentation | □ Ya □ Tidak | |
| Orchestrator Security | Secrets management | □ Ya □ Tidak | |
| Container Runtime | Limit resource usage | □ Ya □ Tidak | |
| Container Runtime | Runtime threat detection | □ Ya □ Tidak | |
| Host OS | Minimal host OS | □ Ya □ Tidak | |
| Host OS | CIS benchmark compliant | □ Ya □ Tidak | |
```

---

## Lampiran F — Rubrik Penilaian Capstone (Eval-5/EAS)

| Komponen | Bobot | Kriteria Penilaian |
|---|---|---|
| **Fase 1: Security Architecture Review** | **30%** | |
| Asset inventory kelengkapan | 10% | Semua komponen terdokumentasi; klasifikasi data tepat |
| Architecture diagram akurasi | 10% | Diagram mencerminkan skenario; trust boundary jelas |
| STRIDE threat model kualitas | 10% | Min. 3 komponen; 4+ threats per komponen; risk rating tepat |
| **Fase 2: Control Implementation** | **40%** | |
| Jumlah kontrol yang diimplementasikan | 10% | Min. 5 kontrol; diprioritaskan dari risk matrix |
| Kualitas implementasi dan evidence | 20% | Before/after state; negative test; evidence ter-hash |
| Validasi yang komprehensif | 10% | Functional + negative test; residual risk didokumentasikan |
| **Fase 3: Laporan dan Komunikasi** | **30%** | |
| Executive summary kualitas | 10% | Non-teknis; berbasis dampak bisnis; actionable |
| Technical findings akurasi | 10% | Evidence-backed; severity tepat; reproducible |
| Evidence pack organisasi | 10% | Terstruktur; hash manifest; timeline lengkap |

**Catatan Penilai:**
- Nilai minimum untuk lulus: 70/100
- Plagiarisme atau evidence yang difabrikasi = nilai 0 dan pelanggaran akademik
- Semua tindakan harus dalam lingkungan lab berotorisasi; bukti akses sistem nyata tanpa otorisasi = gugur
- Bobot mengikuti RPS: Eval-5/EAS = 30% dari nilai akhir

---

## Lampiran G — Pernyataan Etika Praktikum dan Capstone

```
====================================================================
PERNYATAAN ETIKA DAN KOMITMEN KEAMANAN SIBER
Mata Kuliah: Virtualization and Cloud Security (MK-E-05)
Program Studi: Magister Terapan Forensik Digital dan Keamanan Siber
Politeknik Elektronika Negeri Surabaya (PENS)
====================================================================

Saya yang bertanda tangan di bawah ini:

Nama         : ________________________________________________
NIM          : ________________________________________________
Angkatan     : ________________________________________________
Email        : ________________________________________________

menyatakan dan berkomitmen sebagai berikut:

====================================================================
PASAL 1 — BATAS LINGKUNGAN PRAKTIKUM
====================================================================

1.1 Seluruh kegiatan praktikum, lab, dan capstone dalam mata kuliah
    ini HANYA dilakukan dalam lingkungan yang secara eksplisit
    diotorisasi oleh dosen pengampu.

1.2 Lingkungan yang diotorisasi meliputi:
    a. Cluster Kubernetes lokal (Minikube, Kind, k3s) yang disetup
       oleh mahasiswa sendiri di mesin pribadi atau lab;
    b. AWS/Azure/GCP sandbox account yang disediakan atau disetujui
       program studi;
    c. Skenario fiktif (seperti "PT. CloudNusa") yang diberikan dosen;
    d. Dataset, log, dan artefak yang disanitasi dan disediakan dosen.

1.3 Lingkungan yang TIDAK PERNAH diotorisasi (kecuali ada izin
    tertulis eksplisit):
    a. Akun cloud, tenant, cluster, atau resource milik pihak ketiga;
    b. Infrastruktur organisasi tempat saya bekerja (kecuali ada
       izin tertulis dari manajemen);
    c. Internet-facing services milik organisasi mana pun;
    d. Resource publik yang tidak secara eksplisit dibuat untuk
       tujuan praktikum (misal: bug bounty program).

====================================================================
PASAL 2 — PERLINDUNGAN DATA
====================================================================

2.1 Konfigurasi, log, token, secret, credential, dan artefak yang
    dikumpulkan dalam capstone harus disanitasi dari data sensitif
    sebelum dikumpulkan sebagai tugas.

2.2 Artefak lab tidak boleh dibagikan di luar konteks perkuliahan.

2.3 Jika dalam praktikum tidak sengaja menemukan data sensitif nyata
    (misalnya credential aktif dalam dataset latihan), saya wajib
    segera melaporkan kepada dosen dan tidak menggunakannya.

====================================================================
PASAL 3 — PRAKTIK DEFENSIF
====================================================================

3.1 Semua aktivitas dalam mata kuliah ini berfokus pada:
    analisis, pertahanan, deteksi, validasi, dokumentasi, dan
    rekomendasi berbasis evidence.

3.2 Pengetahuan tentang attack techniques yang dipelajari dalam
    mata kuliah ini HANYA digunakan untuk tujuan defensif:
    memahami cara kerja ancaman untuk dapat mendeteksi dan
    mencegahnya — bukan untuk mengeksploitasi sistem nyata.

3.3 Penggunaan pengetahuan dan tools dari mata kuliah ini untuk
    tindakan ofensif tidak sah adalah pelanggaran hukum (UU ITE,
    KUHP, UU PDP) dan pelanggaran kode etik profesi.

====================================================================
PASAL 4 — AKIBAT PELANGGARAN
====================================================================

4.1 Pelanggaran terhadap pernyataan ini dapat mengakibatkan:
    a. Nilai 0 untuk seluruh mata kuliah;
    b. Pelaporan kepada komite akademik program studi;
    c. Pelaporan kepada otoritas hukum jika terdapat indikasi
       tindak pidana.

====================================================================
PASAL 5 — KOMITMEN PROFESIONAL
====================================================================

5.1 Saya memahami bahwa sebagai calon profesional keamanan siber,
    kepercayaan adalah aset terpenting. Saya berkomitmen untuk
    selalu bertindak dalam batas-batas hukum, etika profesi, dan
    otorisasi yang jelas.

5.2 Saya memahami bahwa "niat baik" tidak menggantikan otorisasi
    tertulis. Pengujian tanpa otorisasi adalah pelanggaran,
    bahkan jika tujuannya membantu.

====================================================================
TANDA TANGAN
====================================================================

Surabaya, _______________ 20___

Mahasiswa,                         Diketahui Dosen Pengampu,


_______________________            _______________________
[Nama Mahasiswa]                   [Nama Dosen]
NIM: ______________                NIP/NIDN: ____________
```


---

# KUNCI JAWABAN GLOBAL DAN CATATAN DOSEN

## Panduan Penggunaan Kunci Jawaban Global

Setiap bab dalam buku ini telah menyertakan kunci jawaban lengkap beserta pembahasan teoretis pada Bagian 10 (Kunci Jawaban dan Pembahasan) masing-masing bab. Bagian ini menyajikan catatan tambahan untuk dosen mengenai soal-soal yang memerlukan penilaian subjektif atau diskusi kelas yang lebih mendalam.

---

## Catatan Dosen — Soal Diskusi Kelas

### Bab 1 — Arsitektur Virtualisasi

**Refleksi Profesional Bab 1 (untuk diskusi kelas):**
"Dalam konteks pemerintah Indonesia yang mulai mengadopsi cloud dan virtualisasi, tetapi memiliki concern tentang kedaulatan data, bagaimana kebijakan keamanan yang tepat?"

*Panduan fasilitasi:* Dorong mahasiswa mempertimbangkan framework SPBE (Sistem Pemerintahan Berbasis Elektronik), Peraturan Presiden No. 95/2018, dan BSSN sebagai otoritas keamanan siber nasional. Diskusikan trade-off antara adopsi teknologi dan kedaulatan data.

---

### Bab 2 — Shared Responsibility Model

**Shared Responsibility sebagai topik konflik nyata:** Banyak insiden cloud terjadi karena miscomunication antara customer dan provider tentang siapa bertanggung jawab atas apa. Dorong mahasiswa membawa contoh kasus nyata yang mereka ketahui dan identifikasi di mana letak gap responsibility-nya.

---

### Bab 9 — Logging dan Forensic Readiness

**Dilema privacy vs forensic readiness:** Ini adalah topik yang tidak memiliki jawaban benar tunggal. Fasilitator harus memastikan mahasiswa memahami bahwa:
1. UU PDP mengatur data pribadi, termasuk IP address dan usage patterns yang ada dalam log
2. Forensic readiness memerlukan log yang cukup detail untuk investigation
3. Data retention minimum yang diperlukan compliance berbeda dari yang diperlukan forensic

*Data minimization principle:* Log hanya apa yang diperlukan; anonimisasi apa yang bisa; enkripsi apa yang harus disimpan.

---

### Bab 14 — Capstone Fase 3

**Kewajiban UU PDP dalam studi kasus S3 bucket public:**

Berdasarkan UU No. 27 Tahun 2022 tentang Perlindungan Data Pribadi:
- Pasal 46: kewajiban notifikasi kepada Menteri (Kominfo/Kemenkominfo) dan subjek data dalam 14 hari kerja setelah mengetahui kebocoran
- Pasal 57: sanksi administratif berupa denda hingga 2% dari pendapatan tahunan
- Pasal 67: sanksi pidana (jika ada unsur kesengajaan): penjara hingga 5 tahun dan/atau denda hingga Rp 5 miliar

*Catatan untuk dosen:* Regulasi ini masih relatif baru (efektif Oktober 2024). Mahasiswa didorong memverifikasi perkembangan terbaru regulasi ini melalui sumber resmi (kominfo.go.id, bssn.go.id).

---

## Rekap Evaluasi per Sub-CPMK

| Sub-CPMK | Bab | Evaluasi | Bobot | Bentuk |
|---|---|---|---|---|
| Sub-CPMK-1: Arsitektur virtualisasi dan cloud | 1–3 | Eval-1 | 10% | Quiz/tugas |
| Sub-CPMK-2: IAM dan network security | 4–6 | Eval-2 | 15% | Tugas analisis |
| Sub-CPMK-3: Container security, K8s, logging | 7–9 | Eval-3 | 25% | Lab + laporan |
| Sub-CPMK-4: Secure architecture, monitoring, DR | 10–11 | Eval-4 | 20% | Tugas desain |
| Sub-CPMK-5: Capstone — design, implement, report | 12–14 | Eval-5/EAS | 30% | Capstone project |

---

# DAFTAR PUSTAKA

## Pustaka Utama

1. National Institute of Standards and Technology (NIST). (2011). *SP 800-125: Guide to Security for Full Virtualization Technologies*. U.S. Department of Commerce. https://doi.org/10.6028/NIST.SP.800-125

2. National Institute of Standards and Technology (NIST). (2017). *SP 800-190: Application Container Security Guide*. U.S. Department of Commerce. https://doi.org/10.6028/NIST.SP.800-190

3. National Institute of Standards and Technology (NIST). (2020). *SP 800-207: Zero Trust Architecture*. U.S. Department of Commerce. https://doi.org/10.6028/NIST.SP.800-207

4. Cloud Security Alliance (CSA). (2023). *Cloud Controls Matrix (CCM) v4.0*. Cloud Security Alliance. https://cloudsecurityalliance.org/research/cloud-controls-matrix/

5. Center for Internet Security (CIS). (2023). *CIS Amazon Web Services Foundations Benchmark v1.5*. CIS. https://www.cisecurity.org/benchmark/amazon_web_services

6. Center for Internet Security (CIS). (2023). *CIS Amazon Elastic Kubernetes Service (EKS) Benchmark v1.4*. CIS. https://www.cisecurity.org/benchmark/kubernetes

7. Center for Internet Security (CIS). (2023). *CIS Docker Benchmark v1.6*. CIS. https://www.cisecurity.org/benchmark/docker

## Pustaka Pendukung

8. Cloud Native Computing Foundation (CNCF). (2022). *Cloud Native Security Whitepaper v2*. CNCF. https://github.com/cncf/tag-security/blob/main/community/resources/security-whitepaper/v2/

9. Cloud Native Computing Foundation (CNCF). (2021). *Kubernetes Security Audit*. CNCF. https://github.com/cncf/tag-security/tree/main/assessments/projects/kubernetes

10. Open Web Application Security Project (OWASP). (2022). *Docker Security Cheat Sheet*. OWASP. https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html

11. Open Web Application Security Project (OWASP). (2022). *Kubernetes Security Cheat Sheet*. OWASP. https://cheatsheetseries.owasp.org/cheatsheets/Kubernetes_Security_Cheat_Sheet.html

12. Amazon Web Services. (2023). *AWS Security Best Practices*. AWS Documentation. https://docs.aws.amazon.com/security/

13. Amazon Web Services. (2023). *Amazon EKS Best Practices Guide — Security*. AWS Documentation. https://aws.github.io/aws-eks-best-practices/security/docs/

14. HashiCorp. (2023). *Terraform Security Best Practices*. HashiCorp Developer. https://developer.hashicorp.com/terraform/cloud-docs/recommended-practices

15. Aqua Security. (2022). *The State of Cloud Native Security Report 2022*. Aqua Security. https://www.aquasec.com/resources/

16. Falco Project. (2023). *Falco: Cloud Native Runtime Security*. Falco.org. https://falco.org/docs/

17. Kyverno Project. (2023). *Kyverno: Kubernetes Native Policy Management*. Kyverno.io. https://kyverno.io/docs/

18. Sigstore. (2023). *Cosign: Container Signing, Verification, and Storage in an OCI Registry*. Sigstore. https://docs.sigstore.dev/cosign/overview/

19. Open Policy Agent (OPA). (2023). *OPA Documentation*. OPA.io. https://www.openpolicyagent.org/docs/

20. NIST. (2022). *NIST Cybersecurity Framework (CSF) 1.1*. NIST. https://www.nist.gov/cyberframework

21. Trivy Project. (2023). *Trivy: Vulnerability Scanner for Container Images and File Systems*. Aqua Security. https://trivy.dev/docs/

22. National Institute of Standards and Technology (NIST). (2022). *SP 800-53 Rev 5: Security and Privacy Controls for Information Systems and Organizations*. U.S. Department of Commerce. https://doi.org/10.6028/NIST.SP.800-53r5

23. Peltier, T. R. (2016). *Information Security Policies, Procedures, and Standards: Guidelines for Effective Information Security Management*. CRC Press.

24. Kim, G., Humble, J., Debois, P., & Willis, J. (2016). *The DevOps Handbook: How to Create World-Class Agility, Reliability, and Security in Technology Organizations*. IT Revolution Press.

25. Murdoch, J. (2023). *Cloud Security: A Comprehensive Guide to Secure Cloud Computing*. John Wiley & Sons.

26. Kubernetes Documentation Team. (2023). *Kubernetes Documentation: Security*. Kubernetes.io. https://kubernetes.io/docs/concepts/security/

27. Pemerintah Republik Indonesia. (2022). *Undang-Undang Nomor 27 Tahun 2022 tentang Perlindungan Data Pribadi*. Lembaran Negara Republik Indonesia Tahun 2022 Nomor 196.

28. Badan Siber dan Sandi Negara (BSSN). (2021). *Pedoman Keamanan Sistem Informasi dan Infrastruktur Teknologi Informasi Berbasis Cloud Computing*. BSSN. https://www.bssn.go.id/

29. Miell, I., & Sayers, A. H. (2023). *Docker in Practice* (2nd ed.). Manning Publications.

30. Rice, L., & Hausenblas, M. (2022). *Container Security: Fundamental Technology Concepts that Protect Containerized Applications*. O'Reilly Media.

---

*Buku ajar ini telah diselaraskan dengan Rencana Pembelajaran Semester (RPS) MK-E-05 Virtualization and Cloud Security, Program Studi Magister Terapan Forensik Digital dan Keamanan Siber, PENS. Seluruh materi, contoh kode, dan aktivitas praktikum dirancang untuk tujuan defensif dan pendidikan dalam lingkungan yang berotorisasi.*

*© 2025 Program Studi Magister Terapan Forensik Digital dan Keamanan Siber, PENS. Untuk penggunaan internal akademik.*

