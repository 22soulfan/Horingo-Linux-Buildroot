# 🌀 Horingo Linux: Alpha v0.1.0 (The Spark)

> *"Find your spark. Find your way."*

Horingo Linux is a custom-engineered, **64-bit Linux CLI** (Command Line Interface) built from the ground up using the **Buildroot** framework. It is designed for extreme portability and as a lightweight environment for Python-based automation.

---

## ✨ Features
*   **The Brain:** Linux Kernel v6.6.22 (x86_64 architecture).
*   **The Tools:** 
    *   **Python 3.11.8**: Verified math and scripting engine.
    *   **Nano**: Lightweight text editor for on-the-fly configuration.
    *   **BusyBox**: The standard "Swiss Army Knife" for utilities.
*   **The Login:** `root` (Auto-login enabled / No password required).

---

## 🧬 Buildroot DNA
- **Toolchain:** x86_64-buildroot-linux-gnu-gcc.
- **Init System:** BusyBox init (Optimized for speed).
- **Filesystem:** Squashfs (Read-Only by default).
- **Total Image Size:** ~101MB (Optimized for 700MB CD-ROM).

---

## 🚀 How to Run (The Rebirth)

Ensure you have the **Vitals** (`bzImage` and `rootfs.cpio`) downloaded to your device.

### 💻 Option A: Desktop (Windows/Linux/Mac)
1. Install [QEMU](https://www.qemu.org) and add it to your PATH.
2. Run the "Warp Speed" command:
```bash
qemu-system-x86_64 \
  -kernel bzImage \
  -initrd rootfs.cpio \
  -m 512M \
  -nographic \
  -append "console=ttyS0"
```
3. Run the engine (Wait 30-60s for the initial boot):
```bash
cd ~/storage/downloads
qemu-system-x86_64 -m 512M -kernel bzImage -initrd rootfs.cpio -nographic -append "console=ttyS0"
```

> Note: Instructions may vary. Type pwd and then ls to find your location.


### 📱 Option B: Mobile (Android via Termux)
1. Install [Termux](https://termux.dev) (F-Droid version recommended).
2. Set up the environment and install the x86_64 "Projector":
```bash
pkg update && pkg upgrade
pkg install qemu-system-x86-64-headless
termux-setup-storage
