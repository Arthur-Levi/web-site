# web-site
Missão: fazer um web site com catálogo de produtos da l'occitane

HTML:
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Oásis da Pele</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Cabeçalho com Links de Navegação -->
    <header class="header">
        <div class="container">
            <h1>Oásis da Pele</h1>
            <nav class="nav">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#promocoes">Promoções</a></li>
                    <li><a href="#produtos">Produtos</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Carrossel de Banners -->
    <section class="carousel">
        <div class="carousel-container">
            <div class="carousel-slide">
                <img src="https://br.loccitaneaubresil.com/dw/image/v2/BGNF_PRD/on/demandware.static/-/Library-Sites-LoccitaneBRSharedLibrary/default/dw7ad81ed3/Campanhas%20Caju/Caju%2024'25/02_banner-vitrine-caju-(com-cta)-1920x727-V2.gif" alt="Banner 1">
            </div>
            <div class="carousel-slide">
                <img src="https://br.loccitaneaubresil.com/dw/image/v2/BGNF_PRD/on/demandware.static/-/Library-Sites-LoccitaneBRSharedLibrary/default/dw3b06b59f/Campanhas%20Caju/Caju%2024'25/01_banner%20LP%20caju%20(com%20cta)%201920x727_V2.jpg" alt="Banner 2">
            </div>
            <div class="carousel-slide">
                <img src="banner3.jpg" alt="Banner 3">
            </div>
        </div>
    </section>

    <!-- Produtos em Promoção -->
    <section id="promocoes" class="promotion-section">
        <div class="container">
            <h2>Promoções Especiais</h2>
            <div class="promotion-grid">
                <div class="promotion-card">
                    <img src="promo1.jpg" alt="Promoção 1">
                    <h3>Nome da Promoção 1</h3>
                    <p class="price">De R$ 199,90 por <strong>R$ 149,90</strong></p>
                </div>
            </div>
        </div>
    </section>

    <!-- Produtos -->
    <section id="produtos" class="product-section">
        <div class="container">
            <h2>Nossos Produtos</h2>
            <div class="product-grid">
                <div class="product-card">
                    <img src="produto1.jpg" alt="Produto 1">
                    <h3>Produto 1</h3>
                </div>
                <div class="product-card">
                    <img src="produto2.jpg" alt="Produto 2">
                    <h3>Produto 2</h3>
                </div>
                <!-- Mais produtos... -->
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contato" class="contato-section">
        <div class="container">
            <h2>Contato</h2>
            <p>Entre em contato conosco para mais informações sobre nossos produtos.</p>
        </div>
    </section>

    <!-- Rodapé -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2024 Oásis da Pele. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>

CSS:
/* Global Styles */
body {
    font-family: 'Arial', sans-serif;
    color: #333;
    background-color: #f7f7f7;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}

/* Cabeçalho */
.header {
    background-color: #2c3e50;
    color: #fff;
    padding: 20px 0;
}

.header h1 {
    margin: 0;
    font-size: 2em;
}

.nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
    padding: 0;
    margin-top: 10px;
}

.nav li {
    margin: 0 15px;
    position: relative;
}

.nav a {
    color: #fff;
    text-decoration: none;
    font-size: 1.1em;
    padding: 5px 0;
}

.nav a::after {
    content: '';
    width: 0;
    height: 2px;
    background-color: #f39c12;
    position: absolute;
    bottom: -5px;
    left: 0;
    transition: width 0.3s ease-in-out;
}

.nav a:hover::after {
    width: 100%;
}

/* Carrossel de Banners */
.carousel {
    position: relative;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    overflow: hidden;
}

.carousel-container {
    display: flex;
    transition: transform 0.5s ease-in-out;
}

.carousel-slide {
    min-width: 100%;
    box-sizing: border-box;
}

.carousel-slide img {
    width: 100%;
    height: auto;
}

/* Seções de Produtos */
.promotion-section, .product-section, .contato-section {
    padding: 40px 0;
    background-color: #fff;
}

.promotion-grid, .product-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.promotion-card, .product-card {
    background-color: #fff;
    border: 1px solid #ddd;
    border-radius: 10px;
    width: 200px;
    padding: 15px;
    text-align: center;
    margin-bottom: 20px;
}

.promotion-card img, .product-card img {
    width: 100%;
    height: auto;
    border-radius: 10px;
}

.promotion-card h3, .product-card h3 {
    margin: 10px 0;
    font-size: 1.1em;
}

.price {
    font-size: 1.4em;
    color: #e74c3c;
    margin-bottom: 15px;
}

/* Rodapé */
.footer {
    background-color: #2c3e50;
    color: #fff;
    text-align: center;
    padding: 15px 0;
}

.footer p {
    margin: 0;
}
