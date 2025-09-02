# Simple Steganography Project

This project provides a basic implementation of steganography, the art of hiding a secret message within an image. It uses the **Least Significant Bit (LSB)** technique to embed data into an image's pixel values.

---

## 🚀 How It Works

The project is split into two main scripts: `encrypt.py` and `decrypt.py`.

### 🔒 `encrypt.py`

This script is used to embed a secret message and a passcode into an image. It works by converting the message and passcode into binary data and then replacing the last bit (the LSB) of each pixel's color value with a bit of the secret data. This change is so small that it is invisible to the human eye. The modified image is then saved as a PNG file to prevent compression from corrupting the embedded data.

### 🔓 `decrypt.py`

This script extracts the hidden message from an encrypted image. It reads the LSB of the pixels to retrieve the header, which contains the lengths of the passcode and the secret message. It then reconstructs the hidden passcode and secret message. To reveal the message, you must enter the correct passcode.

---

## 💻 Requirements

To run this project, you need Python and the following libraries:

* **OpenCV**: For handling image files.
* **NumPy**: For efficient manipulation of pixel data.

You can install them using pip:

```bash
pip install opencv-python numpy
````

-----

## 📝 Usage

### 1\. **Encrypt a Message**

1.  Place an image (e.g., `Original Image.jpg`) in the same directory as the script.
2.  Open `encrypt.py` and ensure the `folder` and `img_path` variables are correctly set to your project directory and image file.
3.  Run the script from your terminal:
    ```bash
    python encrypt.py
    ```
4.  Follow the prompts to enter your secret message and a passcode. The script will save a new file, `encrypted Image.png`, with your hidden data.

### 2\. **Decrypt a Message**

1.  Make sure `encrypted Image.png` is in the directory specified in `decrypt.py`.
2.  Open `decrypt.py` and verify the `folder` and `img_path` variables are correct.
3.  Run the script from your terminal:
    ```bash
    python decrypt.py
    ```
4.  Enter the correct passcode when prompted to reveal the secret message.

-----

## ⚠️ Important Notes

  * **File Paths**: Remember to update the file paths in both `encrypt.py` and `decrypt.py` to match your local setup.
  * **Image Format**: The encrypted output must be a **lossless** format like PNG to preserve the pixel data.
  * **Data Size**: The size of the secret message is limited by the number of pixels in the image. Trying to embed too much data will result in an error.

<!-- end list -->

```
```
