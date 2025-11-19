# 🔧 Data Formatter — JavaScript

<p align="center">
  <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="640" />
</p>

A lightweight **Data Formatter** utility built with **JavaScript** that helps transform, validate, and pretty-print data structures (JSON, CSV, XML, TSV). The project focuses on providing easy-to-use formatting tools and visual previews — ideal for developers, QA engineers, and data analysts.

---

## 🚀 Features

✔ Pretty-print JSON with collapsible sections
✔ Convert CSV ↔ JSON bidirectionally
✔ Minify / Beautify JSON
✔ Validate JSON schema (basic)
✔ Sort object keys and format arrays
✔ Export formatted data as a file
✔ Keyboard shortcuts for quick actions
✔ Live preview with syntax highlighting

---

## 🎨 Matrix Animation

This README includes a matrix-style animated banner to give the tool a modern, techy look. The animation is purely decorative and does not affect the formatter functionality.

---


---

## 🧩 Example Code Snippets

### ✅ Pretty-print JSON

```javascript
function prettyPrint(jsonStr) {
  try {
    const obj = JSON.parse(jsonStr);
    return JSON.stringify(obj, null, 2);
  } catch (e) {
    throw new Error('Invalid JSON');
  }
}
```

### ✅ CSV → JSON (simple)

```javascript
function csvToJson(csv) {
  const lines = csv.split('\n');
  const headers = lines[0].split(',');
  return lines.slice(1).map(line => {
    const values = line.split(',');
    return headers.reduce((obj, header, i) => (obj[header.trim()] = values[i].trim(), obj), {});
  });
}
```

### ✅ Download formatted result

```javascript
function download(filename, text) {
  const a = document.createElement('a');
  a.href = URL.createObjectURL(new Blob([text], {type: 'text/plain'}));
  a.download = filename;
  a.click();
  URL.revokeObjectURL(a.href);
}
```

---

## ▶ How to Run

1. Clone the repo:

```
git clone https://github.com/your-username/data-formatter-js.git
cd data-formatter-js
```

2. Open `index.html` in a browser:

```
open index.html
```

---

## 🛠 Tech Stack

* **JavaScript** — Core formatter logic
* **HTML/CSS** — UI & animations
* **Prism.js / Highlight.js** — Syntax highlighting (optional)

---

## ✨ Future Enhancements

* Schema-driven validation (JSON Schema support)
* Advanced CSV parsing (commas in quotes, multiline fields)
* XML ↔ JSON conversion
* Live collaborative editing
* Desktop app wrapper using Electron

---

<p align="center">
  <b>Format smart. Inspect fast. Ship better. 🚀</b>
</p>
