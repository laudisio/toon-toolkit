# 🚀 TOON Toolkit

**JSON ↔ TOON Converter and LLM Token Optimizer**

TOON Toolkit is a Chrome extension that helps developers **reduce token usage in AI prompts** by converting verbose JSON structures into a compact TOON format.

> **TOON (Token Optimized Object Notation)** is a lightweight representation of structured data designed to improve efficiency when working with Large Language Models (LLMs).

---

## 💡 Why TOON?

Structured data like JSON can be extremely verbose in prompts sent to AI models.

➡️ More characters → more tokens → higher API costs  

TOON reduces unnecessary syntax while preserving structure, making it ideal for:

- Prompt engineering  
- LLM pipelines  
- AI agents  
- Structured prompt inputs  

With TOON Toolkit you can instantly convert between formats and estimate token savings.

---

## ✨ Features

- 🔄 Convert **JSON → TOON**
- 🔁 Convert **TOON → JSON**
- 📊 Real token counting using modern LLM encodings
- 💰 Estimate token savings
- 📉 Estimate cost impact per model
- 🤖 Support for multiple model encodings
- 🧼 Clean and simple developer interface
- 🔒 Works entirely offline  

> ⚠️ No data is sent to external servers.

---

## 📦 Example

### JSON

```json
{
  "users":[
    {"id":1,"name":"Alice","role":"admin"},
    {"id":2,"name":"Bob","role":"editor"}
  ]
}
```

### TOON

```txt
users[2]{id,name,role}:
1,Alice,admin
2,Bob,editor
```

✅ TOON provides a more compact representation while maintaining structure.

---

## 📊 Token Savings

TOON Toolkit helps visualize token reduction directly inside the extension.

### Example workflow:

1. Paste JSON  
2. Convert to TOON  
3. View token comparison  
4. Estimate cost impact for your model  

This helps optimize prompts for models such as:

- GPT-4o  
- GPT-4.1  
- GPT-4o-mini  
- Other LLM systems  

---

## 📐 TOON Format

TOON (Token Optimized Object Notation) is designed to be:

- Compact  
- Readable  
- Deterministic  
- JSON compatible  

---

### 🔹 Basic Example

#### JSON

```json
{
  "user": {
    "id": 101,
    "name": "Alice"
  }
}
```

#### TOON

```txt
user:
  id: 101
  name: Alice
```

---

### 🔹 Arrays

#### JSON

```json
{
  "roles": ["admin","editor"]
}
```

#### TOON

```txt
roles:
  [admin, editor]
```

---

### 🔹 Table Format (Optimized)

#### JSON

```json
{
 "users":[
  {"id":1,"name":"Alice","role":"admin"},
  {"id":2,"name":"Bob","role":"editor"}
 ]
}
```

#### TOON

```txt
users[2]{id,name,role}:
1,Alice,admin
2,Bob,editor
```

---

## 🔐 Privacy

TOON Toolkit processes all data **locally in the browser**.

The extension:

- ❌ Does **not collect user data**
- ❌ Does **not send data to servers**
- ❌ Does **not track usage**

👉 See the full privacy policy:  
[https://laudisi.github.io/toon-toolkit/
](https://laudisio.github.io/toon-toolkit/)
---

## ⚙️ Installation

### 🧩 Chrome Web Store
Install directly from the Chrome Web Store.

---

## 🧑‍💻 Development

### 🛠 Tech Stack

- JavaScript  
- Vite  
- Chrome Extension (Manifest v3)  

---

### 📁 Project Structure

```bash
/core
  json-to-toon.js
  toon-to-json.js
  tokenizer.js

/popup
  popup.html
  popup.js
  popup.css

/public
  manifest.json
  icons
```

---

## 🤝 Contributing

Contributions are welcome!

If you have ideas for improving the TOON format or the extension, feel free to open an issue.

---

## 👨‍💻 Author

Created by **Rafael Laudisio dos Santos**

Built to help developers optimize structured data for AI systems.
