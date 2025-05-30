<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Tienda Online</title>
<style>
  body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
  header { padding: 10px; background: #f5f5f5; text-align: center; }
  input[type="text"] { width: 80%; padding: 8px; margin: 10px 0; border-radius: 5px; border: 1px solid #ccc; }
  .container { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; padding: 10px; }
  .product { border: 1px solid #ddd; border-radius: 5px; text-align: center; padding: 10px; }
  .product img { width: 100%; height: 150px; object-fit: cover; border-radius: 5px; }
  .price { color: green; font-weight: bold; margin: 5px 0; }
  .btn { display: block; width: 90%; margin: 5px auto; padding: 8px; border: none; border-radius: 5px; cursor: pointer; }
  .btn-cart { background: black; color: white; }
  .btn-whatsapp { background: orange; color: white; }
</style>
</head>
<body>

<header>
  <h1>Tienda Online</h1>
  <input type="text" id="search" placeholder="Buscar productos...">
</header>

<div class="container" id="products">
  <!-- Productos (puedes añadir más abajo usando el mismo formato) -->
  <div class="product" data-name="Cámara profesional">
    <img src="https://via.placeholder.com/200x150" alt="Cámara profesional">
    <h3>Cámara Profesional</h3>
    <p class="price">$500.000</p>
    <button class="btn btn-cart" onclick="addToCart('Cámara Profesional', 500000)">Añadir al carrito</button>
    <button class="btn btn-whatsapp" onclick="buyWhatsApp('Cámara Profesional', 500000)">Comprar por WhatsApp</button>
  </div>
  <div class="product" data-name="Teléfono inteligente">
    <img src="https://via.placeholder.com/200x150" alt="Teléfono inteligente">
    <h3>Teléfono Inteligente</h3>
    <p class="price">$1.200.000</p>
    <button class="btn btn-cart" onclick="addToCart('Teléfono Inteligente', 1200000)">Añadir al carrito</button>
    <button class="btn btn-whatsapp" onclick="buyWhatsApp('Teléfono Inteligente', 1200000)">Comprar por WhatsApp</button>
  </div>
  <div class="product" data-name="Audífonos inalámbricos">
    <img src="https://via.placeholder.com/200x150" alt="Audífonos inalámbricos">
    <h3>Audífonos Inalámbricos</h3>
    <p class="price">$150.000</p>
    <button class="btn btn-cart" onclick="addToCart('Audífonos Inalámbricos', 150000)">Añadir al carrito</button>
    <button class="btn btn-whatsapp" onclick="buyWhatsApp('Audífonos Inalámbricos', 150000)">Comprar por WhatsApp</button>
  </div>
  <!-- Agrega los otros 4 productos aquí con el mismo formato -->
  <!-- ... -->
</div>

<script>
  const cart = [];

  function addToCart(product, price) {
    cart.push({ product, price });
    alert(`Añadido: ${product}\nTotal: $${cart.reduce((sum, item) => sum + item.price, 0).toLocaleString()}`);
  }

  function buyWhatsApp(product, price) {
    const message = `¡Hola! Quiero comprar:\n- ${product} ($${price.toLocaleString()})`;
    const url = `https://wa.me/573206572598?text=${encodeURIComponent(message)}`;
    window.open(url, '_blank');
  }

  document.getElementById('search').addEventListener('input', function () {
    const searchTerm = this.value.toLowerCase().normalize('NFD').replace(/[\u0300-\u036f]/g, '');
    document.querySelectorAll('.product').forEach(product => {
      const name = product.getAttribute('data-name').toLowerCase().normalize('NFD').replace(/[\u0300-\u036f]/g, '');
      product.style.display = name.includes(searchTerm) ? 'block' : 'none';
    });
  });
</script>

</body>
</html>
