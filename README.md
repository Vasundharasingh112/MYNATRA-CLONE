<!DOCTYPE html>
<html lang="en">
          <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Myntra Clone</title>
            <style>
                /* Reset some basic styles */
                * {
                    margin: 0;
                    padding: 0;
                    box-sizing: border-box;
                }

                /* Basic layout */
                body {
                    font-family: Arial, sans-serif;
                    line-height: 1.6;
                    background-color: #f4f4f4;
                }

                /* Header styles */
                header {
                    background-color: #1c1c1c;
                    padding: 10px 0;
                }

                nav ul {
                    list-style-type: none;
                    display: flex;
                    justify-content: center;
                }

                nav ul li {
                    margin: 0 15px;
                }

                nav ul li a {
                    color: white;
                    text-decoration: none;
                    font-size: 18px;
                }

                /* Main content styles */
                main {
                    padding: 20px;
                    text-align: center;
                }

                .product-list {
                    margin-top: 20px;
                }

                .products {
                    display: flex;
                    justify-content: center;
                    gap: 20px;
                    flex-wrap: wrap;
                }

                .product {
                    background-color: white;
                    border-radius: 8px;
                    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
                    width: 200px;
                    text-align: center;
                    padding: 10px;
                }

                .product img {
                    width: 100%;
                    border-radius: 8px;
                }

                .product h3 {
                    font-size: 18px;
                    margin-top: 10px;
                }

                .product p {
                    color: #555;
                }

                /* Footer styles */
                footer {
                    background-color: #1c1c1c;
                    color: white;
                    padding: 10px 0;
                    text-align: center;
                }
            </style>
        </head>
        <body>

            <!-- Header Section -->
            <header>
                <nav>
                    <ul>
                        <li><a href="/">Home</a></li>
                        <li><a href="/products">Shop</a></li>
                        <li><a href="/cart">Cart</a></li>
                        <li><a href="/profile">Profile</a></li>
                    </ul>
                </nav>
            </header>

            <!-- Main Content Section -->
            <main>
                <h1>Welcome to Myntra Clone</h1>
                <section class="product-list">
                    <h2>Featured Products</h2>
                    <div class="products">
                        <!-- Products will be dynamically inserted here -->
                    </div>
                </section>
            </main>

            <!-- Footer Section -->
            <!-- <footer>
                <p>&copy; 2025 Myntra Clone. All rights reserved.</p>
            </footer> -->

            <script>
                document.addEventListener('DOMContentLoaded', function () {
                    // Simulating fetching products
                    const products = [
                        { id: 1, name: "Red Dress", price: "$50", image: "https://lazostore.in/cdn/shop/files/E9AB47F7-24A6-4316-A1BD-6C2CB2CD0E53.jpg?v=1711204059&width=1445" },
                        { id: 2, name: "Blue Jeans", price: "$40", image: "https://levi.in/cdn/shop/files/A74550001_1.jpg?v=1727161139" },
                        { id: 3, name: "Leather Shoes", price: "$80", image: "https://www.legwork.in/cdn/shop/products/DSC_2425.jpg?v=1671395751&width=1946" },
                        { id: 4, name: "suit", price: "$60", image: "https://www.powersutra.co/cdn/shop/files/PowerSutra0997final0.jpg?v=1738173413&width=1080"}
                        { id: 5, name: "saree", price: "$100", image: "https://images.meesho.com/images/products/320663609/mm5yf_1200.jpg"}
                    ];

                    const productsContainer = document.querySelector('.products');
                    
                    products.forEach(product => {
                        const productElement = document.createElement('div');
                        productElement.classList.add('product');
                        productElement.innerHTML = \`
                            <img src="\${product.image}" alt="\${product.name}">
                            <h3>\${product.name}</h3>
                            <p>\${product.price}</p>
                        \`;
                        productsContainer.appendChild(productElement);
                    });
                });
            </script>

        </body>
        </html>
    `);
});

 Shop route
app.get('/products', (req, res) => {
   res.send(`
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>Myntra Clone - Shop</title>
            <style>
                /* Same CSS as above for simplicity */
                /* Add the same CSS here... */
            </style>
        </head>
        <body>
            <header>
                <nav>
                    <ul>
                        <li><a href="/">Home</a></li>
                        <li><a href="/products">Shop</a></li>
                        <li><a href="/cart">Cart</a></li>
                        <li><a href="/profile">Profile</a></li>
                    </ul>
                </nav>
            </header>

            <main>
                <h1>Shop Products</h1>
                <div class="products">
                    <!-- Products List (This could be dynamically loaded) -->
                    <div class="product">
                        <img src="https://lazostore.in/cdn/shop/files/E9AB47F7-24A6-4316-A1BD-6C2CB2CD0E53.jpg?v=1711204059&width=1445" alt="Product 1">
                        <h3>Red Dress</h3>
                        <p>$50</p>
                    </div>
                    <div class="product">
                        <img src="https://levi.in/cdn/shop/files/A74550001_1.jpg?v=1727161139" 
                        alt="Product 2">
                        <h3>Blue Jeans</h3>
                        <p>$40</p>
                    </div>
                    <div class="product">
                        <img src="https://www.legwork.in/cdn/shop/products/DSC_2425.jpg?v=1671395751&width=1946"
                         alt="Product 3">
                        <h3>Leather Shoes</h3>
                        <p>$80</p>
                        </div>
                     <div class="product">
                        <img src="https://www.powersutra.co/cdn/shop/files/PowerSutra0997final0.jpg?v=1738173413&width=1080" alt="Product 4">
                        <h4>suit</h4>
                        <p>$60</p>
                        
                    </div>
                     <div class="product">
                        <img src="https://images.meesho.com/images/products/320663609/mm5yf_1200.jpg" 
                         alt="Product 5">
                        <h4>saree</h4>
                        <p>$100</p>
                        
                    </div>
                </div>
            </main>

            <footer>
                <p>&copy; 2025 Myntra Clone. All rights reserved.</p>
            </footer>
        </body>
        </html>
    `);
});

// Cart route
app.get('/cart', (req, res) => {
    res.send('<h1>Your Cart</h1><p>Items in your cart will appear here.</p>');
});

// Profile route
app.get('/profile', (req, res) => {
    res.send('<h1>Your Profile</h1><p>Your account details will appear here.</p>');
});

// Start the server
app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000');
});

