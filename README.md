 🛡️ Resume Redactor Tool – User Guide  
### For Recruiters | Automatically redacts contact info while keeping the candidate’s name and work history intact

This open-source tool helps **recruiters safely share candidate resumes with companies** by automatically **blacking out personal contact details** (phone, email, address, social links) — **while preserving the candidate’s name, work experience, and skills**.

> ✅ Runs 100% offline (no data leaves your computer)  
> ✅ Supports Japanese, English, and mixed-language PDFs  
> ✅ Free & open-source (MIT License)

---

## 🔧 Prerequisites

- **Windows, macOS, or Linux**
- **Python 3.7 or newer** installed  
  → Not installed? Download from [python.org](https://www.python.org/downloads/)

---

## 📥 Step 1: Download the Tool

1. Go to the GitHub repository:  
   👉 https://github.com/your-username/resume-redactor *(replace with your actual URL)*

2. Click **"Code" → "Download ZIP"**  
   ![](https://docs.github.com/assets/cb-12345/images/help/repository/code-button.png)

3. Extract the ZIP file and save the folder anywhere (e.g., `Desktop/resume-redactor`)

---

## ⚙️ Step 2: Install Required Libraries

1. Open **Terminal** (macOS/Linux) or **Command Prompt** (Windows)

2. Navigate to the tool’s folder:
   ```bash
   cd path/to/resume-redactor
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   → This takes just a few seconds (internet required)

---

## 📄 Step 3: Prepare Your Resume PDF

- Place the resume you want to redact **inside the `resume-redactor` folder**  
  (e.g., `my_resume.pdf`)

> 💡 Filenames with spaces or non-English characters (like Japanese) are supported!

---

## ▶️ Step 4: Run the Redaction Tool

In your terminal, run:

```bash
python redact_resume.py input.pdf output.pdf
```

### Example:
```bash
python redact_resume.py my_resume.pdf my_resume_sanitized.pdf
```

✅ On success, you’ll see:  
```
✅ Redaction complete: my_resume_sanitized.pdf
```

---

## 🔍 Step 5: Verify the Result

1. Open `my_resume_sanitized.pdf`

2. Confirm the following:

| Field | Status |
|------|--------|
| **Full Name (e.g., Taro Yamada)** | ✅ **Visible** |
| Phone Number (e.g., 03-1234-5678) | ⬛ **Redacted** |
| Email (e.g., taro@example.com) | ⬛ **Redacted** |
| Address (e.g., Shibuya-ku, Tokyo) | ⬛ **Redacted** |
| LinkedIn / GitHub / Portfolio | ⬛ **Redacted** |
| Work History, Skills, Education | ✅ **Visible** |

> ⚠️ If redaction misses some text:  
> Minor layout variations in PDFs may require manual review. The tool works best with standard resume formats.

---

## 🔄 Frequently Asked Questions (FAQ)

### Q: Does it work with English resumes?  
**A: Yes!** Fully supports English, Japanese, and bilingual documents.

### Q: Will the candidate’s name be redacted?  
**A: No.** Names are intentionally **left visible** — only direct contact methods are hidden.

### Q: Is my file uploaded to the cloud?  
**A: Never.** All processing happens **locally on your machine**. No internet required after setup.

### Q: Can I also redact birthdate or age?  
**A:** Yes! Open `redact_resume.py` and add these lines to the `PATTERNS` list:
```python
r'\d{4}年\d{1,2}月\d{1,2}日',
r'\d{4}/\d{1,2}/\d{1,2}',
```

---

## ❤️ Contribute to This Open-Source Project

This tool is released under the **MIT License**.  
- Found a bug? → Open an **Issue**  
- Have an improvement? → Submit a **Pull Request**  
- Like the tool? → Give it a ⭐ **Star on GitHub**!

---

## 📬 Need Help?

Have questions or feedback?  
Contact us via **GitHub Issues** or email: [your-email@example.com]

---

> ✨ **Protecting privacy builds trust.**  
> We hope this tool helps you foster safer, more ethical hiring practices worldwide.

---

✅ **Ready to use!** Copy this guide into your `README.md`, website, or internal documentation.  
Let me know if you'd like a **bilingual (JP/EN) version**, **PDF handout**, or **Docker setup instructions**! 🌍
