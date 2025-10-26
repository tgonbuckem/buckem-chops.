# buckem-chops.
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Buckem Chops</title>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">
<style>
/* Reset & Base */
* { margin: 0; padding: 0; box-sizing: border-box; }
body { font-family: 'Roboto', sans-serif; color: #fff; background: #111; scroll-behavior: smooth; }
a { text-decoration: none; color: inherit; }

/* Header & Nav */
header { background: #222; padding: 20px; display: flex; justify-content: space-between; align-items: center; position: fixed; width: 100%; z-index: 1000; top: 0; }
header h1 { font-family: 'Oswald', sans-serif; font-size: 2rem; color: #ffcc00; }
nav a { margin-left: 20px; font-weight: 500; color: #fff; transition: color 0.3s; }
nav a:hover { color: #ffcc00; }

/* Hero Section */
.hero { background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1590121560164-4db3ad93d0b1?auto=format&fit=crop&w=1350&q=80') center/cover no-repeat; height: 90vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; overflow: hidden; }
.hero h2 { font-family: 'Oswald', sans-serif; font-size: 3rem; color: #ff0000; margin-bottom: 20px; opacity: 0; transform: translateY(50px); animation: slideUp 1s forwards 0.5s; }
.hero p { font-size: 1.2rem; color: #fff; margin-bottom: 30px; opacity: 0; transform: translateY(50px); animation: slideUp 1s forwards 1s; }
.hero a { background: #ffcc00; color: #111; padding: 15px 30px; font-weight: bold; border-radius: 5px; transition: background 0.3s, transform 0.3s; opacity: 0; transform: translateY(50px); animation: slideUp 1s forwards 1.5s; }
.hero a:hover { background: #e6b800; transform: scale(1.05); }

/* Sections */
section { padding: 100px 20px 60px 20px; max-width: 1200px; margin: 0 auto; opacity: 0; transform: translateY(50px); transition: all 0.8s ease-out; }
section.visible { opacity: 1; transform: translateY(0); }
h3 { font-family: 'Oswald', sans-serif; font-size: 2rem; color: #ffcc00; margin-bottom: 40px; text-align: center; }

/* About */
.about p { font-size: 1.1rem; text-align: center; line-height: 1.6; max-width: 800px; margin: 0 auto; }

/* Services */
.services { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
.service-card { background: #222; padding: 20px; border-radius: 10px; width: 250px; text-align: center; transition: transform 0.3s, box-shadow 0.3s; cursor: pointer; }
.service-card:hover { transform: scale(1.1) rotate(-2deg); box-shadow: 0 0 20px #ffcc00; }
.service-card h4 { font-family: 'Oswald', sans-serif; font-size: 1.5rem; color: #ffcc00; margin-bottom: 10px; }
.service-card p { font-size: 1rem; }

/* Booking Form */
.booking form { max-width: 500px; margin: 0 auto; display: flex; flex-direction: column; gap: 15px; }
.booking input, .booking textarea, .booking select { padding: 10px; border-radius: 5px; border: none; }
.booking button { padding: 15px; background: #ffcc00; color: #111; font-weight: bold; border: none; border-radius: 5px; cursor: pointer; transition: background 0.3s, transform 0.3s; }
.booking button:hover { background: #e6b800; transform: scale(1.05); }

/* Contact */
.contact p { text-align: center; font-size: 1.1rem; margin-bottom: 10px; }

/* Footer */
footer { background: #222; text-align: center; padding: 20px; color: #fff; }
footer a { color: #ffcc00; }

/* Animations */
@keyframes slideUp {
  to { opacity: 1; transform: translateY(0); }
}
</style>
</head>
<body>

<!-- Header -->
<header>
  <h1>Buckem Chops</h1>
  <nav>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#booking">Book</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<!-- Hero Section -->
<section class="hero">
  <h2>Your Street Style Barber</h2>
  <p>Fresh fades, sharp shape ups, and beard grooming – we got you.</p>
  <a href="#booking">Book Now</a>
</section>

<!-- About Section -->
<section id="about" class="about">
  <h3>About Buckem Chops</h3>
  <p>Buckem Chops is where style meets precision. Our mission is to deliver clean cuts, bold styles, and a vibe that matches the streets. We specialize in fades, shape ups, and beard grooming, keeping our clients looking fresh every time.</p>
</section>

<!-- Services Section -->
<section id="services" class="services">
  <h3>Our Services</h3>
  <div class="services">
    <div class="service-card">
      <h4>Fade</h4>
      <p>Sharp and clean fades tailored to your style.</p>
    </div>
    <div class="service-card">
      <h4>Shape Up</h4>
      <p>Perfectly lined edges for a crisp look.</p>
    </div>
    <div class="service-card">
      <h4>Beard</h4>
      <p>Expert beard grooming and shaping.</p>
    </div>
  </div>
</section>

<!-- Booking Section -->
<section id="booking" class="booking">
  <h3>Book an Appointment</h3>
  <form id="bookingForm">
    <input type="text" name="name" placeholder="Your Name" required>
    <input type="email" name="email" placeholder="Your Email" required>
    <input type="tel" name="phone" placeholder="Phone Number" required>
    <select name="service" required>
      <option value="">Select Service</option>
      <option value="fade">Fade</option>
      <option value="shapeup">Shape Up</option>
      <option value="beard">Beard</option>
    </select>
    <input type="date" name="date" required>
    <button type="submit">Book Now</button>
  </form>
  <p id="bookingMessage" style="text-align:center; margin-top:10px;"></p>
</section>

<!-- Contact Section -->
<section id="contact" class="contact">
  <h3>Contact Us</h3>
  <p>Phone: <a href="tel:+13173846365">(317) 384-6365</a></p>
  <p>Instagram: <a href="https://instagram.com" target="_blank">@buckemchops</a></p>
  <p>Location: 123 Main Street, Your City</p>
</section>

<!-- Footer -->
<footer>
  &copy; 2025 Buckem Chops. All Rights Reserved.
</footer>

<!-- JavaScript for Booking & Scroll Animations -->
<script>
  // Booking Form
  const form = document.getElementById('bookingForm');
  const message = document.getElementById('bookingMessage');

  form.addEventListener('submit', function(e) {
    e.preventDefault();
    message.textContent = "Thanks! Your appointment request has been received. We'll contact you soon.";
    form.reset();
  });

  // Scroll Animations
  const sections = document.querySelectorAll('section');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if(entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, { threshold: 0.2 });

  sections.forEach(section => observer.observe(section));
</script>

</body>
</html>
