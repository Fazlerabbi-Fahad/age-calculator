# 🎂 Age Calculator — #001 of 100

> **100 Websites Challenge** — Website number one. A beautiful, precise, and fully responsive Age Calculator built with React.

---

## ✨ Features

- **Exact age** — Years, months, and days calculated to today
- **Extended breakdowns** — Total months, weeks, days, hours, and minutes lived
- **Day of birth** — Tells you what day of the week you were born on
- **Next birthday countdown** — Shows the exact date and how many days away it is
- **Animated count-up numbers** — Results animate in smoothly on calculation
- **Input validation** — Inline error messages with shake animation for invalid dates
- **Keyboard support** — Press `Enter` to calculate instantly
- **Fully responsive** — Works seamlessly from 360px mobile up to wide desktop

---

## 🖥️ Preview

| Input Screen | Results Screen |
|---|---|
| Clean date inputs with DD / MM / YYYY fields | Hero age display + stats grid + fun facts + birthday countdown |

**Design aesthetic:** Dark luxury — deep navy/charcoal backgrounds, gold (`#e8c97e`) as the primary accent, purple and cyan secondary pops. Typography: *Playfair Display* for headings, *DM Mono* for numbers, *DM Sans* for body text.

---

## 🚀 Getting Started

### Prerequisites

- Node.js 16+
- React 18+

### Installation

```bash
# Clone the repo (or copy the single file into your project)
git clone https://github.com/your-username/age-calculator.git
cd age-calculator

# Install dependencies
npm install

# Start the development server
npm run dev
```

### Using as a standalone component

Just drop `AgeCalculator.jsx` into any existing React project — it has **zero external dependencies** beyond React itself.

```jsx
import AgeCalculator from './AgeCalculator';

function App() {
  return <AgeCalculator />;
}
```

No additional CSS imports or setup needed — all styles are self-contained inside the component.

---

## 🗂️ Project Structure

```
age-calculator/
├── src/
│   └── AgeCalculator.jsx   # Single-file component (all styles included)
├── public/
│   └── index.html
├── package.json
└── README.md
```

---

## 🧮 How the Age Calculation Works

The calculator uses JavaScript's native `Date` object for precise arithmetic:

1. **Years, months, days** — Calculated by comparing today's date to the birth date, borrowing days/months as needed for accuracy.
2. **Total days** — `Math.floor((today - birthDate) / 86400000)`
3. **Total weeks** — `totalDays / 7`
4. **Total hours / minutes** — Derived from total days (does not include the current partial day's hours)
5. **Next birthday** — Constructs this year's birthday; if already passed, advances to next year

---

## 🎨 Design Tokens

```css
--bg:       #0a0a0f   /* Deep space black */
--surface:  #12121a   /* Card surface */
--card:     #1a1a26   /* Elevated card */
--accent:   #e8c97e   /* Gold — primary accent */
--accent2:  #c77dff   /* Purple — secondary */
--accent3:  #48cae4   /* Cyan — tertiary */
--text:     #f0eeff   /* Off-white text */
--muted:    #6e6e8a   /* Subdued labels */
--error:    #ff6b6b   /* Validation errors */
```

**Fonts loaded from Google Fonts:**
- `Playfair Display` — 400, 700, 900
- `DM Mono` — 300, 400, 500
- `DM Sans` — 300, 400, 500

---

## 📦 Dependencies

| Package | Version | Purpose |
|---|---|---|
| `react` | ^18.0.0 | UI framework |
| `react-dom` | ^18.0.0 | DOM rendering |

No other libraries. No CSS frameworks. No UI kits.

---

## 🛠️ Built With

- **React 18** — Functional components with hooks (`useState`, `useEffect`, `useRef`)
- **CSS-in-JS** — Scoped styles injected via a `<style>` tag inside the component
- **Google Fonts** — Typography loaded via `@import`
- **Native Date API** — No external date libraries

---

## 📋 Validation Rules

| Field | Rule |
|---|---|
| Day | 1 – 31 (also validated against the actual calendar month) |
| Month | 1 – 12 |
| Year | 1900 – current year |
| Full date | Must be a real calendar date, not in the future |

---

## 🗺️ Roadmap

- [ ] Zodiac sign display
- [ ] Chinese zodiac year
- [ ] Share your age as an image card
- [ ] Dark/light theme toggle
- [ ] Birthstone and birth flower info
- [ ] Time zone–aware calculation

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

```bash
# Fork → clone → branch → push → PR
git checkout -b feature/your-feature-name
```

---

## 📄 License

MIT © Fahad — feel free to use, fork, and build on this.

---

> *Part of the **100 Websites in 100 Days** challenge — building one website every day to sharpen design, development, and shipping speed.*
