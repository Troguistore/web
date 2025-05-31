<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Tienda Colombiana - Productos</title>
<style>
  /* Reset y base */
  * { box-sizing: border-box; margin: 0; padding: 0; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;}
  body { background: #f9f9f9; color: #333; min-height: 100vh; display: flex; flex-direction: column;}
  a { text-decoration: none; color: inherit; }

  /* Header */
  header {
    background: #007a00;
    color: white;
    padding: 10px 20px;
    font-weight: bold;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
  }
  header .envio-info {
    font-size: 1rem;
  }
  header .carrito-info {
    font-size: 1rem;
  }
  header .busqueda {
    margin-top: 10px;
    flex-basis: 100%;
  }
  header input[type="search"] {
    width: 100%;
    max-width: 350px;
    padding: 8px 12px;
    border-radius: 5px;
    border: none;
    font-size: 1rem;
  }

  /* Contenedor principal */
  main {
    flex-grow: 1;
    max-width: 1200px;
    margin: 20px auto;
    padding: 0 15px;
  }
  .descripcion-principal {
    margin-bottom: 20px;
    font-size: 1.1rem;
    text-align: center;
    color: #444;
  }

  /* Productos grid */
  .productos-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    gap: 20px;
  }

  /* Tarjeta producto */
  .producto-card {
    background: white;
    border-radius: 8px;
    box-shadow: 0 2px 6px rgb(0 0 0 / 0.1);
    display: flex;
    flex-direction: column;
    cursor: pointer;
    transition: transform 0.15s ease-in-out;
  }
  .producto-card:hover {
    transform: translateY(-5px);
  }
  .producto-img {
    width: 100%;
    height: 200px;
    object-fit: contain;
    border-radius: 8px 8px 0 0;
    background: #f5f5f5;
  }
  .producto-info {
    padding: 15px;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }
  .producto-nombre {
    font-weight: 600;
    font-size: 1.1rem;
    margin-bottom: 6px;
  }
  .producto-precio {
    font-weight: bold;
    font-size: 1.2rem;
    margin-bottom: 8px;
    color: #007a00;
  }
  .producto-desc {
    flex-grow: 1;
    font-size: 0.9rem;
    color: #555;
  }
  .producto-botones {
    margin-top: 12px;
    display: flex;
    gap: 8px;
  }
  button {
    flex-grow: 1;
    padding: 10px;
    border-radius: 6px;
    border: none;
    font-weight: bold;
    cursor: pointer;
    font-size: 1rem;
    transition: background-color 0.25s ease;
  }
  .btn-anadir {
    background: #007a00;
    color: white;
  }
  .btn-anadir:hover {
    background: #005900;
  }
  .btn-whatsapp {
    background: #25d366;
    color: white;
  }
  .btn-whatsapp:hover {
    background: #1ebe57;
  }

  /* Modal Detalles */
  .modal {
    position: fixed;
    top:0; left:0; right:0; bottom:0;
    background: rgba(0,0,0,0.5);
    display: none;
    align-items: center;
    justify-content: center;
    padding: 15px;
    z-index: 1000;
  }
  .modal.active {
    display: flex;
  }
  .modal-content {
    background: white;
    border-radius: 8px;
    max-width: 700px;
    max-height: 90vh;
    overflow-y: auto;
    padding: 20px;
    position: relative;
    box-shadow: 0 0 20px rgba(0,0,0,0.3);
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
  }
  .modal-close {
    position: absolute;
    right: 15px;
    top: 15px;
    cursor: pointer;
    font-weight: bold;
    font-size: 1.5rem;
    color: #888;
  }
  .modal-img {
    flex: 1 1 250px;
    max-height: 400px;
    object-fit: contain;
    border-radius: 6px;
    background: #f5f5f5;
  }
  .modal-info {
    flex: 1 1 300px;
    display: flex;
    flex-direction: column;
  }
  .modal-nombre {
    font-size: 1.6rem;
    font-weight: 700;
    margin-bottom: 12px;
  }
  .modal-precio {
    font-size: 1.4rem;
    font-weight: 700;
    color: #007a00;
    margin-bottom: 12px;
  }
  .modal-desc {
    flex-grow: 1;
    font-size: 1rem;
    color: #555;
    margin-bottom: 15px;
  }
  .modal-botones {
    display: flex;
    gap: 15px;
  }

  /* Footer WhatsApp flotante */
  .whatsapp-float {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #25d366;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0 4px 10px rgba(0,0,0,0.15);
    cursor: pointer;
    z-index: 1100;
    transition: background-color 0.3s;
  }
  .whatsapp-float:hover {
    background: #1ebe57;
  }
  .whatsapp-float svg {
    width: 32px;
    height: 32px;
    fill: white;
  }

  /* Responsive */
  @media (max-width: 600px) {
    header {
      flex-direction: column;
      align-items: flex-start;
    }
    header .carrito-info {
      margin-top: 10px;
    }
  }
</style>
</head>
<body>

