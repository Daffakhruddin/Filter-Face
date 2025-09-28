# Face Mask Filter Desktop App

Aplikasi desktop berbasis **PyQt5 + OpenCV + MediaPipe** untuk menambahkan **masker PNG transparan** ke wajah secara real-time.
Mendukung **multi-face tracking**, **rotasi 3D (yaw, pitch, roll)**, **auto-scaling**, serta kontrol manual dengan slider.

Link Github: https://github.com/Daffakhruddin/Filter-Face
---

## Fitur

* Deteksi wajah otomatis menggunakan **MediaPipe**.
* Mendukung hingga **4 wajah** secara bersamaan.
* **Auto-scale** mask menyesuaikan ukuran wajah.
* **Pose estimation** sederhana: yaw, pitch, roll.
* **Rotasi pseudo-3D** dengan perspective warp.
* **Manual control sliders** (size, offset, roll, sensitivitas).
* **Smoothing adaptif** untuk mengurangi jitter.
* Antarmuka GUI interaktif dengan **PyQt5**.

---

## Requirements

* **Python 3.8 – 3.11** (direkomendasikan Python 3.10 atau 3.11).
* OS: Windows / Linux / macOS (butuh webcam).

### Dependencies

Aplikasi membutuhkan pustaka berikut:

* [PyQt5](https://pypi.org/project/PyQt5/)
* [OpenCV](https://pypi.org/project/opencv-python/)
* [MediaPipe](https://pypi.org/project/mediapipe/)
* [NumPy](https://pypi.org/project/numpy/)

---

## 🔧 Instalasi

Clone repositori (atau simpan file program):

install dependencies:

```bash
pip install -r requirements.txt
```

Atau manual:

```bash
pip install pyqt5 opencv-python mediapipe numpy
```

---

## Run Program

```bash
python filter.py
```

> Pastikan webcam aktif.
> Load file **mask PNG dengan transparansi** (alpha channel) menggunakan tombol **Load Mask**.

---

## `requirements.txt`

```
pyqt5
opencv-python
mediapipe
numpy
```

---

## Catatan

* Gunakan gambar **mask PNG transparan** (RGBA).
* Jika mask tidak punya alpha channel, program akan menambahkan alpha putih (full solid).
* Performa bisa berbeda tergantung resolusi webcam dan spesifikasi PC.
* Default deteksi wajah: **MediaPipe FaceDetection** (cepat, tapi sederhana).

---
