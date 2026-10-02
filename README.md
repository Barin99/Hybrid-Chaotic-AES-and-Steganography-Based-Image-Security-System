# 🔐 Hybrid Chaotic AES and Steganography-Based Image Security System

A secure image protection system that combines **AES-256 encryption, chaotic pixel scrambling, and LSB steganography** to provide multiple layers of security for confidential image data.

The system encrypts an image using AES-256, applies chaotic pixel scrambling to increase image randomness, and hides the encrypted image inside a cover image using Least Significant Bit (LSB) steganography. The embedded data can later be extracted and decrypted to reconstruct the original image.

---

## 📌 Project Overview

Images shared over networks can be exposed to unauthorized access, interception, or manipulation. Traditional encryption protects the image content but does not hide the existence of the encrypted data.

This project combines **cryptography and steganography** to address both aspects:

1. **AES-256 encryption** protects the image content.
2. **Chaotic pixel scrambling** adds an additional transformation layer and improves pixel distribution.
3. **LSB steganography** conceals the encrypted image data inside a cover image.
4. The receiver can extract the hidden data and perform the reverse operations to recover the original image.

### Security Pipeline

```text
Original Image
      │
      ▼
Chaotic Pixel Scrambling
      │
      ▼
AES-256 Encryption
      │
      ▼
Encrypted Image/Data
      │
      ▼
LSB Steganography
      │
      ▼
Stego Image
      │
      ▼
   Transmission
      │
      ▼
Extract Hidden Data
      │
      ▼
AES-256 Decryption
      │
      ▼
Inverse Chaotic Transformation
      │
      ▼
Recovered Image
```

---

## ✨ Features

* 🔐 AES-256 based image encryption
* 🌀 Chaotic pixel scrambling
* 🖼️ LSB-based image steganography
* 🔓 Image decryption and recovery
* 📤 Secure image embedding
* 📥 Hidden-data extraction
* 🛡️ Multi-layer image security
* 📊 Image security evaluation
* ⚠️ Input validation and exception handling
* 📁 Image file processing and storage
* 🌐 Web-based interface for encryption and decryption

---

## 🛠️ Technologies Used

### Programming Languages

* **C#**
* **Python**

### Backend & Web

* ASP.NET Core
* REST/API-based application logic
* HTML
* CSS
* JavaScript

### Security & Image Processing

* AES-256
* CBC Mode
* PyCryptodome
* LSB Steganography
* Chaotic Pixel Scrambling

### Database

* MongoDB

### Development Tools

* Git
* GitHub
* Visual Studio / VS Code

---

## 🏗️ System Architecture

The application consists of several major components:

```text
                    ┌─────────────────────┐
                    │    User Interface   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Backend / API     │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              ▼                ▼                ▼
       ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
       │   Chaotic   │  │    AES-256  │  │     LSB     │
       │ Scrambling  │  │ Encryption  │  │Steganography│
       └─────────────┘  └─────────────┘  └─────────────┘
              │                │                │
              └────────────────┼────────────────┘
                               ▼
                    ┌─────────────────────┐
                    │   Secure Image      │
                    │   / Stego Image     │
                    └─────────────────────┘
```

---

## 🔒 Encryption Process

The encryption process follows multiple stages.

### Step 1 — Image Input

The user selects an image that needs to be protected.

### Step 2 — Chaotic Pixel Scrambling

The image pixels are rearranged using a chaotic transformation.

The purpose of this stage is to disturb the spatial relationship between neighboring pixels and make the image structure less predictable.

### Step 3 — AES-256 Encryption

The scrambled image data is encrypted using **AES-256**.

AES provides strong symmetric-key encryption for protecting the actual image content.

### Step 4 — Steganographic Embedding

The encrypted data is embedded into a cover image using **Least Significant Bit (LSB) steganography**.

The resulting image is called the **stego image**.

---

## 🔓 Decryption Process

The reverse process is performed to recover the original image.

```text
Stego Image
     │
     ▼
Extract Hidden Data
     │
     ▼
AES-256 Decryption
     │
     ▼
Inverse Chaotic Transformation
     │
     ▼
Original Image
```

The system extracts the encrypted data from the stego image, decrypts it using the appropriate AES key, and reverses the chaotic transformation.

---

## 📊 Security Analysis

The project can be evaluated using commonly used image-security metrics.

### 1. Entropy

Entropy measures the randomness of image information.

