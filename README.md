<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TROGUI - Tienda Online</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #000000;
            color: #ffffff;
        }
        header {
            background-color: #ff6600;
            color: #ffffff;
            padding: 20px;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        header h1 {
            margin: 0;
            color: #ff8c00;
        }
        #search {
            width: 80%;
            padding: 10px;
            margin-top: 10px;
            font-size: 16px;
            max-width: 400px;
            border: none;
            border-radius: 5px;
        }
        .product-list {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
            padding: 20px;
            justify-items: center;
        }
        .product {
            border: 1px solid #cccccc;
            border-radius: 10px;
            padding: 20px;
            width: 250px;
            text-align: center;
            background-color: #f9f9f9;
            color: #000000;
            transition: transform 0.3s ease-in-out;
        }
        .product img {
            max-width: 100%;
            border-radius: 10px;
        }
        .product h2 {
            color: #ff6600;
            font-size: 18px;
            margin: 0;
        }
        .product p {
            font-size: 14px;
            margin: 10px 0;
        }
        .product .price {
            font-size: 16px;
            font-weight: bold;
        }
        .product button {
            padding: 10px 20px;
            font-size: 14px;
            cursor: pointer;
            border-radius: 5px;
            border: none;
        }
        .product .buy-form {
            background-color: #ff0000;
            color: #ffffff;
            margin: 10px 5px;
        }
        .product .buy-form:hover {
            background-color: #cc0000;
        }
        .product .whatsapp {
            background-color: #25d366;
            color: #ffffff;
            margin: 10px 5px;
        }
        .product .whatsapp:hover {
            background-color: #1da851;
        }
        @media (max-width: 768px) {
            .product-list {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        @media (max-width: 480px) {
            .product-list {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>TROGUI</h1>
        <p><strong>Envío gratis y pagos contra entrega a toda Colombia</strong></p>
        <input type="text" id="search" placeholder="Buscar productos...">
    </header>
    <main>
        <div class="product-list" id="product-list">
            <!-- Aquí se insertarán los productos -->
        </div>
    </main>
    <script>
        const products = [
                          {
    name: 'Pistola Hidrogel Automática Recargable',
    price: '85,000',
    description: 'Diversión ilimitada con esta pistola de hidrogel recargable y segura. Perfecta para aventuras al aire libre.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1489881/1731776615D_NQ_NP_2X_994826-MCO80104608792_102024-F.webp'
},
{
    name: 'Organizador Esquinero',
    price: '59,000',
    description: 'Optimiza tu baño con este esquinero de acero inoxidable ajustable. Ideal para espacios pequeños.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1003942/1721709852436703583_1468828630401059_3195827248862152715_n.jpg'
},
{
    name: 'Organizador de Zapatos',
    price: '49,000',
    description: 'Ordena y protege tus zapatos con este práctico organizador. Diseño compacto y resistente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1403853/1729968943Frente%20(6).jpg'
},
{
    name: 'Estante Giratorio de Almacenamiento',
    price: '239,000',
    description: 'Estante de almacenamiento giratorio 360°, ideal para frutas, vegetales y utensilios. Sin instalación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/362530/1730823092WhatsApp%20Image%202024-11-05%20at%2010.55.24%20AM.jpeg'
},
{
    name: 'Escurridor de Platos',
    price: '69,000',
    description: 'Práctico escurridor para platos y cubiertos. Compacto, fácil de usar y moderno.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1154718/172531199671y8Mi2kE7L._AC_SL1500_.jpg'
},
{
    name: 'Escurridor de Platos con Tapa',
    price: '139,000',
    description: 'Escurridor desmontable con tapa. Gran capacidad, fácil de limpiar y perfecto para cualquier cocina.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1327787/172841557418f1ae04fb7-variedades_tv_calle_14-ebi456507si-i0dtncfmwb.png'
},
{
    name: 'Trapeador Giratorio',
    price: '59,000',
    description: 'Limpieza fácil y rápida con este trapeador giratorio 360°. Eficiente y absorbente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1371288/1729444310Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-10-20T115147.559.png'
},
{
    name: 'Proyector HY300 Ultra HD',
    price: '259,000',
    description: 'Proyector portátil Ultra HD con imagen nítida y sonido envolvente. Perfecto para cine en casa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1412015/1730220124w=800,h=800,fit=pad.avif'
},
            {
    name: 'Tapete Antideslizante Absorbente Combo',
    price: '49,000',
    description: 'Tapete de PVC y terciopelo, con absorción de agua y secado rápido. Firme base antideslizante. Ideal para baños, cocinas, y más. Disponible en 120x40 cm y 60x40 cm.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/565196/17027618531702498479Tapete%20de%20cocina08.jpg'
},
{
    name: 'Tapete Alfombra Para Baño Absorbente',
    price: '37,000',
    description: 'Alfombrilla para baño de 40x60 cm, suave y respetuosa con la piel. Absorbe y evapora agua rápidamente. Borde de corte suave, fácil de limpiar y lavar. Amplia aplicación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/257672/17018993201701899320Tapete%20De%20Ba%C3%B1o%20Super%20Absorbente%20Y%20Antideslizante%20A.jpg'
},
{
    name: 'Tapete Mágico Ultra Absorbente 30x40',
    price: '35,000',
    description: 'Tapete absorbente y antideslizante de 30x40 cm. Ideal para mantener tu cocina seca al escurrir platos. Material duradero, fácil de limpiar y plegable sin deformarse.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/884774/1716561673Tapete-absorbente-cocina-FK23D-288.11.jpg'
},
{
    name: 'Soporte Base Computador Portátil Ajustable',
    price: '36,000',
    description: 'Soporte para laptop con 7 configuraciones de altura. Compacto, ligero y portátil. Soporta hasta 20kg, con almohadillas antideslizantes. Diseño ergonómico y plegable, fácil de transportar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/589038/1704838924BASE%20AJUSTABLE%20PARA%20PC.png'
},
{
    name: 'Soporte De Toallas Cocina Baño',
    price: '32,000',
    description: 'Soporte de toallas de acero inoxidable y material ABS, fácil de instalar sin perforar. Polos giratorios para un secado eficiente. Duradero y con diseño elegante para cualquier ambiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/212389/17023012281702301228Screenshot_176.jpg'
},            
{
 name: 'Tapete Antideslizante Galaxia Tpcos07',
                price: '29,000',
                description: 'Tapete de poliéster de 39.5 x 60 cm. Perfecto para decoración y múltiples usos. Ideal para la puerta delantera, cocina, baño, dormitorio, sala, entre otros. Adecuado para amantes del cosmos y mascotas. Textura suave y material antideslizante, duradero y fácil de lavar. Se despacha aleatorio según disponibilidad. Contenido: 1 tapete antideslizante de galaxia. 100% nuevo.',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/79394/17030214261703021426Tapete%20Antideslizante%20Galaxia%20Cosmos%20Multiusos%20TPCOS%204.jpg'
},
{
    name: 'Mini Masajeador De Cuello Electrico',
    price: '29,000',
    description: 'Masajeador de cuello portátil con 6 modos y 6 niveles de fuerza. Funciona con 2 pilas AAA. Compacto y fácil de usar, ideal para aliviar dolores musculares.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/624286/1706630140MASAJEADOR%20DE%20CEULLO%202.webp'
},
{
    name: 'Masajeador De Cuello Con Electrodos',
    price: '49,000',
    description: 'Masajeador con infrarrojo, ultrasonido y electro estimulación. Alivia el dolor muscular y mejora la circulación. Incluye collar masajeador, cable de conexión y electro estimuladores.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/918148/1718726800113574820_1.avif'
},
{
    name: 'Masajeador De Cuello Electrico Alivia Dolor',
    price: '89,000',
    description: 'Masajeador eléctrico con 9 niveles de fuerza y varios modos de masaje. Alivia el dolor muscular en cuello, espalda y más. Incluye sistema de auto cierre de seguridad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/415538/1695853630D_NQ_NP_2X_999480-MCO50742711359_072022-F.webp'
},
{
    name: 'Power Bank Super Cargador',
    price: '79,000',
    description: 'Power bank con carga rápida, 2 puertos USB 3.0 y 1 puerto tipo C. Pantalla indicadora, carga inalámbrica, 6,700mAh de capacidad. Garantía de 30 días por mal funcionamiento.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/850687/1715290627CARGADOR1.JPG'
},
{
    name: 'Power Bank Pb11',
    price: '75,000',
    description: 'Cargador portátil de 10,000 mAh con USB para todo tipo de teléfonos. Batería de polímero de litio. Tamaño compacto, fácil de transportar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/414601/1695830205powerbank-10000-mah-pb11-396294.jpg'
},
{
    name: 'Power Bank Multi Puertos 10000mah',
    price: '89,000',
    description: 'Power Bank de 10,000 mAh, diseño delgado con luz LED. Salidas USB y Tipo C, compatible con iPhone, Android, y más. Ideal para viajes.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/454731/1698079425PILA%20PORTATIL%20CARGADOR%20%20POWER%20BANK%20GAR%20148%2004.png'
},
{
    name: 'Audífonos In Ear Inalámbricos F9 5 Negro',
    price: '39,000',
    description: 'Audífonos in-ear inalámbricos con tecnología TWS. Alcance de 10 m, 5 h de batería, cancelación de ruido, micrófono y estuche de carga. Resistente al agua.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/241251/1701975659170197565910000295_10374437_1253317.png'
},
{
    name: 'Audífonos Manos Libres Micrófono Vidvie',
    price: '29,000',
    description: 'Audífonos con micrófono, control de volumen y botón de control. Conector de 3.5mm. Práctico y cómodo para el uso diario.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/582944/17043128401.jpg'
},
{
    name: 'Audífonos Inalámbricos Bluetooth P9',
    price: '65,000',
    description: 'Audífonos Bluetooth con sonido estéreo claro, control de ruido, y diseño elegante. Alcance de 10-15 m. Livianos y cómodos para llevar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/770644/1712890413gsc_121751346_3168857_3.webp'
},
{
    name: 'Reloj Smart Watch + Audífonos +7 Pulsos',
    price: '109,000',
    description: 'Smartwatch con AirPods y 7 pulsos. Resistente al agua y sudor (IPX4). Ideal para deportes y entretenimiento con ajuste personalizado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/734216/1711486970I20.png'
},
{
    name: 'Funda Protectora Case Audífonos Serie 3',
    price: '29,000',
    description: 'Funda de silicona para Audífonos Serie 3. Protección contra golpes, caídas y suciedad. Disponible en varios colores.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/252950/17019086881701908688IMG-20230505-WA0028.jpg'
},
{
    name: 'Audífonos M25',
    price: '59,000',
    description: 'Audífonos M25 con sonido superior y Bluetooth 5.3. A prueba de salpicaduras, 5 h de reproducción, diseño ergonómico. Perfectos para música y gaming.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/823617/1714671391D_NQ_NP_695218-MCO72871806146_112023-O.webp'
},
{
    name: 'Airpods Audífonos Serie 3 Inalámbricos',
    price: '59,000',
    description: 'AirPods con cancelación activa de ruido y modo ambiente. Conexión instantánea con iPhone y Apple Watch, cómodos para uso diario.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/71767/17030248951703024895WhatsApp%20Image%202022-08-02%20at%202.24.07%20PM.jpeg'
},
{
    name: 'Combo 2x1 Audífonos Air39',
    price: '69,000',
    description: 'Combo de audífonos Air39 con excelente calidad de sonido. Diseño ergonómico y conexión Bluetooth para una experiencia inalámbrica completa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/860340/17157030869combo.png'
},
{ 
  name: 'Impresora Portatil', 
  price: '579,000', 
  description: 'Impresora compacta para viajes. Imprime PDF, fotos, y más. Conexión inalámbrica, batería de 1500 mAh. Tamaño de impresión A4, aplicación para edición gratuita, impresión térmica sin tinta.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/900351/1717095755WhatsApp%20Image%202024-05-30%20at%201.32.08%20PM.jpeg' 
},
{ 
  name: 'Rollo Para Impresora Térmica Celular X5', 
  price: '34,000', 
  description: '', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/633780/1707152621IMPRESORA%20TERMICA%20PARA%20CELULAR%2007.png' 
},
{ 
  name: 'Smart Watch Z78 Ultra', 
  price: '105,000', 
  description: 'Reloj inteligente con monitor de salud, impermeable IP67, pantalla HD de 1.52". Ideal para deportes, conexión sencilla a aplicaciones, múltiples idiomas.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/578944/1703859144cc65592e-d8ea-4498-a809-5f674d65a1a5.jpeg' 
},
{ 
  name: 'Reloj Smart Watch Ld6 Serie 7', 
  price: '79,000', 
  description: 'Reloj inteligente con monitor de ritmo cardíaco, marcador de pasos, carga magnética, notificaciones.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/225802/17019846181701984618reloj-smart-watch-ld6-serie-7-dts-shop-plus-245065060.jpg' 
},
{ 
  name: 'Smart Watch T100 Plus', 
  price: '119,000', 
  description: 'Reloj inteligente con pantalla IPS 1.75", 11 carátulas, 8-10 horas de uso continuo. Funciones avanzadas para deportes y notificaciones.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/48572/17030809051703080905SMART.jpeg' 
},
{ 
  name: 'Smart Watch P100', 
  price: '129,000', 
  description: 'Incluye 2 relojes inteligentes (Serie 7 y 8), 4 pulseras, protector, batería MagSafe, cargador y cable Tipo C.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/747339/1712175705WhatsApp%20Image%202024-04-03%20at%203.06.56%20PM.jpeg' 
},
{ 
  name: 'Smart Watch K950 Ultra Waterproof', 
  price: '129,000', 
  description: 'Reloj inteligente impermeable con monitor de salud, notificaciones, control de música, linterna y personalización de carátulas.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/445317/1697575434iiii.jpeg' 
},
{ 
  name: 'Smart Watch T800 Ultra 2 Doble Correa', 
  price: '59,000', 
  description: '', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/669114/1714512204Imagen%20de%20WhatsApp%202024-04-30%20a%20las%2010.53.14_740e6025.jpg' 
},
{ 
  name: 'Smart Watch Ultra 2 Gama Alta', 
  price: '139,000', 
  description: 'Reloj inteligente premium con alto rendimiento, carga rápida, personalización de carátulas, y monitoreo de salud.', 
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/711848/1710453560WhatsApp%20Image%202024-03-14%20at%209.33.01%20AM.jpeg' 
},
{
  name: 'Reloj Smart Watch Táctil Redondo K700',
  price: '129,000',
  description: 'Reloj inteligente redondo con GPS, pantalla táctil de 1.43", monitor de ritmo cardíaco, 100 modos deportivos, Bluetooth, carga rápida, batería de 3 días, llamadas, notificaciones, asistente de voz.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/916371/1718471497RELOJ%20K700.jpg'
},
{
  name: 'Smart Watch T800',
  price: '65,000',
  description: 'Reloj inteligente con pantalla LCD HD 1.81", Bluetooth, 450mAh, carga inalámbrica, modos deportivos, monitoreo de salud, asistente de voz, personalización de carátulas.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/803240/1713994717WhatsApp%20Image%202024-04-24%20at%204.35.03%20PM.jpeg'
},
{
  name: 'Reloj Smart Watch F8 Fitness Monitor',
  price: '99,000',
  description: 'Reloj inteligente con monitor de ritmo cardiaco, podómetro, control de cámara, alertas de llamadas y mensajes, monitor de sueño, y múltiples aplicaciones de fitness.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/52129/17030803461703080346photo5172861897408621119%20(1).jpg'
},
{
  name: 'Reloj Inteligente Smart Watch T500 Pro',
  price: '49,000',
  description: '',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/733689/1711480324T500%20PRO1.jpg'
},
{
  name: 'Patillera Y Afeitadora Buda',
  price: '33,000',
  description: 'Patillera y rasuradora metálica con diseño antideslizante, corte de cabello potente y silencioso, recargable, incluye 3 guías de corte y cepillo de limpieza.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/88251/171157679217030150911703015091photo_4976845766182152946_x.jpg'
},
{
  name: 'Mini Afeitadora Bb 339d',
  price: '49,000',
  description: 'Afeitadora eléctrica compacta con cuchillas de alta velocidad, cabezal flotante 3D, impermeable IPX7, carga rápida USB y 90 minutos de uso continuo.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/382606/17018728061701872806MIN-2.jpg'
},
{
  name: 'Afeitadora Electrica Profesional',
  price: '85,000',
  description: 'Afeitadora recargable con cabezal flotante, impermeable IPX7, pantalla LED, batería de 1200mAh, y 150 minutos de uso con 2 horas de carga.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/666967/1708543344Afeitadora.png'
},
{
  name: 'Afeitadora Multifuncional 3 En 1 Dorada',
  price: '65,000',
  description: 'Afeitadora eléctrica 3 en 1 con pantalla LCD, motor potente, diseño compacto y portátil, fácil limpieza, carga rápida y uso en cualquier momento.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/862656/1715787767maquina%203%20en%201112.jpg'
},
{
  name: 'Maquina Rasuradora Inalámbrica Wahl Prof',
  price: '85,000',
  description: 'Rasuradora Wahl inalámbrica con batería de litio, 70 minutos de uso continuo, motor potente de 6500 RPM, cuchillas profesionales ajustables para cortes precisos.',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/164867/1702306003170230600310000295_10352990_1155538.png'
},
{
  name: 'Máquina De Afeitar 3 En 1 Rasuradora',
  price: '59,000',
  description: '',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/438077/16971267472.jpg'
},
{
   "name": 'Extractor De Leche Eléctrico Doble',
  price: '69,000',
  description: '',
  image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761617/1712617177EXTRACTOR%20M371%20JPG'
},
{
        "name": "Extractor De Leche Materna Eléctrico",
        "price": "89,000",
        "description": "Extractor de leche materna eléctrico, ideal para uso diario. Compacto y fácil de limpiar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg"
 },
 {
        "name": "Estufa Electrica",
        "price": "69,000",
        "description": "Estufa eléctrica de 1000W con 1 quemador. Compacta, con control de perilla y fácil de usar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/607048/1705793898Captura%20de%20Pantalla%202024-01-20%20a%20la(s)%206.37.09%20p.m..png"
 },
 {
        "name": "Estufa Eléctrica Inducción 1 Puesto",
        "price": "209,000",
        "description": "Estufa eléctrica de inducción con 1 puesto y potencia de 1000W. Diseño moderno y eficiente.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/627300/1706739702Estufa%20de%20inducci%C3%B3n%201%20Puesto%20RH-22%2002.png"
 },
 {
        "name": "Estufa Eléctrica 1 Puesto",
        "price": "59,000",
        "description": "Estufa eléctrica portátil con quemador de acero. Rápido calentamiento, fácil limpieza, 1000W.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/743099/1712032879IMG_1128.jpeg"
 },
 {
        "name": "Estufa Electrica Sokany",
        "price": "85,000",
        "description": "Estufa eléctrica Sokany portátil de 1 hornilla. Compacta, ligera y fácil de transportar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/578368/1703795200ESTUFA%20ELECTRICA.jpg"
 },
 {
        "name": "Protector Para Estufa X4",
        "price": "32,000",
        "description": "Set de 4 protectores para estufa. Resistente al calor, fácil de limpiar y reutilizable.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/271232/17018967231701896723350378197_9293312890743864_7625259818432065463_n.jpg"
  },
  {
        "name": "Encendedor Briquet Estufa con Recarga",
        "price": "29,000",
        "description": "Encendedor briquet para estufa, recargable y duradero. Ideal para uso diario.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/233706/17019839661701983966D_NQ_NP_2X_700354-MCO51407897847_092022-F.jpeg"
    },
    {
        "name": "Estufa 4 Puestos Gas",
        "price": "240,000",
        "description": "Estufa portátil de gas con 4 fogones. Ideal para uso en mesa, color negro.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/780118/1713279823IMG_5652.jpeg"
    },
    {
        "name": "Estufa de Gas Portátil",
        "price": "79,000",
        "description": "Estufa de gas portátil, compacta y fácil de transportar. Ideal para camping.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/801716/1713972320ESTUFA.png"
    },
    {
        "name": "Estufa Eléctrica 2 Puestos Hot Plate",
        "price": "69,000",
        "description": "Estufa eléctrica con 2 puestos, ideal para cocinas pequeñas. Potencia de 2000W.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/241977/17019755451701975545estufa-electrica-2-puestos-hot-plate-jx-200w-D_NQ_NP_763750-MCO43530605272_092020-F.png"
    },
    {
        "name": "Estufa Camping Portable",
        "price": "49,000",
        "description": "Estufa portátil para camping. Ligera, fácil de usar y transportar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/704924/1710261392Imagen%20de%20WhatsApp%202024-03-12%20a%20las%2011.32.53_ed3d2075.jpg"
    },
    {
        "name": "Bolsa Para Dormir Sleeping Bag Sbag01n",
        "price": "109,000",
        "description": "Bolsa para dormir de poliéster y algodón. Compacta y cómoda, ideal para aventuras.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/77320/17030217981703021798Bolsa%20Para%20Dormir%20Sleeping%20Bag%20Camping%201%20Persona%20SBAG01%201.jpg"
    },
    {
        "name": "Cobertor Sleeping Para Bebe Rabbit",
        "price": "49,000",
        "description": "Cobertor para bebé en diseño de conejo. Suave, cálido y perfecto para el sueño.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/95972/17023939341702393934sleeping%20conejo1.jpg"
    },
    {
        "name": "Happy Bolsa De Dormir Cojín Sleeping Par",
        "price": "76,000",
        "description": "Bolsa de dormir con cojín integrado, ideal para camping. Cómoda y fácil de transportar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/479801/1698942728D_NQ_NP_932360-MCO69120600575_042023-O.webp"
    },
    {
        "name": "Molde Calavera Silicona Hielera",
        "price": "29,000",
        "description": "Molde de silicona en forma de calavera para hielos. Perfecto para bebidas divertidas.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/744674/17120900581696461107Imagen1.jpg"
    },
    {
        "name": "Hielera Plástica De Fácil Llenado",
        "price": "32,000",
        "description": "Hielera plástica, fácil de llenar y usar. Ideal para bebidas frías en casa.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/797995/1713830814Imagen%20de%20WhatsApp%202024-04-22%20a%20las%2016.13.04_b5c25a14.jpg"
    },
    {
        "name": "Hielera Silicona De Cubos",
        "price": "34,000",
        "description": "Hielera de silicona para hacer cubos de hielo. Resistente y fácil de limpiar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/91899/17023945821702394582HIELERA%20AZUL%201.jpeg"
    },
    {
        "name": "Hielera En Cubos 2 En 1",
        "price": "59,000",
        "description": "Hielera multifuncional 2 en 1. Diseño práctico para cubos de hielo y almacenamiento.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/53305/17030788131703078813HIELERA%202%20EN%201%201.jpeg"
    },
    {
        "name": "Hielera En Esfera",
        "price": "59,000",
        "description": "Hielera para hacer esferas de hielo. Perfecta para bebidas elegantes y presentaciones.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/581952/17042345002024-01-02%2017_25_40-Buy%20Ice%20Hockey%20Mold%2012%20Holes%20Online%20In%20Lebanon%20-%20SKU_2048-46.png"
    },
    {
        "name": "Hielera De Figuras Silicona",
        "price": "29,000",
        "description": "Hielera de silicona con moldes en varias figuras. Fácil de usar y limpiar.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/797980/1713830314Imagen%20de%20WhatsApp%202024-04-22%20a%20las%2016.12.46_599ba277.jpg"
    },
    {
        "name": "Hielera",
        "price": "29,000",
        "description": "Hielera compacta y práctica para uso diario. Ideal para mantener bebidas frías.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/723622/1710889580IMG-20240313-WA0014.jpg"
    },
    {
        "name": "Guante Ejercitador Dedos y Antebrazo",
        "price": "29,000",
        "description": "Fortalecedor de dedos y agarre. Mejora la fuerza de los dedos con 3 niveles de resistencia.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/793487/1713634295171064017981074-584x584-1.jpeg"
    },
    {
        "name": "Juanetero Separador De Dedos",
        "price": "29,000",
        "description": "Set de 2 correctores de juanetes en gel. Alivia el dolor y mejora la alineación de los dedos.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/100287/17023921321702392132photo1662762139.jpeg"
    },
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche materna eléctrico, compacto y fácil de usar. Ideal para madres en lactancia. Diseño ergonómico con múltiples niveles de succión ajustables.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Separador Dedos X 4 Colores Surtidos',
    price: '19,000',
    description: 'Set de 4 separadores de dedos en colores surtidos. Hechos de material suave y flexible, perfectos para aliviar la presión en los dedos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/13096/170239008117023900816N3fT6tjwFztQGtbGMC5eUBcneeZuGUp3xwhZTnM.jpeg'
},
{
    name: 'Kit De Ejercicio Para Dedos, Puño Y Mano',
    price: '39,000',
    description: 'Kit de ejercicio para mejorar la fuerza y destreza de los dedos, puño y mano. Incluye varios accesorios de silicona para un entrenamiento completo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/905824/1717612273WhatsApp%20Image%202024-05-14%20at%2010.55.18%20AM.jpeg'
},
{
    name: 'Dedos de práctica manicure',
    price: '49,000',
    description: 'Dedos de práctica para manicura, ideales para estudiantes y profesionales. Material resistente y reutilizable.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/765775/1712765426WhatsApp%20Image%202024-04-10%20at%2011.01.29%20AM.jpeg'
},
{
    name: 'Almohada de silicona de dedos',
    price: '39,000',
    description: 'Almohada de silicona para relajar y aliviar la tensión en los dedos. Ergonómica y cómoda, perfecta para uso diario.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/79545/170301977817030197780(6).jpg'
},
{
    name: 'Parche para dedos',
    price: '49,000',
    description: 'Parche de silicona para dedos, diseñado para aliviar el dolor y proteger contra el roce. Ideal para uso diario.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/67523/170307134917030713492%20(6).jpg'
},
{
    name: 'Tablet Celular Huskee Lcd 3g Gps 16gb',
    price: '199,000',
    description: 'Tablet celular con pantalla LCD de 7 pulgadas, doble SIM, 3G, y 16GB de almacenamiento. Perfecta para entretenimiento y productividad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/921142/1718921717Tablet%207%20pulgadas%20Doble%20Sim%20Bleytec%2003.png'
},
{
    name: 'Teclado bluetooth tablet - ipad 2 canal',
    price: '89,000',
    description: 'Teclado Bluetooth compacto para tablet y iPad. Conexión rápida y estable con doble canal.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/803916/1714542447D_NQ_NP_806346-MCO54817051079_042023-O.webp'
},
{
    name: 'Combo Teclado Bluetooth Tablet - Ipad',
    price: '79,000',
    description: 'Combo de teclado Bluetooth para tablet y iPad. Incluye mouse, ideal para un uso cómodo y eficiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/803919/1714453045D_NQ_NP_734451-MCO52287435262_112022-O.webp'
},
{
    name: 'Teclado mouse ipad tablet bluetooth',
    price: '119,000',
    description: 'Teclado y mouse Bluetooth para iPad y tablet. Diseño elegante y conexión rápida, perfecto para trabajar en cualquier lugar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/803920/1714542138D_NQ_NP_2X_821155-MCO72120876796_102023-F.webp'
},
{
    name: 'Combo teclado y mouse tablet bluetooth',
    price: '69,000',
    description: 'Combo de teclado y mouse Bluetooth para tablet. Compacto y fácil de transportar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/803918/1714453588D_NQ_NP_2X_730726-MCO54969378845_042023-F.webp'
},
{
    name: 'Tablet wifi 8 pulgadas amazon hd 2gb ram',
    price: '489,000',
    description: 'Tablet Amazon HD de 8 pulgadas con 2GB de RAM. Conectividad Wi-Fi, perfecta para entretenimiento y tareas diarias.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/352260/17018763611701876361TABLET%208%20PULGADAS%20AMAZON%20ALEXA%20HD%203GB%2032GB%2002.png'
},
{
    name: 'Soporte para celular y o tablet',
    price: '29,000',
    description: 'Soporte ajustable para celular y tablet, hecho de material resistente. Perfecto para ver contenido o realizar videollamadas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/101004/17023919911702391991GszhYQQD8MxCUJtacVhIiml1lItQ6ok2GruxnARR.jpeg'
},
{
    name: 'Tableta Para Relajación Pies Cuerpo',
    price: '39,000',
    description: 'Tabletas efervescentes para relajación de pies y cuerpo. Ingredientes orgánicos que alivian la tensión y el dolor.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/412133/1695673328Captura%20de%20pantalla%202023-09-25%20151518.png'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico portátil para una lactancia eficiente y cómoda. Fácil de usar y limpiar, ideal para madres en movimiento.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Tableta Magic Pad Dibujos De Conejito',
    price: '39,000',
    description: 'Tableta mágica con dibujos de conejito, ideal para niños. Promueve la creatividad y el aprendizaje en un formato interactivo y divertido.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/557398/1702412090conejo.webp'
},
{
    name: 'Tableta De Dibujo Mágico 6,5',
    price: '29,000',
    description: 'Tableta mágica de 6,5 pulgadas para dibujar. Fomenta la creatividad y el aprendizaje en un formato portátil y fácil de usar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/456332/1698102021Tableta%20LCD%2012%20pulgadas%20unicolor%2000.png'
},
{
    name: 'Soporte Giratorio Baseu De Cel Y Tablet',
    price: '85,000',
    description: 'Soporte giratorio para celular y tablet, ajustable y robusto. Ideal para uso en el hogar o la oficina, compatible con varios dispositivos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/75416/170302214217030221423%20(38).jpg'
},
{
    name: 'Organizador Zapatos Perchero, 4 Niveles',
    price: '69,000',
    description: 'Perchero organizador de zapatos con 4 niveles. Ahorra espacio y organiza hasta 12 pares de zapatos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/110575/1713549327WhatsApp%20Image%202024-04-19%20at%2012.36.58%20PM.jpeg'
},
{
    name: 'Organizador Zapatos Calzado 6 Niveles',
    price: '89,000',
    description: 'Organizador de zapatos de 6 niveles. Diseño compacto y fácil de montar, ideal para optimizar el espacio en tu hogar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/180112/17023045481702304548ORGANIZADOR%206%20CALZADO%201.jpg'
},
{
    name: 'Zapatero Apilable Organizador Zapatos',
    price: '89,000',
    description: 'Zapatero con capacidad para 27 pares, 10 niveles, ideal para espacios pequeños. Fácil de instalar y mover.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/634429/170716272231c51328-db34-439d-b59e-c27ad26b83ef.jpeg'
},
{
    name: 'Organizador De Zapatos 9 Niveles',
    price: '69,000',
    description: 'Organizador de zapatos con 9 niveles. Compacto, ideal para espacios pequeños y fácil de ensamblar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/658133/1708117885SongmicsSchuhregal15001500Ps.webp'
},
{
    name: 'Bolsa Para Zapatos',
    price: '45,000',
    description: 'Bolsa organizadora para zapatos, ideal para viajes. Protege y organiza tu calzado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/241715/17019755801701975580Captura%20de%20pantalla%202023-04-05%20164537.png'
},
{
    name: 'Limpiador De Zapatos Quita Manchas',
    price: '49,000',
    description: 'Crema de limpieza multifuncional para eliminar manchas y acondicionar zapatos. Suave para todo tipo de cuero.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/917527/17186507601706307717main-image-4%20(1).jpeg'
},
{
    name: 'Cubiertas Impermeables Para Zapatos',
    price: '29,000',
    description: 'Cubiertas impermeables para proteger tus zapatos de la lluvia. Reutilizables y fáciles de limpiar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/872558/1716222770Screenshot_1312.jpg'
},
{
    name: 'Secador De Zapatos Calentador Eléctrico',
    price: '69,000',
    description: 'Secador eléctrico de zapatos, elimina olores y seca rápidamente. Ideal para todo tipo de calzado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/758206/1712588807rBNaFl8Vbc2ADLubAAh2KVBMFpY879.webp'
},
{
    name: 'Organizador De Zapatos',
    price: '49,000',
    description: 'Organizador de zapatos compacto y fácil de ensamblar, ideal para maximizar el espacio en tu hogar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/138972/17023223901702322390ORGANIZADOR%20DE%20ZAPATOS.jpg'
},
{
    name: 'Botas Lluvia Impermeables Zapatos BLZ01',
    price: '33,000',
    description: 'Botas impermeables antideslizantes para lluvia, protegen eficazmente tus zapatos en condiciones húmedas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/875459/1716313473Botas%20Lluvia%20Impermeables%20Zapatos%20Protectores%20Antideslizante%20BLZ01%20Tallas%204%20(1).jpg'
},
{
    name: 'Organizador De Calzado Zapatos 30 Pares',
    price: '49,000',
    description: 'Organizador de calzado para 30 pares. Ideal para mantener ordenado y accesible tu calzado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/138571/17023224261702322426WhatsApp%20Image%202023-01-20%20at%2010.13.25%20AM.jpeg'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico para lactancia, diseñado para comodidad y eficiencia. Facilita la extracción rápida y sin dolor.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Organizador de zapatos 30 pares 10 niveles',
    price: '47,000',
    description: 'Organizador de zapatos de 10 niveles, con capacidad para 30 pares. Ideal para mantener tu calzado ordenado y accesible.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/285844/17018927391701892739zapatero.jpg%201.jpg'
},
{
    name: 'Combo impermeable lluvia + zapatos S M L',
    price: '55,000',
    description: 'Conjunto impermeable de lluvia con zapatos incluidos, disponible en tallas S, M y L. Ideal para mantenerte seco en días lluviosos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/811323/17142315071000126815.jpg'
},
{
    name: 'Secador inteligente de zapatos T11 014',
    price: '79,000',
    description: 'Secador inteligente de zapatos, modelo T11 014. Secado rápido y eficiente para mantener tus zapatos en perfecto estado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/839578/1715184525D_NQ_NP_947378-MCO75079239019_032024-O.webp'
},
{
    name: 'Gancho organizador secador de zapatos x4',
    price: '29,000',
    description: 'Set de 4 ganchos organizadores para secar y mantener tus zapatos en orden. Compactos y fáciles de usar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/734863/1711503227Gancho%20Organizador%20Secador%20De%20Zapatos%20X4.webp'
},
{
    name: 'Set de buceo careta snorkel y aletas',
    price: '209,000',
    description: 'Set completo de buceo con careta, snorkel y aletas. Ideal para aventuras submarinas, brindando comodidad y seguridad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/711530/1710448712LIPIO.jpg'
},
{
    name: 'Careta doble filtro 3M',
    price: '89,000',
    description: 'Careta de seguridad con doble filtro 3M, diseñada para protección efectiva en ambientes contaminados.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/886124/1716575296b93149bf-de1a-4b78-ac40-d58a5e19c422.jpg'
},
{
    name: 'Careta snorkel buceo vidrio templado',
    price: '79,000',
    description: 'Careta para buceo con lente de vidrio templado y ajuste cómodo. Resistente y segura para inmersiones.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/160732/1695317918WhatsApp%20Image%202023-09-07%20at%2010.51.34%20AM%20(1).jpeg'
},
{
    name: 'Micas Careta Electrónica Carel 13',
    price: '29,000',
    description: '2 micas de policarbonato para careta electrónica modelo CAREL-13, con filtro anti impacto. Garantía de 1 año.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/361976/17018756681701875668102229.jpeg'
},
{
    name: 'Careta snorkel kit buceo para niños',
    price: '59,000',
    description: 'Kit de snorkel y careta de buceo para niños. Cómodo, seguro, y perfecto para las aventuras acuáticas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/681817/1709239540SET%20DE%20BUCEO%2024025%20LIMPIO%206.jpg'
},
{
    name: 'Careta para buceo en vidrio templado',
    price: '49,000',
    description: 'Careta de buceo de un solo lente, fabricada con vidrio templado. Ofrece un ajuste cómodo y un sellado excelente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/274984/17018957951701895795NSP-2728%20limpio%202.jpg'
},
{
    name: 'Careta paintball máscara airsoft NA535',
    price: '89,000',
    description: 'Máscara protectora para paintball y airsoft, modelo NA535. Robusta y segura para deportes extremos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/77838/17030217301703021730Careta%20Paintball%20M%C3%A1scara%20Airsoft%20Motocross%20Protecci%C3%B3n%20CP01-DFM%201.jpg'
},
{
    name: 'Careta fotosensible con diseño',
    price: '99,000',
    description: 'Careta de soldadura fotosensible con diseño exclusivo. Alta protección y comodidad en trabajos de soldadura.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/395311/1702929679WhatsApp%20Image%202023-12-12%20at%207.45.16%20AM.jpeg'
},
{
    name: 'Asador Parrilla BBQ Portátil',
    price: '69,000',
    description: 'Parrilla BBQ portátil de acero, ideal para asados al aire libre. Fácil de transportar y duradera.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/307712/1701890781170189078196.jpg'
},
{
    name: 'Horno Asador De Pinchos Vertical X8',
    price: '179,000',
    description: 'Horno asador vertical con capacidad para 8 pinchos. Perfecto para asar diferentes tipos de carnes de manera uniforme.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/828791/1714775623Logo%20marca%20personal%20hipotecas%20abogado%20moderno%20limpio%20verde%20(8).png'
},
{
    name: 'Barril Asador Mediano EC',
    price: '519,000',
    description: 'Asador tipo barril mediano, hecho en acero inoxidable. Incluye 12 ganchos, termómetro y más accesorios. Garantía de 1 año.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/343038/17018793201701879320barril%20mediano%20linea%20economica.jpg'
},
{
    name: 'Barril Asador Mini Línea Premium',
    price: '479,000',
    description: 'Mini asador tipo barril, acero inoxidable con detalles en madera. Incluye 8 ganchos y otros accesorios. Garantía de 5 años.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/343045/17018793191701879319barril%20premium%20%20mini.jpg'
},
{
    name: 'Asador Tipo Barril Pequeño En Acero Inox',
    price: '599,000',
    description: 'Asador barril pequeño de acero inoxidable, perfecto para espacios reducidos. Incluye 10 ganchos y parrilla abatible. Garantía de 5 años.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/395371/17018714011701871401414F98D8-9864-4B8E-91A7-078BAA1234C1.png'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche materna eléctrico con diseño portátil y fácil de usar. Incluye botellas de almacenamiento.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Mini Asador Parrilla De Carbón Portátil',
    price: '89,000',
    description: 'Asador portátil para barbacoa. Superficie de cocción espaciosa, altura ajustable y material duradero.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/792188/1713564408SL31606%201.jpeg'
},
{
    name: 'Parrilla Carbón Asador Portátil FK23D-174',
    price: '149,000',
    description: 'Parrilla de acero inoxidable, portátil y plegable, ideal para camping y picnics. Incluye 2 superficies de parrilla.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/606926/1711055131FK23D-174.3%20(1).jpg'
},
{
    name: 'Máquina Mini Donas 3 Puestos',
    price: '49,000',
    description: 'Mini máquina para hacer donas con bandeja desmontable, fácil limpieza y diseño compacto.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/654768/1708026009Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-02-15T143834.688.png'
},
{
    name: 'Mini Máquina De Donas',
    price: '79,000',
    description: 'Máquina para hacer 7 mini donas en minutos. Superficie antiadherente, diseño compacto y fácil de usar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/483946/1699116945DONAS2.jpeg'
},
{
    name: 'Máquina De Donas 7 Puestos',
    price: '79,000',
    description: 'Máquina para hacer 7 mini donas. Ideal para hacer diferentes tipos de donas y fácil de limpiar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/548955/1701970021mini%20donas.jpg'
},
{
    name: 'Molde Para Donas',
    price: '29,000',
    description: 'Molde para hacer donas caseras, fácil de usar y limpiar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/815946/1714444479molde%20para%20donas.webp'
},
{
    name: 'Super Promo Mini Waflera Antiadherente',
    price: '49,000',
    description: 'Mini waflera con superficie antiadherente, fácil de limpiar y almacenar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/51574/17030804141703080414W5.jpg'
},
{
    name: 'Waflera 1 Puesto Forma Corazón',
    price: '49,000',
    description: 'Waflera con forma de corazón. Superficie antiadherente y fácil de usar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/678934/17091465701.jpg'
},
{
    name: 'Waflera Manual Trébol',
    price: '65,000',
    description: 'Waflera manual con diseño de trébol, calentamiento rápido y superficie antiadherente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/904561/1717476980WhatsApp%20Image%202024-06-03%20at%2010.58.48%20PM-16.jpeg'
},
{
    name: 'Waflera Con Diseño Sokany SK-128',
    price: '79,000',
    description: 'Waflera con diseño moderno, superficie antiadherente y fácil de limpiar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/628226/1706810947Captura%20de%20Pantalla%202024-02-01%20a%20la(s)%201.08.18%20p.m..png'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche eléctrico, cómodo y eficiente. Facilita la extracción de leche materna de manera rápida y sin esfuerzo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Sandwichera Waflera Donera 3 En 1',
    price: '139,000',
    description: 'Máquina 3 en 1 para hacer sándwiches, gofres y donuts con placas antiadherentes y fáciles de cambiar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/862921/1715790940Sandwichera-Waflera-Y-Donera-Antiadherente-Maquina-3-En-1-00.png'
},
{
    name: 'Sandwichera Mediana Sokany 110v/220v',
    price: '65,000',
    description: 'Sandwichera Sokany compacta y fácil de usar con placas antiadherentes. Ideal para preparar sándwiches dorados en minutos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/708261/1710368949G8iNH99dcd9d66e574d68ae68a186c97157dc6.jpg'
},
{
    name: 'Dispensador De Jabón Con Esponja Kp228',
    price: '19,000',
    description: 'Dispensador de jabón con esponja incluida para facilitar la limpieza en la cocina o baño.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/593416/1705086477KP231-1.jpg'
},
{
    name: 'Dispensador de Jabón',
    price: '29,000',
    description: 'Dispensador de jabón moderno y práctico para baño o cocina.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/833943/172055910386.jpg'
},
{
    name: 'Dispensador Agua Eléctrico Recargable',
    price: '39,000',
    description: 'Dispensador de agua eléctrico con batería recargable. Compatible con diversos tamaños de botellas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/285826/17018927401701892740dispensador%20botellon.jpg'
},
{
    name: 'Botella Spray Aceite 100 Ml',
    price: '29,000',
    description: 'Botella spray para aceite de cocina, fabricada en vidrio y acero inoxidable. Ideal para una dosificación precisa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/89197/17030149441703014944D_NQ_NP_2X_666100-MCO49366606662_032022-F.jpeg'
},
{
    name: 'Dispensador de Crema Dental con Porta Cepillos',
    price: '29,000',
    description: 'Dispensador automático de crema dental con soporte para cepillos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/289147/17018924651701892465dispensador-de-crema-dental-automatico-y-cepillo-de-diente-D_NQ_NP_877098-MCO29421394733_022019-F%20(1).jpg'
},
{
    name: 'Dispensador - Organizador De Huevos',
    price: '29,000',
    description: 'Organizador de huevos compacto y funcional para almacenamiento seguro en el refrigerador.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/732646/1711433227D5BB71F6-40B9-429E-8BD3-C1020DC786C8.jpeg'
},
{
    name: 'Dispensador De Agua 3L Botella Plegable 08106',
    price: '29,000',
    description: 'Dispensador de agua plegable de 3 litros, ideal para camping y actividades al aire libre.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/73391/17030244861703024486Dispensador%20De%20Agua%203L%20Botella%20Plegable%20Contenedor%20Camping%2008106%205.jpg'
},
{
    name: 'Cepillo Dispensador de Jabón Líquido',
    price: '29,000',
    description: 'Cepillo con dispensador de jabón para baño, ideal para masajear y estimular el crecimiento del cabello.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/546661/1701878124RT.jpg'
},
{
    name: 'Cepillo Dispensador De Jabón',
    price: '29,000',
    description: 'Cepillo con dispensador de jabón integrado para una limpieza eficiente y cómoda.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/31509/17030822231703082223D_NQ_NP_609679-MCO47330103523_092021-O.jpeg'
},
{
    name: 'Cepillo Exfoliante Con Dispensador',
    price: '32,000',
    description: 'Cepillo exfoliante con dispensador para una limpieza profunda y relajante de la piel.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/307425/17018907971701890797s-l1600.jpg'
},
{
    name: 'Lápiz Para Decorar Café Latte',
    price: '32,000',
    description: 'Lápiz eléctrico para crear arte en latte, ideal para baristas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/245238/1701909242170190924219.jpeg'
},
{
    name: 'Trapeador Mágico',
    price: '49,000',
    description: 'Trapeador auto exprimible con sistema giratorio para una limpieza eficiente y sin contacto con las cerdas sucias.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/768706/1712850428D_NQ_NP_2X_668875-CBT75405003396_042024-F.webp'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico de leche materna para una extracción rápida y cómoda. Ideal para madres lactantes que necesitan extraer leche de manera eficiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Trapero Con Balde Plegable',
    price: '79,000',
    description: 'Trapero con balde plegable, diseño compacto y ergonómico. Incluye trapeador de microfibra, ideal para una limpieza efectiva de diferentes tipos de pisos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/925346/171934626461sqk4NNBsL._AC_SX569_.jpg'
},
{
    name: 'Trapero Giratorio Spin Pq',
    price: '59,000',
    description: 'Trapero giratorio 360 con mango extensible. Incluye cabezal de trapero suave y es ideal para limpiar ventanas y suelos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/903369/1717259336traperos%20colores.webp'
},
{
    name: 'Mopa De Lavado De Coche Con Mango Telescópico',
    price: '32,000',
    description: 'Mopa de microfibra con mango telescópico para lavar coches y superficies. Suave, absorbente y ajustable para alcanzar áreas difíciles.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/940462/1720203709photo_2024-07-05_13-19-49.jpg'
},
{
    name: 'Repuesto De Mopa Trapero Mágico',
    price: '29,000',
    description: 'Repuesto para trapero mágico. Ideal para reemplazar el cabezal de tu trapeador y mantener la eficiencia de limpieza.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/918614/1718741007MOPA%203.jpg'
},
{
    name: 'Bolsa De Filtro Atrapa Pelusa Para Lavado',
    price: '19,000',
    description: 'Bolsa de filtro para atrapar pelusa en la lavadora. Mantiene tu ropa libre de pelusas y protege el filtro de la lavadora.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/784782/1713383676Captura%20de%20pantalla%202024-04-17%20145154.png'
},
{
    name: 'Trapeadora Robot D',
    price: '119,000',
    description: 'Trapeadora robot que limpia automáticamente. Ideal para mantener tus pisos limpios sin esfuerzo adicional.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/717286/171077165617018800781701880078Untitled%20-%202.png'
},
{
    name: 'Trapero Triangular',
    price: '69,000',
    description: 'Trapero triangular para una limpieza eficiente en ángulos y esquinas. Ideal para todo tipo de superficies.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/712367/17104737221.jpg'
},
{
    name: 'Mini Trapero Limpia Vidrios Portátil',
    price: '33,000',
    description: 'Mini trapero absorbente y auto escurrible, ideal para limpiar esquinas y bordes difíciles de alcanzar. Compacto y fácil de usar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/642844/1707489991Mini%20Trapero01.jpg'
},
{
    name: 'Estante Organizador De Libros',
    price: '69,000',
    description: 'Estante organizador con 9 espacios multifuncionales. Ideal para libros, zapatos y más, con un diseño adaptable a cualquier habitación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1032852/1722458583190a761fc53-variedades_tv_calle_14-mhtlwoxwd5-6tuejmeinbt.png'
},
{
            "name": "Extractor De Leche Materna Eléctrico",
            "price": "89,000",
            "description": "Extractor de leche materna eléctrico eficiente, ideal para la extracción rápida y cómoda. Incluye múltiples ajustes de velocidad y succión. Perfecto para madres lactantes.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg"
        },
        {
            "name": "Panel De Luz Para Libros Luz Nocturna",
            "price": "49,000",
            "description": "Panel de luz compacta para lectura nocturna, con material ABS y distribución uniforme de la luz. Ideal para usar en cualquier lugar con poca iluminación.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/1006743/1721766960panel%20de%20luz%20para%20lectura.png"
        },
        {
            "name": "Picador De Alimentos Eléctrico",
            "price": "49,000",
            "description": "Picador multifunción eléctrico: corta verduras, pica carne y tiene cepillo de limpieza. Hecho de ABS+PP+PC+acero inoxidable, fácil de usar y limpiar.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/373959/170187379317018737938000503101196_441728112022160315.jpg"
        },
        {
            "name": "Picador De Verdura",
            "price": "55,000",
            "description": "Picador multifuncional con 7 cuchillas intercambiables. Ideal para triturar, cortar y rebanar verduras y frutas. Incluye un recipiente de 1.2 L.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/831146/1714849544Picador%20Rallador%20De%20Verduras%2016%20En%201%20Cortador.webp"
        },
        {
            "name": "Picador Multifuncional Picatodo Brava",
            "price": "49,000",
            "description": "Picador con diseño seguro y ajustable. Hoja de acero inoxidable y ventosas antideslizantes para un uso cómodo. Ideal para una preparación rápida y segura de alimentos.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/557426/170241353016.png"
        },
        {
            "name": "Picador Triturador Ajos",
            "price": "32,000",
            "description": "Picador de ajos compacto y eficiente. Ideal para triturar ajos rápidamente. Diseño práctico para uso en cocina.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/514580/1715797349il_794xN.4823857258_6gwf.webp"
        },
        {
            "name": "Picador De Papas Y Verduras",
            "price": "49,000",
            "description": "Picador para papas y verduras. Diseñado para cortar de manera uniforme y eficiente. Ideal para uso en la cocina.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/640981/1707411918cortadorDePapas.png"
        },
        {
            "name": "Esterilizador Cepillo Dientes",
            "price": "49,000",
            "description": "Esterilizador UV para cepillos de dientes. Elimina gérmenes con una tasa de esterilización del 99.99%. Incluye carga USB y soporte para cepillo.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/1050258/1723042005D_NQ_NP_2X_928978-MLU70119371214_062023-F.webp"
        },
        {
            "name": "Cepillo Vapor Mascota Expandible",
            "price": "33,000",
            "description": "Cepillo de vapor para mascotas que elimina pelo y proporciona masaje. Recargable por USB, adecuado para gatos y perros.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/1041882/1722725584237C386A-8DC7-400E-8AEF-49DBEA1729DC.jpg"
        },
        {
            "name": "Cepillo Giratorio En Limpieza Profunda",
            "price": "53,000",
            "description": "Cepillo eléctrico rotativo con tres cabezales intercambiables. Ideal para limpiar rincones difíciles y resistente al agua. Incluye cargador USB.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/374494/17018737681701873768D_NQ_NP_988772-MCO54981343941_052023-O%20(1).jpeg"
        },
        {
            "name": "Rodilleras Con Calefacción Terapéuticas",
            "price": "55,000",
            "description": "Rodilleras eléctricas con calefacción para aliviar dolor en rodillas y músculos. Incluye correas ajustables y control de temperatura.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/1031781/1722446790rodillera%20termica%202.png"
        },
        {
            "name": "Rodillera Deportiva Ajustable Negro",
            "price": "29,000",
            "description": "Rodillera deportiva ajustable en color negro. Ideal para soporte y protección durante actividades físicas.",
            "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/980198/1721130636RODILLERA%206912%204_11zon.jpg"
        },
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche materna eléctrico con diseño eficiente para un bombeo cómodo y eficaz. Ideal para madres lactantes que buscan una solución práctica.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Rodillera Pcs Deportiva Ajustable',
    price: '29,000',
    description: 'Rodillera deportiva ajustable para soporte y protección durante actividades físicas. Diseñada para comodidad y soporte óptimo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/999627/1721637993rodillera.jpg'
},
{
    name: 'Rodillera Soporte Rodilla Menisco Rotula',
    price: '45,000',
    description: 'Soporte de rodilla para menisco y rótula. Ideal para alivio de dolor y soporte adicional durante la recuperación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/966616/1720728163Soporte%20de%20Rodilla01.jpg'
},
{
    name: 'Mini Consola',
    price: '59,000',
    description: 'Mini consola portátil con juegos integrados. Compacta y fácil de usar para entretenimiento en cualquier lugar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1016222/1722007635WhatsApp%20Image%202024-07-26%20at%2010.23.13%20AM.jpeg'
},
{
    name: 'Consola De Juegos Retro Portátil X Repr',
    price: '159,000',
    description: 'Consola portátil retro con pantalla HD de 3.5". Incluye 18,000+ juegos, almacenamiento expandible y batería de 2000mAh.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/926591/1719427767WhatsApp%20Image%202024-06-24%20at%204.09.35%20PM.jpeg'
},
{
    name: 'Mini Consola K Juegos Retro',
    price: '115,000',
    description: 'Mini consola retro con más de 10,000 juegos preinstalados. Conexión HDMI para una experiencia de juego en alta definición.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/910945/1718031472D_NQ_NP_902003-MLU75151309861_032024-O.webp'
},
{
    name: 'Consola De Mano Con Retro Juegos Video',
    price: '79,000',
    description: 'Consola de mano con 520 juegos integrados. Incluye controlador de doble jugador y salida de video AV para conectarse al televisor.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/839287/1715178339control%20de%20video%20juegos.jpg'
},
{
    name: 'Consola Retro Con Dos Mandos',
    price: '219,000',
    description: 'Consola retro con dos mandos y soporte HDMI 1080p. Ideal para juegos de pelea y diversión en alta definición.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/811801/1714241983CONSOLA%20RETRO.jpg'
},
{
    name: 'Consola Gs Juegos Bits',
    price: '79,000',
    description: 'Consola con juegos retro de bits. Compacta y ideal para revivir clásicos de videojuegos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/804167/171445413700.webp'
},
{
    name: 'Consola Emulador Gameboy Psneogeo Rs',
    price: '349,000',
    description: 'Consola portátil con pantalla HD de 3.5" y más de 15,000 juegos. Incluye 20 emuladores y batería de 3500mAh.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/698993/1709928795Consola%20de%20Juegos%20Portatil%20R35S%2001.png'
},
{
    name: 'Freidora De Aire Digital',
    price: '249,000',
    description: 'Freidora de aire digital de 4.5L con pantalla táctil. Cocina sin aceite, ideal para preparar comidas saludables.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/767674/1712797184freidora%20de%20aire%20digital.jpeg'
},
{
    name: 'Freidora De Aire Digital Oster Litros',
    price: '369,000',
    description: 'Freidora de aire Oster de 4 litros con control de temperatura y temporizador. Cocina hasta un 20% más rápido con 99.5% menos aceite.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/695941/17098387214L%20DIGITAL.jpg'
},
{
    name: 'Freidora Manual Litros',
    price: '249,000',
    description: 'Freidora de aire con capacidad de 6L, sin necesidad de aceite. Incluye control de temperatura y temporizador, ideal para una cocción saludable.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/539252/1701472592WhatsApp%20Image%202023-12-01%20at%206.11.12%20PM%20(1).jpeg'
},
{
    name: 'Freidora de aire L',
    price: '355,000',
    description: 'Freidora de aire digital de 5.5L con control de temperatura y temporizador ajustable. Cocina saludable con hasta 80% menos grasa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1021027/1722203567IMG-20240727-WA0063.jpg'
},
{
    name: 'Molde Para Freidora Air Fryer Silicona R',
    price: '29,000',
    description: 'Molde de silicona para freidora de aire, ideal para cocinar alimentos sin pegajosos. Facilita la limpieza y mantenimiento.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/979352/1721088931WhatsApp%20Image%202024-07-15%20at%209.02.28%20AM.jpeg'
},
{
    name: 'Removedor Quita Callos Eléctrico',
    price: '45,000',
    description: 'Removedor de callos eléctrico con repuestos incluidos, alimentado por USB. Ideal para eliminar callos y dejar los pies suaves.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/871549/1716168593D_NQ_NP_971791-MLU71215358694_082023-O.webp'
},
{
    name: 'Removedor De Callos Recargable Con Una',
    price: '39,000',
    description: 'Removedor recargable de callos, eficiente y fácil de usar. Ideal para mantener los pies suaves y sin callos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/775523/171314124818b53a8bebe-variedades_tv_calle_14-pkxb2fu1oqn-lrv4zx7ujv%20(1).png'
},
{
    name: 'Pulidor De Callos',
    price: '45,000',
    description: 'Pulidor eléctrico para callos con doble cabezal. Elimina piel muerta y dura, ideal para el cuidado del talón y pies.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713918/1710531528D_NQ_NP_2X_789844-MCO52875268839_122022-F.webp'
},
{
    name: 'Escurridor De Loza 65 Cm',
    price: '69,000',
    description: 'Escurridor multifuncional para platos y utensilios. Diseñado para mantener la cocina ordenada y seca.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1033256/1722465624ESCURRIDOR%20DE%20LOZA%2065%20CM.jpg'
},
{
    name: 'Escurridor De Platos Con Almacenamiento De Puerta De Armario',
    price: '165,000',
    description: 'Escurridor de platos con almacenamiento inteligente, hecho de acero resistente. Ideal para organizar utensilios y mantener la encimera limpia.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/838846/17151423691.png'
},
{
    name: 'Escurridor De Platos Plegable Plástico',
    price: '39,000',
    description: 'Escurridor plegable de platos en plástico, fácil de guardar y limpiar. Ideal para espacios reducidos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/747800/1712184671WhatsApp%20Image%202024-04-03%20at%205.44.53%20PM.jpeg'
},
{
    name: 'Aspersor Piscina Juguete Rociador',
    price: '99,000',
    description: 'Aspersor para piscina en forma de juguete, ideal para el entretenimiento en el agua. Ofrece diversión y frescura durante el verano.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/867790/17159726181.1.jpg'
},
{
    name: 'Piscina Inflable Hongo Infantil',
    price: '99,000',
    description: 'Piscina inflable infantil con forma de hongo, ideal para el verano y para disfrutar en el jardín.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/564906/17027493881.jpg'
},
{
    name: 'Piscina Rígida Acuario',
    price: '69,000',
    description: 'Piscina rígida tipo acuario, resistente y duradera. Ideal para el juego al aire libre y refrescarse en días calurosos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/383243/17018727251701872725woodland-play-center.jpg'
},
{
    name: 'Piscina Con Aro Y Pelota Marca Bes',
    price: '69,000',
    description: 'Piscina con aro y pelota, perfecta para divertirse en el agua. Ideal para niños en días calurosos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/383150/1701872746170187274651124.jpeg'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche materna eléctrico, eficiente y fácil de usar para una extracción cómoda. Ideal para mamás lactantes.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Piscina Con Aro Y Pelota Marca Bes',
    price: '69,000',
    description: 'Piscina inflable con aro y pelota. Ideal para el verano, fácil de inflar y usar en el jardín.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/383150/1701872746170187274651124.jpeg'
},
{
    name: 'Piscina Inflable Acuario',
    price: '149,000',
    description: 'Piscina inflable Acuario de PVC con válvulas de seguridad. Dimensiones: 2.62m x 1.57m x 46cm. Recomendado para mayores de 3 años.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/382592/1701872807170187280754118.jpeg'
},
{
    name: 'Piscina Plegable Bañera Portátil Para Perros',
    price: '229,000',
    description: 'Piscina plegable XXL para niños y mascotas, 160cm diámetro x 30cm profundidad. Antideslizante y fácil de drenar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/138329/17018908071701890807OsqrmdNj9Mad32wo69RWngpTiFV5laVwzeucD4XI.png'
},
{
    name: 'Almohada Ortopédica',
    price: '59,000',
    description: 'Almohada ortopédica de viaje para soporte del cuello en cualquier lugar. Ajustable para mayor comodidad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1077443/1723648358WhatsApp%20Image%202024-08-14%20at%2010.10.42%20AM.jpeg'
},
{
    name: 'Almohada Bebé Para Prevenir Cabeza Plana',
    price: '36,000',
    description: 'Almohada de base plana para bebés, de algodón y espuma viscoelástica. Reduce la presión del cuello y asegura comodidad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/946090/1720281035almohada%20cabeza%20bebe%203.JPG'
},
{
    name: 'Almohada Vertical Memory Foam Para Niños',
    price: '49,000',
    description: 'Almohada vertical de espuma viscoelástica para niños. Ofrece soporte ergonómico y ajustable para un sueño cómodo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914893/1718324099WhatsApp%20Image%202024-06-13%20at%207.03.59%20PM%20(1).jpeg'
},
{
    name: 'Almohada Inflable Para Cuello',
    price: '29,000',
    description: 'Almohada inflable para cuello, ideal para viajes. Fabricada en PVC y terciopelo, compacta y fácil de transportar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/702130/17101691531%20Almohada%20Port%C3%A1til%20Multiusos%20Inflable%20Viajera%2068675.jpg'
},
{
    name: 'Almohada Portátil Multiusos',
    price: '29,000',
    description: 'Almohada inflable multiusos, ideal para viajes y uso doméstico. Ajustable y fácil de inflar y desinflar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/702110/17101686442%20-%20Almohada%20Inflable%20Intex%20Cama.jpg'
},
{
    name: 'Almohada Ortopédica Premium Quality',
    price: '59,000',
    description: 'Almohada ortopédica premium, de fibra de poliéster. Tamaño: 74cm x 48cm x 12-13cm.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/655374/1708030481Captura%20de%20Pantalla%202024-02-15%20a%20la(s)%203.51.17%20p.%C2%A0m..png'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico para leche materna, fácil de usar y eficaz para madres lactantes. Diseño ergonómico que garantiza comodidad y eficiencia. Ideal para extraer leche de manera rápida y conveniente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Almohada Multifuncional',
    price: '39,000',
    description: 'Almohada de memoria para un sueño reparador, con material hipoalergénico para evitar alergias. Ideal para descanso diario, proporcionando gran calidad y comodidad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/599949/1705439835ALMOHADA%20MULTIFUNCIONAL.webp'
},
{
    name: 'Almohada Alimentar Tela Conejo',
    price: '59,000',
    description: 'Cojín para apoyo al dar pecho y ejercicios de cuello y espalda del bebé. Hecho por madres cabeza de hogar, con doble forro y relleno de algodón siliconado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/521386/17007624901.webp'
},
{
    name: 'Cojín Almohada Para Silla En Silicona',
    price: '43,000',
    description: 'Cojín de silicona para silla, flexible y transpirable. Proporciona soporte para la espalda, mejora la postura y absorbe puntos de presión. Funda lavable y resistente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/423623/1696352418COJIN%20PARA%20SILLA%204.JPG'
},
{
    name: 'Almohada Cuello Para Mascotas',
    price: '45,000',
    description: 'Almohada en forma de U para mascotas, brinda comodidad y seguridad. Ideal para casa y viajes, se adapta a razas pequeñas y grandes.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/900171/1717091107WhatsApp%20Image%202024-05-30%20at%2012.31.29%20PM.jpeg'
},
{
    name: 'Almohada Viajera Inflable Kit',
    price: '43,000',
    description: 'Almohada inflable en U con bomba incorporada, fácil de inflar y almacenar. Ideal para viajes, alivia el dolor de cuello y hombros con diseño ergonómico.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/875354/1716312066gsc_127848944_4993301_2.avif'
},
{
    name: 'Almohada De Viaje Masajeadora',
    price: '75,000',
    description: 'Masajeador de cuello con USB, alivia dolor con calor y masaje profundo. Diseño ergonómico y ajustable, ideal para viajar y aliviar el estrés.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/703763/1710198190Captura%20de%20pantalla%202024-03-11%20173811.png'
},
{
    name: 'Amplificador De Sonido Para Oído Sp',
    price: '39,000',
    description: 'Amplificador de sonido compacto con hasta 40 dB de amplificación. Incluye batería, tapones para los oídos y es ideal para problemas auditivos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1016137/1722007120Amplificador%20de%20sonido%20para%20oido%20audifono%20inalambrico%20a%20pila%20FK23D-27%20.jpeg'
},
{
    name: 'Limpiador De Oídos Con Cámara Recargable',
    price: '85,000',
    description: 'Limpiador de oídos con cámara HD 1080P y 6 luces LED. Compatible con Android e iOS, permite ver y grabar el interior del oído para una limpieza precisa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1049520/1722982644Irrigador-de-oidos-CAMARA-CORPORAL-FK23B-34-16-1-680x680.webp'
},
{
    name: 'Set Para El Cuidado De Los Oídos Limpieza',
    price: '29,000',
    description: 'Juego de 8 piezas para limpieza de oídos, incluye herramientas de acero inoxidable para una limpieza efectiva y cómoda. Ideal para prevenir infecciones y mantener el oído saludable.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/682352/1709258231Set%20Para%20El%20Cuidado%20De%20Los%20O%C3%ADdos%20Cuidado%20Limpieza%208%20Piezas.webp'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico eficiente para extraer leche materna. Ideal para madres que desean almacenar y alimentar a su bebé con leche materna de forma cómoda y práctica.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Limpiador Facial Extractor De Espinilla',
    price: '39,000',
    description: 'Aspiradora para espinillas con cinco niveles de succión ajustables. Incluye cabezal de microdermoabrasión para exfoliar y rejuvenecer la piel.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/722566/1710872622extractor%20de%20espinillas%207.jpg'
},
{
    name: 'Limpiador Facial De Espinillas',
    price: '42,000',
    description: 'Limpiador facial de ultra microburbujas que usa vacío y burbujas finas para eliminar impurezas y nutrir la piel. Ideal para cualquier tipo de piel.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/794346/1713728401T11-051%201.jpeg'
},
{
    name: 'Extractor De Espinillas Acne Piezas',
    price: '29,000',
    description: 'Extractor manual de espinillas con diversas piezas para una limpieza efectiva de impurezas faciales.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/743604/17120701751.jpg'
},
{
    name: 'Maquina Lavadora De Brochas De Maquillaje',
    price: '39,000',
    description: 'Máquina automática para limpiar brochas de maquillaje, con motor de 7000 rpm para una limpieza profunda y eficiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1045713/1722898294WhatsApp%20Image%202024-08-01%20at%204.22.47%20PM.jpeg'
},
{
    name: 'Limpiador De Brochas Maquillaje MBCH',
    price: '35,000',
    description: 'Limpiador de brochas de maquillaje para una limpieza rápida y eficaz.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/915614/1718393006Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-06-14T140712.172.png'
},
{
    name: 'Brochas Maquillaje Bambú Eco',
    price: '42,000',
    description: 'Juego de brochas de maquillaje eco-friendly hechas de bambú, ideales para un maquillaje preciso y sostenible.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/833065/171501098811%20Brochas%20Maquillaje%20Bamb%C3%BA%20Eco.webp'
},
{
    name: 'Organizador De Ollas Niveles',
    price: '59,000',
    description: 'Organizador de ollas con 8 niveles ajustables para almacenar ollas, sartenes y otros utensilios de cocina de manera ordenada.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/915783/171840091683742243-1d2a-4256-817e-13a616f13201.jpg'
},
{
    name: 'Set De Ollas En Mármol De 7 Piezas Tokio',
    price: '374,000',
    description: 'Set de ollas de mármol antiadherente de 7 piezas, ideal para una cocina eficiente con una distribución uniforme del calor.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/905935/17176167241717605791WhatsApp%20Image%202024-06-05%20at%2011.40.38%20AM.jpeg'
},
{
    name: 'Olla Express A Presión En Acero L',
    price: '258,000',
    description: 'Olla a presión de acero inoxidable, ideal para cocinar de manera rápida y eficiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/905607/171760318335a42c3b-9ff9-4048-90e1-2edf61b6363a.jpeg'
},
{
    name: 'Juego De Ollas 10 Piezas Tornado',
    price: '395,000',
    description: 'Juego de ollas de 10 piezas, duraderas y eficientes para una experiencia de cocina versátil.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/872770/1716236120WhatsApp%20Image%202024-05-20%20at%203.05.51%20PM.jpeg'
},
{
    name: 'Audífonos Tipo AirPods Con Pantalla',
    price: '99,000',
    description: 'Audífonos Bluetooth tipo AirPods con pantalla táctil, cancelación de ruido y estuche de carga con enganche para correa.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1025265/17222835874979283623979101765.jpg'
},
{
    name: 'Audífonos Bluetooth Con Pantalla Digital',
    price: '99,000',
    description: 'Audífonos Bluetooth con pantalla digital, cancelación de ruido adaptativa, y control de audio avanzado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/905948/1717617023AUDIFOONO%20PANTALLA.jpg'
},
{
    name: 'Gorro De Gel Para Dolor De Migraña',
    price: '39,000',
    description: 'Gorro de gel para aliviar el dolor de migraña y cefaleas, con un diseño cómodo y efectivo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/999081/1721602539WhatsApp%20Image%202024-07-21%20at%205.54.41%20PM%20(1).jpeg'
},
{
    name: 'Carpa Para Niños Con Peluche',
    price: '55,000',
    description: 'Carpa para niños con almohada integrada, ideal para juegos y momentos de descanso. Plegable y suave.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1048912/1722977182carpas.jpg'
},
{
    name: 'Carpa Para Mascotas',
    price: '55,000',
    description: 'Carpa cómoda para mascotas, perfecta para ofrecer un espacio acogedor tanto en casa como en exteriores.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/981800/1721149913Had8aff36b6a94e93923438a2fdeebb55C.png'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche materna eléctrico, eficaz y cómodo. Ideal para madres lactantes. Incluye todos los accesorios necesarios para un uso sencillo y eficiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Carpa Toldo 2x2 Plegable Reforzado Impermeable',
    price: '245,000',
    description: 'Carpa plegable 2x2 m, impermeable y reforzada, ideal para eventos al aire libre. Fácil de montar y desmontar, estructura de acero con 4 niveles de altura.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/584782/1704417191Carpa%20Toldo%202x2_3x3%20Plegable%20Reforzado%20Impermeable%20Eventos%20Azul%201.jpeg'
},
{
    name: 'Pijama Protector Carpa Para Carro',
    price: '139,000',
    description: 'Protector para automóvil impermeable, resistente al sol y a la lluvia. Hecho de polietileno y acetato de vinilo, con material multicapa para máxima protección.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/276552/170189567917018956798Jqv4ox86uW41tpDIjyZB7YLeohRZkYnIpkqYKzG.jpg'
},
{
    name: 'Carpa Impermeable De Moto',
    price: '49,000',
    description: 'Carpa impermeable para motos, ajustable y sin costuras para evitar filtraciones. Disponible en talla S-M y L, incluye tula para guardar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/318388/170188233917018823392.jpg'
},
{
    name: 'Carpa Camuflada Para Personas',
    price: '79,000',
    description: 'Carpa camuflada para 2 personas, resistente al agua y al sol. Incluye parantes, estacas y bolsa de transporte. Medidas: 200x120x100 cm.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1072378/1723571756CAMU.jpg'
},
{
    name: 'Carpa Camping Persona Automatica Mr',
    price: '199,000',
    description: 'Carpa automática para 5 personas, se arma en un minuto. Tela resistente al agua y buena ventilación. Incluye estacas, cuerda corta vientos y estuche de transporte.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1012416/1721920592Carpa%20Camping%205%20Personas%20Autom%C3%A1tica%20Arma%20En%201%20Minuto%20MR-16%201.jpg'
},
{
    name: 'Ventilador Enfriador Humidificador Difusor',
    price: '69,000',
    description: 'Ventilador multifuncional con atomizadores y 3 niveles de velocidad. También funciona como humidificador y máquina de aromaterapia. Ajuste de dirección del viento y temporizador.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1048159/1722967746WhatsApp%20Image%202024-08-05%20at%206.11.36%20PM%20(1).jpeg'
},
{
    name: 'Ventilador Humificador Doble Recargable',
    price: '75,000',
    description: 'Ventilador de aire acondicionado portátil con diseño de pulverización doble. Incluye luces LED y tanque de agua grande. Alimentado por USB.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/946685/1720286339VENTILADOR%20DOBLE%20HUMIDIFICADOR%202.jpg'
},
{
    name: 'Humidificador Difusor De Aromas Hongo Am',
    price: '75,000',
    description: 'Humidificador difusor de aromas en forma de hongo. Ideal para aromatizar y humidificar el ambiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/932135/1720023920WhatsApp%20Image%202024-06-28%20at%203.49.25%20PM%20(1).jpeg'
},
{
    name: 'Humidificador Volcan',
    price: '65,000',
    description: 'Humidificador con diseño volcán, ideal para mejorar la calidad del aire. Compacto y funcional.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/918237/171872858361CPpz8mdWL._AC_SX679_.jpg'
},
{
    name: 'Humidificador Astronauta',
    price: '55,000',
    description: 'Humidificador en forma de astronauta, perfecto para añadir humedad al ambiente y decorar.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/917857/1718669638Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-06-11T163815.527.png'
},
{
    name: 'Humidificador Difusor Aromaterapia',
    price: '49,000',
    description: 'Humidificador y difusor de aceites esenciales. Añade humedad al aire y dispersa aromas para mejorar el ambiente y reducir estrés. Multifuncional y disponible en varios diseños.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/913728/1718294093DI..png'
},
{
    name: 'Humidificador Solar Para Carro',
    price: '59,000',
    description: 'Difusor y ambientador solar para carro con diseño giratorio. Ideal para mantener un aroma fresco en tu vehículo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/895789/1716935714ambientador%20de%20carro.jpg'
},
{
    name: 'Humidificador Difusor',
    price: '42,000',
    description: 'Difusor y humidificador compacto, ideal para mejorar la calidad del aire y agregar humedad al ambiente.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/810300/1714164965ZR11519-1.jpeg'
},
{
    name: 'Humidificador Antigravedad Reloj Ml',
    price: '99,000',
    description: 'Humidificador con diseño antigravedad y forma de reloj. Añade humedad al aire de manera innovadora y elegante.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/800576/1713910598humidificador_esencias-1-7526aec806ddb2121117099325536481-1024-1024.png'
},
{
    name: 'Lampara Proyector Astronauta Galaxy',
    price: '59,000',
    description: 'Lámpara proyector con diseño de astronauta. Proyecta imágenes de galaxias para crear una atmósfera mágica.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1049385/1722981290D_NQ_NP_643422-MCO77992638741_072024-O.webp'
},
{
    name: 'Lampara Astronauta Esfera D',
    price: '55,000',
    description: 'Lámpara en forma de astronauta con diseño esférico. Ideal para decorar y dar un toque espacial a tu habitación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/919875/1718833343Imagen%20de%20WhatsApp%202024-06-19%20a%20las%2016.28.39_906dbb8d.jpg'
},
{
    name: 'Lampara Mata Mosquitos Electrico Pd',
    price: '45,000',
    description: 'Lámpara mata mosquitos con tecnología UV. Incluye luz LED y conexión USB, ideal para mantener tu hogar libre de insectos sin químicos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1073149/1723576941Corrector%20postura%20pd-38%20(1).png'
},
{
    name: 'Lampara Cristal Escritorio Nocturna D',
    price: '37,000',
    description: 'Lámpara de cristal nocturna para escritorio. Aporta una iluminación suave y elegante para tu espacio de trabajo o estudio.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1071813/17235657477.jpg'
},
{
    name: 'Lampara Esfera Bola De Cristal D Base D',
    price: '37,000',
    description: 'Lámpara de esfera de cristal con base decorativa. Ideal para iluminar y embellecer cualquier habitación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1070144/1723503859WhatsApp%20Image%202024-08-09%20at%206.21.15%20PM.jpeg'
},
{
    name: 'Lampara Esfera De Cristal D Virgen',
    price: '37,000',
    description: 'Lámpara de esfera de cristal con diseño elegante. Perfecta para iluminar y decorar espacios con un toque moderno.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1069658/1723499673WhatsApp%20Image%202024-08-09%20at%204.03.52%20PM.jpeg'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico de leche materna, ideal para extraer y almacenar leche de manera eficiente. Incluye accesorios para un uso práctico y cómodo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Lampara Esfera De Cristal Globo Terráqueo',
    price: '37,000',
    description: 'Lámpara esférica de cristal con diseño de globo terráqueo. Ideal para decoración y ambientación de espacios.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1069164/1723498005WhatsApp%20Image%202024-08-09%20at%202.29.57%20PM.jpeg'
},
{
    name: 'Lampara Solar Kit De Herramienta',
    price: '59,000',
    description: 'Linterna LED multifuncional con carga solar y USB. Incluye herramientas esenciales y tiene 3 modos de luz. Ideal para acampar y emergencias.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1065995/1723460975D_NQ_NP_2X_744235-MLC77351113435_062024-F.webp'
},
{
    name: 'Lampara Led Magnetica Multifuncion',
    price: '39,000',
    description: 'Lámpara LED magnética multifuncional. Ofrece iluminación ajustable y es ideal para diversas aplicaciones.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1061702/1723240270Lampara%20Led%20Magnetica%20Blanco%20A.jpg'
},
{
    name: 'Lampara Uv Led De Secado De Uñas',
    price: '39,000',
    description: 'Cabina UV LED para secado de uñas. Compacta y eficiente, ideal para manicura profesional y uso doméstico.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1009856/1721846767D_NQ_NP_2X_869487-MLU70707513177_072023-F.webp'
},
{
    name: 'Kit Pulidor De Uñas Electrico Recargable',
    price: '37,000',
    description: 'Pulidor eléctrico recargable con 5 cabezales. Ofrece manicura completa con ajustes de velocidad y luz LED para precisión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1049353/1722981154D_NQ_NP_776543-MCO69251024777_052023-O.webp'
},
{
    name: 'Lampara Uvled Unas Sun',
    price: '49,000',
    description: 'Lámpara UV LED de 72W para secado rápido de gel y esmalte semipermanente. Ofrece 3 opciones de tiempo y diseño cómodo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/912718/17182180638d892f7f-1ca9-4bcb-a036-672274cd6261.jpg'
},
{
    name: 'Estante Giratorio Almacenamiento Redondo',
    price: '239,000',
    description: 'Estante giratorio de acero, ideal para cocina y otros espacios. Resistente, con capacidad para 200 libras y sin necesidad de instalación.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/362530/1719348215ESTR4.jpg'
},
{
    name: 'Organizador Estante De Baño Repisa',
    price: '75,000',
    description: 'Estante de baño con diseño funcional y resistente. Ideal para organizar artículos en el baño y otras áreas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1048415/1722971274WZ3.jpg'
},
{
    name: 'Estante Lavadora',
    price: '75,000',
    description: 'Estante para lavadora, diseñado para ofrecer almacenamiento adicional y organización en el área de lavandería.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/924704/1719331754organizador%20lavadora%20RS-7%202.jpg'
},
{
    name: 'Estante Carrito Multiusos De Niveles',
    price: '75,000',
    description: 'Carrito de almacenamiento de 4 niveles con ruedas. Ideal para organización en cocinas, baños y oficinas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/766487/1712778146WhatsApp%20Image%202024-04-10%20at%202.36.33%20PM.jpeg'
},
{
    name: 'Combo Hidrolavadora Cepillo Microfibra',
    price: '119,000',
    description: 'Combo de hidrolavadora y cepillo de microfibra. Ideal para limpieza profunda en exteriores e interiores.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/979204/1721082274port.jpg'
},
{
    name: 'Hidrolavadora Alta Presion Portatil V',
    price: '149,000',
    description: 'Hidrolavadora portátil de alta presión con capacidad de 18L. Ideal para limpiar autos, ventanas y más. Incluye accesorios.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1033555/1722480961D_NQ_NP_2X_670320-MCO50056422625_052022-F.jpg'
},
{
    name: 'Combo Taladro Pulidora Dca',
    price: '199,000',
    description: 'Combo taladro y pulidora de Protool. Incluye herramientas versátiles para perforar y pulir con alta velocidad y rendimiento.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1066711/1723472439TALADRO%20DC1A.jpeg'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor eléctrico para extraer leche materna de forma eficiente. Ideal para madres lactantes que buscan comodidad y rapidez en el proceso de extracción.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Kit De Herramientas X 82 Pcs',
    price: '119,000',
    description: 'Juego completo de herramientas manuales de 82 piezas, incluye destornilladores, alicates, llaves, martillo, y más. Fabricado en acero de alta calidad y presentado en estuche de polipropileno.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1061759/172324127817030810311703081031D_NQ_NP_810566-MCO48925173685_012022-O.jpeg'
},
{
    name: 'Guadaña',
    price: '449,000',
    description: 'Guadaña semi profesional de 52CC con motor de 2 tiempos. Tubo de aluminio resistente y bajo consumo de combustible. Ideal para trabajos de jardinería exigentes.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1011380/17218734251713801840GUADA%C3%91A.jpeg'
},
{
    name: 'Guadaña Recargable V Con Ruedas',
    price: '149,000',
    description: 'Guadaña inalámbrica de 1200W con batería de litio de 48V. Incluye ruedas y cuchillas, ideal para corte de césped con gran movilidad y facilidad de uso.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/918641/1718742065D_NQ_NP_2X_784197-MCO75161598533_032024-F.webp'
},
{
    name: 'Guadaña Batería Portátil Completa',
    price: '135,000',
    description: 'Guadaña portátil con batería recargable. Ideal para trabajos de jardinería con facilidad y sin cables.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/967236/1720890128GUADA%C3%91A_1_BATERIA_PORTATIL_COMPLETA(2)%20-%20copia.jpg'
},
{
    name: 'Picador Eléctrico',
    price: '47,000',
    description: 'Picador eléctrico para ingredientes de cocina. Ideal para picar cilantro y especias con rapidez y precisión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/999420/1721618251Screen%20Shot%202024-05-15%20at%2012.36.02%20PM.png'
},
{
    name: 'Picador De Cilantro Y Especias Molillo',
    price: '32,000',
    description: 'Molino multifuncional para cilantro y especias. Material de acero inoxidable con tapa de seguridad para uso fácil y seguro.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/985891/1721245145Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-07-17T143751.596.png'
},
{
    name: 'Taladro Juegos De Herramientas',
    price: '199,000',
    description: 'Kit de taladro inalámbrico de 24V con 2 baterías, cargador y maleta. Incluye accesorios y sistema de iluminación LED para trabajos precisos.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/1086198/1723834093WhatsApp%20Image%202024-08-16%20at%201.47.06%20PM.jpeg'
},
{
    name: 'Taladro Con Percutor ZZ4100',
    price: '169,000',
    description: 'Taladro de impacto de 710W con velocidad variable y reversible. Incluye 20 accesorios para taladrar y atornillar diversos materiales.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/989834/1721317717TALADRO%20ZZ4100.jpeg'
},
{
    name: 'Taladro Destornillador Portátil Giratorio',
    price: '69,000',
    description: 'Taladro destornillador portátil giratorio con alta capacidad y eficiencia. Ideal para trabajos domésticos y de bricolaje.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/992733/1721367890451238719_497745909286941_5035934427497966028_n.jpg'
},
{
    name: 'Kit De Taladro Caja De Herramientas',
    price: '165,000',
    description: 'Taladro compacto y ergonómico con batería de alto rendimiento. Incluye cargador y sistema de iluminación LED para mayor visibilidad.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/962412/1720639206kit%20taladro.png'
},
{
    name: 'Percutor Taladro Con Pilas Y Accesorios',
    price: '169,000',
    description: 'Taladro con percusión a batería, incluye accesorios y pilas. Ideal para una amplia variedad de aplicaciones de perforación y atornillado.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/974116/1720890147WhatsApp%20Image%202024-07-11%20at%207.58.01%20PM.jpeg'
},
{
    name: 'Taladro MK 24V Con Pulidor',
    price: '199,000',
    description: 'Taladro de 24V con mandril de 3/8” y accesorios para pulido. Incluye 2 baterías y base de carga rápida.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/839893/17151934076.png'
},
{
    name: 'Cepillo Cerdas Para Taladro 3 Unds Uyust',
    price: '39,000',
    description: 'Cepillo para taladro con 3 piezas de cerdas de microfibra. Ideal para limpiar superficies del hogar sin rayarlas.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/974462/1720899885uyust%20taladro%20foto%202.jpg'
},
{
    name: 'Extractor De Leche Materna Eléctrico',
    price: '89,000',
    description: 'Extractor de leche materna eléctrico. Eficiente y cómodo para la extracción de leche. Ideal para madres lactantes.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/636963/1707253034WhatsApp%20Image%202024-02-01%20at%204.52.39%20PM.jpeg'
},
{
    name: 'Audífonos i12',
    price: '45,000',
    description: 'Audífonos Bluetooth i12 con cancelación activa de ruido, batería de 35 mAh por auricular y 300 mAh en el estuche. Incluye cargador y garantía de 3 meses.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/878090/1716392718D_NQ_NP_680819-MCO48054379392_102021-O.webp'
},
{
    name: 'Audífonos Conducción Ósea - Aeropex Msl1',
    price: '35,000',
    description: 'Auriculares de conducción ósea, resistentes al agua, con Bluetooth 5.1. Batería de 150 mAh y hasta 4 horas de uso continuo.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/376435/17018735481701873548RUAevSGtG3klAaFUPAdBDbsPAjlKrZeZTn1NxpCx.png'
},
{
    name: 'Audífonos Para Discapacitados',
    price: '45,000',
    description: 'Amplificador auditivo recargable con cancelación de ruido digital. Diseño cómodo y modo de amplificación ajustable.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/88311/17030150781703015078117%20audifo.jpg'
},
{
    name: 'Audífonos Inalámbricos JBL X8',
    price: '69,000',
    description: 'Auriculares JBL inalámbricos con 4 horas de reproducción continua y 20 horas con el estuche. Certificación IPX5 y Bluetooth 5.0.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/217942/17023007781702300778image-removebg-preview%20(24).png'
},
{
    name: 'Audífonos Diadema Gato',
    price: '79,000',
    description: 'Auriculares Bluetooth con orejas de gato y luces LED RGB. Diseño para fiestas y eventos con hasta 6 horas de música.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/104703/1702391239170239123910001740_10302401_961765.jpeg'
},
{
    name: 'AirPods Pro 2ª Generación',
    price: '79,000',
    description: 'AirPods Pro con cancelación activa de ruido, audio espacial y control táctil. Hasta 6 horas de reproducción con una carga.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/711659/1710449942Captura%20de%20pantalla%202024-03-14%20155756.png'
},
{
    name: 'Mini Impresora Portátil Térmica Inalámbrica + 1 Rollo Papel',
    price: '75,000',
    description: 'Impresora térmica portátil con conexión Bluetooth. Imprime en blanco y negro, compatible con iOS y Android. Incluye rollo de papel y cargador.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/918623/1718741339WhatsApp%20Image%202024-06-17%20at%2012.12.29%20PM.jpeg'
},
{
    name: 'Impresora Térmica Portátil Recargable',
    price: '149,000',
    description: 'Impresora térmica de recibos con Bluetooth y soporte para Android, iOS y Windows. Imprime a 203 ppp con una velocidad de 2.756 in/s.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/908611/1717860497Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-06-07T170332.517.png'
            },
            {
                name: 'Tapete Alfombra Para Baño Absorbente',
                price: '37,000',
                description: 'Alfombra de baño super absorbente y antideslizante. Hecha de material suave y ecológico, con superficie que absorbe la humedad y capa de espuma que evapora rápidamente. Fácil de lavar y duradera. Medidas: 40x60 cm. Incluye 1 alfombrilla. Garantía de 30 días por defectos de fábrica.',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/257672/17018993201701899320Tapete%20De%20Ba%C3%B1o%20Super%20Absorbente%20Y%20Antideslizante%20A.jpg'
            }
            //  Agregar aquí más productos hasta 1000

        ];

        const productContainer = document.getElementById('product-list');

        function normalizeString(str) {
            return str.normalize("NFD").replace(/[\u0300-\u036f]/g, "").replace(/[^\w\s]/gi, '').toLowerCase();
        }

        function renderProducts(products) {
            productContainer.innerHTML = '';
            products.forEach(product => {
                const productElement = document.createElement('div');
                productElement.className = 'product';
                productElement.innerHTML = `
                    <img src="${product.image}" alt="${product.name}">
                    <h2>${product.name}</h2>
                    <p class="price">${product.price} COP</p>
                    <p>${product.description}</p>
                    <button class="buy-form" onclick="window.location.href='https://forms.gle/ocFidTiYodHjo1QB7'">Comprar</button>
                    <button class="whatsapp" onclick="buyProduct('${product.name}')">WhatsApp</button>
                `;
                productContainer.appendChild(productElement);
            });
        }

        document.getElementById('search').addEventListener('input', (e) => {
            const query = normalizeString(e.target.value);
            const filteredProducts = products.filter(product => 
                normalizeString(product.name).includes(query)
            );
            renderProducts(filteredProducts);
        });

        renderProducts(products);

        function buyProduct(productName) {
            window.location.href = `https://api.whatsapp.com/send?phone=+3206572598&text=Hola,%20quiero%20comprar%20el%20producto:%20${productName}`;
        }
    </script>
</body>
</html>

