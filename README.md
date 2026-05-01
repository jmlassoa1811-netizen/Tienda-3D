

        /* TITULOS */
        h1, h2 { color: #00e5ff; }

        h1 {
            font-size: 60px;
            font-family: 'Segoe UI', sans-serif;
            text-shadow: 0 0 10px rgba(0,229,255,0.5);
        }

        h2 { 
            font-size: 32px;
            text-shadow: 0 0 8px rgba(0,229,255,0.3);
        }

        /* BODY */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;

            background: radial-gradient(circle at top center, 
            rgba(0, 229, 255, 0.12), 
            rgba(0, 0, 0, 0.95) 50%),
            linear-gradient(135deg, #0f2027, #203a43, #000000);

            color: #e6f1ff;
        }

        /* TABS */
        .tabs { 
            margin: 30px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;; }

        .tabs button {
            padding: 15px 25px;
            margin: 5px;
            border-radius: 12px;
            border: 1px solid rgba(0,229,255,0.2);
            background: linear-gradient(135deg, #0f2027, #203a43);
            color: #00e5ff;
            font-weight: bold;
            cursor: pointer;
            font-size: 16px;
            transition: 0.3s;
            margin: 30px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
        }

        .tabs button:hover {
            background: linear-gradient(135deg, #203a43, #2c5364);
            box-shadow: 0 0 10px rgba(0,229,255,0.4);
        }

        /* CONTENEDOR PRODUCTOS */
        #productosFiguras, 
        #productosLlaveros, 
        #productosJuguetes {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-bottom: 50px;
        }

        /* TARJETAS */
        .producto {
            background: linear-gradient(145deg, #2c3e50, #3b536b);
            margin: 25px auto;
            padding: 20px;
            border-radius: 18px;
            color: #e6f1ff;
            width: 280px;

            box-shadow: 
            0 10px 25px rgba(0,0,0,0.6),
            inset 0 1px 0 rgba(255,255,255,0.05);

            border: 1px solid rgba(255,255,255,0.08);
            backdrop-filter: blur(8px);

            transition: all 0.3s ease;
        }

        .producto:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 
            0 20px 40px rgba(0,0,0,0.8),
            0 0 20px rgba(0, 229, 255, 0.25);
        }

        /* DESCRIPCION */
        .descripcion {
            color: #cce7ff;
            font-family: 'Segoe UI', sans-serif;
        }

        /* PRECIO */
        .precio {
            color: #00ff9f;
            font-size: 20px;
            font-weight: bold;
        }

        /* BOTONES GENERALES */
        button {
            background: linear-gradient(135deg, #00e5ff, #00bcd4);
            color: #002b36;
            padding: 8px 16px;
            border: none;
            border-radius: 20px;
            margin: 5px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            transform: scale(1.1);
            box-shadow: 0 0 10px rgba(0,229,255,0.6);
        }

        /* IMAGENES */
        .producto img {
            display: block;
            margin: auto;
            border-radius: 12px;
        }

        /* INFO ENVIO */
        .info-envio {
            color: #cce7ff;
            font-size: 18px;
            margin: 15px 0;
            font-weight: bold;
            text-align: center;
        }

        /* CARRITO */
        #sidebarCarrito {
            position: fixed;
            top: 0;
            right: -360px;
            width: 360px;
            height: 100%;
            background: #1c2a38;
            color: white;
            padding: 20px;
            transition: right 0.3s ease;
            z-index: 1000;
            overflow-y: auto;
        }

        #abrirCarrito {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 12px 16px;
            border-radius: 12px;
            border: none;
            background: linear-gradient(135deg, #0f2027, #203a43);
            color: #00e5ff;
            font-weight: bold;
            cursor: pointer;
            z-index: 1100;
        }

        /* INPUTS */
        input, select {
            padding: 10px;
            margin: 5px;
            border-radius: 10px;
            border: none;
            width: 90%;
        }

        .carrito-item {
            margin-bottom: 15px;
            border-bottom: 1px solid #ccc;
            padding-bottom: 10px;
        }

        #cerrarCarrito {
            background-color: #ff6b6b;
            color: white;
            margin-top: 20px;
        }

        /* LOADING */
        .loading {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: rgba(0,0,0,0.8);
            color: white;
            padding: 20px;
            border-radius: 10px;
            z-index: 2000;
        }

        /* LOGO */
        .logo-titulo {
            display: flex;
            align-items: center;
            justify-content: center; 
            gap: 15px;
            color: #00e5ff; 
            font-size: 70px;
            font-family: 'Segoe UI', sans-serif;
            text-shadow: 0 0 12px rgba(0,229,255,0.5);
            text-align: center;
        }

        .logo-img {
            width: 110px;  
            height: 110px;
            object-fit: contain;
        }

</style>
</head>

<body>

<h1 class="logo-titulo">
    <img src="Logo.png"  class="logo-img">
    JS 3D
</h1>

<p class="info-envio">
💰 Pago por Nequi<br>
Diseños personalizados al WhatsApp<br>
3007024381<br>

</p>

<div class="tabs">
    <button onclick="mostrarTab('figuras')">Figuras</button>
    <button onclick="mostrarTab('llaveros')">Llaveros</button>
    <button onclick="mostrarTab('juguetes')">Juguetes</button>
</div>

<button id="abrirCarrito">🛒 Carrito</button>

<!-- FIGURAS -->
<div id="figuras">
    <div id="productosFiguras">
        <div class="producto">
            <h2>Ghost Face</h2>
            <p class="precio">$15.000</p>
            <p class="descripcion">Altura: 10cm</p>
            <img src="ghostface.png" width="200">
            <button onclick="comprar('Ghost Face',15000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Michael Jackson Thriller</h2>
            <p class="precio">$20.000</p>
            <p class="descripcion">Altura: 10cm</p>
            <img src="michael-thriller.webp" width="200">
            <button onclick="comprar('Michael Jackson Thriller',20000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Michael Jackson Earth Song</h2>
            <p class="precio">$20.000</p>
            <p class="descripcion">Altura: 10cm</p>
            <img src="michael-earth-song.jpg" width="200">
            <button onclick="comprar('Michael Jackson Earth Song',20000)">Comprar</button>
        </div>
        
        
        <div class="producto">
            <h2>Skeleton</h2>
            <p class="precio">$13.000</p>
            <p class="descripcion">Altura: 10cm</p>
            <img src="skeleton.png" width="280">
            <button onclick="comprar('Skeleton',13000)">Comprar</button>
        </div>

        <div class="producto">
            <h2>Planterman</h2>
            <p class="precio">$18.000</p>
            <p class="descripcion">Altura: 11cm</p>
            <img src="planterman.png" width="250">
            <button onclick="comprar('Planterman',18000)">Comprar</button>
        </div>

        <div class="producto">
            <h2>Araña Articulada</h2>
            <p class="precio">$15.000</p>
            <p class="descripcion">Altura: 11cm</p>
            <img src="arana-articulada.png" width="250">
            <button onclick="comprar('Araña Articulada',15000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Soporte para audifonos</h2>
            <p class="precio">$15.000</p>
            <p class="descripcion">Altura: 11cm</p>
            <img src="soporte-para-audifonos.png" width="250">
            <button onclick="comprar('Soporte para audifonos',15000)">Comprar</button>
        </div>
    </div>
</div>

<!-- LLAVEROS -->
<div id="llaveros" style="display:none;">
    <div id="productosLlaveros">
        <div class="producto">
            <h2>Mini Dragon</h2>
            <p class="precio">$5.000</p>
            <p class="descripcion">Altura: 4cm</p>
            <img src="mini-dragon-articulado.png" width="200">
            <button onclick="comprar('Mini Dragon',5000)">Comprar</button>
        </div>

        <div class="producto">
            <h2>Baby Shark</h2>
            <p class="precio">$8.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="babysharck.png" width="200">
            <button onclick="comprar('Baby Shark',8000)">Comprar</button>
        </div>

        <div class="producto">
            <h2>Tortuga</h2>
            <p class="precio">$8.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="tortuga.png" width="200">
            <button onclick="comprar('Tortuga',8000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Calavera callejera</h2>
            <p class="precio">$8.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="calavera-callejera.png" width="200">
            <button onclick="comprar('Calavera callejera',8000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Falxias de Graduacao</h2>
            <p class="precio">$8.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="falxias-de-graduacao.png" width="200">
            <button onclick="comprar('Falxias de Graduacao ',8000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Fantasmin</h2>
            <p class="precio">$5.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="fantasmin.png" width="200">
            <button onclick="comprar('Fantasmin ',5000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Panda Callejero</h2>
            <p class="precio">$8.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="panda-callejero.png" width="200">
            <button onclick="comprar('Panda Callejero',8000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Cat</h2>
            <p class="precio">$7.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="cat.png" width="200">
            <button onclick="comprar('Cat',7000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Pandita</h2>
            <p class="precio">$7.000</p>
            <p class="descripcion">Altura: 3cm</p>
            <img src="panda-tejido.png" width="200">
            <button onclick="comprar('Pandita',7000)">Comprar</button>
        </div>
    </div>
</div>

<!-- JUGUETES -->
<div id="juguetes" style="display:none;">
    <div id="productosJuguetes">
        <div class="producto">
            <h2>Flexi Rex</h2>
            <p class="precio">$10.000</p>
            <p class="descripcion">Altura: 8cm</p>
            <img src="flexi -rex.png" width="200">
            <button onclick="comprar('Flexi Rex',10000)">Comprar</button>
        </div>

        <div class="producto">
            <h2>Dragon Crystal XL</h2>
            <p class="precio">$35.000</p>
            <p class="descripcion">Altura: 8cm</p>
            <img src="dragon-crisral-xl.png" width="200">
            <button onclick="comprar('Dragon Crystal XL',35000)">Comprar</button>
        </div>

        <div class="producto">
            <h2>Dragon Cristal S</h2>
            <p class="precio">$14.000</p>
            <p class="descripcion">Altura: 8cm</p>
            <img src="dragon-cristal-s.png" width="200">
            <button onclick="comprar('Dragon Crystal S',14000)">Comprar</button>
        </div>
        <div class="producto">
            <h2>Dragon Gusano</h2>
            <p class="precio">$14.000</p>
            <p class="descripcion">Altura: 8cm</p>
            <img src="dragon-gusano.png" width="200">
            <button onclick="comprar('Dragon Gusano',14000)">Comprar</button>
        </div>
    </div>
</div>

<!-- CARRITO -->
<div id="sidebarCarrito">
    <h2>🛍️ Carrito</h2>
    <div id="carritoContenido"><p>No hay productos en el carrito</p></div>
    <h3>Total: $<span id="total">0</span></h3>

    <h3>📋 Datos de envío</h3>
    <input type="text" id="nombre" placeholder="Nombre completo" required>
    <input type="tel" id="numero" placeholder="Número de contacto" required>
    <input type="text" id="direccion" placeholder="Dirección" required>

    <select id="medioPago" required>
        <option value="">Selecciona medio de pago</option>
        <option value="Efectivo">Efectivo</option>
        <option value="Nequi">Nequi</option>
    </select>

    <button onclick="enviarPedido()" style="background-color: #25D366; color: white; margin-top: 20px;">💬 Enviar pedido</button>
    <button id="cerrarCarrito">❌ Cerrar</button>
</div>

<div id="loading" class="loading">
    ⏳ Enviando pedido...
</div>

<script>
// Tu URL de Google Sheets
const GOOGLE_SHEETS_URL = "https://script.google.com/macros/s/AKfycbyGbzV-pnHwpMMdWduU0HfS0plNkcl8XB86WymAy5o5HSqWtch02yOYtvhhR4IOlHHw/exec";

let carrito = {};
let total = 0;

const sidebar = document.getElementById("sidebarCarrito");

document.getElementById("abrirCarrito").onclick = () => sidebar.style.right = "0";
document.getElementById("cerrarCarrito").onclick = () => sidebar.style.right = "-360px";

function mostrarTab(tab){
    document.getElementById("figuras").style.display = "none";
    document.getElementById("llaveros").style.display = "none";
    document.getElementById("juguetes").style.display = "none";
    document.getElementById(tab).style.display = "block";
}

function comprar(nombre, precio){
    if(carrito[nombre]) carrito[nombre].cantidad++;
    else carrito[nombre] = {precio: precio, cantidad: 1};
    actualizarCarrito();
}

function quitar(nombre){
    if(carrito[nombre]){
        carrito[nombre].cantidad--;
        if(carrito[nombre].cantidad <= 0){
            delete carrito[nombre];
        }
        actualizarCarrito();
    }
}

function actualizarCarrito(){
    const cont = document.getElementById("carritoContenido");
    cont.innerHTML = "";
    total = 0;

    if(Object.keys(carrito).length === 0){
        cont.innerHTML = "<p>No hay productos en el carrito</p>";
        document.getElementById("total").innerText = "0";
        return;
    }

    for(let nombre in carrito){
        let item = carrito[nombre];
        total += item.precio * item.cantidad;

        cont.innerHTML += `
        <div class="carrito-item">
            <strong>${nombre}</strong><br>
            Precio: $${item.precio.toLocaleString()} x ${item.cantidad} = $${(item.precio * item.cantidad).toLocaleString()}
            <br>
            <button onclick="comprar('${nombre}', ${item.precio})">➕</button>
            <button onclick="quitar('${nombre}')">➖</button>
        </div>`;
    }

    document.getElementById("total").innerText = total.toLocaleString();
}

// Enviar datos a Google Sheets
async function enviarASheets(datos) {
    try {
        await fetch(GOOGLE_SHEETS_URL, {
            method: "POST",
            mode: "no-cors",
            headers: {
                "Content-Type": "application/json",
            },
            body: JSON.stringify(datos)
        });
        console.log("✅ Datos enviados a Google Sheets");
        return true;
    } catch (error) {
        console.error("❌ Error al enviar a Sheets:", error);
        return false;
    }
}

// Formatear productos para el mensaje
function formatearProductos() {
    let lista = "";
    for(let item in carrito){
        let prod = carrito[item];
        lista += `• ${item} x${prod.cantidad} - $${(prod.precio * prod.cantidad).toLocaleString()}\n`;
    }
    return lista;
}

// Enviar pedido completo
function enviarPedido() {
    const nombre = document.getElementById("nombre").value.trim();
    const numero = document.getElementById("numero").value.trim();
    const direccion = document.getElementById("direccion").value.trim();
    const medioPago = document.getElementById("medioPago").value;

    // Validaciones
    if(!nombre){
        alert("❌ Por favor ingresa tu nombre completo");
        return;
    }
    if(!numero){
        alert("❌ Por favor ingresa tu número de contacto");
        return;
    }
    if(!direccion){
        alert("❌ Por favor ingresa tu dirección");
        return;
    }
    if(!medioPago){
        alert("❌ Por favor selecciona un medio de pago");
        return;
    }
    if(Object.keys(carrito).length === 0){
        alert("❌ El carrito está vacío");
        return;
    }

    // Mostrar loading
    const loading = document.getElementById("loading");
    loading.style.display = "block";

    const productosTexto = formatearProductos();
    
    // Preparar datos para Google Sheets
    const datosSheet = {
        nombre: nombre,
        numero: numero,
        direccion: direccion,
        pago: medioPago,
        total: total,
        productos: productosTexto,
        fecha: new Date().toLocaleString()
    };

    // Enviar a Google Sheets
    enviarASheets(datosSheet);

    // Preparar mensaje para WhatsApp
    let mensajeWhatsApp = "";
    mensajeWhatsApp += "🛍️ *NUEVO PEDIDO - 3D'S* 🛍️%0a";
    mensajeWhatsApp += "%0a";
    mensajeWhatsApp += "👤 *Nombre:* " + nombre + "%0a";
    mensajeWhatsApp += "📱 *Número:* " + numero + "%0a";
    mensajeWhatsApp += "📍 *Dirección:* " + direccion + "%0a";
    mensajeWhatsApp += "💳 *Pago:* " + medioPago + "%0a";
    mensajeWhatsApp += "%0a";
    mensajeWhatsApp += "📦 *PRODUCTOS:*%0a";
    
    // Agregar cada producto
    for(let item in carrito){
        let prod = carrito[item];
        mensajeWhatsApp += "• " + item + " x" + prod.cantidad + " - $" + (prod.precio * prod.cantidad).toLocaleString() + "%0a";
    }
    
    mensajeWhatsApp += "%0a";
    mensajeWhatsApp += "────────────────%0a";
    mensajeWhatsApp += "💰 *TOTAL: $" + total.toLocaleString() + "*%0a";
    mensajeWhatsApp += "%0a";
    mensajeWhatsApp += "🙏 ¡Gracias por tu compra!";

    // Abrir WhatsApp con el mensaje
    const urlWhatsApp = "https://wa.me/573007024381?text=" + mensajeWhatsApp;
    window.open(urlWhatsApp, '_blank');

    // Limpiar después de enviar
    setTimeout(() => {
        loading.style.display = "none";
        
        // Limpiar carrito
        carrito = {};
        total = 0;
        actualizarCarrito();
        
        // Limpiar formulario
        document.getElementById("nombre").value = "";
        document.getElementById("numero").value = "";
        document.getElementById("direccion").value = "";
        document.getElementById("medioPago").value = "";
        
        // Cerrar sidebar
        sidebar.style.right = "-360px";
        
        alert("✅ ¡Pedido enviado con éxito!\n\n📱 Revísalo en WhatsApp\n📊 También quedó registrado en Google Sheets");
    }, 1000);
}
</script>

</body>
</html>
