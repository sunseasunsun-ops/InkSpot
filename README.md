# InkSpot
Guest spot platform connecting traveling tattoo artists with studios across Europe. Built with Claude Code in 2 evenings.
# 🖤 InkSpot — Guest Spot Platform for Tattoo Artists & Studios

<p align="center">
  <img src="https://img.shields.io/badge/Built%20with-Claude%20Code-7c3aed?style=for-the-badge" alt="Built with Claude Code"/>
  <img src="https://img.shields.io/badge/Status-MVP-22c55e?style=for-the-badge" alt="Status: MVP"/>
  <img src="https://img.shields.io/badge/Stack-Vanilla%20JS%20%2B%20Leaflet-eab308?style=for-the-badge" alt="Stack"/>
</p>

---

## 🎯 The Problem

The tattoo industry has a unique tradition: **guest spots** — when a traveling tattoo artist temporarily works at a studio in another city or country. This is how artists grow their clientele, explore new markets, and collaborate internationally.

**But finding a guest spot today is painful:**

- **For artists:** There's no centralized place to discover studios offering guest spots. Artists rely on Instagram DMs, word of mouth, and Facebook groups. They spend hours scrolling, messaging studios that never reply, and have zero visibility into pricing, availability, or what equipment is provided. Going to a new country adds another layer of complexity — every EU country has different licensing and hygiene regulations, and there's no easy way to find out what's required before you book a flight.

- **For studios:** Studios that want to host guest artists have no efficient way to publish availability. They get flooded with low-quality DMs, can't easily review portfolios, and waste time on back-and-forth communication. There's no structured way to manage incoming requests.

- **The licensing nightmare:** A tattoo artist traveling from Berlin to Amsterdam might not know that the Netherlands requires a GGD license costing €250–400 with a mandatory health inspection. France requires a 21-hour hygiene training certificate. Some countries have no requirements at all. This information is scattered across government websites in local languages, and getting it wrong can mean fines or being turned away at the studio door.

**The result:** Talented artists miss opportunities, studios miss revenue, and the whole guest spot ecosystem runs on chaos and luck.

---

## 💡 The Solution — InkSpot

**InkSpot** is a dedicated platform that connects traveling tattoo artists with studios offering guest spots across Europe. Think of it as "Airbnb for tattoo workstations."

### How it works:

**🎨 For Tattoo Artists:**
1. Create a profile with your portfolio, styles, experience, and Instagram
2. Browse studios on an interactive map — filter by style, city, price
3. See exactly what each studio offers: price per day, what's included, what to bring
4. Check the **licensing requirements** for each country before you travel
5. Send a structured guest spot request with your dates and portfolio auto-attached
6. Chat with studios directly, track your request status, and rate studios after your visit

**🏠 For Tattoo Studios:**
1. Register as a studio with your details, photos, pricing, and available spots
2. Receive structured guest spot requests — no more messy DMs
3. Review artist portfolios, experience, and specialties at a glance
4. Accept or decline requests with one tap
5. Manage all incoming requests in a clean dashboard

**⚖️ The Licensing Layer (Unique Feature):**
- Every country in the app shows a clear licensing info card
- Color-coded severity: 🟢 Low (no specific license) / 🟡 Medium (trade license needed) / 🔴 High (strict requirements)
- Specific details: what documents you need, estimated costs, which authority to register with
- Artists can make informed decisions before booking travel

---

## 🌍 Current State — MVP Demo

> ⚠️ **This is an MVP / proof of concept.** The app currently demonstrates the full user flow with sample data.

### What's live now:

| Feature | Status |
|---|---|
| Artist registration & profile | ✅ Working |
| Studio registration & profile | ✅ Working |
| Full profile editing (both roles) | ✅ Working |
| Interactive map (Leaflet + CartoDB) | ✅ Working |
| Studio search & style filters | ✅ Working |
| Guest spot request flow | ✅ Working |
| In-app messaging | ✅ Working |
| Request management (artist side) | ✅ Working |
| Incoming requests dashboard (studio side) | ✅ Working |
| Licensing info for 15 EU countries | ✅ Working |
| Country switching | ✅ Working |
| Studio ratings | ✅ Working |

### Demo data — Germany 🇩🇪

