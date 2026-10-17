<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=200&section=header&text=Game%20Gesture%20Control&fontColor=ffffff&fontSize=46&fontAlignY=38&desc=Main%20game%20cukup%20dengan%20gerakan%20tangan&descAlignY=60&descSize=18" alt="Game Gesture Control" width="100%">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&pause=1200&color=38BDF8&center=true&vCenter=true&width=640&lines=Kontrol+game+tanpa+keyboard;Deteksi+tangan+real-time+lewat+webcam;Python+%2B+MediaPipe+%2B+OpenCV)](https://youtu.be/nodM_wCaihw)

![Python](https://img.shields.io/badge/Python-3.10.10-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=for-the-badge&logo=google&logoColor=white)
![Status](https://img.shields.io/badge/Status-Aktif-22C55E?style=for-the-badge)

<a href="#demo"><img src="https://api.iconify.design/lucide/video.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#demo">Demo</a> &nbsp;&middot;&nbsp;
<a href="#fitur"><img src="https://api.iconify.design/lucide/sparkles.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#fitur">Fitur</a> &nbsp;&middot;&nbsp;
<a href="#cara-kerja"><img src="https://api.iconify.design/lucide/workflow.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#cara-kerja">Cara Kerja</a> &nbsp;&middot;&nbsp;
<a href="#instalasi"><img src="https://api.iconify.design/lucide/download.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#instalasi">Instalasi</a> &nbsp;&middot;&nbsp;
<a href="#troubleshooting"><img src="https://api.iconify.design/lucide/life-buoy.svg?color=%2338bdf8" width="16" alt=""></a> <a href="#troubleshooting">Troubleshooting</a>

</div>

---

## Demo

Tangan jadi controller. Webcam menangkap gerakan, program menerjemahkannya menjadi input game secara langsung.

<div align="center">

[![Tonton demo di YouTube](https://img.youtube.com/vi/nodM_wCaihw/maxresdefault.jpg)](https://youtu.be/nodM_wCaihw)

<a href="https://youtu.be/nodM_wCaihw"><img src="https://api.iconify.design/lucide/circle-play.svg?color=%232563eb" width="18" align="center" alt=""></a>&nbsp;<a href="https://youtu.be/nodM_wCaihw"><b>Tonton demo lengkap di YouTube</b></a>

</div>

---

## Fitur

| Fitur | Keterangan |
|---|---|
| <img src="https://api.iconify.design/lucide/hand.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Deteksi tangan** | Memakai MediaPipe untuk mengenali posisi tangan dan jari |
| <img src="https://api.iconify.design/lucide/gamepad-2.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Kontrol real-time** | Gerakan langsung diterjemahkan menjadi input game tanpa jeda yang terasa |
| <img src="https://api.iconify.design/lucide/zap.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Respons cepat** | Pemrosesan frame ringan, cukup untuk dijalankan di komputer biasa |
| <img src="https://api.iconify.design/lucide/laptop.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Berjalan lokal** | Tidak membutuhkan server atau koneksi internet saat digunakan |
| <img src="https://api.iconify.design/lucide/camera.svg?color=%232563eb" width="20" align="center" alt=""> &nbsp;**Cukup webcam** | Tanpa sensor atau perangkat tambahan |

---

## Cara Kerja

```mermaid
flowchart LR
    A[Webcam] --> B[OpenCV<br/>ambil frame]
    B --> C[MediaPipe<br/>deteksi tangan]
    C --> D[cvzone<br/>baca posisi jari]
    D --> E[Logika gesture]
    E --> F[PyAutoGUI<br/>kirim input]
    F --> G[Game]
```

| Tahap | Library | Peran |
|---|---|---|
| Tangkap video | `opencv-python` | Membaca frame dari webcam |
| Deteksi tangan | `mediapipe` | Mengenali tangan dan titik-titik landmark jari |
| Bantuan visi | `cvzone` | Mempermudah pembacaan posisi jari dan tampilan di layar |
| Kirim input | `pyautogui` | Mensimulasikan input keyboard atau mouse ke game |

---

## Persyaratan

| | Kebutuhan |
|---|---|
| <img src="https://api.iconify.design/lucide/terminal.svg?color=%232563eb" width="20" align="center" alt=""> | **Python 3.10.10** |
| <img src="https://api.iconify.design/lucide/camera.svg?color=%232563eb" width="20" align="center" alt=""> | **Webcam** yang berfungsi |
| <img src="https://api.iconify.design/lucide/lightbulb.svg?color=%232563eb" width="20" align="center" alt=""> | Pencahayaan ruangan yang cukup agar tangan terdeteksi stabil |

---

## Instalasi

**1. Clone repository**

```bash
git clone https://github.com/USERNAME/NAMA-REPO.git
cd NAMA-REPO
```

**2. Buat virtual environment (disarankan)**

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

## Menjalankan

```bash
python main.py
```

1. Pastikan webcam aktif dan tangan terlihat jelas di kamera
2. Buka game yang ingin dikontrol dan biarkan jendelanya tetap aktif
3. Mulai gerakkan tangan

Untuk berhenti, tutup jendela kamera atau tekan `Ctrl + C` di terminal.

---

## Troubleshooting

<details>
<summary><img src="https://api.iconify.design/lucide/camera-off.svg?color=%232563eb" width="18" align="center" alt="">&nbsp; <b>Kamera tidak terbaca atau layar hitam</b></summary>

<br>

- Tutup aplikasi lain yang sedang memakai webcam (Zoom, Meet, OBS, dan sejenisnya)
- Jika ada lebih dari satu kamera, coba ganti indeks kamera di kode, misalnya dari `0` ke `1`
- Periksa izin kamera di pengaturan privasi sistem operasi

</details>

<details>
<summary><img src="https://api.iconify.design/lucide/hand.svg?color=%232563eb" width="18" align="center" alt="">&nbsp; <b>Tangan sering tidak terdeteksi</b></summary>

<br>

- Perbaiki pencahayaan dan hindari cahaya kuat dari belakang tangan
- Gunakan latar yang tidak terlalu ramai
- Jaga jarak tangan ke kamera sekitar satu lengan

</details>

<details>
<summary><img src="https://api.iconify.design/lucide/triangle-alert.svg?color=%232563eb" width="18" align="center" alt="">&nbsp; <b>Error saat instalasi library</b></summary>

<br>

- Pastikan versi Python yang dipakai **3.10.10**, karena library seperti MediaPipe sensitif terhadap versi Python
- Jalankan `python --version` untuk memastikan
- Jika `opencv-python` dan `opencv-contrib-python` bentrok, uninstall keduanya lalu install ulang salah satunya saja

</details>

<details>
<summary><img src="https://api.iconify.design/lucide/mouse-pointer-click.svg?color=%232563eb" width="18" align="center" alt="">&nbsp; <b>Mouse berhenti merespons atau muncul FailSafeException</b></summary>

<br>

PyAutoGUI memiliki fitur pengaman: jika kursor digerakkan ke pojok kiri atas layar, program akan dihentikan. Ini perilaku normal, bukan bug.

</details>

---

## Kontribusi

Ide, saran, dan laporan bug dipersilakan lewat **Issues**. Untuk perubahan kode, silakan buka **Pull Request** dan jelaskan perubahan yang dibuat.

---

<div align="center">

Dibuat oleh **Hary Mukti Ramdhani** &nbsp;&middot;&nbsp; [@HaryMuktiRamdhani](https://github.com/HaryMuktiRamdhani)

Jika project ini bermanfaat, beri bintang pada repository ini.

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=100&section=footer" alt="" width="100%">

</div>
