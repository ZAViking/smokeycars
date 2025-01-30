<template>
    <header class="bg-gray-900 text-white shadow-lg">
      <div class="container mx-auto px-4 py-4 flex items-center justify-between">
        <!-- Logo -->
        <div class="flex items-center space-x-3">
          <img src="" alt="Website Logo" class="w-10 h-10 rounded-lg" />
          <span class="text-xl font-bold">FiveM Car Hub</span>
        </div>
        <!-- Navigation -->
        <nav class="hidden md:flex space-x-8">
          <a href="/" class="hover:text-gray-300">Home</a>
          <a href="/cars" class="hover:text-gray-300">Cars</a>
          <a href="/categories" class="hover:text-gray-300">Categories</a>
          <a href="/contact" class="hover:text-gray-300">Contact</a>
        </nav>
        <!-- Mobile Menu Button -->
        <button class="md:hidden p-2 rounded bg-gray-800 hover:bg-gray-700">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            class="w-6 h-6"
          >
            <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16m-7 6h7" />
          </svg>
        </button>
        <Nav />
      </div>
    </header>
  </template>
  