<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>TROGUI - Tienda Colombiana</title>
<style>
  /* Reset */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #fff;
    color: #333;
  }
  /* Barra superior */
  header {
    background: #ff6f00; /* naranja */
    color: white;
    padding: 15px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
  }
  header h1 {
    font-weight: 900;
    font-size: 1.8rem;
  }
  header .envios {
    font-size: 0.9rem;
  }

  /* Buscador */
  #searchBar {
    margin: 20px auto;
    max-width: 600px;
    width: 90%;
    display: flex;
  }
  #searchInput {
    flex: 1;
    padding: 10px 15px;
    border: 2px solid #ff6f00;
    border-right: none;
    border-radius: 5px 0 0 5px;
    font-size: 1rem;
  }
  #searchBtn {
    background: #ff6f00;
    color: white;
    border: 2px solid #ff6f00;
    border-radius: 0 5px 5px 0;
    padding: 10px 20px;
    cursor: pointer;
    font-weight: 700;
    transition: background 0.3s;
  }
  #searchBtn:hover {
    background: #e65c00;
  }

  /* Contenedor productos */
  #productList {
    max-width: 960px;
    margin: 0 auto 60px;
    padding: 0 15px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 20px;
  }

  .productCard {
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    background: #fafafa;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    box-shadow: 0 0 8px rgb(0 0 0 / 0.05);
    transition: box-shadow 0.3s;
  }
  .productCard:hover {
    box-shadow: 0 0 15px rgb(0 0 0 / 0.15);
  }
  .productImg {
    width: 100%;
    cursor: pointer;
    object-fit: contain;
    max-height: 220px;
    background: white;
  }
  .productInfo {
    padding: 12px 15px;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }
  .productName {
    font-weight: 700;
    margin-bottom: 6px;
    font-size: 1.1rem;
  }
  .productPrice {
    color: #ff6f00;
    font-weight: 900;
    margin-bottom: 8px;
  }
  .productDesc {
    flex-grow: 1;
    font-size: 0.9rem;
    color: #555;
  }
  .buttons {
    margin-top: 10px;
    display: flex;
    gap: 10px;
  }
  button {
    flex: 1;
    padding: 10px 0;
    border: none;
    cursor: pointer;
    font-weight: 700;
    border-radius: 5px;
    font-size: 0.95rem;
    transition: background 0.3s;
  }
  .btnAdd {
    background: #ff6f00;
    color: white;
  }
  .btnAdd:hover {
    background: #e65c00;
  }
  .btnWhats {
    background: #25d366; /* verde WhatsApp */
    color: white;
  }
  .btnWhats:hover {
    background: #1da851;
  }

  /* Carrito superior */
  #cartBar {
    position: fixed;
    top: 0; left: 0; right: 0;
    background: white;
    box-shadow: 0 2px 8px rgb(0 0 0 / 0.1);
    padding: 12px 20px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    font-weight: 700;
    font-size: 1rem;
    z-index: 9999;
    gap: 15px;
  }

  /* Modal producto */
  #modal {
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background: rgba(0,0,0,0.7);
    display: none;
    justify-content: center;
    align-items: center;
    padding: 20px;
    z-index: 10000;
  }
  #modalContent {
    background: white;
    max-width: 800px;
    width: 100%;
    border-radius: 8px;
    overflow-y: auto;
    max-height: 90vh;
    display: flex;
    flex-wrap: wrap;
  }
  #modalImg {
    flex: 1 1 300px;
    max-height: 400px;
    object-fit: contain;
    background: #fafafa;
    border-radius: 8px 0 0 8px;
  }
  #modalDetails {
    flex: 1 1 400px;
    padding: 20px;
    display: flex;
    flex-direction: column;
  }
  #modalDetails h2 {
    color: #ff6f00;
    margin-bottom: 10px;
  }
  #modalDetails p {
    flex-grow: 1;
    font-size: 1rem;
    color: #444;
    margin-bottom: 20px;
    white-space: pre-line;
  }
  #modalDetails .modalButtons {
    display: flex;
    gap: 10px;
  }
  #modalClose {
    position: absolute;
    top: 15px;
    right: 20px;
    font-size: 2rem;
    color: white;
    cursor: pointer;
  }
  @media(max-width:600px) {
    #modalContent {
      flex-direction: column;
    }
    #modalImg, #modalDetails {
      flex: 1 1 100%;
      max-height: none;
      border-radius: 8px 8px 0 0;
    }
  }
