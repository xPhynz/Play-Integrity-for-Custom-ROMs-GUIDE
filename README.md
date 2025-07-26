More guides here: [MyClub-Blog](https://in-myclub.blogspot.com/)

# Guide to Achieving Full Play Integrity on Custom ROMs

This repository provides a detailed guide to achieving full Play Integrity verification [Basic, Device, and Strong] on devices running a Custom ROM. It is common for Custom ROMs not to meet all `MEETS_INTEGRITY` requirements, which can limit the functionality of certain applications, especially banking apps. This guide is designed to help you overcome these limitations.

---

## 1. Prior Considerations and Requirements

* **Rooted Device:** It is essential that your Android device is rooted.
* **Root Manager:** The use of [**KernelSU** or **KernelSU next**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) is strongly recommended instead of Magisk. Magisk is more prone to detection by applications that verify system integrity, which can cause issues with sensitive services like banking applications.
* **Kernel Compatibility:** Please note that Custom ROM developers often optimize their ROMs for a specific kernel. Installing a different kernel than the pre-established one could lead to instabilities or operational problems. It is advisable to consult the ROM's support group to verify kernel compatibility and, if necessary, look for a KernelSU version that is compatible with the recommended kernel.
* **Integrity Verification:** To check your current Play Integrity status, you can install the [**"INTEGRITY CHECKER"**](https://play.google.com/store/apps/details?id=gr.nikolasspyr.integritycheck).

---

## 2. Initial Installation Process

Follow the steps below to set up the necessary modules:

1.  **Install KernelSU:** Download and install the [**KernelSU** or **KernelSU Next**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) application.
2.  **Modules:**
    * Open the KernelSU application.
    * Install the [**[Tricky-Store]**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) module.
    * Install the [**[YuriKey]**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) module.
    * Install the [**[Zygisk-Next]**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) module.
3.  **Reboot Device:** Once all modules are installed, reboot your device.

---

## 3. Yuri Keybox Manager Config

After rebooting, proceed with the Yuri Keybox configuration:

1.  **Install KsuWebUI:** Install the [**[KsuWebUI]**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide).
2.  **Access Yuri Keybox Manager:** Open the KsuWebUI apk and access the **[Yuri Keybox Manager]** section.
3.  **Security Configuration:**
    * Within Yuri Keybox Manager, navigate to "Menu" and select the following options to configure them:
        * Set Up Yuri Keybox
        * Set Up Target.txt
        * Set Up Security Patch
        * Set Up verified Boothash
    * Avoid modifying any other settings in this section.
4.  **Reboot Device:** Exit the [**[KsuWebUI]**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) application and reboot your device again.

After these steps, when checking with the INTEGRITY CHECKER, you should observe that your device has passed two of the three integrity verifications.

---

## 4. Obtaining the Third Integrity Verification

To achieve the third and final integrity verification, do the following:

1.  **Install PlayIntegrityFix:** Install the **[PlayIntegrityFix]** module.
2.  **KsuWebUI Config:**
    * Reopen the [**[KsuWebUI]**](https://github.com/xPhynz/Play-Integrity-for-Custom-ROMs-GUIDE/releases/tag/guide) application.
    * Access the **[Play Integrity Fix [INJECT]]** section.
    * Click on the "Advanced" option.
    * Select the **Spoof Provider** and **Spoof Build** options.
    * **Important Note:** To ensure the correct functioning of Google Wallet, it is necessary to **disable the Spoof Provider option** after completing these steps.

With these steps completed, your device should now pass all three Play Integrity verifications, allowing full use of applications that depend on this security feature.
