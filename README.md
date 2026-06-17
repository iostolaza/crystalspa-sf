# Crystal Wellness San Francisco

A modern, clean, and professional single-page wellness website for Crystal Wellness in San Francisco.

**Live Demo:** *(Add your deployed link here after going live)*

---

## Deployment & Third-Party Services Setup (Completed - June 2026)

This project is now fully deployed and connected.

### Services Used
| Service          | Purpose                              | Status          | Notes |
|------------------|--------------------------------------|-----------------|-------|
| **GitHub**       | Version Control & Deployment         | Connected       | Main repo for the site |
| **Netlify**      | Website Hosting + SSL                | Live            | Auto-deploys from GitHub `main` branch |
| **Squarespace**  | Domain (`crystalspa-sf.com`)         | Configured      | DNS records updated (CNAME + Forwarding) |
| **TidyCal**      | Booking System & Notifications       | Connected       | `https://tidycal.com/awsom138` |

### Completed Setup Steps
1. **GitHub** — Code pushed and connected to Netlify.
2. **Netlify** — Site deployed at `crystalspa-sf.netlify.app`.
3. **Squarespace DNS** — Added CNAME for `www` pointing to Netlify + domain forwarding from root to `www`.
4. **TidyCal** — Booking system live and linked in the site.

> **Note on DNS**: DNS configuration was completed in Squarespace to point the domain to Netlify. No sensitive records were exposed.

### Recommended Ongoing Ownership
- **Domain (Squarespace)**: Keep under client ownership.
- **TidyCal**: Client owns the account (developer added as admin if needed).
- **Netlify + GitHub**: Developer manages for now; can transfer later.

### JavaScript Note
All JavaScript is currently kept inside `index.html`. For a simple static site like this, it is acceptable. For larger projects, it is better to move JavaScript into separate `.js` files.

---

## What's New (June 2026 Update)

This version has been significantly updated based on client feedback:

- Removed sections: Journal, Guest Stories/Testimonials, and "Why Guests Return"
- Removed heavy compliance language
- Removed references to "oil" and "stones"
- Replaced long consultation form with a clean **Book Appointment** popup modal
- Added 4 new trust items with a San Francisco / Bay Area focus
- Improved visual separation between sections using alternating backgrounds
- All 6 services are now available in the booking modal
- Better spacing and professional layout throughout

---

## Booking System (TidyCal)

This site uses **TidyCal** for appointment booking.

### Why TidyCal?
- One-time cost: **$29** (lifetime deal)
- Unlimited bookings
- Email notifications to both client and business owner
- Simple and reliable
- Easy to manage availability via Google Calendar

### How to Connect TidyCal

1. Go to [tidycal.com](https://tidycal.com) and create an account.
2. Connect your **Google Calendar**.
3. Create your services (e.g., Aromatherapy Immersion, Deep Warmth Ritual, etc.) with duration and pricing.
4. Set your availability.
5. Copy your **booking link** or **embed code** from TidyCal.
6. Replace the current booking modal with your TidyCal link/embed (instructions below).

### Replacing the Booking Modal with Real TidyCal

**Option 1 (Recommended - Simple):**
- Replace the `onclick="showBookingModal()"` on the "Book Appointment Now" button with your TidyCal booking link.
- Example:
  ```html
  <a href="https://tidycal.com/yourusername" target="_blank" class="...">
      Book Appointment Now
  </a>
  ```

**Option 2 (Popup style):**
- Keep the modal structure but replace the content inside with TidyCal’s embed code.

---

## Files Included

- `index.html` – Main website (fully updated)
- `robots.txt` & `sitemap.xml` – SEO files
- `DEPLOYMENT.md` – Deployment instructions
- `README.md` – This file (updated with full deployment steps)

---

## Key Sections (Current)

- Hero with local San Francisco messaging
- Our Story
- Wellness Experiences (6 services with modals)
- Areas We Serve (Bay Area focus)
- Common Questions (FAQ)
- Get In Touch + Hours of Operation
- Book Appointment (popup modal)
- Final Call to Action
- Footer

---

## Quick Start

1. Open `index.html` in any browser to preview.
2. Sign up for TidyCal and connect your calendar.
3. Replace the booking button/modal with your TidyCal link.
4. Update phone number, address, and service prices as needed.
5. Deploy using Netlify, Vercel, or GitHub Pages (see `DEPLOYMENT.md`).

---

## Customization Tips

- **Colors**: Edit Tailwind classes or the custom CSS at the top of `index.html`.
- **Services & Prices**: Update both the service cards and the booking modal dropdown.
- **Images**: Replace any remaining placeholder images with your own professional photos.
- **Booking**: Connect TidyCal as described above.

---

## Cost Summary

| Item                    | Cost          | Notes                              |
|-------------------------|---------------|------------------------------------|
| TidyCal (Booking)       | **$29 one-time** | Lifetime deal                     |
| Domain + Hosting        | ~$15–20/year  | Recommended: Netlify + custom domain |
| Total First Year        | **Under $50** | Very low ongoing cost             |

---

**Created for Crystal Wellness • San Francisco, CA**  
Recommended domain: `crystalwellness-sf.com`

*Last updated: June 2026*