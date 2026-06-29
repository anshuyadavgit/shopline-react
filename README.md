# ShopLine 🛒

A simple e-commerce front-end built with React, Vite, and React Router. Products are fetched live from the [DummyJSON](https://dummyjson.com) API.

## Features

- **Product Listing Page** — fetches up to 194 products and displays each as a card with image, title, price, and rating.
- **Product Details Page** — click any product to view its full details (`/product/:id`), with an "Add to Cart" button.
- **Cart Page** — view all items added to the cart, increase/decrease quantity, remove items, and see a full bill summary (Subtotal, GST 18%, Delivery, Total).

## Tech Stack

- React 18
- Vite
- React Router DOM
- Axios
- Context API for global cart state (no Redux needed)

## APIs Used

| Purpose | Endpoint |
|---|---|
| Get all products | `GET https://dummyjson.com/products?limit=194` |
| Get single product | `GET https://dummyjson.com/products/:id` |

## Project Structure

```
shopline/
├── public/
│   └── favicon.svg
├── src/
│   ├── api/
│   │   └── products.js         # axios calls to DummyJSON
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── ProductCard.jsx
│   │   ├── Loader.jsx
│   │   └── ErrorMessage.jsx
│   ├── context/
│   │   └── CartContext.jsx     # global cart state + bill calculations
│   ├── pages/
│   │   ├── ProductListing.jsx  # Task 1
│   │   ├── ProductDetails.jsx  # Task 2
│   │   └── Cart.jsx            # Task 3
│   ├── App.jsx                 # routes
│   ├── main.jsx                # entry point
│   ├── App.css
│   └── index.css
├── index.html
├── package.json
└── vite.config.js
```
# shopline-react
