# 🌙 Luna Crypto Algorithm (LCA)

Luna Crypto Algorithm (LCA) is a lightweight, custom-built encryption algorithm written in PHP. It implements a simplified version of RSA-style public-key cryptography with some unique mechanisms for educational or experimental purposes.

> ⚠️ **Note:** This is a conceptual encryption tool and is **not recommended for production use or secure environments**.

---

## 🔐 Features

- Key generation (public & private)
- Basic RSA-style encryption/decryption
- Simple key formatting and parsing
- Prime number generation and modular arithmetic
- Symmetric validation of key pairs

---

## 📦 Installation

Clone the repository or copy the `LCA` class into your PHP project:

```bash
git clone https://github.com/Minosuko/LCA.git
```

---

## 🧪 Usage

### Key Generation

```php
$lca = new LCA();
$keys = $lca->generateKeys();

echo $keys['public'];
echo $keys['private'];
```

### Encrypt

```php
$ciphertext = $lca->encrypt("hello", $keys['public']);
```

### Decrypt

```php
$plaintext = $lca->decrypt($ciphertext, $keys['private']);
```

---

## 📄 Example Output

**Public Key:**
```
-----BEGIN LCA PUBLIC KEY-----
[base64-encoded key here]
-----END LCA PUBLIC KEY-----
```

**Private Key:**
```
-----BEGIN LCA PRIVATE KEY-----
[base64-encoded key here]
-----END LCA PRIVATE KEY-----
```

---

## ⚙️ How It Works

- Generates small prime numbers for key construction
- Encrypts each character using modular exponentiation
- Validates key pairs by checking encryption/decryption over all 255 ASCII bytes
- Keys are serialized in a custom Base64 format

---

## 🛑 Limitations

- Not cryptographically secure
- Only supports short strings (up to key length)
- Small primes and short key lengths make it vulnerable to brute-force attacks
- For learning or experimentation only

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## ✨ Contributions

Feel free to open issues or submit PRs to improve key strength, add secure padding, or extend features.

---

## 🙌 Credits

Built with 💙 by Minosuko