<header>
  <div class="envio-info">🚚 Envíos gratis y pagos contra entrega Colombia</div>
  <div class="carrito-info">Carrito: <span id="carrito-total">0</span> productos | Total: <span id="carrito-importe">$0</span></div>
  <div class="busqueda">
    <input type="search" id="busqueda" placeholder="Buscar productos..." autocomplete="off" />
  </div>
</header>

<main>
  <div class="descripcion-principal">
    Organiza tu vida con productos prácticos, duraderos y pensados para ti. ¡Compra fácil, rápido y con envío gratis!
  </div>

  <div class="productos-grid" id="productos-grid">
    <!-- Productos se insertan aquí con JS -->
  </div>
</main>

<!-- Modal Detalle Producto -->
<div class="modal" id="modal-detalle">
  <div class="modal-content">
    <span class="modal-close" id="modal-close">&times;</span>
    <img src="" alt="Producto" class="modal-img" id="modal-img" />
    <div class="modal-info">
      <h2 class="modal-nombre" id="modal-nombre"></h2>
      <p class="modal-precio" id="modal-precio"></p>
      <p class="modal-desc" id="modal-desc"></p>
      <div class="modal-botones">
        <button class="btn-anadir" id="modal-add-cart">Añadir al carrito</button>
        <button class="btn-whatsapp" id="modal-buy-whatsapp">Comprar por WhatsApp</button>
      </div>
    </div>
  </div>
</div>

<!-- WhatsApp flotante -->
<div class="whatsapp-float" id="whatsapp-float" title="Comprar por WhatsApp">
  <svg viewBox="0 0 24 24"><path d="M20.52 3.48A11.91 11.91 0 0012 0C5.37 0 0 5.37 0 12a11.78 11.78 0 001.58 6.15L0 24l5.93-1.56a11.92 11.92 0 006.07 1.58c6.63 0 12-5.37 12-12a11.94 11.94 0 00-3.48-8.54zm-8.52 16a8 8 0 01-4.19-1.18l-.3-.18-3.13.82.83-3.06-.2-.31A8 8 0 1112 20.52zm3.87-5.11c-.21-.11-1.25-.62-1.44-.69s-.33-.11-.47.11-.54.69-.66.83-.24.16-.45.05a6.29 6.29 0 01-1.85-1.14 6.9 6.9 0 01-1.28-1.58c-.13-.22 0-.34.1-.45s.21-.26.31-.39a.42.42 0 00.06-.35c-.02-.11-.47-1.13-.64-1.55s-.33-.36-.47-.36h-.4a1.15 1.15 0 00-.83.38 3.57 3.57 0 00-1.1 2.62c0 1.54 1.44 3 1.64 3.2s2.83 4.35 6.86 6.1a6.79 6.79 0 002.96.48 4.22 4.22 0 002.98-1.41 4.09 4.09 0 001.23-2.19 3.61 3.61 0 00-.52-2.25 3.25 3.25 0 00-1.99-1.56z"/></svg>
</div>

