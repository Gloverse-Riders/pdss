# Gloverse

Gloverse is a modern, full-stack e-commerce web application designed to provide users with a seamless food delivery experience. Customers can explore curated restaurant menus, securely manage their profiles, and place real-time food orders, while staff utilize a dedicated administrative dashboard to track workflows and catalog configurations.

## Live Demo & Links
* **Repository:** [GitHub Link](https://github.com/Gloverse-Riders/pdss)

---

## Features

### Customer Experience
* **Dynamic Menu Exploration:** Browse through structured restaurant menus with detailed item specifications, pricing, and ingredients.
* **Seamless Checkout:** Add items to a persistent shopping cart and seamlessly simulate incoming orders.
* **Personalized Profile Management:** Securely configure user profile details, save multi-address settings, and store payment preferences.

### Security & Core Infrastructure
* **Token-Based Authentication:** Outfitted with robust session infrastructure utilizing **JSON Web Tokens (JWT)** to manage registration, secure login flows, and route access guards.
* **Decoupled Asset Management:** Scalable storage architecture engineered to cleanly isolate lightweight metadata transactions from cloud-hosted image files.

### Administrative Dashboard
* **Menu Lifecycle Tools:** Full CRUD operations for administrators to seamlessly update, delete, or add new dishes to active catalogs.
* **Order Tracking Pipeline:** Real-time visibility into incoming purchases to monitor order fulfillment status.
* **User Accounts Oversight:** Centralized command module to oversee registered client profiles and evaluate platform health.

---

## Architecture & Tech Stack

Gloverse follows a decoupled client-server pattern designed for micro-storage optimization:

* **Frontend:** React, Next.js (App Router), Tailwind CSS
* **Backend:** Node.js, Express, REST APIs
* **User Session Management:** JSON Web Tokens (JWT)
* **Primary Database (Metadata):** MongoDB (NoSQL schema storing user records, logs, names, and emails)
* **Cloud Object Storage (Static Assets):** Amazon S3 (Hosting high-definition menu cards, dish imagery, and profile thumbnails)

---



## Installation & Setup

### Prerequisites
* Node.js
* MongoDB database instance
* AWS Account with an active Amazon S3 Bucket

### 1. Clone the Repository
```bash
git clone [https://github.com/Gloverse-Riders/pdss.git](https://github.com/Gloverse-Riders/pdss.git)
cd pdss
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_signing_key

# AWS S3 Configurations
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_REGION=your_bucket_region
AWS_S3_BUCKET_NAME=your_gloverse_bucket_name
# Install root, backend, and frontend dependencies
npm install
# Start both frontend and backend concurrently
npm run dev
