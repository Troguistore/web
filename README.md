<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TROGUI - Tu tienda confiable</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #f5f5f5;
    }
    header {
      background-color: #fff;
      padding: 1rem;
      text-align: center;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    header h1 {
      color: #ff6600;
      margin: 0;
    }
    header p {
      color: #333;
      font-size: 0.9rem;
    }
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 1rem;
      padding: 1rem;
    }
    .product-card {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      overflow: hidden;
      display: flex;
      flex-direction: column;
      transition: transform 0.2s ease;
    }
    .product-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .product-info {
      padding: 1rem;
      flex-grow: 1;
    }
    .product-info h3 {
      margin: 0 0 0.5rem;
      font-size: 1rem;
      color: #333;
    }
    .product-info p {
      color: #ff6600;
      font-weight: bold;
      margin: 0 0 0.5rem;
    }
    .buttons {
      display: flex;
      justify-content: space-between;
      padding: 0.5rem 1rem 1rem;
    }
    .btn {
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 6px;
      cursor: pointer;
      font-size: 0.9rem;
    }
    .btn-cart {
      background: #000;
      color: #fff;
    }
    .btn-whatsapp {
      background: #ff6600;
      color: #fff;
    }
    .cart-summary {
      background: #fff;
      padding: 1rem;
      position: sticky;
      bottom: 0;
      border-top: 2px solid #eee;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 -2px 5px rgba(0,0,0,0.05);
    }
    .cart-summary span {
      font-weight: bold;
    }
  </style>
</head>
<body>
  <header>
    <h1>TROGUI</h1>
    <p>Productos prácticos para el hogar que solucionan tus necesidades diarias. Envío gratis y pago contraentrega 🧡</p>
  </header>

  <main class="product-grid" id="productGrid">
    <!-- Aquí se generan los productos -->
  </main>

  <div class="cart-summary">
    <span id="cartCount">0 productos</span>
    <span id="cartTotal">Total: $0</span>
    <button class="btn btn-whatsapp" onclick="buyOnWhatsApp()">Comprar por WhatsApp</button>
  </div>

  <script>
    const whatsappBaseUrl = "https://wa.me/573053928847?text=";

    const products = [
      {
        name: "Estante giratorio 360°",
        price: 189000,
        image: "https://example.com/estante.jpg"
      },
      {
        name: "Organizador de baño esquinero",
        price: 59000,
        image: "https://example.com/organizador.jpg"
      },
      {
        name: "Trapeador mágico 360°",
        price: 59000,
        image: "https://example.com/trapeador.jpg"
      },
      {
        name: "Mini waflera antiadherente",
        price: 79000,
        image: "https://example.com/waflera.jpg"
      }
      // Agrega más productos aquí
    ];

    const cart = [];

    function renderProducts() {
      const grid = document.getElementById("productGrid");
      grid.innerHTML = products.map((p, index) => `
        <div class="product-card">
          <img src="${p.image}" alt="${p.name}" onerror="this.src='https://via.placeholder.com/200'">
          <div class="product-info">
            <h3>${p.name}</h3>
            <p>$${p.price.toLocaleString()}</p>
          </div>
          <div class="buttons">
            <button class="btn btn-cart" onclick="addToCart(${index})">Añadir al carrito</button>
          </div>
        </div>
      `).join("");
    }

    function addToCart(index) {
      cart.push(products[index]);
      updateCart();
    }

    function updateCart() {
      document.getElementById("cartCount").innerText = `${cart.length} producto${cart.length !== 1 ? 's' : ''}`;
      const total = cart.reduce((sum, p) => sum + p.price, 0);
      document.getElementById("cartTotal").innerText = `Total: $${total.toLocaleString()}`;
    }

    function buyOnWhatsApp() {
      if (cart.length === 0) {
        alert("Agrega al menos un producto al carrito.");
        return;
      }
      const items = cart.map(p => `- ${p.name} ($${p.price.toLocaleString()})`).join("%0A");
      const total = cart.reduce((sum, p) => sum + p.price, 0);
      const message = `Hola, quiero comprar los siguientes productos en TROGUI:%0A${items}%0A%0ATotal: $${total.toLocaleString()}`;
      window.open(whatsappBaseUrl + encodeURIComponent(message), "_blank");
    }

    renderProducts();
  </script>
</body>
</html>