<script>
  // Datos productos (ejemplo con tres, agrega los demás igual)
  const productos = [
    {
      id: 1,
      nombre: "Afeitadora Plegable 2 en 1",
      precio: 79000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/241636/17019755901701975590Screenshot_139.jpg",
      desc_corta: "Práctica, portátil, recargable y resistente al agua.",
      desc_larga: "Afeitadora plegable 2 en 1 para barba, patillas y cuerpo. Carga USB, resistente al agua, portátil y con garantía de calidad."
    },
    {
      id: 2,
      nombre: "Organizador Baño Esquinero",
      precio: 59000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/883693/17165003051716500306Screenshot_177.jpg",
      desc_corta: "Organizador sin tornillos, resistente y anti-óxido.",
      desc_larga: "Organizador esquinero para baño con 4 repisas, soporte para toalla, sin tornillos, acero inoxidable y plástico ABS, anti-óxido y muy resistente."
    },
    {
      id: 3,
      nombre: "Mopa Giratoria 360º",
      precio: 59000,
      img: "https://d39ru7awumhhs2.cloudfront.net/colombia/products/836380/17116356801711635680Screenshot_132.jpg",
      desc_corta: "Mopa doble cabeza, limpia rápido y fácil.",
      desc_larga: "Mopa giratoria 360 grados con dos cabezas de microfibra turbo, cubeta profunda, limpia 6 veces más rápido, ultra absorbente y fácil de usar."
    },
    // Puedes añadir aquí los otros productos que diste, siguiendo esta estructura
  ];

  const productosGrid = document.getElementById("productos-grid");
  const carritoTotal = document.getElementById("carrito-total");
  const carritoImporte = document.getElementById("carrito-importe");
  const busquedaInput = document.getElementById("busqueda");

  let carrito = [];

  // Función para mostrar productos en la cuadrícula
  function mostrarProductos(productosLista) {
    productosGrid.innerHTML = "";
    productosLista.forEach(producto => {
      const card = document.createElement("div");
      card.className = "producto-card";
      card.innerHTML = `
        <img src="${producto.img}" alt="${producto.nombre}" class="producto-img" loading="lazy" />
        <div class="producto-info">
          <div class="producto-nombre">${producto.nombre}</div>
          <div class="producto-precio">$${producto.precio.toLocaleString('es-CO')}</div>
          <div class="producto-desc">${producto.desc_corta}</div>
          <div class="producto-botones">
            <button class="btn-anadir" data-id="${producto.id}">Añadir al carrito</button>
            <button class="btn-whatsapp" data-id="${producto.id}">Comprar por WhatsApp</button>
          </div>
        </div>
      `;
      productosGrid.appendChild(card);

      // Click en imagen para modal
      card.querySelector(".producto-img").addEventListener("click", () => abrirModal(producto.id));
      // Botón añadir carrito
      card.querySelector(".btn-anadir").addEventListener("click", (e) => {
        e.stopPropagation();
        añadirCarrito(producto.id);
      });
      // Botón comprar WhatsApp
      card.querySelector(".btn-whatsapp").addEventListener("click", (e) => {
        e.stopPropagation();
        comprarPorWhatsApp([producto]);
      });
    });
  }

  // Añadir producto al carrito
  function añadirCarrito(id) {
    const producto = productos.find(p => p.id === id);
    if (!producto) return;
    // Ver si ya está
    const item = carrito.find(i => i.id === id);
    if (item) {
      item.cantidad++;
    } else {
      carrito.push({...producto, cantidad: 1});
    }
    actualizarCarritoUI();
    alert(`Producto "${producto.nombre}" añadido al carrito.`);
  }

  // Actualizar carrito en UI
  function actualizarCarritoUI() {
    const totalCantidad = carrito.reduce((acc, item) => acc + item.cantidad, 0);
    const totalPrecio = carrito.reduce((acc, item) => acc + item.precio * item.cantidad, 0);
    carritoTotal.textContent = totalCantidad;
    carritoImporte.textContent = `$${totalPrecio.toLocaleString('es-CO')}`;
  }

  // Modal detalles producto
  const modal = document.getElementById("modal-detalle");
  const modalClose = document.getElementById("modal-close");
  const modalImg = document.getElementById("modal-img");
  const modalNombre = document.getElementById("modal-nombre");
  const modalPrecio = document.getElementById("modal-precio");
  const modalDesc = document.getElementById("modal-desc");
  const modalAddCart = document.getElementById("modal-add-cart");
  const modalBuyWhatsApp = document.getElementById("modal-buy-whatsapp");

  let productoModalActual = null;

  function abrirModal(id) {
    const producto = productos.find(p => p.id === id);
    if (!producto) return;
    productoModalActual = producto;
    modalImg.src = producto.img;
    modalNombre.textContent = producto.nombre;
    modalPrecio.textContent = `$${producto.precio.toLocaleString('es-CO')}`;
    modalDesc.textContent = producto.desc_larga;
    modal.classList.add("active");
  }
  modalClose.onclick = () => {
    modal.classList.remove("active");
  }
  modalAddCart.onclick = () => {
    if (!productoModalActual) return;
    añadirCarrito(productoModalActual.id);
    modal.classList.remove("active");
  }
  modalBuyWhatsApp.onclick = () => {
    if (!productoModalActual) return;
    comprarPorWhatsApp([productoModalActual]);
  }
  window.onclick = (e) => {
    if(e.target === modal){
      modal.classList.remove("active");
    }
  }

  // WhatsApp flotante botón: envía carrito completo
  const whatsappFloat = document.getElementById("whatsapp-float");
  whatsappFloat.onclick = () => {
    if (carrito.length === 0) {
      alert("Tu carrito está vacío.");
      return;
    }
    comprarPorWhatsApp(carrito);
  }

  // Función para abrir WhatsApp con mensaje
  function comprarPorWhatsApp(listaProductos) {
    const telefono = "57TU_NUMERO_AQUI"; // Cambia TU_NUMERO_AQUI por tu número de WhatsApp en formato internacional sin signos
    let mensaje = "Hola, quiero comprar estos productos:%0A";
    listaProductos.forEach(p => {
      mensaje += `- ${p.nombre} x${p.cantidad || 1} - $${p.precio.toLocaleString('es-CO')}%0A`;
    });
    const total = listaProductos.reduce((acc, p) => acc + p.precio * (p.cantidad || 1), 0);
    mensaje += `%0ATotal: $${total.toLocaleString('es-CO')}`;
    const url = `https://wa.me/${telefono}?text=${mensaje}`;
    window.open(url, '_blank');
  }

  // Función para normalizar texto y hacer búsqueda simple tolerante a tildes y mayúsculas
  function normalizar(texto) {
    return texto.normalize("NFD").replace(/[\u0300-\u036f]/g, "").toLowerCase();
  }

  // Buscador
  busquedaInput.addEventListener("input", () => {
    const query = normalizar(busquedaInput.value.trim());
    if (query === "") {
      mostrarProductos(productos);
      return;
    }
    const filtrados = productos.filter(p => normalizar(p.nombre).includes(query) || normalizar(p.desc_corta).includes(query));
    mostrarProductos(filtrados);
  });

  // Al cargar página
  mostrarProductos(productos);
  actualizarCarritoUI();
</script>

</body>
</html>
