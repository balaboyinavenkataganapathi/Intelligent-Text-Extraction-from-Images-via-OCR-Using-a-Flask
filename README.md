# OCR-Based Text Extraction API Using Flask

This project provides a lightweight and easy-to-use REST API for extracting text from images using Optical Character Recognition (OCR). Built with Flask, the API accepts image uploads, processes them using the Tesseract OCR engine, and returns the extracted text in JSON format.

## 🧠 Features

* 📷 Accepts image files via HTTP POST
* 🔍 Uses Tesseract OCR for text recognition
* 🔁 Returns extracted text in JSON format
* 🔓 Lightweight and open-source
* ⚙️ Easily deployable as a microservice

## 🚀 Project Structure

```
OCR-Based-Text-Extraction-API-Using-Flask/
├── app.py                  # Main Flask application
├── requirements.txt        # Python dependencies
├── static/                 # Folder to store uploaded images (optional)
└── README.md               # Project documentation
```

## 🛠️ Requirements

* Python 3.7+
* [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
* pip (Python package manager)

## 📦 Installation

1. **Clone the Repository**

```bash
git clone https://github.com/your-username/OCR-Based-Text-Extraction-API-Using-Flask.git
cd OCR-Based-Text-Extraction-API-Using-Flask
```

2. **Install Python Dependencies**

```bash
pip install -r requirements.txt
```

3. **Install Tesseract OCR**

* **Ubuntu/Debian:**

  ```bash
  sudo apt update
  sudo apt install tesseract-ocr
  ```
* **macOS (using Homebrew):**

  ```bash
  brew install tesseract
  ```
* **Windows:**
  Download and install from [Tesseract OCR official page](https://github.com/tesseract-ocr/tesseract/wiki).

> Make sure `tesseract` is added to your system PATH.

## ▶️ Running the Application

```bash
python app.py
```

By default, the Flask app will run on: `http://127.0.0.1:5000/`

## 📄 API Usage

### Endpoint: `/extract-text`

**Method:** `POST`
**Content-Type:** `multipart/form-data`
**Field name:** `image`

#### Example using `curl`:

```bash
curl -X POST -F image=@example.jpg http://127.0.0.1:5000/extract-text
```

#### Response:

```json
{
  "extracted_text": "This is the text found in the image."
}
```


