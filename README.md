<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tienda de Productos</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f5f5f5;
    }
    .container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      padding: 40px;
      max-width: 1200px;
      margin: auto;
    }
    .product {
      background: #fff;
      border-radius: 10px;
      padding: 15px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      display: flex;
      flex-direction: column;
      align-items: center;
      transition: transform 0.3s;
    }
    .product:hover {
      transform: translateY(-5px);
    }
    .product img {
      width: 100%;
      max-height: 200px;
      object-fit: cover;
      border-radius: 8px;
    }
    .product h3 {
      font-size: 18px;
      margin: 10px 0 5px;
    }
    .price {
      color: #27ae60;
      font-weight: bold;
      margin-bottom: 10px;
    }
    .description {
      font-size: 14px;
      text-align: center;
      margin-bottom: 15px;
    }
    .whatsapp-button {
      background-color: #25d366;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      text-decoration: none;
      font-size: 14px;
      transition: background 0.3s;
    }
    .whatsapp-button:hover {
      background-color: #1ebe57;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="product">
      <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg" alt="Afeitadora 3 en 1">
      <h3>Afeitadora Recargable 3 en 1</h3>
      <div class="price">$59.000</div>
      <div class="description">Barba, axilas, nariz y cabello. Práctica, recargable y portátil.</div>
      <a class="whatsapp-button" href="https://wa.me/573206572598?text=%C2%A1Hola!%20Quisiera%20realizar%20una%20compra%20en%20tu%20tienda.%20%C2%BFPuedes%20ayudarme%20con%20los%20detalles%20de%20la%20Afeitadora%203%20en%201?" target="_blank">Comprar por WhatsApp</a>
    </div>

    <div class="product">
      <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/883693/1716500557imagen_2024-05-23_164213721.png" alt="Organizador de Baño 3 niveles">
      <h3>Organizador de Baño 3 Niveles</h3>
      <div class="price">$75.000</div>
      <div class="description">Estructura metálica para mantener tu baño organizado sin ocupar espacio.</div>
      <a class="whatsapp-button" href="https://wa.me/573206572598?text=%C2%A1Hola!%20Estoy%20interesado%20en%20el%20organizador%20de%20ba%C3%B1o%20de%203%20niveles.%20%C2%BFMe%20puedes%20dar%20m%C3%A1s%20detalles?" target="_blank">Comprar por WhatsApp</a>
    </div>

    <div class="product">
      <img src="https://d39ru7awumhhs2.cloudfront.net/colombia/products/715143/17105582201707951386Captura%20de%20pantalla%202024-02-14%20175254.png" alt="Mini Impresora Portátil">
      <h3>Mini Impresora Portátil</h3>
      <div class="price">$65.000</div>
      <div class="description">Imprime sin tinta desde tu celular: notas, fotos, listas y más.</div>
      <a class="whatsapp-button" href="https://wa.me/573206572598?text=%C2%A1Hola!%20Quiero%20comprar%20la%20mini%20impresora%20port%C3%A1til.%20%C2%BFMe%20puedes%20ayudar%20con%20la%20compra?" target="_blank">Comprar por WhatsApp</a>
    </div>
  </div>
</body>
</html>
