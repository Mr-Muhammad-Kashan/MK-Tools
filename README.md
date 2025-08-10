<div align="center">

# ✨ MK-Tools | Windows-Edition ✨

<a href="https://mr-muhammad-kashan.github.io/MK-Tools.github.io/download.html" target="_blank">
  <img src="https://img.shields.io/badge/Download%20Latest-v1.0-9A4BFF?style=for-the-badge&logo=windows&logoColor=white" alt="Download Now">
</a>
<a href="https://github.com/Mr-Muhammad-Kashan/MK-Tools" target="_blank">
  <img src="https://img.shields.io/badge/View%20on-GitHub-23212E?style=for-the-badge&logo=github&logoColor=white" alt="View on GitHub">
</a>
<a href="https://mr-muhammad-kashan.github.io/Buy-Me-A-Coffee-Website/" target="_blank">
  <img src="https://img.shields.io/badge/Support%20This-Project-FFDD00?style=for-the-badge&logo=buymeacoffee&logoColor=black" alt="Support This Project">
</a>

**The definitive, military-grade Windows optimization suite. Unlock peak performance, enhance UI responsiveness, and take granular control of your system with a single, powerful, and beautifully designed tool.**

</div>

---

<div align="center">
  <img src="https://raw.githubusercontent.com/Mr-Muhammad-Kashan/MK-Tools/main/Gifs/Showcase.gif" alt="MK-Tools Application Showcase" width="900"/>
</div>

---

## 🚀 The Mission: Optimization for Everyone

For too long, deep system optimization has been a complex world reserved for power users and IT professionals. **MK-Tools** was created with a single, clear goal: **To empower everyone.**

Built on over a decade of hands-on experience with Windows internals and hardware, MK-Tools demystifies the process of tweaking your system. It's founded on the belief that powerful optimization capabilities should be **accessible, safe, and easy** for all users. This application gives you one-click control over your machine's performance, privacy, and responsiveness, transforming a daunting task into an effortless experience.

