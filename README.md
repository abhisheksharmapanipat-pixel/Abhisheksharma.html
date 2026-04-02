# Abhisheksharma.html<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ritu Butiq - Best Fits</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  scroll-behavior: smooth;
}

/* HERO */
.hero {
  height: 100vh;
  background: url('https://i.ibb.co/Z6J0LWYJ/IMG-3403.jpg') no-repeat center/cover;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: white;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 10px;
}

.hero p {
  font-size: 1.5rem;
}

.btn {
  background: black;
  color: white;
  padding: 12px 25px;
  border: none;
  cursor: pointer;
  margin-top: 20px;
}

/* PRODUCTS */
.products {
  padding: 50px;
  text-align: center;
}

.carousel {
  display: flex;
  overflow-x: auto;
  gap: 20px;
}

.card {
  min-width: 250px;
  border: 1px solid #ddd;
  padding: 15px;
}

.card img {
  width: 100%;
}

/* CART FORM */
.form-section {
  padding: 50px;
  background: #f5f5f5;
}

input, textarea {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
}

button {
  padding: 12px;
  background: black;
  color: white;
  border: none;
  cursor: pointer;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 20px;
  background: black;
  color: white;
}
</style>
</head>

<body>

<!-- HERO -->
<section class="hero">
  <div>
    <h1>Ritu Butiq</h1>
    <p>Best Fits</p>
    <button class="btn" onclick="scrollToProducts()">Shop Now</button>
  </div>
</section>

<!-- PRODUCTS -->
<section class="products" id="products">
  <h2>Our Collection</h2>

  <div class="carousel">
    
    <div class="card">
      <img src="https://i.ibb.co/Z6J0LWYJ/IMG-3403.jpg">
      <h3>Stylish Kurti</h3>
      <p>₹799</p>
      <button onclick="addToCart('Stylish Kurti')">Add to Cart</button>
    </div>

    <div class="card">
      <img src="https://i.ibb.co/Z6J0LWYJ/IMG-3403.jpg">
      <h3>Designer Suit</h3>
      <p>₹1499</p>
      <button onclick="addToCart('Designer Suit')">Add to Cart</button>
    </div>

    <div class="card">
      <img src="https://i.ibb.co/Z6J0LWYJ/IMG-3403.jpg">
      <h3>Trendy Dress</h3>
      <p>₹999</p>
      <button onclick="addToCart('Trendy Dress')">Add to Cart</button>
    </div>

  </div>
</section>

<!-- ORDER FORM -->
<section class="form-section">
  <h2>Place Your Order</h2>

  <form onsubmit="sendOrder(event)">
    <input type="text" id="name" placeholder="Your Name" required>
    <input type="text" id="phone" placeholder="Phone Number" required>
    <textarea id="order" placeholder="Your Order" required></textarea>
    <button type="submit">Place Order</button>
  </form>
</section>

<!-- FOOTER -->
<footer>
  <p>Contact: abhisheksharma73031@gmail.com</p>
  <p>© 2026 Ritu Butiq</p>
</footer>

<script>
let cart = [];

function scrollToProducts() {
  document.getElementById("products").scrollIntoView();
}

function addToCart(product) {
  cart.push(product);
  alert(product + " added to cart!");
  document.getElementById("order").value = cart.join(", ");
}

function sendOrder(e) {
  e.preventDefault();

  let name = document.getElementById("name").value;
  let phone = document.getElementById("phone").value;
  let order = document.getElementById("order").value;

  let message = `New Order:%0AName: ${name}%0APhone: ${phone}%0AOrder: ${order}`;

  window.open(`https://wa.me/9050953173?text=${message}`, "_blank");
}
</script>

</body>
</html>
