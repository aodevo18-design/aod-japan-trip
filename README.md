<!DOCTYPE html>
<html lang="th" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>อ๊อด พาเที่ยว : 15 Days Japan Journey</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Prompt:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- AOS Animation CSS -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Prompt', 'sans-serif'],
                    },
                    colors: {
                        sakura: '#ffb7c5',
                        ocean: '#0ea5e9'
                    }
                }
            }
        }
    </script>
    <style>
        body { font-family: 'Prompt', sans-serif; background-color: #f8fafc; overflow-x: hidden; }
        
        /* Parallax Backgrounds */
        .hero-bg {
            background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1493976040374-85c8e12f0c0e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
        .bg-alps {
            background-image: linear-gradient(rgba(248, 250, 252, 0.85), rgba(255, 255, 255, 0.95)), url('https://images.unsplash.com/photo-1522850611956-6541fba7493a?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
        .bg-hokkaido {
            background-image: linear-gradient(rgba(240, 249, 255, 0.85), rgba(255, 255, 255, 0.95)), url('https://images.unsplash.com/photo-1542051812871-757508259f7b?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }

        /* Timeline Styles */
        .timeline-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 24px;
            height: 100%;
            width: 4px;
            background: rgba(203, 213, 225, 0.8);
            border-radius: 2px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        
        @media (min-width: 768px) {
            .timeline-container::before { left: 50%; transform: translateX(-50%); }
            .timeline-item:nth-child(odd) .timeline-content { margin-left: auto; padding-left: 3rem; }
            .timeline-item:nth-child(even) .timeline-content { margin-right: auto; padding-right: 3rem; text-align: right; }
            .timeline-item:nth-child(odd) .timeline-dot { left: 50%; transform: translate(-50%, 0); }
            .timeline-item:nth-child(even) .timeline-dot { right: 50%; transform: translate(50%, 0); }
            .timeline-item:nth-child(even) .timeline-content ul { align-items: flex-end; }
            .timeline-item:nth-child(even) .timeline-content li { flex-direction: row-reverse; }
            .timeline-item:nth-child(even) .timeline-content li i { margin-right: 0; margin-left: 1rem; }
            .timeline-item:nth-child(even) .timeline-content .btn-container { justify-content: flex-end; }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 12px; }
        ::-webkit-scrollbar-track { background: #f1f1f1; }
        ::-webkit-scrollbar-thumb { background: #94a3b8; border-radius: 6px; border: 3px solid #f1f1f1; }
        ::-webkit-scrollbar-thumb:hover { background: #64748b; }
        
        /* Glassmorphism Card Hover */
        .glass-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.15);
        }
        .glass-card:hover {
            transform: translateY(-5px) scale(1.01);
            box-shadow: 0 20px 40px -10px rgba(0, 0, 0, 0.2);
        }
    </style>
</head>
<body class="text-gray-900 antialiased">

    <!-- Navbar/Floating Menu -->
    <nav class="fixed top-0 w-full bg-white/90 backdrop-blur-lg shadow-md z-50 transition-all duration-300 border-b border-gray-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0 flex items-center gap-3">
                    <div class="w-10 h-10 bg-gradient-to-br from-rose-500 to-rose-600 rounded-full flex items-center justify-center text-white shadow-lg">
                        <i class="fa-solid fa-plane-departure text-lg"></i>
                    </div>
                    <span class="font-bold text-xl md:text-2xl bg-clip-text text-transparent bg-gradient-to-r from-rose-600 to-blue-600">อ๊อด พาเที่ยว</span>
                </div>
                <div class="flex space-x-2 md:space-x-4 overflow-x-auto whitespace-nowrap hide-scrollbar">
                    <a href="#video" class="hidden md:flex items-center text-gray-700 hover:text-rose-500 px-2 md:px-3 py-2 rounded-md text-sm md:text-base font-semibold transition"><i class="fa-brands fa-youtube mr-1 md:mr-2 text-red-500"></i> คลิปแนะนำ</a>
                    <a href="#pdf-viewer" class="flex items-center text-gray-700 hover:text-blue-500 px-2 md:px-3 py-2 rounded-md text-sm md:text-base font-semibold transition"><i class="fa-solid fa-file-pdf mr-1 text-blue-500"></i> เอกสาร PDF</a>
                    <a href="#part1" class="text-gray-700 hover:text-rose-500 px-2 md:px-3 py-2 rounded-md text-sm md:text-base font-semibold transition"><i class="fa-solid fa-mountain-sun mr-1 text-rose-400"></i> แอลป์</a>
                    <a href="#part2" class="text-gray-700 hover:text-blue-500 px-2 md:px-3 py-2 rounded-md text-sm md:text-base font-semibold transition"><i class="fa-solid fa-snowflake mr-1 text-cyan-400"></i> ฮอกไกโด</a>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="hero-bg h-[100svh] flex items-center justify-center text-center px-4 relative pt-20">
        <div class="absolute inset-0 bg-gradient-to-b from-transparent to-[#f8fafc] opacity-90"></div>
        <div class="relative z-10 text-white w-full max-w-5xl" data-aos="zoom-in" data-aos-duration="1200">
            <div class="inline-flex items-center gap-2 py-2 px-5 rounded-full bg-black/40 backdrop-blur-md text-base md:text-lg font-semibold tracking-wider mb-6 border border-white/30 shadow-xl">
                <span class="text-rose-400"><i class="fa-solid fa-star"></i></span>
                อ๊อด พาเที่ยว นำเสนอ
                <span class="text-rose-400"><i class="fa-solid fa-star"></i></span>
            </div>
            <h1 class="text-5xl md:text-7xl lg:text-8xl font-bold mb-6 drop-shadow-[0_5px_5px_rgba(0,0,0,0.5)] leading-tight">
                JAPAN <span class="text-rose-300">JOURNEY</span>
            </h1>
            <p class="text-xl md:text-3xl font-medium mb-10 max-w-3xl mx-auto drop-shadow-lg leading-relaxed text-gray-100">
                แผนการเดินทาง 15 วัน 14 คืน<br>
                เซนได - เจแปนแอลป์ - ฮอกไกโด
            </p>
            <div class="flex flex-col sm:flex-row justify-center gap-4 text-base md:text-xl font-medium">
                <span class="bg-white/20 backdrop-blur-md px-6 py-3 rounded-xl border border-white/30 shadow-xl flex items-center justify-center"><i class="fa-regular fa-calendar-days mr-3 text-rose-300"></i> 14 - 28 เมษายน 2570</span>
                <span class="bg-white/20 backdrop-blur-md px-6 py-3 rounded-xl border border-white/30 shadow-xl flex items-center justify-center"><i class="fa-solid fa-ticket mr-3 text-blue-300"></i> ใช้ JR Pass (All Japan)</span>
            </div>
            <div class="mt-16 animate-bounce">
                <a href="#video" class="text-white opacity-80 hover:opacity-100 hover:text-rose-400 transition inline-block"><i class="fa-solid fa-circle-chevron-down text-5xl drop-shadow-lg"></i></a>
            </div>
        </div>
    </div>

    <!-- Video Section -->
    <div id="video" class="bg-white pt-20 pb-10 px-4">
        <div class="max-w-5xl mx-auto" data-aos="fade-up">
            <div class="text-center mb-10">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
                    <span class="text-rose-600 text-4xl"><i class="fa-brands fa-youtube drop-shadow-md"></i></span> คลิปแนะนำจาก อ๊อด พาเที่ยว
                </h2>
                <p class="text-xl text-gray-600">ชมบรรยากาศและเตรียมความพร้อมก่อนไปสัมผัสสถานที่จริง</p>
            </div>
            <div class="relative w-full overflow-hidden rounded-3xl shadow-[0_20px_50px_rgba(0,0,0,0.2)] border-8 border-gray-100 bg-black group" style="padding-top: 56.25%;">
                <iframe class="absolute top-0 left-0 w-full h-full transform group-hover:scale-[1.01] transition-transform duration-500" src="https://www.youtube.com/embed/yNmSTEymgrQ?si=vGpJrFw_EA2Wwu0i" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <!-- PDF Viewer Section -->
    <div id="pdf-viewer" class="bg-[#f8fafc] py-16 px-4">
        <div class="max-w-5xl mx-auto" data-aos="fade-up">
            <div class="text-center mb-10">
                <h2 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4">
                    <span class="text-blue-600 text-4xl"><i class="fa-solid fa-file-pdf drop-shadow-md"></i></span> เอกสารสรุปแผนการเดินทาง
                </h2>
                <p class="text-xl text-gray-600">สไลด์สรุปเส้นทางข้ามภูมิภาค สัมผัส 3 ฤดูในทริปเดียว</p>
            </div>
            
            <!-- PDF Container -->
            <div class="relative w-full overflow-hidden rounded-3xl shadow-[0_20px_50px_rgba(0,0,0,0.15)] border-8 border-white bg-gray-200" style="height: 80vh; min-height: 600px;">
                <!-- Embedded PDF using Google Drive Preview -->
                <iframe src="https://drive.google.com/file/d/1VzOwJxkOmAoMTybFZkorLM-TT42mE9ft/preview" width="100%" height="100%" class="border-none rounded-2xl" allow="autoplay"></iframe>
            </div>
            <div class="text-center mt-4">
                <a href="https://drive.google.com/file/d/1VzOwJxkOmAoMTybFZkorLM-TT42mE9ft/view?usp=sharing" target="_blank" class="inline-flex items-center gap-2 text-blue-600 hover:text-blue-800 font-medium transition text-lg">
                    <i class="fa-solid fa-arrow-up-right-from-square"></i> เปิดไฟล์ในหน้าต่างใหม่ (เต็มจอ)
                </a>
            </div>
        </div>
    </div>

    <!-- Timeline Content -->
    <main class="w-full">
        
        <!-- ================= PART 1: ALPS ================= -->
        <div id="part1" class="bg-alps py-24 px-4 sm:px-6 lg:px-8">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-20" data-aos="fade-down">
                    <span class="inline-block py-2 px-6 rounded-full bg-white text-rose-600 font-bold text-lg shadow-md mb-4 border border-rose-100">Part 1</span>
                    <h2 class="text-4xl md:text-5xl font-bold text-gray-900 drop-shadow-sm inline-flex items-center justify-center gap-4 flex-wrap">
                        <span class="w-16 h-16 rounded-full bg-gradient-to-br from-rose-400 to-pink-500 text-white flex items-center justify-center text-3xl shadow-lg"><i class="fa-solid fa-mountain-sun"></i></span>
                        ผจญภัยเจแปนแอลป์
                    </h2>
                    <p class="text-xl md:text-2xl text-gray-700 mt-6 font-medium">ชมซากุระ ลิงแช่ออนเซ็น และกำแพงหิมะตระการตา</p>
                </div>

                <div class="relative timeline-container">
                    
                    <!-- Day 1 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-rose-600 to-pink-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">1</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-0 md:pr-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-rose-100 text-rose-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">14 เมษายน | เซนได</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🌸 วันที่ 1: เริ่มต้นที่โทโฮคุ</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-plane-arrival mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>บินตรงดอนเมือง (DMK) ✈️ สู่เซนได (SDJ) (ถึง 16:30 น.)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-train mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>นั่งรถไฟเข้าเมืองเซนได (จ่ายแยก 660 เยน)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-utensils mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>มื้อค่ำ:</b> ลิ้นวัวย่าง (Gyutan) ร้านดัง Rikyu</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> ย่าน JR Sendai</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Gyutan+Sendai" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-rose-500 to-pink-500 hover:from-rose-600 hover:to-pink-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมภาพลิ้นวัว</a>
                                    <a href="https://www.google.com/search?tbm=isch&q=Aoba+Castle+Sendai" target="_blank" class="inline-flex items-center gap-2 bg-white hover:bg-gray-50 border border-gray-200 text-gray-700 text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-sm hover:shadow-md transition"><i class="fa-regular fa-image"></i> ปราสาทเซนได</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 2 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-rose-600 to-pink-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">2</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300 border-l-4 border-l-green-500">
                                <div class="flex flex-wrap justify-between items-center mb-3 gap-2">
                                    <span class="inline-block bg-rose-100 text-rose-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full shadow-sm">15 เมษายน | ฮาคุบะ</span>
                                    <span class="bg-green-500 text-white font-bold text-sm md:text-base px-3 py-1 rounded-full shadow-md animate-pulse"><i class="fa-solid fa-ticket mr-1"></i> เริ่มใช้ JR Pass</span>
                                </div>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🏔️ วันที่ 2: สู่หมู่บ้านฮาคุบะ</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-train-subway mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>นั่งชินคันเซ็น: Sendai -> Nagano</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-bus mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>ต่อรถบัสเข้าสู่หมู่บ้าน Hakuba</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-camera mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> Oide Park ถ่ายรูปสะพานแขวน วิวเจแปนแอลป์</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hot-tub-person mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> Hakuba (แช่ออนเซ็น)</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Oide+Park+Hakuba+Spring" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-rose-500 to-pink-500 hover:from-rose-600 hover:to-pink-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมภาพ Oide Park</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 3 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-rose-600 to-pink-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">3</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-0 md:pr-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-rose-100 text-rose-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">16 เมษายน | ยูดานากะ</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🐒 วันที่ 3: ยอดเขาฮาคุบะ</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-cable-car mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>ขึ้นกระเช้า <b>Hakuba Happo-one</b> ชมวิวหิมะพาโนรามา</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-train mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>เดินทางโดยรถไฟ: Hakuba -> Yudanaka</span></li>
                                    <li class="flex items-start"><i class="fa-brands fa-redhat mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> เดินเล่นเมือง Shibu Onsen ในชุดยูกาตะ</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> เรียวกังออนเซ็น ย่าน Yudanaka</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Hakuba+Happo-one+views" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-rose-500 to-pink-500 hover:from-rose-600 hover:to-pink-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมวิว Hakuba</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 4 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-rose-600 to-pink-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">4</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-rose-100 text-rose-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">17 เมษายน | นากาโน่-มัตสึโมโตะ</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🏯 วันที่ 4: ลิงแช่น้ำ & ปราสาทอีกา</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-paw mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> Jigokudani ดูลิงหิมะแช่ออนเซ็น</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-train mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>เดินทาง: Nagano -> Matsumoto</span></li>
                                    <li class="flex items-start"><i class="fa-brands fa-fort-awesome mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> Matsumoto Castle ปราสาทดั้งเดิมสีดำ</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> ย่าน JR Matsumoto (คืนที่ 1)</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Jigokudani+Snow+Monkey+Park" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-rose-500 to-pink-500 hover:from-rose-600 hover:to-pink-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> คลิปลิงแช่ออนเซ็น</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 5 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-emerald-500 to-green-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">5</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-0 md:pr-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300 relative overflow-hidden border-2 border-green-200">
                                <div class="absolute top-0 right-0 bg-gradient-to-l from-green-500 to-emerald-400 text-white text-sm md:text-base font-bold px-4 py-2 rounded-bl-2xl z-10 shadow-md">✨ เพิ่งเปิดเส้นทาง!</div>
                                <span class="inline-block bg-green-100 text-green-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm mt-4 md:mt-0">18 เมษายน | คามิโคจิ</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🌲 วันที่ 5: สวรรค์บนดิน คามิโคจิ</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-bus mt-1.5 mr-4 text-green-600 w-6 text-center text-xl"></i> <span>เดินทาง: นั่งรถไฟท้องถิ่น+รถบัส สู่ Kamikochi</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-water mt-1.5 mr-4 text-green-600 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> บึงไทโช (Taisho Pond) สะท้อนเงาภูเขา</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-bridge-water mt-1.5 mr-4 text-green-600 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> สะพานคัปปะ (Kappa Bridge) เดินชมธรรมชาติ</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-green-600 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> ย่าน JR Matsumoto (คืนที่ 2)</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Taisho+Pond+Kamikochi" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-emerald-500 to-green-500 hover:from-emerald-600 hover:to-green-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมบึงไทโช</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 6 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-cyan-500 to-blue-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">6</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300 border-t-4 border-t-cyan-400">
                                <span class="inline-block bg-cyan-100 text-cyan-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">19 เมษายน | ทาเทยามะ คุโรเบะ</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">❄️ วันที่ 6: ทะลวงกำแพงหิมะ</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start bg-amber-50 p-4 rounded-xl border border-amber-200 shadow-sm mb-2"><i class="fa-solid fa-suitcase-rolling mt-1 mr-4 text-amber-600 w-6 text-center text-2xl"></i> <span class="text-amber-800 font-bold">ส่งกระเป๋าเดินทางใบใหญ่ไปโตเกียวล่วงหน้า! เพื่อความสะดวก</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-mountain mt-1.5 mr-4 text-cyan-600 w-6 text-center text-xl"></i> <span>เริ่มเส้นทาง Alpine Route ฝั่ง Shinano-Omachi</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-water mt-1.5 mr-4 text-cyan-600 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> เขื่อนคุโรเบะ (Kurobe Dam)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-snowman mt-1.5 mr-4 text-cyan-600 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> <b>กำแพงหิมะ (Yuki-no-Otani)</b> สูงตระหง่าน > 15 เมตร</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-cyan-600 w-6 text-center text-xl"></i> <span>จบเส้นทางที่ Tateyama / <b>ที่พัก:</b> ย่าน JR Toyama</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Yuki-no-Otani+Snow+Wall" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-cyan-500 to-blue-500 hover:from-cyan-600 hover:to-blue-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมกำแพงหิมะอลังการ</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 7 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-rose-600 to-pink-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">7</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-0 md:pr-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-rose-100 text-rose-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">20 เมษายน | โทยามะ - โตเกียว</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🌷 วันที่ 7: ซากุระ 4 ฤดู</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-seedling mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> Asahi Funakawa (ซากุระ ทิวลิป และภูเขาหิมะในเฟรมเดียว)</span></li>
                                    <li class="flex items-start"><i class="fa-brands fa-canadian-maple-leaf mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> Kansui Park และคาเฟ่ Starbucks ดีไซน์สวย</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-train-subway mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span>นั่งชินคันเซ็นมุ่งหน้าเข้าโตเกียว (Toyama -> Tokyo)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-rose-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> โตเกียว (ใกล้สถานีรถไฟ/ฮาเนดะ) รับกระเป๋าใหญ่</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Asahi+Funakawa+Spring+Quartet" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-rose-500 to-pink-500 hover:from-rose-600 hover:to-pink-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมซากุระ 4 ฤดู</a>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>

        <!-- ================= PART 2: HOKKAIDO ================= -->
        <div id="part2" class="bg-hokkaido py-24 px-4 sm:px-6 lg:px-8 border-t-[10px] border-white">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-20" data-aos="fade-down">
                    <span class="inline-block py-2 px-6 rounded-full bg-white text-blue-600 font-bold text-lg shadow-md mb-4 border border-blue-100">Part 2</span>
                    <h2 class="text-4xl md:text-5xl font-bold text-gray-900 drop-shadow-sm inline-flex items-center justify-center gap-4 flex-wrap">
                        <span class="w-16 h-16 rounded-full bg-gradient-to-br from-blue-400 to-cyan-500 text-white flex items-center justify-center text-3xl shadow-lg"><i class="fa-solid fa-snowflake"></i></span>
                        เริงร่าฮอกไกโด
                    </h2>
                    <p class="text-xl md:text-2xl text-gray-800 mt-6 font-medium bg-white/50 backdrop-blur-sm inline-block px-6 py-2 rounded-full">เล่นหิมะโทมามุ มนต์เสน่ห์โอตารุ และช้อปปิ้งซัปโปโร</p>
                </div>

                <div class="relative timeline-container">
                    
                    <!-- Day 8 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-blue-600 to-cyan-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">8</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-blue-100 text-blue-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">21 เมษายน | บินสู่ฮอกไกโด</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">✈️ วันที่ 8: โทมามุรีสอร์ท</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-plane-departure mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span>บิน: Haneda (HND) ✈️ New Chitose (CTS)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-train mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span>นั่งรถไฟ JR ไปยังสถานี Tomamu</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-swimmer mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>พักผ่อน:</b> ว่ายน้ำที่ Mina-Mina Beach (สระคลื่นเทียม)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> Hoshino Resorts Tomamu</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Hoshino+Resorts+Tomamu+Winter" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-blue-500 to-cyan-500 hover:from-blue-600 hover:to-cyan-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ภาพรีสอร์ท</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 9 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-blue-600 to-cyan-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">9</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-0 md:pr-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-blue-100 text-blue-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">22 เมษายน | โทมามุ</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🏂 วันที่ 9: ลุยหิมะสโนว์บอร์ด</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-person-snowboarding mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span>เล่นสโนว์บอร์ดที่ <b>Tomamu Ski Resort</b> <br><span class="text-base text-gray-500 bg-gray-100 px-2 py-1 rounded mt-2 inline-block">(เป็น Spring Snow ตรวจสอบลานสกีล่วงหน้า)</span></span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-sleigh mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span>หรือทำกิจกรรม Snow Rafting</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-utensils mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>มื้อค่ำ:</b> บุฟเฟ่ต์สุดหรู Nininupuri กลางป่าสน</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> Hoshino Resorts Tomamu (คืนที่ 2)</span></li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!-- Day 10 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-blue-600 to-cyan-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">10</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-blue-100 text-blue-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">23 เมษายน | ซัปโปโร</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🏢 วันที่ 10: เมืองหลวงซัปโปโร</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-train mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span>นั่งรถไฟ: Tomamu -> JR Sapporo</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-building mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> ทำเนียบรัฐบาลเก่า (ตึกอิฐแดง) & สวนโอโดริ</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-fire-burner mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>มื้อค่ำ:</b> เนื้อแกะย่างเจงกิสข่าน ย่าน Susukino</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-hotel mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>ที่พัก:</b> ย่าน JR Sapporo (พักยาว 5 คืน)</span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Former+Hokkaido+Government+Office+Building" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-blue-500 to-cyan-500 hover:from-blue-600 hover:to-cyan-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมตึกอิฐแดง</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 11 -->
                    <div class="relative w-full mb-16 md:mb-24 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-blue-600 to-cyan-400 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2">11</div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-0 md:pr-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-blue-100 text-blue-700 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">24 เมษายน | โอตารุ</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">⚓ วันที่ 11: โรแมนติกโอตารุ</h3>
                                <ul class="space-y-4 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-train mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span>นั่งรถไฟ: Sapporo -> Otaru (วิวทะเลสวยงาม)</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-music mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> พิพิธภัณฑ์กล่องดนตรี, ถนน Sakaimachi</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-fish mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>มื้อเที่ยง:</b> ซูชิสดๆ ที่ Otaru Sushi Street</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-bridge mt-1.5 mr-4 text-blue-500 w-6 text-center text-xl"></i> <span><b>เที่ยว:</b> ถ่ายรูปพลบค่ำที่ <b>คลองโอตารุ (Otaru Canal)</b></span></li>
                                </ul>
                                <div class="mt-8 flex flex-wrap gap-3 btn-container">
                                    <a href="https://www.google.com/search?tbm=isch&q=Otaru+Canal+Sunset" target="_blank" class="inline-flex items-center gap-2 bg-gradient-to-r from-blue-500 to-cyan-500 hover:from-blue-600 hover:to-cyan-600 text-white text-base md:text-lg font-medium py-3 px-6 rounded-full shadow-md hover:shadow-lg transition"><i class="fa-regular fa-image"></i> ชมคลองโอตารุ</a>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Day 12 & 13 & 14 & 15 Combined for brevity and layout -->
                    <div class="relative w-full mb-16 timeline-item" data-aos="fade-up">
                        <div class="absolute left-[12px] md:left-1/2 w-10 h-10 rounded-full bg-gradient-to-tr from-gray-700 to-gray-500 border-4 border-white shadow-xl timeline-dot flex items-center justify-center z-10 text-white text-base font-bold -ml-2 md:-ml-5 top-6 md:top-1/2 md:-translate-y-1/2"><i class="fa-solid fa-star"></i></div>
                        <div class="w-full md:w-1/2 timeline-content pl-16 md:pl-16">
                            <div class="glass-card p-6 md:p-10 rounded-3xl transition-all duration-300">
                                <span class="inline-block bg-gray-200 text-gray-800 font-semibold text-sm md:text-base px-3 py-1 rounded-full mb-3 shadow-sm">25-28 เมษายน | ซัปโปโร & กลับไทย</span>
                                <h3 class="text-2xl md:text-3xl font-bold text-gray-900 mb-6">🎁 วันที่ 12-15: เที่ยวและช้อปปิ้ง</h3>
                                <ul class="space-y-5 text-gray-700 text-lg md:text-xl flex flex-col">
                                    <li class="flex items-start"><i class="fa-solid fa-cookie-bite mt-1.5 mr-4 text-amber-600 w-6 text-center text-2xl"></i> <span><b>วันที่ 12:</b> Shiroi Koibito Park และชมวิวภูเขา Moiwa</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-shrimp mt-1.5 mr-4 text-rose-500 w-6 text-center text-2xl"></i> <span><b>วันที่ 13:</b> ตลาดปลานิโจ & ศาลเจ้าฮอกไกโด</span></li>
                                    <li class="flex items-start"><i class="fa-solid fa-cart-shopping mt-1.5 mr-4 text-blue-500 w-6 text-center text-2xl"></i> <span><b>วันที่ 14:</b> Free Day ช้อปปิ้ง Tanukikoji เต็มวัน</span></li>
                                    <li class="flex items-start bg-blue-50 p-4 rounded-xl border border-blue-200"><i class="fa-solid fa-plane-up mt-1.5 mr-4 text-blue-700 w-6 text-center text-2xl"></i> <span class="font-bold text-blue-900">วันที่ 15: เดินทางไปสนามบินด้วย JR Pass (วันสุดท้าย) แวะซื้อของฝาก และบินกลับดอนเมือง ✈️</span></li>
                                </ul>
                            </div>
                        </div>
                    </div>

                </div>
            </div>
        </div>

    </main>

    <!-- Footer -->
    <footer class="bg-gray-950 text-white py-16 text-center relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-t from-gray-950 to-gray-900"></div>
        <div class="max-w-4xl mx-auto px-4 relative z-10">
            <h2 class="text-3xl md:text-4xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-rose-400 to-blue-400 tracking-wide">
                อ๊อด พาเที่ยว <br class="md:hidden"> <span class="text-2xl md:text-3xl font-medium text-white">: JAPAN JOURNEY 2027</span>
            </h2>
            <p class="text-gray-300 text-lg md:text-xl mb-8 leading-relaxed max-w-2xl mx-auto">
                แผนการเดินทางสุดคุ้ม 15 วัน ที่รวบรวมประสบการณ์สุดประทับใจตั้งแต่โทโฮคุ เจแปนแอลป์ ถึงฮอกไกโด
            </p>
            <div class="flex justify-center gap-6 text-3xl text-gray-500 mb-8">
                <a href="#video" class="hover:text-rose-500 hover:scale-110 transition-all duration-300"><i class="fa-brands fa-youtube"></i></a>
                <i class="fa-solid fa-camera hover:text-white hover:scale-110 transition-all duration-300 cursor-pointer"></i>
                <i class="fa-solid fa-plane hover:text-blue-400 hover:scale-110 transition-all duration-300 cursor-pointer"></i>
            </div>
            <p class="text-gray-600 text-sm md:text-base mt-10">ออกแบบและเรียบเรียงข้อมูลอย่างพิถีพิถัน ขอให้สนุกกับการเดินทางนะครับ!</p>
        </div>
    </footer>

    <!-- AOS Animation JS -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize Animate On Scroll
        AOS.init({
            once: true,
            offset: 50,
            duration: 800,
            easing: 'ease-out-cubic',
        });
    </script>
</body>
</html>
