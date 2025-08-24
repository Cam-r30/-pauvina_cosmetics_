# pauvina
Descubre la belleza que llevas dentro con nuestros productos premium

<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Pauvina Cosmetics</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet"/>
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet"/>
<style>
    body {
      scroll-behavior: smooth;
      background-image: url('https://www.transparenttextures.com/patterns/flowers.png');
      background-color: #fff8f9;
      color: #311917cb;
      font-family: 'Segoe UI', sans-serif;
    }
    .navbar {
      background: linear-gradient(90deg, #b05772, #e68ca0);
    }
    .navbar-brand, .nav-link, .offcanvas-title {
      color: #fff !important;
    }
    header {
      background-image: url('https://images.unsplash.com/photo-1607083200912-d3f56859c891?auto=format&fit=crop&w=1200&q=80');
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-color: #a67873;
    }
    .product-card {
      background-color: #fff0ed;
      border: 1px solid #d8b6a4;
      border-radius: 15px;
      padding: 20px;
      margin: 15px;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    .product-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(176, 87, 114, 0.2);
    }
    .product-img-container {
        width: 100%;
        height: 250px;
        overflow: hidden;
        border-radius: 10px;
        background-color: #ffffff;
        margin-bottom: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .product-img {
      max-width: 100%;
      max-height: 100%;
      object-fit: contain;
      padding: 10px;
    }
    .carousel-item .d-block {
      max-height: 230px;
      object-fit: contain;
      margin: auto;
    }
    .color-options {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin: 10px 0;
    }
    .color-option {
      width: 25px;
      height: 25px;
      border-radius: 50%;
      border: 2px solid #fff;
      cursor: pointer;
      transition: transform 0.2s ease;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .color-option:hover {
      transform: scale(1.2);
    }
    .color-option.selected {
      border: 3px solid #b05772;
      transform: scale(1.2);
    }
    footer {
      background: linear-gradient(45deg, #a05c68, #7e2e3c);
      margin-top: 40px;
      text-align: center;
      padding: 30px;
      color: white;
    }
    footer a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: opacity 0.3s ease;
    }
    footer a:hover {
      opacity: 0.8;
    }
    .social-icon {
      font-size: 20px;
      vertical-align: middle;
    }
    .hero-section {
      background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 100%);
      padding: 60px 0;
      text-align: center;
    }
    .category-filter {
      background: rgba(255, 255, 255, 0.9);
      padding: 20px;
      border-radius: 15px;
      margin: 20px 0;
    }
    .cart-item-color {
      font-size: 12px;
      color: #666;
      font-style: italic;
    }
    .toast {
      z-index: 9999;
    }
    .stock-info {
        font-weight: bold;
        margin-top: 10px;
    }
    .stock-available {
        color: green;
    }
    .stock-out {
        color: red;
    }
    /* Estilos mejorados para el carrito */
    .offcanvas-body {
        padding: 1rem;
    }
    .cart-item {
        display: flex;
        align-items: center;
        margin-bottom: 1rem;
        border-bottom: 1px solid #eee;
        padding-bottom: 1rem;
    }
    .cart-item:last-child {
        border-bottom: none;
    }
    .cart-item-img {
        width: 70px;
        height: 70px;
        border-radius: 8px;
        margin-right: 15px;
        object-fit: cover;
    }
    .cart-item-details {
        flex-grow: 1;
    }
    .cart-item-details h6 {
        margin-bottom: 0;
    }
    .remove-item-btn {
        background: none;
        border: none;
        color: #dc3545;
        font-size: 1.2rem;
        transition: color 0.2s;
    }
    .remove-item-btn:hover {
        color: #c82333;
    }
    .cart-summary {
        padding: 1rem;
        border-top: 2px solid #f8f9fa;
    }
  </style>
</head>
<body>
<nav class="navbar navbar-expand-lg sticky-top shadow">
<div class="container">
<a class="navbar-brand fw-bold fs-4" href="#"><i class="fas fa-spa me-2"></i>Pauvina Cosmetics</a>
<button class="navbar-toggler" data-bs-target="#navbarNav" data-bs-toggle="collapse" type="button">
<span class="navbar-toggler-icon"></span>
</button>
<div class="collapse navbar-collapse justify-content-end" id="navbarNav">
<ul class="navbar-nav align-items-center">
<li class="nav-item mx-2">
<a class="nav-link active" href="#">Inicio</a>
</li>
<li class="nav-item mx-2">
<a class="nav-link" href="#product-list">Productos</a>
</li>
<li class="nav-item mx-2">
<button class="btn btn-outline-light" data-bs-target="#cart" data-bs-toggle="offcanvas">
  <i class="fas fa-shopping-cart me-2"></i>Carrito (<span id="cart-count">0</span>)
</button>
</li>
</ul>
</div>
</div>
</nav>

<header class="text-white text-center py-5">
<div class="container">
<h1 class="display-4 fw-bold mb-3">@pauvina_cosmetics_</h1>
<p class="lead mb-4">Descubre la belleza que llevas dentro con nuestros productos premium</p>
<a class="btn btn-success btn-lg mt-3" href="https://wa.me/573004439621" target="_blank">
  <i class="fab fa-whatsapp me-2"></i>Escríbenos por WhatsApp
</a>
</div>
</header>

<section class="hero-section">
<div class="container">
<h2 class="text-white mb-4">Nuestra Colección</h2>
<div class="category-filter text-center">
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('all')">Todos</button>
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('corrector')">Correctores</button>
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('cejas')">Cejas</button>
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('polvo')">Polvos</button>
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('pestañina')">Pestañinas</button>
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('labial')">Labiales</button>
  <button class="btn btn-outline-primary me-2 mb-2" onclick="filterProducts('velos')">Velos</button>
</div>
</div>
</section>

<main class="container mt-4">
<div class="row" id="product-list"></div>
</main>

<footer>
<div class="container">
<p>© 2025 Pauvina Cosmetics - Todos los derechos reservados</p>
<div class="d-flex justify-content-center mt-3 flex-wrap">
<a href="https://wa.me/573004439621" target="_blank">
  <i class="fab fa-whatsapp social-icon"></i> WhatsApp
</a>
<a href="https://www.instagram.com/pauvina_cosmetics_" target="_blank">
  <i class="fab fa-instagram social-icon"></i> Instagram
</a>
<a href="https://www.facebook.com" target="_blank">
  <i class="fab fa-facebook social-icon"></i> Facebook
</a>
</div>
</div>
</footer>

<div class="offcanvas offcanvas-end" id="cart" tabindex="-1">
<div class="offcanvas-header">
<h5 class="offcanvas-title"><i class="fas fa-shopping-cart me-2"></i>Carrito de Compras</h5>
<button class="btn-close" data-bs-dismiss="offcanvas" type="button"></button>
</div>
<div class="offcanvas-body">
<div id="cart-items">
  <p>No hay productos en el carrito.</p>
</div>
</div>
<div class="cart-summary px-3 pb-3">
<div class="mb-2">
  <label class="form-label" for="code">Código de descuento</label>
  <div class="input-group">
    <input class="form-control" id="code" placeholder="Ingresa tu código" type="text"/>
    <button class="btn btn-outline-secondary" onclick="updateCart()">Aplicar</button>
  </div>
</div>
<div class="d-flex justify-content-between my-2">
  <strong>Total:</strong>
  <strong>$<span id="cart-total">0</span></strong>
</div>
<button class="btn btn-outline-danger mt-2 w-100" onclick="clearCart()">
  <i class="fas fa-trash me-2"></i>Vaciar carrito
</button>
<a class="btn btn-success mt-2 w-100" href="#" id="checkout-link" target="_blank">
  <i class="fab fa-whatsapp me-2"></i>Finalizar compra por WhatsApp
</a>
</div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
<script>
const products = [
  {
    id: 1,
    nombre: 'Corrector de ojeras Bloomshell',
    precio: 16500,
    img: ['imagenes/cb1.jpg', 'imagenes/cb2.jpg'],
    categoria: 'corrector',
    colores: [
      { nombre: '00', codigo: '#ffebee', stock: 1 },
      { nombre: '01', codigo: '#ef9a9a', stock: 1 },
      { nombre: '03', codigo: '#f5f5dc', stock: 1 },
      { nombre: '05', codigo: '#d2b48c', stock: 2 },
      { nombre: '07', codigo: '#a52a2a', stock: 1 },
      { nombre: '08', codigo: '#8d6e63', stock: 1 }
    ]
  },
  {
    id: 2,
    nombre: 'Corrector de ojeras Ani-k',
    precio: 18500,
    img: ['imagenes/ca1.jpg', 'imagenes/ca2.jpg'],
    categoria: 'corrector',
    colores: [
      { nombre: '00', codigo: '#f5f5dc', stock: 1 },
      { nombre: '01', codigo: '#d2b48c', stock: 1 },
      { nombre: '03', codigo: '#a52a2a', stock: 2 },
      { nombre: '04', codigo: '#bcaaa4', stock: 1 },
      { nombre: '05', codigo: '#8d6e63', stock: 1 }
    ]
  },
  {
    id: 3,
    nombre: 'Gel de cejas Melu by Ruby Rose',
    precio: 15400,
    img: ['imagenes/gc1.jpg', 'imagenes/gc2.jpg'],
    categoria: 'cejas',
    colores: [
      { nombre: 'Transparente', codigo: '#ffffff', stock: 5 }
    ]
  },
  {
    id: 4,
    nombre: 'Polvo suelto de Girly 20g',
    precio: 30900,
    img: ['imagenes/ps1.jpg' ],
    categoria: 'polvo',
    colores: [
      { nombre: 'Natural', codigo: '#d7ccc8', stock: 2 }
    ]
  },
  {
    id: 5,
    nombre: 'Corrector de ojeras Bloomshell 10ml nueva presentacion',
    precio: 17500,
    img: ['imagenes/cn1.jpg', 'imagenes/cn2.jpg'],
    categoria: 'corrector',
    colores: [
      { nombre: '01', codigo: '#ef9a9a', stock: 2 },
      { nombre: '02', codigo: '#ef9a9e', stock: 1 },
      { nombre: '03', codigo: '#f5f5dc', stock: 2 }
    ]
  },
  {
    id: 6,
    nombre: 'Pestañina Prosa',
    precio: 18000,
    img: ['imagenes/pp1.jpg', 'imagenes/pp2.jpg'],
    categoria: 'pestañina',
    colores: [
      { nombre: 'Profesional Silicon', codigo: '#000000', stock: 2 },
      { nombre: 'Maxi-Volumen', codigo: '#000000', stock: 1 }
    ]
  },
  {
    id: 7,
    nombre: 'Velos faciales hidratantes Bioaqua',
    precio: 2500,
    img: ['imagenes/vf1.jpg', 'imagenes/vf1.jpg'],
    categoria: 'velos',
    colores: [
      { nombre: 'Rosa', codigo: '#ffc0cb', stock: 2 },
      { nombre: 'Morada', codigo: '#800080', stock: 1 },
      { nombre: 'Azul', codigo: '#add8e6', stock: 1 }
    ]
  },
  {
    id: 8,
    nombre: 'Gloss Bonita Ani-k',
    precio: 17900,
    img: ['imagenes/gb1.jpg', 'imagenes/gb1.jpg'], 
    categoria: 'labial',
    colores: [
      { nombre: 'Rojo', codigo: '#d32f2f', stock: 3 },
      { nombre: 'Transparente', codigo: '#fff', stock: 2 },
      { nombre: 'Rosa', codigo: '#f48fb1', stock: 3 }
    ]
  },
  {
    id: 9,
    nombre: 'Gloss Aura Trendy Tono 01',
    precio: 17900,
    img: ['imagenes/a1.jpg', 'imagenes/a2.jpg'],
    categoria: 'labial',
    colores: [
      { nombre: 'tono1', codigo: '#d32f2f', stock: 3 },
      
    ]
  },
  {
    id: 10,
    nombre: 'Gloss de fresa Engol',
    precio: 4500,
    img: ['imagenes/gf1.jpg', 'imagenes/gf2.jpg'],
    categoria: 'labial',
    colores: [
      { nombre: 'unico', codigo: '#ffc0cb', stock: 3 },
      
    ]
  },
  {
    id: 11,
    nombre: 'Shell tint bloomshell',
    precio: 13500,
    img: ['imagenes/sb1.jpg', 'imagenes/sb2.jpg'],
    categoria: 'labial',
    colores: [
      { nombre: 'Tono 3', codigo: '#c64b49', stock: 1 },
      { nombre: 'Tono 4', codigo: '#c25574', stock: 2 },
      { nombre: 'Tono 5', codigo: '#ba414c', stock: 2 }
    ]
  }
];

let cart = [];
let currentFilter = 'all';
let selectedColors = {};

function renderProducts() {
  const productList = document.getElementById('product-list');
  productList.innerHTML = '';
  
  const filteredProducts = currentFilter === 'all' 
    ? products 
    : products.filter(p => p.categoria === currentFilter);

  filteredProducts.forEach((product) => {
    const col = document.createElement('div');
    col.className = 'col-md-4 col-lg-3';
    
    const selectedColorIndex = selectedColors[`${product.id}`] || 0;
    const selectedColor = product.colores.length > 0 ? product.colores[selectedColorIndex].nombre : '';
    const selectedColorStock = product.colores.length > 0 ? product.colores[selectedColorIndex].stock : 0;
    
    const isOutOfStock = selectedColorStock === 0;
    const stockClass = isOutOfStock ? 'stock-out' : 'stock-available';
    const stockText = isOutOfStock ? '¡Agotado!' : `En stock: ${selectedColorStock} unidades`;
    
    const carouselId = `carousel-${product.id}`;
    const carouselIndicators = product.img.map((_, index) => `
      <button type="button" data-bs-target="#${carouselId}" data-bs-slide-to="${index}" class="${index === 0 ? 'active' : ''}" aria-current="${index === 0}" aria-label="Slide ${index + 1}"></button>
    `).join('');
    const carouselItems = product.img.map((imgUrl, index) => `
      <div class="carousel-item ${index === 0 ? 'active' : ''}">
        <img src="${imgUrl}" class="d-block w-100" alt="${product.nombre}">
      </div>
    `).join('');

    col.innerHTML = `
      <div class="product-card" id="product-${product.id}">
        <div id="${carouselId}" class="carousel slide" data-bs-ride="carousel">
          <div class="carousel-indicators">
            ${carouselIndicators}
          </div>
          <div class="carousel-inner">
            ${carouselItems}
          </div>
          <button class="carousel-control-prev" type="button" data-bs-target="#${carouselId}" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button class="carousel-control-next" type="button" data-bs-target="#${carouselId}" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
        
        <h5 class="mt-2">${product.nombre}</h5>
        <p><strong>$${product.precio.toLocaleString()}</strong></p>
        
        ${product.colores.length > 0 ? `
          <label class="form-label">Tono:</label>
          <div class="color-options mb-2" id="color-options-${product.id}">
            ${product.colores.map((color, colorIndex) => `
              <div class="color-option ${colorIndex === selectedColorIndex ? 'selected' : ''}" 
                   style="background-color: ${color.codigo}"
                   title="${color.nombre}"
                   onclick="selectColor(${product.id}, ${colorIndex})"
                   data-color-name="${color.nombre}"></div>
            `).join('')}
          </div>
          <small class="text-muted" id="selected-color-${product.id}">${selectedColor}</small>
        ` : ''}

        <div class="stock-info ${stockClass}" id="stock-info-${product.id}">
            ${stockText}
        </div>
        
        <label class="form-label mt-2" for="qty-${product.id}">Cantidad:</label>
        <input type="number" class="form-control qty-input" id="qty-${product.id}" min="1" value="1" ${isOutOfStock ? 'disabled' : ''}/>
        <button class="btn btn-primary w-100 mt-3" onclick="addToCart(${product.id})" ${isOutOfStock ? 'disabled' : ''}>
          <i class="fas fa-cart-plus me-2"></i>Agregar al carrito
        </button>
      </div>`;
    productList.appendChild(col);
  });
}

function selectColor(productId, colorIndex) {
  selectedColors[`${productId}`] = colorIndex;
  
  const product = products.find(p => p.id === productId);
  const selectedColorStock = product.colores[colorIndex].stock;

  const colorOptions = document.querySelectorAll(`#color-options-${productId} .color-option`);
  colorOptions.forEach((option, index) => {
    if (index === colorIndex) {
      option.classList.add('selected');
    } else {
      option.classList.remove('selected');
    }
  });
  
  const selectedColorText = document.getElementById(`selected-color-${productId}`);
  if (selectedColorText) {
    selectedColorText.textContent = product.colores[colorIndex].nombre;
  }

  const stockInfo = document.getElementById(`stock-info-${productId}`);
  const qtyInput = document.getElementById(`qty-${productId}`);
  const addToCartBtn = stockInfo.nextElementSibling.nextElementSibling;
  
  stockInfo.textContent = selectedColorStock === 0 ? '¡Agotado!' : `En stock: ${selectedColorStock} unidades`;
  stockInfo.classList.toggle('stock-out', selectedColorStock === 0);
  stockInfo.classList.toggle('stock-available', selectedColorStock > 0);
  qtyInput.disabled = selectedColorStock === 0;
  qtyInput.value = selectedColorStock > 0 ? 1 : 0;
  addToCartBtn.disabled = selectedColorStock === 0;
}

function getSelectedColor(productId) {
  const colorIndex = selectedColors[`${productId}`] || 0;
  const product = products.find(p => p.id === productId);
  return product.colores.length > 0 ? product.colores[colorIndex] : null;
}

function addToCart(productId) {
  const qtyInput = document.getElementById(`qty-${productId}`);
  const quantity = parseInt(qtyInput.value);
  const selectedColorData = getSelectedColor(productId);
  const product = products.find(p => p.id === productId);
  
  if (selectedColorData && !isNaN(quantity) && quantity > 0 && selectedColorData.stock >= quantity) {
    for (let i = 0; i < quantity; i++) {
      cart.push({
        id: product.id,
        nombre: product.nombre,
        precio: product.precio,
        img: product.img[0], // Usamos solo la primera imagen para el carrito
        colorSeleccionado: selectedColorData.nombre,
        colorIndex: selectedColors[`${productId}`]
      });
    }
    selectedColorData.stock -= quantity;
    updateCart();
    renderProducts(); // Re-render para actualizar el stock visual
    
    showToast(`${quantity} x ${product.nombre} (${selectedColorData.nombre})`);
  } else if (selectedColorData.stock < quantity) {
    alert(`No hay suficiente stock de ${product.nombre} en el tono ${selectedColorData.nombre}. Disponibles: ${selectedColorData.stock}`);
  }
}

function removeItemFromCart(index) {
  const removedItem = cart[index];
  const product = products.find(p => p.id === removedItem.id);
  
  if (product) {
    const color = product.colores[removedItem.colorIndex];
    if (color) {
      color.stock += 1; // Devolvemos el stock al color correspondiente
    }
  }
  cart.splice(index, 1);
  updateCart();
  renderProducts(); // Re-render para actualizar el stock visual
}

function showToast(message) {
  const toast = document.createElement('div');
  toast.className = 'position-fixed bottom-0 end-0 p-3';
  toast.style.zIndex = '9999';
  toast.innerHTML = `
    <div class="toast show" role="alert">
      <div class="toast-header">
        <strong class="me-auto">✅ Producto agregado</strong>
        <button type="button" class="btn-close" onclick="this.parentElement.parentElement.parentElement.remove()"></button>
      </div>
      <div class="toast-body">
        ${message}
      </div>
    </div>
  `;
  document.body.appendChild(toast);
  setTimeout(() => {
    if (toast.parentElement) {
      toast.remove();
    }
  }, 3000);
}

function updateCart() {
  const cartItems = document.getElementById('cart-items');
  const cartTotal = document.getElementById('cart-total');
  const cartCount = document.getElementById('cart-count');
  const checkoutLink = document.getElementById('checkout-link');

  cartItems.innerHTML = '';
  let total = 0;

  if (cart.length === 0) {
    cartItems.innerHTML = '<p class="text-center text-muted">No hay productos en el carrito.</p>';
  } else {
    cart.forEach((item, index) => {
      total += item.precio;
      const div = document.createElement('div');
      div.className = 'cart-item';
      div.innerHTML = `
        <img src="${item.img}" alt="${item.nombre}" class="cart-item-img">
        <div class="cart-item-details">
          <h6>${item.nombre}</h6>
          <p class="cart-item-color">Tono: ${item.colorSeleccionado}</p>
          <p class="mb-0"><strong>$${item.precio.toLocaleString()}</strong></p>
        </div>
        <button class="remove-item-btn" onclick="removeItemFromCart(${index})">
          <i class="fas fa-trash-alt"></i>
        </button>
      `;
      cartItems.appendChild(div);
    });
  }

  let discount = 0;
  const code = document.getElementById('code')?.value?.trim().toUpperCase();
  if (code === 'PAUVINA10') {
    discount = Math.round(total * 0.10);
  } else if (code === 'PAUVINA15') {
    discount = Math.round(total * 0.15);
  }

  const finalTotal = total - discount;

  cartTotal.textContent = finalTotal.toLocaleString();
  cartCount.textContent = cart.length;

  let message = "¡Hola! Quiero hacer un pedido en Pauvina Cosmetics:\n\n";
  
  const summary = {};
  cart.forEach(item => {
    const key = `${item.nombre}|${item.colorSeleccionado}`;
    summary[`${key}`] = (summary[`${key}`] || { quantity: 0, precio: item.precio });
    summary[`${key}`].quantity++;
  });

  for (const [key, itemData] of Object.entries(summary)) {
    const [nombre, color] = key.split('|');
    const { quantity, precio } = itemData;
    message += `• ${quantity} x ${nombre} (${color}) - $${precio.toLocaleString()} c/u\n`;
  }

  message += `\nSubtotal: $${total.toLocaleString()}`;
  
  if (discount > 0) {
    message += `\nDescuento aplicado (${code}): -$${discount.toLocaleString()}`;
  }
  
  message += `\nTotal a pagar: $${finalTotal.toLocaleString()}`;
  message += `\n\n¡Gracias! 💖`;

  checkoutLink.href = "https://wa.me/573004439621?text=" + encodeURIComponent(message);
}

function filterProducts(category) {
  currentFilter = category;
  renderProducts();
}

function clearCart() {
  if (confirm('¿Estás seguro de que quieres vaciar el carrito?')) {
    // Restaurar stock
    cart.forEach(item => {
      const product = products.find(p => p.id === item.id);
      if (product) {
        const color = product.colores[item.colorIndex];
        if (color) {
          color.stock += 1;
        }
      }
    });

    cart = [];
    updateCart();
    renderProducts();
  }
}

document.addEventListener('DOMContentLoaded', function() {
  renderProducts();
  updateCart();
});
</script>
</body>
</html>