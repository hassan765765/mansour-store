<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mansour Enterprise Store</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" rel="stylesheet">

<style>

/* =========================================================
   GLOBAL SYSTEM
========================================================= */

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:#f4f6f9;
color:#222;
transition:0.4s;
overflow-x:hidden;
}

body.dark{
background:#121212;
color:#eee;
}

.container{
width:92%;
max-width:1400px;
margin:auto;
}

.section{
padding:90px 0;
}

.section-title{
text-align:center;
font-size:40px;
margin-bottom:60px;
font-weight:700;
position:relative;
}

.section-title:after{
content:"";
width:80px;
height:4px;
background:#00c3ff;
display:block;
margin:20px auto 0;
border-radius:5px;
}

/* =========================================================
   TOP BAR
========================================================= */

.top-bar{
background:#111;
color:white;
padding:10px 0;
font-size:14px;
}

.top-bar .container{
display:flex;
justify-content:space-between;
align-items:center;
}

.top-links a{
color:white;
margin-left:15px;
text-decoration:none;
}

/* =========================================================
   HEADER
========================================================= */

header{
background:white;
box-shadow:0 4px 20px rgba(0,0,0,0.05);
position:sticky;
top:0;
z-index:999;
}

body.dark header{
background:#1e1e1e;
}

.header-wrapper{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 0;
}

.logo{
font-size:28px;
font-weight:800;
letter-spacing:3px;
}

nav ul{
list-style:none;
display:flex;
gap:40px;
}

nav a{
text-decoration:none;
color:#222;
font-weight:500;
position:relative;
}

body.dark nav a{
color:#eee;
}

nav a:after{
content:"";
position:absolute;
bottom:-5px;
left:0;
width:0%;
height:2px;
background:#00c3ff;
transition:0.3s;
}

nav a:hover:after{
width:100%;
}

/* =========================================================
   ICONS
========================================================= */

.header-icons{
display:flex;
gap:25px;
align-items:center;
}

.icon-box{
position:relative;
cursor:pointer;
}

.icon-box span{
position:absolute;
top:-8px;
right:-10px;
background:red;
color:white;
font-size:10px;
padding:3px 6px;
border-radius:50%;
}

/* =========================================================
   HERO
========================================================= */

.hero{
height:550px;
background:url('https://images.unsplash.com/photo-1441986300917-64674bd600d8') center/cover;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
color:white;
position:relative;
}

.hero:before{
content:"";
position:absolute;
width:100%;
height:100%;
background:rgba(0,0,0,0.6);
}

.hero-content{
position:relative;
z-index:2;
}

.hero h1{
font-size:55px;
margin-bottom:20px;
}

.btn{
padding:14px 30px;
border:none;
cursor:pointer;
border-radius:30px;
font-weight:600;
transition:0.3s;
}

.btn-primary{
background:#111;
color:white;
}

.btn-primary:hover{
background:#00c3ff;
}

/* =========================================================
   PRODUCTS GRID
========================================================= */

.products-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
gap:35px;
}

.product-card{
background:white;
border-radius:12px;
overflow:hidden;
box-shadow:0 5px 25px rgba(0,0,0,0.08);
transition:0.4s;
position:relative;
}

body.dark .product-card{
background:#1f1f1f;
}

.product-card:hover{
transform:translateY(-10px);
}

.product-card img{
width:100%;
height:280px;
object-fit:cover;
}

.product-info{
padding:20px;
}

.product-info h3{
margin-bottom:10px;
}

.price{
color:#00a86b;
font-weight:700;
font-size:20px;
}

.old-price{
text-decoration:line-through;
color:#999;
font-size:14px;
margin-left:10px;
}

.rating{
color:gold;
margin:5px 0;
}

.badge{
position:absolute;
top:15px;
left:15px;
background:#ff4d4d;
color:white;
padding:5px 10px;
font-size:12px;
border-radius:20px;
}

.specs{
font-size:13px;
margin:10px 0;
line-height:1.6;
}

/* =========================================================
   CART SIDEBAR
========================================================= */

