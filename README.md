<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TROGUI | Lo que necesitas, donde lo necesitas</title>
  <style>
    :root {
      --main-color: #ff6600;
      --text-color: #333;
      --bg-color: #fff;
    }
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: var(--bg-color);
      color: var(--text-color);
    }
    header {
      background-color: var(--main-color);
      color: white;
      padding: 1rem;
      text-align: center;
    }
    header h1 {
      margin: 0;
      font-size: 2rem;
    }
    header p {
      margin-top: 0.5rem;
    }
    .cart-bar {
      background-color: #ffe0cc;
      padding: 0.5rem 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .products {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 1rem;
      gap: 1rem;
    }
    .product {
      border: 1px solid #ddd;
      border-radius: 10px;
      width: 100%;
      max-width: 300px;
      display: flex;
      flex-direction: column;
      padding: 1rem;
      background: #fff;
    }
    .product img {
      width: 100%;
      border-radius: 10px;
    }
    .product h3 {
      font-size: 1.1rem;
      margin: 0.5rem 0;
    }
    .price {
      font-weight: bold;
      margin-bottom: 0.5rem;
    }
    .btns {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }
    button, a.btn {
      background-color: var(--main-color);
      color: white;
      border: none;
      padding: 0.6rem;
      border-radius: 5px;
      cursor: pointer;
      text-align: center;
      text-decoration: none;
    }
    .read-more {
      background: transparent;
      color: var(--main-color);
      border: none;
      cursor: pointer;
      margin-bottom: 0.5rem;
    }
    @media (min-width: 600px) {
      .product {
        flex: 0 0 calc(33.333% - 2rem);
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>TROGUI</h1>
    <p>Productos prácticos y funcionales para el hogar que solucionan problemas reales. Envío gratis y pago contra entrega.</p>
  </header>

  <div class="cart-bar">
    <span>🛒 Total: <strong id="totalPrice">$0</strong></span>
    <a class="btn" id="buyWhatsApp" href="#" target="_blank">Comprar por WhatsApp</a>
  </div>

  <section class="products" id="productList">
    <!-- Productos se insertarán aquí con JS -->
  </section>

  <script>
    const products = [
      { name: "Careta paintball máscara airsoft NA535", price: 69000, img: "https://i.imgur.com/H2RQyK3.jpg" },
      { name: "Asador Parrilla BBQ Portátil", price: 84900, img: "https://i.imgur.com/XNo6FCp.jpg" },
      { name: "Dispensador De Agua 3L Botella Plegable 08106", price: 25900, img: "https://i.imgur.com/OSKhhSm.jpg" },
      { name: "Cepillo Dispensador de Jabón Líquido", price: 21900, img: "https://i.imgur.com/oyyA8FO.jpg" },
      { name: "Trapeador Mágico 360º con escurridor integrado", price: 59000, img: "https://i.imgur.com/jk0QQIf.jpg" },
      { name: "Cortador de vegetales multifuncional con cesta", price: 49900, img: "https://i.imgur.com/m6OwXz4.jpg" },
      { name: "Rallador Mandolina Profesional De Acero Inoxidable", price: 23900, img: "https://i.imgur.com/j9V4Vqx.jpg" }
    ];

    let cart = [];

    function renderProducts() {
      const container = document.getElementById("productList");
      products.forEach((p, i) => {
        const card = document.createElement("div");
        card.className = "product";
        card.innerHTML = `
          <img src="${p.img}" alt="${p.name}" />
          <h3>${p.name}</h3>
          <button class="read-more" onclick="alert('Más información sobre: ${p.name}')">Leer más</button>
          <p class="price">$${p.price.toLocaleString()}</p>
          <div class="btns">
            <button onclick="addToCart(${i})">Añadir al carrito</button>
          </div>
        `;
        container.appendChild(card);
      });
    }

    function addToCart(index) {
      cart.push(products[index]);
      updateCart();
    }

    function updateCart() {
      const total = cart.reduce((sum, item) => sum + item.price, 0);
      document.getElementById("totalPrice").textContent = `$${total.toLocaleString()}`;
      const names = cart.map(p => `- ${p.name}`).join("%0A");
      const url = `https://wa.me/573138711131?text=Hola!%20Quiero%20comprar:%0A${names}`;
      document.getElementById("buyWhatsApp").href = url;
    }

    renderProducts();
  </script>
</body>
</html>
