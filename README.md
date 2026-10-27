# 👁️ Menâzır — Alhazen Optical Architecture & Studio Display Precision Manager for macOS

<div align="center">
  <img src="https://caneser.com/images/menazir-icon.png" width="128" height="128" alt="Menâzır macOS Icon" />
  <br />
  <h2>Ultra-Lightweight, 100% Native, Zero-Flicker macOS Multi-Display & Optical Engine</h2>
  <p><b>Apple Silicon (M1/M2/M3/M4) & Intel (x86_64) Universal 2 Architecture with Zero Background RAM</b></p>
  <p>
    <a href="README.md"><b>English</b></a> • 
    <a href="README_TR.md"><b>🇹🇷 Türkçe</b></a>
  </p>
  <p>
    <a href="https://caneser.com/downloads/Menazir.dmg"><img src="https://img.shields.io/badge/Download_DMG-v1.5.0_Universal_2-E0C284?style=for-the-badge&logo=apple&logoColor=black" /></a>
    <img src="https://img.shields.io/badge/Apple_Notarized-Official_Security_Passed_✓-10B981?style=for-the-badge&logo=apple" />
  </p>
  <p>
    <img src="https://img.shields.io/badge/Platform-macOS_14+_Sonoma_|_Sequoia-000000?style=flat-square&logo=apple&logoColor=white" />
    <img src="https://img.shields.io/badge/Architecture-Universal_2_(arm64_+_x86__64)-8B5CF6?style=flat-square" />
    <img src="https://img.shields.io/badge/Swift-6.0_|_SwiftUI-F05138?style=flat-square&logo=swift&logoColor=white" />
    <img src="https://img.shields.io/badge/Memory_Idle-0.0_MB_(Zero_Daemons)-success?style=flat-square" />
    <a href="https://github.com/skorcu/kasif"><img src="https://img.shields.io/badge/Sister_App-Kâşif_(Instant_APFS_Search)-0284C7?style=flat-square&logo=apple&logoColor=white" /></a>
    <a href="https://github.com/skorcu/ihya"><img src="https://img.shields.io/badge/Sister_App-İhyâ_(System_Rejuvenation)-10B981?style=flat-square&logo=apple&logoColor=white" /></a>
    <img src="https://img.shields.io/badge/License-Freeware-blue?style=flat-square" />
  </p>
</div>

---

## 🏛️ An Optical Heritage Reborn: Inspired by Ibn al-Haytham

> *"A thousand years ago, Ibn al-Haytham (Alhazen) laid the foundation of modern optics in his magnum opus **Kitâb al-Manâzir** (The Book of Optics), proving that light emanates not from our eyes, but from the universe into our perception.*  
> *In homage to this timeless scientific heritage, **Sarkaç Adam** engineers **Menâzır** for Mac users worldwide: bridging the optical gap between external third-party displays and Apple's reference Retina panels through pure mathematical color science and zero-overhead Swift architecture."*

---

## ⚡ Why Menâzır? (Head-to-Head Comparison)

Conventional third-party display utilities often weigh 80MB–150MB, run persistent background tracking daemons, cause LCD FRC inversion flickering, and lock vital color-matching behind recurring subscription paywalls. **Menâzır** was crafted strictly in native **Swift, CoreGraphics, IOKit DDC, and AppKit**.

| Capability & Metric | 👁️ **Menâzır (v1.5.0 Universal 2)** | 📦 **Conventional Display Utilities** |
| :--- | :--- | :--- |
| **Binary Size** | **1.1 MB** (Universal 2 DMG) | **85 MB – 140 MB** (Bloated Bundles) |
| **Idle Background RAM** | **0.0 MB** (Menu Bar Only / No Daemons) | **120 MB – 250 MB** (Always-on Daemons) |
| **Apple Studio Display D65 Match** | **Automated TwinSync (Planckian Locus)** | **None / Manual Trial-and-Error** |
| **Zero-Flicker Hardware DDC/CI** | **`minLevel = 0.0` Anti-FRC Lock** | **FRC Dithering & Subpixel Shimmer** |
| **Apple iPad (Sidecar) Dimmer** | **Hardware-Independent Smart Overlay** | **Silent Failures / CoreGraphics 1001** |
| **HiDPI Retina Resolution Scaling** | **Built-in 5K Framebuffer Supersampling** | **Locked behind Paid Pro License** |
| **Typography Clarity (Font Smoothing)** | **Azamî Netlik (Level 3 Enforced)** | **Not Supported / Thin Blurry Text** |
| **Sub-Zero Night Dimming** | **Deep Dimming Below 0% Hardware Floor** | **Partially Available** |
| **Command Line Interface (CLI)** | **Built-in `menazir` Terminal Tool** | **Paid Extension or None** |
| **Security & Certification** | **Official Apple Developer ID & Notarized** | **Ad-hoc or Unsigned Warnings** |
| **Pricing** | **100% Free Public Gift** | **$20 – $40 Recurring License** |