## 📋 Table of Contents
- [✨ Key Features](#-key-features)
  - [🚀 Performance Tweaks](#-performance-tweaks)
  - [🎨 UI & Responsiveness](#-ui--responsiveness)
  - [🛠️ Fix Windows](#️-fix-windows)
  - [🧹 Clean Cache](#-clean-cache)
  - [🏛️ Group Policy](#️-group-policy)
- [🏛️ Architectural Blueprint](#️-architectural-blueprint)
- [💻 Technology Stack](#-technology-stack)
- [🔧 Installation & Setup](#-installation--setup)
- [💡 How to Use](#-how-to-use)
- [💖 Support This Project](#-support-this-project)
- [📞 Contact](#-contact)

## ✨ Key Features

MK-Tools is organized into several powerful modules, each targeting a specific aspect of your Windows experience.

### 🚀 Performance Tweaks
Unleash your PC’s full potential by optimizing core system and hardware settings. Reduce CPU load, improve resource allocation, and enhance stability for gaming and professional applications.

| Feature                               | Description                                                              |
| ------------------------------------- | ------------------------------------------------------------------------- |
| **Disable Fast Startup** | Ensures a full, clean shutdown every time, improving long-term stability and hardware compatibility. |
| **Disable Compressed Memory** | Reduces background CPU usage on systems with 16GB+ RAM, preventing micro-stutters. |
| **Hardware-Accelerated GPU Scheduling** | Allows your GPU to manage its own VRAM, potentially reducing latency in games and creative apps. |
| **Prioritize Foreground Applications** | Allocates more CPU resources to your active application for a smoother, more responsive experience. |
| **Optimize SvcHost Splitting** | Forces services into separate processes on high-RAM systems, improving stability and making it easier to identify resource hogs. |

### 🎨 UI & Responsiveness
Customize the Windows user interface to make it faster, cleaner, and more efficient. Remove artificial delays and restore classic, functional UI elements.

| Feature                               | Description                                                              |
| ------------------------------------- | ------------------------------------------------------------------------- |
| **Enable Classic Right-Click Menu** | Restores the full Windows 10 context menu on Windows 11, removing the "Show more options" extra click. |
| **Instant Menu Display** | Removes the 400ms animation delay, making all context menus and drop-downs appear instantly. |
| **100% JPEG Wallpaper Quality** | Prevents Windows from compressing your desktop wallpaper, ensuring a pixel-perfect, crisp image. |
| **Disable Web Search in Start Menu** | Limits Start Menu searches to your local files and apps, improving privacy and search speed. |

### 🛠️ Fix Windows
A powerful diagnostic and repair center to ensure the integrity of your core operating system files.

| Feature                   | Description                                                              |
| ------------------------- | ------------------------------------------------------------------------ |
| **Scan (SFC)** | Runs the System File Checker (`sfc /scannow`) to find and repair corrupted protected system files automatically. |
| **Advanced Scan (DISM)** | Runs the Deployment Image Servicing and Management tool (`DISM /Online /Cleanup-Image /RestoreHealth`) to repair the underlying component store that SFC relies on. This is the ultimate tool for fixing deep system corruption. |

### 🧹 Clean Cache
Reclaim gigabytes of disk space and improve system performance by safely clearing out temporary and cached files from various system locations.

| Feature                               | Description                                                              |
| ------------------------------------- | ------------------------------------------------------------------------- |
| **User & System Temp Folders** | Clears temporary files created by applications and the Windows OS.         |
| **Windows Update Cache** | Deletes old, downloaded update installation files that are no longer needed. |
| **Explorer Thumbnail & Icon Cache** | Resets the cache for file thumbnails and icons to fix visual glitches.     |
| **WinSxS Component Store** | Cleans up outdated and superseded system components to free up significant space. |
| **Windows Prefetch** | Clears files used by Windows to speed up application launching.            |

### 🏛️ Group Policy
For users of Windows Pro editions, this module provides a one-click solution to apply a curated set of Local Group Policies designed to maximize privacy, security, and performance.

| Feature                        | Description                                                              |
| ------------------------------ | ------------------------------------------------------------------------ |
| **Apply Optimized Policies** | Deploys policies that disable telemetry, block Windows Copilot and Recall, prevent bloatware, and restrict web search to create a cleaner, more private, and more efficient system. |
| **Reset Policies to Default** | Performs a forensically clean reset of all Local Group Policies, returning your system to the standard Windows default state. |

---

## 🏛️ Architectural Blueprint

MK-Tools is engineered from the ground up for stability, performance, and security. It operates as a single, self-contained Python application, ensuring all logic and assets are perfectly synchronized.

-   **Entry Point**: The application begins with the `PrivilegeManager`, which uses the standard Windows UAC prompt to ensure the necessary administrative rights for system modification.
-   **Core Engine**: The main `App` class orchestrates all components. It launches a non-blocking, animated `SplashScreen` while running asynchronous pre-flight checks in the background. This ensures the main UI is only revealed once all system states have been audited, providing an instantaneous, ready-to-use experience.
-   **UI Framework**: Built on **CustomTkinter**, providing a modern, themeable, and high-performance graphical interface.
-   **DPI & Scaling**: The `ScreenManager` and `Theme` engine work in tandem to provide full DPI awareness. The UI and all fonts are dynamically scaled based on the system's display settings, ensuring a flawless visual experience from 720p to 4K.
-   **Auditory Feedback**: A singleton `SoundManager`, powered by **Pygame**, provides a rich, non-blocking auditory experience for all user interactions, with a global toggle for user control.
-   **Tweak Logic**: Each system tweak is managed by a dedicated, decoupled backend controller class. These controllers interface directly with the Windows Registry and execute PowerShell commands, containing no UI code and ensuring a perfect separation of concerns.
-   **Process Integrity**: All long-running operations (e.g., `sfc /scannow`) are executed in separate processes. The main `App` class maintains a central process registry, guaranteeing that all child processes are gracefully terminated upon application shutdown, leaving a zero-footprint exit.

---

## 💻 Technology Stack

MK-Tools is built with a curated selection of powerful and reliable technologies.

| Category      | Technology / Library                                                                                                                                                                                                                          |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUI Framework** | ![CustomTkinter](https://img.shields.io/badge/CustomTkinter-1.1.0-3A79F7?style=flat-square)                                                                                                                                                              |
| **Audio** | ![Pygame](https://img.shields.io/badge/Pygame-2.5.2-6A95AE?style=flat-square)                                                                                                                                                                  |
| **System Interop**| ![pywin32](https://img.shields.io/badge/pywin32-306-00529B?style=flat-square) ![psutil](https://img.shields.io/badge/psutil-5.9.8-E44D26?style=flat-square)                                                                                         |
| **Image & Graphics** | ![Pillow](https://img.shields.io/badge/Pillow-10.3.0-FFC300?style=flat-square) ![cairosvg](https://img.shields.io/badge/cairosvg-2.7.1-4A148C?style=flat-square)                                                                                       |
| **Networking** | ![requests](https://img.shields.io/badge/requests-2.31.0-222222?style=flat-square)                                                                                                                                                            |
| **Language** | ![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white)                                                                                                                                     |
| **OS** | ![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?style=flat-square&logo=windows&logoColor=white)                                                                                                                            |

---

## 🔧 Installation & Setup

Getting started with MK-Tools is designed to be simple and secure.

1.  **Download**: Head to the [**Official Download Page**](https://mr-muhammad-kashan.github.io/MK-Tools.github.io/download.html) and grab the latest release.
2.  **Unzip**: Extract the contents of the downloaded `.zip` file to a folder of your choice (e.g., `C:\Program Files\MK-Tools`).
3.  **Run**: Double-click `main.exe` to launch the application.

**System Requirements:**
* **Operating System**: Windows 10 or Windows 11
* **Permissions**: **Administrator rights are required**. The application will automatically prompt you for elevation via the standard Windows UAC dialog upon launch.

---

## 💡 How to Use

1.  **Launch the Application**: When you run `main.exe`, you will first see a User Account Control (UAC) prompt. Click "Yes" to grant the necessary administrative privileges.
2.  **Splash Screen**: An animated splash screen will appear while MK-Tools performs essential pre-flight checks on your system in the background.
3.  **Dashboard**: Once loaded, you will be greeted by the main dashboard. From here, you can use the **Navigation Rail** on the left to access all the different optimization modules.
4.  **Apply Tweaks**: Navigate to your desired section, read the description for each tweak, and use the intuitive buttons to apply or revert changes.
    > **Note**: Many tweaks require a system restart to take full effect. You will be notified when this is necessary.

---

## 💖 Support This Project

MK-Tools is a passion project developed with the goal of making high-end PC optimization accessible to everyone. If you find this tool useful and want to support its continued development, please consider:

<div align="center" style="margin-top: 20px; margin-bottom: 20px;">
  <a href="https://mr-muhammad-kashan.github.io/Buy-Me-A-Coffee-Website/" target="_blank">
    <img src="https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" alt="Buy Me a Coffee">
  </a>
</div>

Your support helps cover development costs and fuels the creation of new features. Thank you!

---

## 📞 Contact

Have questions, suggestions, or feedback? Feel free to reach out!

-   **LinkedIn**: [linkedin.com/in/muhammad-kashan-tariq](https://www.linkedin.com/in/muhammad-kashan-tariq)
-   **GitHub**: [github.com/Mr-Muhammad-Kashan](https://github.com/Mr-Muhammad-Kashan)
-   **Email**: [m.kashan.exe@gmail.com](mailto:m.kashan.exe@gmail.com)

---
<div align="center">
  <em>Engineered with precision by Mohammed Kashan Tariq</em>
</div>
