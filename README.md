# ExcavatorSimVR - Simulator Ekskavator Virtual Reality

Aplikasi simulasi pengoperasian ekskavator Komatsu PC200 berbasis Virtual Reality untuk keperluan pelatihan operator alat berat.

## Informasi Proyek

| Item | Detail |
|------|--------|
| Game Engine | Unreal Engine 5.7.4 |
| Platform | Windows 64-bit (VR) |
| VR Runtime | OpenXR (SteamVR Compatible) |
| Input | 2x Controller ESP32 (Bluetooth) + x360ce |
| Model | Komatsu PC200 |

## Fitur Utama

- **3 Zona Pelatihan**
  - Zona A — Pelatihan navigasi ekskavator
  - Zona B — Pelatihan penggalian tanah (Voxel terrain)
  - Zona C — Pelatihan lanjutan
- **Kontrol realistis** menggunakan 2 joystick fisik berbasis ESP32
- **Sistem evaluasi** dengan penilaian performa otomatis (skor 0-100)
- **Sistem jeda (pause)** dengan opsi lanjutkan atau kembali ke menu
- **Inverse Kinematics** untuk animasi lengan ekskavator yang realistis

## Struktur Folder

```
ExcavatorSimVR/
├── Config/                  # Konfigurasi engine & input
├── Content/
│   ├── objek/
│   │   ├── Komatsu_Pc200/   # Model & Blueprint ekskavator utama
│   │   ├── Environtment/    # Objek lingkungan pelatihan
│   │   └── UI/              # Widget antarmuka (Menu, HUD, Evaluasi)
│   ├── MainMenu.umap        # Peta menu utama
│   └── Level_TrainingBasic.umap  # Peta pelatihan (Zona A/B/C)
├── Plugins/
│   └── VoxelFree/           # Plugin terrain untuk sistem penggalian
└── ExcavatorSimVR.uproject
```

## Download Build (.exe)

File build aplikasi terlalu besar untuk disimpan di GitHub. Silakan unduh dari Google Drive:

**[Download Build (Google Drive)](https://drive.google.com/drive/folders/1HwpxCdC6tYVvOtJvlL1dU9xXMajCgsGY?usp=sharing)**

## Kebutuhan Sistem

| Komponen | Minimum |
|----------|---------|
| OS | Windows 10/11 (64-bit) |
| CPU | AMD Ryzen 5 / Intel Core i5 Gen 10+ |
| RAM | 8 GB |
| GPU | NVIDIA GTX 1060 / AMD RX 580 |
| VR | Headset yang mendukung OpenXR |
| Lainnya | Bluetooth, x360ce, SteamVR |

## Cara Menjalankan

1. Unduh file build dari link Google Drive di atas.
2. Ekstrak file zip ke direktori yang diinginkan.
3. Nyalakan kedua controller ESP32 dan hubungkan via Bluetooth.
4. Jalankan **x360ce** untuk mapping controller.
5. Nyalakan VR headset dan pastikan SteamVR berjalan.
6. Jalankan **ExcavatorSimVR.exe**.

## Kontrol

**Controller Kursi (Lengan & Kabin):**
| Input | Fungsi |
|-------|--------|
| Analog Kiri X | Putar kabin |
| Analog Kiri Y | Gerakkan arm |
| Analog Kanan X | Gerakkan bucket |
| Analog Kanan Y | Gerakkan boom |
| L3 | Pause |
| R3 | Klik UI |

**Controller Meja (Track):**
| Input | Fungsi |
|-------|--------|
| L1 / L2 | Track kiri maju / mundur |
| R1 / R2 | Track kanan maju / mundur |