---

## 🛠️ The 6 Core Optical Pillars

### 1. Studio Color & Light Matching (D65 P3 TwinSync)
Real-time color temperature synchronization with the Apple Studio Display. Maps the 6500K D65 reference white point onto external matte IPS panels using Planckian chromatic adaptation and gamma curve balancing. Turning it on brings the rich warmth and ink-like blacks of Apple's flagship display to your external monitor.

### 2. Zero-Flicker Hardware DDC/CI Control
Directly manages the monitor's physical LED backlight controller over the I2C/DDC bus rather than digitally compressing framebuffer dynamic range. Enforces a strict `minLevel = 0.0` baseline, eliminating the rapid micro-flickering and FRC inversion shimmering that plagues conventional Mac display tools.

### 3. Apple iPad (Sidecar) Smart Dimmer
macOS virtual displays (Sidecar / AirPlay) lack physical GPU CRTC lookup tables, causing standard CoreGraphics transfer calls to fail silently. Menâzır embeds an ultra-smooth, click-through, non-activating software dimming overlay directly on the iPad's `NSScreen`, enabling seamless multi-device brightness management.

### 4. HiDPI Retina Resolution & Scaling
Eliminates blurry text on 2K (2560x1440) and 4K external panels. Forces macOS WindowServer to render at a 5K virtual canvas and downscale via high-order lanczos filtering, delivering 1:1 razor-sharp font rendering.

### 5. Typography & Subpixel Font Clarity Engine
Apple Silicon macOS natively disables subpixel font antialiasing on non-Retina monitors. Menâzır dynamically locks `AppleFontSmoothing` to Level 3 (Azamî Netlik), preventing delicate letterforms from washing out on matte panels.

### 6. Sub-Zero Night Dimming
For darkroom editing and late-night research sessions where the monitor's minimum hardware backlight (0%) remains too piercing. Menâzır applies a secondary logarithmic software transfer multiplier, allowing comfortable illumination down to 5% of normal minimums.

---

## 💻 Terminal Command Line Interface (CLI)

Menâzır automatically registers a lightning-fast `menazir` binary into your `$PATH` (`~/.local/bin/menazir`):

```bash
# Print comprehensive optical status across all connected displays
menazir status

# Instantly match color temperature & brightness with Apple Studio Display
menazir match

# Set synchronized brightness across all displays (0-100)
menazir set 75

# Adjust external monitor contrast
menazir contrast 60

# Set Planckian color temperature (5000K - 7500K)
menazir kelvin 6500

# Control Apple iPad (Sidecar) brightness
menazir ipad 80

# Activate Sub-Zero deep night dimming (0-90)
menazir dim 40

# Revert to factory uncalibrated state
menazir off
```

---

## 🚀 Installation

1. Download the official release: **[Download Menazir.dmg](https://caneser.com/downloads/Menazir.dmg)**.
2. Open the DMG image and drag **Menâzır** into your **Applications** folder (or run the included 1-Click Installer script).
3. Launch **Menâzır**. It rests discretely in your macOS menu bar with zero configuration required.

---

## 🔒 Security, Integrity & Apple Gatekeeper Certification

- **Developer ID Application:** Signed with Apple Developer ID: `SAMLIOGLU KUYUMCULUK SANAYI VE TICARET ANONIM SIRKETI (P5GAL325ZG)`.
- **Apple Notarization Ticket:** Validated and officially stapled via Apple Notary Service (`xcrun notarytool`).
- **Gatekeeper Ready:** Runs seamlessly without "unidentified developer" or "damaged app" quarantine warnings on **macOS Sonoma (14.0+)**, **macOS Sequoia (15.0+)**, and future releases.
