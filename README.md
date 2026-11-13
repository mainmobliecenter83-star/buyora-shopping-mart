<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BUYORA SHOPPING MART</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial;background:#f5f4fa;color:#261044}
header{background:#fff;padding:18px;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap}
.logo{font-size:27px;font-weight:bold;color:#480b82}
.logo span{display:block;font-size:13px;color:#f58220;letter-spacing:3px}
.cart{font-weight:bold;font-size:18px}
.search{display:flex;padding:15px;background:white;gap:5px}
input{padding:14px;flex:1;border:1px solid #ddd;border-radius:25px;font-size:16px;min-width:0}
button{background:#480b82;color:white;border:0;padding:13px 20px;border-radius:25px;cursor:pointer}
nav{display:flex;gap:22px;overflow:auto;padding:18px;background:white;white-space:nowrap}
nav a{color:#480b82;text-decoration:none;font-weight:bold}
.hero{margin:25px;padding:35px;background:linear-gradient(120deg,#39066e,#8116d0,#f58220);color:white;border-radius:25px}
.hero h1{font-size:34px}
.hero button{background:#ffca05;color:#281044;font-weight:bold}
h2{margin:25px 18px}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;padding:15px}
.card{background:white;padding:15px;border-radius:15px;text-align:center}
.card .emoji{font-size:38px}
.products{display:grid;grid-template-columns:repeat(2,1fr);gap:15px;padding:15px}
.product{background:white;border-radius:15px;padding:15px;text-align:center}
.product .pic{font-size:65px;padding:15px}
.price{color:#e66b12;font-weight:bold;font-size:20px}
.product button{width:100%;margin-top:10px}
footer{background:#31075c;color:white;text-align:center;padding:25px;margin-top:30px}
@media(min-width:700px){.products{grid-template-columns:repeat(4,1fr)}}
</style>
</head>
<body>
<header>
<div class="logo">🛍️ BUYORA<span>SHOPPING MART</span></div>
<div class="cart">🛒 Cart: <span id="count">0</span></div>
</header>
<div class="search">
<input id="search" placeholder="Search for products...">
<button onclick="searchProducts()">Search</button>
</div>
<nav>
<a href="#">Home</a><a href="#deals">Hot Deals</a>
<a href="#products">Products</a><a href="#categories">Categories</a>
</nav>
<section class="hero">
<h1>BUYORA SHOPPING MART</h1>
<p>Everything You Need, All in One Place.</p>
<button onclick="document.getElementById('products').scrollIntoView()">Shop Now →</button>
</section>
<h2 id="categories">Shop by Category</h2>
<div class="grid">
<div class="card">📱<h3>Mobiles</h3></div>
<div class="card">🎧<h3>Electronics</h3></div>
<div class="card">👕<h3>Fashion</h3></div>
<div class="card">🏠<h3>Home & Living</h3></div>
<div class="card">🧴<h3>Beauty</h3></div>
<div class="card">⚽<h3>Sports</h3></div>
</div>
<h2 id="deals">🔥 Hot Deals</h2>
<h2 id="products">Our Products</h2>
<div class="products" id="list">
<div class="product"><div class="pic">📱</div><h3>Smartphone</h3><p class="price">Rs. 25,000</p><button onclick="addCart()">Add to Cart</button></div>
<div class="product"><div class="pic">🎧</div><h3>Wireless Headphones</h3><p class="price">Rs. 2,500</p><button onclick="addCart()">Add to Cart</button></div>
<div class="product"><div class="pic">⌚</div><h3>Smart Watch</h3><p class="price">Rs. 3,000</p><button onclick="addCart()">Add to Cart</button></div>
<div class="product"><div class="pic">👟</div><h3>Sports Shoes</h3><p class="price">Rs. 4,500</p><button onclick="addCart()">Add to Cart</button></div>
</div>
<footer>
<h2>BUYORA SHOPPING MART</h2>
<p>Everything You Need, All in One Place.</p>
<p>Pakistan 🇵🇰</p>
</footer>
<script>
let count=0;
function addCart(){
count++;
document.getElementById('count').textContent=count;
alert('Product added to your cart!');
}
function searchProducts(){
let q=document.getElementById('search').value.toLowerCase();
document.querySelectorAll('.product').forEach(p=>{
p.style.display=p.innerText.toLowerCase().includes(q)?'block':'none';
});
}
</script>
</body>
</html>
