<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DF Sultan - Pemesanan Kue Kering Idul Fitri</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Plus Jakarta Sans & Playfair Display -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,700;1,600&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome untuk Ikon -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                        serif: ['"Playfair Display"', 'serif'],
                    },
                    colors: {
                        emeraldRaya: {
                            50: '#ecfdf5',
                            100: '#d1fae5',
                            600: '#059669',
                            700: '#047857',
                            800: '#065f46',
                            900: '#064e3b',
                            950: '#022c22',
                        },
                        goldRaya: {
                            300: '#fcd34d',
                            400: '#fbbf24',
                            500: '#f59e0b',
                            600: '#d97706',
                        }
                    }
                }
            }
        }
    </script>
</head>
<body class="bg-[#FAF8F5] text-stone-800 font-sans antialiased selection:bg-emeraldRaya-800 selection:text-goldRaya-300">

    <!-- Notifikasi Toast -->
    <div id="toast-container" class="fixed top-5 right-5 z-50 flex flex-col gap-2 max-w-xs w-full pointer-events-none"></div>

    <!-- ===================================================================== -->
    <!-- TAMPILAN 1: WEBSITE PUBLIK & PEMESANAN (UNTUK SEMUA ORANG)            -->
    <!-- ===================================================================== -->
    <div id="public-view">
        <!-- Navbar Publik -->
        <nav class="sticky top-0 z-40 bg-emeraldRaya-950/95 backdrop-blur-md text-white border-b border-goldRaya-500/30 shadow-lg">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex justify-between items-center h-16 sm:h-20">
                    <!-- Logo & Nama Toko -->
                    <div class="flex items-center gap-3">
                        <div id="nav-logo-container" class="w-10 h-10 sm:w-11 sm:h-11 rounded-full bg-gradient-to-br from-goldRaya-400 to-goldRaya-600 flex items-center justify-center text-emeraldRaya-950 shadow-md overflow-hidden border border-goldRaya-300/50 shrink-0">
                            <i class="fa-solid fa-moon text-lg"></i>
                        </div>
                        <div>
                            <span id="nav-store-name" class="font-serif font-bold text-base sm:text-xl tracking-wide text-goldRaya-400 block leading-tight">Berkah Raya Cookies</span>
                            <span id="nav-store-subtitle" class="text-[11px] sm:text-xs text-emerald-200/80 block line-clamp-1">Sajian Istimewa Idul Fitri</span>
                        </div>
                    </div>

                    <!-- Tombol Aksi Cepat -->
                    <div class="flex items-center gap-2 sm:gap-3">
                        <a href="#katalog-kue" class="hidden sm:inline-block px-3 py-2 text-xs sm:text-sm font-medium text-emerald-100 hover:text-goldRaya-300 transition">
                            Katalog Kue
                        </a>
                        <a href="#form-pemesanan" class="px-4 py-2 sm:px-5 sm:py-2.5 rounded-xl text-xs sm:text-sm font-bold bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 text-emeraldRaya-950 hover:from-goldRaya-300 hover:to-goldRaya-400 shadow-md transition-all flex items-center gap-2">
                            <i class="fa-solid fa-basket-shopping"></i>
                            <span>Form Pesan</span>
                            <span id="nav-cart-badge" class="hidden px-1.5 py-0.5 text-[10px] rounded-full bg-emeraldRaya-950 text-goldRaya-300 font-bold">0</span>
                        </a>
                    </div>
                </div>
            </div>
        </nav>

        <!-- Hero Section Nuansa Ramadhan & Idul Fitri -->
        <header class="relative bg-gradient-to-b from-emeraldRaya-950 via-emeraldRaya-900 to-emeraldRaya-800 text-white overflow-hidden">
            <!-- Gambar Banner dari Pengaturan Admin -->
            <div id="hero-bg-image-wrapper" class="absolute inset-0 opacity-25 pointer-events-none hidden">
                <img id="hero-bg-image" src="" alt="Banner Toko" class="w-full h-full object-cover">
            </div>

            <!-- Dekorasi Ornamen Islami -->
            <div class="absolute inset-0 opacity-10 pointer-events-none">
                <svg class="w-full h-full" xmlns="http://www.w3.org/2000/svg">
                    <defs>
                        <pattern id="islamic-pattern" width="60" height="60" patternUnits="userSpaceOnUse">
                            <path d="M30 0L60 30L30 60L0 30Z" fill="none" stroke="#fbbf24" stroke-width="1"/>
                            <circle cx="30" cy="30" r="8" fill="none" stroke="#fbbf24" stroke-width="1"/>
                        </pattern>
                    </defs>
                    <rect width="100%" height="100%" fill="url(#islamic-pattern)"/>
                </svg>
            </div>

            <div class="relative max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-12 sm:py-20 text-center">
                <!-- Logo Toko -->
                <div id="hero-logo-wrapper" class="mx-auto mb-5 w-20 h-20 sm:w-24 sm:h-24 rounded-full bg-emeraldRaya-950/80 border-2 border-goldRaya-400 shadow-xl flex items-center justify-center overflow-hidden">
                    <i class="fa-solid fa-star-and-crescent text-3xl sm:text-4xl text-goldRaya-400"></i>
                </div>

                <!-- Badge Promo -->
                <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-emeraldRaya-950/80 border border-goldRaya-500/40 text-goldRaya-300 text-xs sm:text-sm font-medium mb-5 shadow-sm">
                    <i class="fa-solid fa-sparkles text-goldRaya-400"></i>
                    <span id="hero-tagline">Open Pre-Order Ramadhan & Idul Fitri • Homemade & Premium</span>
                </div>

                <h1 id="hero-title" class="font-serif text-3xl sm:text-5xl lg:text-6xl font-bold tracking-tight text-white mb-4 leading-tight">
                    Hadirkan Kehangatan Hari Kemenangan
                </h1>
                
                <!-- Bio Toko -->
                <p id="hero-bio" class="max-w-2xl mx-auto text-sm sm:text-lg text-emerald-100/90 mb-8 leading-relaxed">
                    Kue kering buatan rumah dengan mentega pilihan, resep warisan keluarga, dan tanpa bahan pengawet. Cocok untuk sajian meja tamu maupun hampers orang tersayang.
                </p>

                <div class="flex flex-col sm:flex-row items-center justify-center gap-3 sm:gap-4">
                    <a href="#katalog-kue" class="w-full sm:w-auto px-6 py-3.5 rounded-2xl bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 hover:from-goldRaya-300 hover:to-goldRaya-400 text-emeraldRaya-950 font-bold text-sm sm:text-base shadow-lg shadow-goldRaya-500/20 transition transform hover:-translate-y-0.5 flex items-center justify-center gap-2">
                        <i class="fa-solid fa-cookie-bite"></i> Lihat Daftar Kue
                    </a>
                    <a href="#form-pemesanan" class="w-full sm:w-auto px-6 py-3.5 rounded-2xl bg-emeraldRaya-800/80 hover:bg-emeraldRaya-700 border border-emerald-500/30 text-white font-semibold text-sm sm:text-base transition flex items-center justify-center gap-2">
                        <i class="fa-brands fa-whatsapp text-goldRaya-400 text-lg"></i> Pesan Sekarang
                    </a>
                </div>
            </div>

            <div class="h-6 sm:h-10 bg-[#FAF8F5] rounded-t-[2rem] sm:rounded-t-[3rem]"></div>
        </header>

        <!-- Katalog Kue Kering -->
        <main id="katalog-kue" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-12">
            <div class="flex flex-col sm:flex-row sm:items-end justify-between mb-8 gap-4">
                <div>
                    <span class="text-xs font-bold uppercase tracking-widest text-goldRaya-600 block mb-1">Pilihan Favorit Keluarga</span>
                    <h2 class="font-serif text-2xl sm:text-4xl font-bold text-emeraldRaya-950">Katalog Kue Kering Lebaran</h2>
                </div>
                
                <!-- Filter Kategori -->
                <div class="flex flex-wrap gap-2" id="category-filters">
                    <button onclick="filterCategory('Semua')" class="filter-btn active px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-emeraldRaya-900 text-white transition">Semua</button>
                    <button onclick="filterCategory('Klasik')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white text-stone-600 border border-stone-200 hover:border-emeraldRaya-600 transition">Klasik</button>
                    <button onclick="filterCategory('Cokelat & Keju')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white text-stone-600 border border-stone-200 hover:border-emeraldRaya-600 transition">Cokelat & Keju</button>
                    <button onclick="filterCategory('Paket Hampers')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white text-stone-600 border border-stone-200 hover:border-emeraldRaya-600 transition">Paket Hampers</button>
                </div>
            </div>

            <!-- Grid Daftar Kue -->
            <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8">
                <!-- Diisi lewat JS -->
            </div>

            <div id="empty-state" class="hidden text-center py-16 bg-white rounded-3xl border border-dashed border-stone-300">
                <div class="w-16 h-16 mx-auto mb-4 rounded-full bg-emeraldRaya-50 text-emeraldRaya-700 flex items-center justify-center text-2xl">
                    <i class="fa-solid fa-box-open"></i>
                </div>
                <h3 class="text-lg font-bold text-stone-800 mb-1">Belum ada kue di kategori ini</h3>
                <p class="text-sm text-stone-500">Silakan pilih kategori lain untuk melihat koleksi kue kami.</p>
            </div>
        </main>

        <!-- Form Pemesanan Multi-Item & Pengiriman Langsung ke WhatsApp -->
        <section id="form-pemesanan" class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 py-12 sm:py-16">
            <div class="bg-white rounded-3xl shadow-xl border border-goldRaya-500/20 overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-5">
                    
                    <!-- Kolom Kiri: Info WhatsApp -->
                    <div class="lg:col-span-2 bg-gradient-to-br from-emeraldRaya-950 to-emeraldRaya-800 text-white p-6 sm:p-8 flex flex-col justify-between relative overflow-hidden">
                        <div class="relative z-10">
                            <span class="inline-block px-3 py-1 rounded-full bg-goldRaya-500/20 text-goldRaya-300 text-xs font-semibold mb-4">
                                Pemesanan Mudah & Cepat
                            </span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold mb-3 text-white">Formulir Pesanan Kue Kering</h3>
                            <p class="text-sm text-emerald-100/80 mb-6 leading-relaxed">
                                Anda dapat memesan <strong>beberapa jenis kue sekaligus</strong>. Klik tombol <em>"+ Tambah Jenis Kue Lainnya"</em> untuk menambahkan varian pesanan Anda.
                            </p>

                            <!-- Nomor WhatsApp Tujuan -->
                            <div class="p-4 rounded-2xl bg-emeraldRaya-950/60 border border-goldRaya-500/30 mb-6">
                                <span class="text-xs text-emerald-300 block mb-1">WhatsApp Resmi Pemesanan:</span>
                                <div class="flex items-center justify-between gap-2">
                                    <div class="flex items-center gap-2.5">
                                        <div class="w-9 h-9 rounded-full bg-green-500/20 text-green-400 flex items-center justify-center">
                                            <i class="fa-brands fa-whatsapp text-xl"></i>
                                        </div>
                                        <span id="display-wa-number" class="font-bold text-base sm:text-lg tracking-wide text-goldRaya-300">0881-9665-411</span>
                                    </div>
                                    <button type="button" onclick="copyWaNumber()" class="p-2 rounded-lg bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-xs text-emerald-100 transition" title="Salin Nomor WA">
                                        <i class="fa-regular fa-copy"></i>
                                    </button>
                                </div>
                            </div>
                        </div>

                        <div class="relative z-10 text-xs text-emerald-200/80 space-y-2 border-t border-emeraldRaya-700/60 pt-4">
                            <p><i class="fa-solid fa-check text-goldRaya-400 mr-2"></i>Bisa pesan banyak jenis kue dalam 1 form</p>
                            <p><i class="fa-solid fa-check text-goldRaya-400 mr-2"></i>Langsung terhubung ke WhatsApp Penjual</p>
                            <p><i class="fa-solid fa-check text-goldRaya-400 mr-2"></i>Packing aman & rapi untuk pengiriman</p>
                        </div>
                    </div>

                    <!-- Kolom Kanan: Form Input Pemesanan Dinamis -->
                    <div class="lg:col-span-3 p-6 sm:p-8 lg:p-10">
                        <form id="order-form" onsubmit="submitOrderToWhatsApp(event)" class="space-y-5">
                            <!-- Nama & Nomor HP Pembeli -->
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                                <div>
                                    <label for="order-name" class="block text-sm font-semibold text-stone-700 mb-1.5">Nama Lengkap Pemesan <span class="text-red-500">*</span></label>
                                    <input type="text" id="order-name" required placeholder="Contoh: Ibu Siti Aminah" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-stone-800 text-sm focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600 focus:bg-white transition">
                                </div>
                                <div>
                                    <label for="order-buyer-wa" class="block text-sm font-semibold text-stone-700 mb-1.5">Nomor HP / WhatsApp Anda <span class="text-red-500">*</span></label>
                                    <input type="tel" id="order-buyer-wa" required placeholder="Contoh: 081234567890" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-stone-800 text-sm focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600 focus:bg-white transition">
                                </div>
                            </div>

                            <!-- Daftar Pilihan Kue Dinamis (Multi-Item) -->
                            <div class="space-y-3">
                                <div class="flex items-center justify-between">
                                    <label class="block text-sm font-semibold text-stone-700">Jenis Kue yang Dipesan <span class="text-red-500">*</span></label>
                                    <span class="text-xs text-stone-400">Bisa pilih lebih dari 1 jenis</span>
                                </div>

                                <div id="order-items-container" class="space-y-3">
                                    <!-- Baris pesanan dirender oleh JS -->
                                </div>

                                <button type="button" onclick="addOrderItemRow()" class="w-full py-2.5 px-4 rounded-xl border-2 border-dashed border-emeraldRaya-600/40 hover:border-emeraldRaya-700 bg-emeraldRaya-50/60 hover:bg-emeraldRaya-50 text-emeraldRaya-800 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                                    <i class="fa-solid fa-plus-circle"></i>
                                    <span>Tambah Jenis Kue Lainnya</span>
                                </button>
                            </div>

                            <!-- Total Estimasi Harga -->
                            <div class="p-4 rounded-2xl bg-emeraldRaya-50 border border-emeraldRaya-200 flex items-center justify-between">
                                <div>
                                    <span class="text-xs text-emeraldRaya-800 font-semibold block">Total Estimasi Pesanan:</span>
                                    <span id="order-total-items-count" class="text-xs text-stone-500">1 jenis kue (1 toples)</span>
                                </div>
                                <span id="order-total-price" class="text-xl sm:text-2xl font-bold text-emeraldRaya-900">Rp 0</span>
                            </div>

                            <!-- Alamat / Catatan -->
                            <div>
                                <label for="order-address" class="block text-sm font-semibold text-stone-700 mb-1.5">Alamat Pengiriman / Catatan Tambahan</label>
                                <textarea id="order-address" rows="2" placeholder="Tulis alamat pengiriman atau request kartu ucapan Idul Fitri..." class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-stone-800 text-sm focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600 focus:bg-white transition"></textarea>
                            </div>

                            <!-- Tombol Kirim Langsung ke WhatsApp -->
                            <button type="submit" class="w-full py-4 px-6 rounded-2xl bg-gradient-to-r from-green-600 to-emeraldRaya-800 hover:from-green-500 hover:to-emeraldRaya-700 text-white font-bold text-base shadow-lg shadow-emeraldRaya-900/20 transition transform hover:-translate-y-0.5 flex items-center justify-center gap-3">
                                <i class="fa-brands fa-whatsapp text-2xl text-white"></i>
                                <span>Kirim Pesanan ke WhatsApp Sekarang</span>
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer dengan Tombol Akses Admin Tersembunyi/Rapi -->
        <footer class="bg-emeraldRaya-950 text-emerald-200/80 py-10 border-t border-goldRaya-500/20">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-center sm:text-left">
                <div>
                    <p id="footer-store-name" class="font-serif font-bold text-lg text-goldRaya-400">Berkah Raya Cookies</p>
                    <p id="footer-store-bio" class="text-xs mt-1 max-w-md text-emerald-200/70">Selamat Menunaikan Ibadah Puasa & Hari Raya Idul Fitri. Terima kasih telah mempercayakan sajian Lebaran Anda kepada kami.</p>
                </div>
                <div class="flex flex-wrap items-center justify-center gap-2.5">
                    <button onclick="chatDirectWhatsApp()" class="px-4 py-2.5 rounded-xl bg-green-600 hover:bg-green-500 text-white text-xs sm:text-sm font-semibold transition flex items-center gap-2 shadow-md">
                        <i class="fa-brands fa-whatsapp text-base"></i> Chat WhatsApp Penjual
                    </button>
                    <button onclick="openAdminAccess()" class="px-3.5 py-2.5 rounded-xl bg-emeraldRaya-900 hover:bg-emeraldRaya-800 border border-goldRaya-500/30 text-goldRaya-300 text-xs font-semibold transition flex items-center gap-1.5" title="Kelola Toko (Khusus Pemilik)">
                        <i class="fa-solid fa-lock"></i> Admin
                    </button>
                </div>
            </div>
        </footer>
    </div>

    <!-- ===================================================================== -->
    <!-- TAMPILAN 2: DASHBOARD KHUSUS ADMIN (TERHUBUNG LANGSUNG KE HALAMAN INI)-->
    <!-- ===================================================================== -->
    <div id="admin-view" class="hidden min-h-screen bg-stone-100">
        <!-- Navbar Admin -->
        <nav class="sticky top-0 z-40 bg-emeraldRaya-950 text-white border-b border-goldRaya-500/40 shadow-md">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
                <div class="flex items-center gap-3">
                    <div class="w-9 h-9 rounded-xl bg-goldRaya-500 text-emeraldRaya-950 flex items-center justify-center font-bold">
                        <i class="fa-solid fa-crown"></i>
                    </div>
                    <div>
                        <span class="font-bold text-sm sm:text-base text-goldRaya-400 block leading-none">Mode Admin Toko</span>
                        <span class="text-[11px] text-emerald-200">Perubahan langsung tampil di halaman pemesanan</span>
                    </div>
                </div>

                <div class="flex items-center gap-2 sm:gap-3">
                    <button onclick="switchToPublicView()" class="px-4 py-2 rounded-xl bg-goldRaya-500 hover:bg-goldRaya-400 text-emeraldRaya-950 text-xs sm:text-sm font-bold shadow transition flex items-center gap-1.5">
                        <i class="fa-solid fa-eye"></i>
                        <span>Lihat Halaman Pemesanan</span>
                    </button>
                    <button onclick="logoutAdmin()" class="px-3 py-2 rounded-xl bg-red-600/90 hover:bg-red-600 text-white text-xs font-semibold transition flex items-center gap-1.5" title="Keluar & Kunci Mode Admin">
                        <i class="fa-solid fa-right-from-bracket"></i>
                    </button>
                </div>
            </div>
        </nav>

        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-6">
            
            <!-- Kotak Link Pemesanan Terhubung -->
            <div class="bg-gradient-to-r from-emeraldRaya-900 to-emeraldRaya-800 rounded-3xl p-5 sm:p-6 text-white shadow-md border border-goldRaya-500/30 space-y-3">
                <div class="flex flex-col md:flex-row items-start md:items-center justify-between gap-3">
                    <div>
                        <div class="flex items-center gap-2 mb-1">
                            <span class="inline-block px-2.5 py-0.5 rounded-full bg-goldRaya-400/20 text-goldRaya-300 text-[11px] font-bold">Terhubung 1 File</span>
                            <span id="link-updated-badge" class="hidden px-2.5 py-0.5 rounded-full bg-green-500/20 text-green-300 text-[11px] font-bold">
                                <i class="fa-solid fa-check-circle mr-1"></i>Perubahan Tersimpan!
                            </span>
                        </div>
                        <h2 class="font-serif text-lg sm:text-xl font-bold">Bagikan Link Website Ini ke Pembeli</h2>
                        <p class="text-xs text-emerald-100/80">Saat pembeli membuka link ini, mereka otomatis melihat halaman pemesanan (bukan halaman admin).</p>
                    </div>
                    <div class="flex flex-wrap gap-2 w-full md:w-auto shrink-0">
                        <button onclick="switchToPublicView()" class="flex-1 md:flex-none px-4 py-2.5 rounded-xl bg-white/15 hover:bg-white/25 text-white font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2 border border-white/20">
                            <i class="fa-solid fa-store"></i> Buka Halaman Pembeli
                        </button>
                        <button onclick="copyShareableCustomerLink()" class="flex-1 md:flex-none px-4 py-2.5 rounded-xl bg-goldRaya-400 hover:bg-goldRaya-300 text-emeraldRaya-950 font-bold text-xs sm:text-sm shadow transition flex items-center justify-center gap-2">
                            <i class="fa-solid fa-copy"></i> Salin Link Pembeli
                        </button>
                    </div>
                </div>

                <!-- Kolom Link Aktif -->
                <div class="flex items-center gap-2 bg-emeraldRaya-950/70 p-2.5 rounded-2xl border border-goldRaya-500/30">
                    <i class="fa-solid fa-link text-goldRaya-400 pl-2 text-sm"></i>
                    <input type="text" id="generated-index-link" readonly onclick="this.select()" class="w-full bg-transparent text-emerald-100 text-xs sm:text-sm font-mono focus:outline-none truncate" value="">
                </div>
            </div>

            <!-- Tab Navigasi Admin -->
            <div class="flex flex-wrap gap-2 bg-white p-2 rounded-2xl shadow-sm border border-stone-200">
                <button onclick="switchAdminTab('products')" id="tab-btn-products" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl bg-emeraldRaya-900 text-white font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-cookie"></i> Kelola & Post Kue
                </button>
                <button onclick="switchAdminTab('profile')" id="tab-btn-profile" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl text-stone-600 hover:bg-stone-100 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-store"></i> Edit Bio, Logo & Gambar
                </button>
                <button onclick="switchAdminTab('security')" id="tab-btn-security" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl text-stone-600 hover:bg-stone-100 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-shield-halved"></i> Ubah PIN Admin
                </button>
            </div>

            <!-- TAB 1: KELOLA & POST PRODUK KUE -->
            <div id="admin-tab-products" class="space-y-6">
                <div class="bg-white rounded-3xl p-6 shadow-sm border border-stone-200 flex flex-col sm:flex-row sm:items-center justify-between gap-4">
                    <div>
                        <h3 class="font-serif text-xl sm:text-2xl font-bold text-emeraldRaya-950">Daftar Kue Kering Toko Anda</h3>
                        <p class="text-xs sm:text-sm text-stone-500">Tambah kue baru, ubah harga, ganti foto, atau hapus varian.</p>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <button onclick="openProductModal()" class="px-5 py-3 rounded-xl bg-gradient-to-r from-emeraldRaya-800 to-emeraldRaya-900 hover:from-emeraldRaya-700 hover:to-emeraldRaya-800 text-white font-bold text-xs sm:text-sm shadow-md transition flex items-center gap-2">
                            <i class="fa-solid fa-plus"></i> Post Kue Baru
                        </button>
                        <button onclick="resetDefaultData()" class="px-4 py-3 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 font-semibold text-xs transition flex items-center gap-1.5">
                            <i class="fa-solid fa-rotate-left"></i> Reset Contoh
                        </button>
                    </div>
                </div>

                <div id="admin-product-list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <!-- Dirender lewat JS -->
                </div>
            </div>

            <!-- TAB 2: EDIT BIO, LOGO, GAMBAR BANNER & WHATSAPP -->
            <div id="admin-tab-profile" class="hidden">
                <form onsubmit="saveFullStoreProfile(event)" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200 space-y-6">
                    <div class="border-b border-stone-100 pb-4">
                        <h3 class="font-serif text-xl sm:text-2xl font-bold text-emeraldRaya-950">Edit Semua Identitas, Logo & Bio Toko</h3>
                        <p class="text-xs sm:text-sm text-stone-500">Ubah nama toko, bio, logo, gambar latar belakang, dan nomor WhatsApp penerima order.</p>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Nama Toko Kue <span class="text-red-500">*</span></label>
                            <input type="text" id="edit-store-name" required class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Slogan Singkat</label>
                            <input type="text" id="edit-store-subtitle" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Nomor WhatsApp Penerima Pesanan <span class="text-red-500">*</span></label>
                            <input type="text" id="edit-wa-number" required placeholder="08819665411" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm font-semibold text-emeraldRaya-900 focus:outline-none focus:border-emeraldRaya-600">
                            <p class="text-[11px] text-stone-400 mt-1">Default: 08819665411</p>
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Teks Badge Promo</label>
                            <input type="text" id="edit-tagline" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                        </div>
                    </div>

                    <!-- Edit Logo Toko -->
                    <div class="p-5 rounded-2xl bg-stone-50 border border-stone-200 space-y-4">
                        <h4 class="font-bold text-sm text-emeraldRaya-950 flex items-center gap-2">
                            <i class="fa-solid fa-image text-goldRaya-600"></i> Logo Toko
                        </h4>
                        <div class="flex flex-col sm:flex-row items-start sm:items-center gap-4">
                            <div id="preview-logo-box" class="w-20 h-20 rounded-full bg-emeraldRaya-900 text-goldRaya-400 flex items-center justify-center overflow-hidden border-2 border-goldRaya-400 shrink-0">
                                <i class="fa-solid fa-moon text-2xl"></i>
                            </div>
                            <div class="flex-1 w-full space-y-2">
                                <div class="flex flex-wrap gap-2">
                                    <label class="cursor-pointer px-4 py-2 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-xs font-semibold transition inline-flex items-center gap-2">
                                        <i class="fa-solid fa-upload"></i> Upload Gambar Logo
                                        <input type="file" accept="image/*" onchange="handleImageUpload(event, 'edit-logo-url', 'preview-logo-box')" class="hidden">
                                    </label>
                                    <button type="button" onclick="clearImageField('edit-logo-url', 'preview-logo-box', 'logo')" class="px-3 py-2 rounded-xl bg-stone-200 hover:bg-stone-300 text-stone-700 text-xs font-semibold transition">
                                        Reset Logo Default
                                    </button>
                                </div>
                                <input type="text" id="edit-logo-url" oninput="updateLogoPreview(this.value)" placeholder="Atau masukkan URL gambar logo..." class="w-full px-3.5 py-2 rounded-xl bg-white border border-stone-200 text-xs focus:outline-none focus:border-emeraldRaya-600">
                            </div>
                        </div>
                    </div>

                    <!-- Edit Banner Utama -->
                    <div class="p-5 rounded-2xl bg-stone-50 border border-stone-200 space-y-3">
                        <h4 class="font-bold text-sm text-emeraldRaya-950 flex items-center gap-2">
                            <i class="fa-solid fa-panorama text-goldRaya-600"></i> Gambar Latar Belakang Banner Utama
                        </h4>
                        <div class="flex flex-wrap gap-2">
                            <label class="cursor-pointer px-4 py-2 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-xs font-semibold transition inline-flex items-center gap-2">
                                <i class="fa-solid fa-upload"></i> Upload Foto Banner
                                <input type="file" accept="image/*" onchange="handleImageUpload(event, 'edit-banner-url', null)" class="hidden">
                            </label>
                            <button type="button" onclick="document.getElementById('edit-banner-url').value=''" class="px-3 py-2 rounded-xl bg-stone-200 hover:bg-stone-300 text-stone-700 text-xs font-semibold transition">
                                Hapus Banner
                            </button>
                        </div>
                        <input type="text" id="edit-banner-url" placeholder="Atau masukkan URL gambar banner..." class="w-full px-3.5 py-2 rounded-xl bg-white border border-stone-200 text-xs focus:outline-none focus:border-emeraldRaya-600">
                    </div>

                    <!-- Edit Judul & Bio -->
                    <div class="space-y-4">
                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Judul Besar Halaman Utama</label>
                            <input type="text" id="edit-hero-title" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Bio / Deskripsi Toko</label>
                            <textarea id="edit-store-bio" rows="3" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600"></textarea>
                        </div>
                    </div>

                    <div class="pt-4 border-t border-stone-100 flex justify-end">
                        <button type="submit" class="px-6 py-3.5 rounded-2xl bg-gradient-to-r from-emeraldRaya-800 to-emeraldRaya-900 hover:from-emeraldRaya-700 hover:to-emeraldRaya-800 text-white font-bold text-sm shadow-lg transition flex items-center gap-2">
                            <i class="fa-solid fa-floppy-disk"></i> Simpan Semua Perubahan
                        </button>
                    </div>
                </form>
            </div>

            <!-- TAB 3: KEAMANAN PIN ADMIN -->
            <div id="admin-tab-security" class="hidden">
                <form onsubmit="changeAdminPin(event)" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200 max-w-lg space-y-5">
                    <div>
                        <h3 class="font-serif text-xl font-bold text-emeraldRaya-950">Ganti PIN Khusus Admin</h3>
                        <p class="text-xs text-stone-500 mt-1">Hanya Anda sebagai admin yang mengetahui PIN ini untuk masuk ke Mode Admin.</p>
                    </div>

                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">PIN Admin Baru</label>
                        <input type="password" id="new-admin-pin" required minlength="4" maxlength="10" placeholder="Minimal 4 angka/huruf" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>

                    <button type="submit" class="px-5 py-3 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white font-bold text-sm transition">
                        Simpan PIN Baru
                    </button>
                </form>
            </div>

        </div>
    </div>

    <!-- MODAL LOGIN PIN ADMIN -->
    <div id="admin-pin-modal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/70 backdrop-blur-sm p-4">
        <div class="bg-white rounded-3xl max-w-sm w-full p-7 shadow-2xl border border-goldRaya-500/30 text-center relative">
            <button onclick="closeAdminPinModal()" class="absolute top-4 right-4 w-8 h-8 rounded-full bg-stone-100 hover:bg-stone-200 text-stone-600 flex items-center justify-center transition">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <div class="w-14 h-14 mx-auto mb-3 rounded-2xl bg-emeraldRaya-950 text-goldRaya-400 flex items-center justify-center text-xl shadow-md">
                <i class="fa-solid fa-crown"></i>
            </div>
            <h3 class="font-serif text-xl font-bold text-emeraldRaya-950 mb-1">Akses Khusus Admin</h3>
            <p class="text-xs text-stone-500 mb-5">Masukkan PIN Pemilik Toko untuk mengelola produk, logo, dan bio. (PIN Awal: <strong>1234</strong>)</p>

            <form onsubmit="verifyAdminPin(event)" class="space-y-3">
                <input type="password" id="pin-login-input" required placeholder="Masukkan PIN (1234)" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-center text-lg font-bold tracking-widest focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600">
                <button type="submit" class="w-full py-3 rounded-xl bg-gradient-to-r from-emeraldRaya-800 to-emeraldRaya-950 hover:from-emeraldRaya-700 hover:to-emeraldRaya-900 text-white font-bold text-sm shadow-md transition">
                    Masuk ke Mode Admin
                </button>
            </form>
        </div>
    </div>

    <!-- MODAL TAMBAH / EDIT PRODUK KUE -->
    <div id="product-modal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/65 backdrop-blur-sm p-4">
        <div class="bg-white rounded-3xl max-w-lg w-full p-6 sm:p-8 shadow-2xl border border-stone-100 max-h-[90vh] overflow-y-auto">
            <div class="flex justify-between items-center pb-4 border-b border-stone-100 mb-5">
                <h3 id="modal-title" class="font-serif text-xl sm:text-2xl font-bold text-emeraldRaya-950">Post Kue Kering Baru</h3>
                <button onclick="closeProductModal()" class="w-8 h-8 rounded-full bg-stone-100 hover:bg-stone-200 text-stone-600 flex items-center justify-center transition">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <form id="product-form" onsubmit="saveProduct(event)" class="space-y-4">
                <input type="hidden" id="edit-product-id">
                
                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Nama Kue Kering <span class="text-red-500">*</span></label>
                    <input type="text" id="prod-name" required placeholder="Contoh: Nastar Wisman Lumer" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Harga (Rp) <span class="text-red-500">*</span></label>
                        <input type="number" id="prod-price" required min="1000" step="500" placeholder="Contoh: 85000" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Ukuran / Kemasan <span class="text-red-500">*</span></label>
                        <input type="text" id="prod-weight" required placeholder="Contoh: Toples 500gr" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Kategori</label>
                        <select id="prod-category" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                            <option value="Klasik">Klasik</option>
                            <option value="Cokelat & Keju">Cokelat & Keju</option>
                            <option value="Paket Hampers">Paket Hampers</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Label Badge (Opsional)</label>
                        <input type="text" id="prod-badge" placeholder="Contoh: Best Seller / Baru" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Foto Kue Kering (Upload atau URL)</label>
                    <div class="flex gap-2 mb-2">
                        <label class="cursor-pointer px-3.5 py-2 rounded-xl bg-emeraldRaya-50 hover:bg-emeraldRaya-100 text-emeraldRaya-800 border border-emeraldRaya-200 text-xs font-semibold transition inline-flex items-center gap-1.5">
                            <i class="fa-solid fa-camera"></i> Upload Foto dari Galeri
                            <input type="file" accept="image/*" onchange="handleImageUpload(event, 'prod-image', null)" class="hidden">
                        </label>
                    </div>
                    <input type="text" id="prod-image" placeholder="Atau tempel link URL gambar (https://...)" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                </div>

                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Deskripsi Singkat <span class="text-red-500">*</span></label>
                    <textarea id="prod-desc" rows="3" required placeholder="Jelaskan keunggulan rasa, tekstur, atau bahan premium yang dipakai..." class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600"></textarea>
                </div>

                <div class="pt-3 flex items-center justify-end gap-3 border-t border-stone-100">
                    <button type="button" onclick="closeProductModal()" class="px-5 py-2.5 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 text-sm font-semibold transition">Batal</button>
                    <button type="submit" class="px-6 py-2.5 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-sm font-bold shadow-md transition">Simpan & Posting</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal Konfirmasi Hapus -->
    <div id="delete-modal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/65 backdrop-blur-sm p-4">
        <div class="bg-white rounded-3xl max-w-sm w-full p-6 text-center shadow-2xl">
            <div class="w-14 h-14 mx-auto mb-4 rounded-full bg-red-100 text-red-600 flex items-center justify-center text-2xl">
                <i class="fa-solid fa-trash-can"></i>
            </div>
            <h4 class="font-bold text-lg text-stone-800 mb-1">Hapus Kue Ini?</h4>
            <p class="text-sm text-stone-500 mb-6">Kue yang dihapus akan hilang dari daftar katalog website pemesanan.</p>
            <div class="flex gap-3">
                <button onclick="closeDeleteModal()" class="flex-1 py-2.5 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 font-semibold text-sm transition">Batal</button>
                <button id="confirm-delete-btn" class="flex-1 py-2.5 rounded-xl bg-red-600 hover:bg-red-700 text-white font-semibold text-sm transition">Ya, Hapus</button>
            </div>
        </div>
    </div>

    <script>
        // =====================================================================
        // DATA DEFAULT PRODUK & PROFIL TOKO
        // =====================================================================
        const defaultProducts = [
            {
                id: 'kue-1',
                name: 'Nastar Klasik Wisman Lumer',
                price: 95000,
                weight: 'Toples 500gr',
                category: 'Klasik',
                badge: 'Best Seller',
                image: 'https://images.unsplash.com/photo-1558961363-fa8fdf82db35?auto=format&fit=crop&w=800&q=80',
                desc: 'Adonan lembut dengan mentega Wisman asli, diisi selai nanas madu homemade yang manis legit dan lumer di mulut.'
            },
            {
                id: 'kue-2',
                name: 'Kastengel Keju Edam Spesial',
                price: 105000,
                weight: 'Toples 500gr',
                category: 'Cokelat & Keju',
                badge: 'Favorit',
                image: 'https://images.unsplash.com/photo-1590080875515-8a3a8dc5735e?auto=format&fit=crop&w=800&q=80',
                desc: 'Renyah gurih dengan perpaduan keju Edam tua dan taburan keju Cheddar panggang melimpah di setiap gigitan.'
            },
            {
                id: 'kue-3',
                name: 'Putri Salju Mede Premium',
                price: 85000,
                weight: 'Toples 500gr',
                category: 'Klasik',
                badge: '',
                image: 'https://images.unsplash.com/photo-1499636136210-6f4ee915583e?auto=format&fit=crop&w=800&q=80',
                desc: 'Kue bulan sabit lembut dengan campuran kacang mede panggang cincang, dibalut gula halus dingin yang manis pas.'
            },
            {
                id: 'kue-4',
                name: 'Choco Mede Cookies',
                price: 90000,
                weight: 'Toples 500gr',
                category: 'Cokelat & Keju',
                badge: 'Baru',
                image: 'https://images.unsplash.com/photo-1618923850107-d1a234d7a73a?auto=format&fit=crop&w=800&q=80',
                desc: 'Kukis cokelat pekat dengan topping kacang mede utuh panggang yang renyah. Sangat disukai anak-anak hingga dewasa.'
            },
            {
                id: 'kue-5',
                name: 'Hampers Mubarak 3 Toples',
                price: 275000,
                weight: 'Box Eksklusif (3 x 350gr)',
                category: 'Paket Hampers',
                badge: 'Hemat & Mewah',
                image: 'https://images.unsplash.com/photo-1513201099705-a9746e1e201f?auto=format&fit=crop&w=800&q=80',
                desc: 'Paket bingkisan Lebaran berisi Nastar, Kastengel, dan Putri Salju dalam box hijau emas eksklusif + gratis kartu ucapan.'
            },
            {
                id: 'kue-6',
                name: 'Lidah Kucing Rainbow / Original',
                price: 75000,
                weight: 'Toples 400gr',
                category: 'Klasik',
                badge: '',
                image: 'https://images.unsplash.com/photo-1548365328-8c6db3220e4c?auto=format&fit=crop&w=800&q=80',
                desc: 'Kue tipis yang super renyah, ringan, dan wangi susu mentega. Cocok untuk teman minum teh hangat saat silaturahmi.'
            }
        ];

        const defaultSettings = {
            storeName: 'Berkah Raya Cookies',
            storeSubtitle: 'Sajian Istimewa Idul Fitri',
            waNumber: '08819665411',
            tagline: 'Open Pre-Order Ramadhan & Idul Fitri • Homemade & Premium',
            heroTitle: 'Hadirkan Kehangatan Hari Kemenangan',
            storeBio: 'Kue kering buatan rumah dengan mentega pilihan, resep warisan keluarga, dan tanpa bahan pengawet. Cocok untuk sajian meja tamu maupun hampers orang tersayang.',
            logoUrl: '',
            bannerUrl: ''
        };

        let products = [];
        let storeSettings = {};
        let currentCategory = 'Semua';
        let orderRows = [];
        let isAdminAuthenticated = false;

        document.addEventListener('DOMContentLoaded', () => {
            loadStoreData();
            applyStoreSettings();
            renderPublicProducts();

            if (products.length > 0) {
                orderRows = [{ rowId: Date.now(), productId: products[0].id, qty: 1 }];
            } else {
                orderRows = [{ rowId: Date.now(), productId: '', qty: 1 }];
            }
            renderOrderRows();
            refreshGeneratedIndexLink(false);
        });

        // Muat data dari URL Hash (jika dibuka dari link share) atau localStorage
        function loadStoreData() {
            const hash = window.location.hash;
            if (hash && hash.startsWith('#store=')) {
                try {
                    const encoded = hash.replace('#store=', '');
                    const decodedJson = decodeURIComponent(escape(atob(encoded)));
                    const parsed = JSON.parse(decodedJson);
                    if (parsed.settings) storeSettings = { ...defaultSettings, ...parsed.settings };
                    if (parsed.products) products = parsed.products;
                    localStorage.setItem('raya_cookies_settings_shared', JSON.stringify(storeSettings));
                    localStorage.setItem('raya_cookies_products_shared', JSON.stringify(products));
                    return;
                } catch (e) {
                    console.warn('Gagal membaca parameter toko dari URL:', e);
                }
            }

            const savedSettings = localStorage.getItem('raya_cookies_settings_shared');
            const savedProducts = localStorage.getItem('raya_cookies_products_shared');

            storeSettings = savedSettings ? { ...defaultSettings, ...JSON.parse(savedSettings) } : { ...defaultSettings };
            products = savedProducts ? JSON.parse(savedProducts) : [...defaultProducts];
        }

        // Simpan dan langsung sinkronkan ke tampilan publik & link
        function syncAllData(showUpdatedBadge = true) {
            localStorage.setItem('raya_cookies_settings_shared', JSON.stringify(storeSettings));
            localStorage.setItem('raya_cookies_products_shared', JSON.stringify(products));
            
            // Langsung perbarui tampilan halaman publik di file yang sama
            applyStoreSettings();
            renderPublicProducts();
            renderOrderRows();
            refreshGeneratedIndexLink(showUpdatedBadge);
        }

        // =====================================================================
        // NAVIGASI ANTARA HALAMAN PEMESANAN & MODE ADMIN (1 FILE)
        // =====================================================================
        function openAdminAccess() {
            if (isAdminAuthenticated) {
                switchToAdminView();
            } else {
                document.getElementById('pin-login-input').value = '';
                const modal = document.getElementById('admin-pin-modal');
                modal.classList.remove('hidden');
                modal.classList.add('flex');
                setTimeout(() => document.getElementById('pin-login-input').focus(), 100);
            }
        }

        function closeAdminPinModal() {
            const modal = document.getElementById('admin-pin-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function verifyAdminPin(event) {
            event.preventDefault();
            const entered = document.getElementById('pin-login-input').value.trim();
            const savedPin = localStorage.getItem('raya_cookies_admin_pin') || '1234';

            if (entered === savedPin) {
                isAdminAuthenticated = true;
                closeAdminPinModal();
                switchToAdminView();
                showToast('Selamat datang di Mode Admin!', 'success');
            } else {
                showToast('PIN Admin salah! Coba lagi.', 'error');
            }
        }

        function switchToAdminView() {
            populateProfileForm();
            renderAdminProducts();
            refreshGeneratedIndexLink(false);
            document.getElementById('public-view').classList.add('hidden');
            document.getElementById('admin-view').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function switchToPublicView() {
            applyStoreSettings();
            renderPublicProducts();
            renderOrderRows();
            document.getElementById('admin-view').classList.add('hidden');
            document.getElementById('public-view').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function logoutAdmin() {
            isAdminAuthenticated = false;
            switchToPublicView();
            showToast('Mode Admin dikunci.', 'info');
        }

        function changeAdminPin(event) {
            event.preventDefault();
            const newPin = document.getElementById('new-admin-pin').value.trim();
            if (newPin.length < 4) {
                showToast('PIN minimal 4 karakter.', 'error');
                return;
            }
            localStorage.setItem('raya_cookies_admin_pin', newPin);
            document.getElementById('new-admin-pin').value = '';
            showToast('PIN Admin berhasil diperbarui!', 'success');
        }

        // =====================================================================
        // LOGIKA HALAMAN PUBLIK & PEMESANAN
        // =====================================================================
        function applyStoreSettings() {
            document.getElementById('nav-store-name').textContent = storeSettings.storeName;
            document.getElementById('nav-store-subtitle').textContent = storeSettings.storeSubtitle;
            document.getElementById('footer-store-name').textContent = storeSettings.storeName;
            document.getElementById('footer-store-bio').textContent = storeSettings.storeBio;
            document.getElementById('hero-tagline').textContent = storeSettings.tagline;
            document.getElementById('hero-bio').textContent = storeSettings.storeBio;
            document.getElementById('hero-title').textContent = storeSettings.heroTitle;
            document.title = `${storeSettings.storeName} - Pemesanan Kue Kering`;
            document.getElementById('display-wa-number').textContent = formatPhoneDisplay(storeSettings.waNumber);

            const navLogoContainer = document.getElementById('nav-logo-container');
            const heroLogoWrapper = document.getElementById('hero-logo-wrapper');
            if (storeSettings.logoUrl && storeSettings.logoUrl.trim() !== '') {
                navLogoContainer.innerHTML = `<img src="${storeSettings.logoUrl}" alt="Logo" class="w-full h-full object-cover">`;
                heroLogoWrapper.innerHTML = `<img src="${storeSettings.logoUrl}" alt="Logo Toko" class="w-full h-full object-cover">`;
            } else {
                navLogoContainer.innerHTML = `<i class="fa-solid fa-moon text-lg"></i>`;
                heroLogoWrapper.innerHTML = `<i class="fa-solid fa-star-and-crescent text-3xl sm:text-4xl text-goldRaya-400"></i>`;
            }

            const bannerWrapper = document.getElementById('hero-bg-image-wrapper');
            const bannerImg = document.getElementById('hero-bg-image');
            if (storeSettings.bannerUrl && storeSettings.bannerUrl.trim() !== '') {
                bannerImg.src = storeSettings.bannerUrl;
                bannerWrapper.classList.remove('hidden');
            } else {
                bannerWrapper.classList.add('hidden');
            }
        }

        function renderPublicProducts() {
            const grid = document.getElementById('product-grid');
            const emptyState = document.getElementById('empty-state');
            grid.innerHTML = '';

            const filtered = currentCategory === 'Semua' 
                ? products 
                : products.filter(p => p.category === currentCategory);

            if (filtered.length === 0) {
                grid.classList.add('hidden');
                emptyState.classList.remove('hidden');
                return;
            }

            grid.classList.remove('hidden');
            emptyState.classList.add('hidden');

            filtered.forEach(item => {
                const fallbackImg = `https://placehold.co/600x400/064e3b/fbbf24?text=${encodeURIComponent(item.name)}`;
                const imgUrl = item.image && item.image.trim() !== '' ? item.image : fallbackImg;

                const card = document.createElement('div');
                card.className = 'group bg-white rounded-3xl overflow-hidden shadow-md hover:shadow-xl border border-stone-100 transition-all duration-300 flex flex-col justify-between';

                card.innerHTML = `
                    <div>
                        <div class="relative h-52 sm:h-56 overflow-hidden bg-emeraldRaya-50">
                            <img src="${imgUrl}" alt="${item.name}" onerror="this.onerror=null;this.src='${fallbackImg}';" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                            <div class="absolute top-3 left-3 flex flex-wrap gap-1.5">
                                <span class="px-3 py-1 rounded-full bg-emeraldRaya-950/85 backdrop-blur-sm text-white text-[11px] font-semibold">
                                    ${item.category}
                                </span>
                                ${item.badge ? `
                                <span class="px-3 py-1 rounded-full bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 text-emeraldRaya-950 text-[11px] font-bold shadow-sm">
                                    ${item.badge}
                                </span>` : ''}
                            </div>
                        </div>

                        <div class="p-5 sm:p-6">
                            <h3 class="font-serif font-bold text-lg sm:text-xl text-emeraldRaya-950 leading-snug mb-1">${item.name}</h3>
                            <span class="inline-block text-xs font-medium text-stone-400 mb-3">
                                <i class="fa-solid fa-jar mr-1 text-goldRaya-600"></i> ${item.weight}
                            </span>
                            <p class="text-xs sm:text-sm text-stone-600 line-clamp-3 leading-relaxed">
                                ${item.desc}
                            </p>
                        </div>
                    </div>

                    <div class="px-5 sm:px-6 pb-5 sm:pb-6 pt-3 border-t border-stone-100 flex items-center justify-between gap-3">
                        <div>
                            <span class="text-[11px] text-stone-400 block">Harga</span>
                            <span class="text-lg sm:text-xl font-bold text-emeraldRaya-800">${formatRupiah(item.price)}</span>
                        </div>
                        <button onclick="addProductToOrderForm('${item.id}')" class="px-4 py-2.5 rounded-xl bg-emeraldRaya-50 hover:bg-emeraldRaya-800 text-emeraldRaya-800 hover:text-white font-semibold text-xs sm:text-sm border border-emeraldRaya-200 hover:border-emeraldRaya-800 transition flex items-center gap-1.5">
                            <i class="fa-solid fa-plus"></i> Pilih Kue
                        </button>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        function filterCategory(category) {
            currentCategory = category;
            document.querySelectorAll('.filter-btn').forEach(btn => {
                if (btn.textContent.trim() === category) {
                    btn.classList.add('bg-emeraldRaya-900', 'text-white');
                    btn.classList.remove('bg-white', 'text-stone-600', 'border', 'border-stone-200');
                } else {
                    btn.classList.remove('bg-emeraldRaya-900', 'text-white');
                    btn.classList.add('bg-white', 'text-stone-600', 'border', 'border-stone-200');
                }
            });
            renderPublicProducts();
        }

        // Form Pemesanan Multi-Item
        function renderOrderRows() {
            const container = document.getElementById('order-items-container');
            container.innerHTML = '';

            if (orderRows.length === 0 && products.length > 0) {
                orderRows.push({ rowId: Date.now(), productId: products[0].id, qty: 1 });
            }

            orderRows.forEach((row, index) => {
                if (!products.some(p => p.id === row.productId) && products.length > 0) {
                    row.productId = products[0].id;
                }

                const optionsHtml = products.map(p => `
                    <option value="${p.id}" ${p.id === row.productId ? 'selected' : ''}>
                        ${p.name} (${p.weight}) - ${formatRupiah(p.price)}
                    </option>
                `).join('');

                const rowEl = document.createElement('div');
                rowEl.className = 'p-3.5 rounded-2xl bg-stone-50 border border-stone-200 flex flex-col sm:flex-row items-stretch sm:items-center gap-2.5';
                rowEl.innerHTML = `
                    <div class="flex-1">
                        <span class="text-[11px] font-bold text-stone-400 uppercase block mb-1">Pilihan Kue #${index + 1}</span>
                        <select onchange="updateOrderRowProduct(${row.rowId}, this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-medium focus:outline-none focus:border-emeraldRaya-600">
                            ${optionsHtml || '<option value="">Belum ada kue</option>'}
                        </select>
                    </div>
                    <div class="flex items-end gap-2">
                        <div class="w-24">
                            <span class="text-[11px] font-bold text-stone-400 uppercase block mb-1">Jumlah</span>
                            <input type="number" min="1" value="${row.qty}" oninput="updateOrderRowQty(${row.rowId}, this.value)" onchange="updateOrderRowQty(${row.rowId}, this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-bold text-center focus:outline-none focus:border-emeraldRaya-600">
                        </div>
                        ${orderRows.length > 1 ? `
                        <button type="button" onclick="removeOrderRow(${row.rowId})" class="h-[42px] px-3 rounded-xl bg-red-100 hover:bg-red-600 text-red-600 hover:text-white transition flex items-center justify-center" title="Hapus Baris Ini">
                            <i class="fa-solid fa-trash-can text-xs"></i>
                        </button>` : ''}
                    </div>
                `;
                container.appendChild(rowEl);
            });

            calculateGrandTotal();
        }

        function addOrderItemRow(selectedProductId = null) {
            const defaultId = selectedProductId || (products.length > 0 ? products[0].id : '');
            orderRows.push({
                rowId: Date.now() + Math.random(),
                productId: defaultId,
                qty: 1
            });
            renderOrderRows();
        }

        function addProductToOrderForm(productId) {
            const existingRow = orderRows.find(r => r.productId === productId);
            if (existingRow) {
                existingRow.qty += 1;
                renderOrderRows();
                showToast('Jumlah pesanan kue ditambahkan (+1)!', 'success');
            } else {
                addOrderItemRow(productId);
                showToast('Varian kue ditambahkan ke formulir pesanan!', 'success');
            }
            document.getElementById('form-pemesanan').scrollIntoView({ behavior: 'smooth' });
        }

        function updateOrderRowProduct(rowId, newProductId) {
            const row = orderRows.find(r => r.rowId === rowId);
            if (row) {
                row.productId = newProductId;
                calculateGrandTotal();
            }
        }

        function updateOrderRowQty(rowId, newQty) {
            const row = orderRows.find(r => r.rowId === rowId);
            if (row) {
                const parsed = parseInt(newQty, 10);
                row.qty = parsed > 0 ? parsed : 1;
                calculateGrandTotal();
            }
        }

        function removeOrderRow(rowId) {
            if (orderRows.length <= 1) return;
            orderRows = orderRows.filter(r => r.rowId !== rowId);
            renderOrderRows();
        }

        function calculateGrandTotal() {
            let grandTotal = 0;
            let totalToples = 0;

            orderRows.forEach(row => {
                const product = products.find(p => p.id === row.productId);
                if (product) {
                    grandTotal += product.price * row.qty;
                    totalToples += row.qty;
                }
            });

            document.getElementById('order-total-price').textContent = formatRupiah(grandTotal);
            document.getElementById('order-total-items-count').textContent = `${orderRows.length} jenis kue (Total ${totalToples} toples/paket)`;

            const badge = document.getElementById('nav-cart-badge');
            if (totalToples > 0) {
                badge.textContent = totalToples;
                badge.classList.remove('hidden');
            } else {
                badge.classList.add('hidden');
            }
        }

        function getFormattedTargetWa() {
            let raw = (storeSettings.waNumber || '08819665411').replace(/\D/g, '');
            if (raw.startsWith('0')) {
                raw = '62' + raw.substring(1);
            } else if (!raw.startsWith('62')) {
                raw = '62' + raw;
            }
            return raw;
        }

        function submitOrderToWhatsApp(event) {
            event.preventDefault();

            const buyerName = document.getElementById('order-name').value.trim();
            const buyerWa = document.getElementById('order-buyer-wa').value.trim();
            const address = document.getElementById('order-address').value.trim() || '-';

            let itemsTextList = '';
            let grandTotal = 0;
            let validItemCount = 0;

            orderRows.forEach((row, idx) => {
                const product = products.find(p => p.id === row.productId);
                if (product) {
                    validItemCount++;
                    const subtotal = product.price * row.qty;
                    grandTotal += subtotal;
                    itemsTextList += `${idx + 1}. *${product.name}* (${product.weight})\n   Jumlah: ${row.qty} x ${formatRupiah(product.price)} = *${formatRupiah(subtotal)}*\n`;
                }
            });

            if (validItemCount === 0) {
                showToast('Silakan pilih minimal 1 jenis kue.', 'error');
                return;
            }

            const targetWa = getFormattedTargetWa();
            const message = 
`Assalamu'alaikum *${storeSettings.storeName}* 🌙✨
Saya ingin memesan kue kering Idul Fitri:

*Data Pemesan:*
• Nama: ${buyerName}
• No. HP/WA: ${buyerWa}

*Rincian Pesanan Kue:*
${itemsTextList}
*Total Estimasi Harga: ${formatRupiah(grandTotal)}*

*Alamat / Catatan:*
${address}

Mohon konfirmasi ketersediaan & total pembayarannya ya. Terima kasih! 🙏`;

            const encodedMessage = encodeURIComponent(message);
            const waUrl = `https://wa.me/${targetWa}?text=${encodedMessage}`;

            showToast('Mengarahkan langsung ke WhatsApp...', 'success');
            window.location.href = waUrl;
        }

        function chatDirectWhatsApp() {
            const targetWa = getFormattedTargetWa();
            const text = encodeURIComponent(`Assalamu'alaikum ${storeSettings.storeName}, saya ingin bertanya mengenai pesanan kue kering Lebaran.`);
            window.open(`https://wa.me/${targetWa}?text=${text}`, '_blank');
        }

        function copyWaNumber() {
            const rawWa = storeSettings.waNumber || '08819665411';
            const tempInput = document.createElement('input');
            tempInput.value = rawWa;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);
            showToast('Nomor WhatsApp berhasil disalin!', 'success');
        }

        // =====================================================================
        // LOGIKA MODE ADMIN & LINK PEMBAGIAN
        // =====================================================================
        function switchAdminTab(tabName) {
            ['products', 'profile', 'security'].forEach(t => {
                const panel = document.getElementById(`admin-tab-${t}`);
                const btn = document.getElementById(`tab-btn-${t}`);
                if (t === tabName) {
                    panel.classList.remove('hidden');
                    btn.classList.add('bg-emeraldRaya-900', 'text-white');
                    btn.classList.remove('text-stone-600', 'hover:bg-stone-100');
                } else {
                    panel.classList.add('hidden');
                    btn.classList.remove('bg-emeraldRaya-900', 'text-white');
                    btn.classList.add('text-stone-600', 'hover:bg-stone-100');
                }
            });
        }

        function buildCustomerUrlWithPayload() {
            const baseUrl = window.location.href.split('#')[0];
            try {
                const compactProducts = products.map(p => ({
                    ...p,
                    image: p.image && p.image.startsWith('data:') ? '' : p.image
                }));
                const compactSettings = {
                    ...storeSettings,
                    logoUrl: storeSettings.logoUrl && storeSettings.logoUrl.startsWith('data:') ? '' : storeSettings.logoUrl,
                    bannerUrl: storeSettings.bannerUrl && storeSettings.bannerUrl.startsWith('data:') ? '' : storeSettings.bannerUrl
                };
                const payload = JSON.stringify({ settings: compactSettings, products: compactProducts });
                const encoded = btoa(unescape(encodeURIComponent(payload)));
                if (encoded.length < 7500) {
                    return `${baseUrl}#store=${encoded}`;
                }
            } catch (e) {}
            return baseUrl;
        }

        function refreshGeneratedIndexLink(highlight = false) {
            const shareUrl = buildCustomerUrlWithPayload();
            const linkInput = document.getElementById('generated-index-link');
            const badge = document.getElementById('link-updated-badge');

            if (linkInput) linkInput.value = shareUrl;

            if (highlight && badge) {
                badge.classList.remove('hidden');
                clearTimeout(window.linkBadgeTimeout);
                window.linkBadgeTimeout = setTimeout(() => {
                    badge.classList.add('hidden');
                }, 4000);
            }
        }

        function copyShareableCustomerLink() {
            const shareUrl = buildCustomerUrlWithPayload();
            const linkInput = document.getElementById('generated-index-link');
            if (linkInput) {
                linkInput.value = shareUrl;
                linkInput.select();
                document.execCommand('copy');
            } else {
                const tempInput = document.createElement('input');
                tempInput.value = shareUrl;
                document.body.appendChild(tempInput);
                tempInput.select();
                document.execCommand('copy');
                document.body.removeChild(tempInput);
            }
            showToast('Link pemesanan berhasil disalin! Siap dibagikan ke pembeli.', 'success');
        }

        function populateProfileForm() {
            document.getElementById('edit-store-name').value = storeSettings.storeName;
            document.getElementById('edit-store-subtitle').value = storeSettings.storeSubtitle;
            document.getElementById('edit-wa-number').value = storeSettings.waNumber;
            document.getElementById('edit-tagline').value = storeSettings.tagline;
            document.getElementById('edit-hero-title').value = storeSettings.heroTitle;
            document.getElementById('edit-store-bio').value = storeSettings.storeBio;
            document.getElementById('edit-logo-url').value = storeSettings.logoUrl || '';
            document.getElementById('edit-banner-url').value = storeSettings.bannerUrl || '';
            updateLogoPreview(storeSettings.logoUrl || '');
        }

        function saveFullStoreProfile(event) {
            event.preventDefault();
            storeSettings.storeName = document.getElementById('edit-store-name').value.trim() || defaultSettings.storeName;
            storeSettings.storeSubtitle = document.getElementById('edit-store-subtitle').value.trim() || defaultSettings.storeSubtitle;
            storeSettings.waNumber = document.getElementById('edit-wa-number').value.trim() || '08819665411';
            storeSettings.tagline = document.getElementById('edit-tagline').value.trim() || defaultSettings.tagline;
            storeSettings.heroTitle = document.getElementById('edit-hero-title').value.trim() || defaultSettings.heroTitle;
            storeSettings.storeBio = document.getElementById('edit-store-bio').value.trim() || defaultSettings.storeBio;
            storeSettings.logoUrl = document.getElementById('edit-logo-url').value.trim();
            storeSettings.bannerUrl = document.getElementById('edit-banner-url').value.trim();

            syncAllData(true);
            showToast('Semua perubahan profil, bio & logo berhasil disimpan!', 'success');
        }

        function handleImageUpload(event, targetInputId, previewBoxId) {
            const file = event.target.files[0];
            if (!file) return;

            const reader = new FileReader();
            reader.onload = function(e) {
                const img = new Image();
                img.onload = function() {
                    const canvas = document.createElement('canvas');
                    const maxDim = 800;
                    let w = img.width;
                    let h = img.height;
                    if (w > maxDim || h > maxDim) {
                        if (w > h) {
                            h = Math.round((h * maxDim) / w);
                            w = maxDim;
                        } else {
                            w = Math.round((w * maxDim) / h);
                            h = maxDim;
                        }
                    }
                    canvas.width = w;
                    canvas.height = h;
                    const ctx = canvas.getContext('2d');
                    ctx.drawImage(img, 0, 0, w, h);
                    const compressedDataUrl = canvas.toDataURL('image/jpeg', 0.8);

                    document.getElementById(targetInputId).value = compressedDataUrl;
                    if (previewBoxId === 'preview-logo-box') {
                        updateLogoPreview(compressedDataUrl);
                    }
                    showToast('Gambar berhasil dimuat!', 'success');
                };
                img.src = e.target.result;
            };
            reader.readAsDataURL(file);
        }

        function updateLogoPreview(url) {
            const box = document.getElementById('preview-logo-box');
            if (!box) return;
            if (url && url.trim() !== '') {
                box.innerHTML = `<img src="${url}" alt="Preview Logo" class="w-full h-full object-cover">`;
            } else {
                box.innerHTML = `<i class="fa-solid fa-moon text-2xl"></i>`;
            }
        }

        function clearImageField(inputId, previewBoxId, type) {
            document.getElementById(inputId).value = '';
            if (type === 'logo') updateLogoPreview('');
        }

        function renderAdminProducts() {
            const list = document.getElementById('admin-product-list');
            list.innerHTML = '';

            products.forEach(item => {
                const fallbackImg = `https://placehold.co/600x400/064e3b/fbbf24?text=${encodeURIComponent(item.name)}`;
                const imgUrl = item.image && item.image.trim() !== '' ? item.image : fallbackImg;

                const card = document.createElement('div');
                card.className = 'bg-white rounded-3xl overflow-hidden shadow-sm border border-stone-200 flex flex-col justify-between';
                card.innerHTML = `
                    <div>
                        <div class="relative h-44 bg-stone-100">
                            <img src="${imgUrl}" alt="${item.name}" onerror="this.onerror=null;this.src='${fallbackImg}';" class="w-full h-full object-cover">
                            <span class="absolute top-3 left-3 px-2.5 py-1 rounded-full bg-emeraldRaya-950/85 text-white text-[11px] font-semibold">${item.category}</span>
                        </div>
                        <div class="p-5">
                            <h3 class="font-bold text-base text-stone-800 mb-1">${item.name}</h3>
                            <p class="text-xs text-stone-500 mb-2">${item.weight} • <strong class="text-emeraldRaya-800">${formatRupiah(item.price)}</strong></p>
                            <p class="text-xs text-stone-600 line-clamp-2">${item.desc}</p>
                        </div>
                    </div>
                    <div class="px-5 pb-5 pt-3 border-t border-stone-100 flex gap-2">
                        <button onclick="openProductModal('${item.id}')" class="flex-1 py-2 rounded-xl bg-amber-100 hover:bg-amber-500 text-amber-800 hover:text-white font-semibold text-xs transition flex items-center justify-center gap-1.5">
                            <i class="fa-solid fa-pen"></i> Edit Kue
                        </button>
                        <button onclick="confirmDeleteProduct('${item.id}')" class="px-3.5 py-2 rounded-xl bg-red-100 hover:bg-red-600 text-red-600 hover:text-white font-semibold text-xs transition" title="Hapus Kue">
                            <i class="fa-solid fa-trash"></i>
                        </button>
                    </div>
                `;
                list.appendChild(card);
            });
        }

        function openProductModal(productId = null) {
            const modal = document.getElementById('product-modal');
            const title = document.getElementById('modal-title');
            const form = document.getElementById('product-form');

            form.reset();
            document.getElementById('edit-product-id').value = '';

            if (productId) {
                const product = products.find(p => p.id === productId);
                if (product) {
                    title.textContent = 'Edit Kue Kering';
                    document.getElementById('edit-product-id').value = product.id;
                    document.getElementById('prod-name').value = product.name;
                    document.getElementById('prod-price').value = product.price;
                    document.getElementById('prod-weight').value = product.weight;
                    document.getElementById('prod-category').value = product.category;
                    document.getElementById('prod-badge').value = product.badge || '';
                    document.getElementById('prod-image').value = product.image || '';
                    document.getElementById('prod-desc').value = product.desc;
                }
            } else {
                title.textContent = 'Post Kue Kering Baru';
            }

            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closeProductModal() {
            const modal = document.getElementById('product-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function saveProduct(event) {
            event.preventDefault();
            const editId = document.getElementById('edit-product-id').value;
            const newProductData = {
                id: editId || 'kue-' + Date.now(),
                name: document.getElementById('prod-name').value.trim(),
                price: parseInt(document.getElementById('prod-price').value, 10),
                weight: document.getElementById('prod-weight').value.trim(),
                category: document.getElementById('prod-category').value,
                badge: document.getElementById('prod-badge').value.trim(),
                image: document.getElementById('prod-image').value.trim(),
                desc: document.getElementById('prod-desc').value.trim()
            };

            if (editId) {
                const index = products.findIndex(p => p.id === editId);
                if (index !== -1) {
                    products[index] = newProductData;
                    showToast('Data kue berhasil diperbarui!', 'success');
                }
            } else {
                products.unshift(newProductData);
                showToast('Kue baru berhasil diposting ke halaman utama!', 'success');
            }

            syncAllData(true);
            renderAdminProducts();
            closeProductModal();
        }

        let productToDeleteId = null;
        function confirmDeleteProduct(id) {
            productToDeleteId = id;
            const modal = document.getElementById('delete-modal');
            modal.classList.remove('hidden');
            modal.classList.add('flex');

            document.getElementById('confirm-delete-btn').onclick = () => {
                products = products.filter(p => p.id !== productToDeleteId);
                syncAllData(true);
                renderAdminProducts();
                closeDeleteModal();
                showToast('Kue telah dihapus.', 'info');
            };
        }

        function closeDeleteModal() {
            const modal = document.getElementById('delete-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
            productToDeleteId = null;
        }

        function resetDefaultData() {
            products = [...defaultProducts];
            syncAllData(true);
            renderAdminProducts();
            showToast('Katalog dikembalikan ke data contoh awal.', 'info');
        }

        function formatRupiah(angka) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR',
                minimumFractionDigits: 0
            }).format(angka);
        }

        function formatPhoneDisplay(num) {
            const cleaned = ('' + num).replace(/\D/g, '');
            if (cleaned.startsWith('0') && cleaned.length >= 10) {
                return `${cleaned.slice(0, 4)}-${cleaned.slice(4, 8)}-${cleaned.slice(8)}`;
            }
            return cleaned;
        }

        function showToast(message, type = 'info') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            
            let bgClass = 'bg-emeraldRaya-900 border-goldRaya-500/40 text-white';
            let icon = 'fa-circle-info text-goldRaya-400';

            if (type === 'success') {
                bgClass = 'bg-emeraldRaya-800 border-emerald-400 text-white';
                icon = 'fa-circle-check text-goldRaya-300';
            } else if (type === 'error') {
                bgClass = 'bg-red-800 border-red-400 text-white';
                icon = 'fa-circle-exclamation text-red-200';
            }

            toast.className = `pointer-events-auto flex items-center gap-3 px-4 py-3 rounded-2xl border shadow-xl text-xs sm:text-sm font-medium transform transition-all duration-300 translate-y-0 opacity-100 ${bgClass}`;
            toast.innerHTML = `<i class="fa-solid ${icon} text-base"></i><span>${message}</span>`;

            container.appendChild(toast);

            setTimeout(() => {
                toast.classList.add('opacity-0', '-translate-y-2');
                setTimeout(() => toast.remove(), 300);
            }, 3000);
        }
    </script>
</body>
</html>
