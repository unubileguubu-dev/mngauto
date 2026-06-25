# MNG Auto Club — Brand Guidelines & Website Build Spec
**Prepared by EPAX · v1.0 · For use as Claude Code context**

> **HOW TO USE THIS FILE (read first, Claude Code):**
> This is the single source of truth for the MNG Auto Club website rebuild. Every color, font, spacing, and component decision below is binding. Do not introduce colors, fonts, or styles not defined here. Build mobile-first. The site's #1 job is **lead capture** (call / message / get pre-approved), not browsing. Design every page backward from "press to call." Stack: assume React + Tailwind unless told otherwise; tokens are provided as both CSS variables and a Tailwind config snippet below.

---

## 1. Brand snapshot

| | |
|---|---|
| **Name (canonical)** | MNG Auto Club |
| **What it is** | Mongolian-owned used-car dealership in Los Angeles, CA. DMV Approved Dealer #48175. |
| **Who it serves** | Primarily Mongolian immigrants & non-citizens in the US who struggle to get financed elsewhere; plus walk-in LA buyers and Mongolia-bound shipping clients. |
| **The one true value prop** | *"We get you financed and we speak your language."* Financing with **no SSN, no credit, no visa status required** + Mongolian-language trust + shipping to Mongolia and all 50 states. |
| **Look** | Disciplined gold-on-black. Premium, automotive, trustworthy — NOT flashy. |
| **Feel** | A handshake from someone in your community who actually gets you approved. |

**One-liner (use as hero):** *Drive home today — financed in Mongolian. No SSN, no credit, no status needed.*

---

## 2. Strategic decisions (locked — do not re-litigate)

These resolve real inconsistencies in the current assets. Build to these:

