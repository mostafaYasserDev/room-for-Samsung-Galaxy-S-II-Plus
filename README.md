# 🚀 Samsung Galaxy S II Plus (GT-I9105P / s2vep) — ROM, Root & Upgrade Guide

<div align="center">

[![Android Version](https://img.shields.io/badge/Android-7.1.2%20Nougat-3DDC84?style=for-the-badge&logo=android&logoColor=white)](#)
[![Custom ROM](https://img.shields.io/badge/LineageOS-14.1-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](#)
[![Recovery](https://img.shields.io/badge/TWRP-3.0.2--0-008080?style=for-the-badge)](#)
[![Root](https://img.shields.io/badge/Root-SuperSU%20v2.82-red?style=for-the-badge)](#)
[![Platform Support](https://img.shields.io/badge/OS-Windows%20%7C%20Linux-0078D6?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/Guide-Bilingual%20AR%20%2F%20EN-blue?style=for-the-badge)](#)

### 🌐 اختر لغة الشرح / Choose Your Language:
**[🇸🇦 الشرح باللغة العربية (ويندوز ولينكس)](#-دليل-ترقية-وتفليش-وعمل-روت-لهاتف-samsung-galaxy-s-ii-plus-gt-i9105p)** &nbsp; | &nbsp; **[🇬🇧 English Guide (Windows & Linux)](#-complete-upgrade-custom-rom--root-guide-for-samsung-galaxy-s-ii-plus-gt-i9105p)**

</div>

---

## 🏷️ كلمات مفتاحية للبحث / Search Keywords
`Samsung Galaxy S II Plus` `GT-I9105P` `GT-I9105` `s2vep` `s2ve` `LineageOS 14.1` `Android 7.1.2 Nougat` `TWRP Recovery` `SuperSU Root` `OpenGApps` `Fix Google Play Store` `Custom ROM` `Odin Windows Flash` `Heimdall Linux` `Fedora Android Root` `رووت سامسونج اس 2 بلس` `تحديث اندرويد 7` `حل مشكلة متجر بلاي` `تفليش اودين ويندوز` `تثبيت ريكفري معدل`

---

## 🗂️ هيكل مجلدات المستودع / Repository Structure

```text
room-for-Samsung-Galaxy-S-II-Plus/
├── README.md                    # الدليل الشامل باللغتين العربية والإنجليزية (ويندوز ولينكس)
├── recovery/
│   ├── twrp-3.0.2-s2vep.img     # ريكفري TWRP المخصص لأنظمة لينكس عبر Heimdall (7.3 MB)
│   └── twrp-3.0.2-s2vep.tar.md5 # ريكفري TWRP المخصص لنظام ويندوز عبر Odin (7.3 MB)
├── root/
│   ├── SuperSU-v2.82.zip        # ملف تفليش الروت عبر الريكفري (6.6 MB)
│   └── supersu.apk              # تطبيق إدارة الروت SuperSU (6.0 MB)
├── tools-apk/
│   ├── AdAway.apk               # تطبيق حجب الإعلانات بالروت (5.5 MB)
│   └── TerminalEmulator.apk     # تطبيق الطرفية لاختبار الروت (553 KB)
└── rom/
    └── README.md                # روابط التحميل السحابية المباشرة للروم وحزمة جوجل
```

---

<br>

# 🇸🇦 دليل ترقية وتفليش وعمل روت لهاتف Samsung Galaxy S II Plus (GT-I9105P)

مرحباً بك! هذا المستودع يوثق ويحتوي على كافة الملفات والأدوات المنظمة اللازمة لإحياء هاتف **Samsung Galaxy S II Plus (GT-I9105P)**، وترقيته من نظام أندرويد 4.2.2 القديم جداً إلى نظام **Android 7.1.2 Nougat** المستقر عبر روم **LineageOS 14.1**، مع تثبيت متجر **Google Play Store** الحديث، وصلاحيات **Root** كاملة عبر **SuperSU**، وريكفري **TWRP 3.0.2**.

الشرح مفصل خطوة بخطوة لمستخدمي **ويندوز (Windows عبر Odin)** ومستخدمي **لينكس (Linux عبر Heimdall)**.

---

### 📋 1. بطاقة تعريف ومواصفات الجهاز (Device Specifications)

| الخاصية | القيمة الفنية |
| :--- | :--- |
| **اسم الهاتف** | Samsung Galaxy S II Plus (نسخة NFC) |
| **رقم الموديل (Model)** | `GT-I9105P` |
| **الاسم الكودي (Codename)** | `s2vep` / `s2vepxx` |
| **الشريحة والمعالج (Chipset)** | Broadcom Capri BCM28155 (ثنائي النواة 1.2 GHz) |
| **المعمارية (Architecture)** | `ARMv7-A` (`armeabi-v7a`) 32-bit |
| **الذاكرة العشوائية (RAM)** | 1.0 GB |
| **الذاكرة الداخلية (Storage)** | 8.0 GB (منها ~4.0 GB متاحة كـ `/data` و `/sdcard`) |
| **النظام الأصلي (Stock OS)** | Android 4.2.2 Jelly Bean (واجهة TouchWiz القديمة) |
| **النظام الجديد بعد الترقية** | **Android 7.1.2 Nougat** (روم **LineageOS 14.1**) |
| **حالة الروت (Root)** | **مروّت 100% (Rooted)** عبر `SuperSU v2.82` |
| **الريكفري (Recovery)** | **TWRP 3.0.2-0** دائم ومحمي |

---

### 🛑 2. المشكلات السابقة وسبب الترقية

1. **توقف متجر Google Play القديم:**  
   أوقفت شركة Google خوادم تسجيل الدخول لحسابات Google نهائياً عن جميع أنظمة أندرويد 2.3 وحتى 4.3 في أواخر 2021. هذا التحديث ينقل الهاتف إلى أندرويد 7.1.2 ويعيد تشغيل متجر Google Play الحديث بكفاءة وتشفير حديث.
2. **عدم دعم التطبيقات الحديثة:**  
   معظم التطبيقات أصبحت تتطلب أندرويد 5.0 أو أحدث. الترقية تسمح بتثبيت التطبيقات العصرية.
3. **التخلص من بطء واجهة سامسونج:**  
   روم LineageOS خفيف وسريع ونظيف وخالٍ من تطبيقات سامسونج الثقيلة المستهلكة للرام.

---

### ☁️ 3. روابط التحميل السحابية المباشرة (ROM & GApps Cloud Links)

نظراً للحجم الكبير لملفات الروم وحزمة جوجل (أكثر من 500 ميجابايت وتجاوز حدود GitHub)، يتم توفير روابط تحميل مباشرة وسريعة ودائمة بدلاً من رفعها داخل Git:

* **📱 روم LineageOS 14.1 (Android 7.1.2):**
  * **الحجم:** 318 MB | **MD5:** `ec1d031afd4b496b186b3fc5b6bbe095`
  * 🔗 [تحميل مباشر وسريع (Archive Mirror)](https://archive.org/download/afharchive_173_lineage-141-20200616-unofficial-i9105pzip/lineage-14.1-20200616-UNOFFICIAL-i9105p.zip)
* **🏪 متجر وخدمات جوجل OpenGApps 7.1 Pico:**
  * **الحجم:** 182 MB | **MD5:** `ff23028a1fcabbebec0bf3ccb133c0db`
  * 🔗 [تحميل مباشر وسريع (Archive Mirror)](https://archive.org/download/open_gapps-arm-7.1-pico-20220215/open_gapps-arm-7.1-pico-20220215.zip)

*(قم بتحميل الملفين وضعهما داخل مجلد `rom/` على جهازك)*

---

### ⚡ 4. خطوات التثبيت والتفليش خطوة بخطوة

#### 🎛️ الخطوة 1: تثبيت ريكفري TWRP 3.0.2

##### أولاً: إدخال الهاتف في وضع الداونلود (Download Mode)
1. أطفئ الجهاز بالكامل.
2. اضغط مع الاستمرار على الأزرار الثلاثة معاً: **[خفض الصوت Volume Down + زر القائمة Home + زر التشغيل Power]**.
3. عندما تظهر شاشة التحذير، اضغط على زر **رفع الصوت (Volume Up)** للدخول إلى وضع **ODIN MODE / Download Mode**.

---

##### الخيار (أ): التثبيت عبر نظام ويندوز (Windows باستخدام Odin)
1. قم بتثبيت [تعريفات سامسونج USB لويندوز (Samsung USB Driver)](https://developer.samsung.com/android-usb-driver) إذا لم تكن مثبتة.
2. قم بتحميل برنامج **Odin3** (مثل إصدار v3.10 أو v3.14) وشغله كمسؤول (Run as administrator).
3. وصل الهاتف بالكمبيوتر عبر كابل USB؛ ستلاحظ أن خانة `ID:COM` في Odin أصبحت مضيئة بلون أزرق/سماوي (دليل على التعرف على الجهاز).
4. في برنامج Odin:
   * اضغط على زر **AP** (أو **PDA** في الإصدارات الأقدم).
   * اختر ملف الريكفري الجاهز من المستودع: `recovery/twrp-3.0.2-s2vep.tar.md5`.
5. انتقل لتبويب **Options** في Odin وتأكد من **إلغاء تفعيل خيار `Auto Reboot`** (حتى لا يعيد الجهاز التشغيل للنظام القديم ويستبدل الريكفري بالريكفري الرسمي).
6. اضغط على زر **Start**. ستبدأ العملية وخلال 5 ثوانٍ ستظهر كلمة **PASS!** باللون الأخضر.
7. افصل كابل USB، واخلع بطارية الهاتف ثم أعد تركيبها (أو اضغط معاً على: `[رفع الصوت + Home + Power]` للدخول مباشرة لـ TWRP).

---

##### الخيار (ب): التثبيت عبر نظام لينكس (Linux باستخدام Heimdall)
1. تأكد من تثبيت حزمة `heimdall` على توزيعتك (`sudo dnf install heimdall` على Fedora أو `sudo apt install heimdall-flash` على Ubuntu/Debian).
2. وصل الهاتف بالكمبيوتر وهو في وضع الداونلود، ونفذ الأمر في الطرفية (Terminal):
   ```bash
   sudo heimdall flash --RECOVERY recovery/twrp-3.0.2-s2vep.img --no-reboot
   ```
3. بعد اكتمال التفليش بنجاح بنسبة 100%، ادخل فوراً للريكفري بالضغط على: **[رفع الصوت Volume Up + زر القائمة Home + زر التشغيل Power]**.

---

#### 📁 الخطوة 2: نقل ملفات التثبيت إلى الهاتف

عندما يفتح الهاتف شاشة **TWRP**، قم بتوصيله بالكمبيوتر عبر كابل USB. يتعرف نظام التشغيل تلقائياً على الهاتف عبر بروتوكول **MTP**:

* **على ويندوز (Windows):**
  * افتح مستكشف الملفات (File Explorer) ثم "This PC".
  * ستجد جهاز "Galaxy S II Plus" مفتوحاً كوحدة تخزين.
  * انسخ الملفات الثلاثة مباشرة إلى الذاكرة الداخلية للهاتف (`Internal Storage`):
    1. `rom/lineage-14.1.zip`
    2. `rom/gapps-7.1-pico.zip`
    3. `root/SuperSU-v2.82.zip`
  * *(أو يمكنك استخدام سطر الأوامر عبر `adb push` مثل لينكس أدناه).*

* **على لينكس (Linux):**
  * يمكنك استخدام نافذة الطرفية (Terminal):
    ```bash
    adb push rom/lineage-14.1.zip /sdcard/
    adb push rom/gapps-7.1-pico.zip /sdcard/
    adb push root/SuperSU-v2.82.zip /sdcard/
    ```

---

#### 🧹 الخطوة 3: المسح النظيف (Clean Wipe) في TWRP

لحماية الجهاز من أخطاء الإقلاع (Bootloop) الناتجة عن بقايا النظام القديم:
1. من واجهة TWRP الرئيسية اضغط على **Wipe** ← ثم **Advanced Wipe**.
2. حدد الأقسام التالية بعناية:
   *  **Dalvik / ART Cache**
   *  **System**
   *  **Cache**
   *  **Data**
   * ⚠️ *(تنبيه: لا تحدد Internal Storage إذا كانت الملفات منسوخة عليها)*.
3. اسحب الشريط بالأسفل **(Swipe to Wipe)**.

---

#### ⚡ الخطوة 4: التفليش (Flash) بالترتيب الإلزامي

من واجهة TWRP اضغط على **Install** وثبت الملفات بهذا الترتيب التتابعي:
1. اختر ملف الروم `lineage-14.1.zip` واسحب للتفليش (Swipe to confirm Flash).
2. اختر ملف خدمات ومتجر جوجل `gapps-7.1-pico.zip` واسحب للتفليش.
3. اختر ملف الروت `SuperSU-v2.82.zip` واسحب للتفليش.

---

#### 🚀 الخطوة 5: إعادة التشغيل والإقلاع الأول

* بعد انتهاء التفليش اضغط على زر **Reboot System**.
* يستغرق الإقلاع الأول ما بين **3 إلى 5 دقائق**؛ تظهر شاشة LineageOS وتتحرك بينما يقوم النظام ببناء الحزم والتخزين المؤقت عبر `dex2oat`.
* سيعمل الجهاز مباشرة على معالج الترحيب والإعداد (Setup Wizard) بنظام **Android 7.1.2**.

---

### 🔍 5. كيف تتأكد وتثبت أن الهاتف مروّت 100%؟

1. بعد إتمام إعداد الهاتف، ثبت تطبيق **Terminal Emulator** (الموجود في مجلد `tools-apk/` أو من متجر جوجل).
2. افتح التطبيق واكتب الأمر التالي ثم اضغط **Enter**:
   ```bash
   su
   ```
3. ستظهر رسالة منبثقة من تطبيق SuperSU تطلب صلاحيات الروت ← اضغط **منح (Grant)**.
4. ستتحول إشارة سطر الأوامر فوراً من `$` إلى **`#`** (علامة مستخدم الروت الخارق).
5. اكتب الأمر `id`؛ ستظهر النتيجة المؤكدة:
   ```text
   uid=0(root) gid=0(root) context=u:r:supersu:s0
   ```

---

### ⚙️ 6. اختصارات أزرار الهاتف الهامة (Hardware Keys)

* **وضع الريكفري (TWRP Recovery Mode):**  
  والهاتف مغلق: اضغط مطولاً على **[رفع الصوت + القائمة Home + التشغيل Power]**.
* **وضع الداونلود (Download / Odin Mode):**  
  والهاتف مغلق: اضغط مطولاً على **[خفض الصوت + القائمة Home + التشغيل Power]**، ثم زر **رفع الصوت**.

---

<br>
<hr>
<br>

# 🇬🇧 Complete Upgrade, Custom ROM & Root Guide for Samsung Galaxy S II Plus (GT-I9105P)

Welcome! This repository provides a complete, organized, and verified toolkit to upgrade and revive the **Samsung Galaxy S II Plus (GT-I9105P / s2vep)**. It elevates the device from its dead stock Android 4.2.2 Jelly Bean to a fast, responsive **Android 7.1.2 Nougat (LineageOS 14.1)** with a modern **Google Play Store**, full **SuperSU Root**, and permanent **TWRP 3.0.2** custom recovery.

Comprehensive instructions are provided for both **Windows (via Odin)** and **Linux (via Heimdall)**.

---

### 📋 1. Device Hardware & Software Specifications

| Specification | Technical Value |
| :--- | :--- |
| **Device Model** | Samsung Galaxy S II Plus (NFC Variant) |
| **Model Number** | `GT-I9105P` |
| **Device Codename** | `s2vep` / `s2vepxx` |
| **Chipset / SoC** | Broadcom Capri BCM28155 (Dual-Core 1.2 GHz ARM Cortex-A9) |
| **Architecture** | `ARMv7-A` (`armeabi-v7a`) 32-bit |
| **RAM** | 1.0 GB |
| **Internal Storage** | 8.0 GB (~4.0 GB user storage partition) |
| **Original Stock OS** | Android 4.2.2 Jelly Bean (TouchWiz UI) |
| **Upgraded OS** | **Android 7.1.2 Nougat** via **LineageOS 14.1** (Unofficial) |
| **Root Status** | **100% Rooted** via `SuperSU v2.82` |
| **Custom Recovery** | **TWRP 3.0.2-0** (Permanent & Protected) |

---

### 🛑 2. Why Upgrade? (Issues Solved)

1. **Dead Google Play Store on Stock Firmware:**  
   Google permanently terminated account login servers for Android 2.3–4.3 in late 2021. Updating to Android 7.1.2 updates cryptographic root certificates (TLS 1.2/1.3) and revives full Google Play Store support.
2. **Modern Application Compatibility:**  
   Most modern apps require Android 5.0+ or 7.0+. LineageOS 14.1 enables modern app compatibility.
3. **Bloatware Elimination & Performance:**  
   Replaces heavy Samsung TouchWiz services with a pure, lightweight AOSP-based ROM tuned for 1 GB RAM.

---

### ☁️ 3. Direct High-Speed Cloud Downloads (ROM & GApps)

Due to large file sizes (~500 MB combined), custom ROM packages are hosted via permanent cloud mirrors:

* **📱 LineageOS 14.1 ROM (Android 7.1.2):**
  * **Size:** 318 MB | **MD5:** `ec1d031afd4b496b186b3fc5b6bbe095`
  * 🔗 [Direct Fast Download (Archive Mirror)](https://archive.org/download/afharchive_173_lineage-141-20200616-unofficial-i9105pzip/lineage-14.1-20200616-UNOFFICIAL-i9105p.zip)
* **🏪 OpenGApps 7.1 Pico (Google Play Services & Store):**
  * **Size:** 182 MB | **MD5:** `ff23028a1fcabbebec0bf3ccb133c0db`
  * 🔗 [Direct Fast Download (Archive Mirror)](https://archive.org/download/open_gapps-arm-7.1-pico-20220215/open_gapps-arm-7.1-pico-20220215.zip)

*(Download both packages and place them inside the `rom/` directory)*

---

### ⚡ 4. Step-by-Step Installation Walkthrough

#### 🎛️ Step 1: Flash TWRP 3.0.2 Recovery

##### Enter Download Mode on Phone
1. Power off the phone completely.
2. Press and hold: **[Volume Down + Home + Power]**.
3. When the warning screen appears, press **Volume Up** to confirm and enter **ODIN / Download Mode**.

---

##### Option A: Flashing on Windows (via Odin)
1. Install [Samsung USB Drivers for Windows](https://developer.samsung.com/android-usb-driver).
2. Download and launch **Odin3** as Administrator.
3. Connect the phone to your Windows PC via USB cable. The `ID:COM` box in Odin turns blue/cyan, confirming detection.
4. In Odin:
   * Click on the **AP** button (or **PDA** on legacy Odin versions).
   * Select the pre-packaged recovery file: `recovery/twrp-3.0.2-s2vep.tar.md5`.
5. Under the **Options** tab in Odin, **uncheck `Auto Reboot`** (this ensures the device does not reboot into stock OS and overwrite TWRP).
6. Click **Start**. The flash finishes in ~5 seconds with a green **PASS!** banner.
7. Unplug the USB cable, pull the battery and reinsert it (or immediately press and hold: `[Volume Up + Home + Power]` to boot directly into TWRP).

---

##### Option B: Flashing on Linux (via Heimdall)
1. Install Heimdall package (`sudo dnf install heimdall` on Fedora, `sudo apt install heimdall-flash` on Debian/Ubuntu).
2. Connect the phone in Download Mode and run:
   ```bash
   sudo heimdall flash --RECOVERY recovery/twrp-3.0.2-s2vep.img --no-reboot
   ```
3. Once finished, boot immediately into TWRP by holding: **[Volume Up + Home + Power]**.

---

#### 📁 Step 2: Push Installation Files to Phone

When booted into TWRP recovery, connect the phone via USB. TWRP automatically presents the device over **MTP**:

* **On Windows:**
  * Open File Explorer → "This PC" → "Galaxy S II Plus".
  * Copy the three packages directly into the phone's internal storage (`/sdcard`):
    1. `rom/lineage-14.1.zip`
    2. `rom/gapps-7.1-pico.zip`
    3. `root/SuperSU-v2.82.zip`
* **On Linux:**
  * Push using ADB in terminal:
    ```bash
    adb push rom/lineage-14.1.zip /sdcard/
    adb push rom/gapps-7.1-pico.zip /sdcard/
    adb push root/SuperSU-v2.82.zip /sdcard/
    ```

---

#### 🧹 Step 3: Perform Clean Wipe in TWRP

1. In TWRP, tap **Wipe** → **Advanced Wipe**.
2. Check the following partitions:
   *  **Dalvik / ART Cache**
   *  **System**
   *  **Cache**
   *  **Data**
   * ⚠️ *(Do NOT check Internal Storage if you copied files there)*.
3. Swipe to Wipe.

---

#### ⚡ Step 4: Flash Files in Exact Sequence

From TWRP main menu, tap **Install** and flash in this sequence:
1. `lineage-14.1.zip` (ROM)
2. `gapps-7.1-pico.zip` (Google Apps)
3. `SuperSU-v2.82.zip` (Root)

---

#### 🚀 Step 5: Reboot & First Boot

* Tap **Reboot System**.
* The first boot takes **3 to 5 minutes** while `dex2oat` builds Dalvik/ART caches.
* Complete the initial LineageOS and Google account setup wizard.

---

### 🔍 5. Verifying Root Access

1. Open **Terminal Emulator** on the phone.
2. Run `su` and press Enter.
3. Tap **Grant** on the SuperSU popup dialog.
4. Shell prompt changes from `$` to `#`.
5. Run `id` to verify root privileges:
   ```text
   uid=0(root) gid=0(root) context=u:r:supersu:s0
   ```

---

### ⚙️ 6. Hardware Key Combinations

* **Recovery Mode (TWRP):** Power off → Hold **[Volume Up + Home + Power]**.
* **Download Mode (Odin/Heimdall):** Power off → Hold **[Volume Down + Home + Power]**, then press **Volume Up**.

---

<div align="center">

**Created & Documented by [mostafaYasserDev](https://github.com/mostafaYasserDev) — October 2026**

</div>
