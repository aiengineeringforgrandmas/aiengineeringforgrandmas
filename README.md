
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enhanced AI and LLM Restaurant Simulation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
    </style>
</head>
<body class="bg-gradient-to-br from-purple-100 to-indigo-200 min-h-screen">
    <div id="app" class="flex flex-col items-center space-y-8 p-8">
        <h2 class="text-4xl font-bold mb-4 text-transparent bg-clip-text bg-gradient-to-r from-purple-600 to-indigo-600">AI and LLM Restaurant Simulation</h2>
        
        <div class="flex flex-col items-center space-y-8 bg-white p-8 rounded-xl shadow-xl">
            <!-- Dining Room (User Interface) -->
            <div class="w-full">
                <h3 class="text-2xl font-semibold text-indigo-700 mb-4">Dining Room (User Interface)</h3>
                <div class="flex justify-between items-center">
                    <div id="input" class="w-64 h-16 bg-gray-100 rounded-lg flex items-center justify-center text-lg font-semibold">
                        User Input
                    </div>
                    <i data-lucide="arrow-right" class="text-indigo-500"></i>
                    <div id="output" class="w-64 h-16 bg-indigo-100 rounded-lg flex items-center justify-center text-lg font-semibold">
                        AI Output
                    </div>
                </div>
            </div>

            <!-- Kitchen (Training Process) -->
            <div class="w-full bg-gray-100 p-4 rounded-lg">
                <h3 class="text-2xl font-semibold text-indigo-700 mb-4">Kitchen (Training Process)</h3>
                <div class="flex justify-around">
                    <div class="text-center">
                        <div class="w-16 h-16 bg-green-200 rounded-full flex items-center justify-center text-2xl mb-2">🥕</div>
                        <span class="text-sm font-semibold">Ingredients (Data)</span>
                    </div>
                    <div class="text-center">
                        <div class="w-16 h-16 bg-blue-200 rounded-full flex items-center justify-center text-2xl mb-2">📜</div>
                        <span class="text-sm font-semibold">Recipes (Algorithms)</span>
                    </div>
                    <div class="text-center">
                        <div class="w-16 h-16 bg-red-200 rounded-full flex items-center justify-center text-2xl mb-2">🍳</div>
                        <span class="text-sm font-semibold">Cooking (Training)</span>
                    </div>
                </div>
            </div>

            <!-- Master Chef (LLM) -->
            <div class="w-full text-center">
                <h3 class="text-2xl font-semibold text-indigo-700 mb-4">Master Chef / Alchemist (LLM)</h3>
                <div id="masterChef" class="w-24 h-24 bg-yellow-500 rounded-full flex items-center justify-center text-white text-5xl mx-auto">👨‍🍳</div>
                <span class="text-sm mt-2 font-semibold text-indigo-800">Vast Knowledge & Adaptability</span>
            </div>

            <!-- Specialty Sous Chefs (Specialized Models) -->
            <div class="w-full">
                <h3 class="text-2xl font-semibold text-indigo-700 mb-4">Specialty Sous Chefs (Specialized Models)</h3>
                <div class="grid grid-cols-3 gap-4">
                    <div class="chef text-center">
                        <div class="w-16 h-16 bg-pink-500 rounded-full flex items-center justify-center text-white text-2xl mx-auto">🍰</div>
                        <span class="text-xs mt-1 font-semibold text-indigo-800">Pastry (Text-to-Image)</span>
                    </div>
                    <div class="chef text-center">
                        <div class="w-16 h-16 bg-orange-500 rounded-full flex items-center justify-center text-white text-2xl mx-auto">🥣</div>
                        <span class="text-xs mt-1 font-semibold text-indigo-800">Saucier (NLP)</span>
                    </div>
                    <div class="chef text-center">
                        <div class="w-16 h-16 bg-red-500 rounded-full flex items-center justify-center text-white text-2xl mx-auto">🥩</div>
                        <span class="text-xs mt-1 font-semibold text-indigo-800">Meat (Classification)</span>
                    </div>
                    <div class="chef text-center">
                        <div class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center text-white text-2xl mx-auto">🐟</div>
                        <span class="text-xs mt-1 font-semibold text-indigo-800">Seafood (Time Series)</span>
                    </div>
                    <div class="chef text-center">
                        <div class="w-16 h-16 bg-green-500 rounded-full flex items-center justify-center text-white text-2xl mx-auto">🥕</div>
                        <span class="text-xs mt-1 font-semibold text-indigo-800">Vegan (Generative)</span>
                    </div>
                    <div class="chef text-center">
                        <div class="w-16 h-16 bg-yellow-400 rounded-full flex items-center justify-center text-white text-2xl mx-auto">🧀</div>
                        <span class="text-xs mt-1 font-semibold text-indigo-800">Vegetarian (Transformer)</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Initialize Lucide icons
        lucide.createIcons();

        // Simulation
        const masterChef = document.getElementById('masterChef');
        const chefs = document.querySelectorAll('.chef > div');
        const kitchenElements = document.querySelectorAll('.bg-green-200, .bg-blue-200, .bg-red-200');
        const input = document.getElementById('input');
        const output = document.getElementById('output');

        function activateKitchen() {
            kitchenElements.forEach(element => {
                element.style.animation = 'pulse 0.5s ease-in-out';
                setTimeout(() => {
                    element.style.animation = 'none';
                }, 500);
            });
        }

        function activateMasterChef() {
            masterChef.style.animation = 'float 1s ease-in-out infinite';
            setTimeout(() => {
                masterChef.style.animation = 'none';
            }, 1000);
        }

        function activateChefs() {
            chefs.forEach(chef => {
                chef.style.animation = 'pulse 0.5s ease-in-out';
                setTimeout(() => {
                    chef.style.animation = 'none';
                }, 500);
            });
        }

        function generateOutput() {
            const dishes = ['Gourmet Pizza 🍕', 'Exquisite Sushi 🍣', 'Delicate Soufflé 🥚', 'Perfectly Grilled Steak 🥩', 'Innovative Vegan Dish 🥗'];
            return dishes[Math.floor(Math.random() * dishes.length)];
        }

        function simulateAIProcess() {
            input.textContent = 'Processing...';
            activateKitchen();
            
            setTimeout(() => {
                activateMasterChef();
            }, 500);

            setTimeout(() => {
                activateChefs();
            }, 1000);
            
            setTimeout(() => {
                input.textContent = 'User Input';
                output.textContent = generateOutput();
            }, 2000);
        }

        // Start the simulation
        setInterval(simulateAIProcess, 4000);
    </script>
</body>
</html>


![1-image Data Literacy Month ai engineering for grandmas-750x540-black-bg](https://github.com/user-attachments/assets/f0dd9970-2f51-44d6-872e-7fc4259f88c0)


![image gregory kennedy text AI Engineering for Grandmas Gradient colors-650p-1](https://github.com/user-attachments/assets/ff2f2168-e350-4ff8-9891-4994676a19a5)

## I ❤️ Making AI More Accessible for Beginners! 
I believe that AI should be accessible to everyone, regardless of their technical background.  The AI Engineering for Grandmas project is a step towards that vision.

<!---
aiengineeringforgrandmas/aiengineeringforgrandmas is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


