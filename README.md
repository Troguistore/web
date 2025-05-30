<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Tienda Online</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    background: #f9f9f9;
  }
  h1 {
    text-align: center;
    margin: 20px 0;
  }
  .container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
    max-width: 1200px;
    margin: auto;
  }
  .product-card {
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 8px;
    width: calc(33.333% - 20px);
    box-sizing: border-box;
    overflow: hidden;
    display: flex;
    flex-direction: column;
  }
  .product-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  .product-info {
    padding: 10px;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .product-info h3 {
    margin: 10px 0;
    font-size: 16px;
  }
  .product-info p {
    color: green;
    font-weight: bold;
  }
  .buttons {
    display: flex;
    gap: 5px;
    margin-top: 10px;
  }
  .buttons a, .buttons button {
    flex: 1;
    padding: 10px;
    text-align: center;
    text-decoration: none;
    border: none;
    cursor: pointer;
    border-radius: 4px;
    font-size: 14px;
  }
  .add-to-cart {
    background: #000;
    color: #fff;
  }
  .buy-whatsapp {
    background: orange;
    color: #fff;
  }
  @media (max-width: 768px) {
    .product-card {
      width: calc(50% - 20px);
    }
  }
  @media (max-width: 500px) {
    .product-card {
      width: 100%;
    }
  }
</style>
</head>
<body>

<h1>Nuestros Productos</h1>

<div class="container">
  <!-- Producto 1 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg" alt="Afeitadora 3 en 1" />
    <div class="product-info">
      <h3>Afeitadora 3 en 1</h3>
      <p>$59,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20la%20Afeitadora%203%20en%201." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>

  <!-- Producto 2 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/883693/1716500557imagen_2024-05-23_164213721.png" alt="Organizador para baño" />
    <div class="product-info">
      <h3>Organizador para baño</h3>
      <p>$75,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20el%20Organizador%20para%20baño%20de%20$75,000." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>

  <!-- Producto 3 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/715143/17105582201707951386Captura%20de%20pantalla%202024-02-14%20175254.png" alt="Mini impresora portátil" />
    <div class="product-info">
      <h3>Mini impresora portátil</h3>
      <p>$65,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20la%20Mini%20impresora%20portátil." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>

  <!-- Producto 4 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/1728426/1742573039WhatsApp%20Image%202025-03-21%20at%2011.00.35%20AM%20(1).jpeg" alt="Organizador para baño" />
    <div class="product-info">
      <h3>Organizador para baño 2</h3>
      <p>$49,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20el%20Organizador%20para%20baño%20de%20$49,000." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>

  <!-- Producto 5 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/269969/1721317643efrfw.jpg" alt="Hidrolavadora inalámbrica" />
    <div class="product-info">
      <h3>Hidrolavadora inalámbrica</h3>
      <p>$95,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20la%20Hidrolavadora%20inalámbrica." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>

  <!-- Producto 6 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/1020203/1722111413LOZA%2065CM%20CON%20TAPA.jpg" alt="Escurridor de platos" />
    <div class="product-info">
      <h3>Escurridor de platos</h3>
      <p>$135,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20el%20Escurridor%20de%20platos." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>

  <!-- Producto 7 -->
  <div class="product-card">
    <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/806031/17140754471.PNG" alt="Organizador esquinero para baño" />
    <div class="product-info">
      <h3>Organizador esquinero</h3>
      <p>$69,000</p>
      <div class="buttons">
        <button class="add-to-cart">Añadir al carrito</button>
        <a href="https://wa.me/573206572598?text=¡Hola!%20Quisiera%20comprar%20el%20Organizador%20esquinero%20para%20baño." target="_blank" class="buy-whatsapp">Comprar por WhatsApp</a>
      </div>
    </div>
  </div>
</div>

</body>
</html>
