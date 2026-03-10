# ⛳ Golf Score Translator

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

> A lightweight JavaScript utility that converts a golf score into its traditional golf terminology — from **Hole-in-one** to **Go Home!**

---

## 📋 Table of Contents

- [Features](#-features)
- [Demo](#-demo)
- [Installation](#-installation)
- [Usage](#-usage)
- [Score Reference](#-score-reference)
- [API](#-api)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

- ✅ Covers all standard golf score terms
- ✅ Handles edge cases (e.g. Hole-in-one always triggers at 1 stroke)
- ✅ Uses strict equality (`===`) for reliable comparisons
- ✅ Zero dependencies — pure vanilla JavaScript
- ✅ Lightweight and easy to integrate into any project

---

## 🎮 Demo

```javascript
golfScore(5, 1);  // ⛳ "Hole-in-one!"
golfScore(5, 2);  // 🦅 "Eagle"
golfScore(4, 3);  // 🐦 "Birdie"
golfScore(4, 4);  // ✅ "Par"
golfScore(4, 5);  // 😬 "Bogey"
golfScore(4, 6);  // 😓 "Double Bogey"
golfScore(4, 7);  // 🏠 "Go Home!"
```

---

## 📦 Installation

No installation required! Just copy the function into your project.

```bash
# Clone the repository
git clone https://github.com/your-username/golf-score-translator.git

# Navigate into the project
cd golf-score-translator
```

Or simply grab the function directly:

```javascript
function golfScore(par, strokes) {
  if (strokes === 1) {
    return "Hole-in-one!";
  } else if (strokes <= par - 2) {
    return "Eagle";
  } else if (strokes === par - 1) {
    return "Birdie";
  } else if (strokes === par) {
    return "Par";
  } else if (strokes === par + 1) {
    return "Bogey";
  } else if (strokes === par + 2) {
    return "Double Bogey";
  } else {
    return "Go Home!";
  }
}
```

---

## 🚀 Usage

```javascript
const result = golfScore(4, 3);
console.log(result); // "Birdie"
```

You can also use it dynamically with user input:

```javascript
const par = parseInt(prompt("Enter par:"));
const strokes = parseInt(prompt("Enter strokes:"));
console.log(golfScore(par, strokes));
```

---

## 📊 Score Reference

| Strokes       | Term             | Description                        |
|---------------|------------------|------------------------------------|
| 1             | 🏆 Hole-in-one!  | One stroke, regardless of par      |
| ≤ par - 2     | 🦅 Eagle         | Two or more under par              |
| par - 1       | 🐦 Birdie        | One stroke under par               |
| par           | ✅ Par           | Exactly at par                     |
| par + 1       | 😬 Bogey         | One stroke over par                |
| par + 2       | 😓 Double Bogey  | Two strokes over par               |
| ≥ par + 3     | 🏠 Go Home!      | Three or more strokes over par     |

---

## 📖 API

### `golfScore(par, strokes)`

| Parameter | Type     | Required | Description                       |
|-----------|----------|----------|-----------------------------------|
| `par`     | `Number` | ✅ Yes   | The par value for the hole        |
| `strokes` | `Number` | ✅ Yes   | The number of strokes taken       |

**Returns:** `String` — the golf score term.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

<p align="center">Made with ❤️ and JavaScript</p>
