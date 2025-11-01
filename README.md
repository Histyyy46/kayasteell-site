<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    
    <!-- 
      !!! BU SATIR ÇOK ÖNEMLİ !!!
      Bu 'viewport' etiketi, sitenin mobil cihazların ekran genişliğine göre
      kendini doğru bir şekilde ölçeklendirmesini sağlar.
      Bu olmazsa, site telefonda küçücük bir masaüstü versiyonu gibi görünür.
    -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <title>Kaya Steel - Çelik Konstrüksiyon Çözümleri</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Font - Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome (ikonlar için) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" xintegrity="sha512-DTOQO9RWCH3ppGqcWaEA1BIZOC6xxalwEsw9c2QQeAIftl+Vegovlnee1c9QX4TctnWMn13TZye+giMm8e2LwA==" crossorigin="anonymous" referrerpolicy="no-referrer" />

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f9fa; 
        }
        .hero-section {
            background-image: url('https://placehold.co/1920x1000/4a5568/f7fafc?text=Modern+Çelik+Yapı');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }
        header {
            background-color: #1f2937;
        }
        #mobile-menu {
            display: none;
        }
    </style>
</head>
<body class="antialiased">

    <!-- HEADER / Gezinme Çubuğu -->
    <header class="sticky top-0 z-50 shadow-md">
        <nav class="container mx-auto px-6 py-4">
            <div class="flex items-center justify-between">
                <!-- Logo -->
                <div class="text-white text-2xl font-bold flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4 6a2 2 0 012-2h12a2 2 0 012 2v12a2 2 0 01-2 2H6a2 2 0 01-2-2V6z" />
                        <path stroke-linecap="round" stroke-linejoin="round" d="M10 12h4" />
                        <path stroke-linecap="round" stroke-linejoin="round" d="M12 10v4" />
                    </svg>
                    KAYA STEEL
                </div>

                <!-- 
                  !!! DUYARLI TASARIM ÖRNEĞİ !!!
                  'hidden': Normalde (mobilde) gizlidir.
                  'md:flex': "Medium" (orta) ekran boyutundan (tablet/masaüstü) itibaren görünür (flex) olur.
                  Bu, "Masaüstü Menüsü"dür.
                -->
                <div class="hidden md:flex items-center space-x-6 text-gray-300">
                    <a href="#home" class="hover:text-white transition duration-300">ANA SAYFA</a>
                    <a href="#services" class="hover:text-white transition duration-300">HİZMETLER</a>
                    <a href="#about" class="hover:text-white transition duration-300">HAKKIMIZDA</a>
                    <a href="#contact" class="hover:text-white transition duration-300">İLETİŞİM</a>
                    <button class="text-gray-300 hover:text-white transition duration-300">
                        <i class="fa-solid fa-magnifying-glass"></i>
                    </button>
                </div>

                <!-- 
                  !!! DUYARLI TASARIM ÖRNEĞİ !!!
                  'md:hidden': "Medium" (orta) ekran boyutundan itibaren gizlenir.
                  Bu, sadece mobilde görünen "Hamburger Menü Butonu"dur.
                -->
                <div class="md:hidden">
                    <button id="mobile-menu-button" class="text-white focus:outline-none">
                        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                        </svg>
                    </button>
                </div>
            </div>

            <!-- Mobil Menü (Açılır) - Bu bölüm de 'md:hidden' ile sadece mobilde görünür -->
            <div id="mobile-menu" class="md:hidden mt-4 space-y-2">
                <a href="#home" class="block px-4 py-2 text-gray-300 hover:bg-gray-700 hover:text-white rounded-md transition duration-300">ANA SAYFA</a>
                <a href="#services" class="block px-4 py-2 text-gray-300 hover:bg-gray-700 hover:text-white rounded-md transition duration-300">HİZMETLER</a>
                <a href="#about" class="block px-4 py-2 text-gray-300 hover:bg-gray-700 hover:text-white rounded-md transition duration-300">HAKKIMIZDA</a>
                <a href="#contact" class="block px-4 py-2 text-gray-300 hover:bg-gray-700 hover:text-white rounded-md transition duration-300">İLETİŞİM</a>
                <div class="px-4 py-2">
                     <button class="text-gray-300 hover:text-white transition duration-300">
                        <i class="fa-solid fa-magnifying-glass mr-2"></i> Ara
                    </button>
                </div>
            </div>
        </nav>
    </header>

    <!-- ANA GÖVDE -->
    <main>
        <!-- Kahraman (Hero) Bölümü -->
        <!-- 
          !!! DUYARLI TASARIM ÖRNEĞİ !!!
          'h-[70vh]': Yükseklik mobilde ekranın %70'i.
          'md:h-[90vh]': Yükseklik orta ekrandan itibaren %90'ı.
        -->
        <section id="home" class="hero-section h-[70vh] md:h-[90vh] flex items-center justify-center text-white relative">
            <div class="absolute inset-0 bg-black opacity-50"></div>
            
            <div class="container mx-auto px-6 text-center z-10">
                <!-- 
                  !!! DUYARLI TASARIM ÖRNEĞİ !!!
                  'text-3xl': Yazı boyutu mobilde (default).
                  'md:text-5xl': Yazı boyutu orta ekranda.
                  'lg:text-6xl': Yazı boyutu geniş ekranda (masaüstü).
                -->
                <h1 class="text-3xl md:text-5xl lg:text-6xl font-bold mb-4 leading-tight">
                    KAYA STEEL: GÜÇLÜ, DAYANIKLI, ESTETİK
                </h1>
                <h2 class="text-2xl md:text-4xl font-semibold text-gray-200 mb-8">
                    ÇELİK KONSTRÜKSİYON ÇÖZÜMLERİ
                </h2>
                <p class="text-lg md:text-xl text-gray-300 max-w-3xl mx-auto mb-10">
                    Nasip-persoo-teklone ikram alan yihnic-kero-kibdcbldcbln rppol-tekehecebil-ceeem. (Örnek metin)
                </p>
                <a href="#services" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-lg text-lg transition duration-300 shadow-lg">
                    Hizmetlerimizi Keşfedin
                </a>
            </div>
        </section>

        <!-- Öne Çıkan Hizmetler Bölümü -->
        <section id="services" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-xl md:text-2xl text-gray-700 mb-2">
                        Kaya Steel olarak, çelikten yaşam ve tasarımda tüm çelik konstrüksiyon evler
                    </h2>
                    <h3 class="text-3xl md:text-4xl font-bold text-gray-900">
                        Öne Çıkan Hizmetler
                    </h3>
                </div>

                <!-- 
                  !!! DUYARLI TASARIM ÖRNEĞİ !!!
                  'grid-cols-1': Mobilde (default) kartlar 1 sütunlu (alt alta dizilir).
                  'md:grid-cols-3': Orta ekrandan itibaren 3 sütunlu (yan yana dizilir).
                -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Kart 1: Hazır Ev Modelleri -->
                    <div class="border border-gray-200 rounded-lg p-8 text-center shadow-lg hover:shadow-xl transition-shadow duration-300 bg-white">
                        <div class="flex items-center justify-center mb-6">
                            <div class="bg-blue-100 text-blue-600 p-4 rounded-full">
                                <i class="fa-solid fa-house-chimney-window fa-2x"></i>
                            </div>
                        </div>
                        <h4 class="text-2xl font-semibold text-gray-900 mb-3">Hazır Ev Modelleri</h4>
                        <p class="text-gray-600 mb-6">
                            Sizin zevk ve ihtiyaçlarınıza göre özenle tasarlanmış, modern ve dayanıklı hazır çelik ev modellerimiz.
                        </p>
                        <a href="#" class="inline-block bg-gray-800 hover:bg-gray-900 text-white font-medium py-2 px-6 rounded-lg transition duration-300">
                            Daha Fazla Bilgi
                        </a>
                    </div>

                    <!-- Kart 2: Özel Tasarım Evler -->
                    <div class="border border-gray-200 rounded-lg p-8 text-center shadow-lg hover:shadow-xl transition-shadow duration-300 bg-white">
                         <div class="flex items-center justify-center mb-6">
                            <div class="bg-blue-100 text-blue-600 p-4 rounded-full">
                                <i class="fa-solid fa-compass-drafting fa-2x"></i>
                            </div>
                        </div>
                        <h4 class="text-2xl font-semibold text-gray-900 mb-3">Özel Tasarım Evler</h4>
                        <p class="text-gray-600 mb-6">
                            Hayalinizdeki evi birlikte tasarlayalım. Mimarlarımızla çalışarak size özel çelik konstrüksiyon çözümleri.
                        </p>
                        <a href="#" class="inline-block bg-gray-800 hover:bg-gray-900 text-white font-medium py-2 px-6 rounded-lg transition duration-300">
                            Daha Fazla Bilgi
                        </a>
                    </div>

                    <!-- Kart 3: Endüstriyel Yapılar -->
                    <div class="border border-gray-200 rounded-lg p-8 text-center shadow-lg hover:shadow-xl transition-shadow duration-300 bg-white">
                         <div class="flex items-center justify-center mb-6">
                            <div class="bg-blue-100 text-blue-600 p-4 rounded-full">
                                <i class="fa-solid fa-industry fa-2x"></i>
                            </div>
                        </div>
                        <h4 class="text-2xl font-semibold text-gray-900 mb-3">Endüstriyel Yapılar</h4>
                        <p class="text-gray-600 mb-6">
                            Fabrikalar, depolar ve atölyeler için güçlü, ekonomik ve hızlı kurulumlu çelik yapı çözümleri sunuyoruz.
                        </p>
                        <a href="#" class="inline-block bg-gray-800 hover:bg-gray-900 text-white font-medium py-2 px-6 rounded-lg transition duration-300">
                            Daha Fazla Bilgi
                        </a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Hakkımızda Bölümü -->
        <section id="about" class="py-20 bg-gray-50">
            <div class="container mx-auto px-6">
                <!-- 
                  !!! DUYARLI TASARIM ÖRNEĞİ !!!
                  'flex-col': Mobilde (default) resim ve yazı alt alta dizilir.
                  'md:flex-row': Orta ekrandan itibaren yan yana dizilir.
                -->
                <div class="flex flex-col md:flex-row items-center gap-12">
                    <!-- Resim ('md:w-1/2' -> ortadan itibaren genişliğin yarısı) -->
                    <div class="md:w-1/2">
                        <img src="https://placehold.co/600x400/a0aec0/f7fafc?text=Kaya+Steel+Ekibi" alt="Hakkımızda" class="rounded-lg shadow-xl w-full">
                    </div>
                    <!-- Metin ('md:w-1/2' -> ortadan itibaren genişliğin yarısı) -->
                    <div class="md:w-1/2">
                        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4">Hakkımızda</h2>
                        <p class="text-gray-700 text-lg mb-4">
                            Kaya Steel, yılların verdiği tecrübe ile çelik konstrüksiyon sektöründe lider firmalardan biri olmayı hedeflemektedir. Müşteri memnuniyetini en üst düzeyde tutarak, kaliteli ve güvenilir hizmet sunmaktayız.
                        </p>
                        <p class="text-gray-700 text-lg">
                            Modern teknolojiyi ve yenilikçi tasarım anlayışını birleştirerek, hem estetik hem de dayanıklı yapılar inşa ediyoruz. Projeleriniz için bizimle iletişime geçin.
                        </p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- FOOTER / Alt Bilgi -->
    <footer id="contact" class="bg-gray-900 text-gray-300 pt-16 pb-8">
        <div class="container mx-auto px-6">
            <!-- 
              !!! DUYARLI TASARIM ÖRNEĞİ !!!
              'grid-cols-1': Mobilde (default) 1 sütunlu (alt alta).
              'md:grid-cols-4': Orta ekrandan itibaren 4 sütunlu (yan yana).
            -->
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-10">
                <!-- Kurumsal -->
                <div>
                    <h5 class="text-white text-lg font-semibold mb-4">KURUMSAL</h5>
                    <ul class="space-y-2">
                        <li><a href="#about" class="hover:text-white transition duration-300">Hakkımızda</a></li>
                        <li><a href="#services" class="hover:text-white transition duration-300">Hizmetlerimiz</a></li>
                        <li><a href="#" class="hover:text-white transition duration-300">Projelerimiz</a></li>
                        <li><a href="#" class="hover:text-white transition duration-300">Kariyer</a></li>
                    </ul>
                </div>
                <!-- Destek -->
                <div>
                    <h5 class="text-white text-lg font-semibold mb-4">DESTEK</h5>
                    <ul class="space-y-2">
                        <li><a href="#" class="hover:text-white transition duration-300">Sıkça Sorulan Sorular</a></li>
                        <li><a href="#" class="hover:text-white transition duration-300">Teknik Destek</a></li>
                        <li><a href="#" class="hover:text-white transition duration-300">Garanti Koşulları</a></li>
                    </ul>
                </div>
                <!-- İletişim -->
                <div>
                    <h5 class="text-white text-lg font-semibold mb-4">İLETİŞİM</h5>
                    <ul class="space-y-2">
                        <li class="flex items-start">
                            <i class="fa-solid fa-location-dot mt-1 mr-3 flex-shrink-0"></i>
                            <span>Adres: Örnek Mah. Çelik Sk. No:123, İstanbul</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fa-solid fa-phone mr-3"></i>
                            <span>+90 (212) 555 44 33</span>
                        </li>
                         <li class="flex items-center">
                            <i class="fa-solid fa-envelope mr-3"></i>
                            <span>info@kayasteel.com</span>
                        </li>
                    </ul>
                </div>
                <!-- Sosyal Medya -->
                <div>
                    <h5 class="text-white text-lg font-semibold mb-4">BİZİ TAKİP EDİN</h5>
                    <p class="mb-4">En yeni projelerimiz ve haberler için sosyal medyadayız.</p>
                    <div class="flex space-x-4">
                        <a href="https://www.instagram.com/kayasteell" target="_blank" rel="noopener noreferrer" class="text-gray-300 hover:text-white text-2xl transition duration-300">
                            <i class="fa-brands fa-instagram"></i>
                        </a>
                        <a href="#" class="text-gray-300 hover:text-white text-2xl transition duration-300">
                            <i class="fa-brands fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-300 hover:text-white text-2xl transition duration-300">
                            <i class="fa-brands fa-linkedin-in"></i>
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="border-t border-gray-700 pt-8 mt-8 text-center">
                <p>&copy; 2025 Kaya Steel. Tüm hakları saklıdır.</p>
                <p class="text-sm text-gray-500 mt-1">
                    Bu web sitesi bir demo olarak tasarlanmıştır.
                </p>
            </div>
        </div>
    </footer>

    <!-- JavaScript (Mobil Menü için) -->
    <script>
        const menuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        menuButton.addEventListener('click', () => {
            if (mobileMenu.style.display === 'block') {
                mobileMenu.style.display = 'none';
            } else {
                mobileMenu.style.display = 'block';
            }
        });
    </script>

</body>
</html>

