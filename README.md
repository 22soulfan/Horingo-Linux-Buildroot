# 🌀 Horingo Linux: Alpha v0.1.0 (The Spark)

> *"Find your spark. Find your way."*

Horingo Linux is a custom-engineered, **64-bit Linux CLI** (Command Line Interface) built from the ground up using the **Buildroot** framework. It is designed for extreme portability and as a lightweight environment for Python-based automation.

> NOTE TO ALL USERS: I have three accounts: 22soulfan, gabexalt0928, and hirohamada2014. I (22soulfan) forked their repos since they are mine. Here, I forked Horingo Linux, a distro based on Buildroot.
> DISCLAIMER: Horingo Linux is in development. Stay tuned.
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

> NOTE: Instructions, ISO version, and anything else may vary.
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



### 📱 Option B: Mobile (Android via Termux)
1. Install [Termux](https://termux.dev) (F-Droid version recommended).
2. Set up the environment and install the x86_64 "Projector":
```bash
pkg update && pkg upgrade
pkg install qemu-system-x86-64-headless
termux-setup-storage
```

### 📺 Option C: Mobile Graphics (via Limbo x86 Emulator)
If you prefer a graphical BIOS-style boot on Android, use the **Limbo PC Emulator**:

1. **Setup the Machine**:
   - **Architecture**: `x86_64`
   - **Machine Type**: `pc`
   - **CPU Model**: `qemu64`
   - **CPU Cores**: `1` or `2`
   - **RAM**: `512MB`
2. **Mount the Soul**:
   - **Removable Storage**: Check **CDROM**.
   - **Image**: Select your `Horingo-i386-Alpha.iso` (or `rootfs.iso9660`).
3. **Graphics Interface**:
   - **VGA Display**: `std`
   - **User Interface**: `SDL`
4. **Boot**: Press the **Play** button to see the SeaBIOS and the Horingo login prompt.

---

## ⚖️ License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for the full legal text.



