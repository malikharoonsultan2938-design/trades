# trades
1. FOLDER STRUCTURE (VERY IMPORTANT)

Create your project like this:

agri-trade-hub/
│
├── index.html
├── about.html
├── products.html
├── trade.html
├── contact.html
│
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── app.js
│   └── images/
│       └── placeholder.jpg
│
├── data/
│   └── products.json
│
└── README.md

✅ 2. index.html (HOME)
<!DOCTYPE html>
<html>
<head>
  <title>Agriculture & Fertilizer Trade Hub</title>
  <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>

<header>
  <h1>Agriculture & Fertilizer Industry</h1>
  <nav>
    <a href="index.html">Home</a>
    <a href="products.html">Products</a>
    <a href="trade.html">Trade Center</a>
    <a href="contact.html">Contact</a>
  </nav>
</header>

<section class="hero">
  <h2>Trusted Trade Hub for Seeds, Fertilizers, Wheat, Maize & Corn</h2>
  <p>Connecting traders, buyers, and agriculture industry worldwide.</p>
</section>

<section class="features">
  <div class="card">Seeds Trade</div>
  <div class="card">Fertilizer Supply</div>
  <div class="card">Crop Market</div>
</section>

<footer>
  <p>© 2026 Agriculture & Fertilizer Industry</p>
</footer>

</body>
</html>

✅ 3. products.html (PRODUCT LIST)
<!DOCTYPE html>
<html>
<head>
  <title>Products</title>
  <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>

<h2>Available Products</h2>

<input type="text" id="search" placeholder="Search products...">

<div id="product-list"></div>

<script src="assets/js/app.js"></script>
</body>
</html>

✅ 4. trade.html (BUY / SELL HUB)
<!DOCTYPE html>
<html>
<head>
  <title>Trade Center</title>
  <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>

<h2>Trade Center</h2>

<div class="trade-box">
  <h3>Want to Buy?</h3>
  <p>Browse products and contact sellers.</p>
</div>

<div class="trade-box">
  <h3>Want to Sell?</h3>
  <p>Contact industry owner to list your products.</p>
</div>

</body>
</html>

✅ 5. contact.html
<!DOCTYPE html>
<html>
<head>
  <title>Contact</title>
  <link rel="stylesheet" href="assets/css/style.css">
</head>
<body>

<h2>Contact Industry</h2>

<p>WhatsApp: +92XXXXXXXXX</p>
<p>Phone: +92XXXXXXXXX</p>

</body>
</html>

✅ 6. assets/css/style.css
body {
  font-family: Arial;
  margin: 0;
  background: #f4f7f2;
}

header {
  background: #2e7d32;
  color: white;
  padding: 15px;
}

nav a {
  color: white;
  margin: 10px;
  text-decoration: none;
}

.hero {
  padding: 40px;
  background: #c8e6c9;
}

.card {
  background: white;
  padding: 20px;
  margin: 10px;
  display: inline-block;
}

.trade-box {
  background: white;
  padding: 20px;
  margin: 20px;
}

✅ 7. data/products.json (FAKE DATABASE)
[
  {
    "name": "Hybrid Corn Seed",
    "crop": "Corn",
    "quality": "High Yield",
    "seller": "Trader",
    "contact": "https://wa.me/92XXXXXXXXX"
  },
  {
    "name": "Urea Fertilizer",
    "crop": "Wheat",
    "quality": "Premium",
    "seller": "Industry",
    "contact": "https://wa.me/92XXXXXXXXX"
  }
]

✅ 8. assets/js/app.js
fetch("data/products.json")
  .then(res => res.json())
  .then(data => {
    const list = document.getElementById("product-list");
    data.forEach(p => {
      list.innerHTML += `
        <div class="card">
          <h3>${p.name}</h3>
          <p>Crop: ${p.crop}</p>
          <p>Quality: ${p.quality}</p>
          <p>Seller: ${p.seller}</p>
          <a href="${p.contact}">Contact</a>
        </div>
      `;
    });
  });

✅ 9. README.md (VERY IMPORTANT FOR SELLING)
# Agriculture & Fertilizer Trade Hub

This platform is a professional agriculture industry website for trading seeds, fertilizers, wheat, maize, and corn.

## Technology
HTML, CSS, JavaScript, JSON

## Deployment
Upload files to GitHub  
Enable GitHub Pages  
Website goes live

## Handover
Buyer can:
- Change content
- Add products in JSON
- Update contact info
- Upgrade to login system later

## Future Upgrade
- Admin login
- Trader dashboard
- Buyer accounts
- Online marketplace