The current demo is pre-loaded with **20 real Berlin tattoo studios** across districts like Kreuzberg, Mitte, Friedrichshain, Charlottenburg, Prenzlauer Berg, and Neukölln. Each studio has:
- Real pricing (€30–60/day range)
- Accurate style specializations
- What's included vs. what to bring
- Map coordinates for real locations

**Why Germany as the starting point:**
- Berlin is the tattoo capital of Europe — highest density of studios and guest artists
- Germany has relatively low licensing barriers (Gewerbe registration + hygiene compliance)
- Large international artist community already doing guest spots
- Natural expansion from here to rest of EU

### What's needed for production:

- **Backend + Database** — Currently all data is in-memory. Need persistent storage for real user accounts, studios, and requests
- **Real studio onboarding** — Studios need to register themselves and verify their listings. The 20 Berlin studios are sample data to demonstrate the concept
- **Image upload** — Currently using placeholder portfolio images. Need real file upload for portfolios and studio photos
- **Authentication** — Real auth system (email/password, Google, Apple sign-in)
- **Payment integration** — For premium listings or booking deposits
- **Push notifications** — For new requests, messages, status updates
- **Expansion to other cities** — The country/licensing framework is ready for 15 EU countries, but studio listings need to be populated per city

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla JavaScript (zero dependencies) |
| Styling | Custom CSS (dark theme, mobile-first) |
| Maps | Leaflet.js + CartoDB dark tiles |
| Architecture | Single-page app, screen-based navigation |
| Hosting | Static HTML — can be deployed anywhere |

**Why vanilla JS?** This is an MVP built for speed. No build tools, no npm, no framework overhead. One HTML file, opens in any browser, deploys in seconds. The architecture is clean enough to migrate to React/Vue when the time comes.

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/your-username/inkspot.git

# That's it. Open the file:
open index.html

# Or serve it:
npx serve .
```

No build step. No dependencies. No environment variables. Just open `index.html` in a browser.

---

## 📱 Demo Flow

### As a Tattoo Artist:
1. **Welcome** → Create Account → Select "Tattoo Artist"
2. **Explore** → Browse Berlin studios on the map, filter by style
3. **Detail** → Tap a studio, see pricing, photos, what to bring
4. **Request** → Send a guest spot request with dates
5. **Requests** → Track status (Pending / Accepted / Declined)
6. **Chat** → Message studios directly
7. **Profile** → Edit your info, portfolio, styles, availability

### As a Studio Owner:
1. **Welcome** → Create Account → Select "Studio Owner"
2. **Dashboard** → See incoming guest spot requests
3. **Review** → View artist portfolio, experience, message
4. **Accept/Decline** → Manage requests
5. **Studio Profile** → Edit studio info, photos, pricing, hours

---

## 📊 Market Opportunity

- **~200,000** professional tattoo artists in Europe
- **~50,000** tattoo studios across the EU
- Guest spots are a **$500M+** annual market (studio fees, travel, supplies)
- **Zero** dedicated platforms exist for this workflow
- Current alternatives: Instagram DMs, Facebook groups, word of mouth
- The industry is growing **8–10% annually** with increasing international mobility

---

## 🗺 Roadmap

**Phase 1 — MVP (Current)**
- [x] Core user flows for artists and studios
- [x] Interactive map with studio listings
- [x] Licensing info framework for 15 EU countries
- [x] In-app messaging
- [x] Profile editing with portfolio management

**Phase 2 — Beta**
- [ ] Backend (Node.js + PostgreSQL)
- [ ] Real authentication & user accounts
- [ ] Studio self-registration & verification
- [ ] Image upload for portfolios
- [ ] Push notifications
- [ ] Expand to 5 major cities (Berlin, Amsterdam, Barcelona, London, Prague)

**Phase 3 — Launch**
- [ ] Payment integration (Stripe)
- [ ] Calendar/availability system
- [ ] Review & rating system (expanded)
- [ ] Studio verification badges
- [ ] Artist verification (portfolio review)
- [ ] Mobile apps (React Native)

---

## 👤 Author

**Vlad Shevchenko**

Built in 2 evenings with Claude Code, February 2025.

---

## 📄 License

MIT License — free to use, modify, and distribute.
