<p align="center"><img src="screenshots/logo.png" width="90" alt="Dastiphone logo"/></p>
<h1 align="center">Dastiphone</h1>
<p align="center"><b>A marketplace to buy and sell new and used phones in Pakistan, with a web app and an Android app</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React"/>
  <img src="https://img.shields.io/badge/React_Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React Native"/>
  <img src="https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white" alt="Expo"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express"/>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB"/>
  <img src="https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white" alt="Socket.io"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind"/>
</p>

> 🔒 **Source code is private.** This repository is a public showcase of the product.
> Code walkthroughs are available for interviews: **umarnasrullah870@gmail.com**

---

## 💡 What it is

Dastiphone ("hand-to-hand phone") is an OLX-style marketplace built only for phones. Buyers can filter by
**PTA status, battery health, storage, RAM, condition and city**, and chat with sellers in real time.
Sellers post an ad in two minutes. The web app and the Android app share one API, one database and one account system.

## ✨ Features

- **Smart search & filters:** brand, model, price range, PTA approved / non-PTA, battery health, storage, condition and seller type
- **Phone ad pages:** photo gallery, full specifications, seller card, "buy safely" tips and similar phones
- **Post an ad:** guided form with auto-filled specs for the selected model, condition grading, photos and location
- **Real-time chat:** buyer-seller messaging with quick replies (Socket.io)
- **Accounts:** sign up with SMS code, Google or email; saved phones and saved searches with price-drop alerts
- **Seller profiles:** verified badges, active and sold ads, reply time
- **Admin panel:** review and approve ads, ban users (logs them out and hides all their ads)
- **Bilingual:** shared English / Urdu text, colours and fonts between web and app
- **Production-ready:** Cloudinary image uploads, password-reset email (Resend), Nginx + PM2 deployment scripts and database backups

## 🏗️ Architecture

```text
 Website (React + Vite + Tailwind) ─┐
                                    ├──► Node + Express + TypeScript API ──► MongoDB Atlas
 Android app (React Native + Expo) ─┘          │  Socket.io (chat)
                                               ├──► Cloudinary (photos)
                                               └──► Resend (emails)
 Hosting: VPS with Nginx reverse proxy + PM2, automated backups
```

## 🌐 Website

![Home page](screenshots/web/01-home.jpg)

| Search & filters | Phone details |
|---|---|
| ![Search](screenshots/web/02-search-filters.jpg) | ![Details](screenshots/web/03-phone-details.jpg) |
| **Post an ad** | **Messages** |
| ![Post ad](screenshots/web/04-post-an-ad.jpg) | ![Messages](screenshots/web/05-messages.jpg) |
| **Seller profile** | |
| ![Seller](screenshots/web/06-seller-profile.jpg) | |

## 📱 Android app (React Native + Expo)

<table>
  <tr>
    <th>Home</th><th>Search</th><th>Phone details</th><th>Sell your phone</th>
  </tr>
  <tr valign="top">
    <td><img src="screenshots/app/01-home.jpg" width="190" alt="Home"/></td>
    <td><img src="screenshots/app/02-search-results.jpg" width="190" alt="Search results"/></td>
    <td><img src="screenshots/app/03-phone-details.jpg" width="190" alt="Phone details"/></td>
    <td><img src="screenshots/app/05-sell-your-phone.jpg" width="190" alt="Sell your phone"/></td>
  </tr>
  <tr>
    <th>Login</th><th>Create account</th><th>Chat</th><th>Saved phones</th>
  </tr>
  <tr valign="top">
    <td><img src="screenshots/app/04-login.jpg" width="190" alt="Login"/></td>
    <td><img src="screenshots/app/10-create-account.jpg" width="190" alt="Create account"/></td>
    <td><img src="screenshots/app/07-chat.jpg" width="190" alt="Chat"/></td>
    <td><img src="screenshots/app/11-saved-phones.jpg" width="190" alt="Saved phones"/></td>
  </tr>
  <tr>
    <th>My account</th><th>Seller profile</th><th>Settings</th><th></th>
  </tr>
  <tr valign="top">
    <td><img src="screenshots/app/06-my-account.jpg" width="190" alt="My account"/></td>
    <td><img src="screenshots/app/08-seller-profile.jpg" width="190" alt="Seller profile"/></td>
    <td><img src="screenshots/app/09-settings.jpg" width="190" alt="Settings"/></td>
    <td></td>
  </tr>
</table>

App stack: Expo Router, TanStack Query, Secure Store, push notifications, image picker, location and Socket.io client.

*Screens show design / demo data.*

## 👤 Author

**M. Umar Nasrullah**, product design and full-stack development (web, mobile, API, deployment)

[GitHub](https://github.com/umarnasrullah) · [LinkedIn](https://www.linkedin.com/in/muhammad-umar-nasrullah-657418264) · umarnasrullah870@gmail.com

---

© 2026 M. Umar Nasrullah. All rights reserved. See [LICENSE](LICENSE).
