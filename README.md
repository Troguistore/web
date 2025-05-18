<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TROGUI</title>
  <style>
    :root {
      --orange: #f97316;
      --black: #000;
      --white: #fff;
    }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      color: #333;
    }
    header {
      background-color: var(--orange);
      color: var(--white);
      padding: 1rem;
      text-align: center;
    }
    header h1 {
      margin: 0;
      font-size: 2rem;
    }
    header p {
      margin: 0.5rem 0 0;
      font-size: 1rem;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1rem;
      padding: 1rem;
    }
    .product {
      background: #fff;
      padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .product img {
      max-width: 100%;
      border-radius: 8px;
    }
    .product h3 {
      font-size: 1rem;
      margin: 0.5rem 0;
    }
    .price {
      font-weight: bold;
      margin-bottom: 0.5rem;
    }
    .buttons {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
    }
    button {
      border: none;
      padding: 0.5rem;
      border-radius: 6px;
      cursor: pointer;
      font-size: 1rem;
    }
    .add-to-cart {
      background-color: var(--black);
      color: var(--white);
    }
    .buy-whatsapp {
      background-color: var(--orange);
      color: var(--white);
    }
    .cart-summary {
      text-align: center;
      padding: 1rem;
      background-color: #eee;
      font-size: 1rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>TROGUI</h1>
    <p>Productos prácticos, funcionales y al mejor precio para tu hogar.</p>
  </header>

  <div class="cart-summary" id="cart-summary">
    Total productos: <span id="cart-count">0</span> | Valor total: $<span id="cart-total">0</span>
  </div>

  <section class="products" id="products">
    <!-- Productos se insertarán aquí dinámicamente -->
  </section>

  <script>
    const products = [
      { id: 1, name: 'Estante Giratorio', price: 239000, image: 'https://via.placeholder.com/200' },
      { id: 2, name: 'Organizador de Baño', price: 59000, image: 'https://via.placeholder.com/200' },
      { id: 3, name: 'Trapeador 360º', price: 59000, image: 'https://via.placeholder.com/200' },
      { id: 4, name: 'Mini Waflera', price: 79000, image: 'https://via.placeholder.com/200' },
      // Agrega más productos aquí
    ];

    const cart = [];

    function renderProducts() {
      const container = document.getElementById('products');
      products.forEach(product => {
        const div = document.createElement('div');
        div.className = 'product';
        div.innerHTML = `
          <img src="${product.image}" alt="${product.name}">
          <h3>${product.name}</h3>
          <div class="price">$${product.price.toLocaleString()}</div>
          <div class="buttons">
            <button class="add-to-cart" onclick="addToCart(${product.id})">Añadir al carrito</button>
            <button class="buy-whatsapp" onclick="buyViaWhatsApp(${product.id})">Comprar por WhatsApp</button>
          </div>
        `;
        container.appendChild(div);
      });
    }

    function addToCart(id) {
      const product = products.find(p => p.id === id);
      cart.push(product);
      updateCartSummary();
    }

    function updateCartSummary() {
      const count = cart.length;
      const total = cart.reduce((sum, p) => sum + p.price, 0);
      document.getElementById('cart-count').textContent = count;
      document.getElementById('cart-total').textContent = total.toLocaleString();
    }

    function buyViaWhatsApp(id) {
      let text = "Hola, quiero comprar los siguientes productos en TROGUI:%0A";
      if (cart.length > 0) {
        cart.forEach(p => {
          text += `- ${p.name} ($${p.price.toLocaleString()})%0A`;
        });
      } else {
        const product = products.find(p => p.id === id);
        text += `- ${product.name} ($${product.price.toLocaleString()})%0A`;
      }
      const phone = '573008437886';
      const url = `https://wa.me/${phone}?text=${text}`;
      window.open(url, '_blank');
    }

    renderProducts();
  </script>
</body>
</html>
