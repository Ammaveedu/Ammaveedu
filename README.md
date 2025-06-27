<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ammaveedu - Delicious Home Food in JP Nagar, Bangalore</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter (for general text) -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <!-- Google Fonts - Noto Sans Malayalam (for Malayalam text) -->
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Malayalam:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7fafc; /* Light gray background */
        }
        .hero-section {
            /* Initial background color, will be replaced by AI image */
            background-color: #2d3748;
            background-size: cover;
            background-position: center;
            height: 600px; /* Adjust height as needed */
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden; /* Ensure content doesn't spill */
        }
        .hero-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5); /* Dark overlay for text readability */
            display: flex; /* Make overlay a flex container */
            flex-direction: column; /* Stack items vertically */
            align-items: center; /* Center items horizontally */
            justify-content: center; /* Center items vertically */
            transition: background-color 0.5s ease-in-out; /* Smooth transition for overlay */
        }
        .section-title {
            position: relative;
            display: inline-block;
            padding-bottom: 8px;
        }
        .section-title::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 60px;
            height: 3px;
            background-color: #f56565; /* Red accent */
            border-radius: 9999px;
        }
        /* Styles for loading spinner */
        .loading-spinner {
            border: 4px solid rgba(255, 255, 255, 0.3);
            border-top-color: #f56565;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin-bottom: 1rem;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        /* Specific style for Malayalam text */
        .malayalam-font {
            font-family: 'Noto Sans Malayalam', sans-serif;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Navigation Bar -->
    <nav class="bg-white shadow-lg py-4 px-6 md:px-12 fixed w-full z-10 top-0">
        <div class="container mx-auto flex justify-between items-center">
            <div class="flex items-center space-x-3"> <!-- Container for logo and name -->
                <img src="https://placehold.co/50x50/f56565/ffffff?text=KHF" alt="Kerala Home Food Logo" class="w-10 h-10 rounded-full shadow-md">
                <a href="#" class="text-2xl font-bold text-gray-900 rounded-md p-2 hover:bg-gray-100 transition duration-300">Ammaveedu</a>
            </div>
            <div class="hidden md:flex space-x-8">
                <a href="#home" class="text-gray-600 hover:text-red-500 font-semibold transition duration-300 rounded-md p-2">Home</a>
                <a href="#menu" class="text-gray-600 hover:text-red-500 font-semibold transition duration-300 rounded-md p-2">Menu</a>
                <a href="#about" class="text-gray-600 hover:text-red-500 font-semibold transition duration-300 rounded-md p-2">About Us</a>
                <a href="#contact" class="text-gray-600 hover:text-red-500 font-semibold transition duration-300 rounded-md p-2">Contact</a>
            </div>
            <!-- Mobile Menu Button -->
            <button id="mobile-menu-button" class="md:hidden text-gray-600 hover:text-red-500 focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                </svg>
            </button>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden mt-4 space-y-2 text-center">
            <a href="#home" class="block text-gray-600 hover:text-red-500 font-semibold py-2 rounded-md transition duration-300">Home</a>
            <a href="#menu" class="block text-gray-600 hover:text-red-500 font-semibold py-2 rounded-md transition duration-300">Menu</a>
            <a href="#about" class="block text-gray-600 hover:text-red-500 font-semibold py-2 rounded-md transition duration-300">About Us</a>
            <a href="#contact" class="block text-gray-600 hover:text-red-500 font-semibold py-2 rounded-md transition duration-300">Contact</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero-section mt-16">
        <div class="hero-overlay">
            <div id="hero-loading-indicator" class="relative z-10 text-white p-8 rounded-lg shadow-xl max-w-2xl mx-auto bg-black bg-opacity-40 flex flex-col items-center justify-center">
                <div class="loading-spinner"></div>
                <p class="text-lg font-semibold">Loading beautiful Kerala hotel image...</p>
            </div>
            <div id="hero-content" class="relative z-10 text-white p-8 rounded-lg shadow-xl max-w-2xl mx-auto bg-black bg-opacity-40 hidden">
                <h1 class="text-5xl font-extrabold mb-4 leading-tight">Welcome to <span class="text-red-400">Ammaveedu</span></h1>
                <p class="text-4xl font-bold mb-4 malayalam-font">നാട്ടിലെവിടാ.....?</p>
                <p class="text-xl mb-8">Experience culinary excellence and a cozy ambiance. We serve the freshest ingredients with passion.</p>
                <a href="#menu" class="bg-red-500 hover:bg-red-600 text-white font-bold py-3 px-8 rounded-full shadow-lg transition duration-300 transform hover:scale-105">Explore Our Menu</a>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="py-16 bg-gray-50">
        <div class="container mx-auto px-6 md:px-12">
            <h2 class="text-4xl font-bold text-center mb-12 section-title text-gray-900">Our Delicious Menu</h2>

            <!-- Appetizers (Kerala Specific) -->
            <div class="mb-12">
                <h3 class="text-3xl font-semibold text-gray-800 mb-6 text-center">Appetizers</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Pazham Pori (Banana Fritters) -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Pazham+Pori" alt="Pazham Pori" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Pazham Pori (Banana Fritters)</h4>
                        <p class="text-gray-600 mb-3">Sweet ripe plantain slices dipped in a spiced flour batter and deep-fried.</p>
                        <span class="text-red-500 text-lg font-bold">₹40</span>
                    </div>
                    <!-- Uzhunnu Vada (Dal Vada) -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Uzhunnu+Vada" alt="Uzhunnu Vada" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Uzhunnu Vada (Dal Fritters)</h4>
                        <p class="text-gray-600 mb-3">Crispy and savory lentil fritters, a popular tea-time snack.</p>
                        <span class="text-red-500 text-lg font-bold">₹35</span>
                    </div>
                    <!-- Kappa Vada (Tapioca Fritters) -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Kappa+Vada" alt="Kappa Vada" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Kappa Vada (Tapioca Fritters)</h4>
                        <p class="text-gray-600 mb-3">Spicy and flavorful fritters made from mashed tapioca and spices.</p>
                        <span class="text-red-500 text-lg font-bold">₹45</span>
                    </div>
                </div>
            </div>

            <!-- Snacks (AI Generated) -->
            <div class="mb-12">
                <h3 class="text-3xl font-semibold text-gray-800 mb-6 text-center">Snacks</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Snack Item 1 -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <div id="snack-1-image-container" class="w-36 h-36 rounded-full mb-4 border-4 border-red-200 flex items-center justify-center bg-gray-100">
                            <div class="loading-spinner"></div>
                        </div>
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Parippu Vada (Lentil Fritters)</h4>
                        <p class="text-gray-600 mb-3">Crispy and spicy fritters made from split pigeon peas.</p>
                        <span class="text-red-500 text-lg font-bold">₹30</span>
                    </div>
                    <!-- Snack Item 2 -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <div id="snack-2-image-container" class="w-36 h-36 rounded-full mb-4 border-4 border-red-200 flex items-center justify-center bg-gray-100">
                            <div class="loading-spinner"></div>
                        </div>
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Sukhiyan (Sweet Green Gram Fritters)</h4>
                        <p class="text-gray-600 mb-3">Sweet dumplings made with green gram and jaggery, deep-fried.</p>
                        <span class="text-red-500 text-lg font-bold">₹40</span>
                    </div>
                    <!-- Snack Item 3 -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <div id="snack-3-image-container" class="w-36 h-36 rounded-full mb-4 border-4 border-red-200 flex items-center justify-center bg-gray-100">
                            <div class="loading-spinner"></div>
                        </div>
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Ethakka Appam (Steamed Plantain Cake)</h4>
                        <p class="text-gray-600 mb-3">Steamed sweet snack made with ripe plantains and rice flour.</p>
                        <span class="text-red-500 text-lg font-bold">₹50</span>
                    </div>
                    <!-- Snack Item 4 -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <div id="snack-4-image-container" class="w-36 h-36 rounded-full mb-4 border-4 border-red-200 flex items-center justify-center bg-gray-100">
                            <div class="loading-spinner"></div>
                        </div>
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Kozhukatta (Rice Dumplings)</h4>
                        <p class="text-gray-600 mb-3">Steamed rice dumplings with a sweet coconut and jaggery filling.</p>
                        <span class="text-red-500 text-lg font-bold">₹45</span>
                    </div>
                    <!-- Snack Item 5 -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <div id="snack-5-image-container" class="w-36 h-36 rounded-full mb-4 border-4 border-red-200 flex items-center justify-center bg-gray-100">
                            <div class="loading-spinner"></div>
                        </div>
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Chatti Pathiri (Layered Flatbread)</h4>
                        <p class="text-gray-600 mb-3">Sweet or savory layered flatbread, often with a rich filling.</p>
                        <span class="text-red-500 text-lg font-bold">₹60</span>
                    </div>
                </div>
            </div>

            <!-- Main Courses (Kerala Specific) -->
            <div class="mb-12">
                <h3 class="text-3xl font-semibold text-gray-800 mb-6 text-center">Main Courses</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Kerala Fish Curry (Meen Curry) -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Meen+Curry" alt="Kerala Fish Curry" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Kerala Fish Curry (Meen Curry)</h4>
                        <p class="text-gray-600 mb-3">Tangy and spicy fish curry cooked in a traditional clay pot with kokum.</p>
                        <span class="text-red-500 text-lg font-bold">₹150</span>
                    </div>
                    <!-- Appam with Stew -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Appam+Stew" alt="Appam with Stew" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Appam with Vegetable Stew</h4>
                        <p class="text-gray-600 mb-3">Fluffy, lace-edged rice pancakes served with a mild coconut milk vegetable stew.</p>
                        <span class="text-red-500 text-lg font-bold">₹120</span>
                    </div>
                    <!-- Kerala Parotta with Chicken Curry -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Parotta+Curry" alt="Kerala Parotta with Chicken Curry" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Kerala Parotta with Chicken Curry</h4>
                        <p class="text-gray-600 mb-3">Layered, flaky flatbread served with a rich and aromatic chicken curry.</p>
                        <span class="text-red-500 text-lg font-bold">₹140</span>
                    </div>
                </div>
            </div>

            <!-- Desserts (Kerala Specific) -->
            <div>
                <h3 class="text-3xl font-semibold text-gray-800 mb-6 text-center">Desserts</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Ada Pradhaman -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Ada+Pradhaman" alt="Ada Pradhaman" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Ada Pradhaman</h4>
                        <p class="text-gray-600 mb-3">Traditional Kerala payasam made with rice ada, jaggery, and coconut milk.</p>
                        <span class="text-red-500 text-lg font-bold">₹60</span>
                    </div>
                    <!-- Elaneer Pudding (Tender Coconut Pudding) -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Elaneer+Pudding" alt="Elaneer Pudding" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Elaneer Pudding</h4>
                        <p class="text-gray-600 mb-3">Light and refreshing pudding made from tender coconut water and pulp.</p>
                        <span class="text-red-500 text-lg font-bold">₹55</span>
                    </div>
                    <!-- Unniyappam -->
                    <div class="bg-white rounded-xl shadow-lg p-6 flex flex-col items-center text-center transform hover:scale-105 transition duration-300">
                        <img src="https://placehold.co/150x150/e2e8f0/4a5568?text=Unniyappam" alt="Unniyappam" class="w-36 h-36 object-cover rounded-full mb-4 border-4 border-red-200">
                        <h4 class="text-xl font-bold text-gray-900 mb-2">Unniyappam</h4>
                        <p class="text-gray-600 mb-3">Sweet, fried rice flour dumplings with jaggery and banana.</p>
                        <span class="text-red-500 text-lg font-bold">₹45</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-16 bg-white">
        <div class="container mx-auto px-6 md:px-12 flex flex-col md:flex-row items-center gap-12">
            <div class="md:w-1/2 flex items-center justify-center min-h-[400px] bg-gray-100 rounded-xl shadow-xl" id="restaurant-interior-image-container">
                <!-- Loading spinner will appear here -->
                <div class="loading-spinner"></div>
            </div>
            <div class="md:w-1/2 text-center md:text-left">
                <h2 class="text-4xl font-bold mb-6 section-title text-gray-900">About Ammaveedu</h2>
                <p class="text-lg text-gray-700 leading-relaxed mb-4">
                    Welcome to Ammaveedu, where culinary passion meets a cozy dining experience. Established in [Year], we have been serving our community with fresh, high-quality ingredients and a commitment to exceptional taste.
                </p>
                <p class="text-lg text-gray-700 leading-relaxed mb-4">
                    We are proud to be operating from **JP Nagar, Bangalore**, bringing authentic home-style Kerala food to your table. Our chefs meticulously craft each dish, blending traditional recipes with modern twists to create a unique and memorable flavor profile.
                </p>
                <p class="text-lg text-gray-700 leading-relaxed">
                    We believe in creating not just meals, but experiences that bring people together. Come and enjoy our warm ambiance, friendly service, and a menu designed to delight every palate. We look forward to welcoming you!
                </p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-16 bg-gray-50">
        <div class="container mx-auto px-6 md:px-12">
            <h2 class="text-4xl font-bold text-center mb-12 section-title text-gray-900">Contact Us</h2>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
                <!-- Contact Information -->
                <div class="bg-white rounded-xl shadow-lg p-8 text-center">
                    <h3 class="text-2xl font-semibold text-gray-800 mb-6">Get in Touch</h3>
                    <p class="text-lg text-gray-700 mb-4">
                        <strong class="text-red-500">Address:</strong> 123 Restaurant Lane, JP Nagar, Bangalore, FC 98765
                    </p>
                    <p class="text-lg text-gray-700 mb-4">
                        <strong class="text-red-500">Phone:</strong> <a href="tel:+919656656067" class="text-blue-600 hover:underline">9656656067</a>
                    </p>
                    <p class="text-lg text-gray-700 mb-4">
                        <strong class="text-red-500">Email:</strong> info@yourrestaurant.com
                    </p>
                    <p class="text-lg text-gray-700 mb-4">
                        <strong class="text-red-500">Hours:</strong> <br>
                        Monday - Friday: 11:00 AM - 10:00 PM <br>
                        Saturday - Sunday: 12:00 PM - 11:00 PM
                    </p>
                    <div class="mt-6">
                        <a href="https://www.google.com/maps/search/Ammaveedu+JP+Nagar+Bangalore" target="_blank" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-3 px-6 rounded-full shadow-lg transition duration-300 transform hover:scale-105 inline-flex items-center">
                            <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.727A8 8 0 016.343 5.273L12 10l-5.657-4.727a8 8 0 0111.314 11.314z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 13a3 3 0 100-6 3 3 0 000 6z"></path></svg>
                            Find Us on Map
                        </a>
                    </div>
                </div>

                <!-- Contact Form -->
                <div class="bg-white rounded-xl shadow-lg p-8">
                    <h3 class="text-2xl font-semibold text-gray-800 mb-6 text-center">Send Us a Message</h3>
                    <!-- Formspree integration -->
                    <form action="https://formspree.io/f/f/yourformid" method="POST" class="space-y-6">
                        <div>
                            <label for="name" class="block text-sm font-medium text-gray-700 mb-2">Name</label>
                            <input type="text" id="name" name="name" class="mt-1 block w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-red-500 focus:border-red-500 sm:text-base" placeholder="Your Name" required>
                        </div>
                        <div>
                            <label for="email" class="block text-sm font-medium text-gray-700 mb-2">Email</label>
                            <input type="email" id="email" name="email" class="mt-1 block w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-red-500 focus:border-red-500 sm:text-base" placeholder="your.email@example.com" required>
                            <!-- Hidden input to capture reply-to email for Formspree -->
                            <input type="hidden" name="_replyto" value="sharmsharmil@gmail.com">
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-700 mb-2">Message</label>
                            <textarea id="message" name="message" rows="5" class="mt-1 block w-full px-4 py-3 border border-gray-300 rounded-lg shadow-sm focus:ring-red-500 focus:border-red-500 sm:text-base" placeholder="Your message..." required></textarea>
                        </div>
                        <div>
                            <button type="submit" class="w-full bg-red-500 hover:bg-red-600 text-white font-bold py-3 px-6 rounded-full shadow-lg transition duration-300 transform hover:scale-105">Send Message</button>
                        </div>
                    </form>
                    <p id="form-status" class="mt-4 text-center text-sm font-semibold text-green-600 hidden">Thank you for your message! We\'ll get back to you soon.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-8">
        <div class="container mx-auto px-6 md:px-12 text-center">
            <p>&copy; 2025 Ammaveedu. All rights reserved.</p>
            <div class="flex justify-center space-x-6 mt-4">
                <a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a>
                <a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();

                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });

                // Close mobile menu if open
                const mobileMenu = document.getElementById('mobile-menu');
                if (!mobileMenu.classList.contains('hidden')) {
                    mobileMenu.classList.add('hidden');
                }
            });
        });

        // Mobile menu toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Function to generate and set background image for hero section
        async function generateHeroBackgroundImage(promptText) {
            const heroSection = document.getElementById('home');
            const heroLoadingIndicator = document.getElementById('hero-loading-indicator');
            const heroContent = document.getElementById('hero-content');

            if (!heroSection || !heroLoadingIndicator || !heroContent) return;

            // Show loading indicator, hide content
            heroLoadingIndicator.classList.remove('hidden');
            heroContent.classList.add('hidden');
            heroSection.style.backgroundImage = 'none'; // Clear any previous background image

            const prompt = promptText;
            const payload = { instances: { prompt: prompt }, parameters: { "sampleCount": 1} };
            const apiKey = ""; // Canvas will automatically provide this
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/imagen-3.0-generate-002:predict?key=${apiKey}`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                if (!response.ok) {
                    const errorText = await response.text();
                    console.error(`Hero image generation failed with status ${response.status}:`, errorText);
                    // Fallback to a placeholder image on error
                    heroSection.style.backgroundImage = `url('https://placehold.co/1920x800/2d3748/ffffff?text=Error+Loading+Image')`;
                    heroLoadingIndicator.classList.add('hidden');
                    heroContent.classList.remove('hidden');
                    return;
                }

                const result = await response.json();

                if (result.predictions && result.predictions.length > 0 && result.predictions[0].bytesBase64Encoded) {
                    const imageUrl = `data:image/png;base64,${result.predictions[0].bytesBase64Encoded}`;
                    heroSection.style.backgroundImage = `url('${imageUrl}')`;
                } else {
                    console.error('Hero image generation failed: No predictions found or invalid format.');
                    heroSection.style.backgroundImage = `url('https://placehold.co/1920x800/2d3748/ffffff?text=Error+Loading+Image')`;
                }
            } catch (error) {
                console.error('Error generating hero image (network or parsing):', error);
                heroSection.style.backgroundImage = `url('https://placehold.co/1920x800/2d3748/ffffff?text=Error+Loading+Image')`;
            } finally {
                // Hide loading indicator and show content regardless of success or failure
                heroLoadingIndicator.classList.add('hidden');
                heroContent.classList.remove('hidden');
            }
        }

        // Function to generate and set image for menu items or interior
        async function generateImageForElement(containerId, promptText, width = 150, height = 150, isCircular = true) {
            const container = document.getElementById(containerId);
            if (!container) return;

            // Clear existing content and add loading spinner
            container.innerHTML = '<div class="loading-spinner"></div>';
            // Ensure container has flex properties for centering the spinner
            container.classList.add('flex', 'items-center', 'justify-center');

            const prompt = promptText;
            const payload = { instances: { prompt: prompt }, parameters: { "sampleCount": 1} };
            const apiKey = ""; // Canvas will automatically provide this
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/imagen-3.0-generate-002:predict?key=${apiKey}`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                if (!response.ok) {
                    const errorText = await response.text();
                    console.error(`Image generation failed for ${containerId} with status ${response.status}:`, errorText);
                    container.innerHTML = `<img src="https://placehold.co/${width}x${height}/e2e8f0/4a5568?text=Error" alt="Error loading image" class="${isCircular ? 'rounded-full' : 'rounded-xl'} shadow-xl w-full h-auto object-cover border-4 border-red-200">`;
                    return;
                }

                const result = await response.json();

                if (result.predictions && result.predictions.length > 0 && result.predictions[0].bytesBase64Encoded) {
                    const imageUrl = `data:image/png;base64,${result.predictions[0].bytesBase64Encoded}`;
                    const imgElement = document.createElement('img');
                    imgElement.src = imageUrl;
                    imgElement.alt = promptText;
                    imgElement.classList.add(
                        isCircular ? 'rounded-full' : 'rounded-xl',
                        'shadow-xl',
                        'w-full',
                        'h-auto',
                        'object-cover',
                        'border-4',
                        'border-red-200'
                    ); // Apply Tailwind classes
                    container.innerHTML = ''; // Clear spinner
                    container.appendChild(imgElement);
                    container.classList.remove('flex', 'items-center', 'justify-center'); // Remove flex properties
                } else {
                    console.error(`Image generation failed for ${containerId}: No predictions found or invalid format in successful response.`);
                    container.innerHTML = `<img src="https://placehold.co/${width}x${height}/e2e8f0/4a5568?text=Error" alt="Error loading image" class="${isCircular ? 'rounded-full' : 'rounded-xl'} shadow-xl w-full h-auto object-cover border-4 border-red-200">`;
                }
            } catch (error) {
                console.error(`Error generating image for ${containerId} (network or parsing):`, error);
                container.innerHTML = `<img src="https://placehold.co/${width}x${height}/e2e8f0/4a5568?text=Error" alt="Error loading image" class="${isCircular ? 'rounded-full' : 'rounded-xl'} shadow-xl w-full h-auto object-cover border-4 border-red-200">`;
            }
        }


        // Generate images on page load
        document.addEventListener('DOMContentLoaded', () => {
            // Generate hero background image
            generateHeroBackgroundImage(
                'AI-generated image of a traditional Kerala hotel exterior, vibrant architecture, lush greenery, inviting entrance, realistic, high quality, daytime'
            );

            // Generate interior image
            generateImageForElement(
                'restaurant-interior-image-container',
                'AI-generated image of a cozy, traditional Kerala restaurant interior, warm lighting, wooden furniture, authentic decor, inviting atmosphere, high quality, realistic',
                600, 400, false // Not circular
            );

            // Generate snack images
            generateImageForElement('snack-1-image-container', 'AI-generated image of Parippu Vada, crispy lentil fritters, Kerala snack, home food style, realistic', 150, 150, true);
            generateImageForElement('snack-2-image-container', 'AI-generated image of Sukhiyan, sweet green gram fritters, Kerala snack, home food style, realistic', 150, 150, true);
            generateImageForElement('snack-3-image-container', 'AI-generated image of Ethakka Appam, steamed plantain cake, Kerala snack, home food style, realistic', 150, 150, true);
            generateImageForElement('snack-4-image-container', 'AI-generated image of Kozhukatta, steamed rice dumplings with coconut and jaggery filling, Kerala snack, home food style, realistic', 150, 150, true);
            generateImageForElement('snack-5-image-container', 'AI-generated image of Chatti Pathiri, layered flatbread, Kerala snack, home food style, realistic', 150, 150, true);


            // Handle Formspree submission for success message
            const contactForm = document.querySelector('#contact form');
            const formStatus = document.getElementById('form-status');

            if (contactForm) {
                contactForm.addEventListener('submit', async (event) => {
                    event.preventDefault(); // Prevent default form submission

                    const formData = new FormData(contactForm);
                    try {
                        const response = await fetch(contactForm.action, {
                            method: contactForm.method,
                            body: formData,
                            headers: {
                                'Accept': 'application/json' // Important for Formspree to return JSON
                            }
                        });

                        if (response.ok) {
                            formStatus.textContent = 'Thank you for your message! We\'ll get back to you soon.';
                            formStatus.classList.remove('hidden', 'text-red-600');
                            formStatus.classList.add('text-green-600');
                            contactForm.reset(); // Clear the form
                        } else {
                            const errorData = await response.json();
                            if (errorData.errors) {
                                formStatus.textContent = `Error: ${errorData.errors.map(e => e.message).join(', ')}`;
                            } else {
                                formStatus.textContent = 'Oops! There was a problem sending your message.';
                            }
                            formStatus.classList.remove('hidden', 'text-green-600');
                            formStatus.classList.add('text-red-600');
                        }
                    } catch (error) {
                        console.error('Form submission error:', error);
                        formStatus.textContent = 'Oops! Network error. Please try again later.';
                        formStatus.classList.remove('hidden', 'text-green-600');
                        formStatus.classList.add('text-red-600');
                    }
                });
            }
        });
    </script>
</body>
</html>
