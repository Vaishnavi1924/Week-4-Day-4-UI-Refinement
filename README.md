# Week-4-Day-4-UI-Refinement
The goal is to make your e-commerce SaaS look like a polished application rather than a basic project. We’ll use responsive CSS so the layout adapts to desktop, tablet, and mobile screens. Media queries are a standard way to change layouts based on viewport size


1. Replace index.css

Open:

frontend/src/index.css

You can replace the existing styling with this cleaner version:

/* =========================
   GLOBAL
========================= */

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.5;
  font-weight: 400;
}

body {
  background: #f5f7fb;
  color: #1f2937;
}

a {
  text-decoration: none;
  color: inherit;
}

button,
input,
select,
textarea {
  font: inherit;
}

button {
  cursor: pointer;
}

/* =========================
   NAVBAR
========================= */

.navbar {
  background: #111827;
  color: white;
  padding: 15px 30px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  gap: 20px;
}

.navbar h2 {
  font-size: 22px;
}

.navbar-links {
  display: flex;
  align-items: center;
  gap: 18px;
}

.navbar-links a {
  color: white;
  font-weight: 500;
}

.navbar-links a:hover {
  color: #93c5fd;
}

.navbar button {
  background: #dc2626;
  color: white;
  border: none;
  padding: 8px 14px;
  border-radius: 6px;
}

/* =========================
   PAGE CONTAINER
========================= */

.page-container {
  width: min(1200px, 92%);
  margin: 30px auto;
}

/* =========================
   BUTTONS
========================= */

button,
.primary-button {
  background: #2563eb;
  color: white;

  border: none;
  border-radius: 7px;

  padding: 10px 16px;

  transition: 0.2s;
}

button:hover,
.primary-button:hover {
  background: #1d4ed8;
}

.secondary-button {
  background: #6b7280;
}

.secondary-button:hover {
  background: #4b5563;
}

.danger-button {
  background: #dc2626;
}

.danger-button:hover {
  background: #b91c1c;
}

/* =========================
   FORMS
========================= */

.form-container {
  width: min(450px, 92%);
  margin: 50px auto;

  background: white;
  padding: 30px;

  border-radius: 12px;

  box-shadow:
    0 4px 20px rgba(0, 0, 0, 0.08);
}

.form-container h1 {
  margin-bottom: 25px;
  text-align: center;
}

.form-group {
  margin-bottom: 18px;
}

.form-group label {
  display: block;
  margin-bottom: 6px;
  font-weight: 600;
}

.form-group input,
.form-group textarea,
.form-group select {
  width: 100%;

  padding: 11px;

  border: 1px solid #d1d5db;
  border-radius: 7px;

  outline: none;
}

.form-group input:focus,
.form-group textarea:focus,
.form-group select:focus {
  border-color: #2563eb;
}

/* =========================
   DASHBOARD
========================= */

.dashboard-container,
.analytics-page {
  width: min(1200px, 92%);
  margin: 30px auto;
}

.dashboard-header {
  margin-bottom: 25px;
}

.dashboard-header h1 {
  margin-bottom: 5px;
}

/* =========================
   STAT CARDS
========================= */

.stats-grid,
.analytics-grid {
  display: grid;

  grid-template-columns:
    repeat(auto-fit, minmax(200px, 1fr));

  gap: 20px;

  margin: 25px 0;
}

.stat-card,
.analytics-card {
  background: white;

  padding: 22px;

  border-radius: 12px;

  border: 1px solid #e5e7eb;

  box-shadow:
    0 3px 12px rgba(0, 0, 0, 0.05);
}

.stat-card h3,
.analytics-card h3 {
  color: #6b7280;
  font-size: 15px;
  margin-bottom: 8px;
}

.stat-card p,
.analytics-card p {
  font-size: 28px;
  font-weight: 700;
}

/* =========================
   PRODUCTS
========================= */

.product-grid {
  display: grid;

  grid-template-columns:
    repeat(auto-fill, minmax(230px, 1fr));

  gap: 24px;

  margin-top: 25px;
}

.product-card {
  background: white;

  border-radius: 12px;

  overflow: hidden;

  border: 1px solid #e5e7eb;

  box-shadow:
    0 3px 12px rgba(0, 0, 0, 0.06);

  transition:
    transform 0.2s,
    box-shadow 0.2s;
}

.product-card:hover {
  transform: translateY(-4px);

  box-shadow:
    0 8px 20px rgba(0, 0, 0, 0.1);
}

.product-card img {
  width: 100%;
  height: 200px;

  object-fit: cover;

  background: #f3f4f6;
}

