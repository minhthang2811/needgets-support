# Needgets support site

The public web pages for [Needgets](https://minhthang2811.github.io/needgets-support/),
beautiful widgets for the iPhone and iPad Home Screen and Lock Screen. The app's own code is in a
private repository; this one holds only what App Store Connect and the app link to.

## Pages

| Page | English | Vietnamese | Linked from |
|---|---|---|---|
| `index.html` | https://minhthang2811.github.io/needgets-support/ | https://minhthang2811.github.io/needgets-support/#vi | App Store Connect Support URL and Marketing URL |
| `privacy/index.html` | https://minhthang2811.github.io/needgets-support/privacy/ | https://minhthang2811.github.io/needgets-support/privacy/#vi | App Store Connect Privacy Policy URL; the app's Settings, paywall and onboarding |

Each page holds English, then Vietnamese, at one address. `site.js` shows one language at a time:
the one the address names (`#vi`), or else the browser's language. Without JavaScript both halves show.

- **Support** (`index.html`): the app's screens, what it does, help in four groups (widgets,
  designs, Needgets Pro, your data), how to reach us, and the policy in one line.
- **Privacy policy** (`privacy/index.html`): the policy at a glance, then fifteen numbered
  sections. It covers what Guideline 5.1.1(i) asks for (what is collected and how it is used,
  third parties, retention and deletion, and withdrawing consent).

## Files

| File | What it is |
|---|---|
| `index.html`, `privacy/index.html` | The two pages |
| `style.css` | The one stylesheet, in the app's own colours: lavender paper, one ember accent, SF Pro Rounded headings |
| `site.js` | The language switch and the table of contents. It stores nothing |
| `icons.svg` | The icons, as one sprite (adapted from Lucide, ISC License) |
| `images/*.jpg` | The app's screens, 660 px wide, in English and Vietnamese (`-en`, `-vi`) |
| `images/og.jpg` | The 1200 × 630 card shown when a page is shared |
| `icon.png`, `apple-touch-icon.png`, `favicon.png` | The app icon at 192, 180 and 64 px |
| `.nojekyll` | Keeps GitHub Pages from running Jekyll over the site |

The pages load nothing from other sites (no web fonts, scripts or analytics), so reading the
privacy policy tells no one.

## Previewing and publishing

Plain HTML with one stylesheet and no build step. To preview, serve the folder with
`python3 -m http.server 8000` and open <http://localhost:8000/>. GitHub Pages serves `main`, `/`,
so a change goes live a minute or so after it lands on `main`.

## Changing the privacy policy

If the app starts to collect, send or keep any new data, update the policy before that version
ships: both halves, and the effective date in each (*Effective …* and *Có hiệu lực từ …*). Then
check that the App Privacy answers in App Store Connect and the app's `PrivacyInfo.xcprivacy` still agree.