.cart-sidebar{
position:fixed;
right:-450px;
top:0;
width:450px;
height:100%;
background:white;
box-shadow:-5px 0 25px rgba(0,0,0,0.1);
padding:30px;
transition:0.4s;
overflow-y:auto;
z-index:2000;
}

.cart-sidebar.active{
right:0;
}

.cart-item{
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:20px;
border-bottom:1px solid #eee;
padding-bottom:10px;
}

.qty{
display:flex;
gap:8px;
align-items:center;
}

.qty button{
padding:5px 10px;
}

/* =========================================================
   SUMMARY
========================================================= */

.summary{
margin-top:20px;
}

.summary div{
display:flex;
justify-content:space-between;
margin-bottom:10px;
}

/* =========================================================
   FAQ
========================================================= */

.faq-item{
margin-bottom:15px;
border:1px solid #ddd;
border-radius:8px;
overflow:hidden;
}

.faq-question{
padding:15px;
cursor:pointer;
background:#f1f1f1;
font-weight:600;
}

.faq-answer{
display:none;
padding:15px;
}

/* =========================================================
   FOOTER
========================================================= */

footer{
background:#000;
color:white;
padding:70px 0;
text-align:center;
}

/* =========================================================
   WHATSAPP
========================================================= */

.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
color:white;
padding:15px;
border-radius:50%;
font-size:24px;
z-index:3000;
}

/* =========================================================
   SCROLL TOP
========================================================= */

.scroll-top{
position:fixed;
bottom:90px;
right:20px;
background:#00c3ff;
color:white;
padding:10px 15px;
border-radius:50%;
cursor:pointer;
display:none;
}

</style>
</head>
<body>

<div class="top-bar">
<div class="container">
<div>🚚 Free Shipping Over $100 | 🔒 Secure Payment</div>
<div class="top-links">
<a href="#">Track Order</a>
<a href="#">Help</a>
</div>
</div>
</div>

<header>
<div class="container header-wrapper">
<div class="logo">MANSOUR</div>
<nav>
<ul>
<li><a href="#">Home</a></li>
<li><a href="#products">Products</a></li>
<li><a href="#faq">FAQ</a></li>
<li><a href="#contact">Contact</a></li>
</ul>
</nav>
<div class="header-icons">
<div class="icon-box" onclick="toggleDark()"><i class="fa fa-moon"></i></div>
<div class="icon-box" onclick="toggleCart()">
<i class="fa fa-shopping-cart"></i>
<span id="cartCount">0</span>
</div>
</div>
</div>
</header>

<section class="hero">
<div class="hero-content">
<h1>Premium Shopping Experience</h1>
<button class="btn btn-primary">Shop Now</button>
</div>
</section>

<section class="section" id="products">
<div class="container">
<h2 class="section-title">Featured Products</h2>
<div class="products-grid" id="productsContainer"></div>
</div>
</section>

<section class="section" id="faq">
<div class="container">
<h2 class="section-title">Frequently Asked Questions</h2>

<div class="faq-item">
<div class="faq-question" onclick="toggleFAQ(this)">Do you ship internationally?</div>
<div class="faq-answer">Yes we ship worldwide with tracking.</div>
</div>

<div class="faq-item">
<div class="faq-question" onclick="toggleFAQ(this)">What payment methods are accepted?</div>
<div class="faq-answer">Visa, MasterCard, PayPal, Cash on Delivery.</div>
</div>

</div>
</section>

<footer>
© 2026 Mansour Enterprise Store | All Rights Reserved
</footer>

<div class="cart-sidebar" id="cartSidebar">
<h2>Your Cart</h2>
<div id="cartItems"></div>
<div class="summary">
<div><span>Subtotal</span><span id="subtotal">$0</span></div>
<div><span>Tax (5%)</span><span id="tax">$0</span></div>
<div><span>Shipping</span><span>$10</span></div>
<hr>
<div><strong>Total</strong><strong id="total">$0</strong></div>
</div>
<input type="text" id="coupon" placeholder="Coupon Code">
<button class="btn btn-primary" onclick="applyCoupon()">Apply Coupon</button>
</div>

<a href="https://wa.me/96181142884" class="whatsapp" target="_blank">
<i class="fab fa-whatsapp"></i>
</a>

