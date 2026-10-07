# DeepFake_Forensics_Project
# 🔍 Deepfake / AI Identity Protector

## Forensics, Testing and Research

This project focuses on the **forensic analysis, robustness testing, and research of digital images** to help identify possible manipulation and understand the reliability of deepfake detection systems.

---

## 📌 Project Overview

Deepfakes and AI-generated images can be used to manipulate digital identity and spread misleading content.

The **Deepfake / AI Identity Protector** project aims to study different forensic techniques and testing methods that can help analyze digital media and detect possible manipulation.

My assigned module focuses on:

* 🖼️ Media Forensics
* 🔐 SHA-256 Hashing
* 📊 Error Level Analysis (ELA)
* 📚 Literature Survey
* 🧪 Robustness Testing

---

## 🎯 Objectives

The main objectives of this module are:

1. Analyze image metadata using EXIF.
2. Generate SHA-256 hashes for image integrity verification.
3. Perform Error Level Analysis (ELA).
4. Study existing research on deepfake detection.
5. Test image analysis under different conditions.
6. Evaluate the effect of JPEG compression, resizing, and blurring.

---

# 🛠️ Technologies Used

* **Python 3**
* **Pillow (PIL)**
* **OpenCV**
* **SHA-256 / hashlib**
* **Google Scholar**
* **arXiv**
* **IEEE Xplore**

---

# 📂 Project Structure

```text
DeepFake_Forensics/
│
├── code/
│   ├── exif_analysis.py
│   ├── hash_analysis.py
│   ├── ela_analysis.py
│   └── robustness_test.py
│
├── images/
│   └── original/
│       ├── img1.jpg
│       ├── img2.jpg
│       └── img3.jpg
│
├── results/
│   ├── ela/
│   ├── robustness/
│   └── reports/
│
├── papers/
│   └── literature_survey.xlsx
│
└── README.md
```

---

# 🔬 1. EXIF Metadata Analysis

EXIF (Exchangeable Image File Format) metadata can contain information about an image such as:

* Camera make
* Camera model
* Date and time
* Software
* GPS information
* Image settings

### Tool Used

**Pillow**

### Run

```bash
python code/exif_analysis.py
```

### Purpose

EXIF information can provide useful clues about the origin and processing history of an image.

> Note: Absence of EXIF metadata does not automatically mean that an image is fake.

---

# 🔐 2. SHA-256 Hashing

SHA-256 is used to generate a unique digital fingerprint for an image file.

### Tool Used

**Python hashlib**

### Run

```bash
python code/hash_analysis.py
```

### Purpose

The hash can be used to compare files and check whether an image has been modified.

Even a small change to the file normally produces a completely different SHA-256 hash.

---

# 📊 3. Error Level Analysis (ELA)

Error Level Analysis is a forensic technique used to visualize differences caused by JPEG compression.

### Tool Used

**Pillow**

### Run

```bash
python code/ela_analysis.py
```

The generated ELA image is stored inside:

```text
results/ela/
```

### Purpose

ELA can highlight areas with different compression characteristics that may deserve further investigation.

> ELA is not a standalone deepfake detector. Its results should be interpreted together with other forensic evidence.

---

# 🧪 4. Robustness Testing

Robustness testing checks how image processing affects forensic analysis.

The following transformations are tested:

### JPEG Compression

Tests whether image compression affects the analysis.

```text
Original Image
      ↓
JPEG Compression
      ↓
Compressed Image
```

### Image Resizing

Tests the effect of changing image dimensions.

```text
Original Image
      ↓
Resize
      ↓
Resized Image
```

### Image Blurring

Tests the effect of blur on forensic analysis.

```text
Original Image
      ↓
Gaussian Blur
      ↓
Blurred Image
```

### Run

```bash
python code/robustness_test.py
```

The generated images are stored in:

```text
results/robustness/
```

---

# 📚 5. Literature Survey

A literature survey is conducted to study existing research on deepfake detection.

Research papers are collected from:

* Google Scholar
* arXiv
* IEEE Xplore

Three deepfake detection papers are reviewed.

For each paper, the following information is recorded:

| Field      | Description                        |
| ---------- | ---------------------------------- |
| Title      | Research paper title               |
| Year       | Publication year                   |
| Method     | Detection technique used           |
| Dataset    | Dataset used for experiments       |
| Result     | Main experimental result           |
| Limitation | Limitations of the proposed method |

The literature survey is stored in:

```text
papers/literature_survey.xlsx
```

---

# 📈 Expected Results

The project produces:

* EXIF metadata information
* SHA-256 hash values
* ELA images
* JPEG-compressed images
* Resized images
* Blurred images
* Literature survey of deepfake detection research

These results help understand how digital images can be analyzed and how image manipulation or processing can affect forensic investigation.

---

# ⚠️ Limitations

* EXIF metadata can be removed or modified.
* SHA-256 detects file changes but does not determine whether an image is a deepfake.
* ELA can provide forensic clues but cannot independently confirm manipulation.
* Image compression and resizing can affect forensic results.
* Deepfake detection methods may perform differently across different datasets and image qualities.

---

# 🚀 Future Improvements

Possible future improvements include:

* Integration with automated deepfake detection models.
* Face manipulation detection.
* AI-generated image detection.
* Video forensic analysis.
* Automated forensic report generation.
* Testing against larger deepfake datasets.
* Combining multiple forensic techniques into a single analysis pipeline.

---

# 👨‍💻 Module

**Project:** Deepfake / AI Identity Protector
**Module:** Forensics, Testing and Research

---

## 📜 Disclaimer

This project is developed for **educational and research purposes**. Forensic techniques such as EXIF analysis and ELA provide supporting evidence and should not be treated as definitive proof of image manipulation without further investigation.
