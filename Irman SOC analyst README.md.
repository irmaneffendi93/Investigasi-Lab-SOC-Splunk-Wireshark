# 🛡️ Cybersecurity & SOC Tier 1 Analyst Portfolio

Selamat datang di repositori portofolio saya! Repositori ini mendokumentasikan proyek laboratorium deteksi ancaman (*Threat Detection*), triase peringatan (*Alert Triage*), dan investigasi insiden keamanan siber menggunakan **Splunk Enterprise** dan **Wireshark**.

---

## 👨‍💻 Tentang Saya
**Irman Efendi** — *Junior SOC Analyst (Tier 1) | IT Infrastructure & Cybersecurity Specialist*  
📍 Tangerang Selatan, Banten, Indonesia  
📧 Email: irmaneffendie93@gmail.com  
📄 Dokumen Lengkap: [Lihat CV Lengkap](./CV_Irman_Efendi_SOC_Analyst.pdf)

### Core Competencies & Tools
* **SIEM & Log Analysis:** Splunk Enterprise (SPL Queries, `eval`, `where`, Threshold-based Detection)
* **Network Traffic Analysis:** Wireshark (PCAP Inspection, HTTP/TCP Stream Analysis)
* **SOC Tier 1 Operations:** Alert Triage, True Positive vs. False Positive Validation, Severity Scoring, Incident Containment & Escalation
* **Frameworks & Standards:** MITRE ATT&CK Mapping, NIST SP 800-61 Incident Handling, SKKNI SOC (KEPNAKER No. 391 Tahun 2020)

---

## 🔍 Studi Kasus Investigasi Lab SOC (Splunk & Wireshark)

### 1. Brute Force & Suspicious Privileged Login
* **MITRE ATT&CK:** `T1110` (Brute Force), `T1078` (Valid Accounts)
* **Tools:** Splunk Enterprise (SPL)
* **Ringkasan Investigasi:** Melakukan analisis log autentikasi pada Splunk dan mendeteksi percobaan login berulang dari alamat IP eksternal yang menargetkan akun administrator (*privileged accounts*).
* **Klasifikasi:** **True Positive (High Severity)**
* **Tindakan & Mitigasi:** Merekomendasikan pemblokiran IP sumber pada perimeter firewall, melakukan *reset* kredensial akun terdampak, mengaktifkan MFA, serta eskalasi tiket insiden ke **Tier 2 SOC**.

---

### 2. Active Reconnaissance & SQL Injection Attempt
* **MITRE ATT&CK:** `T1595` (Active Scanning), `T1190` (Exploit Public-Facing Application)
* **Tools:** Splunk Enterprise (Firewall & WAF Logs)
* **Ringkasan Investigasi:** Menganalisis lonjakan trafik *TCP port scanning* secara cepat (*burst*) yang diikuti pola serangan *SQL Injection* berulang pada aplikasi web (status `HTTP 403 Blocked` oleh WAF).
* **Klasifikasi:** **True Positive (Medium-High Severity)**
* **Tindakan & Mitigasi:** Merekomendasikan *blacklisting* IP penyerang pada perangkat perimeter serta berkoordinasi dengan tim pengembang untuk memastikan validasi input menggunakan *parameterized queries*.

---

### 3. Endpoint Malware, Credential Dumping & Data Exfiltration Correlation
* **MITRE ATT&CK:** `T1059.001` (PowerShell), `T1486` (Data Encrypted for Impact), `T1003.001` (LSASS Memory), `T1048` (Exfiltration Over Alternative Protocol)
* **Tools:** Splunk Enterprise (Endpoint & Network Correlation)
* **Ringkasan Investigasi:** Mengkorelasikan serangkaian peringatan kritis pada satu *endpoint* (eksekusi skrip PowerShell mencurigakan, indikasi aktivitas *ransomware*, dan akses memori LSASS untuk pencurian kredensial) dengan upaya transfer data keluar (*outbound*) sebesar **810.62 MB** yang berhasil diblokir dalam rentang waktu 12 menit.
* **Klasifikasi:** **True Positive (Critical Severity)**
* **Tindakan & Mitigasi:** Melakukan isolasi *host* (*endpoint containment*) segera dari jaringan perusahaan untuk mencegah penyebaran lateral dan melakukan eskalasi prioritas tinggi ke **Tier 2 Incident Response**.

---

### 4. Network Packet Inspection (False Positive Validation)
* **MITRE ATT&CK:** *N/A (Benign Traffic)*
* **Tools:** Wireshark (PCAP Analysis)
* **Ringkasan Investigasi:** Memeriksa 149 paket jaringan (`HTTP GET` dan aliran *TCP stream*) dari peringatan anomali trafik keluar. Hasil inspeksi *payload* menunjukkan trafik tersebut merupakan proses pembaruan *Microsoft Office Click-to-Run* yang gagal terhubung ke server resmi.
* **Klasifikasi:** **False Positive (Benign)**
* **Tindakan & Mitigasi:** Menutup tiket peringatan dengan dokumentasi bukti PCAP tanpa melakukan eskalasi yang tidak perlu ke tim Tier 2.

---

## 📂 Daftar Dokumen di Repositori Ini
* `CV_Irman_Efendi_SOC_Analyst.pdf` — Curriculum Vitae terbaru.
* `Portofolio_SOC_Analyst_L1_Irman_Efendi.pdf` — Laporan lengkap beserta tangkapan layar (*screenshot*) hasil investigasi Splunk & Wireshark.
* `pengalaman kerja IT.pdf` — Rincian rekam jejak operasional IT & infrastruktur.
