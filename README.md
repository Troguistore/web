<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tienda Online</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f8f8f8;
      margin: 0;
      padding: 20px;
    }

    .container {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .product {
      background-color: white;
      border-radius: 10px;
      padding: 15px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      display: flex;
      flex-direction: column;
      align-items: center;
      height: 100%;
    }

    .product img {
      max-width: 100%;
      max-height: 200px;
      object-fit: contain;
      margin-bottom: 10px;
    }

    .product h3 {
      font-size: 18px;
      margin: 10px 0 5px;
      text-align: center;
    }

    .product p {
      font-size: 14px;
      text-align: center;
    }

    .price {
      font-weight: bold;
      color: green;
      margin: 10px 0;
      font-size: 16px;
    }

    .buy-btn {
      background-color: orange;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      text-decoration: none;
      font-weight: bold;
      margin-top: auto;
    }

    .buy-btn:hover {
      background-color: darkorange;
    }
  </style>
</head>
<body>
  <h1 style="text-align: center;">Catálogo de Productos</h1>
  <div class="container">

    <div class="product">
      <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg" alt="Afeitadora 3 en 1" />
      <h3>Afeitadora recargable 3 en 1</h3>
      <p>Para barba, axilas, nariz y cabello. ¡Siempre listo!</p>
      <div class="price">$59,000</div>
      <a class="buy-btn" href="https://wa.me/573206572598?text=%C2%A1Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20%C2%BFPuedes%20ayudarme%20con%20los%20detalles%20de">Comprar por WhatsApp</a>
    </div>

    <div class="product">
      <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/883693/1716500557imagen_2024-05-23_164213721.png" alt="Organizador baño 3 niveles" />
      <h3>Organizador de baño 3 niveles</h3>
      <p>Ideal para mantener tu baño cómodo y hermoso.</p>
      <div class="price">$75,000</div>
      <a class="buy-btn" href="https://wa.me/573206572598?text=%C2%A1Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20%C2%BFPuedes%20ayudarme%20con%20los%20detalles%20de">Comprar por WhatsApp</a>
    </div>

    <div class="product">
      <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/715143/17105582201707951386Captura%20de%20pantalla%202024-02-14%20175254.png" alt="Mini impresora térmica portátil" />
      <h3>Mini impresora portátil</h3>
      <p>Imprime fotos, apuntes y más. Sin tinta, ¡sólo con tu celular!</p>
      <div class="price">$65,000</div>
      <a class="buy-btn" href="https://wa.me/573206572598?text=%C2%A1Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20%C2%BFPuedes%20ayudarme%20con%20los%20detalles%20de">Comprar por WhatsApp</a>
    </div>

    <!-- Puedes seguir agregando más productos con el mismo formato -->

  </div>
</body>
</html>
