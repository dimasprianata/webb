<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DIMAS PRIANATA ABI 1 (209240019)</title>
  <link rel="stylesheet" href="styles css.css">
</head>
<body>
  <!-- Header -->
  <header>
    <h1>GARASI DIMAS</h1>
    <nav>
      <a href="#HOME">BERANDA</a>
      <a href="#PRODUK">PRODUK</a>
      <a href="#KERANANG">KERANJANG </a>
      <a href="#KONTAK">KONTAK</a>
    </nav>
  </header>

  <!-- Home -->
  <section id="home" class="hero">
    <h2>WELCOME TO GARASI DIMAS</h2>
    <p>Garasi Yang Berisi Mobil Impian.</p>
  </section>

  <!-- Produk -->
  <section id="produk" class="products">
    <h2></h2>
    <div class="product" data-name="Lamborghni Aventador" data-price="1.000.000">
      <img src="img/lamborghini-aventador-front-angle-low-view-871719.avif" alt="Lamborghini Aventador">
      <h3>LAMBORGHINI AVENTADOR</h3>
      <p>spesifikasi mesin Lamborghini Aventador ini ditenagai dua pilihan mesin Bensin berkapasitas 6498 cc. Aventador tersedia dengan transmisi Otomatis tergantung variannya. Juga, tergantung pilihan dan jenis bahan bakar, konsumsi BBM Aventador mencapai 4.1 kmpl untuk perkotaan, 9.3 kmpl saat menjelajah perjalanan luar kota. Aventador adalah Coupe 2 seater dengan panjang 4780 mm, lebar 2265 mm, wheelbase 2700 mm.

.</p>
      <span>Rp1.000.000</span>
      <button onclick="addToCart('Lamborghni Aventador', 1000000)">Tambah ke Keranjang</button>
    </div>
    <div class="product" data-name="Bugatt" data-price="1.000.001">
      <img src="img/bugati.jfif" alt="Bugatti">
      <h3>BUGATTI</h3>
      <p>mesin W16 8.0 liter quad-turbocharged dengan tenaga maksimal hingga 1.825 hp dan torsi 1.850 Nm. Transmisi yang digunakan adalah otomatis dual-clutch 7-percepatan. Beberapa model Bugatti, seperti Chiron, mampu mencapai kecepatan maksimal 420 km/jam.</p>
      <span>Rp1.000.001</span>
      <button onclick="addToCart('Bugatti',1000001,)">Tambah ke Keranjang</button>
    </div>
    <div class="product" data-name="PAJERO " data-price="18000">
      <img src="img/pero.jfif" alt="PAJERO ">
      <h3>PAJERO</h3>
      <p>mobil impian para anak muda yang mempunyai mesin diesel 4N15 2.4L MIVEC yang bertenaga dan efisien. Kapasitas mesinnya bervariasi antara 2442 cc hingga 2477 cc, menghasilkan tenaga 134 hingga 179 hp.</p>
      <span>Rp100.000.000.000</span>
      <button onclick="addToCart('PAJERO', 100000000000)">Tambah ke Keranjang</button>
    </div>
     <div class="product" data-name="INOVA " data-price="18000">
      <img src="img/inova.jfif" alt="INOVA ">
      <h3>INOVA</h3>
      <p>mobil impian para anak muda Toyota Kijang Innova menawarkan beberapa varian dengan spesifikasi berbeda, baik dari segi mesin, transmisi, dan fitur. Varian Innova 2.0 M/T (manual) hadir denganmesin bensin 1 TR-FE 4-silinder 16-valve DOHC dengan Dual VVT-i (1998 cc) atau mesin diesel 2GD-FTV 4-silinder 16-valve DOHC dengan VNT Intercooler (2393 cc). Innova juga tersedia dengan transmisi otomatis (A/T). </p>
      <span>Rp90.000.000.000</span>
      <button onclick="addToCart('INOVA', 900000000000)">Tambah ke Keranjang</button>
    </div>
  </section>

  <!-- Keranjang -->
  <section id="keranjang">
    <h2>Keranjang Anda</h2>
    <ul id="cart-list"></ul>
    <p>Total: <span id="cart-total">Rp 0</span></p>
    <button onclick="checkout()">Checkout</button>
  </section>

  <!-- Tentang Kami -->
  <section id="kontak">
    <h2> </p>
  </section>

  <script src="scripts.js"></script>
