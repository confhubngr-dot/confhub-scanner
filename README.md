# ConfHub Scanner

Delegate check-in scanner. Used by stewards at the door.

**Live at:** https://scan.confhub.ng

## Files
- `scan.html` — the scanner
- `index.html` — identical copy, so the bare domain works

## Nothing in here needs editing
Event details are entered on screen when a steward opens it:
- **API URL** — the /exec address for that event's Apps Script
- **Desk passcode** — from that event's ConfHub Settings tab
- **Desk name** — e.g. Door 1

One scanner serves every conference. Different event = different API URL and passcode.

## Notes
- Needs HTTPS for the camera (Cloudflare Pages provides this)
- Validates offline; check-ins queue in the browser and sync every 30s
- QR libraries are inlined, so it works with no network
