# VS Code GLOSSA (ΓΛΩΣΣΑ)

![Version](https://img.shields.io/badge/version-0.0.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)

Language support for **GLOSSA (ΓΛΩΣΣΑ)**, the Greek educational programming language used in secondary education.

---

## ✨ Features

- **Syntax Highlighting** — Full support for Greek keywords, operators, and constructs
- **File Association** — Automatic recognition of `.gls` and `.glo` files
- **Comment Support** — Line comments with `!` (exclamation mark)
- **Bracket Matching** — Auto-closing and matching for brackets and quotes
- **Code Folding** — Collapse/expand code blocks

### Supported Keywords

| Category | Keywords |
|----------|----------|
| **Program Structure** | `ΠΡΟΓΡΑΜΜΑ`, `ΑΛΓΟΡΙΘΜΟΣ`, `ΑΡΧΗ`, `ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ`, `ΤΕΛΟΣ` |
| **Declarations** | `ΣΤΑΘΕΡΕΣ`, `ΜΕΤΑΒΛΗΤΕΣ` |
| **Data Types** | `ΑΚΕΡΑΙΕΣ`, `ΠΡΑΓΜΑΤΙΚΕΣ`, `ΧΑΡΑΚΤΗΡΕΣ`, `ΛΟΓΙΚΕΣ` |
| **Control Flow** | `ΑΝ`, `ΤΟΤΕ`, `ΑΛΛΙΩΣ`, `ΑΛΛΙΩΣ_ΑΝ`, `ΤΕΛΟΣ_ΑΝ` |
| **Loops** | `ΟΣΟ`, `ΕΠΑΝΑΛΑΒΕ`, `ΓΙΑ`, `ΑΠΟ`, `ΜΕΧΡΙ`, `ΜΕ_ΒΗΜΑ`, `ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ` |
| **I/O** | `ΔΙΑΒΑΣΕ`, `ΓΡΑΨΕ` |
| **Logical** | `ΚΑΙ`, `Η`, `ΟΧΙ`, `ΑΛΗΘΗΣ`, `ΨΕΥΔΗΣ` |
| **Operators** | `div`, `mod`, `←`, `<-` |

---

## 📖 Usage

Create a file with `.gls` or `.glo` extension and start writing GLOSSA code:

```glossa
ΠΡΟΓΡΑΜΜΑ Έλεγχος_Χρωμάτων
! Αυτό είναι ένα σχόλιο για δοκιμή
! Σκοπός: Να ελέγξουμε αν το VS Code χρωματίζει σωστά τις λέξεις

ΣΤΑΘΕΡΕΣ
  ΠΙ = 3.14159
  ΜΗΝΥΜΑ = "Καλημέρα Κόσμε"

ΜΕΤΑΒΛΗΤΕΣ
  ΑΚΕΡΑΙΕΣ: Ι, Μετρητής, Αποτέλεσμα
  ΠΡΑΓΜΑΤΙΚΕΣ: Μέσος_Όρος, Τιμή
  ΛΟΓΙΚΕΣ: Βρέθηκε
  ΧΑΡΑΚΤΗΡΕΣ: Όνομα

ΑΡΧΗ
  ! Είσοδος / Έξοδος
  ΓΡΑΨΕ 'Δώσε έναν αριθμό:'
  ΔΙΑΒΑΣΕ Τιμή

  ! Δομές Επιλογής
  ΑΝ Τιμή > 0 ΤΟΤΕ
    ΓΡΑΨΕ "Θετικός"
  ΑΛΛΙΩΣ_ΑΝ Τιμή = 0 ΤΟΤΕ
    ΓΡΑΨΕ "Μηδέν"
  ΑΛΛΙΩΣ
    ΓΡΑΨΕ "Αρνητικός"
  ΤΕΛΟΣ_ΑΝ

  ! Δομές Επανάληψης
  Μετρητής <-- 0
  ΟΣΟ Μετρητής < 10 ΕΠΑΝΑΛΑΒΕ
    Μετρητής <-- Μετρητής + 1
  ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ

  ΓΙΑ Ι ΑΠΟ 1 ΜΕΧΡΙ 100 ΜΕ_ΒΗΜΑ 2
    Αποτέλεσμα <-- Ι mod 2
    Αποτέλεσμα <-- Ι div 2
  ΤΕΛΟΣ_ΕΠΑΝΑΛΗΨΗΣ

  ! Λογικές Πράξεις
  Βρέθηκε <-- ΑΛΗΘΗΣ
  ΑΝ (ΟΧΙ Βρέθηκε) ΚΑΙ (Τιμή <> 5) ΤΟΤΕ
    ΓΡΑΨΕ "Συνθήκη Αληθής"
  ΤΕΛΟΣ_ΑΝ

ΤΕΛΟΣ_ΠΡΟΓΡΑΜΜΑΤΟΣ
```

---

## ⚙️ Recommended Settings

For the best experience with Greek characters, add these settings to your VS Code `settings.json`:

```json
{
  "editor.unicodeHighlight.ambiguousCharacters": false,
  "editor.unicodeHighlight.nonBasicASCII": false
}
```

This disables Unicode highlighting warnings for Greek characters.

---

## 🐛 Known Issues

1. **Unicode Highlighting Warnings** — VS Code may show warnings for Greek characters. Disable Unicode highlighting in settings (see above).
2. **Font Rendering** — Some fonts may not render Greek characters properly. We recommend using fonts with good Greek support (e.g., Consolas, JetBrains Mono, Fira Code).

---

## 📋 Requirements

- VS Code version 1.70.0 or higher

---

## 🗺️ Roadmap

- [x] Syntax Highlighting
- [x] File Association (`.gls`, `.glo`)
- [ ] Code Snippets for common constructs
- [ ] IntelliSense and Auto-completion
- [ ] Error Diagnostics
- [ ] Debugging Support

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit [issues](https://github.com/Sotiris01/glossa-vscode/issues) and pull requests on [GitHub](https://github.com/Sotiris01/glossa-vscode).

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Inspired by [markoutso/glo](https://github.com/markoutso/glo.git)
- The Greek educational community using GLOSSA
- VS Code Extension development documentation
- TextMate grammar specification

---

## 👤 Author

**Mpalatsias Sotiris**

- GitHub: [@Sotiris01](https://github.com/Sotiris01)
- Email: sotiris.mp@gmail.com

---

**Enjoy coding in ΓΛΩΣΣΑ! 🇬🇷**
