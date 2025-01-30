<template>
  <!-- Hero Section -->
  <!-- <section class="hero">
    <div class="hero-content">
      <h1 class="hero-title">Discover Your Dream Rides</h1>
      <p class="hero-subtitle">
        Realistic cars with top-tier handling for your FiveM experience
      </p>
      <a href="/cars" class="hero-button">Browse Cars</a>
    </div>
  </section> -->

  <!-- Popular Categories -->
  <section class="py-12 bg-gray-100">
    <div class="container mx-auto px-4">
      <h2 class="section-title">Popular Categories</h2>
      <div class="card-grid md:grid-cols-3">
        <div class="card">
          <img src="" alt="Sports Cars" />
          <h3 class="text-xl font-bold mb-2">Sports Cars</h3>
          <p>Experience high-performance speed and style.</p>
        </div>
        <!-- Add more cards -->
      </div>
    </div>
  </section>

  <!-- Featured Cars -->
  <section class="py-12">
    <div class="container mx-auto px-4">
      <h2 class="section-title">Top Featured Cars</h2>
      <div class="grid gap-8 md:grid-cols-3">
        <div class="feature-card">
          <img src="" alt="Car Name" />
          <h3 class="text-xl font-bold mb-2">Lamborghini Aventador</h3>
          <ul class="text-gray-600">
            <li>Top Speed: 350 km/h</li>
            <li>0-100 km/h: 2.9s</li>
            <li>Braking: 32m</li>
          </ul>
          <a href="/cars/lamborghini-aventador" class="hero-button">
            View Details
          </a>
        </div>
        <!-- Add more vehicle cards -->
      </div>
    </div>
  </section>

  <!-- Subscribe Section -->
  <section class="subscribe-section">
    <div class="container mx-auto px-4">
      <h2 class="section-title">Stay Updated</h2>
      <p>Get the latest updates on new cars, features, and server improvements.</p>
      <form class="subscribe-form">
        <input type="email" placeholder="Enter your email" />
        <button type="submit">Subscribe</button>
      </form>
    </div>
  </section>
</template>
