# Design-Inclusivity Departmental Society
Design Inclusivity is the approach of creating products, experiences, and systems that are usable and welcoming for people of all identities, abilities, and backgrounds. It ensures no one is left out of the design experience — whether in fashion, digital design, or physical spaces.
In essence:

Designing for everyone, not just the majority.
It’s where creativity meets empathy.
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Style Decoder</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Varela+Round&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        :root {
            --bg-color: #121212; /* Dark background */
            --text-color: #F0F8FF; /* Light text */
            --accent-neon: #00FFFF; /* Cyan */
            --accent-pink: #FF69B4;
            --card-bg: #1E1E1E;
            --pastel-base: #D1C4E9; /* Soft lavender */
            --pastel-accent1: #A7FFEB; /* Mint */
            --pastel-accent2: #FFD180; /* Light orange */
            --font-primary: 'Varela Round', sans-serif;
            --font-secondary: 'Press Start 2P', cursive;
        }
        body {
            font-family: var(--font-primary);
            background-color: var(--bg-color);
            color: var(--text-color);
            overflow-x: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }
        .container {
            max-width: 960px;
            padding: 2rem;
            width: 100%;
        }
        .card {
            background-color: var(--card-bg);
            border-radius: 1rem;
            border: 2px solid var(--pastel-base);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.7);
        }
        .btn {
            background-color: var(--accent-neon);
            color: var(--bg-color);
            font-family: var(--font-secondary);
            border-radius: 0.5rem;
            padding: 0.75rem 1.5rem;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out, transform 0.2s ease-in-out;
        }
        .btn:hover {
            background-color: var(--accent-pink);
            transform: scale(1.05);
        }
        .option-card {
            background-color: #2E2E2E;
            border-radius: 0.75rem;
            padding: 1rem;
            margin-bottom: 0.5rem;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out, transform 0.2s ease-in-out, border 0.2s ease-in-out;
            border: 2px solid transparent;
        }
        .option-card:hover {
            background-color: #444444;
            transform: scale(1.02);
            border-color: var(--pastel-accent1);
        }
        .option-card.selected {
            background-color: var(--pastel-base);
            color: var(--bg-color);
            border-color: var(--accent-neon);
        }
        /* Camera styles */
        .camera-container {
            position: relative;
            width: 100%;
            padding-top: 100%; /* 1:1 aspect ratio */
            border-radius: 1rem;
            overflow: hidden;
            border: 2px solid var(--pastel-accent2);
        }
        .camera-container > * {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .camera-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .camera-overlay-image {
            /* The base64 data URI of the user-provided camera frame image */
            background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAQAAAAHgCAIAAACtY1n+AAAAA3NCSVQICAjb4U/gAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAAjHSURBVHhe7d1BihtlFAdwX2rI80gB4R3B3UHcQdwh3ME8A8G8A6s+o72kI7hJk5k+ySUpWj/e3d3/u+97v+2+n/r73zNn79l99y7Z2/e8Z8/7nfNmfZ733e+z3zPm/T9//M+b9/7PmfP+73zPm/f+/5nz/u/Z8/7//M+b93/Pm/d/z5v3/v+b9/7/m/f8z5/3/m/f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M+f9/zPn/f8z5/3/M%3D');
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;
            width: 90%;
            height: 90%;
            max-width: 500px;
            max-height: 500px;
        }
        .monochrome-filter {
            filter: grayscale(100%);
        }
    </style>
</head>
<body class="p-6">
    <div class="container mx-auto">
        <!-- Main Menu Screen -->
        <div id="main-menu" class="flex flex-col items-center justify-center text-center space-y-8">
            <h1 class="text-4xl md:text-5xl font-bold text-center">
                Style Decoder
            </h1>
            <p class="text-lg md:text-xl text-gray-400">Unlock your inner fashion persona with our three fun quizzes!</p>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6 w-full mt-8">
                <!-- Game 1 Card -->
                <div data-game-id="0" class="card p-6 md:p-8 flex flex-col items-center cursor-pointer">
                    <span class="text-5xl mb-4">🤔</span>
                    <h2 class="text-xl font-bold text-accent-neon">Game 01</h2>
                    <p class="text-sm md:text-base text-center mt-2">What Kind of Fashion Follower Are You?</p>
                </div>
                <!-- Game 2 Card -->
                <div data-game-id="1" class="card p-6 md:p-8 flex flex-col items-center cursor-pointer">
                    <span class="text-5xl mb-4">🎨</span>
                    <h2 class="text-xl font-bold text-accent-neon">Game 02</h2>
                    <p class="text-sm md:text-base text-center mt-2">What’s Your Inner Color?</p>
                </div>
                <!-- Game 3 Card -->
                <div data-game-id="2" class="card p-6 md:p-8 flex flex-col items-center cursor-pointer">
                    <span class="text-5xl mb-4">💅</span>
                    <h2 class="text-xl font-bold text-accent-neon">Game 03</h2>
                    <p class="text-sm md:text-base text-center mt-2">What’s Your Fashion Style?</p>
                </div>
            </div>
        </div>

        <!-- Quiz Section -->
        <div id="quiz-section" class="hidden flex-col items-center text-center space-y-6">
            <h2 id="quiz-title" class="text-3xl md:text-4xl font-bold text-accent-neon"></h2>
            <p id="quiz-question" class="text-xl md:text-2xl font-semibold mt-4 text-pastel-base"></p>
            <div id="quiz-options" class="w-full mt-6">
                <!-- Quiz options will be dynamically inserted here -->
            </div>
            <button id="next-btn" class="btn mt-6 disabled:bg-gray-700 disabled:cursor-not-allowed" disabled>Next</button>
        </div>

        <!-- Result Section -->
        <div id="result-section" class="hidden flex-col items-center text-center space-y-8">
            <h2 class="text-3xl md:text-4xl font-bold text-accent-neon">Your Result</h2>
            <div class="card p-8 w-full max-w-md">
                <span id="result-icon" class="text-6xl block mb-4 animate-pulse">🎉</span>
                <h3 id="result-title" class="text-2xl font-bold text-accent-pink mb-2"></h3>
                <p id="result-description" class="text-lg text-gray-400"></p>
            </div>
            <div id="gemini-analysis-section" class="hidden w-full space-y-4">
                <h3 class="text-xl md:text-2xl font-bold text-accent-neon">✨ Your Style Analysis</h3>
                <div class="card p-6 md:p-8">
                    <p id="gemini-text" class="text-base text-gray-300"></p>
                    <p id="gemini-loading" class="text-base text-gray-400 mt-2 hidden">Generating analysis...</p>
                </div>
            </div>
            <div class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-4 w-full mt-6">
                <button id="try-again-btn" class="btn w-full md:w-auto">Try Another Game</button>
                <button id="camera-btn" class="btn w-full md:w-auto">Take Photo!</button>
            </div>
            <button id="gemini-btn" class="btn mt-4">✨ Get a Personalized Style Analysis</button>
        </div>

        <!-- Camera Section -->
        <div id="camera-section" class="hidden flex-col items-center justify-center p-6 space-y-4">
            <h2 class="text-2xl md:text-3xl font-bold text-center text-accent-neon">Strike a Pose! 📸</h2>
            <p class="text-center text-gray-400">Get ready to show you're #ExclusivelyInclusive!</p>
            <div class="camera-container">
                <video id="webcam" playsinline autoplay class="w-full h-full object-cover monochrome-filter"></video>
                <canvas id="photo-canvas" class="hidden"></canvas>
                <div class="camera-overlay">
                    <div class="camera-overlay-image"></div>
                </div>
            </div>
            <div class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-4 w-full pt-4">
                <button id="capture-btn" class="btn w-full md:w-auto">Take Photo</button>
                <a id="download-btn" class="hidden btn w-full md:w-auto text-center" download="exclusively-inclusive-photo.png">Download</a>
            </div>
            <p id="message-box" class="text-red-500 hidden"></p>
            <button id="back-to-menu-btn" class="btn mt-4">Back to Menu</button>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const state = {
                currentScreen: 'main-menu',
                gameData: null,
                currentQuestionIndex: 0,
                answers: {}
            };
            const screens = {
                'main-menu': document.getElementById('main-menu'),
                'quiz-section': document.getElementById('quiz-section'),
                'result-section': document.getElementById('result-section'),
                'camera-section': document.getElementById('camera-section')
            };
            const gameData = [
                {
                    title: "Fashion Follower Quiz",
                    questions: [
                        {
                            text: "Where do you mostly get fashion inspiration from?",
                            options: [
                                { text: "Pinterest", value: "A", emoji: "📌" },
                                { text: "Instagram", value: "B", emoji: "📸" },
                                { text: "YouTube / Celebrities", value: "C", emoji: "📺" },
                                { text: "My own instincts", value: "D", emoji: "🔮" }
                            ]
                        },
                        {
                            text: "How often do you follow fashion trends?",
                            options: [
                                { text: "Every season", value: "A", emoji: "🗓️" },
                                { text: "Occasionally", value: "B", emoji: "🤷" },
                                { text: "Only if I like them", value: "C", emoji: "💖" },
                                { text: "Rarely – I make my own", value: "D", emoji: "✨" }
                            ]
                        },
                        {
                            text: "What type of fashion content do you save?",
                            options: [
                                { text: "Trend alerts", value: "A", emoji: "⚡" },
                                { text: "Outfit ideas", value: "B", emoji: "💡" },
                                { text: "Celebrity styles", value: "C", emoji: "🌟" },
                                { text: "DIY/upcycled looks", value: "D", emoji: "✂️" }
                            ]
                        },
                        {
                            text: "What’s your go-to outfit on a chill day?",
                            options: [
                                { text: "The latest trendy outfit", value: "A", emoji: "📈" },
                                { text: "Comfy & casual", value: "B", emoji: "🛋️" },
                                { text: "Something statement-making", value: "C", emoji: "📢" },
                                { text: "Thrifted or custom-mixed", value: "D", emoji: "♻️" }
                            ]
                        }
                    ],
                    results: {
                        'A': { title: "Trend Tracker", description: "You're always one step ahead, spotting new trends before they even hit the runway.", icon: "📈" },
                        'B': { title: "Mood Dresser", description: "Your style is an extension of your feelings, effortlessly chic and always authentic.", icon: "😌" },
                        'C': { title: "Style Watcher", description: "You observe and adapt the best of what's out there to create your own signature look.", icon: "👀" },
                        'D': { title: "Fashion Rebel", description: "You set the rules, not follow them. Your style is unapologetically original and bold.", icon: "🤘" }
                    }
                },
                {
                    title: "Inner Color Quiz",
                    questions: [
                        {
                            text: "You feel most calm when you're...",
                            options: [
                                { text: "In nature", value: "A", emoji: "🌳" },
                                { text: "In your room", value: "B", emoji: "🧘" },
                                { text: "Socializing", value: "C", emoji: "🗣️" },
                                { text: "Creating something", value: "D", emoji: "🖌️" }
                            ]
                        },
                        {
                            text: "Which word describes your vibe best?",
                            options: [
                                { text: "Peaceful", value: "A", emoji: "🕊️" },
                                { text: "Focused", value: "B", emoji: "🎯" },
                                { text: "Energetic", value: "C", emoji: "🔥" },
                                { text: "Artistic", value: "D", emoji: "🎨" }
                            ]
                        },
                        {
                            text: "How do you solve problems?",
                            options: [
                                { text: "Step back and breathe", value: "A", emoji: "🧘‍♀️" },
                                { text: "Focus until it's done", value: "B", emoji: "💡" },
                                { text: "Talk it out", value: "C", emoji: "💬" },
                                { text: "Create or brainstorm solutions", value: "D", emoji: "🧠" }
                            ]
                        },
                        {
                            text: "Pick an object you vibe with:",
                            options: [
                                { text: "Leaf", value: "A", emoji: "🌿" },
                                { text: "Crystal", value: "B", emoji: "💎" },
                                { text: "Disco Ball", value: "C", emoji: "✨" },
                                { text: "Paintbrush", value: "D", emoji: "🌈" }
                            ]
                        }
                    ],
                    results: {
                        'A': { title: "Green", description: "Your inner color is Green, symbolizing Balance & Renewal. You are grounded, harmonious, and connected to the natural world.", icon: "💚" },
                        'B': { title: "Blue", description: "Your inner color is Blue, representing Focus & Calm. You are a deep thinker, analytical, and bring a sense of serenity to any situation.", icon: "💙" },
                        'C': { title: "Red", description: "Your inner color is Red, for Passion & Energy. You are bold, vibrant, and driven, always ready to take on the next challenge.", icon: "❤️" },
                        'D': { title: "Purple", description: "Your inner color is Purple, representing Creativity & Expression. You are imaginative, unique, and always looking for new ways to express yourself.", icon: "💜" }
                    }
                },
                {
                    title: "Fashion Style Quiz",
                    questions: [
                        {
                            text: "Your favorite footwear is:",
                            options: [
                                { text: "Sneakers", value: "A", emoji: "👟" },
                                { text: "Boots", value: "B", emoji: "👢" },
                                { text: "Sandals", value: "C", emoji: "🩴" },
                                { text: "Heels / Loafers", value: "D", emoji: "👠" }
                            ]
                        },
                        {
                            text: "If your wardrobe was a playlist, it would be:",
                            options: [
                                { text: "Hip-hop / EDM", value: "A", emoji: "🎶" },
                                { text: "Jazz / Indie", value: "B", emoji: "🎷" },
                                { text: "Chill / Acoustic", value: "C", emoji: "🎸" },
                                { text: "Classical / Pop", value: "D", emoji: "🎼" }
                            ]
                        },
                        {
                            text: "You’d rather shop at:",
                            options: [
                                { text: "Street markets", value: "A", emoji: "🛍️" },
                                { text: "Online stores", value: "B", emoji: "🌐" },
                                { text: "Boutiques", value: "C", emoji: "🏷️" },
                                { text: "High-end brands", value: "D", emoji: "💎" }
                            ]
                        },
                        {
                            text: "You always look for clothes that feel...",
                            options: [
                                { text: "Effortless", value: "A", emoji: "🕊️" },
                                { text: "Edgy", value: "B", emoji: "😎" },
                                { text: "Clean & classic", value: "C", emoji: "👔" },
                                { text: "Expressive", value: "D", emoji: "✨" }
                            ]
                        }
                    ],
                    results: {
                        'A': { title: "Casual/Relaxed", description: "Your style is all about comfort and ease, with a cool, laid-back vibe.", icon: "👕" },
                        'B': { title: "Streetwear", description: "You have an urban edge, blending trendy pieces with a strong sense of individuality.", icon: "🧢" },
                        'C': { title: "Formal/Minimal", description: "You favor clean lines, neutral tones, and timeless elegance.", icon: "👗" },
                        'D': { title: "Experimental/Avant-garde", description: "You love to push boundaries, using fashion as a canvas for bold and artistic expression.", icon: "👘" }
                    }
                }
            ];
            const quizTitleEl = document.getElementById('quiz-title');
            const quizQuestionEl = document.getElementById('quiz-question');
            const quizOptionsEl = document.getElementById('quiz-options');
            const nextBtn = document.getElementById('next-btn');
            const resultTitleEl = document.getElementById('result-title');
            const resultDescriptionEl = document.getElementById('result-description');
            const resultIconEl = document.getElementById('result-icon');
            const tryAgainBtn = document.getElementById('try-again-btn');
            const cameraBtn = document.getElementById('camera-btn');
            const geminiBtn = document.getElementById('gemini-btn');
            const geminiAnalysisSection = document.getElementById('gemini-analysis-section');
            const geminiTextEl = document.getElementById('gemini-text');
            const geminiLoadingEl = document.getElementById('gemini-loading');
            const webcam = document.getElementById('webcam');
            const photoCanvas = document.getElementById('photo-canvas');
            const captureBtn = document.getElementById('capture-btn');
            const downloadBtn = document.getElementById('download-btn');
            const messageBox = document.getElementById('message-box');
            const backToMenuBtn = document.getElementById('back-to-menu-btn');
            let stream = null;
            function showScreen(screenName) {
                for (const key in screens) {
                    screens[key].classList.add('hidden', 'flex-col');
                }
                screens[screenName].classList.remove('hidden', 'flex-col');
                screens[screenName].classList.add('flex');
            }
            function renderQuiz() {
                const quiz = state.gameData;
                const currentQuestion = quiz.questions[state.currentQuestionIndex];
                quizTitleEl.textContent = quiz.title;
                quizQuestionEl.textContent = currentQuestion.text;
                quizOptionsEl.innerHTML = '';
                currentQuestion.options.forEach(option => {
                    const optionCard = document.createElement('div');
                    optionCard.className = "option-card p-4 md:p-6 flex items-center space-x-4 cursor-pointer";
                    optionCard.innerHTML = `
                        <span class="text-3xl">${option.emoji}</span>
                        <p class="text-base md:text-lg font-medium">${option.text}</p>
                    `;
                    optionCard.addEventListener('click', () => {
                        document.querySelectorAll('.option-card').forEach(card => card.classList.remove('selected'));
                        optionCard.classList.add('selected');
                        state.answers[state.currentQuestionIndex] = option.value;
                        nextBtn.disabled = false;
                    });
                    quizOptionsEl.appendChild(optionCard);
                });
                nextBtn.textContent = (state.currentQuestionIndex === quiz.questions.length - 1) ? "See Result" : "Next";
                nextBtn.disabled = !state.answers[state.currentQuestionIndex];
            }
            function calculateResult() {
                const scores = { A: 0, B: 0, C: 0, D: 0 };
                Object.values(state.answers).forEach(answer => {
                    scores[answer]++;
                });
                let maxScore = 0;
                let resultKey = null;
                for (const key in scores) {
                    if (scores[key] > maxScore) {
                        maxScore = scores[key];
                        resultKey = key;
                    }
                }
                if (!resultKey) resultKey = 'A';
                const result = state.gameData.results[resultKey];
                resultTitleEl.textContent = result.title;
                resultDescriptionEl.textContent = result.description;
                resultIconEl.textContent = result.icon;
                showScreen('result-section');
            }
            async function getGeminiAnalysis(styleType) {
                geminiLoadingEl.classList.remove('hidden');
                geminiBtn.disabled = true;
                geminiTextEl.textContent = '';
                geminiAnalysisSection.classList.remove('hidden');
                const prompt = `You are a creative fashion advisor. Based on the style type "${styleType}", generate a single paragraph of text (2-3 sentences) that gives a personalized style analysis. In your response, suggest a celebrity style icon for this type, a simple color palette, and one key item of clothing they should try. Do not mention the style type name in your response. Do not use markdown formatting.`;
                let chatHistory = [];
                chatHistory.push({ role: "user", parts: [{ text: prompt }] });
                const payload = { contents: chatHistory };
                const apiKey = "";
                const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-05-20:generateContent?key=${apiKey}`;
                try {
                    const response = await fetch(apiUrl, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });
                    const result = await response.json();
                    if (result.candidates && result.candidates.length > 0 &&
                        result.candidates[0].content && result.candidates[0].content.parts &&
                        result.candidates[0].content.parts.length > 0) {
                        const text = result.candidates[0].content.parts[0].text;
                        geminiTextEl.textContent = text;
                    } else {
                        geminiTextEl.textContent = "Could not generate analysis. Please try again later.";
                        console.error('Gemini API response error:', result);
                    }
                } catch (err) {
                    geminiTextEl.textContent = "An error occurred while connecting to the server. Please try again.";
                    console.error('Fetch error:', err);
                } finally {
                    geminiLoadingEl.classList.add('hidden');
                    geminiBtn.disabled = false;
                }
            }
            document.querySelectorAll('[data-game-id]').forEach(card => {
                card.addEventListener('click', (e) => {
                    const gameId = e.currentTarget.dataset.gameId;
                    state.gameData = gameData[gameId];
                    state.currentQuestionIndex = 0;
                    state.answers = {};
                    renderQuiz();
                    showScreen('quiz-section');
                    geminiAnalysisSection.classList.add('hidden');
                    geminiTextEl.textContent = '';
                });
            });
            nextBtn.addEventListener('click', () => {
                if (state.currentQuestionIndex < state.gameData.questions.length - 1) {
                    state.currentQuestionIndex++;
                    renderQuiz();
                } else {
                    calculateResult();
                }
            });
            tryAgainBtn.addEventListener('click', () => {
                showScreen('main-menu');
            });
            cameraBtn.addEventListener('click', async () => {
                showScreen('camera-section');
                try {
                    stream = await navigator.mediaDevices.getUserMedia({ video: { facingMode: 'user' }, audio: false });
                    webcam.srcObject = stream;
                    webcam.play();
                } catch (err) {
                    console.error("Error accessing camera: ", err);
                    messageBox.textContent = "Error: Could not access the camera. Please check permissions.";
                    messageBox.classList.remove('hidden');
                }
            });
            captureBtn.addEventListener('click', () => {
                if (!stream) {
                    messageBox.textContent = "Camera is not ready yet.";
                    messageBox.classList.remove('hidden');
                    return;
                }
                photoCanvas.width = webcam.videoWidth;
                photoCanvas.height = webcam.videoHeight;
                const context = photoCanvas.getContext('2d');
                context.filter = 'grayscale(100%)';
                context.drawImage(webcam, 0, 0, photoCanvas.width, photoCanvas.height);
                context.filter = 'none';
                const overlayImg = new Image();
                const overlayElement = document.querySelector('.camera-overlay-image');
                const svgDataUrl = getComputedStyle(overlayElement).backgroundImage.slice(5, -2);
                overlayImg.onload = () => {
                    const canvasWidth = photoCanvas.width;
                    const canvasHeight = photoCanvas.height;
                    const overlaySize = Math.min(canvasWidth, canvasHeight) * 0.9;
                    const x = (canvasWidth - overlaySize) / 2;
                    const y = (canvasHeight - overlaySize) / 2;
                    context.drawImage(overlayImg, x, y, overlaySize, overlaySize);
                    const dataUrl = photoCanvas.toDataURL('image/png');
                    downloadBtn.href = dataUrl;
                    downloadBtn.classList.remove('hidden');
                    captureBtn.textContent = 'Take Another Photo';
                };
                overlayImg.src = svgDataUrl;
            });
            backToMenuBtn.addEventListener('click', () => {
                if (stream) {
                    stream.getTracks().forEach(track => track.stop());
                }
                showScreen('main-menu');
            });
            geminiBtn.addEventListener('click', () => {
                const styleType = resultTitleEl.textContent;
                getGeminiAnalysis(styleType);
            });
        });
    </script>
</body>
</html>
