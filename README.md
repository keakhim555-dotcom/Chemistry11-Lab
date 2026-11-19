<!DOCTYPE html>
<html lang="km">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>មន្ទីរពិសោធន៍គីមីវិទ្យា ថ្នាក់ទី១១ ៖ ការវាស់ប៉ូតង់ស្យែលស្តង់ដា (SHE)</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Khmer Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Battambang:wght@400;700&family=Kantumruy+Pro:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <!-- Tone.js for subtle feedback sounds -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.49/Tone.js"></script>

    <style>
        body {
            font-family: 'Kantumruy Pro', 'Battambang', sans-serif;
            background-color: #f1f5f9;
            color: #0f172a;
        }
        ::-webkit-scrollbar {
            width: 7px;
            height: 7px;
        }
        ::-webkit-scrollbar-track {
            background: #e2e8f0;
        }
        ::-webkit-scrollbar-thumb {
            background: #94a3b8;
            border-radius: 9999px;
        }
        @media print {
            body * { visibility: hidden; }
            #printable-area, #printable-area * { visibility: visible; }
            #printable-area {
                position: absolute;
                left: 0; top: 0; width: 100%;
                background: white !important; padding: 0 !important;
            }
            .no-print { display: none !important; }
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- Header Navigation -->
    <header class="bg-gradient-to-r from-blue-900 via-indigo-900 to-slate-900 text-white shadow-lg sticky top-0 z-50 no-print">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-3">
            <div class="flex flex-col lg:flex-row lg:items-center lg:justify-between gap-3">
                <div class="flex items-center gap-3">
                    <div class="bg-amber-400/20 border border-amber-300/40 p-2.5 rounded-2xl">
                        <i data-lucide="zap" class="w-7 h-7 text-amber-300"></i>
                    </div>
                    <div>
                        <div class="flex flex-wrap items-center gap-2">
                            <h1 class="text-base sm:text-xl font-bold tracking-wide">មន្ទីរពិសោធន៍គីមីវិទ្យាអនឡាញ • ថ្នាក់ទី១១</h1>
                            <span class="text-[11px] bg-sky-400/20 text-sky-200 border border-sky-300/30 px-2.5 py-0.5 rounded-full font-semibold">អេឡិចត្រូគីមី</span>
                        </div>
                        <p class="text-xs text-blue-100/90">៣.១.៣. ការវាស់ប៉ូតង់ស្យែលស្តង់ដានៃគូរេដុក ដោយប្រើអេឡិចត្រូតអ៊ីដ្រូសែនស្តង់ដា (SHE)</p>
                    </div>
                </div>

                <!-- Navigation Tabs -->
                <nav class="flex flex-wrap gap-1.5 bg-black/30 p-1.5 rounded-2xl">
                    <button onclick="switchTab('lab')" id="tab-lab" class="tab-btn flex items-center gap-1.5 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold transition-all bg-white text-indigo-950 shadow cursor-pointer">
                        <i data-lucide="flask-conical" class="w-4 h-4"></i>
                        <span>បន្ទប់ពិសោធន៍និម្មិត</span>
                    </button>
                    <button onclick="switchTab('theory')" id="tab-theory" class="tab-btn flex items-center gap-1.5 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold transition-all text-white hover:bg-white/15 cursor-pointer">
                        <i data-lucide="book-open" class="w-4 h-4"></i>
                        <span>សង្ខេបមេរៀន &amp; តារាង E°</span>
                    </button>
                </nav>
            </div>
        </div>
    </header>

    <!-- Main Container -->
    <main class="flex-grow max-w-7xl w-full mx-auto px-3 sm:px-6 lg:px-8 py-5">

        <!-- ========================================================== -->
        <!-- TAB 1: INTERACTIVE ELECTROCHEMICAL CELL LAB                -->
        <!-- ========================================================== -->
        <section id="view-lab" class="tab-view space-y-5">

            <!-- Controls & Half-Cell Selector Bar -->
            <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-4 sm:p-5 space-y-4">
                <div class="flex flex-wrap items-center justify-between gap-2 border-b border-slate-100 pb-3">
                    <div class="flex items-center gap-2">
                        <span class="bg-indigo-100 text-indigo-800 text-xs font-bold px-2.5 py-1 rounded-lg">លក្ខខណ្ឌស្តង់ដា</span>
                        <h2 class="font-bold text-slate-800 text-sm sm:text-base">សីតុណ្ហភាព 298 K (25°C) • សម្ពាធឧស្ម័ន H₂ = 1 bar • កំហាប់អ៊ីយ៉ុង = 1 M</h2>
                    </div>
                    <div class="flex items-center gap-2 text-xs text-slate-600 bg-slate-100 px-3 py-1 rounded-full font-semibold">
                        <span>E°(H⁺/H₂) = 0.00 V</span>
                    </div>
                </div>

                <!-- Metal Electrode Picker -->
                <div class="space-y-2">
                    <label class="text-xs font-bold text-slate-700 block">១. ជ្រើសរើសកន្លះពិលលោហៈ (Mⁿ⁺/M) ដើម្បីភ្ជាប់ជាមួយអេឡិចត្រូតអ៊ីដ្រូសែនស្តង់ដា (SHE) ៖</label>
                    <div class="grid grid-cols-2 sm:grid-cols-5 gap-2.5">
                        <button type="button" onclick="selectCouple('Cu')" id="btn-couple-Cu" class="couple-card flex items-center gap-2.5 p-2.5 rounded-xl border-2 border-indigo-600 bg-indigo-50/70 text-left transition-all cursor-pointer">
                            <span class="w-8 h-8 rounded-lg bg-amber-700 text-white font-bold text-xs flex items-center justify-center shrink-0 shadow-xs">Cu</span>
                            <div>
                                <div class="text-xs font-bold text-slate-900">Cu²⁺ / Cu</div>
                                <div class="text-[11px] text-emerald-700 font-semibold">E° = +0.34 V</div>
                            </div>
                        </button>

                        <button type="button" onclick="selectCouple('Zn')" id="btn-couple-Zn" class="couple-card flex items-center gap-2.5 p-2.5 rounded-xl border-2 border-slate-200 bg-white hover:border-slate-300 text-left transition-all cursor-pointer">
                            <span class="w-8 h-8 rounded-lg bg-slate-500 text-white font-bold text-xs flex items-center justify-center shrink-0 shadow-xs">Zn</span>
                            <div>
                                <div class="text-xs font-bold text-slate-900">Zn²⁺ / Zn</div>
                                <div class="text-[11px] text-rose-700 font-semibold">E° = -0.76 V</div>
                            </div>
                        </button>

                        <button type="button" onclick="selectCouple('Ag')" id="btn-couple-Ag" class="couple-card flex items-center gap-2.5 p-2.5 rounded-xl border-2 border-slate-200 bg-white hover:border-slate-300 text-left transition-all cursor-pointer">
                            <span class="w-8 h-8 rounded-lg bg-slate-300 text-slate-900 font-bold text-xs flex items-center justify-center shrink-0 shadow-xs">Ag</span>
                            <div>
                                <div class="text-xs font-bold text-slate-900">Ag⁺ / Ag</div>
                                <div class="text-[11px] text-emerald-700 font-semibold">E° = +0.80 V</div>
                            </div>
                        </button>

                        <button type="button" onclick="selectCouple('Fe')" id="btn-couple-Fe" class="couple-card flex items-center gap-2.5 p-2.5 rounded-xl border-2 border-slate-200 bg-white hover:border-slate-300 text-left transition-all cursor-pointer">
                            <span class="w-8 h-8 rounded-lg bg-zinc-600 text-white font-bold text-xs flex items-center justify-center shrink-0 shadow-xs">Fe</span>
                            <div>
                                <div class="text-xs font-bold text-slate-900">Fe²⁺ / Fe</div>
                                <div class="text-[11px] text-rose-700 font-semibold">E° = -0.44 V</div>
                            </div>
                        </button>

                        <button type="button" onclick="selectCouple('Mg')" id="btn-couple-Mg" class="couple-card flex items-center gap-2.5 p-2.5 rounded-xl border-2 border-slate-200 bg-white hover:border-slate-300 text-left transition-all cursor-pointer">
                            <span class="w-8 h-8 rounded-lg bg-slate-400 text-slate-950 font-bold text-xs flex items-center justify-center shrink-0 shadow-xs">Mg</span>
                            <div>
                                <div class="text-xs font-bold text-slate-900">Mg²⁺ / Mg</div>
                                <div class="text-[11px] text-rose-700 font-semibold">E° = -2.37 V</div>
                            </div>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Main Lab Workspace Grid -->
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-5 items-start">

                <!-- Left Simulation Canvas (7 cols) -->
                <div class="lg:col-span-7 bg-white rounded-2xl shadow-sm border border-slate-200 overflow-hidden flex flex-col">
                    <div class="bg-slate-50 border-b border-slate-200 px-4 py-3 flex flex-wrap items-center justify-between gap-2">
                        <div class="flex items-center gap-2">
                            <span id="circuit-dot" class="w-2.5 h-2.5 rounded-full bg-amber-500"></span>
                            <span id="circuit-status" class="text-xs sm:text-sm font-bold text-slate-800">សៀគ្វីចំហ • ចុច «ភ្ជាប់សៀគ្វី / បើកឧស្ម័ន H₂» ដើម្បីវាស់</span>
                        </div>
                        <div class="bg-slate-900 text-emerald-400 px-3 py-1 rounded-lg font-mono text-xs sm:text-sm font-bold tracking-wider">
                            V = <span id="volt-badge">0.00 V</span>
                        </div>
                    </div>

                    <!-- Interactive Canvas -->
                    <div class="relative w-full bg-gradient-to-b from-slate-50 via-white to-slate-100 min-h-[450px] flex items-center justify-center p-2">
                        <canvas id="cellCanvas" class="w-full h-full rounded-xl"></canvas>
                    </div>

                    <!-- Action Toolbar -->
                    <div class="bg-slate-50 border-t border-slate-200 p-3.5 flex flex-wrap items-center justify-between gap-2.5">
                        <div class="flex flex-wrap items-center gap-2">
                            <button id="btn-toggle-circuit" onclick="toggleCircuit()" class="flex items-center gap-2 bg-indigo-600 hover:bg-indigo-700 active:scale-95 text-white font-semibold px-4 py-2.5 rounded-xl shadow-md shadow-indigo-600/20 transition-all cursor-pointer text-xs sm:text-sm">
                                <i data-lucide="power" class="w-4 h-4"></i>
                                <span id="btn-circuit-label">ភ្ជាប់សៀគ្វី / បើកឧស្ម័ន H₂</span>
                            </button>

                            <button type="button" onclick="toggleSaltBridge()" id="btn-salt-bridge" class="flex items-center gap-1.5 bg-cyan-600 hover:bg-cyan-700 text-white font-semibold px-3.5 py-2.5 rounded-xl transition-all cursor-pointer text-xs sm:text-sm">
                                <i data-lucide="git-merge" class="w-4 h-4"></i>
                                <span id="salt-bridge-label">ដកស្ពានអំបិលចេញ</span>
                            </button>

                            <button type="button" onclick="resetLab()" class="flex items-center gap-1.5 bg-slate-200 hover:bg-slate-300 text-slate-700 font-semibold px-3.5 py-2.5 rounded-xl transition-all cursor-pointer text-xs sm:text-sm">
                                <i data-lucide="rotate-ccw" class="w-4 h-4"></i>
                                <span>កំណត់ឡើងវិញ</span>
                            </button>
                        </div>

                        <label class="flex items-center gap-2 text-xs font-semibold text-slate-700 cursor-pointer select-none">
                            <input type="checkbox" id="chk-micro" checked class="rounded text-indigo-600 focus:ring-indigo-500 cursor-pointer">
                            <span>បង្ហាញចលនាអេឡិចត្រុង (e⁻) &amp; អ៊ីយ៉ុង</span>
                        </label>
                    </div>
                </div>

                <!-- Right Chemical Analysis & Equations Panel (5 cols) -->
                <div class="lg:col-span-5 space-y-4">

                    <!-- Polarity & Potential Card -->
                    <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-4 space-y-3">
                        <div class="flex items-center justify-between border-b border-slate-100 pb-2">
                            <h3 class="font-bold text-slate-800 text-sm sm:text-base flex items-center gap-2">
                                <i data-lucide="activity" class="w-4 h-4 text-indigo-600"></i>
                                <span>ការវិភាគប៉ូល និងប៉ូតង់ស្យែលស្តង់ដា</span>
                            </h3>
                            <span id="couple-tag" class="text-xs font-bold bg-indigo-50 text-indigo-800 border border-indigo-200 px-2.5 py-0.5 rounded-full">Cu²⁺ / Cu</span>
                        </div>

                        <div class="grid grid-cols-2 gap-2.5 text-xs">
                            <div id="box-she-role" class="p-3 rounded-xl border border-rose-200 bg-rose-50/70 space-y-1">
                                <div class="font-bold text-rose-900">អេឡិចត្រូត SHE (ឆ្វេង)</div>
                                <div id="she-polarity" class="text-sm font-extrabold text-rose-700">អាណូត ( – )</div>
                                <div id="she-process" class="text-[11px] text-slate-600">រងអុកស៊ីតកម្ម (បោះបង់ e⁻)</div>
                            </div>

                            <div id="box-metal-role" class="p-3 rounded-xl border border-emerald-200 bg-emerald-50/70 space-y-1">
                                <div id="metal-box-title" class="font-bold text-emerald-900">អេឡិចត្រូត Cu (ស្តាំ)</div>
                                <div id="metal-polarity" class="text-sm font-extrabold text-emerald-700">កាតូត ( + )</div>
                                <div id="metal-process" class="text-[11px] text-slate-600">រងរេដុកម្ម (ចាប់យក e⁻)</div>
                            </div>
                        </div>

                        <!-- Half-Equations & Overall Equation -->
                        <div class="bg-slate-50 border border-slate-200 rounded-xl p-3 space-y-2 text-xs">
                            <div>
                                <span class="font-bold text-rose-800">• កន្លះសមីការនៅអាណូត ( – ) ៖</span>
                                <div id="eq-anode" class="font-mono text-slate-900 bg-white px-2.5 py-1 rounded-lg border border-slate-200 mt-1">
                                    H₂(g)  →  2H⁺(aq) + 2e⁻
                                </div>
                            </div>
                            <div>
                                <span class="font-bold text-emerald-800">• កន្លះសមីការនៅកាតូត ( + ) ៖</span>
                                <div id="eq-cathode" class="font-mono text-slate-900 bg-white px-2.5 py-1 rounded-lg border border-slate-200 mt-1">
                                    Cu²⁺(aq) + 2e⁻  →  Cu(s)
                                </div>
                            </div>
                            <div>
                                <span class="font-bold text-indigo-900">• សមីការតុល្យការសរុប ៖</span>
                                <div id="eq-overall" class="font-mono font-bold text-indigo-950 bg-indigo-50/70 px-2.5 py-1 rounded-lg border border-indigo-200 mt-1">
                                    H₂(g) + Cu²⁺(aq)  →  2H⁺(aq) + Cu(s)
                                </div>
                            </div>
                        </div>

                        <!-- Formula Calculation Box -->
                        <div class="bg-amber-50/80 border border-amber-200 rounded-xl p-3 text-xs space-y-1">
                            <div class="font-bold text-amber-900">រូបមន្តគណនាប៉ូតង់ស្យែលស្តង់ដា E°(Mⁿ⁺/M) ៖</div>
                            <div id="formula-calc" class="font-mono text-slate-800 leading-relaxed">
                                ΔE° = E°(កាតូត) - E°(អាណូត)<br>
                                0.34 V = E°(Cu²⁺/Cu) - 0.00 V  ⇒  <strong>E°(Cu²⁺/Cu) = +0.34 V</strong>
                            </div>
                        </div>
                    </div>

                    <!-- Recorded Measurements Table -->
                    <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-4 space-y-2.5">
                        <div class="flex items-center justify-between border-b border-slate-100 pb-2">
                            <h3 class="font-bold text-slate-800 text-sm flex items-center gap-2">
                                <i data-lucide="table" class="w-4 h-4 text-teal-600"></i>
                                <span>តារាងកត់ត្រាលទ្ធផលពិសោធន៍</span>
                            </h3>
                            <button type="button" onclick="recordMeasurement()" class="text-[11px] font-bold bg-teal-600 hover:bg-teal-700 text-white px-2.5 py-1 rounded-lg transition-colors cursor-pointer">
                                + កត់ត្រាលទ្ធផលនេះ
                            </button>
                        </div>

                        <div class="overflow-x-auto max-h-40">
                            <table class="w-full text-[11px] text-left border-collapse">
                                <thead>
                                    <tr class="bg-slate-100 text-slate-700 border-b border-slate-200">
                                        <th class="py-1.5 px-2">គូរេដុក</th>
                                        <th class="py-1.5 px-2">ប៉ូលលោហៈ</th>
                                        <th class="py-1.5 px-2">វ៉ុលម៉ែត្រ</th>
                                        <th class="py-1.5 px-2">E° (V)</th>
                                    </tr>
                                </thead>
                                <tbody id="record-tbody" class="divide-y divide-slate-100">
                                    <tr>
                                        <td colspan="4" class="py-3 text-center text-slate-400">ភ្ជាប់សៀគ្វី រួចចុច «+ កត់ត្រាលទ្ធផលនេះ»</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- ========================================================== -->
        <!-- TAB 2: THEORY & STANDARD REDUCTION POTENTIAL TABLE         -->
        <!-- ========================================================== -->
        <section id="view-theory" class="tab-view hidden">
            <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-6 sm:p-8 space-y-6" id="theory-area">
                <div class="flex flex-wrap items-center justify-between gap-3 border-b border-slate-200 pb-4 no-print">
                    <div>
                        <span class="text-xs font-bold bg-indigo-100 text-indigo-800 px-2.5 py-1 rounded-full">ខ្លឹមសារមេរៀន ថ្នាក់ទី១១</span>
                        <h2 class="text-lg sm:text-xl font-bold text-slate-900 mt-1">៣.១.៣. ការវាស់ប៉ូតង់ស្យែលស្តង់ដានៃគូរេដុក (SHE)</h2>
                    </div>
                    <button onclick="printArea('theory-area')" class="flex items-center gap-1.5 bg-indigo-600 hover:bg-indigo-700 text-white px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold cursor-pointer">
                        <i data-lucide="printer" class="w-4 h-4"></i>
                        <span>បោះពុម្ពមេរៀន</span>
                    </button>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-5 text-sm leading-relaxed">
                    <div class="bg-slate-50 p-4 rounded-2xl border border-slate-200 space-y-2">
                        <h3 class="font-bold text-indigo-900 text-base">១. អេឡិចត្រូតអ៊ីដ្រូសែនស្តង់ដា (SHE)</h3>
                        <p class="text-slate-700">
                            គេមិនអាចវាស់ប៉ូតង់ស្យែលដាច់ខាតនៃកន្លះពិលតែមួយបានទេ ដូច្នេះគេជ្រើសរើសយក <strong>អេឡិចត្រូតអ៊ីដ្រូសែនស្តង់ដា (SHE)</strong> ជាអេឡិចត្រូតយោង ដោយកំណត់តម្លៃប៉ូតង់ស្យែលស្តង់ដារបស់វាស្មើសូន្យជានិច្ច៖
                        </p>
                        <div class="bg-white p-2.5 rounded-xl border border-indigo-200 font-mono font-bold text-center text-indigo-900">
                            E°(H⁺ / H₂) = 0.00 V  (នៅ 298 K, P = 1 bar, [H⁺] = 1 M)
                        </div>
                    </div>

                    <div class="bg-slate-50 p-4 rounded-2xl border border-slate-200 space-y-2">
                        <h3 class="font-bold text-indigo-900 text-base">២. គោលការណ៍កំណត់សញ្ញានៃ E°(Mⁿ⁺/M)</h3>
                        <ul class="list-disc list-inside space-y-1.5 text-slate-700">
                            <li><strong>ករណីលោហៈជាកាតូត (+) ៖</strong> អេឡិចត្រុងផ្លាស់ទីពី SHE ទៅកាន់លោហៈ (ឧ. Cu, Ag)។ តម្លៃ <strong>E° &gt; 0</strong> (ឧ. E°(Cu²⁺/Cu) = +0.34 V)។</li>
                            <li><strong>ករណីលោហៈជាអាណូត (–) ៖</strong> អេឡិចត្រុងផ្លាស់ទីពីលោហៈទៅកាន់ SHE (ឧ. Zn, Fe, Mg)។ តម្លៃ <strong>E° &lt; 0</strong> (ឧ. E°(Zn²⁺/Zn) = -0.76 V)។</li>
                            <li><strong>តួនាទីស្ពានអំបិល ៖</strong> ភ្ជាប់សៀគ្វីខាងក្នុង និងរក្សាតុល្យភាពបន្ទុកអគ្គិសនីក្នុងសូលុយស្យុងទាំងពីរ។</li>
                        </ul>
                    </div>
                </div>

                <!-- Standard Reduction Potentials Table -->
                <div class="space-y-2">
                    <h3 class="font-bold text-slate-800 text-base">៣. តារាងប៉ូតង់ស្យែលរេដុកម្មស្តង់ដាមួយចំនួន (នៅ 298 K)</h3>
                    <div class="overflow-x-auto">
                        <table class="w-full text-sm border-collapse border border-slate-300">
                            <thead>
                                <tr class="bg-indigo-900 text-white">
                                    <th class="border border-slate-300 p-2.5 text-left">គូរេដុក (Ox / Red)</th>
                                    <th class="border border-slate-300 p-2.5 text-left">កន្លះសមីការរេដុកម្ម</th>
                                    <th class="border border-slate-300 p-2.5 text-center">E° (V)</th>
                                    <th class="border border-slate-300 p-2.5 text-left">លក្ខណៈប្រៀបធៀបជាមួយ H₂</th>
                                </tr>
                            </thead>
                            <tbody class="divide-y divide-slate-200">
                                <tr class="bg-emerald-50/40">
                                    <td class="border border-slate-300 p-2.5 font-bold">Ag⁺ / Ag</td>
                                    <td class="border border-slate-300 p-2.5 font-mono">Ag⁺ + e⁻ ⇌ Ag</td>
                                    <td class="border border-slate-300 p-2.5 text-center font-mono font-bold text-emerald-700">+0.80 V</td>
                                    <td class="border border-slate-300 p-2.5">Ag⁺ ជាអុកស៊ីតករខ្លាំងជាង H⁺ (Ag ជាកាតូត)</td>
                                </tr>
                                <tr class="bg-emerald-50/40">
                                    <td class="border border-slate-300 p-2.5 font-bold">Cu²⁺ / Cu</td>
                                    <td class="border border-slate-300 p-2.5 font-mono">Cu²⁺ + 2e⁻ ⇌ Cu</td>
                                    <td class="border border-slate-300 p-2.5 text-center font-mono font-bold text-emerald-700">+0.34 V</td>
                                    <td class="border border-slate-300 p-2.5">Cu²⁺ ជាអុកស៊ីតករខ្លាំងជាង H⁺ (Cu ជាកាតូត)</td>
                                </tr>
                                <tr class="bg-amber-50 font-semibold">
                                    <td class="border border-slate-300 p-2.5 font-bold text-amber-900">H⁺ / H₂ (SHE)</td>
                                    <td class="border border-slate-300 p-2.5 font-mono">2H⁺ + 2e⁻ ⇌ H₂</td>
                                    <td class="border border-slate-300 p-2.5 text-center font-mono font-bold text-amber-900">0.00 V</td>
                                    <td class="border border-slate-300 p-2.5">អេឡិចត្រូតយោងស្តង់ដា</td>
                                </tr>
                                <tr class="bg-rose-50/40">
                                    <td class="border border-slate-300 p-2.5 font-bold">Fe²⁺ / Fe</td>
                                    <td class="border border-slate-300 p-2.5 font-mono">Fe²⁺ + 2e⁻ ⇌ Fe</td>
                                    <td class="border border-slate-300 p-2.5 text-center font-mono font-bold text-rose-700">-0.44 V</td>
                                    <td class="border border-slate-300 p-2.5">Fe ជារេដុករខ្លាំងជាង H₂ (Fe ជាអាណូត)</td>
                                </tr>
                                <tr class="bg-rose-50/40">
                                    <td class="border border-slate-300 p-2.5 font-bold">Zn²⁺ / Zn</td>
                                    <td class="border border-slate-300 p-2.5 font-mono">Zn²⁺ + 2e⁻ ⇌ Zn</td>
                                    <td class="border border-slate-300 p-2.5 text-center font-mono font-bold text-rose-700">-0.76 V</td>
                                    <td class="border border-slate-300 p-2.5">Zn ជារេដុករខ្លាំងជាង H₂ (Zn ជាអាណូត)</td>
                                </tr>
                                <tr class="bg-rose-50/40">
                                    <td class="border border-slate-300 p-2.5 font-bold">Mg²⁺ / Mg</td>
                                    <td class="border border-slate-300 p-2.5 font-mono">Mg²⁺ + 2e⁻ ⇌ Mg</td>
                                    <td class="border border-slate-300 p-2.5 text-center font-mono font-bold text-rose-700">-2.37 V</td>
                                    <td class="border border-slate-300 p-2.5">Mg ជារេដុករខ្លាំងជាង H₂ (Mg ជាអាណូត)</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================== -->
        <!-- TAB 3: INTERACTIVE STUDENT WORKSHEET                       -->
        <!-- ========================================================== -->
        <section id="view-worksheet" class="tab-view hidden">
            <div class="bg-white rounded-2xl shadow-sm border border-slate-200 p-6 sm:p-8 space-y-6" id="worksheet-area">
                <div class="flex flex-wrap items-center justify-between gap-3 border-b border-slate-200 pb-4 no-print">
                    <div>
                        <span class="text-xs font-bold bg-amber-100 text-amber-800 px-2.5 py-1 rounded-full">លំហាត់អនុវត្ត</span>
                        <h2 class="text-lg sm:text-xl font-bold text-slate-900 mt-1">សន្លឹកកិច្ចការសិស្ស ៖ ការវាស់ប៉ូតង់ស្យែលស្តង់ដា (SHE)</h2>
                    </div>
                    <button onclick="printArea('worksheet-area')" class="flex items-center gap-1.5 bg-indigo-600 hover:bg-indigo-700 text-white px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold cursor-pointer">
                        <i data-lucide="printer" class="w-4 h-4"></i>
                        <span>បោះពុម្ពសន្លឹកកិច្ចការ</span>
                    </button>
                </div>

                <!-- Interactive Fill-in-the-blank Questions -->
                <div class="bg-indigo-50/70 border border-indigo-200 rounded-2xl p-5 space-y-4 text-sm">
                    <h3 class="font-bold text-indigo-950 text-base">ផ្នែកទី១ ៖ សំណួរបំពេញចន្លោះ (ចូរធ្វើពិសោធន៍ រួចជ្រើសរើសចម្លើយត្រឹមត្រូវ)</h3>

                    <div class="space-y-3 leading-loose text-slate-800">
                        <p>
                            ១. នៅក្នុងថ្មពិលដែលផ្សំឡើងពីអេឡិចត្រូតអ៊ីដ្រូសែនស្តង់ដា (SHE) និងអេឡិចត្រូតទង់ដែង (Cu²⁺/Cu) ៖ អេឡិចត្រូត Cu ដើរតួជាប៉ូល
                            <select id="q1" class="mx-1 px-2.5 py-1 rounded-lg border border-indigo-400 bg-white font-bold text-indigo-900">
                                <option value="">-- រើស --</option>
                                <option value="កាតូត (+)">កាតូត (+)</option>
                                <option value="អាណូត (-)">អាណូត (-)</option>
                            </select>
                            ហើយអេឡិចត្រុងផ្លាស់ទីតាមខ្សែចម្លងពី
                            <select id="q2" class="mx-1 px-2.5 py-1 rounded-lg border border-indigo-400 bg-white font-bold text-indigo-900">
                                <option value="">-- រើស --</option>
                                <option value="SHE ទៅ Cu">SHE ទៅ Cu</option>
                                <option value="Cu ទៅ SHE">Cu ទៅ SHE</option>
                            </select>
                            ។
                        </p>

                        <p>
                            ២. នៅពេលជំនួសអេឡិចត្រូត Cu ដោយអេឡិចត្រូតស័ង្កសី (Zn²⁺/Zn) ៖ អេឡិចត្រូត Zn ដើរតួជាប៉ូល
                            <select id="q3" class="mx-1 px-2.5 py-1 rounded-lg border border-indigo-400 bg-white font-bold text-indigo-900">
                                <option value="">-- រើស --</option>
                                <option value="កាតូត (+)">កាតូត (+)</option>
                                <option value="អាណូត (-)">អាណូត (-)</option>
                            </select>
                            ហើយប៉ូតង់ស្យែលស្តង់ដា E°(Zn²⁺/Zn) មានតម្លៃស្មើ
                            <select id="q4" class="mx-1 px-2.5 py-1 rounded-lg border border-indigo-400 bg-white font-bold text-indigo-900">
                                <option value="">-- រើស --</option>
                                <option value="+0.76 V">+0.76 V</option>
                                <option value="-0.76 V">-0.76 V</option>
                            </select>
                            ។
                        </p>

                        <p>
                            ៣. ប្រសិនបើយើងដក <strong>ស្ពានអំបិល</strong> ចេញពីថ្មពិល នោះតម្លៃនៅលើវ៉ុលម៉ែត្រនឹងធ្លាក់ចុះស្មើ
                            <select id="q5" class="mx-1 px-2.5 py-1 rounded-lg border border-indigo-400 bg-white font-bold text-indigo-900">
                                <option value="">-- រើស --</option>
                                <option value="0.00 V">0.00 V</option>
                                <option value="1.10 V">1.10 V</option>
                            </select>
                            ព្រោះសៀគ្វីខាងក្នុងត្រូវបានកាត់ផ្តាច់។
                        </p>
                    </div>

                    <div class="flex flex-wrap items-center gap-3 pt-2 no-print">
                        <button type="button" onclick="checkQuiz()" class="bg-indigo-700 hover:bg-indigo-800 text-white px-4 py-2 rounded-xl text-xs sm:text-sm font-bold shadow-sm cursor-pointer">
                            ផ្ទៀងផ្ទាត់ចម្លើយ
                        </button>
                        <span id="quiz-feedback" class="text-xs sm:text-sm font-bold"></span>
                    </div>
                </div>

                <!-- Short Written Reflection -->
                <div class="space-y-3 text-sm">
                    <h3 class="font-bold text-slate-800 text-base">ផ្នែកទី២ ៖ សំណួរពិភាក្សាក្រុម</h3>
                    <div class="space-y-1.5">
                        <label class="font-semibold text-slate-700 block">១. ហេតុអ្វីបានជាកំណាត់ប្លាទីន (Pt) នៅក្នុងអេឡិចត្រូត SHE ត្រូវស្រោបដោយម្សៅប្លាទីនខ្មៅ?</label>
                        <textarea rows="2" placeholder="សរសេរចម្លើយរបស់អ្នកនៅទីនេះ..." class="w-full p-2.5 rounded-xl border border-slate-300 focus:border-indigo-500 focus:outline-none"></textarea>
                    </div>
                    <div class="space-y-1.5">
                        <label class="font-semibold text-slate-700 block">២. ចូររៀបលំដាប់កម្លាំងរេដុករនៃលោហៈ Cu, Zn, Ag, Fe, Mg ពីខ្សោយទៅខ្លាំង ដោយផ្អែកលើទិន្នន័យពិសោធន៍។</label>
                        <textarea rows="2" placeholder="ឧ. Ag < Cu < ..." class="w-full p-2.5 rounded-xl border border-slate-300 focus:border-indigo-500 focus:outline-none"></textarea>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-white border-t border-slate-200 py-3.5 text-center text-xs text-slate-500 no-print">
        មន្ទីរពិសោធន៍គីមីវិទ្យាអនឡាញ • ថ្នាក់ទី១១ (ការវាស់ប៉ូតង់ស្យែលស្តង់ដានៃគូរេដុក - SHE)
    </footer>

    <!-- ========================================================== -->
    <!-- JAVASCRIPT SIMULATION ENGINE                               -->
    <!-- ========================================================== -->
    <script>
        lucide.createIcons();

        // Tab Switching
        function switchTab(tabName) {
            document.querySelectorAll('.tab-view').forEach(el => el.classList.add('hidden'));
            document.getElementById('view-' + tabName).classList.remove('hidden');

            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('bg-white', 'text-indigo-950', 'shadow');
                btn.classList.add('text-white', 'hover:bg-white/15');
            });

            const activeBtn = document.getElementById('tab-' + tabName);
            activeBtn.classList.remove('text-white', 'hover:bg-white/15');
            activeBtn.classList.add('bg-white', 'text-indigo-950', 'shadow');

            if (tabName === 'lab') resizeCanvas();
        }

        function printArea(id) {
            const content = document.getElementById(id).innerHTML;
            const printDiv = document.createElement('div');
            printDiv.id = 'printable-area';
            printDiv.className = 'p-6 bg-white text-black';
            printDiv.innerHTML = content;
            document.body.appendChild(printDiv);
            window.print();
            document.body.removeChild(printDiv);
        }

        function playTone(freq = 'C5') {
            try {
                if (typeof Tone !== 'undefined') {
                    const synth = new Tone.Synth().toDestination();
                    synth.triggerAttackRelease(freq, '16n');
                }
            } catch (_) {}
        }

        // Standard Half-Cell Data (at 298 K, 1 M)
        const COUPLES = {
            Cu: {
                symbol: 'Cu',
                ion: 'Cu²⁺',
                salt: 'CuSO₄ 1 M',
                e0: 0.34,
                metalColor: '#b45309',
                metalHighlight: '#d97706',
                solColor: 'rgba(56, 189, 248, 0.32)',
                solBorder: 'rgba(14, 165, 233, 0.55)',
                anodeEq: 'H₂(g)  →  2H⁺(aq) + 2e⁻',
                cathodeEq: 'Cu²⁺(aq) + 2e⁻  →  Cu(s)',
                overallEq: 'H₂(g) + Cu²⁺(aq)  →  2H⁺(aq) + Cu(s)'
            },
            Zn: {
                symbol: 'Zn',
                ion: 'Zn²⁺',
                salt: 'ZnSO₄ 1 M',
                e0: -0.76,
                metalColor: '#64748b',
                metalHighlight: '#94a3b8',
                solColor: 'rgba(203, 213, 225, 0.32)',
                solBorder: 'rgba(148, 163, 184, 0.55)',
                anodeEq: 'Zn(s)  →  Zn²⁺(aq) + 2e⁻',
                cathodeEq: '2H⁺(aq) + 2e⁻  →  H₂(g)',
                overallEq: 'Zn(s) + 2H⁺(aq)  →  Zn²⁺(aq) + H₂(g)'
            },
            Ag: {
                symbol: 'Ag',
                ion: 'Ag⁺',
                salt: 'AgNO₃ 1 M',
                e0: 0.80,
                metalColor: '#cbd5e1',
                metalHighlight: '#f1f5f9',
                solColor: 'rgba(226, 232, 240, 0.35)',
                solBorder: 'rgba(148, 163, 184, 0.55)',
                anodeEq: 'H₂(g)  →  2H⁺(aq) + 2e⁻',
                cathodeEq: '2Ag⁺(aq) + 2e⁻  →  2Ag(s)',
                overallEq: 'H₂(g) + 2Ag⁺(aq)  →  2H⁺(aq) + 2Ag(s)'
            },
            Fe: {
                symbol: 'Fe',
                ion: 'Fe²⁺',
                salt: 'FeSO₄ 1 M',
                e0: -0.44,
                metalColor: '#475569',
                metalHighlight: '#64748b',
                solColor: 'rgba(134, 239, 172, 0.28)',
                solBorder: 'rgba(34, 197, 94, 0.45)',
                anodeEq: 'Fe(s)  →  Fe²⁺(aq) + 2e⁻',
                cathodeEq: '2H⁺(aq) + 2e⁻  →  H₂(g)',
                overallEq: 'Fe(s) + 2H⁺(aq)  →  Fe²⁺(aq) + H₂(g)'
            },
            Mg: {
                symbol: 'Mg',
                ion: 'Mg²⁺',
                salt: 'MgSO₄ 1 M',
                e0: -2.37,
                metalColor: '#94a3b8',
                metalHighlight: '#e2e8f0',
                solColor: 'rgba(224, 242, 254, 0.32)',
                solBorder: 'rgba(125, 211, 252, 0.5)',
                anodeEq: 'Mg(s)  →  Mg²⁺(aq) + 2e⁻',
                cathodeEq: '2H⁺(aq) + 2e⁻  →  H₂(g)',
                overallEq: 'Mg(s) + 2H⁺(aq)  →  Mg²⁺(aq) + H₂(g)'
            }
        };

        let currentKey = 'Cu';
        let circuitClosed = false;
        let saltBridgeIn = true;

        // Animated Particles
        let h2Bubbles = [];
        let electrons = [];
        let bridgeIons = [];

        const canvas = document.getElementById('cellCanvas');
        const ctx = canvas.getContext('2d');

        function initParticles() {
            h2Bubbles = Array.from({ length: 18 }, () => ({
                x: (Math.random() - 0.5) * 26,
                y: Math.random() * 65,
                r: Math.random() * 2.5 + 1.5,
                vy: Math.random() * 0.9 + 0.5
            }));

            electrons = Array.from({ length: 12 }, (_, i) => ({
                t: i / 12
            }));

            bridgeIons = [
                { type: 'K⁺', t: 0.2, color: '#0284c7' },
                { type: 'K⁺', t: 0.65, color: '#0284c7' },
                { type: 'NO₃⁻', t: 0.35, color: '#e11d48' },
                { type: 'NO₃⁻', t: 0.8, color: '#e11d48' }
            ];
        }

        function resizeCanvas() {
            const dpr = window.devicePixelRatio || 1;
            const rect = canvas.parentElement.getBoundingClientRect();
            const w = Math.max(320, rect.width - 12);
            const h = Math.max(430, rect.height - 12);

            canvas.style.width = w + 'px';
            canvas.style.height = h + 'px';
            canvas.width = Math.floor(w * dpr);
            canvas.height = Math.floor(h * dpr);
            ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
        }

        window.addEventListener('resize', resizeCanvas);

        function selectCouple(key) {
            currentKey = key;
            document.querySelectorAll('.couple-card').forEach(btn => {
                btn.classList.remove('border-indigo-600', 'bg-indigo-50/70');
                btn.classList.add('border-slate-200', 'bg-white');
            });
            const active = document.getElementById('btn-couple-' + key);
            active.classList.remove('border-slate-200', 'bg-white');
            active.classList.add('border-indigo-600', 'bg-indigo-50/70');

            updateAnalysisPanel();
            playTone('E5');
        }

        function toggleCircuit() {
            circuitClosed = !circuitClosed;
            const btn = document.getElementById('btn-toggle-circuit');
            const label = document.getElementById('btn-circuit-label');
            if (circuitClosed) {
                label.textContent = 'ផ្តាច់សៀគ្វី / បិទឧស្ម័ន';
                btn.classList.replace('bg-indigo-600', 'bg-rose-600');
                btn.classList.replace('hover:bg-indigo-700', 'hover:bg-rose-700');
                playTone('G5');
            } else {
                label.textContent = 'ភ្ជាប់សៀគ្វី / បើកឧស្ម័ន H₂';
                btn.classList.replace('bg-rose-600', 'bg-indigo-600');
                btn.classList.replace('hover:bg-rose-700', 'hover:bg-indigo-700');
                playTone('C5');
            }
            updateAnalysisPanel();
        }

        function toggleSaltBridge() {
            saltBridgeIn = !saltBridgeIn;
            const label = document.getElementById('salt-bridge-label');
            label.textContent = saltBridgeIn ? 'ដកស្ពានអំបិលចេញ' : 'ដាក់ស្ពានអំបិលចូលវិញ';
            updateAnalysisPanel();
        }

        function resetLab() {
            circuitClosed = false;
            saltBridgeIn = true;
            document.getElementById('btn-circuit-label').textContent = 'ភ្ជាប់សៀគ្វី / បើកឧស្ម័ន H₂';
            const btn = document.getElementById('btn-toggle-circuit');
            btn.classList.remove('bg-rose-600', 'hover:bg-rose-700');
            btn.classList.add('bg-indigo-600', 'hover:bg-indigo-700');
            document.getElementById('salt-bridge-label').textContent = 'ដកស្ពានអំបិលចេញ';
            initParticles();
            updateAnalysisPanel();
        }

        function isActiveFlow() {
            return circuitClosed && saltBridgeIn;
        }

        function updateAnalysisPanel() {
            const c = COUPLES[currentKey];
            const active = isActiveFlow();
            const isMetalCathode = c.e0 > 0;

            // Status bar & voltmeter readout
            const dot = document.getElementById('circuit-dot');
            const statusText = document.getElementById('circuit-status');
            const voltBadge = document.getElementById('volt-badge');

            if (!circuitClosed) {
                dot.className = 'w-2.5 h-2.5 rounded-full bg-amber-500';
                statusText.textContent = 'សៀគ្វីចំហ • ចុច «ភ្ជាប់សៀគ្វី / បើកឧស្ម័ន H₂» ដើម្បីវាស់';
                voltBadge.textContent = '0.00 V';
            } else if (!saltBridgeIn) {
                dot.className = 'w-2.5 h-2.5 rounded-full bg-rose-500';
                statusText.textContent = 'គ្មានស្ពានអំបិល! សៀគ្វីខាងក្នុងដាច់ (V = 0.00 V)';
                voltBadge.textContent = '0.00 V';
            } else {
                dot.className = 'w-2.5 h-2.5 rounded-full bg-emerald-500 animate-ping';
                statusText.textContent = `សៀគ្វីបិទ • កំពុងវាស់គូរេដុក ${c.ion}/${c.symbol} នៅ 298 K`;
                const sign = c.e0 > 0 ? '+' : '';
                voltBadge.textContent = `${sign}${c.e0.toFixed(2)} V`;
            }

            // Right Panel Details
            document.getElementById('couple-tag').textContent = `${c.ion} / ${c.symbol}`;
            document.getElementById('metal-box-title').textContent = `អេឡិចត្រូត ${c.symbol} (ស្តាំ)`;

            const sheBox = document.getElementById('box-she-role');
            const metalBox = document.getElementById('box-metal-role');

            if (isMetalCathode) {
                sheBox.className = 'p-3 rounded-xl border border-rose-200 bg-rose-50/70 space-y-1';
                document.getElementById('she-polarity').className = 'text-sm font-extrabold text-rose-700';
                document.getElementById('she-polarity').textContent = 'អាណូត ( – )';
                document.getElementById('she-process').textContent = 'រងអុកស៊ីតកម្ម (បោះបង់ e⁻)';

                metalBox.className = 'p-3 rounded-xl border border-emerald-200 bg-emerald-50/70 space-y-1';
                document.getElementById('metal-polarity').className = 'text-sm font-extrabold text-emerald-700';
                document.getElementById('metal-polarity').textContent = 'កាតូត ( + )';
                document.getElementById('metal-process').textContent = 'រងរេដុកម្ម (ចាប់យក e⁻)';
            } else {
                sheBox.className = 'p-3 rounded-xl border border-emerald-200 bg-emerald-50/70 space-y-1';
                document.getElementById('she-polarity').className = 'text-sm font-extrabold text-emerald-700';
                document.getElementById('she-polarity').textContent = 'កាតូត ( + )';
                document.getElementById('she-process').textContent = 'រងរេដុកម្ម (ចាប់យក e⁻)';

                metalBox.className = 'p-3 rounded-xl border border-rose-200 bg-rose-50/70 space-y-1';
                document.getElementById('metal-polarity').className = 'text-sm font-extrabold text-rose-700';
                document.getElementById('metal-polarity').textContent = 'អាណូត ( – )';
                document.getElementById('metal-process').textContent = 'រងអុកស៊ីតកម្ម (បោះបង់ e⁻)';
            }

            document.getElementById('eq-anode').textContent = c.anodeEq;
            document.getElementById('eq-cathode').textContent = c.cathodeEq;
            document.getElementById('eq-overall').textContent = c.overallEq;

            const absV = Math.abs(c.e0).toFixed(2);
            const signV = c.e0 > 0 ? `+${c.e0.toFixed(2)} V` : `${c.e0.toFixed(2)} V`;
            if (isMetalCathode) {
                document.getElementById('formula-calc').innerHTML =
                    `ΔE° = E°(កាតូត) - E°(អាណូត)<br>${absV} V = E°(${c.ion}/${c.symbol}) - 0.00 V  ⇒  <strong>E°(${c.ion}/${c.symbol}) = ${signV}</strong>`;
            } else {
                document.getElementById('formula-calc').innerHTML =
                    `ΔE° = E°(កាតូត) - E°(អាណូត)<br>${absV} V = 0.00 V - E°(${c.ion}/${c.symbol})  ⇒  <strong>E°(${c.ion}/${c.symbol}) = ${signV}</strong>`;
            }
        }

        function recordMeasurement() {
            const c = COUPLES[currentKey];
            const tbody = document.getElementById('record-tbody');
            if (tbody.querySelector('td[colspan]')) tbody.innerHTML = '';

            const active = isActiveFlow();
            const pol = c.e0 > 0 ? 'កាតូត (+)' : 'អាណូត (–)';
            const voltVal = active ? `${c.e0 > 0 ? '+' : ''}${c.e0.toFixed(2)} V` : '0.00 V (ចំហ)';
            const e0Val = `${c.e0 > 0 ? '+' : ''}${c.e0.toFixed(2)} V`;

            const tr = document.createElement('tr');
            tr.innerHTML = `
                <td class="py-1.5 px-2 font-bold text-slate-800">${c.ion}/${c.symbol}</td>
                <td class="py-1.5 px-2 ${c.e0 > 0 ? 'text-emerald-700' : 'text-rose-700'} font-semibold">${pol}</td>
                <td class="py-1.5 px-2 font-mono">${voltVal}</td>
                <td class="py-1.5 px-2 font-mono font-bold text-indigo-900">${e0Val}</td>
            `;
            tbody.prepend(tr);
            playTone('A5');
        }

        // ==========================================================
        // CANVAS DRAWING (MATCHING THE TEXTBOOK DIAGRAM + ANIMATION)
        // ==========================================================
        function drawCellDiagram() {
            const dpr = window.devicePixelRatio || 1;
            const w = canvas.width / dpr;
            const h = canvas.height / dpr;
            ctx.clearRect(0, 0, w, h);

            const c = COUPLES[currentKey];
            const active = isActiveFlow();
            const showMicro = document.getElementById('chk-micro').checked;
            const isMetalCathode = c.e0 > 0;

            const cx = w / 2;
            const beakerW = Math.min(185, w * 0.36);
            const beakerH = 148;
            const beakerY = h - 65;

            const leftCenter = cx - beakerW * 0.68;
            const rightCenter = cx + beakerW * 0.68;
            const wireTopY = 58;

            // 1. Draw Beakers & Solutions
            // Left Beaker (H+ 1 M)
            drawBeaker(leftCenter, beakerY, beakerW, beakerH, 'rgba(56, 189, 248, 0.24)', 'rgba(14, 165, 233, 0.45)', 'H⁺  1 M');
            // Right Beaker (Metal Salt 1 M)
            drawBeaker(rightCenter, beakerY, beakerW, beakerH, c.solColor, c.solBorder, c.salt);

            // 2. Draw SHE Glass Jacket & Pt Electrode (Left)
            const sheTubeW = 34;
            const sheTopY = wireTopY + 55;
            const sheBotY = beakerY - 36;

            // Pt Wire & Blackened Platinum Foil inside SHE
            ctx.strokeStyle = '#1e293b';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.moveTo(leftCenter, wireTopY);
            ctx.lineTo(leftCenter, sheBotY - 12);
            ctx.stroke();

            // Platinum black plate
            ctx.save();
            ctx.translate(leftCenter, sheBotY - 12);
            ctx.rotate(-0.25);
            ctx.fillStyle = '#0f172a';
            ctx.fillRect(-10, -4, 20, 8);
            ctx.restore();

            // Glass Envelope around SHE with H2 side inlet
            ctx.fillStyle = 'rgba(255, 255, 255, 0.45)';
            ctx.strokeStyle = '#475569';
            ctx.lineWidth = 1.8;
            ctx.beginPath();
            ctx.moveTo(leftCenter - 8, sheTopY);
            ctx.lineTo(leftCenter + 8, sheTopY);
            ctx.quadraticCurveTo(leftCenter + sheTubeW / 2, sheTopY + 12, leftCenter + sheTubeW / 2, sheTopY + 26);
            ctx.lineTo(leftCenter + sheTubeW / 2, sheBotY);
            ctx.moveTo(leftCenter - sheTubeW / 2, sheBotY);
            ctx.lineTo(leftCenter - sheTubeW / 2, sheTopY + 52);
            // Side tube for H2 gas inlet
            ctx.lineTo(leftCenter - sheTubeW / 2 - 22, sheTopY + 52);
            ctx.moveTo(leftCenter - sheTubeW / 2 - 22, sheTopY + 42);
            ctx.lineTo(leftCenter - sheTubeW / 2, sheTopY + 42);
            ctx.lineTo(leftCenter - sheTubeW / 2, sheTopY + 26);
            ctx.quadraticCurveTo(leftCenter - sheTubeW / 2, sheTopY + 12, leftCenter - 8, sheTopY);
            ctx.stroke();

            // H2 1 bar inlet arrow & label
            ctx.fillStyle = '#0f172a';
            ctx.font = 'bold 12px "Kantumruy Pro", sans-serif';
            ctx.textAlign = 'right';
            ctx.fillText('H₂ 1 bar', leftCenter - sheTubeW / 2 - 58, sheTopY + 51);
            drawArrow(leftCenter - sheTubeW / 2 - 54, sheTopY + 47, leftCenter - sheTubeW / 2 - 25, sheTopY + 47, '#0f172a');

            // H2 Bubbles in Left Beaker when circuit is closed
            if (circuitClosed) {
                ctx.fillStyle = 'rgba(255, 255, 255, 0.9)';
                ctx.strokeStyle = '#0284c7';
                ctx.lineWidth = 1;
                h2Bubbles.forEach(b => {
                    b.y += b.vy;
                    if (b.y > 75) b.y = 0;
                    ctx.beginPath();
                    ctx.arc(leftCenter + b.x, sheBotY - 4 - b.y, b.r, 0, Math.PI * 2);
                    ctx.fill();
                    ctx.stroke();
                });
            }

            // 3. Draw Metal Electrode Bar (Right)
            const barW = 34;
            const barTopY = wireTopY + 48;
            const barBotY = beakerY - 22;

            ctx.fillStyle = c.metalColor;
            ctx.strokeStyle = '#1e293b';
            ctx.lineWidth = 1.6;
            ctx.beginPath();
            ctx.rect(rightCenter - barW / 2, barTopY, barW, barBotY - barTopY);
            ctx.fill();
            ctx.stroke();

            // Metallic shine strip
            ctx.fillStyle = c.metalHighlight;
            ctx.fillRect(rightCenter - barW / 2 + 4, barTopY + 2, 6, barBotY - barTopY - 4);

            // Label pointer for Metal Electrode (like textbook "-> Cu")
            drawArrow(rightCenter + 8, barTopY + 26, rightCenter + barW / 2 + 32, barTopY + 26, '#0f172a');
            ctx.fillStyle = '#0f172a';
            ctx.font = 'bold 13px "Kantumruy Pro", sans-serif';
            ctx.textAlign = 'left';
            ctx.fillText(c.symbol, rightCenter + barW / 2 + 37, barTopY + 30);

            // Ion label inside right solution
            ctx.fillStyle = '#1e293b';
            ctx.font = 'bold 12px sans-serif';
            ctx.textAlign = 'left';
            ctx.fillText(c.ion, rightCenter + barW / 2 + 12, beakerY - 48);

            // 4. Draw Salt Bridge (U-tube connecting both beakers)
            if (saltBridgeIn) {
                const sbLeft = leftCenter + beakerW * 0.32;
                const sbRight = rightCenter - beakerW * 0.32;
                const sbTopY = beakerY - beakerH - 18;
                const sbDipY = beakerY - beakerH + 46;

                ctx.strokeStyle = '#0284c7';
                ctx.lineWidth = 12;
                ctx.lineCap = 'round';
                ctx.lineJoin = 'round';
                ctx.beginPath();
                ctx.moveTo(sbLeft, sbDipY);
                ctx.lineTo(sbLeft, sbTopY);
                ctx.lineTo(sbRight, sbTopY);
                ctx.lineTo(sbRight, sbDipY);
                ctx.stroke();

                ctx.strokeStyle = 'rgba(224, 242, 254, 0.85)';
                ctx.lineWidth = 8;
                ctx.beginPath();
                ctx.moveTo(sbLeft, sbDipY);
                ctx.lineTo(sbLeft, sbTopY);
                ctx.lineTo(sbRight, sbTopY);
                ctx.lineTo(sbRight, sbDipY);
                ctx.stroke();

                // Salt Bridge Label (298 K / ស្ពានអំបិល)
                ctx.fillStyle = '#0f172a';
                ctx.font = 'bold 12px "Kantumruy Pro", sans-serif';
                ctx.textAlign = 'center';
                ctx.fillText('298 K', cx, sbTopY - 24);
                ctx.fillText('ស្ពានអំបិល', cx, sbTopY - 9);

                // Animated ions inside salt bridge when active
                if (active && showMicro) {
                    bridgeIons.forEach(ion => {
                        const dir = isMetalCathode ? 1 : -1;
                        if (ion.type === 'K⁺') {
                            ion.t = (ion.t + 0.004 * dir + 1) % 1;
                        } else {
                            ion.t = (ion.t - 0.004 * dir + 1) % 1;
                        }
                        const ix = sbLeft + (sbRight - sbLeft) * ion.t;
                        ctx.fillStyle = ion.color;
                        ctx.font = 'bold 9.5px sans-serif';
                        ctx.fillText(ion.type, ix, sbTopY + 3);
                    });
                }
            }

            // 5. External Circuit Wires & Digital Voltmeter Box
            const meterW = 86;
            const meterH = 34;

            ctx.strokeStyle = '#1e293b';
            ctx.lineWidth = 2.2;
            ctx.beginPath();
            // Left wire from SHE to Voltmeter
            ctx.moveTo(leftCenter, sheTopY);
            ctx.lineTo(leftCenter, wireTopY);
            ctx.lineTo(cx - meterW / 2, wireTopY);
            // Right wire from Voltmeter to Metal
            ctx.moveTo(cx + meterW / 2, wireTopY);
            ctx.lineTo(rightCenter, wireTopY);
            ctx.lineTo(rightCenter, barTopY);
            ctx.stroke();

            // Voltmeter Box
            ctx.fillStyle = '#ffffff';
            ctx.strokeStyle = '#0f172a';
            ctx.lineWidth = 2;
            ctx.beginPath();
            ctx.roundRect(cx - meterW / 2, wireTopY - meterH / 2, meterW, meterH, 6);
            ctx.fill();
            ctx.stroke();

            // Voltmeter Value Text
            ctx.fillStyle = active ? '#047857' : '#64748b';
            ctx.font = 'bold 14px monospace';
            ctx.textAlign = 'center';
            const displayV = active ? `${c.e0 > 0 ? '+' : ''}${c.e0.toFixed(2)} V` : '0.00 V';
            ctx.fillText(displayV, cx, wireTopY + 5);

            // 6. Polarity Labels: អាណូត (–) and កាតូត (+)
            ctx.font = 'bold 13px "Kantumruy Pro", sans-serif';
            if (isMetalCathode) {
                ctx.fillStyle = '#be123c';
                ctx.textAlign = 'center';
                ctx.fillText('អាណូត ( – )', leftCenter, wireTopY - 12);

                ctx.fillStyle = '#047857';
                ctx.fillText('កាតូត ( + )', rightCenter, wireTopY - 12);
            } else {
                ctx.fillStyle = '#047857';
                ctx.textAlign = 'center';
                ctx.fillText('កាតូត ( + )', leftCenter, wireTopY - 12);

                ctx.fillStyle = '#be123c';
                ctx.fillText('អាណូត ( – )', rightCenter, wireTopY - 12);
            }

            // 7. Electron Flow Direction Arrow & Animated e- Dots
            if (active) {
                const arrowY = wireTopY - 10;
                if (isMetalCathode) {
                    drawArrow(cx + meterW / 2 + 12, arrowY, cx + meterW / 2 + 44, arrowY, '#0f172a');
                    ctx.fillStyle = '#0f172a';
                    ctx.font = 'bold 12px sans-serif';
                    ctx.fillText('e⁻', cx + meterW / 2 + 28, arrowY - 5);
                } else {
                    drawArrow(cx - meterW / 2 - 12, arrowY, cx - meterW / 2 - 44, arrowY, '#0f172a');
                    ctx.fillStyle = '#0f172a';
                    ctx.font = 'bold 12px sans-serif';
                    ctx.fillText('e⁻', cx - meterW / 2 - 28, arrowY - 5);
                }

                if (showMicro) {
                    const dir = isMetalCathode ? 1 : -1;
                    electrons.forEach(e => {
                        e.t = (e.t + 0.005 * dir + 1) % 1;
                        const ex = leftCenter + (rightCenter - leftCenter) * e.t;
                        // Skip inside voltmeter box
                        if (Math.abs(ex - cx) > meterW / 2 + 4) {
                            ctx.fillStyle = '#eab308';
                            ctx.strokeStyle = '#854d0e';
                            ctx.lineWidth = 1.2;
                            ctx.beginPath();
                            ctx.arc(ex, wireTopY, 4.5, 0, Math.PI * 2);
                            ctx.fill();
                            ctx.stroke();
                        }
                    });
                }
            }

            // 8. Caption underneath diagram (matching textbook figure caption)
            ctx.fillStyle = '#334155';
            ctx.font = 'italic bold 12px "Kantumruy Pro", sans-serif';
            ctx.textAlign = 'center';
            const roleDesc = isMetalCathode
                ? `បង្ហាញពីថ្មពិលមានអេឡិចត្រូត ${c.symbol} ជាកាតូត និងអេឡិចត្រូតអ៊ីដ្រូសែន (SHE) ជាអាណូត`
                : `បង្ហាញពីថ្មពិលមានអេឡិចត្រូត ${c.symbol} ជាអាណូត និងអេឡិចត្រូតអ៊ីដ្រូសែន (SHE) ជាកាតូត`;
            ctx.fillText(roleDesc, cx, h - 22);
        }

        function drawBeaker(cx, yBot, w, h, fillColor, strokeColor, bottomLabel) {
            const left = cx - w / 2;
            const top = yBot - h;
            const liqTop = top + 30;

            // Solution fill
            ctx.fillStyle = fillColor;
            ctx.beginPath();
            ctx.roundRect(left + 2, liqTop, w - 4, yBot - liqTop - 2, [0, 0, 14, 14]);
            ctx.fill();

            // Meniscus line
            ctx.strokeStyle = strokeColor;
            ctx.lineWidth = 1.5;
            ctx.beginPath();
            ctx.moveTo(left + 2, liqTop);
            ctx.lineTo(left + w - 2, liqTop);
            ctx.stroke();

            // Glass beaker walls
            ctx.strokeStyle = '#475569';
            ctx.lineWidth = 2.2;
            ctx.beginPath();
            ctx.moveTo(left - 4, top);
            ctx.lineTo(left, top + 6);
            ctx.lineTo(left, yBot - 14);
            ctx.quadraticCurveTo(left, yBot, left + 14, yBot);
            ctx.lineTo(left + w - 14, yBot);
            ctx.quadraticCurveTo(left + w, yBot, left + w, yBot - 14);
            ctx.lineTo(left + w, top + 6);
            ctx.lineTo(left + w + 4, top);
            ctx.stroke();

            // Bottom solution label (e.g., H+ 1 M or CuSO4 1 M)
            ctx.fillStyle = '#0f172a';
            ctx.font = 'bold 12.5px "Kantumruy Pro", sans-serif';
            ctx.textAlign = 'center';
            ctx.fillText(bottomLabel, cx, yBot - 12);
        }

        function drawArrow(x1, y1, x2, y2, color) {
            const headLen = 7;
            const angle = Math.atan2(y2 - y1, x2 - x1);
            ctx.strokeStyle = color;
            ctx.fillStyle = color;
            ctx.lineWidth = 1.8;
            ctx.beginPath();
            ctx.moveTo(x1, y1);
            ctx.lineTo(x2, y2);
            ctx.stroke();

            ctx.beginPath();
            ctx.moveTo(x2, y2);
            ctx.lineTo(x2 - headLen * Math.cos(angle - Math.PI / 6), y2 - headLen * Math.sin(angle - Math.PI / 6));
            ctx.lineTo(x2 - headLen * Math.cos(angle + Math.PI / 6), y2 - headLen * Math.sin(angle + Math.PI / 6));
            ctx.closePath();
            ctx.fill();
        }

        function animate() {
            drawCellDiagram();
            requestAnimationFrame(animate);
        }

        window.onload = function () {
            resizeCanvas();
            initParticles();
            updateAnalysisPanel();
            requestAnimationFrame(animate);
        };
    </script>
</body>
</html>
