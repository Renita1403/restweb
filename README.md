# Ex.07 Restaurant Website
## Date:

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Delicious Restaurant</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    body {
      background: #fffaf3;
      color: #333;
      line-height: 1.6;
    }

    /* Navigation Bar */
    header {
      background: #ff6347;
      padding: 15px 10%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header h1 {
      color: #fff;
      font-size: 28px;
      font-weight: bold;
    }

    nav ul {
      display: flex;
      list-style: none;
    }

    nav ul li {
      margin: 0 15px;
    }

    nav ul li a {
      color: #fff;
      text-decoration: none;
      font-size: 16px;
      transition: 0.3s;
    }

    nav ul li a:hover {
      color: #ffd580;
    }

    /* Hero Section */
    .hero {
      height: 90vh;
      background: url("https://images.unsplash.com/photo-1504674900247-0877df9cc836") center/cover no-repeat;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #fff;
      position: relative;
    }

    .hero::after {
      content: "";
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.5);
    }

    .hero-content {
      position: relative;
      z-index: 1;
    }

    .hero h2 {
      font-size: 48px;
      margin-bottom: 15px;
    }

    .hero p {
      font-size: 18px;
      margin-bottom: 20px;
    }

    .btn {
      display: inline-block;
      padding: 12px 25px;
      background: #ff6347;
      color: #fff;
      text-decoration: none;
      border-radius: 25px;
      transition: 0.3s;
    }

    .btn:hover {
      background: #ffd580;
      color: #333;
    }

    /* About Section */
    .about {
      padding: 60px 10%;
      text-align: center;
    }

    .about h2 {
      font-size: 32px;
      margin-bottom: 20px;
      color: #ff6347;
    }

    .about p {
      font-size: 18px;
      color: #555;
      max-width: 700px;
      margin: auto;
    }

    /* Menu Section */
    .menu {
      background: #fff3e6;
      padding: 60px 10%;
      text-align: center;
    }

    .menu h2 {
      font-size: 32px;
      margin-bottom: 30px;
      color: #ff6347;
    }

    .menu-items {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 25px;
    }

    .menu-card {
      background: #fff;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: 0.3s;
    }

    .menu-card:hover {
      transform: translateY(-8px);
    }

    .menu-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .menu-card h3 {
      margin: 15px 0;
      color: #333;
    }

    .menu-card p {
      color: #666;
      font-size: 14px;
      padding: 0 15px 15px;
    }

    /* Reservation Section */
    .reservation {
      padding: 60px 10%;
      background: #fdf6f0;
      text-align: center;
    }

    .reservation h2 {
      font-size: 32px;
      margin-bottom: 20px;
      color: #ff6347;
    }

    .reservation p {
      margin-bottom: 30px;
      color: #444;
    }

    form {
      max-width: 600px;
      margin: auto;
      background: #fff;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      text-align: left;
    }

    form label {
      display: block;
      margin-bottom: 8px;
      font-weight: 600;
      color: #333;
    }

    form input, form select {
      width: 100%;
      padding: 10px;
      margin-bottom: 20px;
      border-radius: 8px;
      border: 1px solid #ccc;
      outline: none;
      font-size: 15px;
    }

    form input:focus, form select:focus {
      border-color: #ff6347;
    }

    form button {
      width: 100%;
      padding: 12px;
      background: #ff6347;
      border: none;
      color: #fff;
      font-size: 16px;
      border-radius: 25px;
      cursor: pointer;
      transition: 0.3s;
    }

    form button:hover {
      background: #ffd580;
      color: #333;
    }

    /* Contact Section */
    .contact {
      padding: 60px 10%;
      background: #ff6347;
      color: #fff;
      text-align: center;
    }

    .contact h2 {
      margin-bottom: 20px;
      font-size: 32px;
    }

    .contact p {
      margin-bottom: 10px;
    }

    footer {
      background: #222;
      color: #fff;
      text-align: center;
      padding: 15px 0;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <h1>Delicious</h1>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#reservation">Reservation</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero" id="hero">
    <div class="hero-content">
      <h2>Welcome to Delicious</h2>
      <p>Experience the best food with a touch of love</p>
      <a href="#menu" class="btn">View Menu</a>
    </div>
  </section>

  <!-- About -->
  <section class="about" id="about">
    <h2>About Us</h2>
    <p>At Delicious Restaurant, we serve freshly prepared meals using the finest ingredients. Our chefs craft every dish with passion to bring you a delightful dining experience.</p>
  </section>

  <!-- Menu -->
  <section class="menu" id="menu">
    <h2>Our Menu</h2>
    <div class="menu-items">
      <div class="menu-card">
        <img src="https://images.unsplash.com/photo-1600891964092-4316c288032e" alt="Pizza">
        <h3>Italian Pizza</h3>
        <p>Cheesy, crispy, and topped with fresh ingredients.</p>
      </div>
      <div class="menu-card">
        <img src="https://images.unsplash.com/photo-1606755962773-0e72c3a0f56d" alt="Burger">
        <h3>Juicy Burger</h3>
        <p>Grilled to perfection with a side of fries.</p>
      </div>
      <div class="menu-card">
        <img src="https://images.unsplash.com/photo-1546069901-ba9599a7e63c" alt="Pasta">
        <h3>Classic Pasta</h3>
        <p>A perfect blend of sauces and spices.</p>
      </div>
    </div>
  </section>

  <!-- Reservation -->
  <section class="reservation" id="reservation">
    <h2>Reserve Your Table</h2>
    <p>Fill out the form below to book your table in advance.</p>
    <form>
      <label for="name">Full Name</label>
      <input type="text" id="name" placeholder="Enter your name" required>

      <label for="phone">Phone Number</label>
      <input type="tel" id="phone" placeholder="Enter your phone number" required>

      <label for="date">Date</label>
      <input type="date" id="date" required>

      <label for="time">Time</label>
      <input type="time" id="time" required>

      <label for="guests">Number of Guests</label>
      <select id="guests" required>
        <option value="">Select Guests</option>
        <option>1 Person</option>
        <option>2 People</option>
        <option>3 People</option>
        <option>4 People</option>
        <option>5+ People</option>
      </select>

      <button type="submit">Book Now</button>
    </form>
  </section>

  <!-- Contact -->
  <section class="contact" id="contact">
    <h2>Contact Us</h2>
    <p>📍 123 Food Street, Tasty City</p>
    <p>📞 +91 9876543210</p>
    <p>✉ info@delicious.com</p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Delicious Restaurant | All Rights Reserved</p>
  </footer>

</body>
</html>
```
## OUTPUT:
![alt text](<Screenshot 2025-10-02 102344.png>)
![alt text](<Screenshot 2025-10-02 102401.png>)
![alt text](<Screenshot 2025-10-02 102418.png>)
![alt text](<Screenshot 2025-10-02 102432.png>)



## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
