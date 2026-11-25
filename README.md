# Badel w Bi3 Shopper | بدّل وبيع

**An Arabic classifieds marketplace for Lebanon**

Badel w Bi3 helps people in Lebanon find a used sofa, browse cars, look for an apartment, or discover a job opening. Shoppers can search listings in Arabic, save favorites, and contact the advertiser directly on WhatsApp.

## How it works

- **For shoppers** — Search by keyword, browse categories, and open a listing to see its photos, price, and location.
- **For advertisers** — Submit a listing with photos, a description, a location, and a WhatsApp number so interested shoppers can get in touch.
- **For moderators** — Review submissions in the admin dashboard and approve or reject them before they appear in the public catalog.

## Inside the project

The right-to-left interface uses HTML, CSS, and vanilla JavaScript. A Node.js and Express API handles accounts and listings, with Mongoose models for MongoDB. Moderation updates trigger a rebuild of the public listings cache so shoppers can browse approved ads without a database query for every request.

## Run locally

1. Install Node.js 22.12 or later and make a MongoDB connection available.
2. From the project directory, install dependencies and copy the example configuration.

   ```sh
   npm ci
   cp env.example .env
   ```

   On Windows PowerShell, use `Copy-Item env.example .env` for the copy step.

3. Set `MONGODB_URI` and a private `JWT_SECRET` in `.env`. For admin access, also set `ADMIN_EMAIL` and `ADMIN_PASSWORD`.
4. Run `npm start` and open [localhost:3000](http://localhost:3000). A fresh database starts without the production listings.

## Project links

[Project website](https://badelwbi3.com/) · [Mohammad Olleik on GitHub](https://github.com/mhmdolleik-fullstack)
