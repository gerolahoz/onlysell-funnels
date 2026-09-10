# pp-it delivery site

Static hosting of Pallet Pro IT deliverables at **pp-it.onlysell.lat**.

## Structure

```
site/
├── pallet-pro/f7k5tvg20u/       → Core (160 progetti, AI PDF 32 MB)
├── attrezzi/tyorksuhxa/         → Bonus 1
├── scelta-pallet/wf2h8x07ce/    → Bonus 2
├── passo-passo/dk0nwj69kq/      → Bonus 3
├── modelli-esterni/bdbfpdw2xs/  → Bonus 4
├── finitura/8iut6egpl7/         → Bonus 5
├── calcolatore/reu9le77gk/      → Bonus 6 (JS calcolatore)
├── pallet-in-euro/izkmh878gk/   → OTO 1
├── maestro-ai/oezku1kdgi/       → OTO 2 (JS chat + Gemini)
├── officina-instagrammabile/2a1a15vetq/ → OTO 3
└── pallet-zero-euro/r7pqg9q19u/ → OTO 4
```

Each product has its own randomized URL — not linked to any other, not discoverable, not indexed.

## Deploy

nginx:alpine + static files. Build:

```bash
docker build -t pp-it-delivery .
docker run --rm -p 8080:80 pp-it-delivery
```

Coolify: point to this repo, Dockerfile build pack, domain `pp-it.onlysell.lat`, port 80.

## URLs mapping

See `urls-random.json` for the mapping product → URL.
The URLs are randomized 10-char alphanum lowercase, ~3.6×10¹⁵ combinations.

The user distributes each URL manually based on the product a customer bought.
