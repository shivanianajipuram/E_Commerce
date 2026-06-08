 ## MERN E-Commerce Platform

A full-featured MERN stack e-commerce application with authentication, cart system, admin dashboard, Cloudinary image uploads, and Razorpay (with dummy fallback mode).

---

# FEATURES

## User Features
- Register / Login (JWT Auth)
- Browse products
- Add to cart
- Checkout with address
- Dummy / Razorpay payment flow
- Order history tracking

## Admin Features
- Add / Edit / Delete products
- Upload product images (Cloudinary)
- View all orders
- Manage users

## System Features
- MongoDB (LOCAL NON-SRV)
- Cloudinary image storage
- Razorpay payment integration
- Dummy payment bypass mode
- JWT authentication

---

# PROJECT STRUCTURE

```bash
shopping/
│
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   ├── server.js
│   └── .env
│
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── redux/
│   │   └── context/
│
├── package.json
└── README.md
```

---

# SETUP INSTRUCTIONS

## 1. Clone Repository

```bash
git clone <repo-url>
cd shopping
```

---

## 2. Install Dependencies

```bash
npm install
```

OR manual setup:

```bash
cd backend
npm install

cd ../frontend
npm install
```

---

## 3. Start MongoDB (LOCAL NON-SRV)

```bash
mongod
```

OR use MongoDB Compass GUI

---

## 4. Backend ENV Setup

Create file:

```bash
backend/.env
```

Add:

```env
PORT=5000
NODE_ENV=development

MONGO_URI=Atlas_Uri

JWT_SECRET=super_secret_key

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

RAZORPAY_KEY_ID=your_key_id
RAZORPAY_KEY_SECRET=your_key_secret
```

---

# CLOUDINARY SETUP

```bash
1. Go to https://cloudinary.com
2. Create account
3. Copy credentials
4. Paste into .env
```

---

# RAZORPAY SETUP (OPTIONAL)

```bash
1. Go to https://razorpay.com
2. Create account
3. Get API keys
4. Add to .env
```

---

# DUMMY PAYMENT MODE

If Razorpay keys are not configured:

```text
System automatically switches to Dummy Mode
No real payment required
Used for testing and demo projects
```

Flow:
- Click Pay Now
- Select Student Bypass Mode
- Order is directly saved in MongoDB

---

# RUN PROJECT

```bash
npm run dev
```

---

# APPLICATION URLS

```bash
Frontend -> http://localhost:3000 / 3001
Backend  -> http://localhost:5000
```

---
## NOTE
If the local host port doesnt work go to windows and terminate the host .
```bash
npx kill PORT_NUMBER
```
# USER FLOW

## Login / Register

```bash
Open website -> Login -> Enter credentials
```

## Browse Products

```bash
Home page -> View products -> Open product details
```

## Add to Cart

```bash
Click Add to Cart
Go to Cart page
```

## Checkout

```bash
Fill shipping details:
- Full Name
- Street
- City
- Postal Code
- Country
```

## Payment

### Razorpay Mode

```bash
Payment popup opens -> Pay using test card
```

### Dummy Mode

```bash
Click Pay Now -> Choose Student Bypass Mode
Order saved instantly
```

## Order Success

```bash
Redirected to success page
Cart cleared
Order stored in database
```

## View Orders

```bash
Go to My Orders
View purchase history
```

---

# ADMIN FLOW

## Admin Login

```bash
Email: admin@shopping.com
Password: password123
```

## Admin Features

```bash
- Add Products
- Edit Products
- Delete Products
- Upload Images (Cloudinary)
- View Orders
```

## Add Product Flow

```bash
Admin Panel -> Add Product
Fill details -> Upload Image -> Submit
```

---

# DEPLOYMENT

## Backend (Render)

```bash
npm install
npm start
```

## Frontend (Vercel)

```bash
npm run build
```

Output:

```bash
build/
```

---

## MongoDB Production

Atlas:

```bash
MONGO_URI
```

---

# COMMON ISSUES

```bash
MongoDB not running -> run mongod
Images not uploading -> check Cloudinary keys
Payment not working -> use Dummy Mode
```
---

## LIVE DEMO:
```bash
https://e-commerce-8lds.onrender.com
```