</body>
</html> 
<link rel="stylesheet" href="styles css.css"

 <script>
</body>
</html>
<!-- Contoh Footer Menu -->
<footer class="site-footer">
    <div class="footer-container">
        <div class="footer-column">
            </ul>
        </div> 

        <div class="footer-column">
            <h4>BANTUAN</h4>
            <ul>
                <li><a href="https://wa.wizard.id/7befcb">KONTAK KAMI</a></li>
            </ul>
        </div>

        <div class="footer-column">
            <h4>IKUTI KAMI</h4>
            <ul>
                <li><a href="https://www.tiktok.com/@dimas_prianata?_t=ZS-8vdOcU5cKG2&_r=1"></i> TIKTOK</a></li>
                <li><a href="https://www.instagram.com/dimas_prianata?igsh=MXQ4dnJkNTdnbHYwOQ=="></i> INSTAGRAM</a></li>
            </ul>
        </div>
    </div>

    <div class="footer-bottom">
        <p>&copy; 2025 GARASI DIMAS. All rights reserved.</p>
        <div class="legal-links">
            <a href="/privacy">Kebijakan Privasi</a> | 
            <a href="/terms">Syarat & Ketentuan</a>
        </div>
    </div>
</footer>

<style>

  let cart = [];

function addToCart(name, price) {
  cart.push({ name, price });
  updateCart();
}

function updateCart() {
  const cartList = document.getElementById('cart-list');
  const cartTotal = document.getElementById('cart-total');
  cartList.innerHTML = '';
  let total = 0;

  cart.forEach(item => {
    const li = document.createElement('li');
    li.textContent = `${item.name} - Rp${item.price.toLocaleString()}`;
    cartList.appendChild(li);
    total += item.price;
  });

  cartTotal.textContent = `Rp${total.toLocaleString()}`;
}

function checkout() {
  if (cart.length === 0) {
    alert("Keranjang kosong!");
    return;
  }
  alert("Terima kasih! Pesanan Anda sedang diproses.");
  cart = [];
  updateCart();
}
   body {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
    margin: 0;
    padding: 0;
    background: lab(37.53% 8.26 44.42);
  }
  
  header {
    background-color: #917548;
    color: rgb(0, 0, 0);
    padding: 40px;
    text-align: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
  
  nav a {
    margin: 0 15px;
    color: white;
    text-decoration: center;
    text-align: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
  
  .hero {
    background: hsl(44, 100%, 88%);
    padding: 50px;
    text-align: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
  
  .products {
    display: flex;
    justify-content: space-around;
    padding: 20px;
    flex-wrap: wrap;
    text-align: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
  
  .product {
    background: white;
    border-radius: 8px;
    padding: 15px;
    margin: 10px;
    width: 250px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    text-align: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
  
  .product img {
    width: 100%;
    height: auto;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
     
  #keranjang {
    padding: 20px;
    background-color: #fff;
    text-align: center;
  }
  
  button {
    background-color: #f0c404;
    color: white;
    border: none;
    padding: 10px;
    margin-top: 10px;
    cursor: pointer;
    text-align: center all;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
  }
  /* CSS untuk Footer */
.site-footer {
    background-color: lab(37.53% 8.26 44.42);
    color: #ecf0f1;
    padding: 40px 0;
    margin-top: 50px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    padding: 0 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
}

.footer-column {
    flex: 1;
    margin-right: 30px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
}

.footer-column h4 {
    color: rgb(238, 241, 243);
    margin-bottom: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
}

.footer-column ul {
    list-style: none;
    padding: 0;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column a {
    color: #ecf0f1;
    text-decoration: none;
}

.footer-column a:hover {
    color: #f8fbfd;
}

.footer-bottom {
    text-align: center;
    margin-top: 4px;
    padding-top: 20px;
    border-top: 1px solid rgb(184, 156, 66);
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
}

.legal-links {
    margin-top: 0px;
}

.legal-links a {
    color: #bdc3c7;
    margin: 0 0px;
}

/* Responsive Design */
@media (max-width: 768px) {
    .footer-container {
        flex-direction: column;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
    }
    
    .footer-column {
        margin-bottom: 30px;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif, sans-serif;
    }
}
