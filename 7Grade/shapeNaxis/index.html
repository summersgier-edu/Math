<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ورقة عمل: اكتشف الرسمة المخفية</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Tajawal:wght@400;700;900&display=swap');
        
        body {
            font-family: 'Tajawal', sans-serif;
            background-color: #f8fafc;
            color: #0f172a;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 1rem;
        }

        /* Paper aesthetic for the main container */
        .worksheet-container {
            background-color: white;
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
            border-radius: 1rem;
            width: 100%;
            max-width: 1100px;
            padding: 2rem;
            margin-top: 1rem;
        }

        .canvas-container {
            position: relative;
            background-color: #ffffff;
            border: 2px solid #cbd5e1;
            border-radius: 0.5rem;
            overflow: hidden;
            display: flex;
            justify-content: center;
        }

        canvas {
            cursor: crosshair;
            max-width: 100%;
            height: auto;
        }

        .point-item {
            transition: all 0.2s;
        }
        
        .point-item.active {
            background-color: #eff6ff;
            border-color: #3b82f6;
            transform: scale(1.02);
            box-shadow: 0 4px 6px -1px rgba(59, 130, 246, 0.2);
        }

        .point-item.done {
            background-color: #f0fdf4;
            border-color: #22c55e;
            color: #15803d;
            opacity: 0.8;
        }

        /* Print Styles - Crucial for worksheets! */
        @media print {
            body {
                background-color: white;
                padding: 0;
            }
            .worksheet-container {
                box-shadow: none;
                max-width: 100%;
                width: 100%;
                padding: 0;
                margin: 0;
            }
            .no-print {
                display: none !important;
            }
            .canvas-container {
                border: 1px solid #000;
            }
            .point-item {
                border: 1px solid #000 !important;
                background-color: transparent !important;
                color: #000 !important;
                box-shadow: none !important;
                transform: none !important;
            }
            * {
                print-color-adjust: exact !important;
                -webkit-print-color-adjust: exact !important;
            }
        }

        /* PDF Export Styles (Mimics print mode for html2pdf) */
        .pdf-export {
            background-color: white !important;
            padding: 0 !important;
        }
        .pdf-export .worksheet-container {
            box-shadow: none !important;
            max-width: 100% !important;
            width: 100% !important;
            padding: 0 !important;
            margin: 0 !important;
        }
        .pdf-export .no-print { display: none !important; }
        .pdf-export .canvas-container { border: 1px solid #000 !important; }
        .pdf-export .point-item { 
            border: 1px solid #000 !important; 
            background-color: transparent !important; 
            color: #000 !important; 
            box-shadow: none !important; 
            transform: none !important; 
        }
        .pdf-export #name-date-row { display: flex !important; }
        .pdf-export .print\:bg-transparent { background-color: transparent !important; }
        .pdf-export .print\:p-0 { padding: 0 !important; }
        .pdf-export .print\:border-slate-400 { border-color: #94a3b8 !important; }
        .pdf-export .print\:border-0 { border-width: 0 !important; }
        .pdf-export .print\:border-b-2 { border-bottom-width: 2px !important; }
        .pdf-export .print\:border-black { border-color: #000 !important; }
        .pdf-export .print\:rounded-none { border-radius: 0 !important; }
        .pdf-export #challenge-section { display: block !important; }
    </style>
</head>
<body>

    <!-- Header Actions (Hidden when printing) -->
    <div class="w-full max-w-6xl flex justify-between items-center mb-2 no-print bg-white p-4 rounded-xl shadow-sm border border-slate-200">
        <div>
            <h1 class="text-xl font-black text-indigo-600"><i class="fa-solid fa-pencil-ruler mr-2"></i> التدريب التفاعلي</h1>
            <p class="text-sm text-slate-500">انقر على الشبكة لتوصيل النقاط بالترتيب، أو اطبع الورقة للحل اليدوي.</p>
        </div>
        <div class="flex gap-3">
            <button onclick="resetWorksheet()" class="px-4 py-2 bg-slate-100 hover:bg-slate-200 text-slate-700 rounded-lg font-bold transition flex items-center gap-2">
                <i class="fa-solid fa-rotate-right"></i> إعادة البدء
            </button>
            <button onclick="downloadPDF()" class="px-4 py-2 bg-red-600 hover:bg-red-700 text-white rounded-lg font-bold transition shadow-md flex items-center gap-2">
                <i class="fa-solid fa-file-pdf"></i> تنزيل PDF
            </button>
        </div>
    </div>

    <!-- Main Worksheet -->
    <div class="worksheet-container" id="worksheet-content">
        
        <!-- Worksheet Header -->
        <header class="text-center mb-8 border-b-2 border-slate-200 pb-6">
            <h1 class="text-3xl font-black text-slate-800 mb-2">ورقة عمل: اكتشف الرسمة المخفية 🔍</h1>
            <div id="name-date-row" class="hidden print:flex justify-between items-center mt-6 text-lg font-bold text-slate-700 w-full">
                <span>اسم الطالب: _____________________</span>
                <span>التاريخ: ___ / ___ / _____</span>
            </div>
            <p class="mt-6 text-slate-600 text-lg font-bold bg-slate-100 p-3 rounded-lg print:bg-transparent print:p-0">
                📌 التعليمات: عيّن النقاط الـ 17 التالية على هيئة المحاور بالترتيب، وصِل بين كل نقطة والنقطة التي تليها بخط مستقيم لتكتشف الرسمة السرية!
            </p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-start">
            
            <!-- Left Side: Table of Points -->
            <div class="lg:col-span-4 order-2 lg:order-1">
                <h3 class="text-xl font-bold text-slate-800 mb-4 flex items-center gap-2">
                    <i class="fa-solid fa-list-ol text-indigo-500"></i> قائمة الإحداثيات:
                </h3>
                <!-- Points Grid -->
                <div id="points-list" class="grid grid-cols-2 lg:grid-cols-1 gap-2">
                    <!-- Points will be injected here via JS -->
                </div>

                <div id="success-message" class="hidden mt-6 bg-green-100 border-2 border-green-500 text-green-700 p-4 rounded-xl text-center font-black text-xl shadow-lg no-print transform transition scale-105">
                    🎉 ممتاز! لقد رسمت صاروخاً فضائياً! 🚀
                </div>
                
                <!-- زر إعادة الرسم التلقائي (مخفي في البداية) -->
                <button id="btn-animate" onclick="animateDrawing()" class="hidden mt-4 w-full py-3 bg-fuchsia-600 hover:bg-fuchsia-700 text-white rounded-xl font-black text-lg transition shadow-lg flex items-center justify-center gap-2 no-print transform hover:scale-105">
                    <i class="fa-solid fa-wand-magic-sparkles"></i> إعادة عرض الرسمة ببطء
                </button>
            </div>

            <!-- Right Side: The Cartesian Grid -->
            <div class="lg:col-span-8 order-1 lg:order-2">
                <div class="canvas-container p-2">
                    <!-- High resolution canvas for sharp printing -->
                    <canvas id="gridCanvas" width="800" height="800"></canvas>
                </div>
            </div>
            
        </div>

        <!-- قسم إحصاء وتحليل النقاط -->
        <div class="mt-10 border-t-2 border-slate-200 pt-8 print:break-inside-avoid">
            <h3 class="text-2xl font-bold text-slate-800 mb-4 flex items-center gap-2">
                <i class="fa-solid fa-chart-pie text-indigo-500"></i> إحصاء وتحليل النقاط:
            </h3>
            <p class="text-slate-600 text-lg mb-6 font-bold">
                بعد الانتهاء من رسم الشكل، تأمل قائمة النقاط الـ 17 وسجل عدد النقاط التي تقع في كل من الأماكن التالية:
            </p>
            <div class="grid grid-cols-2 md:grid-cols-3 gap-4 lg:gap-6">
                <div id="q1-container" class="border-2 border-slate-200 rounded-xl p-4 flex justify-between items-center bg-slate-50 print:bg-transparent print:border-slate-400 transition-colors">
                    <span class="font-bold text-slate-700 text-lg">الربع الأول:</span>
                    <input type="text" id="q1-input" inputmode="numeric" class="w-16 h-10 text-center font-black text-xl border border-slate-300 rounded-lg focus:border-indigo-500 focus:outline-none print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent">
                </div>
                <div id="q2-container" class="border-2 border-slate-200 rounded-xl p-4 flex justify-between items-center bg-slate-50 print:bg-transparent print:border-slate-400 transition-colors">
                    <span class="font-bold text-slate-700 text-lg">الربع الثاني:</span>
                    <input type="text" id="q2-input" inputmode="numeric" class="w-16 h-10 text-center font-black text-xl border border-slate-300 rounded-lg focus:border-indigo-500 focus:outline-none print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent">
                </div>
                <div id="q3-container" class="border-2 border-slate-200 rounded-xl p-4 flex justify-between items-center bg-slate-50 print:bg-transparent print:border-slate-400 transition-colors">
                    <span class="font-bold text-slate-700 text-lg">الربع الثالث:</span>
                    <input type="text" id="q3-input" inputmode="numeric" class="w-16 h-10 text-center font-black text-xl border border-slate-300 rounded-lg focus:border-indigo-500 focus:outline-none print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent">
                </div>
                <div id="q4-container" class="border-2 border-slate-200 rounded-xl p-4 flex justify-between items-center bg-slate-50 print:bg-transparent print:border-slate-400 transition-colors">
                    <span class="font-bold text-slate-700 text-lg">الربع الرابع:</span>
                    <input type="text" id="q4-input" inputmode="numeric" class="w-16 h-10 text-center font-black text-xl border border-slate-300 rounded-lg focus:border-indigo-500 focus:outline-none print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent">
                </div>
                <div id="x-axis-container" class="border-2 border-slate-200 rounded-xl p-4 flex justify-between items-center bg-slate-50 print:bg-transparent print:border-slate-400 transition-colors">
                    <span class="font-bold text-slate-700 text-lg">على محور X:</span>
                    <input type="text" id="x-axis-input" inputmode="numeric" class="w-16 h-10 text-center font-black text-xl border border-slate-300 rounded-lg focus:border-indigo-500 focus:outline-none print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent">
                </div>
                <div id="y-axis-container" class="border-2 border-slate-200 rounded-xl p-4 flex justify-between items-center bg-slate-50 print:bg-transparent print:border-slate-400 transition-colors">
                    <span class="font-bold text-slate-700 text-lg">على محور Y:</span>
                    <input type="text" id="y-axis-input" inputmode="numeric" class="w-16 h-10 text-center font-black text-xl border border-slate-300 rounded-lg focus:border-indigo-500 focus:outline-none print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent">
                </div>
            </div>
            
            <!-- سؤال التفكير العالي (التماثل والانعكاس) -->
            <div class="mt-6 border-2 border-indigo-200 bg-indigo-50 p-6 rounded-xl print:bg-transparent print:border-slate-400">
                <h4 class="text-xl font-bold text-indigo-700 mb-3 flex items-center gap-2">
                    <i class="fa-solid fa-lightbulb text-amber-500"></i> سؤال التفكير والتأمل (التماثل):
                </h4>
                <p class="text-slate-700 font-bold mb-4 text-lg">
                    الصاروخ الفضائي متماثل (نصفه الأيمن يشبه الأيسر). تأمل النقطة <span class="font-mono text-indigo-600" dir="ltr">( +2 , +4 )</span> التي تمثل يمين مقدمة الصاروخ. 
                    <br>ما هي النقطة التي تمثل الجزء المقابل لها تماماً (انعكاسها) في الجهة اليسرى للصاروخ؟
                </p>
                <div class="flex items-center gap-4 text-xl font-black font-mono mt-4" dir="ltr">
                    ( X: <input type="text" id="sym-x-input" class="w-16 h-10 text-center border-2 border-slate-300 rounded-lg focus:border-indigo-500 outline-none transition-colors print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent"> ,
                      Y: <input type="text" id="sym-y-input" class="w-16 h-10 text-center border-2 border-slate-300 rounded-lg focus:border-indigo-500 outline-none transition-colors print:border-0 print:border-b-2 print:border-black print:rounded-none print:bg-transparent"> )
                </div>
            </div>

            <!-- أزرار التحقق (لا تظهر في الطباعة) -->
            <div class="mt-8 flex flex-col items-center gap-4 no-print">
                <button onclick="checkStatsAnswers()" class="px-8 py-3 bg-indigo-600 hover:bg-indigo-700 text-white rounded-xl font-black text-xl transition shadow-lg flex items-center gap-3 transform hover:scale-105">
                    <i class="fa-solid fa-check-double"></i> تحقق من الإجابات
                </button>
                <div id="stats-feedback" class="hidden text-lg font-bold px-6 py-4 rounded-xl text-center w-full max-w-2xl shadow-sm transition-all duration-300"></div>
            </div>
        </div>

        <!-- قسم تحدي الزميل (الهندسة العكسية) يظهر فقط في الطباعة -->
        <div id="challenge-section" class="hidden print:block mt-16 border-t-4 border-dashed border-slate-300 pt-10 print:break-before-page">
            <h2 class="text-3xl font-black text-slate-800 mb-4 text-center">🎯 تحدَّ زميلك! (الهندسة العكسية)</h2>
            <p class="text-slate-600 text-lg font-bold text-center mb-8 max-w-4xl mx-auto">
                <i class="fa-solid fa-pen-nib text-indigo-500 ml-1"></i>
                أطلق العنان لخيالك! ارسم شكلاً بسيطاً (مثل نجمة، منزل، أو قارب) على الشبكة التالية. 
                اكتب إحداثيات زوايا رسمتك بالترتيب في الجدول، ثم اطوِ الورقة (أو أعطِ قائمة النقاط فقط) لزميلك ليحاول اكتشاف ورسم الشكل الخاص بك!
            </p>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-start">
                
                <!-- Challenge Canvas -->
                <div class="flex justify-center p-2 border-2 border-slate-200 rounded-xl bg-white shadow-sm">
                    <canvas id="challengeCanvas" width="600" height="600" class="max-w-full h-auto"></canvas>
                </div>
                
                <!-- Blank Coordinates List -->
                <div class="bg-slate-50 border-2 border-slate-200 rounded-xl p-6 print:bg-transparent print:border-slate-400">
                    <h3 class="text-xl font-bold text-slate-800 mb-6 border-b-2 border-slate-200 pb-2">
                        قائمة الإحداثيات السرية الخاصة بي:
                    </h3>
                    <div class="grid grid-cols-2 gap-y-8 gap-x-4" dir="ltr">
                        <!-- Generate 12 empty coordinate lines -->
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">1.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">2.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">3.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">4.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">5.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">6.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">7.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">8.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">9.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">10.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">11.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                        <div class="font-mono text-lg font-bold text-slate-600 flex items-center gap-2"><span class="w-6 text-right">12.</span> ( <span class="w-12 border-b-2 border-slate-400 inline-block"></span> , <span class="w-12 border-b-2 border-slate-400 inline-block"></span> )</div>
                    </div>
                </div>
            </div>
        </div>

    </div>

    <!-- Application Logic -->
    <script>
        // --- Configuration & Data ---
        // 17 Points that draw a Rocket Spacecraft
        const shapePoints = [
            { id: 1,  x: 0,  y: 8 },   // Tip
            { id: 2,  x: 2,  y: 4 },   // Right nose curve
            { id: 3,  x: 2,  y: 0 },   // Right body mid (على محور X)
            { id: 4,  x: 2,  y: -2 },  // Right body low
            { id: 5,  x: 4,  y: -5 },  // Right fin top
            { id: 6,  x: 4,  y: -7 },  // Right fin bottom tip
            { id: 7,  x: 2,  y: -7 },  // Right fin inner base
            { id: 8,  x: 1,  y: -9 },  // Right nozzle
            { id: 9,  x: 0,  y: -8 },  // Nozzle middle dip
            { id: 10, x: -1, y: -9 },  // Left nozzle
            { id: 11, x: -2, y: -7 },  // Left fin inner base
            { id: 12, x: -4, y: -7 },  // Left fin bottom tip
            { id: 13, x: -4, y: -5 },  // Left fin top
            { id: 14, x: -2, y: -2 },  // Left body low
            { id: 15, x: -2, y: 0 },   // Left body mid (على محور X)
            { id: 16, x: -2, y: 4 },   // Left nose curve
            { id: 17, x: 0,  y: 8 }    // Back to Tip (closes the shape)
        ];

        let currentStep = 0; // Index of the point the user needs to click next
        let userPath = [];   // Stores successfully clicked points
        
        const gridRange = 10; // -10 to +10

        // --- Audio Context for Game-like feedback ---
        let audioCtx = null;
        function getAudioCtx() {
            if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
            if (audioCtx.state === 'suspended') audioCtx.resume();
            return audioCtx;
        }

        function playSound(type) {
            try {
                const ctx = getAudioCtx();
                const now = ctx.currentTime;
                const osc = ctx.createOscillator();
                const gain = ctx.createGain();
                
                if (type === 'success') {
                    osc.type = 'sine';
                    osc.frequency.setValueAtTime(600, now);
                    osc.frequency.exponentialRampToValueAtTime(1200, now + 0.1);
                    gain.gain.setValueAtTime(0.1, now);
                    gain.gain.exponentialRampToValueAtTime(0.01, now + 0.2);
                    osc.connect(gain); gain.connect(ctx.destination);
                    osc.start(now); osc.stop(now + 0.2);
                } else if (type === 'error') {
                    osc.type = 'sine';
                    osc.frequency.setValueAtTime(300, now);
                    osc.frequency.exponentialRampToValueAtTime(150, now + 0.2);
                    gain.gain.setValueAtTime(0.1, now);
                    gain.gain.exponentialRampToValueAtTime(0.01, now + 0.2);
                    osc.connect(gain); gain.connect(ctx.destination);
                    osc.start(now); osc.stop(now + 0.2);
                } else if (type === 'win') {
                    // Win chord
                    [523.25, 659.25, 783.99, 1046.50].forEach((freq, i) => {
                        const o = ctx.createOscillator();
                        const g = ctx.createGain();
                        o.type = 'triangle';
                        o.frequency.setValueAtTime(freq, now + i * 0.1);
                        g.gain.setValueAtTime(0, now + i * 0.1);
                        g.gain.linearRampToValueAtTime(0.1, now + i * 0.1 + 0.05);
                        g.gain.exponentialRampToValueAtTime(0.001, now + i * 0.1 + 0.5);
                        o.connect(g); g.connect(ctx.destination);
                        o.start(now + i * 0.1); o.stop(now + i * 0.1 + 0.6);
                    });
                }
            } catch (e) {}
        }

        // --- DOM Elements & Canvas ---
        const canvas = document.getElementById('gridCanvas');
        const ctx = canvas.getContext('2d');
        const pointsListDiv = document.getElementById('points-list');

        function initApp() {
            renderPointsList();
            drawGrid();
            drawChallengeGrid(); // رسم شبكة تحدي الزميل
            
            canvas.addEventListener('click', (e) => {
                getAudioCtx(); // initialize audio on first click
                handleCanvasClick(e);
            });
        }

        function renderPointsList() {
            pointsListDiv.innerHTML = '';
            shapePoints.forEach((pt, index) => {
                const el = document.createElement('div');
                el.id = `point-item-${index}`;
                
                // Base classes
                el.className = `point-item border-2 border-slate-200 rounded-lg p-3 flex justify-between items-center text-slate-600 font-bold`;
                
                if (index === currentStep) {
                    el.classList.add('active'); // highlight current target
                } else if (index < currentStep) {
                    el.classList.add('done'); // mark as done
                }

                // Format coordinates with sign
                const fmtX = pt.x > 0 ? `+${pt.x}` : pt.x;
                const fmtY = pt.y > 0 ? `+${pt.y}` : pt.y;

                el.innerHTML = `
                    <span class="w-24 text-sm">النقطة ${pt.id}:</span>
                    <span class="font-mono text-lg tracking-wider" dir="ltr">( ${fmtX} , ${fmtY} )</span>
                    <i class="fa-solid ${index < currentStep ? 'fa-check-circle' : 'fa-circle'} text-lg opacity-80"></i>
                `;
                pointsListDiv.appendChild(el);
            });

            if (currentStep >= shapePoints.length) {
                document.getElementById('success-message').classList.remove('hidden');
                document.getElementById('btn-animate').classList.remove('hidden');
            } else {
                document.getElementById('success-message').classList.add('hidden');
                document.getElementById('btn-animate').classList.add('hidden');
            }
        }

        // --- Drawing Logic ---
        function getCanvasMetrics() {
            const w = canvas.width;
            const h = canvas.height;
            const originX = w / 2;
            const originY = h / 2;
            const stepX = w / (gridRange * 2);
            const stepY = h / (gridRange * 2);
            return { w, h, originX, originY, stepX, stepY };
        }

        function coordToPx(x, y) {
            const { originX, originY, stepX, stepY } = getCanvasMetrics();
            return {
                px: originX + (x * stepX),
                py: originY - (y * stepY) // Y is inverted in canvas
            };
        }

        function pxToCoord(px, py) {
            const { originX, originY, stepX, stepY } = getCanvasMetrics();
            const x = Math.round((px - originX) / stepX);
            const y = Math.round((originY - py) / stepY);
            return { x, y };
        }

        function drawGrid() {
            const { w, h, originX, originY, stepX, stepY } = getCanvasMetrics();
            
            // Clear canvas
            ctx.fillStyle = '#ffffff';
            ctx.fillRect(0, 0, w, h);

            // 1. Draw Grid Lines (thin gray)
            ctx.lineWidth = 1.5;
            ctx.strokeStyle = '#e2e8f0'; // slate-200
            
            for (let i = -gridRange; i <= gridRange; i++) {
                // Vertical
                const xPos = originX + (i * stepX);
                ctx.beginPath();
                ctx.moveTo(xPos, 0); ctx.lineTo(xPos, h);
                ctx.stroke();

                // Horizontal
                const yPos = originY - (i * stepY);
                ctx.beginPath();
                ctx.moveTo(0, yPos); ctx.lineTo(w, yPos);
                ctx.stroke();
            }

            // 2. Draw Main Axes (thick dark)
            ctx.lineWidth = 3;
            ctx.strokeStyle = '#0f172a'; // slate-900

            ctx.beginPath(); // X Axis
            ctx.moveTo(0, originY); ctx.lineTo(w, originY);
            ctx.stroke();

            ctx.beginPath(); // Y Axis
            ctx.moveTo(originX, 0); ctx.lineTo(originX, h);
            ctx.stroke();

            // 3. Draw Axis Labels
            ctx.font = 'bold 16px font-mono, sans-serif';
            ctx.fillStyle = '#475569'; // slate-600
            ctx.textBaseline = 'middle';
            ctx.textAlign = 'center';

            for (let i = -gridRange; i <= gridRange; i++) {
                if (i === 0) continue;
                
                // X axis numbers
                const xp = originX + (i * stepX);
                ctx.fillText(i > 0 ? `+${i}` : i, xp, originY + 22);

                // Y axis numbers
                const yp = originY - (i * stepY);
                ctx.textAlign = 'right';
                ctx.fillText(i > 0 ? `+${i}` : i, originX - 10, yp);
                ctx.textAlign = 'center';
            }

            // Origin Label
            ctx.fillStyle = '#ef4444'; // red-500
            ctx.font = 'bold 16px font-mono';
            ctx.textAlign = 'right';
            ctx.fillText('(0,0)', originX - 10, originY + 22);

            // كتابة أسماء الأرباع بخط شفاف كخلفية مريحة
            ctx.font = '900 36px Tajawal, sans-serif';
            ctx.fillStyle = 'rgba(249, 115, 22, 0.12)'; // برتقالي شفاف
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            
            const qOffX = (gridRange * stepX) / 2;
            const qOffY = (gridRange * stepY) / 2;

            ctx.fillText('الربع الأول', originX + qOffX, originY - qOffY);
            ctx.fillText('الربع الثاني', originX - qOffX, originY - qOffY);
            ctx.fillText('الربع الثالث', originX - qOffX, originY + qOffY);
            ctx.fillText('الربع الرابع', originX + qOffX, originY + qOffY);

            // 4. Draw Student Progress (Lines and Dots)
            if (userPath.length > 0) {
                // Draw connecting lines
                ctx.beginPath();
                ctx.lineWidth = 5;
                ctx.strokeStyle = '#4f46e5'; // indigo-600
                ctx.lineJoin = 'round';
                ctx.lineCap = 'round';

                const startPx = coordToPx(userPath[0].x, userPath[0].y);
                ctx.moveTo(startPx.px, startPx.py);

                for (let i = 1; i < userPath.length; i++) {
                    const nextPx = coordToPx(userPath[i].x, userPath[i].y);
                    ctx.lineTo(nextPx.px, nextPx.py);
                }
                ctx.stroke();

                // Draw dots at clicked points
                userPath.forEach((pt, idx) => {
                    const pos = coordToPx(pt.x, pt.y);
                    ctx.beginPath();
                    ctx.fillStyle = '#ffffff';
                    ctx.arc(pos.px, pos.py, 8, 0, Math.PI * 2);
                    ctx.fill();
                    
                    ctx.beginPath();
                    ctx.lineWidth = 3;
                    ctx.strokeStyle = '#4f46e5';
                    ctx.arc(pos.px, pos.py, 8, 0, Math.PI * 2);
                    ctx.stroke();
                    
                    // Add point number
                    ctx.fillStyle = '#4f46e5';
                    ctx.font = 'bold 12px sans-serif';
                    ctx.textAlign = 'center';
                    ctx.fillText(idx + 1, pos.px, pos.py - 15);
                });
            }
        }

        function drawChallengeGrid() {
            const chCanvas = document.getElementById('challengeCanvas');
            const chCtx = chCanvas.getContext('2d');
            
            const w = chCanvas.width;
            const h = chCanvas.height;
            const originX = w / 2;
            const originY = h / 2;
            const stepX = w / (gridRange * 2);
            const stepY = h / (gridRange * 2);

            chCtx.fillStyle = '#ffffff';
            chCtx.fillRect(0, 0, w, h);

            chCtx.lineWidth = 1.5;
            chCtx.strokeStyle = '#e2e8f0'; 
            
            for (let i = -gridRange; i <= gridRange; i++) {
                const xPos = originX + (i * stepX);
                chCtx.beginPath();
                chCtx.moveTo(xPos, 0); chCtx.lineTo(xPos, h);
                chCtx.stroke();

                const yPos = originY - (i * stepY);
                chCtx.beginPath();
                chCtx.moveTo(0, yPos); chCtx.lineTo(w, yPos);
                chCtx.stroke();
            }

            chCtx.lineWidth = 3;
            chCtx.strokeStyle = '#0f172a';
            chCtx.beginPath(); chCtx.moveTo(0, originY); chCtx.lineTo(w, originY); chCtx.stroke();
            chCtx.beginPath(); chCtx.moveTo(originX, 0); chCtx.lineTo(originX, h); chCtx.stroke();

            chCtx.font = 'bold 12px font-mono, sans-serif';
            chCtx.fillStyle = '#94a3b8';
            chCtx.textBaseline = 'middle';
            chCtx.textAlign = 'center';

            for (let i = -gridRange; i <= gridRange; i++) {
                if (i === 0) continue;
                const xp = originX + (i * stepX);
                chCtx.fillText(i > 0 ? `+${i}` : i, xp, originY + 16);

                const yp = originY - (i * stepY);
                chCtx.textAlign = 'right';
                chCtx.fillText(i > 0 ? `+${i}` : i, originX - 6, yp);
                chCtx.textAlign = 'center';
            }
        }

        // --- Interaction ---
        function handleCanvasClick(e) {
            // Ignore clicks if worksheet is complete
            if (currentStep >= shapePoints.length) return;

            const rect = canvas.getBoundingClientRect();
            // Scale correctly based on actual canvas layout vs HTML attributes
            const scaleX = canvas.width / rect.width;
            const scaleY = canvas.height / rect.height;

            const clickPxX = (e.clientX - rect.left) * scaleX;
            const clickPxY = (e.clientY - rect.top) * scaleY;

            // Snap to nearest grid coordinate
            const clickedCoord = pxToCoord(clickPxX, clickPxY);
            
            // Limit bounds
            if(Math.abs(clickedCoord.x) > 10 || Math.abs(clickedCoord.y) > 10) return;

            // Check if it matches the current target
            const targetPoint = shapePoints[currentStep];

            if (clickedCoord.x === targetPoint.x && clickedCoord.y === targetPoint.y) {
                // Correct!
                playSound('success');
                userPath.push({ x: targetPoint.x, y: targetPoint.y });
                currentStep++;
                
                renderPointsList();
                drawGrid();

                if (currentStep >= shapePoints.length) {
                    setTimeout(() => playSound('win'), 200);
                }

            } else {
                // Wrong click feedback
                playSound('error');
                showWrongClick(clickedCoord.x, clickedCoord.y);
            }
        }

        function showWrongClick(x, y) {
            // Re-render base grid first to clear any old Xs
            drawGrid();
            
            const pos = coordToPx(x, y);
            ctx.fillStyle = '#ef4444'; // red-500
            ctx.font = 'bold 24px sans-serif';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('❌', pos.px, pos.py);

            // Remove the X after a short delay
            setTimeout(() => {
                drawGrid();
            }, 600);
        }
        
        // --- Auto-Draw Animation ---
        function animateDrawing() {
            const btn = document.getElementById('btn-animate');
            btn.disabled = true;
            btn.classList.add('opacity-50', 'cursor-not-allowed');
            btn.innerHTML = '<i class="fa-solid fa-spinner fa-spin"></i> جاري الرسم...';

            const fullPath = [...userPath];
            userPath = []; // إفراغ المسار للبدء من جديد
            drawGrid();
            
            let i = 0;
            function drawNext() {
                if (i < fullPath.length) {
                    userPath.push(fullPath[i]);
                    drawGrid();
                    playSound('success'); // صوت نبضة خفيفة مع كل نقطة
                    i++;
                    setTimeout(drawNext, 250); // سرعة الحركة بين النقاط (250ms)
                } else {
                    btn.disabled = false;
                    btn.classList.remove('opacity-50', 'cursor-not-allowed');
                    btn.innerHTML = '<i class="fa-solid fa-wand-magic-sparkles"></i> إعادة عرض الرسمة ببطء';
                    playSound('win');
                }
            }
            // بدء التحريك بعد مهلة قصيرة
            setTimeout(drawNext, 400);
        }

        function resetWorksheet() {
            currentStep = 0;
            userPath = [];
            renderPointsList();
            drawGrid();

            // Clear stats inputs and feedback
            const fields = ['q1', 'q2', 'q3', 'q4', 'x-axis', 'y-axis'];
            fields.forEach(id => {
                const inputEl = document.getElementById(`${id}-input`);
                const containerEl = document.getElementById(`${id}-container`);
                if(inputEl) inputEl.value = '';
                if(containerEl) {
                    containerEl.classList.remove('bg-green-100', 'border-green-500', 'bg-red-100', 'border-red-500');
                    containerEl.classList.add('bg-slate-50', 'border-slate-200');
                }
            });
            
            // Clear Symmetry Inputs
            const symX = document.getElementById('sym-x-input');
            const symY = document.getElementById('sym-y-input');
            if(symX) { symX.value = ''; symX.classList.remove('bg-green-100', 'border-green-500', 'bg-red-100', 'border-red-500'); }
            if(symY) { symY.value = ''; symY.classList.remove('bg-green-100', 'border-green-500', 'bg-red-100', 'border-red-500'); }

            const feedback = document.getElementById('stats-feedback');
            if(feedback) feedback.classList.add('hidden');
        }

        // --- Stats Checking Logic ---
        function checkStatsAnswers() {
            // Calculate correct answers dynamically based on shapePoints
            let counts = { q1: 0, q2: 0, q3: 0, q4: 0, 'x-axis': 0, 'y-axis': 0 };
            
            shapePoints.forEach(pt => {
                if (pt.x === 0) counts['y-axis']++;
                else if (pt.y === 0) counts['x-axis']++;
                else if (pt.x > 0 && pt.y > 0) counts.q1++;
                else if (pt.x < 0 && pt.y > 0) counts.q2++;
                else if (pt.x < 0 && pt.y < 0) counts.q3++;
                else if (pt.x > 0 && pt.y < 0) counts.q4++;
            });

            let allCorrect = true;
            let hasAttempt = false;

            const fields = ['q1', 'q2', 'q3', 'q4', 'x-axis', 'y-axis'];
            
            fields.forEach(id => {
                const inputEl = document.getElementById(`${id}-input`);
                const containerEl = document.getElementById(`${id}-container`);
                const val = inputEl.value.trim();
                
                // Reset styles
                containerEl.classList.remove('bg-slate-50', 'border-slate-200', 'bg-green-100', 'border-green-500', 'bg-red-100', 'border-red-500');
                
                if (val === '') {
                    containerEl.classList.add('bg-slate-50', 'border-slate-200');
                    allCorrect = false;
                } else {
                    hasAttempt = true;
                    if (parseInt(val) === counts[id]) {
                        containerEl.classList.add('bg-green-100', 'border-green-500');
                    } else {
                        containerEl.classList.add('bg-red-100', 'border-red-500');
                        allCorrect = false;
                    }
                }
            });

            // Check Symmetry Question (Reflection of +2, +4 across Y-axis is -2, +4)
            const symXInput = document.getElementById('sym-x-input');
            const symYInput = document.getElementById('sym-y-input');
            const symXVal = symXInput.value.trim();
            const symYVal = symYInput.value.trim();
            
            symXInput.classList.remove('bg-green-100', 'border-green-500', 'bg-red-100', 'border-red-500');
            symYInput.classList.remove('bg-green-100', 'border-green-500', 'bg-red-100', 'border-red-500');
            
            if (symXVal === '' || symYVal === '') {
                allCorrect = false;
            } else {
                hasAttempt = true;
                // Correct X is -2
                if (parseInt(symXVal) === -2) {
                    symXInput.classList.add('bg-green-100', 'border-green-500');
                } else {
                    symXInput.classList.add('bg-red-100', 'border-red-500');
                    allCorrect = false;
                }
                
                // Correct Y is +4
                if (parseInt(symYVal) === 4) {
                    symYInput.classList.add('bg-green-100', 'border-green-500');
                } else {
                    symYInput.classList.add('bg-red-100', 'border-red-500');
                    allCorrect = false;
                }
            }

            const feedback = document.getElementById('stats-feedback');
            feedback.classList.remove('hidden', 'bg-green-100', 'text-green-700', 'border-green-500', 'bg-red-100', 'text-red-700', 'border-red-500', 'bg-amber-100', 'text-amber-700', 'border-amber-500');
            
            if (!hasAttempt) {
                feedback.classList.add('bg-amber-100', 'text-amber-700', 'border-2', 'border-amber-500');
                feedback.innerHTML = '<i class="fa-solid fa-triangle-exclamation mr-2"></i> الرجاء إدخال الأرقام في المربعات أولاً.';
            } else if (allCorrect) {
                playSound('win');
                feedback.classList.add('bg-green-100', 'text-green-700', 'border-2', 'border-green-500');
                feedback.innerHTML = '<i class="fa-solid fa-star mr-2"></i> رائع! جميع إجاباتك صحيحة، لقد قمت بتحليل الرسمة بدقة.';
            } else {
                playSound('error');
                feedback.classList.add('bg-red-100', 'text-red-700', 'border-2', 'border-red-500');
                feedback.innerHTML = '<i class="fa-solid fa-circle-xmark mr-2"></i> يوجد بعض الأخطاء. راجع المربعات المحددة باللون الأحمر وحاول مجدداً.';
            }
        }

        // --- PDF Download Logic ---
        function downloadPDF() {
            // إضافة كلاس التصدير لتحويل الواجهة إلى مظهر ورقة العمل المطبوعة
            document.body.classList.add('pdf-export');
            
            const element = document.getElementById('worksheet-content');
            
            const opt = {
                margin:       0.3,
                filename:     'ورقة_عمل_اكتشف_الرسمة.pdf',
                image:        { type: 'jpeg', quality: 0.98 },
                html2canvas:  { scale: 2, useCORS: true, logging: false },
                jsPDF:        { unit: 'in', format: 'a4', orientation: 'portrait' }
            };

            // توليد الـ PDF ثم إزالة كلاس التصدير للعودة للشكل التفاعلي
            html2pdf().set(opt).from(element).save().then(() => {
                document.body.classList.remove('pdf-export');
            });
        }

        // Boot
        window.onload = initApp;
    </script>
</body>
</html>