A higher entropy value in an encrypted image generally indicates a more random pixel distribution.

### 2. NPCR

**Number of Pixels Change Rate (NPCR)** measures the percentage of pixels that change when a small modification is made to the original image.

```text
NPCR = (Number of changed pixels / Total pixels) × 100
```

### 3. UACI

**Unified Average Changing Intensity (UACI)** measures the average intensity difference between two images.

It helps evaluate how significantly pixel values change after encryption.

### 4. PSNR

**Peak Signal-to-Noise Ratio (PSNR)** can be used to measure the similarity between the original and recovered images or to evaluate the visual impact of transformations.

---

## 📂 Project Structure

```text
Hybrid-Chaotic-AES-and-Steganography-Based-Image-Security-System/
│
├── frontend/
│   ├── HTML/
│   ├── CSS/
│   └── JavaScript/
│
├── backend/
│   ├── Controllers/
│   ├── Services/
│   ├── Models/
│   └── Utilities/
│
├── python/
│   ├── encryption/
│   ├── decryption/
│   ├── chaotic/
│   └── steganography/
│
├── images/
│   ├── input/
│   ├── encrypted/
│   └── output/
│
├── README.md
└── ...
```

> The exact folder structure may vary depending on the implementation.

---

## 🚀 Getting Started

### Prerequisites

Make sure the following are installed:

* Python 3.x
* .NET SDK
* MongoDB
* Git
* Visual Studio or VS Code

---

## 📥 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/sujal0311/image-encryption_decryption_system.git
```

```bash
cd image-encryption_decryption_system
```

### 2. Install Python Dependencies

```bash
pip install pycryptodome
```

Install any additional dependencies required by the project.

### 3. Configure MongoDB

Make sure MongoDB is running locally or configure the project with your MongoDB connection string.

### 4. Run the Application

Run the backend using the appropriate .NET command:

```bash
dotnet run
```

If the project contains a separate Python service, start the Python component according to its configuration.

---

## 💻 Usage

### Encryption

1. Open the application.
2. Select an input image.
3. Provide the required encryption key/configuration.
4. Start the encryption process.
5. The system performs chaotic scrambling.
6. AES-256 encryption is applied.
7. The encrypted data is embedded into a cover image.
8. The resulting stego image is generated.

### Decryption

1. Upload the stego image.
2. Provide the required key.
3. Extract the hidden encrypted data.
4. Decrypt the data using AES-256.
5. Apply the inverse chaotic transformation.
6. Recover the original image.

---

## 🔐 Security Layers

The project uses multiple security mechanisms:

| Layer | Technique            | Purpose                      |
| ----- | -------------------- | ---------------------------- |
| 1     | Chaotic Scrambling   | Disrupts pixel relationships |
| 2     | AES-256              | Encrypts image information   |
| 3     | LSB Steganography    | Hides encrypted information  |
| 4     | Key-Based Decryption | Controls authorized recovery |

The combination provides both **content confidentiality** and **data concealment**.

---

## 🎯 Objectives

* Develop a secure image encryption and decryption system.
* Combine cryptographic and steganographic techniques.
* Improve the randomness of encrypted image data.
* Hide encrypted information inside a cover image.
* Provide a user-friendly web interface.
* Evaluate image security using statistical metrics.
* Demonstrate practical application of information security concepts.

---

## 📈 Advantages

* Multi-layer image protection
* Strong AES-256 encryption
* Additional pixel-level scrambling
* Conceals the presence of encrypted information
* Supports image encryption and recovery
* Can be implemented as a web-based security application

---

## ⚠️ Limitations

* LSB steganography has limited payload capacity.
* The security of the system depends partly on secure key management.
* Large images may require more processing time and storage.
* Steganographic embedding can be affected by image modifications or compression.
* The system is primarily designed for image-based data.

---

## 🔮 Future Enhancements

* Support for additional image formats.
* Advanced chaotic maps for pixel scrambling.
* Improved key-management mechanisms.
* Adaptive steganography techniques.
* Cloud-based deployment.
* Authentication and role-based access.
* Support for larger payloads.
* Automated security-metric reporting.
* Performance optimization for large images.

---

## 👨‍💻 Author

**Barin Ghosh**

B.Tech — Computer Science & Engineering
B. P. Poddar Institute of Management & Technology, Kolkata

---

## 📄 License

This project is developed for **educational and academic purposes**.

If you use or modify this project, please provide appropriate attribution to the original project.
