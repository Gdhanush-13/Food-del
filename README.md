# 🍅 Tomato Food Delivery App (MERN + Stripe)

Tomato is a full-stack food delivery platform built using the MERN stack (MongoDB, Express, React, Node.js) with Stripe integration for payments. It features a responsive frontend for users, an admin dashboard for management, and a secure backend API.

---

## 📁 Project Structure

tomato-app/
│
├── backend/ # Node.js + Express API
├── frontend/ # User-facing React app
└── admin/ # Admin dashboard (React)

yaml
Copy
Edit

---

## 🧩 Tech Stack

| Layer       | Tech Used                    |
|------------|-------------------------------|
| Frontend    | React.js (Vite), Axios       |
| Backend     | Node.js, Express.js          |
| Database    | MongoDB Atlas (Mongoose)     |
| Auth        | JWT Tokens                   |
| Payment     | Stripe API                   |
| Admin Panel | React.js                     |

---

## 🚀 Features

### 👨‍🍳 User (Frontend)
- Explore menu categories
- Add/remove dishes from cart
- Authentication (login/signup)
- Place order via Stripe
- Responsive UI

### ⚙️ Backend (API)
- RESTful API endpoints
- MongoDB database connection
- JWT authentication & token handling
- CRUD operations on food, cart, and orders
- Stripe checkout session API

### 🛠️ Admin Panel
- Admin login
- View/Add/Delete food items
- View orders and users
- Controlled access to dashboard

---

## 📦 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/tomato-app.git
cd tomato-app
2. Frontend Setup (/frontend)
bash
Copy
Edit
cd frontend
npm install
npm run dev
Create a .env file in frontend/:

env
Copy
Edit
VITE_APP_BASE_URL=http://localhost:4000
3. Backend Setup (/backend)
bash
Copy
Edit
cd backend
npm install
npm run dev
Create a .env file in backend/:

env
Copy
Edit
PORT=4000
MONGODB_URL=mongodb+srv://<username>:<password>@cluster0.mongodb.net/food-del
JWT_SECRET=your_jwt_secret_key
STRIPE_SECRET_KEY=your_stripe_secret_key
4. Admin Panel Setup (/admin)
bash
Copy
Edit
cd admin
npm install
npm run dev
Create a .env file in admin/:

env
Copy
Edit
VITE_ADMIN_API_BASE_URL=http://localhost:4000
🔐 Authentication
JWT tokens are used for secure user authentication.

Tokens are stored in localStorage and sent via headers for protected routes.

💳 Stripe Integration
Payment handled via Stripe Checkout.

Requires a Stripe account and API keys.

📦 API Overview
👤 User APIs
Endpoint	Method	Description
/api/user/register	POST	Register new user
/api/user/login	POST	Login user

🍱 Food APIs
Endpoint	Method	Description
/api/food/list	GET	List all food items
/api/food/add	POST	Add food item

🛒 Cart APIs
Endpoint	Method	Description
/api/cart/add	POST	Add item to cart
/api/cart/remove	POST	Remove item
/api/cart/get	POST	Get cart contents

💳 Payment API
Endpoint	Method	Description
/api/payment/create-checkout-session	POST	Stripe payment session

👨‍💻 Author
Dhanush — Website Implementation Specialist | Full Stack Developer
Feel free to contribute or fork this project.

📄 License
MIT License — use it for personal or commercial projects.

✅ Tips
MongoDB Atlas should have IP whitelisting configured.

Use strong secrets and production-ready Stripe keys in deployment.

For deployment, consider Vercel (frontend), Render (backend), or any cloud provider.
