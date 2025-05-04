📝 How It Works
Input:

Secret message (user input)

Author name (user input)

Two passwords (used to derive two encryption keys)

Encryption:

Combine message and metadata

Compute SHA-256 hash

Encrypt hash and combined data with separate Fernet keys

DCT Embedding:

Embed binary of encrypted data in middle-frequency DCT coefficients

Store coefficient change logs

Tampering Simulation:

Invert DCT coefficients in the stego image to simulate tampering

Extraction & Verification:

Extract and decrypt data

Recompute hash and compare with blockchain-stored hash

Detect any tampering

Blockchain:

Store encrypted hash using Web3.py on Ganache

Retrieve and verify during integrity check

🛡️ Security Measures
Encryption with Fernet + PBKDF2HMAC + SHA256

Two separate salts and keys for hash and data

Tampering detection through hash mismatch or data corruption

📊 Quality Metrics
PSNR: Measures distortion between original and stego image

SSIM: Measures structural similarity

⚙️ Blockchain Setup (Ganache)
Start Ganache locally:

bash
Copy
Edit
ganache-cli -p 7545
Smart contract is automatically compiled and deployed using Web3.py with solcx.

📸 Sample Metadata
yaml
Copy
Edit
Secret Message to Embed: HelloWorld!
Metadata to Embed: Timestamp: 2025-05-04T12:34:56 | Author: User
🔍 Example Output
Encrypted Data: ...hex...

Encrypted Hash: ...hex...

Stego Image: ✅ stego_image.png

Tampered Image: ❌ tampered_stego_image.png

Blockchain Verification: PASS / FAIL
