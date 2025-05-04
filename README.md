# Steg-Trust
A Dual-Key Blockchain-Verified  Steganographic System


# 🔐 Secure Image Steganography with Blockchain-based Tampering Detection

This project securely embeds a secret message and metadata into an image using DCT-based steganography, encrypts both the embedded data and its hash with separate keys, and stores the encrypted hash on a local Ethereum blockchain using Ganache. Tampering is detected by comparing extracted content and verifying it against the blockchain-stored hash.

## 📌 Features

- DCT-based data embedding in image blue channel
- Separate key-based encryption of:
  - Secret message + metadata
  - SHA-256 hash of the combined data
- Metadata includes timestamp and author
- Tamper detection through DCT coefficient inversion
- Local blockchain (Ganache) for storing and verifying encrypted hash
- PSNR and SSIM comparison between original and stego images
- Robust logging of DCT coefficient changes for debugging

---

## 🧰 Requirements

Install dependencies in Google Colab or your local Python environment:

```bash
apt-get update
apt-get install -y nodejs npm
npm install -g ganache-cli
pip install opencv-python scikit-image cryptography web3 py-solc-x
