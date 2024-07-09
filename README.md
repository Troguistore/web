<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TROGUI ROPA - Tienda Online</title>
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
        }
        .product-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            padding: 20px;
        }
        .product {
            border: 1px solid #cccccc;
            border-radius: 10px;
            margin: 10px;
            padding: 20px;
            width: 250px;
            text-align: center;
            background-color: #f9f9f9;
            color: #000000;
        }
        .product img {
            max-width: 100%;
            border-radius: 10px;
        }
        .product h2 {
            color: #ff6600;
            font-size: 24px;
        }
        .product p {
            font-size: 16px;
        }
        .product .price {
            font-size: 20px;
            font-weight: bold;
        }
        .product button {
            background-color: #000000;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 5px;
        }
        .product button:hover {
            background-color: #ff6600;
        }
    </style>
</head>
<body>
    <header>
        <h1>TROGUI ROPA</h1>
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
                name: 'Tenis adidas capellada',
                price: '89,000',
                description: 'Tallas: 35 36 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/711254/1710444483WhatsApp%20Image%202024-03-14%20at%202.09.47%20PM%20(1).jpeg'
            },
            {
name: 'Adidas Bounce Blanco Rosa Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/888514/1716662311WhatsApp%20Image%202024-05-24%20at%206.28.13%20PM%20(4).jpeg'
},
{
    name: 'Adidas Superstar Blanco Unisex',
    price: '89,000',
    description: 'Talla desde la 35 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/70833/17030250961703025096IMG_20220623_150655.jpg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/170187091517018709152e486f13-e49a-4fcf-8236-d1a77b3d91a8-removebg-preview.png'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/170187091517018709157c994a14-3d0d-40ea-8e4a-66a15368ddd9-removebg-preview.png'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217160WhatsApp%20Image%202024-03-23%20at%2012.31.27%20PM%20(1).jpeg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217160WhatsApp%20Image%202024-03-23%20at%2012.31.28%20PM%20(2).jpeg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217160WhatsApp%20Image%202024-03-23%20at%2012.31.29%20PM%20(3).jpeg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217160WhatsApp%20Image%202024-03-23%20at%2012.31.29%20PM%20(2).jpeg'
},
{
    name: 'Adidas Suela Alta Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/700646/171000747917018799541701879954WhatsApp%20Image%202023-07-30%20at%204.40.46%20PM%20(1).jpeg'
},
{
    name: 'Adidas Suela Alta Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/700646/171000747917018799531701879953WhatsApp%20Image%202023-07-30%20at%204.40.47%20PM%20(1).jpeg'
},
{
    name: 'Adidas Suela Alta Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/700646/171000747917018799541701879954WhatsApp%20Image%202023-07-30%20at%204.40.47%20PM.jpeg'
},
{
    name: 'Adidas Suela Alta Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/700646/171000747917018799541701879954WhatsApp%20Image%202023-07-30%20at%204.40.46%20PM.jpeg'
},
{
    name: 'Bolso Adidas Hombre',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/799878/1713902400bolso%20gris.jpeg'
},
{
    name: 'Bolso Adidas Hombre',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/799878/1713902400bolso%20negro.jpeg'
},
{
    name: 'Bolso Adidas Hombre',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/799878/1713902400bolso%20blanco.jpeg'
},
{
    name: 'Adidas Fresh Caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/720177/171080883317018927411701892741WhatsApp%20Image%202023-06-12%20at%206.09.44%20PM.jpeg'
},
{
    name: 'Adidas Fresh Caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/720177/171080883417018927401701892740WhatsApp%20Image%202023-06-12%20at%206.09.45%20PM.jpeg'
},
{
    name: 'Adidas Fresh Caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/720177/171080883417018949181701894918WhatsApp%20Image%202023-06-12%20at%206.09.41%20PM.jpeg'
},
{
    name: 'Adidas Fresh Caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/720177/171080883417018927401701892740WhatsApp%20Image%202023-06-12%20at%206.09.44%20PM%20(1).jpeg'
},
{
    name: 'Adidas Fresh Caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/720177/171080883417018949181701894918WhatsApp%20Image%202023-06-12%20at%206.09.43%20PM.jpeg'
},
{
    name: 'Conjunto Deportivo Adidas',
    price: '89,000',
    description: '👕*CONJUNTO DEPORTIVO DRITFIT TELA GALLETA 🍪👕✅•Calidad AAA✅•Con bolsillo y cremallera✅•Importado✅ Tallas disponibles S M L Xl variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/902789/171718940257321e32-26be-4bd3-88ea-d6fc676b7b58.jpg'
},
{
    name: 'Zapatillas Adidas 2000 Zx Caballero',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400360/17018709081701870908WhatsApp_Image_2023-09-16_at_16.19.59__1_-removebg-preview.png'
},
{
    name: 'Tenis Adidas Mujer Suela Cocodrilo',
    price: '89,000',
    description: 'Material: Sintético Suela: Inyectada Modelo: Deportivo Sexo: Dama Color: Variable',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/435534/1697038904WhatsApp%20Image%202023-10-05%20at%204.17.21%20PM.jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.51%20PM%20(2).jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/17150597133db35847-aaaa-4542-b4ec-26917c634952.jpg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.50%20PM.jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.50%20PM%20(1).jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.51%20PM%20(1).jpeg'
},
{
    name: 'Docena Medias Adidas',
    price: '49,000',
    description: 'Descubre el confort y la elegancia con nuestras medias tobilleras Adidas Triple A!',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/910530/1717881492PHOTO-2024-06-08-14-21-46.jpeg'
},
{
    name: 'Bolso Carriel Antirrobo Canguro Deportivo',
    price: '65,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/604610/17147697608f7f6fae-12d8-4fca-b721-42f329190956.jpg'
},
{
    name: 'Maleta Antirrobo Canguro Mochila, Bolso',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/494505/171924698973ed2b6c-a1d1-4135-b73f-3efe98d25c8f.jpeg'
},
{
    name: 'Bolso Dama Ref S13',
    price: '69,000',
    description: '✅FRENTE MATERIAL SINTÉTICO BRILLANTE ✅DOS COMPARTIMENTOS ✅CIERRES METÁLICOS ALTO 13 CM ANCHO 20 CM',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/617326/1706218352WhatsApp%20Image%202024-01-18%20at%202.49.20%20PM.jpeg'
},
{
    name: 'Bolso Dama Ref S13',
    price: '69,000',
    description: '✅FRENTE MATERIAL SINTÉTICO BRILLANTE ✅DOS COMPARTIMENTOS ✅CIERRES METÁLICOS ALTO 13 CM ANCHO 20 CM',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/617326/1706218352WhatsApp%20Image%202024-01-18%20at%202.49.18%20PM.jpeg'
},
{
    name: 'Bolso Dama Ref S13',
    price: '69,000',
    description: '✅FRENTE MATERIAL SINTÉTICO BRILLANTE ✅DOS COMPARTIMENTOS ✅CIERRES METÁLICOS ALTO 13 CM ANCHO 20 CM',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/617326/1706218352WhatsApp%20Image%202024-01-18%20at%202.49.19%20PM%20(1).jpeg'
},
{
    name: 'Bolso Dama Ref S13',
    price: '69,000',
    description: '✅FRENTE MATERIAL SINTÉTICO BRILLANTE ✅DOS COMPARTIMENTOS ✅CIERRES METÁLICOS ALTO 13 CM ANCHO 20 CM',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/617326/1706218352WhatsApp%20Image%202024-01-18%20at%202.49.19%20PM.jpeg'
},
{
    name: 'Bolso para celular multifuncional',
    price: '42,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/850382/1715288233PhotoRoom_20240202_233232.JPG'
},
{
    name: 'Bolso Viajero Cruzado Pechero',
    price: '49,000',
    description: 'color negro, rosado, gris y blanco',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/878511/1716503395WhatsApp%20Image%202024-05-23%20at%204.08.23%20PM%20(2).jpeg'
},
{
                name: 'Adidas 2k Blanco Naranja Caballero',
                price: '89,000',
                description: 'Tallas: 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284293/17018822151701882215xltU3RMvvSS7M6N9juJct9FdtTbEV5GJG8JT46p7.jpg'
            },
            {
    name: 'Adidas Bounce Gris Rosa Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/888519/1716662752WhatsApp%20Image%202024-05-24%20at%206.28.13%20PM%20(2).jpeg'
},
{
    name: 'Adidas 2k full negro caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284306/17018822151701882215z3c7EatlZivGgG7AEdLuDKaD4PH7tnhMpy9t3Lxy.jpg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217161WhatsApp%20Image%202024-03-23%20at%2012.31.26%20PM%20(1).jpeg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217161WhatsApp%20Image%202024-03-23%20at%2012.31.29%20PM%20(1).jpeg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/1711217161WhatsApp%20Image%202024-03-23%20at%2012.31.27%20PM%20(2).jpeg'
},
{
    name: 'Tenis Adidas Forum Caballero',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/400321/17018709151701870915659fcb4f-8d1d-42a8-882e-65f76581f15a-removebg-preview.png'
},
{
    name: 'Adidas 2k Blanco Naranja Caballero',
    price: '89,000',
    description: 'Talla desde la 37 hasta 43 (variedad de colores)',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284293/17018822151701882215xltU3RMvvSS7M6N9juJct9FdtTbEV5GJG8JT46p7.jpg'
},
{
    name: 'Adidas Stan Smith',
    price: '89,000',
    description: 'Blanco, blanco con verde y blanco con negro',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/671362/1708718576WhatsApp%20Image%202024-02-23%20at%202.20.27%20PM.jpeg'
},
{
    name: 'Estuche para guardar gorras',
    price: '89,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/765586/1712761593e3ecd5c3-516e-40a2-84ed-654e416fd57f.jpeg'
},
{
    name: 'Gorra para bebé',
    price: '47,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/802961/1713988399WhatsApp%20Image%202024-04-24%20at%2013.45.49.jpeg'
},
{
    name: 'Gorra Guadalupe Espigas Negras',
    price: '76,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/924085/1719281385WhatsApp%20Image%202024-06-24%20at%2011.50.09%20AM.jpeg'
},
{
    name: 'Adidas Bounce Negro Gris Caballero',
    price: '89,000',
    description: 'Talla 37, 38, 39, 40, 41, 42 y 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/888502/1716661355WhatsApp%20Image%202024-05-24%20at%206.33.13%20PM%20(2).jpeg'
},
{
    name: 'Tenis Adidas Samba',
    price: '89,000',
    description: 'Blanco con verde, blanco con azul y rojo, blanco con negro, negro con rosado, talla desde la 37 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/895850/1717778628WhatsApp%20Image%202024-06-04%20at%203.35.18%20PM.jpeg'
},
{
    name: 'Adidas 2k Negro Fucsia Dama',
    price: '89,000',
    description: 'Desde la talla 35 hasta la 40',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/319528/17018822151701882215WhatsApp%20Image%202023-07-16%20at%205.00.05%20PM%20(3).jpeg'
},
{
    name: 'Adidas Ultraboost Dama',
    price: '89,000',
    description: 'Talla desde la 35 hasta la 40',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/677570/1709061208WhatsApp%20Image%202023-07-15%20at%2011.24.34%20AM%20(1).jpeg'
},
{
    name: 'Adidas Ultra Boost',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713317/1710518440WhatsApp%20Image%202024-03-15%20at%2010.56.42%20AM%20(2).jpeg'
},
{
    name: 'Adidas Ultra Boost',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713317/1710518440WhatsApp%20Image%202024-03-15%20at%2010.56.42%20AM%20(3).jpeg'
},{
    name: 'Gorra At Originals Drill',
    price: '69,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/879123/171640482114.jpg'
},
{
    name: 'Gorra Premium Tio Rico',
    price: '59,000',
    description: 'Blanco y negro',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/852457/1718985549WhatsApp%20Image%202024-05-10%20at%2011.52.38%20AM.jpeg'
},
{
    name: 'Gorra de búho',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/454907/1700071505WhatsApp%20Image%202023-11-15%20at%2013.03.31.jpeg'
},
{
    name: 'Gorra del Nacional',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/523808/1700853772WhatsApp%20Image%202023-11-23%20at%2011.30.50.jpeg'
},
{
    name: 'Gorra Essentials Gamuza',
    price: '49,000',
    description: 'Café oscuro, rojo, azul, café claro, blanco',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/773521/1716941802WhatsApp%20Image%202024-05-28%20at%202.26.13%20PM%20(2).jpeg'
},
{
    name: 'Gorra Silvestre WB',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/891057/1716831160WhatsApp%20Image%202024-05-27%20at%2012.21.12%20PM.jpeg'
},
{
    name: 'Gorra Goorin Bros',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/450801/1704654835WhatsApp%20Image%202024-01-07%20at%2012.04.59.jpeg'
},
{
    name: 'Gorra Goorin Bros',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/450801/1704654835WhatsApp%20Image%202024-01-07%20at%2012.05.02%20(1).jpeg'
},
{
    name: 'Gorra Goorin Bros',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/450801/1704654835WhatsApp%20Image%202024-01-07%20at%2012.05.02.jpeg'
},
{
    name: 'Gorra Goorin Bros',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/450801/1704654835WhatsApp%20Image%202024-01-07%20at%2012.05.00.jpeg'
},
{
    name: 'Gorra Goorin Bros',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/450801/1704654835WhatsApp%20Image%202024-01-07%20at%2012.05.03.jpeg'
},
{
    name: 'Gorra Goorin Bros',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/450801/1704654835WhatsApp%20Image%202024-01-07%20at%2012.05.01.jpeg'
},
{
    name: 'Gorra Caballo Pin',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/472068/1698694648WhatsApp%20Image%202023-10-30%20at%2014.10.29.jpeg'
},
{
    name: 'Tenis Adidas Mujer Suela Cocodrilo',
    price: '89,000',
    description: 'Material: Sintético Suela: Inyectada Modelo: Deportivo Sexo: Dama Color: Variable',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/435534/1697038904WhatsApp%20Image%202023-10-05%20at%204.17.21%20PM.jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.51%20PM%20(2).jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/17150597133db35847-aaaa-4542-b4ec-26917c634952.jpg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.50%20PM.jpeg'
},
{
    name: 'Adidas Trebol Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/748278/1712205061WhatsApp%20Image%202023-07-16%20at%2010.23.50%20PM%20(1).jpeg'
},
{
        "name": "Tapete Antideslizante Galaxia Tpcos07",
        "price": "29,000",
        "description": "Tapete de poliéster de 39.5 x 60 cm. Perfecto para decoración y múltiples usos. Ideal para la puerta delantera, cocina, baño, dormitorio, sala, entre otros. Adecuado para amantes del cosmos y mascotas. Textura suave y material antideslizante, duradero y fácil de lavar. Se despacha aleatorio según disponibilidad. Contenido: 1 tapete antideslizante de galaxia. 100% nuevo.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/79394/17030214261703021426Tapete%20Antideslizante%20Galaxia%20Cosmos%20Multiusos%20TPCOS%204.jpg"
    },
    {
name: 'Tenis Running Adidas Alphabounce',
    price: '99,000',
    description: 'Tenis Running Adidas Alphabounce- Capellada inyectada Unicolor @- Marcas en Estampado y repujado @- Suela ultraliviana tipo running unicolor con marcas tipo original. @- Apliques en caucho y PVC tipo original. @- ⁠plantilla confort contramarcada. @- Riata reflectante en la parte trasera para protección en actividades nocturnas. -Unisex.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/763439/1712967743WhatsApp%20Image%202024-04-12%20at%207.04.03%20PM.jpeg'
},
{
    name: 'Maleta De Gimnasio Deportivo Fitness Mul',
    price: '49,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/797379/1713818696WhatsApp%20Image%202024-04-22%20at%203.27.55%20PM.jpeg'
},
{
    name: 'Maleta De Mano Para Cabina Viaje Amazon',
    price: '129,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/906366/1717628003MALETA%20DE%20VIAJE%20AMAZON%2003.png'
},
{
    name: 'Juego De Mochilas Kit X5',
    price: '99,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/879408/17164099096f56a43c-7f1f-42cc-ada5-e661a226129d%20(1).jpg'
},
{
    name: 'Mochila Kwai',
    price: '69,000',
    description: 'colores beige, lila y rosa',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/760551/1712605419descarga%20-%202024-02-05T082802.263.png'
},
{
    name: 'Mochila Donuts',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/599540/1705434415MOCHILA%20DONUTS.webp'
},
{
    name: 'Conjunto Deportivo',
    price: '49,000',
    description: 'talla única, colores verde, azul, gris y rojo',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/650701/1707857955Screenshot_1055.jpg'
},
{
    name: 'Conjunto Burda Vena',
    price: '65,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/608530/1708523846ENTERIZOS%20%20-%2037.jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.56%20PM.jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316181WhatsApp%20Image%202024-06-13%20at%202.40.57%20PM%20(2).jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316181WhatsApp%20Image%202024-06-13%20at%202.40.57%20PM%20(3).jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.57%20PM%20(1).jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.56%20PM%20(2).jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.56%20PM%20(3).jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.57%20PM.jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.56%20PM%20(4).jpeg'
},
{
    name: 'Conjunto Deportivo 3 Piezas',
    price: '69,000',
    description: 'Conjunto Deportivo DAMA 3 Piezas. Incluye: 1 Falda short + 1 Top + 1 Blusa velo. El conjunto viene en dos tallas: Talla Normal: Si eres en pantalón 6 - 8 - 10. Talla Plus: Si eres en pantalón 12 - 14 - 16 - 18.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/914749/1718316180WhatsApp%20Image%202024-06-13%20at%202.40.56%20PM%20(1).jpeg'
},
{
    name: 'Conjunto Print',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/919076/17187574866AD045B8-924D-4650-BF05-26A46DC7A364.jpg'
},
{
    name: 'Conjunto Print',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/919076/1718757487B04FD7AC-8C44-4D2F-A148-365ECFB0CDD5.jpg'
},
{
    name: 'Conjunto Print',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/919076/17187574870818EB80-2DC5-494F-A59C-B4606F0A6F0C.jpg'
},
{
    name: 'Conjunto Print',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/919076/1718757486214A65B6-83E1-45DF-9CE9-2A7D9182BB91.jpg'
},
{
    name: 'Conjunto Ref 04',
    price: '115,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/819989/1714501219acf6cc26-4ae6-4b86-af0e-8f8e5c3f70e8.jpeg'
},
{
    name: 'Conjunto Palazzo',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/923922/1719266456IMG_8046.jpeg'
},
{
    name: 'Conjunto Palazzo',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/923922/1719266456IMG_8047.jpeg'
},
{
    name: 'Conjunto bebé',
    price: '178,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/540396/1701538095WhatsApp%20Image%202023-12-01%20at%206.20.39%20PM.jpeg'
},
{
    name: 'Conjunto Nike',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/902808/1717189956f57c7bf2-4dac-4067-b0e2-54751d599201.jpg'
},
{
    name: 'Conjunto Oversize Burda',
    price: '69,000',
    description: 'colores negro, azul rey, camel, rojo, palo de rosa, azul claro, gris, lila',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/608471/170734034817.jpg'
},
{
    name: 'Conjunto Burda Bota Campana',
    price: '69,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/625646/17066534471.jpg'
},
{
    name: 'Vestido De Baño Asoleador',
    price: '49,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623031/1707204007fotos%20sin%20precio%20-%2058.png'
},
{
    name: 'Enterizo Largo Tiras',
    price: '69,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/852860/17156653881.jpg'
},
{
    name: 'Body Control Abdomen Blanco',
    price: '59,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/775793/171316404313.jpg'
},
{
    name: 'Body Control Abdomen Blanco',
    price: '59,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/775793/17131640438.jpg'
},
{
    name: 'Camiseta Colombia Col 1 2024',
    price: '75,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/917525/1718978471WhatsApp%20Image%202024-06-17%20at%2022.39.29%20(6).jpeg'
},
{
    name: 'Camiseta Colombia Col 1 2024',
    price: '75,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/917525/1718978474WhatsApp%20Image%202024-06-17%20at%2022.39.31%20(9).jpeg'
},
{
    name: 'Blusa Corta Mallatex Lurex',
    price: '49,000',
    description: 'colores negro, blanco y camel',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/608077/17059537025.jpg'
},
{
    name: 'Blusa Manga Larga Mallatex Lurex',
    price: '55,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/608219/17059538271.jpg'
},
{
    name: 'Leggins Suplex',
    price: '42,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/885578/17165678877C10C55B-E3FF-4131-8F3B-0F1BB8F3D7F3.jpeg'
},
{
    name: 'Enterizo Corto Manga Corta Cierre Pluss',
    price: '69,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/902675/1717186187IMG_3287.jpg'
},
{
    name: 'Camiseta Local Amarilla Colombia 3a',
    price: '75,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/908438/17178112964.jpg'
},
{
    name: 'Vestido Enresortado',
    price: '79,000',
    description: 'Este vestido te ofrece un ajuste perfecto que te hará sentir segura y cómoda en cualquier ocasión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761605/171261663032AF27B9-0DD9-412E-A505-446449C335E4.jpg'
},
{
    name: 'Vestido Enresortado',
    price: '79,000',
    description: 'Este vestido te ofrece un ajuste perfecto que te hará sentir segura y cómoda en cualquier ocasión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761605/1712616633C60DFD46-68C5-4097-8B8C-42C7EEF0201E.jpg'
},
{
    name: 'Vestido Enresortado',
    price: '79,000',
    description: 'Este vestido te ofrece un ajuste perfecto que te hará sentir segura y cómoda en cualquier ocasión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761605/1712616632D79CE47B-1E1F-45B1-89BE-4145C06C86FF.jpg'
},
{
    name: 'Vestido Enresortado',
    price: '79,000',
    description: 'Este vestido te ofrece un ajuste perfecto que te hará sentir segura y cómoda en cualquier ocasión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761605/171261663376CE95C6-A2B7-422C-8FDB-354453A6B002.jpg'
},
{
    name: 'Tenis Adidas Dunk Dama',
    price: '69,000',
    description: 'Material: Sintético Suela; InyectadaModelo; Deportivo Sexo: Dama Color :Variable',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/288752/17018925151701892515WhatsApp%20Image%202023-06-15%20at%204.57.31%20PM%20(4).jpeg'
},
{
    name: 'Tenis Adidas Dunk Dama',
    price: '69,000',
    description: 'Material: Sintético Suela; InyectadaModelo; Deportivo Sexo: Dama Color :Variable',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/288752/17018925151701892515WhatsApp%20Image%202023-06-15%20at%204.57.32%20PM%20(1).jpeg'
},
{
    name: 'Tenis Adidas Dunk Dama',
    price: '69,000',
    description: 'Material: Sintético Suela; InyectadaModelo; Deportivo Sexo: Dama Color :Variable',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/288752/17018925141701892514WhatsApp%20Image%202023-06-15%20at%204.57.31%20PM%20(5).jpeg'
},
{
    name: 'Tenis Adidas Dunk Dama',
    price: '69,000',
    description: 'Material: Sintético Suela; InyectadaModelo; Deportivo Sexo: Dama Color :Variable',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/288752/17018925141701892514WhatsApp%20Image%202023-06-15%20at%204.57.31%20PM%20(3).jpeg'
},
{
    name: 'Adidas 2k Negro Naranja Caballero',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284280/17018949211701894921d9fb7646-0a94-4553-9b0d-e306e6544313.jpg'
},
{
    name: 'Trio Adidas Retropy',
    price: '165,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/798871/1713888641WhatsApp%20Image%202024-02-23%20at%205.39.18%20PM%20(8).jpeg'
},
{
    name: 'Trio Adidas Retropy',
    price: '165,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/798871/1713888641WhatsApp%20Image%202024-02-23%20at%205.39.19%20PM%20(2).jpeg'
},
{
    name: 'Trio Adidas Retropy',
    price: '165,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/798871/1713888641WhatsApp%20Image%202024-02-24%20at%2012.33.33%20PM.jpeg'
},
{
    name: 'Trio Adidas Retropy',
    price: '165,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/798871/1713888641WhatsApp%20Image%202024-02-23%20at%205.39.18%20PM%20(4).jpeg'
},
{
    name: 'Adidas Bounce Blanco Rosa Dama',
    price: '89,000',
    description: 'Talla desde la 35 hasta la 40, variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/888514/1716662311WhatsApp%20Image%202024-05-24%20at%206.28.13%20PM%20(4).jpeg'
},
{
    name: 'Adidas Ozmillen Dama',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/924727/1719332249IMG_3658.JPG'
},
{
    name: 'Adidas Ozmillen Dama',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/924727/1719332249IMG_3656%20(1).JPG'
},
{
    name: 'Adidas Ozmillen Dama',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/924727/1719332249IMG_3653.JPG'
},
{
    name: 'Adidas Ozmillen Dama',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/924727/1719332248IMG_3655.JPG'
},
{
    name: 'Bolso Deportivo - Gym Y O Viaje Rojo',
    price: '65,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/446275/1697643265CAD5F6F6-D273-458A-A80A-DBB7B9989D31.jpeg'
},
{
    name: 'M04 Bolso Viajero',
    price: '129,000',
    description: 'Bolso viajero elaborado en sintético de alta calidad, no descascara no pela y sus herrajes no cambian de color, en su interior tiene dos bolsillos funcionales en los lados, y un bolsillo funcional con cierre, trae una tira graduable y espacio suficiente para que lleves tus pertenencias de manera organizada. Va empacado en bolsa blanca en tela no tejida y recubierta en una bolsa de plástica. MEDIDAS Alto: 30cm Ancho: 48 cm Profundidad:25cm',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/658139/1708118345M04%20CAFE%202-Photoroom.jpg'
},
{
    name: 'Vestido Enresortado',
    price: '79,000',
    description: 'Este vestido te ofrece un ajuste perfecto que te hará sentir segura y cómoda en cualquier ocasión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761605/171261663218996E07-D932-4C9D-AE4D-147591DCC6EC.jpg'
},
{
    name: 'Vestido Enresortado',
    price: '79,000',
    description: 'Este vestido te ofrece un ajuste perfecto que te hará sentir segura y cómoda en cualquier ocasión.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/761605/1712616632B44A7FF6-4DD2-4A94-92FE-72D9C3459C6F.jpg'
},
{
    name: 'Vestido Kalvin',
    price: '59,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/82163/17018825211701882521SkM592AFRAqPfjiVw5IJdPE10cENzeYzY2mnG8cX.jpg'
},
{
    name: 'Vestido De Baño Ariel Vb para niña',
    price: '65,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/467629/1698439639WhatsAppImage2022-07-21at2.20.37PM_2_1024x1024@2x.webp'
},
{
    name: 'Vestido de baño barbie vb niña',
    price: '65,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/467619/1698439332WhatsAppImage2022-07-21at2.20.39PM_1024x1024@2x.webp'
},
{
    name: 'Vestido de baño flamencos vb niña',
    price: '65,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/467666/1698440085WhatsAppImage2022-07-21at2.20.36PM_1024x1024@2x.webp'
},
{
    name: 'Buzo Buso,Hoodies Hombre Manchester City',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/257972/17018993021701899302WhatsApp%20Image%202023-05-11%20at%201.12.18%20PM.jpeg'
},
{
    name: 'Buzo, buso hoodie karol g',
    price: '79,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/712034/1710455201WhatsApp%20Image%202024-03-09%20at%2012.43.16%20PM%20(3).jpeg'
},
{
    name: '2 Buso buzo, hoodie millonarios azul rey',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/830858/1714842729millonarios%20%20azul%20rey%20.jpg'
},
{
    name: 'Buso buzo, hoodie pareja america combinad',
    price: '139,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/835384/1715054821WhatsApp%20Image%202024-03-27%20at%2011.31.22%20AM%20(5).jpeg'
},
{
    name: 'Buzo buso,hoodies hombre liverpool',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/118119/17023889421702388942WhatsApp%20Image%202022-11-30%20at%2011.37.57%20AM.jpeg'
},
{
    name: 'Buzo buso,hoodies osito mujer blanco',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/298784/17018914951701891495WhatsApp%20Image%202023-06-24%20at%2010.56.22%20AM%20(3).jpeg'
},
{
    name: 'Buzo buso,hoodies hombre nacional saco',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/73927/17030223991703022399guia-de-tallas-masculino-Mesa-de-trabajo-1-copia.png'
},
{
    name: 'Buzo buso,hoodies hombre america saco',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/73918/17030224001703022400guia-de-tallas-masculino-Mesa-de-trabajo-1-copia.png'
},
{
    name: 'Buzo, Buso Hoodie Blanco Mickey',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/615087/1706126231mickey.png'
},
{
    name: 'Buzo, Buso monastery',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/731020/1711219399WhatsApp%20Image%202024-03-23%20at%2012.21.22.jpeg'
},
{
    name: 'Buzo , Buso Real Madrid',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/118637/17023888761702388876real%20madrid.jpg'
},
{
    name: 'Saco del América',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/73921/17030224001703022400guia-de-tallas-masculino-Mesa-de-trabajo-1-copia.png'
},
{
    name: 'Saco de Bucaramanga',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/835298/1715047920BUCARAMANGA%20COMBIANDO.jpg'
},
{
    name: 'Saco del millonario',
    price: '79,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/81910/17030194891703019489millos%20.jpg'
},
{
    name: 'Deportivo Nike Speed X',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/908304/17177992676335f60f-2f50-4541-82d3-1aa3c39a550f.jpg'
},
{
    name: 'M04 Bolso Viajero',
    price: '129,000',
    description: 'Bolso viajero elaborado en sintético de alta calidad, no descascara no pela y sus herrajes no cambian de color, en su interior tiene dos bolsillos funcionales en los lados, y un bolsillo funcional con cierre, trae una tira graduable y espacio suficiente para que lleves tus pertenencias de manera organizada. Va empacado en bolsa blanca en tela no tejida y recubierta en una bolsa de plástica. MEDIDAS Alto: 30cm Ancho: 48 cm Profundidad:25cm',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/658139/1708118345M04%20NEGRO%202-Photoroom.jpg'
},
{
    name: 'Bolso Morral De Lujo Llavero Pompon',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/743736/171207324627.png'
},
{
    name: 'Bolso Morral De Lujo Llavero Pompon',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/743736/171207324628.png'
},
{
    name: 'Bolso Morral De Lujo Llavero Pompon',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/743736/17120732461.png'
},
{
    name: 'Bolso Grande De Viaje Morral Multif Bo 6',
    price: '65,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/915819/1718402410Dise%C3%B1o%20sin%20t%C3%ADtulo%20-%202024-06-14T165858.903.png'
},
{
    name: 'Bolso Cajita Guess Calidad Premium',
    price: '125,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/730615/1711211169photo1710820173%20(4).jpeg'
},
{
    name: 'Bolso Louis Vuiton S15',
    price: '69,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/747444/1712177577WhatsApp%20Image%202024-03-26%20at%2011.58.16%20AM.jpeg'
},
{
    name: 'Bolso viajero',
    price: '59,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/902809/1717189981Bolso%20Viajero.jpeg'
},
{
    name: 'Bolso Pañalera Tipo Morral',
    price: '77,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/616205/1706199938WhatsApp%20Image%202024-01-25%20at%2010.32.34%20AM.jpeg'
},
{
    name: 'Bolso Playero Y Manos Libres Lv',
    price: '129,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/632554/1707091424WhatsApp%20Image%202022-11-11%20at%2010.34.38%20PM%20(4).jpeg'
},
{
    name: 'Bolso Playero Y Manos Libres Lv',
    price: '129,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/632554/1707091424WhatsApp%20Image%202022-11-11%20at%2010.34.38%20PM%20(2).jpeg'
},
{
    name: 'Bolso Playero Y Manos Libres Lv',
    price: '129,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/632554/1707091424WhatsApp%20Image%202022-11-11%20at%2010.34.38%20PM%20(3).jpeg'
},
{
    name: 'Bolso Playero Y Manos Libres Lv',
    price: '129,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/632554/1707091424WhatsApp%20Image%202022-11-11%20at%2010.34.38%20PM%20(1).jpeg'
},
{
    name: 'Bolso Playero Y Manos Libres Lv',
    price: '129,000',
    description: 'Variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/632554/1707091424WhatsApp%20Image%202022-11-11%20at%2010.34.38%20PM.jpeg'
},
{
    name: 'Bolso Dama Mano Libres Marc Jacobs',
    price: '68,000',
    description: 'COLORES DISPONIBLES: BLANCO, ROSADO Y MORADO',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/850388/1715288554PhotoRoom_20240203_000557.JPG'
},
{
    name: 'Bolso Cartera Para Dama Gla 2320',
    price: '119,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/376567/17018735301701873530_CHO9038.jpg'
},
{
    name: 'Gorra Casa Blanca',
    price: '49,000',
    description: 'Beige y negra',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/760391/1712603719WhatsApp%20Image%202024-03-11%20at%2010.34.53%20(1).jpeg'
},
{
    name: 'Gorra Mexicana Jalisco',
    price: '58,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/902099/1717170018WhatsApp%20Image%202024-05-31%20at%2010.26.51%20AM.jpeg'
},
{
    name: 'Adidas Ultra Boost',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713317/1710518440WhatsApp%20Image%202024-03-15%20at%2010.56.42%20AM.jpeg'
},
{
    name: 'Adidas Ultra Boost',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713317/1710518440WhatsApp%20Image%202024-03-15%20at%2010.56.42%20AM%20(2).jpeg'
},
{
    name: 'Adidas Ultra Boost',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713317/1710518440WhatsApp%20Image%202024-03-15%20at%2010.56.42%20AM%20(1).jpeg'
},
{
    name: 'Nike Comando Negro Blanco',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/70853/17030250961703025096nike-comando-blanco-negro-jhoan-mena-1112153045.jpg'
},
{
    name: 'Tenis Nike Dunk Dama',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/328277/17018814701701881470WhatsApp%20Image%202023-07-23%20at%2010.00.37%20PM.jpeg'
},
{
    name: 'Tenis Nike Dunk Dama',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/328277/17018814691701881469WhatsApp%20Image%202023-07-23%20at%2010.00.35%20PM.jpeg'
},
{
    name: 'Nike Botin Jordan Retro 1 Negro',
    price: '99,000',
    description: 'talla desde la 35 hasta la 43',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/70847/1710968561WhatsApp%20Image%202024-03-20%20at%204.59.57%20PM%20(1).jpeg'
},
{
    name: 'Nike Runnin Llavero Gris',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/67857/17030712951703071295WhatsApp%20Image%202022-07-15%20at%2012.51.57%20PM%20(1).jpeg'
},
{
    name: 'Tenis Nike Running V2k Dama',
    price: '99,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/713856/17105310125-65f495e62fae7_5_upscaled_by_dgb_lol__Balanced.jpg'
},
{
    name: 'Tenis Nike Gt Zoom Caballero',
    price: '129,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/580196/1712428108WhatsApp%20Image%202024-04-05%20at%205.45.55%20PM.jpeg'
},
{
    name: 'Nike Winflo 9 Blanco Rosa Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/363535/17018755431701875543WhatsApp%20Image%202023-08-21%20at%2010.08.37%20PM.jpeg'
},
{
    name: 'Nike comando blanco',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/70851/17023897621702389762O2ZDaPMz1XSQxnydA7yDibXus28JcUst9aw1H3Lv.jpeg'
},
{
    name: 'Nike Comando Full Negro',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/70852/17030250961703025096nike-comando-negro-jhoan-mena-1043304441.jpg'
},
{
    name: 'Conjunto Dritfit Nike',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/902841/17171906289fb00d5d-603c-495a-a9fb-444de773005d.jpg'
},
{
    name: 'Nike Air 4',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/391107/17018717981701871798Sin%20ti%CC%81tulo%20(1080%20%C3%97%201080%C2%A0px)%20-%205.PNG'
},
{
    name: 'Nike Air 4',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/391107/17018717991701871799Sin%20ti%CC%81tulo%20(1080%20%C3%97%201080%C2%A0px)%20-%207.PNG'
},
{
    name: 'Nike Air 4',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/391107/17018717981701871798Sin%20ti%CC%81tulo%20(1080%20%C3%97%201080%C2%A0px)%20-%206.PNG'
},
{
    name: 'Nike Air 4',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/391107/17018717991701871799Sin%20ti%CC%81tulo%20(1080%20%C3%97%201080%C2%A0px)%20-%208.PNG'
},
{
    name: 'Nike Retro 1',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623198/1706561088for%206.jpg'
},
{
    name: 'Nike Retro 1',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623198/1706561088for%203.jpg'
},
{
    name: 'Nike Retro 1',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623198/1706561088for%202.jpg'
},
{
    name: 'Nike Retro 1',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623198/1706561088for%205.jpg'
},
{
    name: 'Nike Retro 1',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623198/1706561088FOR%204.jpg'
},
{
    name: 'Nike Retro 1',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/623198/1706561088kik.jpg'
},
{
    name: 'Tenis Nike 270 Blanco',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/103089/170232234017023223400rhQYNOC68cvlbpQMRkDQV5rtT7KeM5g5bvqd7Zu.jpeg'
},
{
    name: 'Deportivo Nike React',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/903534/171727279459322720-2db2-48a0-98a4-5299f9878e4c.jpg'
},
{
    name: 'Deportivo Nike React',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/903534/171780047901435ac3-2220-434f-abf0-261900bb393d.jpg'
},
{
    name: 'Nike Fly Dama',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/689649/1709648814WhatsApp%20Image%202024-03-04%20at%208.21.18%20AM.jpeg'
},
{
    name: 'Nike Fly Dama',
    price: '89,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/689649/1709648814WhatsApp%20Image%202024-03-04%20at%208.21.20%20AM%20(1).jpeg'
},
{
    name: 'Nike Tavas Blanco',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/70846/17030223641703022364NVzb9r97aZrjsSAfXsP5h0qF7PEhCptcxPFSKTpc.jpeg'
},
{
    name: 'Nike Runnin Llavero Negro',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/67855/17030712951703071295WhatsApp%20Image%202022-07-15%20at%2012.51.57%20PM%20(3).jpeg'
},
{
    name: 'Nike Trebol Negro',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/363739/17018755381701875538WhatsApp%20Image%202023-08-21%20at%2011.27.20%20PM%20(2).jpeg'
},
{
    name: 'Calzado Dama Nike Zoom - X Ref 711',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/443071/1697503836PhotoRoom-20231007-120210.jpg'
},
{
    name: 'Calzado Dama Nike Zoom - X Ref 711',
    price: '89,000',
    description: 'variedad de colores',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/443071/1707359139IMG_6832.JPG'
},
{
    name: 'Nike Air Runnin.',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/205949/1708436545DSC_1264.jpg'
},
{
    name: 'Nike Air Runnin.',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/205949/1708436547DSC_0314.jpg'
},
{
    name: 'Nike Air Runnin.',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/205949/1708436547DSC_0277.jpg'
},
{
    name: 'Nike Air Runnin.',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/205949/1708436547DSC_0314.jpg'
},
{
    name: 'Bota Nike Retro',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/815783/1714431445d0f3004f-b3e3-4dc6-a077-f74a5272ab97.jpg'
},
{
    name: 'Bota Nike',
    price: '99,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/899368/1717082197ae13ca82-e29d-4353-8197-82290be1c5f1.jpg'
},
{
    name: 'Tenis Nike Zoom Invencible Unisex',
    price: '89,000',
    description: 'Prepárate para descubrir las nuevas Nike ZoomX, la solución perfecta para corredores que buscan máxima amortiguación y retorno de energía.',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/694880/17098203539E3FE2B5-3BA8-491B-9497-16E996F5C321.jpg'
},
{
    name: 'Nike Air 4',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/391107/170866247016967225032.png'
},
{
    name: 'Nike Air 4',
    price: '89,000',
    description: '',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/391107/1710261139NIKERUNN_720x720_crop_center.webp'
},
{
    name: 'Adidas Trebol Blanco Dama',
    price: '89,000',
    description: 'Talla desde la 35 hasta la 40',
    image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/319635/17018822071701882207WhatsApp%20Image%202023-07-16%20at%2010.23.51%20PM%20(1).jpeg'
            },
            {
                
        "name": "Tapete Antideslizante Absorbente Combo",
        "price": "49,000",
        "description": "Tapete de PVC y terciopelo técnico, con fuerte antideslizante y absorción de agua rápida. Ideal para baños, cocinas, lavanderías, y más. Alta calidad, duradero y fácil de limpiar. Disponible en dos tamaños: 120x40 cm y 60x40 cm. Colores y patrones modernos que combinan con cualquier decoración.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/565196/17027618531702498479Tapete%20de%20cocina08.jpg"
    },
    {
        "name": "Tapete Alfombra Para Baño Absorbente",
        "price": "37,000",
        "description": "Alfombra de baño super absorbente y antideslizante. Hecha de material suave y ecológico, con superficie que absorbe la humedad y capa de espuma que evapora rápidamente. Fácil de lavar y duradera. Medidas: 40x60 cm. Incluye 1 alfombrilla. Garantía de 30 días por defectos de fábrica.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/257672/17018993201701899320Tapete%20De%20Ba%C3%B1o%20Super%20Absorbente%20Y%20Antideslizante%20A.jpg"
    },
    {
        "name": "Tapete Mágico Ultra Absorbente 30 40",
        "price": "35,000",
        "description": "Tapete de cocina absorbente de caucho natural, súper absorbente y de secado rápido. Resistente a manchas, aceite y calor. Ideal para escurrir platos sin desbordar agua. Material ultra absorbente y antideslizante. Medidas: 30x40 cm. Colores: Negro, Azul, Beige. Incluye 1 tapete.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/884774/1716561673Tapete-absorbente-cocina-FK23D-288.11.jpg"
    },
    {
        "name": "Soporte Base Computador Portátil Ajustable",
        "price": "36,000",
        "description": "Soporte para laptop con 7 configuraciones de altura, protege tus ojos y mejora la postura. Compacto, ligero y portátil, soporta hasta 20 kg. Almohadillas antideslizantes y funda protectora incluidas. Garantía por defectos de fábrica si se devuelve en su empaque original.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/589038/1704838924BASE%20AJUSTABLE%20PARA%20PC.png"
    },
    {
        "name": "Soporte De Toallas Cocina Baño",
        "price": "32,000",
        "description": "Soporte de toallas fácil de instalar sin perforaciones. Polos giratorios de acero inoxidable y ABS para mayor durabilidad. Adecuado para uso comercial y doméstico. Diseño elegante que añade estilo al ambiente.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/212389/17023012281702301228Screenshot_176.jpg"
    },
    {
        "name": "Mini Masajeador De Cuello Eléctrico",
        "price": "29,000",
        "description": "Masajeador eléctrico de cuello con 6 modos y niveles de masaje. Compacto y portátil, funciona con 2 pilas AAA. Capacidad de batería de 120 mAh. Fácil de usar, ajustable a diferentes necesidades. Ideal para aliviar tensiones musculares.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/624286/1706630140MASAJEADOR%20DE%20CEULLO%202.webp"
    },
    {
        "name": "Masajeador De Cuello Con Electrodos",
        "price": "49,000",
        "description": "Masajeador de cuello recargable con 3 modalidades: calor infrarrojo, ultrasonido y electrofrecuencia. Tecnología de ajuste en 3D. Incluye collar masajeador, cable y 2 electroestimuladores. Dimensiones: 16x14x4.5 cm. Garantía de 10 días por defectos de fábrica.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/918148/1718726800113574820_1.avif"
    },
    {
        "name": "Masajeador De Cuello Eléctrico Alivia Dolor",
        "price": "89,000",
        "description": "Masajeador eléctrico para cuello, espalda y hombros con 9 niveles de fuerza y función de auto cierre de seguridad. Funcionalidad de masaje multidireccional. Tensión nominal: 220V, potencia: 55W. Garantía del vendedor: 1 mes.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/415538/1695853630D_NQ_NP_2X_999480-MCO50742711359_072022-F.webp"
    },
    {
        "name": "Power Bank Super Cargador",
        "price": "79,000",
        "description": "Power bank con convertidor USB de carga rápida. Incluye 2 puertos USB 3.0 y 1 puerto tipo C. Capacidad de 6700 mAh. Pantalla indicadora y carga inalámbrica rápida. Garantía: 10 días por pedido incompleto o roto, 30 días por mal funcionamiento.",
        "image": "https://d39ru7awumhhs2.cloudfront.net/colombia/products/850687/1715290627CARGADOR1.JPG"
    },
    {
                name: 'Adidas Fresh Negro Naranja Caballero',
                price: '89,000',
                description: 'Tallas: 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284335/17018949181701894918WhatsApp%20Image%202023-06-12%20at%206.09.43%20PM.jpeg'
            },
            {
                name: 'Adidas 2k Blanco Azul Caballero',
                price: '89,000',
                description: 'Tallas: 37 38 39 40 41 42 43',
                image: 'https://d39ru7awumhhs2.cloudfront.net/colombia/products/284302/17018822161701882216L6cf4BmoN0nQSiY96hojYNJVjrFPsWYe6Lh4Wzzt.jpg'
            }
        ];

        const productContainer = document.getElementById('product-list');

        function renderProducts(products) {
            productContainer.innerHTML = '';
            products.forEach((product, index) => {
                const productElement = document.createElement('div');
                productElement.className = 'product';
                productElement.innerHTML = `
                    <img src="${product.image}" alt="${product.name}">
                    <h2 contenteditable="true" data-index="${index}" data-attr="name">${product.name}</h2>
                    <p class="price" contenteditable="true" data-index="${index}" data-attr="price">${product.price}</p>
                    <p contenteditable="true" data-index="${index}" data-attr="description">${product.description}</p>
                    <button onclick="editProduct(${index})">Envío gratis</button>
                    <button onclick="buyProduct('${product.name}')">Comprar</button>
                `;
                productContainer.appendChild(productElement);
            });
        }

        document.getElementById('search').addEventListener('input', (e) => {
            const query = e.target.value.toLowerCase();
            const filteredProducts = products.filter(product => 
                product.name.toLowerCase().includes(query)
            );
            renderProducts(filteredProducts);
        });

        renderProducts(products);

        function editProduct(index) {
            const password = prompt('Ingrese la contraseña para editar:');
            if (password === '12345') {
                const newName = document.querySelector(`[data-attr="name"][data-index="${index}"]`).innerText;
                const newPrice = document.querySelector(`[data-attr="price"][data-index="${index}"]`).innerText;
                const newDescription = document.querySelector(`[data-attr="description"][data-index="${index}"]`).innerText;

                products[index].name = newName;
                products[index].price = newPrice;
                products[index].description = newDescription;

                renderProducts(products);
            } else {
                alert('Contraseña incorrecta. No se pueden realizar cambios.');
            }
        }

        function buyProduct(productName) {
            window.location.href = `https://api.whatsapp.com/send?phone=+3206572598&text=*Hola%20quiero%20que%20me%20env%C3%ADes%20este%20producto*%20${productName}%20*aqu%C3%AD%20te%20env%C3%ADo%20mi%20nombre%20y%20direcci%C3%B3n%20completa*`;
        }
    </script>
</body>
</html>


