# Secure Images with TripleDES

This is a mini-project for encrypting and decrypting images through a simple web application using the Triple DES (3DES) algorithm.

## Introduction

This web application provides a straightforward way to secure image files. Users can upload an image, encrypt it with a secret key using the Triple DES algorithm, and then download the encrypted output. Conversely, they can upload an encrypted file and decrypt it using the correct secret key to retrieve the original image.

## Features

* **Image Encryption:** Encrypts `.jpeg` images using a user-provided secret key and the Triple DES algorithm. The encrypted output is saved as a text file.
* **Image Decryption:** Decrypts previously encrypted image files using the same secret key. The decrypted output is downloaded as an image file.
* **Simple Web Interface:** Easy-to-use drag-and-drop or file selection for image input.

## Technologies Used

* **Frontend:** HTML, CSS, JavaScript
* **Cryptography Library:** CryptoJS (specifically for Triple DES)
* **File Handling:** FileSaver.js (for saving files on the client-side)

## Setup and Installation

This project is designed to be very easy to run.

1.  **Clone the Repository:**
    ```bash
    git clone <your_repository_url>
    cd secure-images-with-tripledes # Or whatever your project folder is named
    ```
    (Replace `<your_repository_url>` with the actual URL of your GitHub repository.)

2.  **Launch the Application:**
    Simply open the `dashboard.html` file in your web browser. There's no need for a local server or additional installations.

    ```bash
    # Example (using a command that opens files, adjust for your OS if needed)
    start dashboard.html  # On Windows
    open dashboard.html   # On macOS
    xdg-open dashboard.html # On Linux (might vary)
    ```

## How to Use

1.  **Dashboard:**
    * Open `dashboard.html` in your web browser.
    * You will see two buttons: "Encrypt" and "Decrypt".

2.  **Encrypting an Image:**
    * Click the "Encrypt" button.
    * On the "Encrypt your picture" page:
        * Drag and drop an image file into the designated area, or click "Select file" to browse for an image.
        * Enter your secret key in the "Enter your secret key" field.
        * Click the "Encrypt" button.
        * A file named `encrypted_image` (a text file containing the encrypted data) will be downloaded to your computer.

3.  **Decrypting an Image:**
    * From the dashboard, click the "Decrypt" button.
    * On the "Decrypt your picture" page:
        * Drag and drop your `encrypted_image` file (or the text file containing the encrypted data) into the designated area, or click "Select file" to browse for it. The content of the file will appear in the text area.
        * Enter the **exact same secret key** you used for encryption in the "Enter your secret key" field.
        * Click the "Decrypt" button.
        * A file named `decrypted_image` (your original image) will be downloaded to your computer.

## Important Notes

* **Secret Key:** The security of your image relies entirely on the strength and secrecy of your key. Choose a strong, unique key and keep it confidential. Losing the key means you cannot decrypt your image.
* **File Type:** The encryption process converts the image to a base64 encoded JPEG string before encryption.
* **Error Handling:** The decryption process includes basic error handling for incorrect secret keys or corrupted encrypted data.

## Resources

This project utilized code snippets and concepts from the following online resources:
* [cite_start][https://codepen.io/banik/pen/dgQvWO](https://codepen.io/banik/pen/dgQvWO) [cite: 1]
* [https://codepen.io/wouwisl/pen/LYGMya](https://codepen.io/wouwisl/pen/LYGMya)
