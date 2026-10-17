<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=200&section=header&text=Game%20Gesture%20Control&fontColor=ffffff&fontSize=46&fontAlignY=38&desc=Main%20game%20cukup%20dengan%20gerakan%20tangan&descAlignY=60&descSize=18" alt="Game Gesture Control" width="100%">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=38BDF8&center=true&vCenter=true&width=640&lines=Kontrol+game+tanpa+keyboard;Deteksi+tangan+real-time+lewat+webcam;Python+%2B+MediaPipe+%2B+OpenCV)](https://youtu.be/nodM_wCaihw)

![Python](https://img.shields.io/badge/Python-3.10.10-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=for-the-badge&logo=google&logoColor=white)
![Status](https://img.shields.io/badge/Status-Aktif-22C55E?style=for-the-badge)

[**Tonton Demo**](#-demo) · [**Fitur**](#-fitur) · [**Cara Kerja**](#-cara-kerja) · [**Instalasi**](#-instalasi) · [**Troubleshooting**](#-troubleshooting)

</div>

---

## 🎥 Demo

Tangan jadi controller. Webcam menangkap gerakan, program menerjemahkannya jadi input game secara langsung.

<div align="center">

[![Tonton demo di YouTube](https://img.youtube.com/vi/nodM_wCaihw/maxresdefault.jpg)](https://youtu.be/nodM_wCaihw)

▶️ **Klik gambar di atas untuk menonton demo lengkap di YouTube**

</div>

---

## ✨ Fitur

| | Fitur | Keterangan |
|---|---|---|
| 🖐️ | **Deteksi tangan** | Memakai MediaPipe untuk mengenali posisi tangan dan jari |
| 🎮 | **Kontrol real-time** | Gerakan langsung diterjemahkan jadi input game tanpa jeda yang terasa |
| ⚡ | **Respons cepat** | Pemrosesan frame ringan, cukup untuk dijalankan di komputer biasa |
| 💻 | **Jalan lokal** | Tidak butuh server atau koneksi internet saat dipakai |
| 📷 | **Cukup webcam** | Tanpa sensor atau perangkat tambahan |

---

## 🧠 Cara Kerja

```mermaid
flowchart LR
    A[📷 Webcam] --> B[OpenCV<br/>ambil frame]
    B --> C[MediaPipe<br/>deteksi tangan]
    C --> D[cvzone<br/>baca posisi jari]
    D --> E[Logika gesture]
    E --> F[PyAutoGUI<br/>kirim input]
    F --> G[🎮 Game]
```

| Tahap | Library | Peran |
|---|---|---|
| Tangkap video | `opencv-python` | Membaca frame dari webcam |
| Deteksi tangan | `mediapipe` | Mengenali tangan dan titik-titik landmark jari |
| Bantuan visi | `cvzone` | Mempermudah pembacaan posisi jari dan tampilan di layar |
| Kirim input | `pyautogui` | Mensimulasikan input keyboard/mouse ke game |

---

## 🛠️ Persyaratan

- 🐍 **Python 3.10.10**
- 📷 **Webcam** yang berfungsi
- 💡 Ruangan dengan pencahayaan cukup supaya tangan terdeteksi stabil

---

## 📦 Instalasi

**1. Clone repository**

```bash
git clone https://github.com/USERNAME/NAMA-REPO.git
cd NAMA-REPO
```

**2. (Disarankan) Buat virtual environment**

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Linux / macOS
source venv/bin/activate
```

**3. Install library**

```bash
pip install opencv-python
pip install opencv-contrib-python
pip install mediapipe
pip install cvzone
pip install pyautogui
```

---

## ▶️ Menjalankan

```bash
python main.py
```

1. Pastikan webcam aktif dan tangan terlihat jelas di kamera
2. Buka game yang ingin dikontrol dan biarkan jendelanya aktif
3. Mulai gerakkan tangan

Untuk berhenti, tutup jendela kamera atau tekan `Ctrl + C` di terminal.

---

## 🧩 Troubleshooting

<details>
<summary><b>📷 Kamera tidak terbaca atau layar hitam</b></summary>

<br>

- Tutup aplikasi lain yang sedang memakai webcam (Zoom, Meet, OBS, dan sejenisnya)
- Jika ada lebih dari satu kamera, coba ganti indeks kamera di kode, misalnya dari `0` ke `1`
- Cek izin kamera di pengaturan privasi sistem operasi

</details>

<details>
<summary><b>🖐️ Tangan sering tidak terdeteksi</b></summary>

<br>

- Perbaiki pencahayaan, hindari cahaya kuat dari belakang tangan
- Gunakan latar yang tidak terlalu ramai
- Jaga jarak tangan ke kamera sekitar satu lengan

</details>

<details>
<summary><b>⚠️ Error saat instalasi library</b></summary>

<br>

- Pastikan versi Python yang dipakai **3.10.10**, karena library seperti MediaPipe sensitif terhadap versi Python
- Jalankan `python --version` untuk memastikan
- Jika `opencv-python` dan `opencv-contrib-python` bentrok, uninstall keduanya lalu install ulang salah satu saja

</details>

<details>
<summary><b>🖱️ Mouse berhenti merespons atau muncul FailSafeException</b></summary>

<br>

PyAutoGUI punya fitur pengaman: jika kursor digerakkan ke pojok kiri atas layar, program akan dihentikan. Ini perilaku normal, bukan bug.

</details>

---

## 🤝 Kontribusi

Ide, saran, dan laporan bug dipersilakan lewat **Issues**. Jika ingin mengubah kode, silakan buka **Pull Request** dan jelaskan perubahan yang kamu buat.

---

<div align="center">

Dibuat oleh **Hary Mukti Ramdhani** · [@HaryMuktiRamdhani](https://github.com/HaryMuktiRamdhani)

Kalau project ini membantu, kasih ⭐ ya!

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=100&section=footer" alt="" width="100%">

</div>
