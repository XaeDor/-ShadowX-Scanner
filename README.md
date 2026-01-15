# 🕷️ ShadowX-Scanner

> **Modular Web Vulnerability Scanner for Learning, Labs, CTFs & Bug Bounty Practice**

ShadowX-Scanner is a **modular web vulnerability scanner** designed for **education and controlled security testing**.
It combines static crawling, JavaScript-based crawling, forced endpoint discovery, and multiple vulnerability engines in a **safe & extensible architecture**.

---

## ⚠️ Educational & Authorized Use Only

Scan **only**:

* Assets you own
* Labs / CTF platforms
* Bug bounty programs that explicitly allow testing

🚫 Unauthorized scanning is illegal.

---

## ✨ Features

### Crawling

* ✔ Static HTML crawler
* ✔ JavaScript crawler (**Playwright-powered**)
* ✔ Forced endpoint discovery

### Vulnerability Engines

* ✔ SQL Injection
* ✔ Cross-Site Scripting (XSS)
* ✔ Local File Inclusion (LFI)
* ✔ Server-Side Request Forgery (SSRF)
* ✔ Open Redirect
* ✔ IDOR (Insecure Direct Object Reference)

### Scan Control

* ✔ Safe Mode (low & slow scanning)
* ✔ Aggressive Mode (**LAB / CTF only**)
* ✔ CLI-controlled limits (URLs, delay, threads)
* ✔ Clean `Ctrl + C` handling
* ✔ Modular & extensible architecture

---

## 📁 Project Structure

```text
ShadowX-Scanner/
│
├── main.py
├── crawler.py
├── js_crawler.py
├── context.py
├── output.py
│
├── engines/
│   ├── sqli.py
│   ├── xss.py
│   ├── lfi.py
│   ├── ssrf.py
│   ├── redirect.py
│   ├── idor.py
│   └── forced_endpoints.py
│
├── requirements.txt
└── README.md
```

---

## 🛠️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/XaeDor/ShadowX-Scanner.git
cd ShadowX-Scanner
```

### 2️⃣ Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ (Optional but Recommended) Install Playwright

Required for scanning **JavaScript-heavy websites**.

```bash
pip install playwright
playwright install chromium
```

> If Playwright is not installed, ShadowX-Scanner will still work using **static crawling only**.

---

## 🚀 Usage

### 🔹 Basic Scan

```bash
python3 main.py -d example.com
```

### 🔹 Limit URLs

```bash
python3 main.py -d example.com -u 20
```

### 🔹 Safe Mode (Recommended for real websites)

```bash
python3 main.py -d example.com --safe
```

### 🔹 Aggressive Mode (**CTF / LAB ONLY**)

```bash
python3 main.py -d testphp.vulnweb.com --aggressive
```

### 🔹 Delay Control

```bash
python3 main.py -d example.com --delay 2
```

---

## 🧾 CLI Options

| Option             | Description            |
| ------------------ | ---------------------- |
| `-d`, `--domain`   | Target domain          |
| `-u`, `--max-urls` | Maximum URLs to scan   |
| `-t`, `--threads`  | Concurrent threads     |
| `--delay`          | Delay between requests |
| `--safe`           | Low & slow scanning    |
| `--aggressive`     | Labs / CTF only        |

```bash
python3 main.py -h
```

---

## 📊 Output

* Live scan progress
* Categorized vulnerabilities
* Confidence levels (**LOW / MEDIUM / HIGH**)
* Final scan summary

---

## 👨‍💻 Author

**ShadowX (XaeDor)**
GitHub: [https://github.com/XaeDor](https://github.com/XaeDor)

---

## ⭐ Support

If you like this project:

* ⭐ Star the repository
* 🍴 Fork it
* 🐞 Open issues / submit PRs

---

## 📜 License & Copyright

Copyright © 2026 **XaeDor**

This project is licensed under the **MIT License**.
You are free to use, modify, and distribute this tool, provided the original copyright notice and license are included.

---

## ⚠️ Legal Disclaimer

ShadowX-Scanner is intended **ONLY** for:

* Educational purposes
* Learning web security
* Authorized penetration testing
* Bug bounty programs
* Labs / CTF environments

🚫 **Do NOT use this tool on systems you do not own or have explicit permission to test.**

The author (**XaeDor**) is **NOT responsible** for:

* Illegal usage
* Damage caused
* Misuse of this tool

Use responsibly and ethically.
