# Rochester Lodge — New Patient Funnel (Campaign 3: Cosmetic New Patient)

Lead-generation landing page for the **New Patient Check-Up + £100 Off
Whitening** campaign. Built from the Smile Makeover funnel template —
same brand system (navy `#1E2238`, gold CTA family, logo gold `#AF9651`,
Marcellus + Raleway), same photography, same form/webhook/thank-you
architecture. Only the campaign texts differ.

**The offer** (from the running ad copy):
- New patient check-up — £50, reduced from £72
- £100 off professional, dentist-led whitening
- Over £120 in total savings · limited spaces this month

## Files

| File | Purpose |
|---|---|
| `index.html` | The funnel page — self-contained HTML/CSS/JS. Indexable. |
| `thank-you.html` | Confirmation page; carries the **single** conversion-event block. Permanently `noindex`. |
| `assets/` | Brand symbol, practice photography, before/after cases. |

## Hero variants (message match)

| URL | Hero |
|---|---|
| plain or `?src=meta` | *New patient check-up + £100 off whitening* |
| `?src=google` | *£50 New Patient Check-Up in Bromley + £100 Off Whitening* |
| `?angle=checkup` | *Your £50 new patient check-up* |
| `?angle=whitening` | *£100 off professional whitening* |

## Wiring

- **Lead delivery** — the form POSTs to this campaign's GHL inbound
  webhook (`…/webhook-trigger/KN0ZBAZ8T97LgaKYA35a`) with goal, timing,
  name, phone, email, ad source/angle and page URL. Submit one test
  lead to map fields in GHL's builder.
- **Phone** — +44 7446 462551 (same GHL tracking number as the Smile
  Makeover campaign; calls won't attribute per-campaign unless a second
  number is added).
- **Conversion tag** — paste into the marked block on `thank-you.html`
  only. `index.html` fires nothing on submit by design.
- **Before/afters** — currently carries the six Smile Makeover cases
  (consented, captions confirmed); swap for campaign-specific cases
  when supplied.

> Compliance: offer figures (£50 / £72 / £100 off / £120 savings) come
> from the client's ad copy; the practice holds the evidence. Whitening
> is described as dentist-led following examination (UK requirement).
