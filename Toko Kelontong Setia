<!DOCTYPE html><html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Toko Kelontong Setia</title>
<style>
body {font-family: Arial; margin:0; background:#f5f5f5;}
header {background:#2e7d32; color:white; padding:15px; text-align:center;}
.container {padding:15px; display:grid; grid-template-columns:repeat(auto-fit,minmax(150px,1fr)); gap:10px;}
.card {background:white; padding:10px; border-radius:10px; box-shadow:0 2px 5px rgba(0,0,0,0.1); text-align:center;}
.card img {width:100%; border-radius:10px;}
button {background:#2e7d32; color:white; border:none; padding:8px; border-radius:5px; cursor:pointer; width:100%;}
#cart {position:fixed; bottom:0; left:0; right:0; background:white; padding:10px; box-shadow:0 -2px 5px rgba(0,0,0,0.2);}
</style>
</head>
<body><header>
<h1>🛒 Toko Kelontong Setia</h1>
<p>Lengkap, Hemat, dan Selalu Setia</p>
</header><div class="container" id="products"></div><div id="cart">
<strong>Keranjang: </strong><span id="cartItems">0 item</span>
<button onclick="checkout()">Checkout via WhatsApp</button>
</div><script>
const phone = "62895425425618";

const products = [
{name:"Beras 5kg", price:65000, img:"https://via.placeholder.com/150"},
{name:"Minyak 1L", price:18000, img:"https://via.placeholder.com/150"},
{name:"Mie Instan", price:3000, img:"https://via.placeholder.com/150"},
{name:"Gula 1kg", price:14000, img:"https://via.placeholder.com/150"},
{name:"Telur 1kg", price:28000, img:"https://via.placeholder.com/150"}
];

let cart = [];

function renderProducts(){
const container = document.getElementById("products");
products.forEach((p,i)=>{
container.innerHTML += `
<div class="card">
<img src="${p.img}">
<h4>${p.name}</h4>
<p>Rp${p.price}</p>
<button onclick="addToCart(${i})">Tambah</button>
</div>`;
});
}

function addToCart(i){
cart.push(products[i]);
updateCart();
}

function updateCart(){
document.getElementById("cartItems").innerText = cart.length + " item";
}

function checkout(){
let message = "Halo, saya mau pesan:%0A";
cart.forEach(p=>{
message += "- " + p.name + "%0A";
});
window.open("https://wa.me/" + phone + "?text=" + message);
}

renderProducts();
</script></body>
</html>
