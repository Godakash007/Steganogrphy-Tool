# 🔐 Steganography Tool

## 🧩 Introduction

The **Steganography Tool** is a Python-based cybersecurity application designed to **securely hide and extract sensitive information** within digital files such as **images, PDFs, and DOCX documents**.

Unlike traditional encryption methods, **steganography conceals data inside a carrier file** without visibly altering it — making this tool highly effective for **secure communication, data privacy, and digital forensics**.

This project integrates:
- **Least Significant Bit (LSB)** encoding for image steganography.
- **Metadata embedding** for document-based steganography.
- A **graphical interface** for simple and intuitive use.

---

## ✨ Key Features

### 🔹 1. Image Steganography
- Uses **Least Significant Bit (LSB)** encoding to hide secret messages or images within cover images.  
- Supports multiple formats — **PNG**, **JPEG**, **BMP**, etc.  
- Ensures **minimal visual distortion**, keeping the hidden content undetectable to the human eye.  

### 🔹 2. PDF Steganography
- Embeds hidden data inside the **metadata** section of PDF files.  
- Uses **Base64 encoding** for secure embedding and decoding.  
- Ideal for **confidential message transfer** and **covert data storage**.  

### 🔹 3. DOCX Steganography
- Conceals binary data within **Microsoft Word documents** using invisible text fields.  
- Maintains full readability of the document while embedding hidden information.  
- Allows secure extraction without structural modification.  

### 🔹 4. Hidden Content Detection & Prediction *(Future Upgrade)*
- Analyzes images, PDFs, and DOCX files for hidden data signatures.  
- Uses **pixel variance analysis** and **metadata scanning** to identify potential steganography.  
- Designed for **forensic analysts** to detect hidden threats within files.  

### 🔹 5. Modern & User-Friendly GUI
- Built using **CustomTkinter** with a **glassmorphic frosted effect** for a clean, modern design.  
- Allows users to upload, encode, decode, and analyze files easily.  
- Supports **manual and automated processing** of hidden data.  

---

## 💡 Use Cases

| Purpose | Description |
|----------|-------------|
| **Secure Communication** | Hide confidential messages inside harmless files to prevent interception. |
| **Digital Forensics** | Detect and extract hidden data during cybersecurity investigations. |
| **Watermarking & Copyright Protection** | Embed ownership or verification details in digital media. |
| **Covert Information Transfer** | Transfer sensitive data undetected. |
| **Anti-Censorship & Privacy Protection** | Bypass surveillance and censorship with embedded communication. |

---

## 🛠️ Technologies Used

| Library / Framework | Purpose |
|---------------------|----------|
| **Python** | Core programming language |
| **PIL (Pillow)** | Image processing and manipulation |
| **NumPy** | Pixel-level data computation |
| **PyPDF2** | PDF metadata handling |
| **python-docx** | DOCX data embedding and extraction |
| **CustomTkinter** | Modern graphical user interface (GUI) |

---

## 🧠 How It Works

### 🔸 Image Steganography
- Converts images into pixel arrays using **NumPy**.
- Hides bits of the secret image inside the least significant bits (LSB) of the cover image pixels.
- Saves the result as a new “encoded” image that looks identical to the original.

### 🔸 PDF Steganography
- Reads the target and base PDF using **PyPDF2**.
- Encodes the secret PDF in **Base64** and hides it in the **metadata** of the base PDF.
- Extraction decodes the Base64 data and reconstructs the original hidden PDF.

### 🔸 DOCX Steganography
- Converts the secret DOCX into Base64.
- Embeds it as **hidden text** inside a base Word file.
- Extraction locates and decodes the hidden Base64 text back into a document.

---

## 🧰 Installation

### Prerequisites
Make sure you have **Python 3.8+** installed.

### Step 1: Clone this repository
```bash
git clone https://github.com/yourusername/Steganography-Tool.git
cd Steganography-Tool
```
## ⚙️ Installation & Usage

### Step 2: Install Dependencies
```bash
pip install pillow numpy PyPDF2 python-docx customtkinter
```
### Step 3: Run the Tool
```bash
python main.py
```
### Project Structure
```bash
Steganography-Tool/
│
├── steg_tool.py
├── logo.png                   
├── README.md                   
├── requirements.txt          
└── samples/                   
```
## 🖼️ GUI Overview

- **Sidebar:** Navigation menu for Image, PDF, and DOCX modes.  
- **Main Area:** Contains buttons for hiding or extracting data.  
- **Modern UI:** Glassmorphic design with rounded edges and frosted transparency.  

---

## ⚙️ Example Workflow

### 🖼️ Image Example
1. Select a **cover image** and **secret image**.  
2. Click **“Hide Secret in Image.”**  
3. Save the encoded image.  
4. Later, choose the encoded image and click **“Extract Secret.”**

### 📄 PDF Example
1. Choose a **base PDF** and another **PDF to hide.**  
2. Click **“Hide PDF.”**  
3. Save the new PDF containing the embedded data.  
4. Use **“Extract PDF”** to retrieve it.

### 📝 DOCX Example
1. Choose a **base DOCX** and a **secret DOCX** to embed.  
2. Click **“Hide DOCX.”**  
3. Save the output file and later extract it via **“Extract DOCX.”**

---

## 🧑‍💻 Developer Notes

- GUI designed using **CustomTkinter** (Dark Mode + Frosted Glass effect).  
- Code follows a modular design for easy future upgrades:
  - 🧠 **Content Detection Module**  
  - 🤖 **AI-based Steganalysis Module**  
  - ☁️ **Cloud Sync Support for Forensic Use**  

---

## 📜 License

This project is licensed under the **MIT License**.  
You are free to **use, modify, and distribute** this software with proper attribution.

