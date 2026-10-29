# Kivu Bites: restaurant website template

**A fast, bilingual restaurant website where customers build an order and send it on WhatsApp, the way people in Goma already order food.**

🔗 **Live demo:** https://patricksafari840.github.io/kivu-bites/

> Kivu Bites is a fictional lakeside grill. The site is a template I use to show small businesses (restaurants, snack bars, hotels) what a modern website can do for them.

## Features

- **Menu with photos**, categories (lake fish, grill, Congolese classics, sides, drinks) and tags (spicy, vegetarian, chef's pick).
- **Dollar and franc prices**: every price is shown in USD with the CDF equivalent (rate set in one place).
- **Cart + WhatsApp ordering**: add dishes, choose pickup or delivery, add a name, address and note; the site writes a clean order message and opens WhatsApp with it. No app or payment gateway needed.
- **Live open/closed status** calculated in Goma time (`Africa/Lubumbashi`, UTC+2), whatever the visitor's time zone, plus the weekly opening hours with today highlighted.
- **Bilingual EN/FR**, remembers the visitor's choice; the order message is written in the same language.
- **SEO ready**: meta and Open Graph tags, `Restaurant` structured data (JSON-LD), lazy-loaded images, map from OpenStreetMap.
- Responsive and accessible: works on cheap Android phones, respects reduced motion.

## Make it yours

Everything a client would change is at the top of the script in `index.html`:

```js
const CONFIG = {
  name: 'Kivu Bites',
  whatsapp: '243819405130',   // the restaurant's WhatsApp number
  fcPerUsd: 2850,             // exchange rate for franc prices
  deliveryFeeUsd: 2,
  timeZone: 'Africa/Lubumbashi',
  hours: { 0: ['12:00','21:00'], 1: ['11:00','22:00'], /* … */ }
};
const MENU = [ /* dishes with price, category, photo, EN/FR text */ ];
```

Food photos in `img/` were generated with AI (Higgsfield) for this demo; a real client would use photos of their own dishes.

## Tech

Plain HTML, CSS and JavaScript in one file: no framework, no build step, hosted free on GitHub Pages. Fonts: Fraunces and DM Sans (Google Fonts).

## Run locally

```bash
git clone https://github.com/PatrickSafari840/kivu-bites.git
cd kivu-bites
python -m http.server 8000   # then open http://localhost:8000
```

---

Designed and built by **Patrick Safari**: websites, visuals and AI video ads for businesses in Goma and beyond · [Portfolio](https://patricksafari840.github.io/patrick_safari_portfolio/) · [Services](https://patricksafari840.github.io/patrick_safari_portfolio/services.html) · [LinkedIn](https://www.linkedin.com/in/patrick-safari-166077255/)

Licensed under the MIT License.