.product-card-content {
  padding: 18px;
}

.product-card h3 {
  margin-bottom: 8px;
}

.product-price {
  color: #2563eb;
  font-size: 20px;
  font-weight: 700;
  margin: 10px 0;
}

/* =========================
   CART
========================= */

.cart-page,
.orders-page,
.shop-page {
  width: min(1000px, 92%);
  margin: 30px auto;
}

.cart-item {
  background: white;

  padding: 20px;

  margin: 15px 0;

  border-radius: 10px;

  border: 1px solid #e5e7eb;

  display: flex;
  align-items: center;

  gap: 20px;

  flex-wrap: wrap;
}

.cart-item img {
  width: 90px;
  height: 90px;

  object-fit: cover;

  border-radius: 8px;
}

.cart-total {
  background: white;

  padding: 20px;

  border-radius: 10px;

  margin-top: 20px;

  text-align: right;
}

/* =========================
   ORDERS
========================= */

.orders-list {
  display: grid;

  gap: 20px;

  margin-top: 25px;
}

.order-card {
  background: white;

  padding: 22px;

  border-radius: 12px;

  border: 1px solid #e5e7eb;

  box-shadow:
    0 3px 12px rgba(0, 0, 0, 0.05);
}

.order-card h3 {
  margin-bottom: 12px;
}

.order-card p {
  margin: 6px 0;
}

.order-status {
  margin-top: 18px;

  display: flex;
  align-items: center;

  gap: 10px;
}

.order-status select {
  padding: 8px;

  border: 1px solid #d1d5db;

  border-radius: 6px;
}

/* =========================
   STATUS BADGES
========================= */

.status-badge {
  display: inline-block;

  padding: 5px 10px;

  border-radius: 20px;

  font-size: 13px;

  font-weight: 600;
}

.status-placed {
  background: #fef3c7;
  color: #92400e;
}

.status-processing {
  background: #dbeafe;
  color: #1e40af;
}

.status-shipped {
  background: #e0e7ff;
  color: #3730a3;
}

.status-delivered {
  background: #dcfce7;
  color: #166534;
}

.status-cancelled {
  background: #fee2e2;
  color: #991b1b;
}

/* =========================
   TABLE
========================= */

.data-table-container {
  width: 100%;
  overflow-x: auto;

  background: white;

  border-radius: 10px;
}

.data-table {
  width: 100%;

  border-collapse: collapse;

  min-width: 650px;
}

.data-table th,
.data-table td {
  padding: 13px;

  border-bottom: 1px solid #e5e7eb;

  text-align: left;
}

.data-table th {
  background: #f9fafb;
}

/* =========================
   EMPTY STATE
========================= */

.empty-state {
  background: white;

  padding: 50px 20px;

  text-align: center;

  border-radius: 12px;

  border: 1px solid #e5e7eb;
}

.empty-state h2 {
  margin-bottom: 10px;
}

/* =========================
   SUCCESS PAGE
========================= */

.order-success {
  width: min(600px, 92%);

  margin: 80px auto;

  padding: 40px;

  background: white;

  border-radius: 15px;

  text-align: center;

  box-shadow:
    0 5px 25px rgba(0, 0, 0, 0.08);
}

.order-success h1 {
  margin-bottom: 15px;
}

.order-success p {
  margin: 10px 0;
}

/* =========================
   MOBILE RESPONSIVE
========================= */

@media (max-width: 768px) {

  .navbar {
    padding: 14px 18px;

    flex-direction: column;

    align-items: flex-start;
  }

  .navbar-links {
    width: 100%;

    flex-wrap: wrap;

    gap: 12px;
  }

  .dashboard-container,
  .analytics-page,
  .shop-page,
  .cart-page,
  .orders-page {
    width: 94%;

    margin: 20px auto;
  }

  .product-grid {
    grid-template-columns:
      repeat(2, 1fr);

    gap: 15px;
  }

  .product-card img {
    height: 160px;
  }

  .cart-item {
    align-items: flex-start;

    flex-direction: column;
  }

  .order-status {
    align-items: flex-start;

    flex-direction: column;
  }
}

/* =========================
   SMALL MOBILE
========================= */

@media (max-width: 480px) {

  .product-grid {
    grid-template-columns: 1fr;
  }

  .stats-grid,
  .analytics-grid {
    grid-template-columns: 1fr;
  }

  .form-container {
    padding: 20px;
    margin-top: 25px;
  }

  .navbar h2 {
    font-size: 19px;
  }

  .navbar-links {
    flex-direction: column;
    align-items: flex-start;
  }

  .order-success {
    padding: 25px;
    margin-top: 40px;
  }
}

