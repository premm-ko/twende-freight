# Twende 🚢

**African freight, booked in minutes.** *Twende* — Swahili for "let's go."

A proof-of-concept freight quote marketplace for African logistics, inspired by platforms like Freightos. Single self-contained HTML page, no build step, no backend — all quotes, bookings and tracking events are simulated client-side.

## Demo flow

1. **Quote** — pick origin (global gateways or African ports), destination (including inland hubs like Nairobi, Kampala, Kigali, Lusaka), cargo weight and load type (LCL / FCL 20ft / FCL 40ft).
2. **Compare** — six carriers priced per lane with transit times, flagged *Cheapest* and *Fastest*. Prices derive from real haversine distances with deterministic per-lane jitter.
3. **Book** — confirm and receive a `TWD-XXXX` reference.
4. **Track** — door-to-door timeline plus a live map showing the shipment's current position, with a transit simulator slider. Includes customs and named inland corridor legs (SGR rail, Northern Corridor, North–South road corridor). Try the pre-seeded reference `TWD-4102`.
5. **Admin console** — toggle carriers on/off and edit their rate/speed multipliers; the next quote search reflects the changes instantly. Review all bookings and jump to tracking. Carrier edits and bookings persist in `localStorage`.
6. **Autoplay demo** — the "Watch the demo" button runs the whole flow hands-free.

## Run it

Open `index.html` in a browser — that's it. Or visit the GitHub Pages deployment.

## Next steps beyond the PoC

- Real backend (Node.js + Express, PostgreSQL, Redis) per the target architecture
- Carrier API integrations replacing the mock rate engine
- Auth (JWT), payments, notifications, live tracking feeds
