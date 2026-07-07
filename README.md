# Twende 🚢

**African freight, booked in minutes.** *Twende* — Swahili for "let's go."

A proof-of-concept freight quote marketplace for African logistics, inspired by platforms like Freightos. Single self-contained HTML page, no build step, no backend — all quotes, bookings and tracking events are simulated client-side.

## Demo flow

1. **Quote** — pick origin (global gateways or African ports), destination (including inland hubs like Nairobi, Kampala, Kigali, Lusaka), cargo weight and load type (LCL / FCL 20ft / FCL 40ft).
2. **Compare** — six carriers priced per lane with transit times, flagged *Cheapest* and *Fastest*. Prices derive from real haversine distances with deterministic per-lane jitter.
3. **Book** — confirm and receive a `TWD-XXXX` reference.
4. **Track** — door-to-door timeline including customs and named inland corridor legs (SGR rail, Northern Corridor, North–South road corridor). Try the pre-seeded reference `TWD-4102`.

## Run it

Open `index.html` in a browser — that's it. Or visit the GitHub Pages deployment.

## Next steps beyond the PoC

- Real backend (Node.js + Express, PostgreSQL, Redis) per the target architecture
- Carrier API integrations replacing the mock rate engine
- Auth (JWT), payments, notifications, live tracking feeds
