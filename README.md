<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AURORA | Premium Sound</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;800&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        body { background: #050000; color: white; font-family: 'Inter', sans-serif; overflow-x: hidden; }
        .futuristic { font-family: 'Orbitron', sans-serif; }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(15px); border: 1px solid rgba(220, 38, 38, 0.2); transition: 0.3s; }
        .glass:hover { border-color: #dc2626; box-shadow: 0 0 20px rgba(220, 38, 38, 0.3); }
        .bg-gradient-dark { background: radial-gradient(circle at top right, #3d0000 0%, #050000 70%); }
        .hidden { display: none; }
    </style>
</head>
<body class="bg-gradient-dark min-height-screen">

    <nav class="sticky top-0 z-50 glass px-6 py-4 flex justify-between items-center mb-8">
        <h1 class="futuristic text-2xl font-bold text-red-600 tracking-tighter">AURORA AUDIO</h1>
        <div class="hidden md:flex space-x-8 text-xs uppercase tracking-widest font-semibold">
            <a href="#" class="hover:text-red-500">Shop</a>
            <a href="#" class="hover:text-red-500">Deals</a>
            <a href="#" class="hover:text-red-500">Support</a>
        </div>
        <div class="flex items-center space-x-6">
            <button onclick="toggleAuth()" class="text-sm border-b border-red-600">Login / Signup</button>
            <button onclick="toggleCart()" class="relative">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                </svg>
                <span id="cart-count" class="absolute -top-2 -right-2 bg-red-600 text-[10px] px-1.5 rounded-full">0</span>
            </button>
        </div>
    </nav>

    <div id="auth-modal" class="fixed inset-0 z-[100] hidden flex items-center justify-center bg-black/80 backdrop-blur-md">
        <div class="glass p-8 rounded-2xl w-full max-w-md relative">
            <button onclick="toggleAuth()" class="absolute top-4 right-4 text-gray-500 hover:text-white">✕</button>
            <h2 class="futuristic text-2xl mb-6 text-center">CREATE ACCOUNT</h2>
            <div class="space-y-4">
                <input type="text" placeholder="Full Name" class="w-full bg-white/5 border border-white/10 p-3 rounded-lg focus:outline-none focus:border-red-600">
                <input type="email" placeholder="Email or Phone Number" class="w-full bg-white/5 border border-white/10 p-3 rounded-lg focus:outline-none focus:border-red-600">
                <input type="password" placeholder="Password" class="w-full bg-white/5 border border-white/10 p-3 rounded-lg focus:outline-none focus:border-red-600">
                <textarea placeholder="Delivery Address" class="w-full bg-white/5 border border-white/10 p-3 rounded-lg focus:outline-none focus:border-red-600"></textarea>
                <button class="w-full bg-red-600 py-3 futuristic font-bold rounded-lg hover:bg-red-700 transition">REGISTER</button>
            </div>
        </div>
    </div>

    <main class="max-w-7xl mx-auto px-6 pb-20">
        <header class="mb
