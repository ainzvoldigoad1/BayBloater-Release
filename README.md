# BayBloater

**Advanced System Application Manager for Android**

BayBloater is a root-level application manager designed for advanced Android users. It provides low-level control over the Android system package manager, allowing for the manipulation and removal of both user-installed and OEM-integrated system applications.

---

## Key Capabilities

### System App Heuristics
BayBloater implements comprehensive package name heuristics to accurately identify system applications, including deep integration with specific OEM components across major manufacturers (e.g., Xiaomi, Samsung, Oppo, Vivo, OnePlus, and Qualcomm bases).

### Core Administration Tools
Provides direct access to critical package management commands:
1. **Launch Application:** Execute standard intent to open the application.
2. **Application Settings:** Navigate to the native Android App Info interface.
3. **State Management:** Disable or enable packages using `pm disable-user` without data loss.
4. **Data Wipe:** Clear local user storage corresponding to the application using `pm clear`.
5. **Process Termination:** Force stop the application process via `am force-stop`.
6. **Cache Clearance:** Remove temporary cache directories directly via shell commands.
7. **APK Extraction:** Copy the base `.apk` file to local storage for backup or analysis.
8. **Identifier Copy:** Copy the package name for scripting or external reference.

### Uninstallation Workflow
A multi-stage process designed to handle removals safely:
- **User Applications:** Standard removal followed by residual data and cache clearance.
- **System Applications:** Advanced removal involving partition remounting, package disabling, and physical deletion of the application directory via root shell.
- **Metadata Archival:** Automatic backup of application metadata to facilitate future restoration.

### Global Operations
- **Storage Metrics:** Real-time calculation of total application size and package count.
- **Data Export:** Generate a text-based inventory of all installed applications.
- **Sorting Mechanisms:** Organize packages by Name, File Size, Installation Date, or Update Date.
- **Power Operations:** Execute system restarts, zygote soft reboots, recovery boots, and complete Dalvik cache erasure.

---

## System Requirements
- **Root Permissions:** Magisk, KernelSU, or SuperSU is strictly required. Non-rooted environments are not supported.
- **Operating System:** Android 7.0 (API Level 24) or higher.

## Installation Instructions
1. Navigate to the [Releases](https://github.com/ainzvoldigoad1/BayBloater-Release/releases) section.
2. Download the latest `BayBloater-vX.X.X.apk`.
3. Install the application on the target Android device.
4. Grant Superuser permissions when requested upon initial launch.

## Disclaimer
Modifying core system applications carries inherent risks. Incorrect uninstallation of critical Android frameworks or OEM services may result in bootloops, data loss, or systemic instability. BayBloater includes confirmation safeguards, but usage is entirely at the user's discretion and responsibility. Ensure comprehensive system backups are maintained before executing deep debloat operations.