<div class="scroll-top" onclick="scrollTopPage()">
<i class="fa fa-arrow-up"></i>
</div>

<script>

/* PRODUCT DATA */

const products=[
{id:1,name:"Luxury Watch",price:120,old:150,stock:10,img:"https://images.unsplash.com/photo-1518546305927-5a555bb7020d"},
{id:2,name:"Smart Headphones",price:90,old:120,stock:20,img:"https://images.unsplash.com/photo-1518441902117-2a0d5a0d4c3e"},
{id:3,name:"Gaming Mouse",price:45,old:60,stock:30,img:"https://images.unsplash.com/photo-1587202372775-e229f172b9d7"},
{id:4,name:"Leather Bag",price:150,old:190,stock:12,img:"https://images.unsplash.com/photo-1584917865442-de89df76afd3"},
{id:5,name:"Wireless Speaker",price:75,old:95,stock:18,img:"https://images.unsplash.com/photo-1585386959984-a4155224a1ad"},
{id:6,name:"Modern Shoes",price:110,old:140,stock:25,img:"https://images.unsplash.com/photo-1542291026-7eec264c27ff"},
{id:7,name:"Smartphone",price:600,old:699,stock:8,img:"https://images.unsplash.com/photo-1511707171634-5f897ff02aa9"},
{id:8,name:"Sunglasses",price:60,old:85,stock:22,img:"https://images.unsplash.com/photo-1511497584788-876760111969"}
];

let cart=[];
let discount=0;

function renderProducts(){
const container=document.getElementById("productsContainer");
products.forEach(p=>{
container.innerHTML+=`
<div class="product-card">
<div class="badge">SALE</div>
<img src="${p.img}">
<div class="product-info">
<h3>${p.name}</h3>
<div class="price">$${p.price}
<span class="old-price">$${p.old}</span>
</div>
<div class="rating">★★★★☆</div>
<div class="specs">
✔ Premium Quality<br>
✔ Warranty Included<br>
✔ Stock: ${p.stock}<br>
✔ Fast Delivery
</div>
<button class="btn btn-primary" onclick="addToCart(${p.id})">Add To Cart</button>
</div>
</div>
`;
});
}

function addToCart(id){
let item=cart.find(i=>i.id===id);
if(item){item.qty++;}else{
let product=products.find(p=>p.id===id);
cart.push({...product,qty:1});
}
updateCart();
}

function updateCart(){
document.getElementById("cartCount").innerText=cart.length;
const cartItems=document.getElementById("cartItems");
cartItems.innerHTML="";
let subtotal=0;
cart.forEach((item,index)=>{
subtotal+=item.price*item.qty;
cartItems.innerHTML+=`
<div class="cart-item">
<div>${item.name} x ${item.qty}</div>
<div class="qty">
<button onclick="changeQty(${index},-1)">-</button>
<button onclick="changeQty(${index},1)">+</button>
</div>
</div>
`;
});
let tax=subtotal*0.05;
let total=subtotal+tax+10-discount;
document.getElementById("subtotal").innerText="$"+subtotal;
document.getElementById("tax").innerText="$"+tax.toFixed(2);
document.getElementById("total").innerText="$"+total.toFixed(2);
}

function changeQty(i,val){
cart[i].qty+=val;
if(cart[i].qty<=0)cart.splice(i,1);
updateCart();
}

function toggleCart(){
document.getElementById("cartSidebar").classList.toggle("active");
}

function toggleDark(){
document.body.classList.toggle("dark");
}

function applyCoupon(){
let code=document.getElementById("coupon").value;
if(code==="MANSOUR10"){discount=10;alert("Coupon Applied");}
updateCart();
}

function toggleFAQ(el){
let ans=el.nextElementSibling;
ans.style.display=ans.style.display==="block"?"none":"block";
}

function scrollTopPage(){
window.scrollTo({top:0,behavior:"smooth"});
}

window.addEventListener("scroll",()=>{
document.querySelector(".scroll-top").style.display=
window.scrollY>300?"block":"none";
});

renderProducts();

</script>

</body>
</html>


