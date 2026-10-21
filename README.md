# 🔒 Corporate Training Cheat Sheet Vault

A lightweight, automated repository designed to host a **GitHub Pages** site containing encrypted PDF files. Its main purpose is to store and share answers for mandatory, tedious corporate training modules (compliance, safety, HR courses, etc.).

> **Disclaimer:** All PDF files hosted on this page are encrypted. You need the decryption password from the maintainer/community to access the contents.

---

## 🚀 How It Works

1. **Add Encrypted PDF:** You upload or commit an encrypted PDF file containing training answers/notes to the repository.
2. **Push to `main`:** Push your changes to the `main` branch.
3. **Automated Build:** A GitHub Actions workflow automatically:
   * Scans the repository for `.pdf` files.
   * Generates an updated `index.html` file listing all available documents.
   * Deploys the site to **GitHub Pages**.

---

## 🛠️ How to Add a New Training PDF

### Method 1: Using Git CLI

```bash
# 1. Encrypt your PDF locally (e.g., using qpdf or 7-Zip/AES-256)
# 2. Copy the encrypted file into the repository root directory
cp /path/to/encrypted-compliance-answers.pdf .

# 3. Stage, commit, and push
git add encrypted-compliance-answers.pdf
git commit -m "add: answers for Q3 compliance training"
git push origin main
```

### Method 2: Via GitHub Web Interface

1. Go to your repository on GitHub.
2. Click **Add file** -> **Upload files**.
3. Drag and drop your **encrypted** PDF.
4. Click **Commit changes**.

---

## ⚠️ Security & Safety Guidelines

* **ALWAYS Encrypt Before Uploading:** GitHub Pages is publicly accessible. Never commit unencrypted documents, confidential corporate secrets, or personal identifiable information (PII).
* **Keep Passwords Separate:** Do NOT commit passwords or decryption keys to this repository, commit history, or issue trackers. Share keys via secure, out-of-band channels.
* **Descriptive File Names:** Use clear file names so people know which training the PDF corresponds to (e.g., `2026-cybersecurity-basics-answers.pdf`).

---

## 💻 Technical Setup

This project uses a zero-maintenance GitHub Actions workflow (`.github/workflows/deploy.yml`) that automatically generates the HTML index page on every push to `main`. No manual web development or HTML editing required!