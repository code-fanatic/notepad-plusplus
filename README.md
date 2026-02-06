# Notepad++ Regular Expression Cheat Sheet
A **clear, beginner-friendly Regular Expression reference** specifically for **Notepad++ (Regular Expression Search mode)**, based on the **official Notepad++ documentation** and the **Boost regex engine**.
This repo is meant to be a **practical lookup guide** — not theory-heavy — with real examples that actually work in Notepad++.

---

## 📌 What This Repository Contains
- ✅ Correct regex patterns that work in **Notepad++**
- ✅ Clear explanations for:
  - Characters (`\w`, `\d`, etc.)
  - Digits
  - Whitespace
  - Brackets & quantifiers
- ✅ Fixed common regex mistakes found in online tutorials
- ✅ Examples verified against the **official NPP user manual**

---

## 🧠 Regex Engine Used
Notepad++ uses the **Boost Regular Expression engine**, which is **similar to PCRE but not identical**.
This guide follows:
- **Regular expression search mode**
- [Official documentation](https://npp-user-manual.org/docs/searching/#regular-expressions)

---

## 📂 File Structure
```
.
├── README.md
└── regex-reference.md   (main cheat sheet)
```
*(Rename the file if yours is named differently)*
---

## 📝 How to Use in Notepad++
1. Open **Notepad++**
2. Press **Ctrl + F** or **Ctrl + H**
3. Select **Search Mode → Regular expression**
4. Copy a pattern from this repo
5. Paste it into **Find what**
6. Search / Replace as needed

---

## ✨ Example Use Cases

- 🔍 Find variable names
- 🧹 Remove comments from JavaScript files
- 🔢 Match digits or numeric IDs
- 🧾 Clean logs or formatted text
- 🧩 Learn regex step-by-step with real examples

---

## ⚠️ Important Notes
- Regex is **case-sensitive** unless *Match case* is disabled
- `.` does **not** match newline unless:

  - `. matches newline` is enabled, or
  - `(?s)` is used
- `{}` are **quantifiers**, not literals (must be escaped to match literally)
- Regex cannot fully parse programming languages — use carefully

---

## 📖 Source & References
- [Official Notepad++ Regex Documentation](https://npp-user-manual.org/docs/searching/#regular-expressions)

---

## 🤝 Contributing
Found a mistake or want to improve an example?
- Fork the repo
- Make your changes
- Open a Pull Request
Corrections and improvements are welcome 👍

---

## 📜 License
This project is released under the **MIT License**.
Feel free to use, modify, and share.