2. Improve the Navbar

Your current Navbar.jsx should have a clean structure like this:

import { Link, useNavigate } from "react-router-dom";
import { useDispatch, useSelector } from "react-redux";
import { logout } from "../redux/authSlice";

function Navbar() {
  const { user } = useSelector(
    (state) => state.auth
  );

  const dispatch = useDispatch();
  const navigate = useNavigate();

  const handleLogout = () => {
    dispatch(logout());
    navigate("/login");
  };

  return (
    <nav className="navbar">

      <Link to="/">
        <h2>MultiShop</h2>
      </Link>

      <div className="navbar-links">

        {user?.role === "customer" && (
          <>
            <Link to="/shop">
              Shop
            </Link>

            <Link to="/cart">
              Cart
            </Link>

            <Link to="/my-orders">
              My Orders
            </Link>
          </>
        )}

        {user?.role === "vendor" && (
          <>
            <Link to="/vendor-dashboard">
              Dashboard
            </Link>

            <Link to="/products">
              Products
            </Link>

            <Link to="/inventory">
              Inventory
            </Link>

            <Link to="/store-management">
              Store
            </Link>

            <Link to="/vendor-orders">
              Orders
            </Link>

            <Link to="/analytics">
              Analytics
            </Link>
          </>
        )}

        {user?.role === "superadmin" && (
          <Link to="/admin-dashboard">
            Admin Dashboard
          </Link>
        )}

        {user && (
          <button
            onClick={handleLogout}
          >
            Logout
          </button>
        )}

      </div>
    </nav>
  );
}

export default Navbar;
3. Add better status badges

In MyOrders.jsx, instead of:

<strong>
  {order.orderStatus}
</strong>

use:

<span
  className={`status-badge status-${order.orderStatus}`}
>
  {order.orderStatus}
</span>

Do the same in VendorOrders.jsx.

For example:

PLACED       🟡
PROCESSING   🔵
SHIPPED      🟣
DELIVERED    🟢
CANCELLED    🔴

The colors are controlled by CSS rather than hard-coded into the React components.

4. Improve product cards

In Shop.jsx, structure each card like:

<div
  className="product-card"
  key={product._id}
>
  {product.image && (
    <img
      src={product.image}
      alt={product.name}
    />
  )}

  <div className="product-card-content">

    <h3>{product.name}</h3>

    <p>
      {product.description}
    </p>

    <p className="product-price">
      ₹{product.price}
    </p>

    <p>
      Stock: {product.stock}
    </p>

    <button
      onClick={() =>
        handleAddToCart(product)
      }
    >
      Add to Cart
    </button>

  </div>
</div>

This gives each product a proper visual hierarchy.

5. Make the homepage useful

Your current / route can be a simple landing page instead of an empty screen.

In App.jsx, you can create a small home component:

function Home() {
  return (
    <div className="page-container">

      <section className="order-success">

        <h1>
          Welcome to MultiShop
        </h1>

        <p>
          A multi-tenant SaaS e-commerce
          platform for independent vendors.
        </p>

        <br />

        <Link
          to="/shop"
          className="primary-button"
        >
          Start Shopping
        </Link>

      </section>

    </div>
  );
}

Then:

<Route
  path="/"
  element={<Home />}
/>
6. Check mobile view

Run:

cd frontend
npm run dev

Open the application in Chrome.

Press:

F12

Then click the:

📱 Toggle device toolbar

Test:

Mobile
Tablet
Desktop

You should see the product cards automatically change from:

Desktop

┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐
│      │ │      │ │      │ │      │
└──────┘ └──────┘ └──────┘ └──────┘

to:

Mobile

┌──────────────┐
│              │
└──────────────┘

┌──────────────┐
│              │
└──────────────┘

Responsive design is specifically intended to make layouts work across different screen sizes and devices.

7. One important frontend check

Make sure main.jsx still contains:

<BrowserRouter>
  <App />
</BrowserRouter>

and:

<Provider store={store}>

Your structure should remain:

main.jsx
   ↓
Provider
   ↓
BrowserRouter
   ↓
App
   ↓
Navbar + Pages
8. Your UI is now organized
                    MultiShop
                       │
        ┌──────────────┼──────────────┐
        │              │              │
     Customer        Vendor        Super Admin
        │              │              │
      Shop          Dashboard      Admin Dashboard
      Cart          Products
    My Orders       Inventory
                    Store
                    Orders
                    Analytics
