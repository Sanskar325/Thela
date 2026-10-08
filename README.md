# Ghoom XI

Website for **Ghoom XI**, our fast food cart in Purnia, Bihar. Momos, rolls, chowmein, burgers and kulhad chai, cooked to order every evening.

Live site: https://sanskar325.github.io/Thela/

## What's on the site

- An animated line drawing of the cart rolling down the street, with the chef at the tawa and a cat walking alongside
- The full menu in English and Hindi, with veg and non-veg marks, half and full plates, search and filters
- Order ahead: pick your dishes, choose pickup or home delivery, and send the order to us on WhatsApp
- Ghoom quests: ₹20 off a first order, a stamp card where the 6th order gets free momos, and a free kulhad chai for trying all four favourites, all kept against the customer's WhatsApp number
- Pay by UPI or cash
- Opening hours and directions to the cart on Google Maps
- A contact and review form that sends your message to us on WhatsApp
- Works on phones and laptops

## How it's built

The whole site is one file, `index.html`, written in plain HTML, CSS and JavaScript. There are no frameworks and no build step. Fonts load from Google Fonts.

## Run it on your computer

Open `index.html` in any browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then go to http://localhost:8000.

## Updating the details

Everything you would normally change is at the top of the `<script>` block near the end of `index.html`.

| Section | What it holds |
| --- | --- |
| `CONFIG` | WhatsApp number, phone number, UPI ID, the cart's location, opening hours, delivery charges, FSSAI number, Zomato and Swiggy links |
| `TEAM` | The people behind the cart: names, roles, a line about each, and photos |
| `MENU` | Dishes, Hindi names, notes and prices |
| `CONFIG.quests` | Coupon codes and rewards for the welcome discount, the stamp card and the menu explorer |

A few examples:

```js
whatsapp: '91XXXXXXXXXX',                 // country code + number, digits only
location: { lat: 25.7771, lng: 87.4753 }, // the exact spot where the cart stands
hours: { open: '16:00', close: '22:30', closedDays: [] },
```

Buttons for things that are not filled in yet (phone, UPI, Zomato, Swiggy, Google reviews) stay hidden until you add them.

There are no customer accounts: each customer's WhatsApp number is their Ghoom card. We keep stamps, dishes tried and rewards in our own ledger, and every WhatsApp order includes any coupon used, so check the ledger before you confirm a reward.

To add a photo to the team section, put the image in a `makers/` folder and set its path, for example `photo: 'makers/sanskar.jpg'`.

## Hosting

The site is served by GitHub Pages from the `main` branch. Any change pushed to `main` goes live within a minute or two.

## Find us

Ghoom XI, Line Bazar Chowk, Purnia, Bihar 854301
