# AI EMI Calculator

India's first **AI-powered EMI calculator** with natural language support. Calculate EMI, FD returns, SIP growth, loan affordability, and more — by just typing in plain English or Hinglish.

**[Live Demo](https://gocredit.money/embed/emi-calculator)** | **[Get Embed Code](https://gocredit.money/emi-calculator-widget)**

![AI EMI Calculator](https://gocredit.money/logo-ai.png)

## Features

### Two Modes
- **Calculator Mode** — Traditional sliders for 6 loan types (Personal, Home, Car, Education, Gold, Two-Wheeler)
- **AI Chat Mode** — Type natural language queries like "5 lakh loan at 12% for 3 years"

### AI Chat Supports
- **EMI Calculation** — "5 lakh personal loan at 14% for 3 years"
- **Home/Car/Education Loans** — "30 lakh home loan at 8.5% for 20 years"
- **FD Returns** — "FD 10 lakh at 7.5% for 5 years"
- **SIP Growth** — "SIP 5000 monthly at 12% for 10 years"
- **Loan Affordability** — "How much loan on 40000 salary"
- **Rate Comparison** — "Compare 10.5% vs 14% on 5 lakh for 3 years"
- **Prepayment Impact** — "Prepay 1 lakh on 10 lakh loan at 12% for 5 years"
- **Hinglish** — "40000 salary pe kitna loan milega"

### Technical
- **Single HTML file** — no build tools, no dependencies, no frameworks
- **32KB total** — inline CSS + JS, loads instantly
- **100% client-side** — no API calls, no tracking, no cookies
- **Mobile-first responsive** — works on all screen sizes
- **XSS-safe** — user input is sanitized via DOM textContent
- **Accurate** — uses standard reducing balance EMI formula, quarterly compounding for FD

## Quick Start

### Option 1: Embed via iframe (recommended)

```html
<iframe
  src="https://gocredit.money/embed/emi-calculator"
  width="100%"
  height="600"
  style="border:none;border-radius:16px;max-width:540px;"
  title="AI EMI Calculator"
></iframe>
```

### Option 2: Self-host

1. Download `index.html`
2. Serve it from your own domain
3. That's it — single file, no dependencies

```bash
# Clone
git clone https://github.com/quaterni0n/gocredit-emi-calculator.git
cd gocredit-emi-calculator

# Serve locally
python3 -m http.server 8080
# Open http://localhost:8080
```

### Option 3: Open directly

Just open `index.html` in any browser. It works offline too.

## Embed Sizes

| Size | Code |
|------|------|
| Default (540px) | `width="540px" height="600"` |
| Full Width | `width="100%" height="600"` |
| Compact (400px) | `width="400px" height="620"` |

## Loan Types & Rate Ranges

| Loan Type | Rate Range | Max Tenure |
|-----------|-----------|------------|
| Personal | 10.49% – 36% | 7 years |
| Home | 8.35% – 14% | 30 years |
| Car | 8.5% – 16% | 7 years |
| Education | 8% – 15% | 15 years |
| Gold | 7% – 18% | 5 years |
| Two-Wheeler | 9% – 24% | 4 years |

## Calculation Formulas

### EMI (Reducing Balance)
```
EMI = P × r × (1+r)^n / ((1+r)^n - 1)
where P = principal, r = monthly rate, n = months
```

### FD Maturity (Quarterly Compounding)
```
Maturity = P × (1 + R/4)^(4×Y)
where P = principal, R = annual rate, Y = years
```

### SIP Future Value
```
FV = S × ((1+r)^n - 1) / r × (1+r)
where S = monthly SIP, r = monthly rate, n = months
```

### Affordability (FOIR 50%)
```
Max EMI = Salary × 0.5
Max Loan = reverse EMI formula with Max EMI
```

## Customization

The widget uses a purple (#6C5CE7) theme. To customize:

1. Download `index.html`
2. Find and replace `#6C5CE7` with your brand color
3. Update the "Powered by" footer with your branding
4. Host on your domain

## Browser Support

Works in all modern browsers:
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## License

MIT License — free for personal and commercial use.

## Built by

[GoCredit](https://gocredit.money) — India's first AI-powered personal finance platform. Compare 55+ lenders, get instant loan offers.

---

**Star this repo** if you find it useful! Contributions welcome.