1. **One identity.** Use the **Luxury Motors gold-on-black logo** (the cleaner Facebook mark) as the primary logo. Drop the flag-heavy website logo. Tagline "Luxury Motors" is optional sub-text; the canonical brand name is **MNG Auto Club**.
2. **One address.** Confirm the live address with the client before launch. Default to **4322 Wilshire Blvd, Suite 102, Los Angeles, CA 90010** (the dealer-license address) unless the client says otherwise. Never show two.
3. **Kill the Amazon-yellow banner (#FFD814).** It cheapens the brand. The promo message lives in a gold-on-black ribbon instead.
4. **Lead with financing + trust, not luxury.** Inventory is reliable Japanese (Toyota/Honda/Lexus). Sell *access*, not exotics.
5. **Mobile-first, call-first.** Most buyers arrive on a phone from Facebook. A sticky "Call / Message" bar is mandatory on mobile.
6. **Bilingual EN ⇄ MN.** Every page ships in English and Mongolian (Cyrillic). Use a visible language toggle. Default language = English; remember choice.

---

## 3. Positioning — value props, ranked

Show them in this order on the homepage. Order = priority:

1. **Financing for everyone** — No SSN · No credit · No visa status · lowest rates, fast approval.
2. **We speak Mongolian** — buy a car in your own language, from your own community.
3. **We outpay CarMax & any dealer** — we also buy your car for more.
4. **Nationwide + Mongolia shipping** — delivered to any US city or shipped home.
5. **DMV Approved Dealer #48175** — licensed, legitimate, 4,800+ community followers.

---

## 4. Audience

| Segment | Need | What converts them |
|---|---|---|
| Mongolian immigrants / non-citizens | Can't get financed (no SSN/credit) | "No status needed" + Mongolian copy + phone call to a Mongolian rep |
| LA walk-in buyers | Reliable car, fair price | Clean inventory grid + price + mileage + "outpay CarMax" |
| Mongolia-bound buyers | Ship a US car home | Shipping section + WhatsApp/Messenger contact |

**Behavioral truth:** they're on a phone, scrolling from Facebook, and they convert by *calling or messaging* — not by filling a 12-field form. Make contact one tap.

---

## 5. Voice & tone

- **Confident, plain, warm.** No jargon, no hype words ("unbeatable," "amazing"). Specific beats clever.
- **Trust-first.** Every claim backs a worry: "No credit? Approved." "No SSN? Approved."
- **Bilingual parity.** Mongolian is a first-class language here, not a translation afterthought. Mongolian copy should read like a native wrote it, not Google Translate.
- **Active voice, real verbs.** "Get approved," "Call us," "See the car" — never "Submit" or "Inquire."

**Examples**
- ✅ "Get pre-approved in 10 minutes — no SSN, no credit needed."
- ✅ "Захидлаар бичээрэй — монголоор тусална." (Message us — we'll help in Mongolian.)
- ❌ "Inquire about our premium financing solutions."

---

## 6. Logo usage

- **Primary:** Luxury Motors gold-on-black mark (car silhouette + "MNG AUTO CLUB").
- **Clear space:** keep padding ≥ the height of the "M" on all sides.
- **Min width:** 120px on mobile nav, 160px on desktop.
- **Backgrounds:** gold logo on `onyx`/`carbon` only. On a light section, use an all-`onyx` (black) version of the mark. Never put the gold mark on the yellow ribbon or on a busy photo without a dark scrim.
- **Don't:** recolor, add the flag, stretch, add drop-shadows, or place on low-contrast photo.

---

## 7. Color tokens

Gold-on-black, warm, premium. The full system:

| Token | Hex | Role |
|---|---|---|
| `onyx` | `#0B0B0D` | Primary background |
| `carbon` | `#16161A` | Cards, elevated surfaces |
| `steel` | `#2A2A30` | Borders, dividers |
| `gold` | `#C9A24B` | Primary accent — CTAs, highlights, logo gold |
| `gold-bright` | `#E4C97A` | Hover/active, champagne highlight, price emphasis |
| `bone` | `#F5F3EE` | Primary text on dark (warm white, softer than #FFF) |
| `ash` | `#9A9AA2` | Secondary text, labels, captions |
| `mongol-red` | `#C8102E` | Heritage accent — ONLY in the "Mongolian-owned" badge / tiny flourishes |
| `success` | `#2E9E5B` | "In stock," "Approved" |
| `surface-light` | `#F5F3EE` | Optional light section bg (use sparingly) |

**Rules**
- Default page = dark (`onyx`). Gold is a spice, not a wallpaper — gold should cover < 10% of any screen.
- `mongol-red` appears in exactly one place: the "Монголын эзэмшилтэй / Mongolian-owned" trust badge. Nowhere else.
- Contrast: `bone` on `onyx` = ~16:1 (AAA). Never put `gold` text on `onyx` for body copy (fails contrast at small sizes) — gold is for large headings, borders, icons, and buttons only.

**CSS variables**
```css
:root {
  --onyx:#0B0B0D; --carbon:#16161A; --steel:#2A2A30;
  --gold:#C9A24B; --gold-bright:#E4C97A;
  --bone:#F5F3EE; --ash:#9A9AA2; --mongol-red:#C8102E;
  --success:#2E9E5B;
}
```

**Tailwind config**
```js
// tailwind.config.js → theme.extend.colors
colors: {
  onyx:'#0B0B0D', carbon:'#16161A', steel:'#2A2A30',
  gold:{ DEFAULT:'#C9A24B', bright:'#E4C97A' },
  bone:'#F5F3EE', ash:'#9A9AA2',
  mongol:'#C8102E', success:'#2E9E5B',
}
```

---

## 8. Typography

**Both faces MUST carry full Cyrillic glyphs** (Mongolian). Both below do. Verify rendering on a Cyrillic test string before launch: `Сайн байна уу, бид танд туслахад бэлэн байна.`

| Role | Typeface | Source | Use |
|---|---|---|---|
| Display / headings | **Saira** | Google Fonts | Hero, section titles, vehicle name, price. Slightly condensed = automotive/dashboard feel. Weights 600–800. |
| Body / UI / forms | **Inter** | Google Fonts | Paragraphs, labels, buttons, nav. Weights 400–600. |
| Numbers (price/mileage) | Inter or Saira w/ `font-variant-numeric: tabular-nums` | — | Always tabular figures so prices/mileage align. |

**Type scale (mobile → desktop, px)**
| Element | Mobile | Desktop | Weight |
|---|---|---|---|
| Hero H1 | 34 | 56 | Saira 800 |
| Section H2 | 26 | 38 | Saira 700 |
| Card title (vehicle) | 18 | 20 | Saira 600 |
| Price | 22 | 28 | Saira 700, `gold-bright` |
| Body | 16 | 17 | Inter 400 |
| Label / eyebrow | 12 | 13 | Inter 600, uppercase, `+0.08em` tracking, `ash` |

**Import**
```html
<link href="https://fonts.googleapis.com/css2?family=Saira:wght@500;600;700;800&family=Inter:wght@400;500;600&display=swap&subset=cyrillic,latin" rel="stylesheet">
```

---

## 9. Imagery

- **Real inventory photos only.** No stock photos of generic cars. The client already shoots cars in their indoor garage — that dark, controlled background actually works; keep it.
- **Show the odometer / mileage** as a trust signal where possible.
- **Treatment:** slight darkening at the bottom (gradient scrim `onyx` → transparent) so white text sits on any photo.
- **Aspect ratios:** inventory card image 4:3; hero 16:9 (desktop) / 4:5 (mobile); vehicle gallery 4:3.
- **Don't:** heavy filters, fake luxury showrooms, or flag overlays.

---

## 10. Page structure & build order

Build in this order. **Ship page 1 before touching page 2.**

### Page 1 — Homepage (the only page that must be perfect at launch)
```
┌────────────────────────────────┐
│ [logo]            [EN|MN] [☰]   │  sticky nav, transparent→solid on scroll
├────────────────────────────────┤
│ HERO (dark photo + scrim)       │
│  H1: Drive home today —         │
│      financed in Mongolian.     │
│  sub: No SSN · No credit ·      │
│       No status. Fast approval. │
│  [ Get pre-approved ] [ Call ]  │  gold primary + outline secondary
├────────────────────────────────┤
│ TRUST BAR  DMV #48175 · 4.8K ·  │  thin row, gold dividers
│  EN/KR/MN/中文 · Ships 50 states│
├────────────────────────────────┤
│ 5 VALUE PROPS (icon + 1 line)   │  order from §3
├────────────────────────────────┤
│ IN STOCK (inventory grid)       │  6–8 cards + "See all"
├────────────────────────────────┤
│ FINANCING (the money section)   │  "No SSN/credit/status" → form/CTA
├────────────────────────────────┤
│ SELL / TRADE  "We outpay CarMax"│
├────────────────────────────────┤
│ SHIPPING  US + Mongolia         │
├────────────────────────────────┤
│ FOOTER  address · phones · map  │
└────────────────────────────────┘
[ STICKY MOBILE BAR: Call · Message ]  ← always visible on mobile
```

### Page 2 — Inventory (filterable grid)
Filters: make, price range, mileage. Each card → vehicle detail.

### Page 3 — Vehicle detail
Gallery · year/make/model · price · mileage · "Est. monthly from $X" · sticky **[Call about this car] / [Message]** · "No credit? Still approved" reassurance.

### Page 4 — Financing / Get pre-approved
Short form: name · phone · car interested in · preferred language. **Max 4 fields.** Every extra field drops completion ~10%. Reassure: "No SSN required to start."

### Page 5 — Contact
3 named reps with direct phones, address, embedded map, Facebook/Instagram/YouTube, hours.

---

## 11. Components

**Buttons**
- Primary: `gold` bg, `onyx` text, 8px radius, Inter 600, hover → `gold-bright`. Used for the single most important action per section.
- Secondary: transparent, 1px `gold` border, `bone` text, hover → `carbon` fill.
- Tap target ≥ 48px height on mobile.

**Inventory card** (`carbon` bg, 8px radius, 1px `steel` border)
```
[ 4:3 photo, scrim bottom ]
2020 Toyota Camry LE Hybrid     ← Saira 600, bone
79,293 mi                        ← Inter, ash, tabular
$ / "from $XXX/mo"               ← Saira 700, gold-bright
[ See details ]                  ← secondary button, full width
```
Hover: border → `gold`, lift 2px.

**Trust bar** — single row, `ash` text, `gold` "·" dividers. Items: DMV #48175 · 4,800+ followers · EN/KR/MN/中文 · Ships nationwide & to Mongolia.

**Sticky mobile CTA bar** — fixed bottom, `carbon` bg, 1px `steel` top border, two buttons: **Call** (gold) + **Message** (outline). Non-negotiable.

**Language toggle** — `EN | MN` pill in nav, active = `gold` text. Persist choice (localStorage / cookie). All copy mirrored.

**Mongolian-owned badge** — small pill, `mongol-red` accent, "Монголын эзэмшилтэй · Mongolian-owned." The only place red appears.

**Radius scale:** cards/buttons 8px · inputs 6px · pills/badges full. **Spacing:** 4px base unit (4/8/12/16/24/32/48/64). Section vertical padding: 48px mobile / 96px desktop.

---

## 12. Signature element

**The "Approved" stamp moment.** On the financing section, a gold foil-style stamp/seal reading **APPROVED · НОГДУУЛСАН** that animates in on scroll (respect `prefers-reduced-motion`). It embodies the entire value prop — *you, specifically, get approved here* — in one image. This is the one place to spend boldness. Keep everything else quiet.

---

## 13. Copy library (starter — EN / MN)

| Slot | English | Mongolian (Cyrillic) |
|---|---|---|
| Hero H1 | Drive home today — financed in Mongolian. | Өнөөдөр машинтай боль — монголоор санхүүжүүлнэ. |
| Hero sub | No SSN · No credit · No status. Fast approval. | SSN, зээлийн түүх, визийн статус шаардлагагүй. Шуурхай зөвшөөрөл. |
| Primary CTA | Get pre-approved | Урьдчилан зөвшөөрөл авах |
| Secondary CTA | Call us | Залгах |
| Financing | No credit? No SSN? Still approved. | Зээлгүй юу? SSN-гүй юу? Бид зөвшөөрнө. |
| Sell/trade | We outpay CarMax and any dealer. | Бид CarMax болон бусад дилерээс илүү төлнө. |
| Shipping | Delivered anywhere in the US — or shipped home to Mongolia. | АНУ-ын аль ч хотод хүргэнэ — эсвэл Монгол руу тээвэрлэнэ. |

*Replace with client-confirmed wording before launch; keep this tone.*

---

## 14. Don'ts

- ❌ No Amazon-yellow (`#FFD814`) anywhere.
- ❌ No two logos, two names, or two addresses.
- ❌ No flag/Soyombo backgrounds (heritage = one small red badge only).
- ❌ No gold body text (fails contrast).
- ❌ No long contact forms (4 fields max).
- ❌ No stock photos of cars.
- ❌ No "luxury exotic" posturing the inventory can't back.
- ❌ No English-only sections. Parity always.

---

## 15. Pre-launch checklist

- [ ] One address confirmed with client
- [ ] Cyrillic renders in Saira + Inter (test string)
- [ ] Sticky mobile call/message bar works
- [ ] Lighthouse mobile performance ≥ 90
- [ ] All CTAs are tap-to-call / tap-to-message (`tel:` / Messenger / WhatsApp links)
- [ ] EN/MN parity on every page
- [ ] Real inventory photos, not placeholders
- [ ] Keyboard focus visible, `prefers-reduced-motion` respected
