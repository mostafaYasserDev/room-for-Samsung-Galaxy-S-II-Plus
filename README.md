# 🚀 Samsung Galaxy S II Plus (GT-I9105P / s2vep) — ROM, Root & Upgrade Guide

<div align="center">

[![Android Version](https://img.shields.io/badge/Android-7.1.2%20Nougat-3DDC84?style=for-the-badge&logo=android&logoColor=white)](#)
[![Custom ROM](https://img.shields.io/badge/LineageOS-14.1-167C80?style=for-the-badge&logo=lineageos&logoColor=white)](#)
[![Recovery](https://img.shields.io/badge/TWRP-3.0.2--0-008080?style=for-the-badge)](#)
[![Root](https://img.shields.io/badge/Root-SuperSU%20v2.82-red?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/Guide-Bilingual%20AR%20%2F%20EN-blue?style=for-the-badge)](#)

### 🌐 اختر لغة الشرح / Choose Your Language:
**[🇸🇦 الشرح باللغة العربية](#-دليل-ترقية-وتفليش-وعمل-روت-لهاتف-samsung-galaxy-s-ii-plus-gt-i9105p)** &nbsp; | &nbsp; **[🇬🇧 English Guide](#-complete-upgrade-custom-rom--root-guide-for-samsung-galaxy-s-ii-plus-gt-i9105p)**

</div>

---

## 🏷️ كلمات مفتاحية للبحث / Search Keywords
`Samsung Galaxy S II Plus` `GT-I9105P` `GT-I9105` `s2vep` `s2ve` `LineageOS 14.1` `Android 7.1.2 Nougat` `TWRP Recovery` `SuperSU Root` `OpenGApps` `Fix Google Play Store` `Custom ROM` `Heimdall Linux` `Fedora Android Root` `رووت سامسونج اس 2 بلس` `تحديث اندرويد 7` `حل مشكلة متجر بلاي`

---

## 🗂️ هيكل مجلدات المستودع / Repository Structure

```text
room-for-Samsung-Galaxy-S-II-Plus/
├── README.md               # الدليل الشامل باللغتين العربية والإنجليزية
├── recovery/
│   └── twrp-3.0.2-s2vep.img # ريكفري TWRP المخصص للجهاز (7.3 MB)
├── root/
│   ├── SuperSU-v2.82.zip   # ملف تفليش الروت عبر الريكفري (6.6 MB)
│   └── supersu.apk         # تطبيق إدارة الروت SuperSU (6.0 MB)
├── tools-apk/
│   ├── AdAway.apk          # تطبيق حجب الإعلانات بالروت (5.5 MB)
│   └── TerminalEmulator.apk # تطبيق الطرفية لاختبار الروت (553 KB)
└── rom/
    └── README.md           # روابط التحميل السحابية المباشرة للروم وحزمة جوجل
```

---

<br>

# 🇸🇦 دليل ترقية وتفليش وعمل روت لهاتف Samsung Galaxy S II Plus (GT-I9105P)

مرحباً بك! هذا المستودع يوثق ويحتوي على كافة الملفات والأدوات المنظمة اللازمة لإحياء هاتف **Samsung Galaxy S II Plus (GT-I9105P)**، وترقيته من نظام أندرويد 4.2.2 القديم جداً إلى نظام **Android 7.1.2 Nougat** المستقر عبر روم **LineageOS 14.1**، مع تثبيت متجر **Google Play Store** الحديث، وصلاحيات **Root** كاملة عبر **SuperSU**، وريكفري **TWRP 3.0.2**.

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
   أوقفت شركة Google خوادم تسجيل الدخول لحسابات Google نهائياً عن جميع أنظمة أندرويد 2.3 وحتى 4.3 في أواخر 2021. هذا التحديث ينقل الهاتف إلى أندرويد 7.1.2 ويعيد تشغيل متجر Google Play الحديث بكفاءة.
2. **عدم دعم التطبيقات الحديثة:**
   معظم التطبيقات أصبحت تتطلب أندرويد 5.0 أو أحدث. الترقية تسمح بتثبيت التطبيقات العصرية.
3. **التخلص من بطء واجهة سامسونج:**
   روم LineageOS خفيف وسريع ونظيف وخالٍ من تطبيقات سامسونج الثقيلة.

---

### ☁️ 3. روابط التحميل السحابية المباشرة (ROM & GApps Cloud Links)

نظراً للحجم الكبير لملفات الروم وحزمة جوجل (أكثر من 500 ميجابايت)، يتم توفير روابط تحميل مباشرة وسريعة ودائمة بدلاً من رفعها داخل Git:

* **📱 روم LineageOS 14.1 (Android 7.1.2):**
  * **الحجم:** 318 MB | **MD5:** `ec1d031afd4b496b186b3fc5b6bbe095`
  * 🔗 [تحميل مباشر وسريع (Archive Mirror)](https://archive.org/download/afharchive_173_lineage-141-20200616-unofficial-i9105pzip/lineage-14.1-20200616-UNOFFICIAL-i9105p.zip)
* **🏪 متجر وخدمات جوجل OpenGApps 7.1 Pico:**
  * **الحجم:** 182 MB | **MD5:** `ff23028a1fcabbebec0bf3ccb133c0db`
  * 🔗 [تحميل مباشر وسريع (Archive Mirror)](https://archive.org/download/open_gapps-arm-7.1-pico-20220215/open_gapps-arm-7.1-pico-20220215.zip)

*(يمكنك وضع الملفين بعد تحميلهما داخل مجلد `rom/`)*

---

### ⚡ 4. خطوات التثبيت والتفليش خطوة بخطوة

#### الخطوة 1: تثبيت ريكفري TWRP 3.0.2
1. أدخل الهاتف في وضع الداونلود (Download Mode): أطفئ الجهاز ثم اضغط معاً **[خفض الصوت + القائمة Home + التشغيل Power]** ثم زر **رفع الصوت**.
2. على حاسوب لينكس، نفذ الأمر عبر Heimdall باستخدام الملف الموجود في مجلد `recovery/`:
   ```bash
   sudo heimdall flash --RECOVERY recovery/twrp-3.0.2-s2vep.img --no-reboot
   ```
3. ادخل فوراً للريكفري بالضغط على: **[رفع الصوت + القائمة Home + التشغيل Power]**.

#### الخطوة 2: نقل الملفات إلى الهاتف
قم بتوصيل الهاتف بالحاسوب ونقل الملفات إلى الذاكرة الداخلية عبر ADB:
```bash
adb push rom/lineage-14.1.zip /sdcard/
adb push rom/gapps-7.1-pico.zip /sdcard/
adb push root/SuperSU-v2.82.zip /sdcard/
```

#### الخطوة 3: المسح النظيف (Wipe) في TWRP
من واجهة TWRP:
* ادخل إلى **Wipe** ← **Advanced Wipe**.
* حدد: **Dalvik / ART Cache**, **System**, **Cache**, **Data** (لا تحدد Internal Storage / الذاكرة الداخلية).
* اسحب للتأكيد (Swipe to Wipe).

#### الخطوة 4: التفليش (Flash) بالترتيب الصحيح
من واجهة TWRP اضغط **Install** وثبت الملفات بالترتيب:
1. ثبت ملف الروم: `lineage-14.1.zip`
2. ثبت ملف خدمات جوجل: `gapps-7.1-pico.zip`
3. ثبت ملف الروت: `SuperSU-v2.82.zip`

#### الخطوة 5: إعادة التشغيل والإقلاع الأول
* اختر **Reboot System**.
* الإقلاع الأول يستغرق من **3 إلى 5 دقائق** لبناء حزم النظام عبر `dex2oat`.
* سيعمل الهاتف على معالج الإعداد الترحيبي (Setup Wizard) بنظام **Android 7.1.2**.

---

### 🔍 5. كيف تتأكد وتثبت أن الهاتف مروّت 100%؟
1. افتح تطبيق **Terminal Emulator** على الهاتف.
2. اكتب `su` واضغط **Enter**.
3. ستظهر نافذة من SuperSU تطلب الإذن ← اضغط **منح (Grant)**.
4. ستتحول العلامة من `$` إلى **`#`** (علامة الروت).
5. اكتب الأمر `id`؛ ستظهر النتيجة القاطعة:
   ```text
   uid=0(root) gid=0(root)
   ```

---

<br>
<hr>
<br>

# 🇬🇧 Complete Upgrade, Custom ROM & Root Guide for Samsung Galaxy S II Plus (GT-I9105P)

Welcome! This repository documents the entire process and provides an organized toolkit to upgrade and revive the **Samsung Galaxy S II Plus (GT-I9105P / s2vep)**. It upgrades the device from its obsolete stock Android 4.2.2 Jelly Bean to a clean, fast, and stable **Android 7.1.2 Nougat (LineageOS 14.1)** with working **Google Play Store**, full **SuperSU Root**, and permanent **TWRP 3.0.2** custom recovery.

---

### 📋 1. Device Hardware & Software Specifications

| Specification | Value |
| :--- | :--- |
| **Device Model** | Samsung Galaxy S II Plus (NFC Variant) |
| **Model Number** | `GT-I9105P` |
| **Device Codename** | `s2vep` / `s2vepxx` |
| **Chipset / SoC** | Broadcom Capri BCM28155 (Dual-Core 1.2 GHz ARM Cortex-A9) |
| **Architecture** | `ARMv7-A` (`armeabi-v7a`) 32-bit |
| **RAM** | 1.0 GB |
| **Internal Storage** | 8.0 GB (~4.0 GB user-accessible partition) |
| **Original Stock OS** | Android 4.2.2 Jelly Bean (TouchWiz UI) |
| **Upgraded OS** | **Android 7.1.2 Nougat** via **LineageOS 14.1** (Unofficial) |
| **Root Status** | **100% Rooted** via `SuperSU v2.82` |
| **Custom Recovery** | **TWRP 3.0.2-0** (Permanent & Protected) |

---

### 🛑 2. Why Upgrade? (Issues Solved)

1. **Dead Google Play Store on Legacy Android:**
   Google shut down account sign-ins on Android 2.3 through 4.3 back in late 2021. Upgrading to Android 7.1.2 brings modern security certificates (TLS 1.2/1.3) and restores full, working Google Play Store functionality.
2. **Modern App Compatibility:**
   Modern apps (WhatsApp, Telegram, YouTube, etc.) drop support for Android 4.x. Android 7.1.2 supports modern app ecosystems.
3. **Superior Performance & Battery:**
   LineageOS removes Samsung's heavy bloatware, running lean and fast on 1 GB of RAM.

---

### ☁️ 3. Direct High-Speed Cloud Downloads (ROM & GApps)

Due to large file sizes (~500MB total), ROM packages are linked via permanent high-speed cloud mirrors:

* **📱 LineageOS 14.1 ROM (Android 7.1.2):**
  * **Size:** 318 MB | **MD5:** `ec1d031afd4b496b186b3fc5b6bbe095`
  * 🔗 [Direct Fast Download (Archive Mirror)](https://archive.org/download/afharchive_173_lineage-141-20200616-unofficial-i9105pzip/lineage-14.1-20200616-UNOFFICIAL-i9105p.zip)
* **🏪 OpenGApps 7.1 Pico (Google Play Services & Store):**
  * **Size:** 182 MB | **MD5:** `ff23028a1fcabbebec0bf3ccb133c0db`
  * 🔗 [Direct Fast Download (Archive Mirror)](https://archive.org/download/open_gapps-arm-7.1-pico-20220215/open_gapps-arm-7.1-pico-20220215.zip)

*(Download and place both files inside the `rom/` folder)*

---

### ⚡ 4. Step-by-Step Installation Walkthrough

#### Step 1: Flash TWRP Recovery
1. Boot phone into Download Mode: Power off, then hold **[Volume Down + Home + Power]**, then press **Volume Up**.
2. Flash using Heimdall on Linux:
   ```bash
   sudo heimdall flash --RECOVERY recovery/twrp-3.0.2-s2vep.img --no-reboot
   ```
3. Boot directly into TWRP recovery by holding **[Volume Up + Home + Power]**.

#### Step 2: Push Installation Files
Transfer the downloaded files via ADB:
```bash
adb push rom/lineage-14.1.zip /sdcard/
adb push rom/gapps-7.1-pico.zip /sdcard/
adb push root/SuperSU-v2.82.zip /sdcard/
```

#### Step 3: Perform Clean Wipe in TWRP
* In TWRP, go to **Wipe** → **Advanced Wipe**.
* Select: **Dalvik / ART Cache**, **System**, **Cache**, **Data** (DO NOT select Internal Storage / SD card).
* Swipe to Wipe.

#### Step 4: Flash Files in Exact Sequence
In TWRP, tap **Install** and queue/flash in this order:
1. `lineage-14.1.zip` (ROM)
2. `gapps-7.1-pico.zip` (Google Services)
3. `SuperSU-v2.82.zip` (Root)

#### Step 5: Reboot & First Boot
* Tap **Reboot System**.
* The first boot takes **3 to 5 minutes** while ART compiler (`dex2oat`) builds system caches.
* Complete the initial LineageOS / Google Setup Wizard.

---

### 🔍 5. Verifying Root Access

1. Open **Terminal Emulator** on the phone.
2. Type `su` and press **Enter**.
3. Grant SuperSU permission when prompted.
4. Prompt symbol switches from `$` to `#`.
5. Run `id` to confirm:
   ```text
   uid=0(root) gid=0(root)
   ```

---

### ⚙️ 6. Hardware Button Combinations

* **Recovery Mode (TWRP):** `[Volume Up + Home + Power]` (from powered-off state).
* **Download Mode (Odin/Heimdall):** `[Volume Down + Home + Power]` (from powered-off state), then `Volume Up`.

---

<div align="center">

**Created & Documented by [mostafaYasserDev](https://github.com/mostafaYasserDev) — October 2026**

</div>
