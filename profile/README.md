<div align="center" id="top">
  <a href="https://www.synvya.com">
    <picture>
      <img src="Banner GitHub Jan 2026.png" alt="Synvya">
    </picture>
  </a>
</div>
<div align="center">
  <br>
  <a href="https://synvya.com/">New customers. Turned into regulars.</a>
  </br>
</div>

---

# We bring new customers and turn them into regulars.

Synvya helps restaurants get found when guests ask AI assistants (ChatGPT, Claude, Perplexity) where to eat — and turns those recommendations into **direct bookings**. Guests can make reservations straight with your restaurant through their assistant of choice, with **no marketplace in the middle** and **no commission layer**. You keep ownership of the guest relationship and the data you generate (intent, preferences, and repeat visits), rather than handing it to a closed directory app.  

Learn more and sign up at [synvya.com](https://synvya.com).

## What restaurants get
- **AI Discovery:** AI-optimized restaurant + menu data so assistants can recommend you accurately.
- **Real-time updates:** Keep one source of truth for your menu, hours, and details.
- **Direct conversion:** Reservations (and takeout coming next) routed to you, not a middleman.

## How it works (high level)
1. A restaurant publishes a verified profile + structured menu data.
2. AI assistants discover the restaurant via open protocols.
3. Reservations are negotiated via a lightweight, privacy-preserving message flow (encrypted).
4. (Next) Orders and fulfillment flow end-to-end.

## Start here (restaurants)
- Create an account: https://account.synvya.com
- Publish your restaurant profile + menu
- Enable reservation messaging (if applicable)

## Security & privacy
- Restaurant keys are generated locally and used to sign/publish data.
- Reservation messages use encrypted using restaurant keys.
- Your data stays under your control; the goal is direct guest relationships.

## Roadmap
- [ ] Harden reservation protocol + broader interoperability
- [ ] Takeout / ordering as an additional conversion channel

---

Follow us on [Nostr](https://www.primal.net/synvya#notes) or check [synvya.com](https://www.synvya.com) for more details.

---
## For Developers

## Repos
- **client** — Merchant onboarding + profile management + menu publishing (Square catalog → structured menu events).  
  Includes reservation messaging + encryption details and menu event generation (kinds 30402/30405).  
- **mcp-server** — MCP server for AI assistants that want to discover restaurants.
- **reservation-protocol** — Draft Nostr Implementation Possibilities (NIP) for restaurant reservations (protocol + schemas).

## Protocol quick reference
- **Restaurant profile:** kind `0`
- **Menu items:** kind `30402`
- **Menu collections/sections:** kind `30405`
- **Reservations (4-message flow):**
  - `9901` request → `9902` response (confirm/decline/cancel)
  - `9903` modify request → `9904` modify response
  - Messages exchanged via encrypted gift-wrapped patterns

## References
- [NIP-01](https://github.com/nostr-protocol/nips/blob/master/01.md)
- [NIP-59](https://github.com/nostr-protocol/nips/blob/master/59.md) Gift Wrap
- Gamma Markets [marketplace specification](https://github.com/GammaMarkets/market-spec/blob/main/spec.md)
