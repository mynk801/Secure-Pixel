# SecurePixel - Image Encryption and Steganography System

SecurePixel is a project that implements a two-layer image encryption process, combining **Henon Map-based encryption** with **Steganography** to secure images. This ensures that the target image is scrambled and then concealed within a base image for additional security.

## Features

- **Two-Layer Encryption**:
  - First layer uses Henon Map for pixel randomization.
  - Second layer hides the encrypted image behind a base image using steganography.
- **Decryption Process**:
  - The process is reversed to retrieve the hidden and decrypted target image.
- **User-Friendly Interface**:
  - A web-based interface to perform both encryption and decryption.

## Process Overview

### 1. Original Images

- **Base Image**:  
  This is the image behind which the target image will be hidden using steganography.  
  ![Base Image](Backend/base_image/2.jpg)

- **Target Image**:  
  This is the image to be encrypted and hidden.  
  ![Target Image](Backend/target_image/1.jpg)

### 2. Henon Map Encrypted Image

- The target image is encrypted using a Henon Map, which scrambles its pixels in a way that is reversible only with the correct keys.  
  ![Encrypted Target Image](Backend/output/encrypted_target.png)

### 3. Steganography - Hiding the Encrypted Image

- The encrypted target image is now hidden behind the base image using steganography techniques. The result is a new image that looks identical to the base image but contains the encrypted target image.  
  ![Steganography Image](Backend/output/steg.png)

### 4. Decryption and Recovery

- **Recovered Target Image**:  
  After the decryption process, the scrambled target image is extracted from the base image but is still in its encrypted form.  
  ![Recovered Target Image](Backend/output/Target_re.png)

- **Final Decrypted Target Image**:  
  Finally, the extracted target image is decrypted to restore the original target image.  
  ![Decrypted Target Image](Backend/output/decrypted_target.png)

## Running the Application

To run the application, follow these steps:

1. Navigate to the `Frontend` folder:
   ```bash
   cd Frontend

2. Install the necessary dependencies:
   ```bash
   pip install -r requirements.txt

3. Run the application:
   ```bash
   python main.py
4. Open your browser and go to `http://127.0.0.1:5000` to access the web interface.

