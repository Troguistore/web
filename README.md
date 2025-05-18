<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TROGUI - Tienda Online</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: Arial, sans-serif; background: #fff; color: #333; }
    header {
      background-color: #f97316;
      padding: 20px;
      text-align: center;
      color: white;
    }
    header h1 { font-size: 2rem; }
    header p { margin-top: 10px; font-size: 1rem; }

    .container {
      padding: 20px;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
    }
    .product {
      border: 1px solid #ccc;
      border-radius: 10px;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      background: #fff;
    }
    .product img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .product h3 {
      font-size: 1.1rem;
      margin: 10px;
    }
    .product .price {
      color: #f97316;
      font-weight: bold;
      margin: 0 10px 10px;
    }
    .buttons {
      margin: 10px;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .btn {
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1rem;
    }
    .add-cart {
      background-color: #000;
      color: #fff;
    }
    .buy-whatsapp {
      background-color: #f97316;
      color: #fff;
    }
    .cart-summary {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: #f97316;
      color: white;
      padding: 10px;
      font-size: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  </style>
</head>
<body>
  <header>
    <h1>TROGUI</h1>
    <p>En TROGUI, encuentras productos únicos, útiles, prácticos y perfectos para ti y tu hogar.</p>
  </header>

  <div class="container">
    <div class="products" id="product-list">
      <!-- Productos serán insertados aquí con JS -->
    </div>
  </div>

  <div class="cart-summary" id="cart-summary">
    <span id="cart-count">0 productos</span>
    <span id="cart-total">Total: $0</span>
  </div>

  <script>
    const productos = [
      { nombre: 'Lámpara Luna 3D Decorativa', precio: 49000, imagen: 'https://via.placeholder.com/300?text=Luna' },
      { nombre: 'Estante Giratorio Metálico 360°', precio: 239000, imagen: 'https://via.placeholder.com/300?text=Estante' },
      { nombre: 'Organizador Esquinero de Baño', precio: 59000, imagen: 'https://via.placeholder.com/300?text=Organizador' },
      { nombre: 'Mini Waflera Antiadherente', precio: 49000, imagen: 'https://via.placeholder.com/300?text=Waflera' }
      // Agrega más productos si deseas
    ];

    const carrito = [];
    const contenedor = document.getElementById('product-list');
    const resumen = document.getElementById('cart-summary');
    const cartCount = document.getElementById('cart-count');
    const cartTotal = document.getElementById('cart-total');

    productos.forEach((producto, index) => {
      const card = document.createElement('div');
      card.className = 'product';
      card.innerHTML = `
        <img src="${producto.imagen}" alt="${producto.nombre}" />
        <h3>${producto.nombre}</h3>
        <p class="price">$${producto.precio.toLocaleString()}</p>
        <div class="buttons">
          <button class="btn add-cart" onclick="agregarAlCarrito(${index})">Añadir al carrito</button>
          <button class="btn buy-whatsapp" onclick="comprarWhatsApp(${index})">Comprar por WhatsApp</button>
        </div>
      `;
      contenedor.appendChild(card);
    });

    function actualizarResumen() {
      cartCount.textContent = `${carrito.length} producto${carrito.length !== 1 ? 's' : ''}`;
      const total = carrito.reduce((acc, prod) => acc + prod.precio, 0);
      cartTotal.textContent = `Total: $${total.toLocaleString()}`;
    }

    function agregarAlCarrito(index) {
      carrito.push(productos[index]);
      actualizarResumen();
    }

    function comprarWhatsApp(index) {
      const baseUrl = 'https://wa.me/573053181755';
      let mensaje = '';
      if (carrito.length > 0) {
        mensaje = 'Hola, quiero comprar los siguientes productos:%0A';
        carrito.forEach(p => {
          mensaje += `- ${p.nombre} ($${p.precio.toLocaleString()})%0A`;
        });
        const total = carrito.reduce((acc, prod) => acc + prod.precio, 0);
        mensaje += `%0ATotal: $${total.toLocaleString()}`;
      } else {
        const producto = productos[index];
        mensaje = `Hola, quiero comprar el producto: ${producto.nombre} por $${producto.precio.toLocaleString()}`;
      }
      window.open(`${baseUrl}?text=${mensaje}`, '_blank');
    }
  </script>
</body>
</html>
