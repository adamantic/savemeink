# 🖨️ Save Me Ink

**Free tool to reduce PDF ink usage for printing. Save money, save the planet.**

🌐 **Live at:** [savemeink.com](https://savemeink.com)

---

## The Problem

Printing is expensive. A single ink cartridge can cost $30-50, and most of that ink goes toward:

- Gray backgrounds
- Subtle gradients and shadows
- Anti-aliased text edges
- Color elements you don't need in black & white

**The average document wastes 30-50% of ink** on visual elements that don't improve readability.

---

## The Solution

Save Me Ink converts your PDFs to **pure black and white** using adaptive thresholding. This removes all the unnecessary gray tones while keeping text and images perfectly legible.

### Before & After

| Before | After |
|--------|-------|
| Grays, gradients, shadows | Pure black & white |
| Heavy ink usage | Minimal ink usage |
| Expensive to print | Cheap to print |

---

## How It Works

1. **Upload** your PDF (drag & drop or click)
2. **Process** — we convert each page to pure black & white
3. **Download** your ink-optimized PDF
4. **Print** and save money 💰

### Technical Details

Under the hood, Save Me Ink:

1. Renders each PDF page to a high-resolution canvas using [pdf.js](https://mozilla.github.io/pdf.js/)
2. Applies adaptive thresholding to convert all pixels to pure black or white
3. Reconstructs the PDF using [pdf-lib](https://pdf-lib.js.org/)

The threshold algorithm analyzes each pixel's brightness and converts it to either black (ink) or white (no ink). This eliminates all the gray tones that waste ink.

---

## 🔒 100% Private

**Your files never leave your device.**

All processing happens directly in your browser using JavaScript. We don't upload your files to any server. We can't see your documents. Nobody can.

This isn't just a privacy feature — it's the architecture. There is no server.

---

## Benefits

### 💰 Save Money
Reduce ink usage by 30-70% depending on the document. Over a year of printing, that adds up to real savings.

### 🌍 Better for the Environment
Less ink = less plastic cartridges = less waste. Ink cartridges are notoriously bad for the environment.

### ⚡ Fast & Free
Process PDFs in seconds. No sign-up, no limits, no cost. Ever.

### 🔒 Private by Design
Your documents stay on your device. We literally cannot see them.

---

## Why We Built This

Printing shouldn't cost a fortune. Students printing lecture notes, small businesses printing invoices, anyone printing anything — they're all paying an "ink tax" on content that would look just as good in pure black and white.

We built Save Me Ink to give that money back.

---

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS
- **PDF Reading:** [pdf.js](https://mozilla.github.io/pdf.js/) (Mozilla)
- **PDF Writing:** [pdf-lib](https://pdf-lib.js.org/)
- **Hosting:** [Cloudflare Pages](https://pages.cloudflare.com/) (free tier)
- **Backend:** None! 100% client-side

---

## Self-Hosting

Want to run your own instance? It's just a static HTML file:

```bash
git clone https://github.com/adamantic/savemeink.git
cd savemeink
# Open index.html in your browser, or serve with any static server:
python -m http.server 8000
```

---

## Contributing

PRs welcome! Some ideas:

- [ ] Adjustable threshold slider
- [ ] Batch processing (multiple PDFs)
- [ ] Preview before/after comparison
- [ ] PWA support for offline use
- [ ] Dark mode toggle (ironic, we know)

---

## License

MIT — do whatever you want with it.

---

Made with 🦀 by [adamantic](https://github.com/adamantic)
