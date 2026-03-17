


<img width="4100" height="2304" alt="Picsart_26-03-17_11-54-19-738" src="https://github.com/user-attachments/assets/5a57fe6a-3e04-4d91-9b9e-a95ac342848f" />

# Lunaris-AOSP-3.8-QPR2-Unofficial-for-spaced

## 🚀 Performance & System
* **Power Management:** Reworked `PowerHint` implementation and migrated to policy-based power nodes.
* **CPU Tuning:** Optimized `schedutil` up/down rate limits for improved frequency scaling.
* **Memory Management:** * Increased zRAM to **70%** of total RAM.
    * Adjusted `swappiness` to **70** and disabled zRAM writeback.
    * Updated Low Memory Killer (LMK) properties for better multitasking.
* **Graphics & Rendering:** * Allocated **4 buffers** to SurfaceFlinger for smoother frame delivery.
    * Increased SurfaceFlinger region sampling frequency.
    * Imported Motorola phase offsets; dropped legacy phase durations and multi-threshold tuning.
* **Cleanup:** Removed MediaTek gauge, legacy power properties, `mmstat` tracing, and the compat namespace.
* **Toolchain:** Overrode kernel BPF version and removed kernel Clang version pinning.

## 🎮 Display & UI
* **High Refresh Rate:** Enabled **120Hz support** for games.
* **Animation Refinement:** * Simplified activity open/close transitions.
    * Replaced standard accelerate interpolator with **linear** for consistent motion.
    * Dynamic animation scaling based on screen percentage.
* **Visual Enhancements:** * Reduced blur radius in overlays and added support for rounded corners.
    * Adjusted status bar start/end paddings for better alignment.
* **Refresh Rate Logic:** Reverted Smooth Display in favor of explicit min/peak refresh rate toggles.

## 🔋 Memory & Runtime
* **ART/Dalvik:** Reverted dynamic heap overrides and grouped property initializations.
* **Legacy Cleanup:** Removed Android 11 `libinit` adaptations and cleaned up stale includes.
* **Core System:** Migrated `system/core/base` changes for better upstream compatibility.

## 📡 Connectivity & Audio
* **NFC:** Modernized stack by switching to **AIDL NXP NFC HAL** and refining the configuration.
* **Audio:** * Improved mute duration handling.
    * Stripped unused codecs and MTK encoder performance hints.
    * Disabled Audio HAL PCM dumping and dropped Dolby Atmos for a leaner audio path.

## 🧩 Sensors & HAL
* **Sensor Stack:** Added **Dynamic Sensors HAL** support.
* **Compatibility:** Linked MTK sensor multihal with `libbase` shim and patched blobs to utilize `libtinyxml2-v34`.

## 🔐 Security & Filesystem
* **Security:** Disabled Factory Reset Protection (FRP).
* **Filesystem:** Implemented `metadata_csum` for the `/metadata` partition.
* **Cleanup:** Purged duplicate blobs and redundant vendor framework matrices.

## 🧱 Build System & Fixes
* **Blueprint Migration:** Converted `rootdir` to Blueprint for modern build standards.
* **Maintenance:** Renamed Lineage overlays and removed unused/duplicate configurations.
* **Bug Fix:** Resolved permission issues for `opluserserve1`.

# 🎧 Added Sony Dolby


## HUGES THANKS TO @HELLINFIX FOR TREES AND HELPING 🫡