</style>
</head>
<body>

<header>
  <h1 style="color:#ff6f00;">TROGUI</h1>
  <div class="envios">🚚 Envíos gratis • Pago contra entrega Colombia</div>
</header>

<div id="cartBar">
  Total: <span id="cartTotal">0</span> COP
</div>

<div id="searchBar">
  <input type="text" id="searchInput" placeholder="Buscar productos..." />
  <button id="searchBtn">Buscar</button>
</div>

<section id="productList">
  <!-- Aquí se cargan los productos desde JS -->
</section>

<!-- Modal producto -->
<div id="modal">
  <span id="modalClose">&times;</span>
  <div id="modalContent">
    <img id="modalImg" src="" alt="Producto" />
    <div id="modalDetails">
      <h2 id="modalName"></h2>
      <p id="modalDesc"></p>
      <div class="modalButtons">
        <button class="btnAdd" id="modalAddBtn">Añadir al carrito</button>
        <button class="btnWhats" id="modalWhatsBtn">Comprar por WhatsApp</button>
      </div>
    </div>
  </div>
</div>

<script>
  // Datos de productos
  const products = [
    {
      id: 1,
      name: "Afeitadora 3 en 1",
      price: 59000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg",
      shortDesc: "Recargable 3 en 1 para barba, axilas, nariz y cabello. Orden y estilo siempre.",
      fullDesc: `Afeitadora recargable 3 en 1 que no se note el desorden, te deja listo para todo: barba, axilas, nariz y cabello.`,
    },
    {
      id: 2,
      name: "Organizador para baño 1",
      price: 75000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/883693/1716500557imagen_2024-05-23_164213721.png",
      shortDesc: "Organizador de acero inoxidable, resistente y sin óxido para tu baño u otros espacios.",
      fullDesc: `Organizador de baño hecho en acero inoxidable y ABS, resistente, sin óxido, con 4 repisas y colgadores.`,
    },
    {
      id: 3,
      name: "Organizador para baño 2",
      price: 59000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/883706/1716500639Screenshot_2024-05-23-16-48-32-042_com.google.android.apps_.photos.jpg",
      shortDesc: "Multiuso, sin óxido y resistente, ideal para organizar tu baño de forma práctica.",
      fullDesc: `Organizador multiuso de baño, sin óxido y resistente, con diseño compacto y práctico.`,
    },
    {
      id: 4,
      name: "Organizador para baño 3",
      price: 59000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/883708/1716500691Screenshot_2024-05-23-16-48-55-090_com.google.android.apps_.photos.jpg",
      shortDesc: "Esquinero para baño, con espacio para toallas y productos, sin instalación necesaria.",
      fullDesc: `Esquinero para baño con múltiples niveles para toallas, productos y más, fácil de colocar sin instalación.`,
    }
  ];

  let cart = [];

  // Referencias DOM
  const productList = document.getElementById('productList');
  const cartTotalEl = document.getElementById('cartTotal');
  const searchInput = document.getElementById('searchInput');
  const searchBtn = document.getElementById('searchBtn');
  const modal = document.getElementById('modal');
  const modalImg = document.getElementById('modalImg');
  const modalName = document.getElementById('modalName');
  const modalDesc = document.getElementById('modalDesc');
  const modalAddBtn = document.getElementById('modalAddBtn');
  const modalWhatsBtn = document.getElementById('modalWhatsBtn');
  const modalClose = document.getElementById('modalClose');

  // Función para mostrar productos en pantalla
  function renderProducts(list) {
    productList.innerHTML = "";
    list.forEach(prod => {
      const card = document.createElement('div');
      card.className = 'productCard';

      card.innerHTML = `
        <img src="${prod.img}" alt="${prod.name}" class="productImg" data-id="${prod.id}" />
        <div class="productInfo">
          <div class="productName">${prod.name}</div>
          <div class="productPrice">${prod.price.toLocaleString()} COP</div>
          <div class="productDesc">${prod.shortDesc}</div>
          <div class="buttons">
            <button class="btnAdd" data-id="${prod.id}">Añadir al carrito</button>
            <button class="btnWhats" data-id="${prod.id}">Comprar por WhatsApp</button>
          </div>
        </div>
      `;
      productList.appendChild(card);
    });
  }

  // Añadir producto al carrito
  function addToCart(id) {
    const prod = products.find(p => p.id === id);
    if(!prod) return;
    const found = cart.find(c => c.id === id);
    if(found) {
      found.qty++;
    } else {
      cart.push({...prod, qty: 1});
    }
    updateCartTotal();
  }

  // Actualiza el total en el carrito
  function updateCartTotal() {
    const total = cart.reduce((acc, item) => acc + item.price * item.qty, 0);
    cartTotalEl.textContent = total.toLocaleString();
  }

  // Limpieza de texto para búsqueda: elimina tildes y pasa a minúsculas
  function cleanText(text) {
    return text.normalize("NFD").replace(/[\u0300-\u036f]/g, "").toLowerCase();
  }

  // Búsqueda simple ignorando tildes y errores simples
  function searchProducts(term) {
    const cleanedTerm = cleanText(term);
    return products.filter(p => cleanText(p.name).includes(cleanedTerm) || cleanText(p.shortDesc).includes(cleanedTerm));
  }

  // Mostrar modal con detalles del producto
  function openModal(id) {
    const prod = products.find(p => p.id === id);
    if(!prod) return;
    modalImg.src = prod.img;
    modalName.textContent = prod.name;
    modalDesc.textContent = prod.fullDesc;
    modal.style.display = 'flex';

    // Añadir al carrito desde modal
    modalAddBtn.onclick = () => {
      addToCart(id);
      alert(`Producto "${prod.name}" añadido al carrito.`);
    };
    // Comprar por WhatsApp desde modal
    modalWhatsBtn.onclick = () => {
      sendWhatsApp([ {...prod, qty: 1} ]);
    }
  }

  // Cerrar modal
  modalClose.onclick = () => {
    modal.style.display = 'none';
  };
  modal.onclick = e => {
    if(e.target === modal) modal.style.display = 'none';
  };

  // Botón añadir al carrito en lista productos
  productList.addEventListener('click', e => {
    if(e.target.classList.contains('btnAdd')) {
      const id = Number(e.target.dataset.id);
      addToCart(id);
      alert("Producto añadido al carrito.");
    }
    if(e.target.classList.contains('btnWhats')) {
      const id = Number(e.target.dataset.id);
      const prod = products.find(p => p.id === id);
      sendWhatsApp([ {...prod, qty: 1} ]);
    }
    if(e.target.classList.contains('productImg')) {
      const id = Number(e.target.dataset.id);
      openModal(id);
    }
  });

  // Enviar mensaje a WhatsApp con lista de productos
  function sendWhatsApp(items) {
    if(items.length === 0) return;
    let msg = `Hola, quiero hacer un pedido en TROGUI:\n`;
    items.forEach(item => {
      msg += `- ${item.name} x${item.qty} = ${(item.price * item.qty).toLocaleString()} COP\n`;
    });
    const total = items.reduce((acc, i) => acc + i.price * i.qty, 0);
    msg += `Total: ${total.toLocaleString()} COP\n\nGracias!`;
    const url = `https://wa.me/573001234567?text=${encodeURIComponent(msg)}`;
    window.open(url, '_blank');
  }

  // Botón comprar carrito WhatsApp
  const cartBar = document.getElementById('cartBar');
  cartBar.addEventListener('click', () => {
    if(cart.length === 0) {
      alert("El carrito está vacío.");
      return;
    }
    sendWhatsApp(cart);
  });

  // Búsqueda
  searchBtn.addEventListener('click', () => {
    const term = searchInput.value.trim();
    if(term === '') {
      renderProducts(products);
    } else {
      const results = searchProducts(term);
      if(results.length === 0) alert('No se encontraron productos.');
      renderProducts(results);
    }
  });

  // Enter en input búsqueda activa botón buscar
  searchInput.addEventListener('keydown', e => {
    if(e.key === 'Enter') searchBtn.click();
  });

  // Render inicial
  renderProducts(products);
  updateCartTotal();
</script>

</body>
</html>
