<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DF Sultan - Katalog & Pemesanan Kue Kering Idul Fitri</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Playfair Display & Plus Jakarta Sans -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,700;1,600&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <script>
        // Konfigurasi tema Ramadhan & Idul Fitri (Emerald Green & Gold)
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
        };
    </script>
</head>
<body class="bg-[#FAF8F5] text-stone-800 font-sans antialiased selection:bg-emeraldRaya-800 selection:text-goldRaya-300">

    <!-- Container Notifikasi Toast -->
    <div id="toast-container" class="fixed top-5 right-5 z-50 flex flex-col gap-2 max-w-xs w-full pointer-events-none"></div>

    <!-- ===================================================================== -->
    <!-- TAMPILAN 1: WEBSITE PUBLIK & PEMESANAN                                -->
    <!-- ===================================================================== -->
    <div id="public-view">
        <!-- Navbar Publik -->
        <nav class="sticky top-0 z-40 bg-emeraldRaya-950/95 backdrop-blur-md text-white border-b border-goldRaya-500/30 shadow-lg">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex justify-between items-center h-16 sm:h-20">
                    <!-- Logo & Identitas Toko -->
                    <div class="flex items-center gap-3 min-w-0">
                        <div class="w-10 h-10 sm:w-11 sm:h-11 rounded-full bg-gradient-to-br from-goldRaya-400 to-goldRaya-600 flex items-center justify-center text-emeraldRaya-950 shadow-md overflow-hidden border border-goldRaya-300/50 shrink-0">
                            <img id="nav-logo-img" src="" alt="Logo DF Sultan" class="w-full h-full object-cover hidden" onerror="handleImageFallback(this, 'nav-logo-fallback')">
                            <i id="nav-logo-fallback" class="fa-solid fa-moon text-lg"></i>
                        </div>
                        <div class="min-w-0">
                            <span id="nav-store-name" class="font-serif font-bold text-base sm:text-xl tracking-wide text-goldRaya-400 block leading-tight truncate">DF Sultan</span>
                            <span id="nav-store-subtitle" class="text-[11px] sm:text-xs text-emerald-200/80 block truncate">Sajian Istimewa Idul Fitri • Malang - Turen</span>
                        </div>
                    </div>

                    <!-- Navigasi & Tombol Aksi -->
                    <div class="flex items-center gap-2 sm:gap-3 shrink-0">
                        <a href="#katalog-kue" class="hidden sm:inline-block px-3 py-2 text-xs sm:text-sm font-medium text-emerald-100 hover:text-goldRaya-300 transition">
                            Katalog Kue
                        </a>
                        <a href="#form-pemesanan" class="px-3.5 py-2 sm:px-5 sm:py-2.5 rounded-xl text-xs sm:text-sm font-bold bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 text-emeraldRaya-950 hover:from-goldRaya-300 hover:to-goldRaya-400 shadow-md transition flex items-center gap-2">
                            <i class="fa-solid fa-basket-shopping"></i>
                            <span>Pesan</span>
                            <span id="nav-cart-badge" class="hidden px-1.5 py-0.5 text-[10px] rounded-full bg-emeraldRaya-950 text-goldRaya-300 font-bold">0</span>
                        </a>
                        <button type="button" onclick="openAdminModal()" class="px-3 py-2 rounded-xl bg-emeraldRaya-900 hover:bg-emeraldRaya-800 border border-goldRaya-500/40 text-goldRaya-300 text-xs font-semibold transition flex items-center gap-1.5" aria-label="Buka Mode Admin">
                            <i class="fa-solid fa-lock"></i>
                            <span class="hidden md:inline">Admin</span>
                        </button>
                    </div>
                </div>
            </div>
        </nav>

        <!-- Hero Section -->
        <header class="relative bg-gradient-to-b from-emeraldRaya-950 via-emeraldRaya-900 to-emeraldRaya-800 text-white overflow-hidden">
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
                <div class="mx-auto mb-5 w-24 h-24 sm:w-28 sm:h-28 rounded-full bg-emeraldRaya-950/80 border-2 border-goldRaya-400 shadow-xl flex items-center justify-center overflow-hidden">
                    <img id="hero-logo-img" src="" alt="Logo Utama DF Sultan" class="w-full h-full object-cover hidden" onerror="handleImageFallback(this, 'hero-logo-fallback')">
                    <i id="hero-logo-fallback" class="fa-solid fa-star-and-crescent text-3xl sm:text-4xl text-goldRaya-400"></i>
                </div>

                <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-emeraldRaya-950/80 border border-goldRaya-500/40 text-goldRaya-300 text-xs sm:text-sm font-medium mb-5 shadow-sm">
                    <i class="fa-solid fa-sparkles text-goldRaya-400"></i>
                    <span id="hero-tagline">Open Pre-Order Ramadhan & Idul Fitri • Malang - Turen</span>
                </div>

                <h1 id="hero-title" class="font-serif text-3xl sm:text-5xl lg:text-6xl font-bold tracking-tight text-white mb-4 leading-tight">
                    Hadirkan Kehangatan Hari Kemenangan
                </h1>

                <p id="hero-bio" class="max-w-2xl mx-auto text-sm sm:text-lg text-emerald-100/90 mb-8 leading-relaxed">
                    Kue kering buatan rumah DF Sultan (Malang - Turen) dengan bahan pilihan, resep keluarga, dan tanpa bahan pengawet. Cocok untuk sajian meja tamu maupun hampers Idul Fitri.
                </p>

                <div class="flex flex-col sm:flex-row items-center justify-center gap-3 sm:gap-4">
                    <a href="#katalog-kue" class="w-full sm:w-auto px-6 py-3.5 rounded-2xl bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 hover:from-goldRaya-300 hover:to-goldRaya-400 text-emeraldRaya-950 font-bold text-sm sm:text-base shadow-lg shadow-goldRaya-500/20 transition transform hover:-translate-y-0.5 flex items-center justify-center gap-2">
                        <i class="fa-solid fa-cookie-bite"></i> Lihat Katalog Kue
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
                    <span class="text-xs font-bold uppercase tracking-widest text-goldRaya-600 block mb-1">Pilihan Kemasan 250gr, 500gr & Hampers</span>
                    <h2 class="font-serif text-2xl sm:text-4xl font-bold text-emeraldRaya-950">Katalog Kue Kering Lebaran</h2>
                </div>

                <!-- Filter Kategori -->
                <div class="flex flex-wrap gap-2" id="category-filters">
                    <button type="button" onclick="filterCategory('Semua')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-emeraldRaya-900 text-white transition">Semua</button>
                    <button type="button" onclick="filterCategory('Klasik')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white text-stone-600 border border-stone-200 hover:border-emeraldRaya-600 transition">Klasik</button>
                    <button type="button" onclick="filterCategory('Cokelat & Keju')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white text-stone-600 border border-stone-200 hover:border-emeraldRaya-600 transition">Cokelat & Keju</button>
                    <button type="button" onclick="filterCategory('Paket Hampers')" class="filter-btn px-4 py-2 rounded-xl text-xs sm:text-sm font-semibold bg-white text-stone-600 border border-stone-200 hover:border-emeraldRaya-600 transition">Paket Hampers</button>
                </div>
            </div>

            <!-- Grid Produk -->
            <div id="product-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8"></div>

            <!-- State Kosong -->
            <div id="empty-state" class="hidden text-center py-16 bg-white rounded-3xl border border-dashed border-stone-300">
                <div class="w-16 h-16 mx-auto mb-4 rounded-full bg-emeraldRaya-50 text-emeraldRaya-700 flex items-center justify-center text-2xl">
                    <i class="fa-solid fa-box-open"></i>
                </div>
                <h3 class="text-lg font-bold text-stone-800 mb-1">Belum ada kue di kategori ini</h3>
                <p class="text-sm text-stone-500">Silakan pilih kategori lain untuk melihat koleksi kue kami.</p>
            </div>
        </main>

        <!-- Form Pemesanan Multi-Item & Pembayaran Transfer / COD -->
        <section id="form-pemesanan" class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 py-12 sm:py-16">
            <div class="bg-white rounded-3xl shadow-xl border border-goldRaya-500/20 overflow-hidden">
                <div class="grid grid-cols-1 lg:grid-cols-5">
                    <!-- Kolom Kiri: Info Toko & WhatsApp Penjual -->
                    <div class="lg:col-span-2 bg-gradient-to-br from-emeraldRaya-950 to-emeraldRaya-800 text-white p-6 sm:p-8 flex flex-col justify-between relative overflow-hidden">
                        <div class="relative z-10">
                            <span class="inline-block px-3 py-1 rounded-full bg-goldRaya-500/20 text-goldRaya-300 text-xs font-semibold mb-4">
                                Pemesanan Mudah & Cepat
                            </span>
                            <h3 class="font-serif text-2xl sm:text-3xl font-bold mb-3 text-white">Formulir Pesanan Kue Kering</h3>
                            <p class="text-sm text-emerald-100/80 mb-6 leading-relaxed">
                                Pilih beberapa jenis kue beserta ukuran toplesnya, tentukan metode pembayaran <strong>Transfer Bank</strong> atau <strong>COD (Bayar di Tempat)</strong>, lalu kirim otomatis ke WhatsApp penjual.
                            </p>

                            <div class="p-4 rounded-2xl bg-emeraldRaya-950/60 border border-goldRaya-500/30 mb-6">
                                <span class="text-xs text-emerald-300 block mb-1">WhatsApp Resmi Penjual (Malang - Turen):</span>
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
                            <p><i class="fa-solid fa-check text-goldRaya-400 mr-2"></i>Tersedia kemasan 250gr, 500gr & paket hampers</p>
                            <p><i class="fa-solid fa-check text-goldRaya-400 mr-2"></i>Pembayaran Transfer Bank atau COD (Bayar di Tempat)</p>
                            <p><i class="fa-solid fa-check text-goldRaya-400 mr-2"></i>Rincian pesanan & metode bayar otomatis ke WhatsApp</p>
                        </div>
                    </div>

                    <!-- Kolom Kanan: Form Input Pemesanan (Tanpa Kolom No. WA Pemesan & Tanpa QRIS) -->
                    <div class="lg:col-span-3 p-6 sm:p-8 lg:p-10">
                        <form id="order-form" onsubmit="submitOrderToWhatsApp(event)" class="space-y-5">
                            <div>
                                <label for="order-name" class="block text-sm font-semibold text-stone-700 mb-1.5">Nama Lengkap Pemesan <span class="text-red-500">*</span></label>
                                <input type="text" id="order-name" required placeholder="Contoh: Ibu Siti Aminah" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-stone-800 text-sm focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600 focus:bg-white transition">
                            </div>

                            <!-- Baris Pesanan Multi-Item -->
                            <div class="space-y-3">
                                <div class="flex items-center justify-between">
                                    <label class="block text-sm font-semibold text-stone-700">Jenis Kue, Kemasan & Jumlah <span class="text-red-500">*</span></label>
                                    <span class="text-xs text-stone-400">Bisa pilih lebih dari 1 jenis</span>
                                </div>

                                <div id="order-items-container" class="space-y-3"></div>

                                <button type="button" onclick="addOrderItemRow()" class="w-full py-2.5 px-4 rounded-xl border-2 border-dashed border-emeraldRaya-600/40 hover:border-emeraldRaya-700 bg-emeraldRaya-50/60 hover:bg-emeraldRaya-50 text-emeraldRaya-800 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                                    <i class="fa-solid fa-plus-circle"></i>
                                    <span>Tambah Jenis Kue Lainnya</span>
                                </button>
                            </div>

                            <!-- Pilihan Metode Pembayaran: Transfer Bank atau COD -->
                            <div class="space-y-3">
                                <div>
                                    <label for="order-payment" class="block text-sm font-semibold text-stone-700 mb-1.5">Metode Pembayaran <span class="text-red-500">*</span></label>
                                    <select id="order-payment" onchange="togglePaymentDetails()" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-stone-800 text-sm font-semibold focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600 focus:bg-white transition">
                                        <option value="Transfer Bank">Transfer Bank</option>
                                        <option value="COD (Bayar di Tempat)">COD (Bayar di Tempat)</option>
                                    </select>
                                </div>

                                <!-- Detail Rekening Jika Pilih Transfer Bank -->
                                <div id="transfer-detail-box" class="p-4 rounded-2xl bg-emeraldRaya-50/90 border border-emeraldRaya-200 space-y-2">
                                    <div class="flex items-center justify-between gap-2">
                                        <span class="text-xs font-bold uppercase tracking-wider text-emeraldRaya-950 flex items-center gap-1.5">
                                            <i class="fa-solid fa-building-columns text-emeraldRaya-700"></i> Informasi Rekening Transfer
                                        </span>
                                        <button type="button" onclick="copyBankAccount()" class="px-2.5 py-1 rounded-lg bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-[11px] font-semibold transition flex items-center gap-1">
                                            <i class="fa-regular fa-copy"></i> Salin No. Rek
                                        </button>
                                    </div>
                                    <p id="display-bank-info" class="text-xs sm:text-sm font-semibold text-stone-800">Bank BRI • 315101055033531 a.n. Dewa Perwira Septyan</p>
                                    <p class="text-[11px] text-stone-500">Detail metode pembayaran ini akan otomatis disertakan dalam pesan WhatsApp pesanan Anda.</p>
                                </div>

                                <!-- Info Singkat Jika Pilih COD -->
                                <div id="cod-detail-box" class="hidden p-4 rounded-2xl bg-amber-50/90 border border-amber-200 space-y-1">
                                    <span class="text-xs font-bold uppercase tracking-wider text-amber-900 flex items-center gap-1.5">
                                        <i class="fa-solid fa-hand-holding-dollar text-goldRaya-600"></i> Pembayaran COD (Bayar di Tempat)
                                    </span>
                                    <p class="text-xs text-stone-700">Pembayaran dilakukan secara tunai saat pesanan diterima/diantar sesuai kesepakatan area Malang - Turen.</p>
                                </div>
                            </div>

                            <!-- Ringkasan Total -->
                            <div class="p-4 rounded-2xl bg-emeraldRaya-50 border border-emeraldRaya-200 flex items-center justify-between">
                                <div>
                                    <span class="text-xs text-emeraldRaya-800 font-semibold block">Total Estimasi Pesanan:</span>
                                    <span id="order-total-items-count" class="text-xs text-stone-500">1 jenis kue (Total 1 toples/paket)</span>
                                </div>
                                <span id="order-total-price" class="text-xl sm:text-2xl font-bold text-emeraldRaya-900">Rp 0</span>
                            </div>

                            <!-- Alamat & Catatan -->
                            <div>
                                <label for="order-address" class="block text-sm font-semibold text-stone-700 mb-1.5">Alamat Pengiriman / Catatan Tambahan</label>
                                <textarea id="order-address" rows="2" placeholder="Tulis alamat pengiriman (Malang / Turen / luar kota) atau catatan tambahan..." class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-stone-800 text-sm focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600 focus:bg-white transition"></textarea>
                            </div>

                            <button type="submit" class="w-full py-4 px-6 rounded-2xl bg-gradient-to-r from-green-600 to-emeraldRaya-800 hover:from-green-500 hover:to-emeraldRaya-700 text-white font-bold text-base shadow-lg shadow-emeraldRaya-900/20 transition transform hover:-translate-y-0.5 flex items-center justify-center gap-3">
                                <i class="fa-brands fa-whatsapp text-2xl text-white"></i>
                                <span>Kirim Pesanan ke WhatsApp Sekarang</span>
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="bg-emeraldRaya-950 text-emerald-200/80 py-10 border-t border-goldRaya-500/20">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-center sm:text-left">
                <div>
                    <p id="footer-store-name" class="font-serif font-bold text-lg text-goldRaya-400">DF Sultan</p>
                    <p id="footer-store-bio" class="text-xs mt-1 max-w-md text-emerald-200/70">Kue kering buatan rumah DF Sultan (Malang - Turen) untuk sajian Ramadhan & Idul Fitri.</p>
                </div>
                <div class="flex flex-wrap items-center justify-center gap-2.5">
                    <button type="button" onclick="chatDirectWhatsApp()" class="px-4 py-2.5 rounded-xl bg-green-600 hover:bg-green-500 text-white text-xs sm:text-sm font-semibold transition flex items-center gap-2 shadow-md">
                        <i class="fa-brands fa-whatsapp text-base"></i> Chat WhatsApp Penjual
                    </button>
                    <button type="button" onclick="openAdminModal()" class="px-3.5 py-2.5 rounded-xl bg-emeraldRaya-900 hover:bg-emeraldRaya-800 border border-goldRaya-500/30 text-goldRaya-300 text-xs font-semibold transition flex items-center gap-1.5">
                        <i class="fa-solid fa-lock"></i> Admin
                    </button>
                </div>
            </div>
        </footer>
    </div>

    <!-- ===================================================================== -->
    <!-- TAMPILAN 2: DASHBOARD MODE ADMIN                                      -->
    <!-- ===================================================================== -->
    <div id="admin-view" class="hidden min-h-screen bg-stone-100">
        <nav class="sticky top-0 z-40 bg-emeraldRaya-950 text-white border-b border-goldRaya-500/40 shadow-md">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between gap-2">
                <div class="flex items-center gap-3 min-w-0">
                    <div class="w-9 h-9 rounded-xl bg-goldRaya-500 text-emeraldRaya-950 flex items-center justify-center font-bold shrink-0">
                        <i class="fa-solid fa-crown"></i>
                    </div>
                    <div class="min-w-0">
                        <span class="font-bold text-sm sm:text-base text-goldRaya-400 block leading-none truncate">Mode Admin Toko</span>
                        <span class="text-[11px] text-emerald-200 truncate block">Kelola Produk, Foto Permanen, Rekening & Kode HTML</span>
                    </div>
                </div>

                <div class="flex items-center gap-2 shrink-0">
                    <button type="button" onclick="saveAndApplyToPublic()" class="px-3.5 py-2 rounded-xl bg-emerald-600 hover:bg-emerald-500 text-white text-xs sm:text-sm font-bold shadow transition flex items-center gap-1.5">
                        <i class="fa-solid fa-floppy-disk"></i>
                        <span>Simpan Perubahan</span>
                    </button>
                    <button type="button" onclick="switchToPublicView()" class="px-3.5 py-2 rounded-xl bg-goldRaya-500 hover:bg-goldRaya-400 text-emeraldRaya-950 text-xs sm:text-sm font-bold shadow transition flex items-center gap-1.5">
                        <i class="fa-solid fa-eye"></i>
                        <span class="hidden sm:inline">Mode Publik</span>
                    </button>
                    <button type="button" onclick="logoutAdmin()" class="px-3 py-2 rounded-xl bg-red-600/90 hover:bg-red-600 text-white text-xs font-semibold transition flex items-center gap-1.5" title="Keluar Mode Admin">
                        <i class="fa-solid fa-right-from-bracket"></i>
                    </button>
                </div>
            </div>
        </nav>

        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-6">
            <!-- Tab Navigasi Admin -->
            <div class="flex flex-wrap gap-2 bg-white p-2 rounded-2xl shadow-sm border border-stone-200">
                <button type="button" onclick="switchAdminTab('products')" id="tab-btn-products" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl bg-emeraldRaya-900 text-white font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-cookie"></i> Kelola & Post Kue
                </button>
                <button type="button" onclick="switchAdminTab('profile')" id="tab-btn-profile" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl text-stone-600 hover:bg-stone-100 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-store"></i> Edit Bio, Logo & Rekening
                </button>
                <button type="button" onclick="switchAdminTab('code')" id="tab-btn-code" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl text-stone-600 hover:bg-stone-100 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-code"></i> Kode HTML Terbaru
                </button>
                <button type="button" onclick="switchAdminTab('security')" id="tab-btn-security" class="flex-1 sm:flex-none px-5 py-2.5 rounded-xl text-stone-600 hover:bg-stone-100 font-semibold text-xs sm:text-sm transition flex items-center justify-center gap-2">
                    <i class="fa-solid fa-shield-halved"></i> Ubah Password
                </button>
            </div>

            <!-- TAB 1: KELOLA & POST PRODUK KUE -->
            <div id="admin-tab-products" class="space-y-6">
                <div class="bg-white rounded-3xl p-6 shadow-sm border border-stone-200 flex flex-col sm:flex-row sm:items-center justify-between gap-4">
                    <div>
                        <h3 class="font-serif text-xl sm:text-2xl font-bold text-emeraldRaya-950">Daftar Kue & Paket Hampers</h3>
                        <p class="text-xs sm:text-sm text-stone-500">Tambah kue baru, ubah harga 250gr/500gr/hampers, ganti foto permanen, atau hapus item.</p>
                    </div>
                    <div class="flex flex-wrap gap-2">
                        <button type="button" onclick="openProductModal()" class="px-5 py-3 rounded-xl bg-gradient-to-r from-emeraldRaya-800 to-emeraldRaya-900 hover:from-emeraldRaya-700 hover:to-emeraldRaya-800 text-white font-bold text-xs sm:text-sm shadow-md transition flex items-center gap-2">
                            <i class="fa-solid fa-plus"></i> Post Kue Baru
                        </button>
                        <button type="button" onclick="resetDefaultData()" class="px-4 py-3 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 font-semibold text-xs transition flex items-center gap-1.5">
                            <i class="fa-solid fa-rotate-left"></i> Reset Default
                        </button>
                    </div>
                </div>

                <div id="admin-product-list" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6"></div>
            </div>

            <!-- TAB 2: EDIT BIO, LOGO & REKENING TRANSFER -->
            <div id="admin-tab-profile" class="hidden">
                <form onsubmit="saveFullStoreProfile(event)" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200 space-y-6">
                    <div class="border-b border-stone-100 pb-4">
                        <h3 class="font-serif text-xl sm:text-2xl font-bold text-emeraldRaya-950">Edit Identitas, Logo, Rekening & Bio Toko</h3>
                        <p class="text-xs sm:text-sm text-stone-500">Foto yang diunggah tersimpan permanen di browser namun tetap bisa diganti atau dihapus kapan saja.</p>
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
                        </div>

                        <div>
                            <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Teks Badge Promo</label>
                            <input type="text" id="edit-tagline" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                        </div>
                    </div>

                    <!-- Edit Logo Toko (Permanen & Bisa Diubah) -->
                    <div class="p-5 rounded-2xl bg-stone-50 border border-stone-200 space-y-3">
                        <div class="flex flex-wrap items-center justify-between gap-2">
                            <h4 class="font-bold text-sm text-emeraldRaya-950 flex items-center gap-2">
                                <i class="fa-solid fa-image text-goldRaya-600"></i> Logo Toko (Tersimpan Permanen & Bisa Diubah)
                            </h4>
                            <span id="logo-persistent-badge" class="text-[11px] font-semibold px-2.5 py-1 rounded-full bg-stone-200 text-stone-600">Ikon Bawaan</span>
                        </div>
                        <div class="flex flex-col sm:flex-row items-center gap-4">
                            <div class="w-16 h-16 rounded-full bg-emeraldRaya-900 text-goldRaya-400 flex items-center justify-center overflow-hidden border-2 border-goldRaya-400 shrink-0">
                                <img id="preview-logo-img" src="" alt="Preview Logo" class="w-full h-full object-cover hidden">
                                <i id="preview-logo-icon" class="fa-solid fa-moon text-xl"></i>
                            </div>
                            <div class="flex-1 w-full space-y-2">
                                <div class="flex flex-wrap gap-2">
                                    <label class="cursor-pointer px-4 py-2 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-xs font-semibold transition inline-flex items-center gap-1.5">
                                        <i class="fa-solid fa-upload"></i> Upload / Ganti Logo
                                        <input type="file" accept="image/*" onchange="handleLogoUpload(event)" class="hidden">
                                    </label>
                                    <button type="button" onclick="clearLogoPhoto()" class="px-3.5 py-2 rounded-xl bg-red-100 hover:bg-red-600 text-red-700 hover:text-white text-xs font-semibold transition">
                                        Hapus Logo
                                    </button>
                                </div>
                                <input type="text" id="edit-logo-url" oninput="updateLogoPreview(this.value)" placeholder="Atau tempel URL / nama file logo (kosongkan untuk ikon default)" class="w-full px-3.5 py-2 rounded-xl bg-white border border-stone-200 text-xs focus:outline-none focus:border-emeraldRaya-600">
                            </div>
                        </div>
                    </div>

                    <!-- Edit Detail Rekening Transfer Bank -->
                    <div class="p-5 rounded-2xl bg-stone-50 border border-stone-200 space-y-3">
                        <h4 class="font-bold text-sm text-emeraldRaya-950 flex items-center gap-2">
                            <i class="fa-solid fa-building-columns text-goldRaya-600"></i> Detail Rekening Transfer Bank
                        </h4>
                        <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
                            <div>
                                <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Nama Bank</label>
                                <input type="text" id="edit-bank-name" placeholder="Bank BRI" class="w-full px-4 py-2.5 rounded-xl bg-white border border-stone-200 text-xs sm:text-sm focus:outline-none focus:border-emeraldRaya-600">
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Nomor Rekening</label>
                                <input type="text" id="edit-bank-account" placeholder="315101055033531" class="w-full px-4 py-2.5 rounded-xl bg-white border border-stone-200 text-xs sm:text-sm focus:outline-none focus:border-emeraldRaya-600">
                            </div>
                            <div>
                                <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Atas Nama (a.n.)</label>
                                <input type="text" id="edit-bank-holder" placeholder="Dewa Perwira Septyan" class="w-full px-4 py-2.5 rounded-xl bg-white border border-stone-200 text-xs sm:text-sm focus:outline-none focus:border-emeraldRaya-600">
                            </div>
                        </div>
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
                            <i class="fa-solid fa-floppy-disk"></i> Simpan Perubahan
                        </button>
                    </div>
                </form>
            </div>

            <!-- TAB 3: KODE HTML OTOMATIS SESUAI POSTINGAN ADMIN -->
            <div id="admin-tab-code" class="hidden">
                <div class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200 space-y-4">
                    <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-3 border-b border-stone-100 pb-4">
                        <div>
                            <h3 class="font-serif text-xl sm:text-2xl font-bold text-emeraldRaya-950">Kode HTML Sinkron Postingan Admin</h3>
                            <p class="text-xs sm:text-sm text-stone-500">Kode di bawah otomatis memperbarui data toko, rekening transfer, harga, dan kue sesuai yang disimpan di Mode Admin.</p>
                        </div>
                        <div class="flex flex-wrap gap-2">
                            <button type="button" onclick="rebuildGeneratedHtmlCode(true)" class="px-4 py-2.5 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 text-xs font-bold transition flex items-center gap-1.5">
                                <i class="fa-solid fa-rotate"></i> Segarkan Kode
                            </button>
                            <button type="button" onclick="copyGeneratedHtmlCode()" class="px-4 py-2.5 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-xs font-bold transition flex items-center gap-1.5">
                                <i class="fa-regular fa-copy"></i> Salin Kode HTML
                            </button>
                            <button type="button" onclick="downloadGeneratedHtmlFile()" class="px-4 py-2.5 rounded-xl bg-goldRaya-500 hover:bg-goldRaya-400 text-emeraldRaya-950 text-xs font-bold transition flex items-center gap-1.5">
                                <i class="fa-solid fa-download"></i> Unduh index.html
                            </button>
                        </div>
                    </div>

                    <textarea id="generated-html-output" rows="16" readonly class="w-full p-4 rounded-2xl bg-stone-950 text-emerald-300 font-mono text-xs leading-relaxed border border-stone-800 focus:outline-none"></textarea>
                </div>
            </div>

            <!-- TAB 4: KEAMANAN PASSWORD ADMIN -->
            <div id="admin-tab-security" class="hidden">
                <form onsubmit="changeAdminPin(event)" class="bg-white rounded-3xl p-6 sm:p-8 shadow-sm border border-stone-200 max-w-lg space-y-5">
                    <div>
                        <h3 class="font-serif text-xl font-bold text-emeraldRaya-950">Ganti Password Admin</h3>
                        <p class="text-xs text-stone-500 mt-1">Masukkan password baru untuk masuk ke Mode Admin (minimal 4 karakter).</p>
                    </div>

                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1.5">Password Admin Baru</label>
                        <input type="password" id="new-admin-pin" required minlength="4" maxlength="20" placeholder="Masukkan password baru" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>

                    <button type="submit" class="px-5 py-3 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white font-bold text-sm transition">
                        Simpan Password Baru
                    </button>
                </form>
            </div>
        </div>
    </div>

    <!-- MODAL LOGIN PASSWORD ADMIN (TERSEMBUNYI TANPA PETUNJUK PASSWORD) -->
    <div id="admin-pin-modal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/70 backdrop-blur-sm p-4">
        <div class="bg-white rounded-3xl max-w-sm w-full p-7 shadow-2xl border border-goldRaya-500/30 text-center relative">
            <button type="button" onclick="closeAdminModal()" class="absolute top-4 right-4 w-8 h-8 rounded-full bg-stone-100 hover:bg-stone-200 text-stone-600 flex items-center justify-center transition">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <div class="w-14 h-14 mx-auto mb-3 rounded-2xl bg-emeraldRaya-950 text-goldRaya-400 flex items-center justify-center text-xl shadow-md">
                <i class="fa-solid fa-crown"></i>
            </div>
            <h3 class="font-serif text-xl font-bold text-emeraldRaya-950 mb-1">Akses Mode Admin</h3>
            <p class="text-xs text-stone-500 mb-5">Masukkan password pemilik toko untuk mengelola katalog & pengaturan.</p>

            <form onsubmit="verifyAdminPin(event)" class="space-y-3">
                <input type="password" id="pin-login-input" required placeholder="Password Admin" autocomplete="current-password" class="w-full px-4 py-3 rounded-xl bg-stone-50 border border-stone-200 text-center text-base font-bold tracking-widest focus:outline-none focus:ring-2 focus:ring-emeraldRaya-600">
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
                <button type="button" onclick="closeProductModal()" class="w-8 h-8 rounded-full bg-stone-100 hover:bg-stone-200 text-stone-600 flex items-center justify-center transition">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <form id="product-form" onsubmit="saveProduct(event)" class="space-y-4">
                <input type="hidden" id="edit-product-id">

                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Nama Kue / Paket <span class="text-red-500">*</span></label>
                    <input type="text" id="prod-name" required placeholder="Contoh: Nastar Nanas Spesial" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Harga Utama (Rp) <span class="text-red-500">*</span></label>
                        <input type="number" id="prod-price" required min="1000" step="500" placeholder="45000" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Kemasan Utama <span class="text-red-500">*</span></label>
                        <input type="text" id="prod-weight" required placeholder="Toples 250gr" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Harga Kemasan 500gr (Opsional)</label>
                        <input type="number" id="prod-price-500" min="0" step="500" placeholder="85000" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                    <div>
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Label Badge (Opsional)</label>
                        <input type="text" id="prod-badge" placeholder="Contoh: Best Seller" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Kategori</label>
                    <select id="prod-category" class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600">
                        <option value="Klasik">Klasik</option>
                        <option value="Cokelat & Keju">Cokelat & Keju</option>
                        <option value="Paket Hampers">Paket Hampers</option>
                    </select>
                </div>

                <!-- Upload & Edit Foto Produk Permanen (Tetap Bisa Diubah) -->
                <div class="p-4 rounded-2xl bg-stone-50 border border-stone-200 space-y-3">
                    <div class="flex items-center justify-between gap-2">
                        <label class="block text-xs font-bold uppercase tracking-wider text-stone-700">Foto Produk Permanen (Bisa Diganti)</label>
                        <span id="prod-photo-status" class="text-[11px] font-semibold px-2 py-0.5 rounded-full bg-stone-200 text-stone-600">Default</span>
                    </div>
                    <div class="flex items-center gap-3">
                        <img id="preview-prod-img" src="" alt="Preview Kue" class="w-16 h-16 rounded-xl object-cover bg-white border border-stone-200 hidden shrink-0">
                        <div class="flex-1 space-y-2">
                            <div class="flex flex-wrap gap-2">
                                <label class="cursor-pointer px-3.5 py-2 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-xs font-semibold transition inline-flex items-center gap-1.5">
                                    <i class="fa-solid fa-upload"></i> Upload / Ganti Foto
                                    <input type="file" accept="image/*" onchange="handleProductPhotoUpload(event)" class="hidden">
                                </label>
                                <button type="button" onclick="clearProductPhoto()" class="px-3 py-2 rounded-xl bg-red-100 hover:bg-red-600 text-red-700 hover:text-white text-xs font-semibold transition">
                                    Hapus Foto
                                </button>
                            </div>
                            <input type="text" id="prod-image" oninput="updateProductModalPreview(this.value)" placeholder="Nama file / URL gambar (contoh: 1001103667_3.jpg)" class="w-full px-3 py-2 rounded-xl bg-white border border-stone-200 text-xs focus:outline-none focus:border-emeraldRaya-600">
                        </div>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold uppercase tracking-wider text-stone-600 mb-1">Deskripsi Singkat <span class="text-red-500">*</span></label>
                    <textarea id="prod-desc" rows="3" required placeholder="Jelaskan komposisi dan rasa kue..." class="w-full px-4 py-2.5 rounded-xl bg-stone-50 border border-stone-200 text-sm focus:outline-none focus:border-emeraldRaya-600"></textarea>
                </div>

                <div class="pt-3 flex items-center justify-end gap-3 border-t border-stone-100">
                    <button type="button" onclick="closeProductModal()" class="px-5 py-2.5 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 text-sm font-semibold transition">Batal</button>
                    <button type="submit" class="px-6 py-2.5 rounded-xl bg-emeraldRaya-800 hover:bg-emeraldRaya-700 text-white text-sm font-bold shadow-md transition">Simpan Perubahan</button>
                </div>
            </form>
        </div>
    </div>

    <!-- MODAL KONFIRMASI HAPUS -->
    <div id="delete-modal" class="fixed inset-0 z-50 hidden items-center justify-center bg-black/65 backdrop-blur-sm p-4">
        <div class="bg-white rounded-3xl max-w-sm w-full p-6 text-center shadow-2xl">
            <div class="w-14 h-14 mx-auto mb-4 rounded-full bg-red-100 text-red-600 flex items-center justify-center text-2xl">
                <i class="fa-solid fa-trash-can"></i>
            </div>
            <h4 class="font-bold text-lg text-stone-800 mb-1">Hapus Kue Ini?</h4>
            <p class="text-sm text-stone-500 mb-6">Kue yang dihapus akan hilang dari katalog & pemesanan setelah disimpan.</p>
            <div class="flex gap-3">
                <button type="button" onclick="closeDeleteModal()" class="flex-1 py-2.5 rounded-xl bg-stone-100 hover:bg-stone-200 text-stone-700 font-semibold text-sm transition">Batal</button>
                <button type="button" id="confirm-delete-btn" class="flex-1 py-2.5 rounded-xl bg-red-600 hover:bg-red-700 text-white font-semibold text-sm transition">Ya, Hapus</button>
            </div>
        </div>
    </div>

    <script>
        // =====================================================================
        // 1. KONFIGURASI DEFAULT TOKO & PRODUK DF SULTAN
        // =====================================================================
        const DEFAULT_ADMIN_PIN = '240901';

        const defaultSettings = {
            storeName: 'DF Sultan',
            storeSubtitle: 'Sajian Istimewa Idul Fitri • Malang - Turen',
            waNumber: '08819665411',
            tagline: 'Open Pre-Order Ramadhan & Idul Fitri • Malang - Turen',
            heroTitle: 'Hadirkan Kehangatan Hari Kemenangan',
            storeBio: 'Kue kering buatan rumah DF Sultan (Malang - Turen) dengan bahan pilihan, resep keluarga, dan tanpa bahan pengawet. Cocok untuk sajian meja tamu maupun hampers Idul Fitri.',
            logoUrl: '',
            bankName: 'Bank BRI',
            bankAccount: '315101055033531',
            bankHolder: 'Dewa Perwira Septyan'
        };

        const defaultProducts = [
            {
                id: 'kue-nastar',
                name: 'Nastar Nanas Spesial',
                price: 45000,
                weight: 'Toples 250gr',
                price500: 85000,
                category: 'Klasik',
                badge: 'Best Seller',
                image: '1001103667_3.jpg',
                desc: 'Nastar lembut dengan selai nanas pilihan dan aroma butter wangi. Tersedia kemasan 250gr & 500gr.'
            },
            {
                id: 'kue-kastengel',
                name: 'Kastengel Keju',
                price: 45000,
                weight: 'Toples 250gr',
                price500: 85000,
                category: 'Cokelat & Keju',
                badge: 'Favorit',
                image: '1001103668_3.jpg',
                desc: 'Kastengel gurih renyah dengan taburan keju melimpah. Tersedia kemasan 250gr & 500gr.'
            },
            {
                id: 'kue-thumbprint',
                name: 'Thumbprint Cookies',
                price: 45000,
                weight: 'Toples 250gr',
                price500: 85000,
                category: 'Klasik',
                badge: 'Spesial',
                image: '1001103666_3.jpg',
                desc: 'Kukis renyah dengan balutan keju dan isian selai strawberry manis segar. Tersedia kemasan 250gr & 500gr.'
            },
            {
                id: 'kue-lidah-kucing',
                name: 'Lidah Kucing Keju Premium',
                price: 40000,
                weight: 'Toples 250gr',
                price500: 85000,
                category: 'Cokelat & Keju',
                badge: 'Harga Spesial',
                image: '1001103665_3.jpg',
                desc: 'Lidah kucing tipis super renyah dengan sentuhan keju gurih. Tersedia kemasan 250gr & 500gr.'
            },
            {
                id: 'hampers-3-toples',
                name: 'Paket Hampers 3 Toples',
                price: 145000,
                weight: 'Paket 3 Toples',
                price500: 0,
                category: 'Paket Hampers',
                badge: 'Hampers Hemat',
                image: '1001104008.jpg',
                desc: 'Rangkaian 3 toples kue kering pilihan DF Sultan dengan kemasan spesial Idul Fitri.'
            },
            {
                id: 'hampers-4-toples',
                name: 'Paket Hampers 4 Toples Lengkap',
                price: 190000,
                weight: 'Paket 4 Toples',
                price500: 0,
                category: 'Paket Hampers',
                badge: 'Paling Lengkap',
                image: '1001104009.jpg',
                desc: 'Paket lengkap 4 varian kue kering DF Sultan untuk hantaran hari raya.'
            }
        ];

        const STORAGE_SETTINGS_KEY = 'dfsultan_settings_v13';
        const STORAGE_PRODUCTS_KEY = 'dfsultan_products_v13';
        const STORAGE_PIN_KEY = 'dfsultan_admin_pin_v13';
        const STORAGE_PERSISTENT_PHOTOS_KEY = 'dfsultan_persistent_photos_v13';

        let storeSettings = {};
        let products = [];
        let persistentPhotos = { logoDataUrl: '', productsById: {} };
        let cardSelectedVariant = {};
        let orderRows = [];
        let currentCategory = 'Semua';
        let isAdminAuthenticated = false;

        // =====================================================================
        // INISIALISASI & PENYIMPANAN DATA
        // =====================================================================
        document.addEventListener('DOMContentLoaded', () => {
            loadStoreData();
            applyStoreSettings();
            renderPublicProducts();

            const firstProd = products[0];
            const firstVar = firstProd ? getProductVariants(firstProd)[0] : null;
            orderRows = firstProd
                ? [{ rowId: Date.now(), productId: firstProd.id, variantLabel: firstVar ? firstVar.label : firstProd.weight, qty: 1 }]
                : [{ rowId: Date.now(), productId: '', variantLabel: '', qty: 1 }];

            renderOrderRows();
            togglePaymentDetails();
            rebuildGeneratedHtmlCode(false);
        });

        function loadStoreData() {
            try {
                const savedPhotos = localStorage.getItem(STORAGE_PERSISTENT_PHOTOS_KEY);
                if (savedPhotos) {
                    const parsedPhotos = JSON.parse(savedPhotos);
                    persistentPhotos = {
                        logoDataUrl: parsedPhotos.logoDataUrl || '',
                        productsById: parsedPhotos.productsById || {}
                    };
                }

                const savedSettings = localStorage.getItem(STORAGE_SETTINGS_KEY);
                storeSettings = savedSettings ? { ...defaultSettings, ...JSON.parse(savedSettings) } : { ...defaultSettings };
                if (persistentPhotos.logoDataUrl) {
                    storeSettings.logoUrl = persistentPhotos.logoDataUrl;
                }

                const savedProducts = localStorage.getItem(STORAGE_PRODUCTS_KEY);
                const rawProducts = savedProducts ? JSON.parse(savedProducts) : [...defaultProducts];
                products = rawProducts.map(item => {
                    const hasSavedPhoto = Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id);
                    return {
                        ...item,
                        price500: typeof item.price500 === 'number'
                            ? item.price500
                            : (item.category === 'Paket Hampers' ? 0 : 85000),
                        image: hasSavedPhoto ? persistentPhotos.productsById[item.id] : (item.image || '')
                    };
                });
            } catch (err) {
                storeSettings = { ...defaultSettings };
                products = [...defaultProducts];
            }
        }

        function savePersistentPhotos() {
            try {
                localStorage.setItem(STORAGE_PERSISTENT_PHOTOS_KEY, JSON.stringify(persistentPhotos));
            } catch (err) {
                showToast('Ukuran foto melebihi kapasitas browser, gunakan file/URL lebih ringan.', 'error');
            }
        }

        function syncAllData(updateHtmlExport = true) {
            if (persistentPhotos.logoDataUrl) {
                storeSettings.logoUrl = persistentPhotos.logoDataUrl;
            }
            products = products.map(item => {
                if (Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id)) {
                    return { ...item, image: persistentPhotos.productsById[item.id] };
                }
                return item;
            });

            localStorage.setItem(STORAGE_SETTINGS_KEY, JSON.stringify(storeSettings));
            localStorage.setItem(STORAGE_PRODUCTS_KEY, JSON.stringify(products));
            savePersistentPhotos();

            applyStoreSettings();
            renderPublicProducts();
            renderOrderRows();
            togglePaymentDetails();
            if (updateHtmlExport) {
                rebuildGeneratedHtmlCode(false);
            }
        }

        // =====================================================================
        // VARIAN KEMASAN (250GR, 500GR RP 85.000 & HAMPERS)
        // =====================================================================
        function getProductVariants(product) {
            const variants = [
                { label: product.weight || 'Toples 250gr', price: Number(product.price) || 0 }
            ];
            if (Number(product.price500) > 0) {
                variants.push({ label: 'Toples 500gr', price: Number(product.price500) });
            }
            return variants;
        }

        function getSelectedVariant(product, preferredLabel = null) {
            const variants = getProductVariants(product);
            const targetLabel = preferredLabel || cardSelectedVariant[product.id];
            return variants.find(v => v.label === targetLabel) || variants[0];
        }

        function selectCardVariant(productId, variantLabel) {
            cardSelectedVariant[productId] = variantLabel;
            renderPublicProducts();
        }

        // =====================================================================
        // MODE ADMIN & PASSWORD TERSEMBUNYI (DEFAULT: 240901)
        // =====================================================================
        function openAdminModal() {
            if (isAdminAuthenticated) {
                switchToAdminView();
                return;
            }
            document.getElementById('pin-login-input').value = '';
            const modal = document.getElementById('admin-pin-modal');
            modal.classList.remove('hidden');
            modal.classList.add('flex');
            setTimeout(() => document.getElementById('pin-login-input').focus(), 100);
        }

        function closeAdminModal() {
            const modal = document.getElementById('admin-pin-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function verifyAdminPin(event) {
            event.preventDefault();
            const enteredPin = document.getElementById('pin-login-input').value.trim();
            const savedPin = localStorage.getItem(STORAGE_PIN_KEY) || DEFAULT_ADMIN_PIN;

            if (enteredPin === savedPin) {
                isAdminAuthenticated = true;
                closeAdminModal();
                switchToAdminView();
                showToast('Selamat datang di Mode Admin DF Sultan!', 'success');
            } else {
                showToast('Password admin salah.', 'error');
            }
        }

        function switchToAdminView() {
            populateProfileForm();
            renderAdminProducts();
            rebuildGeneratedHtmlCode(false);
            document.getElementById('public-view').classList.add('hidden');
            document.getElementById('admin-view').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function switchToPublicView() {
            applyStoreSettings();
            renderPublicProducts();
            renderOrderRows();
            togglePaymentDetails();
            document.getElementById('admin-view').classList.add('hidden');
            document.getElementById('public-view').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function logoutAdmin() {
            isAdminAuthenticated = false;
            switchToPublicView();
            showToast('Mode Admin dikunci.', 'info');
        }

        function switchAdminTab(tabName) {
            ['products', 'profile', 'code', 'security'].forEach(t => {
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
            if (tabName === 'code') {
                rebuildGeneratedHtmlCode(false);
            }
        }

        function saveAndApplyToPublic() {
            if (!document.getElementById('admin-tab-profile').classList.contains('hidden')) {
                storeSettings.storeName = document.getElementById('edit-store-name').value.trim() || defaultSettings.storeName;
                storeSettings.storeSubtitle = document.getElementById('edit-store-subtitle').value.trim() || defaultSettings.storeSubtitle;
                storeSettings.waNumber = document.getElementById('edit-wa-number').value.trim() || '08819665411';
                storeSettings.tagline = document.getElementById('edit-tagline').value.trim() || defaultSettings.tagline;
                storeSettings.heroTitle = document.getElementById('edit-hero-title').value.trim() || defaultSettings.heroTitle;
                storeSettings.storeBio = document.getElementById('edit-store-bio').value.trim() || defaultSettings.storeBio;
                storeSettings.bankName = document.getElementById('edit-bank-name').value.trim() || defaultSettings.bankName;
                storeSettings.bankAccount = document.getElementById('edit-bank-account').value.trim() || defaultSettings.bankAccount;
                storeSettings.bankHolder = document.getElementById('edit-bank-holder').value.trim() || defaultSettings.bankHolder;

                const logoVal = document.getElementById('edit-logo-url').value.trim();
                storeSettings.logoUrl = logoVal;
                persistentPhotos.logoDataUrl = logoVal.startsWith('data:image/') ? logoVal : '';
            }

            syncAllData(true);
            switchToPublicView();
            showToast('Perubahan disimpan & langsung tampil di Mode Publik!', 'success');
        }

        function changeAdminPin(event) {
            event.preventDefault();
            const newPin = document.getElementById('new-admin-pin').value.trim();
            if (newPin.length < 4) {
                showToast('Password minimal 4 karakter.', 'error');
                return;
            }
            localStorage.setItem(STORAGE_PIN_KEY, newPin);
            document.getElementById('new-admin-pin').value = '';
            rebuildGeneratedHtmlCode(false);
            showToast('Password Admin berhasil diperbarui!', 'success');
        }

        // =====================================================================
        // RENDER KATALOG PUBLIK & METODE PEMBAYARAN (TRANSFER / COD)
        // =====================================================================
        function handleImageFallback(imgEl, fallbackId) {
            imgEl.classList.add('hidden');
            const fallback = document.getElementById(fallbackId);
            if (fallback) fallback.classList.remove('hidden');
        }

        function formatBankSummary() {
            const bank = (storeSettings.bankName || defaultSettings.bankName).trim();
            const acc = (storeSettings.bankAccount || defaultSettings.bankAccount).trim();
            const holder = (storeSettings.bankHolder || defaultSettings.bankHolder).trim();
            return `${bank} • ${acc} a.n. ${holder}`;
        }

        function applyStoreSettings() {
            document.getElementById('nav-store-name').textContent = storeSettings.storeName;
            document.getElementById('nav-store-subtitle').textContent = storeSettings.storeSubtitle;
            document.getElementById('footer-store-name').textContent = storeSettings.storeName;
            document.getElementById('footer-store-bio').textContent = storeSettings.storeBio;
            document.getElementById('hero-tagline').textContent = storeSettings.tagline;
            document.getElementById('hero-bio').textContent = storeSettings.storeBio;
            document.getElementById('hero-title').textContent = storeSettings.heroTitle;
            document.title = `${storeSettings.storeName} - Katalog & Pemesanan Kue Kering Idul Fitri`;
            document.getElementById('display-wa-number').textContent = formatPhoneDisplay(storeSettings.waNumber);
            document.getElementById('display-bank-info').textContent = formatBankSummary();

            const activeLogo = (persistentPhotos.logoDataUrl || storeSettings.logoUrl || '').trim();
            const navLogoImg = document.getElementById('nav-logo-img');
            const navLogoFallback = document.getElementById('nav-logo-fallback');
            const heroLogoImg = document.getElementById('hero-logo-img');
            const heroLogoFallback = document.getElementById('hero-logo-fallback');

            if (activeLogo) {
                navLogoImg.src = activeLogo;
                navLogoImg.classList.remove('hidden');
                navLogoFallback.classList.add('hidden');

                heroLogoImg.src = activeLogo;
                heroLogoImg.classList.remove('hidden');
                heroLogoFallback.classList.add('hidden');
            } else {
                navLogoImg.classList.add('hidden');
                navLogoFallback.classList.remove('hidden');
                heroLogoImg.classList.add('hidden');
                heroLogoFallback.classList.remove('hidden');
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
                const variants = getProductVariants(item);
                const activeVar = getSelectedVariant(item);
                const fallbackImg = `https://placehold.co/600x450/064e3b/fbbf24?text=${encodeURIComponent(item.name)}`;
                const imgUrl = (item.image || '').trim() || fallbackImg;

                const variantButtonsHtml = variants.length > 1
                    ? `<div class="flex flex-wrap gap-1.5 mt-3">
                        ${variants.map(v => {
                            const isSelected = v.label === activeVar.label;
                            return `<button type="button" onclick="selectCardVariant('${item.id}', '${v.label.replace(/'/g, "\\'")}')" class="px-2.5 py-1 rounded-lg text-xs font-semibold border transition ${isSelected ? 'bg-emeraldRaya-900 text-goldRaya-300 border-emeraldRaya-900' : 'bg-stone-50 text-stone-600 border-stone-200 hover:border-emeraldRaya-600'}">${v.label} (${formatRupiah(v.price)})</button>`;
                        }).join('')}
                       </div>`
                    : `<span class="inline-block text-xs font-medium text-stone-400 mt-1"><i class="fa-solid fa-jar mr-1 text-goldRaya-600"></i> ${activeVar.label}</span>`;

                const card = document.createElement('div');
                card.className = 'group bg-white rounded-3xl overflow-hidden shadow-md hover:shadow-xl border border-stone-100 transition-all duration-300 flex flex-col justify-between';

                card.innerHTML = `
                    <div>
                        <div class="relative h-56 sm:h-60 overflow-hidden bg-emeraldRaya-50">
                            <img src="${imgUrl}" alt="${item.name}" onerror="this.onerror=null;this.src='${fallbackImg}';" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
                            <div class="absolute top-3 left-3 flex flex-wrap gap-1.5">
                                <span class="px-3 py-1 rounded-full bg-emeraldRaya-950/85 backdrop-blur-sm text-white text-[11px] font-semibold">
                                    ${item.category}
                                </span>
                                ${item.badge ? `<span class="px-3 py-1 rounded-full bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 text-emeraldRaya-950 text-[11px] font-bold shadow-sm">${item.badge}</span>` : ''}
                            </div>
                        </div>

                        <div class="p-5 sm:p-6">
                            <h3 class="font-serif font-bold text-lg sm:text-xl text-emeraldRaya-950 leading-snug">${item.name}</h3>
                            ${variantButtonsHtml}
                            <p class="text-xs sm:text-sm text-stone-600 mt-3 leading-relaxed">
                                ${item.desc}
                            </p>
                        </div>
                    </div>

                    <div class="px-5 sm:px-6 pb-5 sm:pb-6 pt-3 border-t border-stone-100 flex items-center justify-between gap-3">
                        <div>
                            <span class="text-[11px] text-stone-400 block">${activeVar.label}</span>
                            <span class="text-lg sm:text-xl font-bold text-emeraldRaya-800">${formatRupiah(activeVar.price)}</span>
                        </div>
                        <button type="button" onclick="addProductToOrderForm('${item.id}', '${activeVar.label.replace(/'/g, "\\'")}')" class="px-4 py-2.5 rounded-xl bg-emeraldRaya-50 hover:bg-emeraldRaya-800 text-emeraldRaya-800 hover:text-white font-semibold text-xs sm:text-sm border border-emeraldRaya-200 hover:border-emeraldRaya-800 transition flex items-center gap-1.5">
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

        // =====================================================================
        // FORM PEMESANAN MULTI-ITEM & PEMBAYARAN TRANSFER / COD KE WHATSAPP
        // =====================================================================
        function togglePaymentDetails() {
            const paymentSelect = document.getElementById('order-payment');
            const transferBox = document.getElementById('transfer-detail-box');
            const codBox = document.getElementById('cod-detail-box');
            if (!paymentSelect || !transferBox || !codBox) return;

            if (paymentSelect.value === 'Transfer Bank') {
                transferBox.classList.remove('hidden');
                codBox.classList.add('hidden');
            } else {
                transferBox.classList.add('hidden');
                codBox.classList.remove('hidden');
            }
        }

        function copyBankAccount() {
            const accNum = (storeSettings.bankAccount || defaultSettings.bankAccount).trim();
            copyTextToClipboard(accNum, `Nomor rekening ${accNum} berhasil disalin!`);
        }

        function renderOrderRows() {
            const container = document.getElementById('order-items-container');
            container.innerHTML = '';

            if (orderRows.length === 0 && products.length > 0) {
                const v = getProductVariants(products[0])[0];
                orderRows.push({ rowId: Date.now(), productId: products[0].id, variantLabel: v ? v.label : products[0].weight, qty: 1 });
            }

            orderRows.forEach((row, index) => {
                const product = products.find(p => p.id === row.productId) || products[0];
                if (!product) return;
                row.productId = product.id;

                const variants = getProductVariants(product);
                const selectedVar = getSelectedVariant(product, row.variantLabel);
                row.variantLabel = selectedVar.label;

                const productOptions = products.map(p => `
                    <option value="${p.id}" ${p.id === product.id ? 'selected' : ''}>${p.name}</option>
                `).join('');

                const variantOptions = variants.map(v => `
                    <option value="${v.label}" ${v.label === selectedVar.label ? 'selected' : ''}>${v.label} - ${formatRupiah(v.price)}</option>
                `).join('');

                const rowEl = document.createElement('div');
                rowEl.className = 'p-3.5 rounded-2xl bg-stone-50 border border-stone-200 space-y-2.5';
                rowEl.innerHTML = `
                    <div class="flex items-center justify-between">
                        <span class="text-[11px] font-bold text-stone-400 uppercase">Pilihan Kue #${index + 1}</span>
                        ${orderRows.length > 1 ? `<button type="button" onclick="removeOrderRow(${row.rowId})" class="text-xs font-semibold text-red-600 hover:text-red-700 flex items-center gap-1"><i class="fa-solid fa-trash-can"></i> Hapus</button>` : ''}
                    </div>
                    <div class="grid grid-cols-1 sm:grid-cols-12 gap-2.5">
                        <div class="sm:col-span-6">
                            <select onchange="updateOrderRowProduct(${row.rowId}, this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-medium focus:outline-none focus:border-emeraldRaya-600">
                                ${productOptions}
                            </select>
                        </div>
                        <div class="sm:col-span-4">
                            <select onchange="updateOrderRowVariant(${row.rowId}, this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-medium focus:outline-none focus:border-emeraldRaya-600">
                                ${variantOptions}
                            </select>
                        </div>
                        <div class="sm:col-span-2">
                            <input type="number" min="1" value="${row.qty}" oninput="updateOrderRowQty(${row.rowId}, this.value)" onchange="updateOrderRowQty(${row.rowId}, this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-bold text-center focus:outline-none focus:border-emeraldRaya-600" aria-label="Jumlah">
                        </div>
                    </div>
                `;
                container.appendChild(rowEl);
            });

            calculateGrandTotal();
        }

        function addOrderItemRow(selectedProductId = null, selectedVariantLabel = null) {
            const prod = products.find(p => p.id === selectedProductId) || products[0];
            if (!prod) return;
            const variant = getSelectedVariant(prod, selectedVariantLabel);
            orderRows.push({
                rowId: Date.now() + Math.random(),
                productId: prod.id,
                variantLabel: variant.label,
                qty: 1
            });
            renderOrderRows();
        }

        function addProductToOrderForm(productId, variantLabel = null) {
            const prod = products.find(p => p.id === productId);
            if (!prod) return;
            const variant = getSelectedVariant(prod, variantLabel);
            const existingRow = orderRows.find(r => r.productId === prod.id && r.variantLabel === variant.label);

            if (existingRow) {
                existingRow.qty += 1;
                renderOrderRows();
                showToast(`Jumlah ${prod.name} (${variant.label}) ditambah (+1)!`, 'success');
            } else {
                addOrderItemRow(prod.id, variant.label);
                showToast(`${prod.name} (${variant.label}) ditambahkan ke pesanan!`, 'success');
            }
            document.getElementById('form-pemesanan').scrollIntoView({ behavior: 'smooth' });
        }

        function updateOrderRowProduct(rowId, newProductId) {
            const row = orderRows.find(r => r.rowId === rowId);
            const prod = products.find(p => p.id === newProductId);
            if (row && prod) {
                row.productId = prod.id;
                const firstVar = getProductVariants(prod)[0];
                row.variantLabel = firstVar ? firstVar.label : prod.weight;
                renderOrderRows();
            }
        }

        function updateOrderRowVariant(rowId, newVariantLabel) {
            const row = orderRows.find(r => r.rowId === rowId);
            if (row) {
                row.variantLabel = newVariantLabel;
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
            let totalQty = 0;

            orderRows.forEach(row => {
                const product = products.find(p => p.id === row.productId);
                if (product) {
                    const variant = getSelectedVariant(product, row.variantLabel);
                    grandTotal += variant.price * row.qty;
                    totalQty += row.qty;
                }
            });

            document.getElementById('order-total-price').textContent = formatRupiah(grandTotal);
            document.getElementById('order-total-items-count').textContent = `${orderRows.length} jenis kue (Total ${totalQty} toples/paket)`;

            const badge = document.getElementById('nav-cart-badge');
            if (totalQty > 0) {
                badge.textContent = totalQty;
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
            const paymentMethod = document.getElementById('order-payment').value;
            const address = document.getElementById('order-address').value.trim() || '-';

            let itemsTextList = '';
            let grandTotal = 0;
            let validCount = 0;

            orderRows.forEach((row, idx) => {
                const product = products.find(p => p.id === row.productId);
                if (product) {
                    validCount++;
                    const variant = getSelectedVariant(product, row.variantLabel);
                    const subtotal = variant.price * row.qty;
                    grandTotal += subtotal;
                    itemsTextList += `${idx + 1}. *${product.name}* (${variant.label})\n   Jumlah: ${row.qty} x ${formatRupiah(variant.price)} = *${formatRupiah(subtotal)}*\n`;
                }
            });

            if (validCount === 0) {
                showToast('Silakan pilih minimal 1 jenis kue.', 'error');
                return;
            }

            const paymentDetailLine = paymentMethod === 'Transfer Bank'
                ? `\n• Rekening Tujuan: ${formatBankSummary()}`
                : '\n• Keterangan Bayar: Tunai saat pesanan diterima (COD)';

            const targetWa = getFormattedTargetWa();
            const message =
`Assalamu'alaikum *${storeSettings.storeName}* 🌙✨
Saya ingin memesan kue kering Idul Fitri:

*Data Pemesan:*
• Nama: ${buyerName}
• Metode Pembayaran: *${paymentMethod}*${paymentDetailLine}

*Rincian Pesanan Kue:*
${itemsTextList}
*Total Estimasi Harga: ${formatRupiah(grandTotal)}*

*Alamat / Catatan:*
${address}

Mohon konfirmasi ketersediaan & proses pesanannya ya. Terima kasih! 🙏`;

            const waUrl = `https://wa.me/${targetWa}?text=${encodeURIComponent(message)}`;
            showToast('Mengarahkan ke WhatsApp penjual...', 'success');
            window.location.href = waUrl;
        }

        function chatDirectWhatsApp() {
            const targetWa = getFormattedTargetWa();
            const text = encodeURIComponent(`Assalamu'alaikum ${storeSettings.storeName}, saya ingin bertanya mengenai pesanan kue kering Lebaran.`);
            window.open(`https://wa.me/${targetWa}?text=${text}`, '_blank', 'noopener,noreferrer');
        }

        function copyWaNumber() {
            const rawWa = storeSettings.waNumber || '08819665411';
            copyTextToClipboard(rawWa, 'Nomor WhatsApp berhasil disalin!');
        }

        // =====================================================================
        // KELOLA PROFIL, LOGO PERMANEN & PRODUK DI MODE ADMIN
        // =====================================================================
        function populateProfileForm() {
            document.getElementById('edit-store-name').value = storeSettings.storeName;
            document.getElementById('edit-store-subtitle').value = storeSettings.storeSubtitle;
            document.getElementById('edit-wa-number').value = storeSettings.waNumber;
            document.getElementById('edit-tagline').value = storeSettings.tagline;
            document.getElementById('edit-hero-title').value = storeSettings.heroTitle;
            document.getElementById('edit-store-bio').value = storeSettings.storeBio;
            document.getElementById('edit-bank-name').value = storeSettings.bankName || defaultSettings.bankName;
            document.getElementById('edit-bank-account').value = storeSettings.bankAccount || defaultSettings.bankAccount;
            document.getElementById('edit-bank-holder').value = storeSettings.bankHolder || defaultSettings.bankHolder;

            const activeLogo = persistentPhotos.logoDataUrl || storeSettings.logoUrl || '';
            document.getElementById('edit-logo-url').value = activeLogo;
            updateLogoPreview(activeLogo);
        }

        function refreshLogoBadge() {
            const badge = document.getElementById('logo-persistent-badge');
            if (!badge) return;
            if (persistentPhotos.logoDataUrl) {
                badge.textContent = 'Logo Tersimpan Permanen (Bisa Diganti)';
                badge.className = 'text-[11px] font-semibold px-2.5 py-1 rounded-full bg-emerald-100 text-emerald-800';
            } else if ((storeSettings.logoUrl || '').trim()) {
                badge.textContent = 'Menggunakan URL / File Logo';
                badge.className = 'text-[11px] font-semibold px-2.5 py-1 rounded-full bg-amber-100 text-amber-800';
            } else {
                badge.textContent = 'Ikon Bawaan';
                badge.className = 'text-[11px] font-semibold px-2.5 py-1 rounded-full bg-stone-200 text-stone-600';
            }
        }

        function updateLogoPreview(val) {
            const trimmed = (val || '').trim();
            const img = document.getElementById('preview-logo-img');
            const icon = document.getElementById('preview-logo-icon');
            if (trimmed) {
                img.src = trimmed;
                img.classList.remove('hidden');
                icon.classList.add('hidden');
            } else {
                img.classList.add('hidden');
                icon.classList.remove('hidden');
            }
            refreshLogoBadge();
        }

        function handleLogoUpload(event) {
            const file = event.target.files && event.target.files[0];
            if (!file) return;
            compressImageFile(file, 360, 0.82, dataUrl => {
                persistentPhotos.logoDataUrl = dataUrl;
                storeSettings.logoUrl = dataUrl;
                document.getElementById('edit-logo-url').value = dataUrl;
                savePersistentPhotos();
                updateLogoPreview(dataUrl);
                applyStoreSettings();
                rebuildGeneratedHtmlCode(false);
                showToast('Logo toko tersimpan permanen & tetap bisa diganti!', 'success');
            });
            event.target.value = '';
        }

        function clearLogoPhoto() {
            persistentPhotos.logoDataUrl = '';
            storeSettings.logoUrl = '';
            document.getElementById('edit-logo-url').value = '';
            savePersistentPhotos();
            updateLogoPreview('');
            applyStoreSettings();
            rebuildGeneratedHtmlCode(false);
            showToast('Logo toko dihapus.', 'info');
        }

        function saveFullStoreProfile(event) {
            event.preventDefault();
            storeSettings.storeName = document.getElementById('edit-store-name').value.trim() || defaultSettings.storeName;
            storeSettings.storeSubtitle = document.getElementById('edit-store-subtitle').value.trim() || defaultSettings.storeSubtitle;
            storeSettings.waNumber = document.getElementById('edit-wa-number').value.trim() || '08819665411';
            storeSettings.tagline = document.getElementById('edit-tagline').value.trim() || defaultSettings.tagline;
            storeSettings.heroTitle = document.getElementById('edit-hero-title').value.trim() || defaultSettings.heroTitle;
            storeSettings.storeBio = document.getElementById('edit-store-bio').value.trim() || defaultSettings.storeBio;
            storeSettings.bankName = document.getElementById('edit-bank-name').value.trim() || defaultSettings.bankName;
            storeSettings.bankAccount = document.getElementById('edit-bank-account').value.trim() || defaultSettings.bankAccount;
            storeSettings.bankHolder = document.getElementById('edit-bank-holder').value.trim() || defaultSettings.bankHolder;

            const enteredLogo = document.getElementById('edit-logo-url').value.trim();
            storeSettings.logoUrl = enteredLogo;
            persistentPhotos.logoDataUrl = enteredLogo.startsWith('data:image/') ? enteredLogo : '';

            syncAllData(true);
            switchToPublicView();
            showToast('Perubahan profil, logo & rekening disimpan ke Mode Publik!', 'success');
        }

        function renderAdminProducts() {
            const list = document.getElementById('admin-product-list');
            list.innerHTML = '';

            products.forEach(item => {
                const fallbackImg = `https://placehold.co/600x400/064e3b/fbbf24?text=${encodeURIComponent(item.name)}`;
                const imgUrl = (item.image || '').trim() || fallbackImg;
                const isPermanentPhoto = Boolean(persistentPhotos.productsById[item.id]);
                const price500Text = Number(item.price500) > 0 ? ` • 500gr: ${formatRupiah(item.price500)}` : '';

                const card = document.createElement('div');
                card.className = 'bg-white rounded-3xl overflow-hidden shadow-sm border border-stone-200 flex flex-col justify-between';
                card.innerHTML = `
                    <div>
                        <div class="relative h-44 bg-stone-100">
                            <img src="${imgUrl}" alt="${item.name}" onerror="this.onerror=null;this.src='${fallbackImg}';" class="w-full h-full object-cover">
                            <span class="absolute top-3 left-3 px-2.5 py-1 rounded-full bg-emeraldRaya-950/85 text-white text-[11px] font-semibold">${item.category}</span>
                            ${isPermanentPhoto ? `<span class="absolute top-3 right-3 px-2.5 py-1 rounded-full bg-goldRaya-400 text-emeraldRaya-950 text-[10px] font-bold">Foto Permanen</span>` : ''}
                        </div>
                        <div class="p-5">
                            <h3 class="font-bold text-base text-stone-800 mb-1">${item.name}</h3>
                            <p class="text-xs text-stone-500 mb-2">${item.weight}: <strong class="text-emeraldRaya-800">${formatRupiah(item.price)}</strong>${price500Text}</p>
                            <p class="text-xs text-stone-600 line-clamp-2">${item.desc}</p>
                        </div>
                    </div>
                    <div class="px-5 pb-5 pt-3 border-t border-stone-100 flex gap-2">
                        <button type="button" onclick="openProductModal('${item.id}')" class="flex-1 py-2 rounded-xl bg-amber-100 hover:bg-amber-500 text-amber-800 hover:text-white font-semibold text-xs transition flex items-center justify-center gap-1.5">
                            <i class="fa-solid fa-pen"></i> Edit & Ganti Foto
                        </button>
                        <button type="button" onclick="confirmDeleteProduct('${item.id}')" class="px-3.5 py-2 rounded-xl bg-red-100 hover:bg-red-600 text-red-600 hover:text-white font-semibold text-xs transition" title="Hapus">
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
                    title.textContent = 'Edit Kue & Foto Permanen';
                    document.getElementById('edit-product-id').value = product.id;
                    document.getElementById('prod-name').value = product.name;
                    document.getElementById('prod-price').value = product.price;
                    document.getElementById('prod-weight').value = product.weight;
                    document.getElementById('prod-price-500').value = product.price500 || '';
                    document.getElementById('prod-badge').value = product.badge || '';
                    document.getElementById('prod-category').value = product.category;
                    document.getElementById('prod-image').value = product.image || '';
                    document.getElementById('prod-desc').value = product.desc;
                    updateProductModalPreview(product.image || '', Boolean(persistentPhotos.productsById[product.id]));
                }
            } else {
                title.textContent = 'Post Kue Kering Baru';
                document.getElementById('prod-price-500').value = '85000';
                updateProductModalPreview('', false);
            }

            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closeProductModal() {
            const modal = document.getElementById('product-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
        }

        function updateProductModalPreview(val, isSavedPermanent = false) {
            const trimmed = (val || '').trim();
            const img = document.getElementById('preview-prod-img');
            const statusEl = document.getElementById('prod-photo-status');

            if (trimmed) {
                img.src = trimmed;
                img.classList.remove('hidden');
            } else {
                img.classList.add('hidden');
            }

            if (isSavedPermanent || trimmed.startsWith('data:image/')) {
                statusEl.textContent = 'Permanen (Bisa Diganti)';
                statusEl.className = 'text-[11px] font-semibold px-2 py-0.5 rounded-full bg-emerald-100 text-emerald-800';
            } else if (trimmed) {
                statusEl.textContent = 'File / URL';
                statusEl.className = 'text-[11px] font-semibold px-2 py-0.5 rounded-full bg-amber-100 text-amber-800';
            } else {
                statusEl.textContent = 'Kosong';
                statusEl.className = 'text-[11px] font-semibold px-2 py-0.5 rounded-full bg-stone-200 text-stone-600';
            }
        }

        function handleProductPhotoUpload(event) {
            const file = event.target.files && event.target.files[0];
            if (!file) return;
            const currentId = document.getElementById('edit-product-id').value || ('kue-' + Date.now());
            document.getElementById('edit-product-id').value = currentId;

            compressImageFile(file, 720, 0.82, dataUrl => {
                persistentPhotos.productsById[currentId] = dataUrl;
                document.getElementById('prod-image').value = dataUrl;
                savePersistentPhotos();
                updateProductModalPreview(dataUrl, true);
                showToast('Foto kue tersimpan permanen & tetap bisa diganti!', 'success');
            });
            event.target.value = '';
        }

        function clearProductPhoto() {
            const currentId = document.getElementById('edit-product-id').value;
            if (currentId && Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, currentId)) {
                delete persistentPhotos.productsById[currentId];
                savePersistentPhotos();
            }
            document.getElementById('prod-image').value = '';
            updateProductModalPreview('', false);
            showToast('Foto kue dikosongkan.', 'info');
        }

        function saveProduct(event) {
            event.preventDefault();
            const editId = document.getElementById('edit-product-id').value || ('kue-' + Date.now());
            const imgInputVal = document.getElementById('prod-image').value.trim();

            if (imgInputVal.startsWith('data:image/')) {
                persistentPhotos.productsById[editId] = imgInputVal;
            } else if (Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, editId)) {
                delete persistentPhotos.productsById[editId];
            }

            const newProductData = {
                id: editId,
                name: document.getElementById('prod-name').value.trim(),
                price: parseInt(document.getElementById('prod-price').value, 10) || 45000,
                weight: document.getElementById('prod-weight').value.trim() || 'Toples 250gr',
                price500: parseInt(document.getElementById('prod-price-500').value, 10) || 0,
                category: document.getElementById('prod-category').value,
                badge: document.getElementById('prod-badge').value.trim(),
                image: imgInputVal,
                desc: document.getElementById('prod-desc').value.trim()
            };

            const existingIndex = products.findIndex(p => p.id === editId);
            if (existingIndex !== -1) {
                products[existingIndex] = newProductData;
                showToast('Data kue & foto diperbarui!', 'success');
            } else {
                products.unshift(newProductData);
                showToast('Kue baru berhasil diposting!', 'success');
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
                if (Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, productToDeleteId)) {
                    delete persistentPhotos.productsById[productToDeleteId];
                }
                syncAllData(true);
                renderAdminProducts();
                closeDeleteModal();
                showToast('Produk kue telah dihapus.', 'info');
            };
        }

        function closeDeleteModal() {
            const modal = document.getElementById('delete-modal');
            modal.classList.add('hidden');
            modal.classList.remove('flex');
            productToDeleteId = null;
        }

        function resetDefaultData() {
            storeSettings = {
                ...defaultSettings,
                logoUrl: persistentPhotos.logoDataUrl || ''
            };
            products = defaultProducts.map(item => ({
                ...item,
                image: Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id)
                    ? persistentPhotos.productsById[item.id]
                    : item.image
            }));
            syncAllData(true);
            populateProfileForm();
            renderAdminProducts();
            showToast('Katalog & pengaturan dikembalikan ke default!', 'info');
        }

        // =====================================================================
        // GENERATOR KODE HTML OTOMATIS SESUAI POSTINGAN ADMIN
        // =====================================================================
        function escapeInlineScriptJson(obj) {
            return JSON.stringify(obj, null, 2).replace(/<\/script>/gi, '<\\/script>');
        }

        function rebuildGeneratedHtmlCode(notifyUser = false) {
            const textarea = document.getElementById('generated-html-output');
            if (!textarea) return;

            const currentPin = localStorage.getItem(STORAGE_PIN_KEY) || DEFAULT_ADMIN_PIN;
            const snapshotSettings = {
                ...defaultSettings,
                ...storeSettings,
                logoUrl: persistentPhotos.logoDataUrl || storeSettings.logoUrl || ''
            };
            const snapshotProducts = products.map(item => ({
                ...item,
                image: Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id)
                    ? persistentPhotos.productsById[item.id]
                    : (item.image || '')
            }));

            const docClone = document.documentElement.cloneNode(true);
            const scripts = docClone.querySelectorAll('script');
            const mainScript = scripts[scripts.length - 1];

            if (mainScript) {
                const updatedScriptBody = `
        const DEFAULT_ADMIN_PIN = ${JSON.stringify(currentPin)};

        const defaultSettings = ${escapeInlineScriptJson(snapshotSettings)};

        const defaultProducts = ${escapeInlineScriptJson(snapshotProducts)};

        const STORAGE_SETTINGS_KEY = 'dfsultan_settings_v13';
        const STORAGE_PRODUCTS_KEY = 'dfsultan_products_v13';
        const STORAGE_PIN_KEY = 'dfsultan_admin_pin_v13';
        const STORAGE_PERSISTENT_PHOTOS_KEY = 'dfsultan_persistent_photos_v13';

        let storeSettings = {};
        let products = [];
        let persistentPhotos = { logoDataUrl: '', productsById: {} };
        let cardSelectedVariant = {};
        let orderRows = [];
        let currentCategory = 'Semua';
        let isAdminAuthenticated = false;

        document.addEventListener('DOMContentLoaded', () => {
            loadStoreData();
            applyStoreSettings();
            renderPublicProducts();

            const firstProd = products[0];
            const firstVar = firstProd ? getProductVariants(firstProd)[0] : null;
            orderRows = firstProd
                ? [{ rowId: Date.now(), productId: firstProd.id, variantLabel: firstVar ? firstVar.label : firstProd.weight, qty: 1 }]
                : [{ rowId: Date.now(), productId: '', variantLabel: '', qty: 1 }];

            renderOrderRows();
            togglePaymentDetails();
            rebuildGeneratedHtmlCode(false);
        });

        function loadStoreData() {
            try {
                const savedPhotos = localStorage.getItem(STORAGE_PERSISTENT_PHOTOS_KEY);
                if (savedPhotos) {
                    const parsedPhotos = JSON.parse(savedPhotos);
                    persistentPhotos = {
                        logoDataUrl: parsedPhotos.logoDataUrl || '',
                        productsById: parsedPhotos.productsById || {}
                    };
                }
                const savedSettings = localStorage.getItem(STORAGE_SETTINGS_KEY);
                storeSettings = savedSettings ? { ...defaultSettings, ...JSON.parse(savedSettings) } : { ...defaultSettings };
                if (persistentPhotos.logoDataUrl) storeSettings.logoUrl = persistentPhotos.logoDataUrl;

                const savedProducts = localStorage.getItem(STORAGE_PRODUCTS_KEY);
                const rawProducts = savedProducts ? JSON.parse(savedProducts) : [...defaultProducts];
                products = rawProducts.map(item => ({
                    ...item,
                    price500: typeof item.price500 === 'number' ? item.price500 : (item.category === 'Paket Hampers' ? 0 : 85000),
                    image: Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id) ? persistentPhotos.productsById[item.id] : (item.image || '')
                }));
            } catch (err) {
                storeSettings = { ...defaultSettings };
                products = [...defaultProducts];
            }
        }

        function savePersistentPhotos() {
            try {
                localStorage.setItem(STORAGE_PERSISTENT_PHOTOS_KEY, JSON.stringify(persistentPhotos));
            } catch (err) {
                showToast('Ukuran foto melebihi kapasitas browser.', 'error');
            }
        }

        function syncAllData(updateHtmlExport = true) {
            if (persistentPhotos.logoDataUrl) storeSettings.logoUrl = persistentPhotos.logoDataUrl;
            products = products.map(item => Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id)
                ? { ...item, image: persistentPhotos.productsById[item.id] }
                : item);

            localStorage.setItem(STORAGE_SETTINGS_KEY, JSON.stringify(storeSettings));
            localStorage.setItem(STORAGE_PRODUCTS_KEY, JSON.stringify(products));
            savePersistentPhotos();
            applyStoreSettings();
            renderPublicProducts();
            renderOrderRows();
            togglePaymentDetails();
            if (updateHtmlExport) rebuildGeneratedHtmlCode(false);
        }

        function getProductVariants(product) {
            const variants = [{ label: product.weight || 'Toples 250gr', price: Number(product.price) || 0 }];
            if (Number(product.price500) > 0) variants.push({ label: 'Toples 500gr', price: Number(product.price500) });
            return variants;
        }

        function getSelectedVariant(product, preferredLabel = null) {
            const variants = getProductVariants(product);
            const targetLabel = preferredLabel || cardSelectedVariant[product.id];
            return variants.find(v => v.label === targetLabel) || variants[0];
        }

        function selectCardVariant(productId, variantLabel) {
            cardSelectedVariant[productId] = variantLabel;
            renderPublicProducts();
        }

        function openAdminModal() {
            if (isAdminAuthenticated) { switchToAdminView(); return; }
            document.getElementById('pin-login-input').value = '';
            const modal = document.getElementById('admin-pin-modal');
            modal.classList.remove('hidden'); modal.classList.add('flex');
            setTimeout(() => document.getElementById('pin-login-input').focus(), 100);
        }

        function closeAdminModal() {
            const modal = document.getElementById('admin-pin-modal');
            modal.classList.add('hidden'); modal.classList.remove('flex');
        }

        function verifyAdminPin(event) {
            event.preventDefault();
            const enteredPin = document.getElementById('pin-login-input').value.trim();
            const savedPin = localStorage.getItem(STORAGE_PIN_KEY) || DEFAULT_ADMIN_PIN;
            if (enteredPin === savedPin) {
                isAdminAuthenticated = true;
                closeAdminModal();
                switchToAdminView();
                showToast('Selamat datang di Mode Admin DF Sultan!', 'success');
            } else {
                showToast('Password admin salah.', 'error');
            }
        }

        function switchToAdminView() {
            populateProfileForm();
            renderAdminProducts();
            rebuildGeneratedHtmlCode(false);
            document.getElementById('public-view').classList.add('hidden');
            document.getElementById('admin-view').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function switchToPublicView() {
            applyStoreSettings(); renderPublicProducts(); renderOrderRows(); togglePaymentDetails();
            document.getElementById('admin-view').classList.add('hidden');
            document.getElementById('public-view').classList.remove('hidden');
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function logoutAdmin() {
            isAdminAuthenticated = false;
            switchToPublicView();
            showToast('Mode Admin dikunci.', 'info');
        }

        function switchAdminTab(tabName) {
            ['products', 'profile', 'code', 'security'].forEach(t => {
                const panel = document.getElementById('admin-tab-' + t);
                const btn = document.getElementById('tab-btn-' + t);
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
            if (tabName === 'code') rebuildGeneratedHtmlCode(false);
        }

        function saveAndApplyToPublic() {
            if (!document.getElementById('admin-tab-profile').classList.contains('hidden')) {
                storeSettings.storeName = document.getElementById('edit-store-name').value.trim() || defaultSettings.storeName;
                storeSettings.storeSubtitle = document.getElementById('edit-store-subtitle').value.trim() || defaultSettings.storeSubtitle;
                storeSettings.waNumber = document.getElementById('edit-wa-number').value.trim() || '08819665411';
                storeSettings.tagline = document.getElementById('edit-tagline').value.trim() || defaultSettings.tagline;
                storeSettings.heroTitle = document.getElementById('edit-hero-title').value.trim() || defaultSettings.heroTitle;
                storeSettings.storeBio = document.getElementById('edit-store-bio').value.trim() || defaultSettings.storeBio;
                storeSettings.bankName = document.getElementById('edit-bank-name').value.trim() || defaultSettings.bankName;
                storeSettings.bankAccount = document.getElementById('edit-bank-account').value.trim() || defaultSettings.bankAccount;
                storeSettings.bankHolder = document.getElementById('edit-bank-holder').value.trim() || defaultSettings.bankHolder;
                const logoVal = document.getElementById('edit-logo-url').value.trim();
                storeSettings.logoUrl = logoVal;
                persistentPhotos.logoDataUrl = logoVal.startsWith('data:image/') ? logoVal : '';
            }
            syncAllData(true);
            switchToPublicView();
            showToast('Perubahan disimpan & langsung tampil di Mode Publik!', 'success');
        }

        function changeAdminPin(event) {
            event.preventDefault();
            const newPin = document.getElementById('new-admin-pin').value.trim();
            if (newPin.length < 4) { showToast('Password minimal 4 karakter.', 'error'); return; }
            localStorage.setItem(STORAGE_PIN_KEY, newPin);
            document.getElementById('new-admin-pin').value = '';
            rebuildGeneratedHtmlCode(false);
            showToast('Password Admin berhasil diperbarui!', 'success');
        }

        function handleImageFallback(imgEl, fallbackId) {
            imgEl.classList.add('hidden');
            const fallback = document.getElementById(fallbackId);
            if (fallback) fallback.classList.remove('hidden');
        }

        function formatBankSummary() {
            const bank = (storeSettings.bankName || defaultSettings.bankName).trim();
            const acc = (storeSettings.bankAccount || defaultSettings.bankAccount).trim();
            const holder = (storeSettings.bankHolder || defaultSettings.bankHolder).trim();
            return bank + ' • ' + acc + ' a.n. ' + holder;
        }

        function applyStoreSettings() {
            document.getElementById('nav-store-name').textContent = storeSettings.storeName;
            document.getElementById('nav-store-subtitle').textContent = storeSettings.storeSubtitle;
            document.getElementById('footer-store-name').textContent = storeSettings.storeName;
            document.getElementById('footer-store-bio').textContent = storeSettings.storeBio;
            document.getElementById('hero-tagline').textContent = storeSettings.tagline;
            document.getElementById('hero-bio').textContent = storeSettings.storeBio;
            document.getElementById('hero-title').textContent = storeSettings.heroTitle;
            document.title = storeSettings.storeName + ' - Katalog & Pemesanan Kue Kering Idul Fitri';
            document.getElementById('display-wa-number').textContent = formatPhoneDisplay(storeSettings.waNumber);
            document.getElementById('display-bank-info').textContent = formatBankSummary();

            const activeLogo = (persistentPhotos.logoDataUrl || storeSettings.logoUrl || '').trim();
            const navLogoImg = document.getElementById('nav-logo-img');
            const navLogoFallback = document.getElementById('nav-logo-fallback');
            const heroLogoImg = document.getElementById('hero-logo-img');
            const heroLogoFallback = document.getElementById('hero-logo-fallback');

            if (activeLogo) {
                navLogoImg.src = activeLogo; navLogoImg.classList.remove('hidden'); navLogoFallback.classList.add('hidden');
                heroLogoImg.src = activeLogo; heroLogoImg.classList.remove('hidden'); heroLogoFallback.classList.add('hidden');
            } else {
                navLogoImg.classList.add('hidden'); navLogoFallback.classList.remove('hidden');
                heroLogoImg.classList.add('hidden'); heroLogoFallback.classList.remove('hidden');
            }
        }

        function renderPublicProducts() {
            const grid = document.getElementById('product-grid');
            const emptyState = document.getElementById('empty-state');
            grid.innerHTML = '';
            const filtered = currentCategory === 'Semua' ? products : products.filter(p => p.category === currentCategory);
            if (filtered.length === 0) { grid.classList.add('hidden'); emptyState.classList.remove('hidden'); return; }
            grid.classList.remove('hidden'); emptyState.classList.add('hidden');

            filtered.forEach(item => {
                const variants = getProductVariants(item);
                const activeVar = getSelectedVariant(item);
                const fallbackImg = 'https://placehold.co/600x450/064e3b/fbbf24?text=' + encodeURIComponent(item.name);
                const imgUrl = (item.image || '').trim() || fallbackImg;
                const variantButtonsHtml = variants.length > 1
                    ? '<div class="flex flex-wrap gap-1.5 mt-3">' + variants.map(v => {
                        const isSelected = v.label === activeVar.label;
                        return '<button type="button" onclick="selectCardVariant(\\'' + item.id + '\\', \\'' + v.label.replace(/'/g, "\\\\'") + '\\')" class="px-2.5 py-1 rounded-lg text-xs font-semibold border transition ' + (isSelected ? 'bg-emeraldRaya-900 text-goldRaya-300 border-emeraldRaya-900' : 'bg-stone-50 text-stone-600 border-stone-200 hover:border-emeraldRaya-600') + '">' + v.label + ' (' + formatRupiah(v.price) + ')</button>';
                    }).join('') + '</div>'
                    : '<span class="inline-block text-xs font-medium text-stone-400 mt-1"><i class="fa-solid fa-jar mr-1 text-goldRaya-600"></i> ' + activeVar.label + '</span>';

                const card = document.createElement('div');
                card.className = 'group bg-white rounded-3xl overflow-hidden shadow-md hover:shadow-xl border border-stone-100 transition-all duration-300 flex flex-col justify-between';
                card.innerHTML = '<div><div class="relative h-56 sm:h-60 overflow-hidden bg-emeraldRaya-50"><img src="' + imgUrl + '" alt="' + item.name + '" onerror="this.onerror=null;this.src=\\'' + fallbackImg + '\\';" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"><div class="absolute top-3 left-3 flex flex-wrap gap-1.5"><span class="px-3 py-1 rounded-full bg-emeraldRaya-950/85 backdrop-blur-sm text-white text-[11px] font-semibold">' + item.category + '</span>' + (item.badge ? '<span class="px-3 py-1 rounded-full bg-gradient-to-r from-goldRaya-400 to-goldRaya-500 text-emeraldRaya-950 text-[11px] font-bold shadow-sm">' + item.badge + '</span>' : '') + '</div></div><div class="p-5 sm:p-6"><h3 class="font-serif font-bold text-lg sm:text-xl text-emeraldRaya-950 leading-snug">' + item.name + '</h3>' + variantButtonsHtml + '<p class="text-xs sm:text-sm text-stone-600 mt-3 leading-relaxed">' + item.desc + '</p></div></div><div class="px-5 sm:px-6 pb-5 sm:pb-6 pt-3 border-t border-stone-100 flex items-center justify-between gap-3"><div><span class="text-[11px] text-stone-400 block">' + activeVar.label + '</span><span class="text-lg sm:text-xl font-bold text-emeraldRaya-800">' + formatRupiah(activeVar.price) + '</span></div><button type="button" onclick="addProductToOrderForm(\\'' + item.id + '\\', \\'' + activeVar.label.replace(/'/g, "\\\\'") + '\\')" class="px-4 py-2.5 rounded-xl bg-emeraldRaya-50 hover:bg-emeraldRaya-800 text-emeraldRaya-800 hover:text-white font-semibold text-xs sm:text-sm border border-emeraldRaya-200 hover:border-emeraldRaya-800 transition flex items-center gap-1.5"><i class="fa-solid fa-plus"></i> Pilih Kue</button></div>';
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

        function togglePaymentDetails() {
            const paymentSelect = document.getElementById('order-payment');
            const transferBox = document.getElementById('transfer-detail-box');
            const codBox = document.getElementById('cod-detail-box');
            if (!paymentSelect || !transferBox || !codBox) return;
            if (paymentSelect.value === 'Transfer Bank') { transferBox.classList.remove('hidden'); codBox.classList.add('hidden'); }
            else { transferBox.classList.add('hidden'); codBox.classList.remove('hidden'); }
        }

        function copyBankAccount() {
            const accNum = (storeSettings.bankAccount || defaultSettings.bankAccount).trim();
            copyTextToClipboard(accNum, 'Nomor rekening ' + accNum + ' berhasil disalin!');
        }

        function renderOrderRows() {
            const container = document.getElementById('order-items-container');
            container.innerHTML = '';
            if (orderRows.length === 0 && products.length > 0) {
                const v = getProductVariants(products[0])[0];
                orderRows.push({ rowId: Date.now(), productId: products[0].id, variantLabel: v ? v.label : products[0].weight, qty: 1 });
            }
            orderRows.forEach((row, index) => {
                const product = products.find(p => p.id === row.productId) || products[0];
                if (!product) return;
                row.productId = product.id;
                const variants = getProductVariants(product);
                const selectedVar = getSelectedVariant(product, row.variantLabel);
                row.variantLabel = selectedVar.label;

                const rowEl = document.createElement('div');
                rowEl.className = 'p-3.5 rounded-2xl bg-stone-50 border border-stone-200 space-y-2.5';
                rowEl.innerHTML = '<div class="flex items-center justify-between"><span class="text-[11px] font-bold text-stone-400 uppercase">Pilihan Kue #' + (index + 1) + '</span>' + (orderRows.length > 1 ? '<button type="button" onclick="removeOrderRow(' + row.rowId + ')" class="text-xs font-semibold text-red-600 hover:text-red-700 flex items-center gap-1"><i class="fa-solid fa-trash-can"></i> Hapus</button>' : '') + '</div><div class="grid grid-cols-1 sm:grid-cols-12 gap-2.5"><div class="sm:col-span-6"><select onchange="updateOrderRowProduct(' + row.rowId + ', this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-medium focus:outline-none focus:border-emeraldRaya-600">' + products.map(p => '<option value="' + p.id + '" ' + (p.id === product.id ? 'selected' : '') + '>' + p.name + '</option>').join('') + '</select></div><div class="sm:col-span-4"><select onchange="updateOrderRowVariant(' + row.rowId + ', this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-medium focus:outline-none focus:border-emeraldRaya-600">' + variants.map(v => '<option value="' + v.label + '" ' + (v.label === selectedVar.label ? 'selected' : '') + '>' + v.label + ' - ' + formatRupiah(v.price) + '</option>').join('') + '</select></div><div class="sm:col-span-2"><input type="number" min="1" value="' + row.qty + '" oninput="updateOrderRowQty(' + row.rowId + ', this.value)" onchange="updateOrderRowQty(' + row.rowId + ', this.value)" class="w-full px-3 py-2.5 rounded-xl bg-white border border-stone-200 text-stone-800 text-xs sm:text-sm font-bold text-center focus:outline-none focus:border-emeraldRaya-600"></div></div>';
                container.appendChild(rowEl);
            });
            calculateGrandTotal();
        }

        function addOrderItemRow(selectedProductId = null, selectedVariantLabel = null) {
            const prod = products.find(p => p.id === selectedProductId) || products[0];
            if (!prod) return;
            const variant = getSelectedVariant(prod, selectedVariantLabel);
            orderRows.push({ rowId: Date.now() + Math.random(), productId: prod.id, variantLabel: variant.label, qty: 1 });
            renderOrderRows();
        }

        function addProductToOrderForm(productId, variantLabel = null) {
            const prod = products.find(p => p.id === productId);
            if (!prod) return;
            const variant = getSelectedVariant(prod, variantLabel);
            const existingRow = orderRows.find(r => r.productId === prod.id && r.variantLabel === variant.label);
            if (existingRow) { existingRow.qty += 1; renderOrderRows(); showToast('Jumlah ' + prod.name + ' (' + variant.label + ') ditambah (+1)!', 'success'); }
            else { addOrderItemRow(prod.id, variant.label); showToast(prod.name + ' (' + variant.label + ') ditambahkan ke pesanan!', 'success'); }
            document.getElementById('form-pemesanan').scrollIntoView({ behavior: 'smooth' });
        }

        function updateOrderRowProduct(rowId, newProductId) {
            const row = orderRows.find(r => r.rowId === rowId);
            const prod = products.find(p => p.id === newProductId);
            if (row && prod) { row.productId = prod.id; const firstVar = getProductVariants(prod)[0]; row.variantLabel = firstVar ? firstVar.label : prod.weight; renderOrderRows(); }
        }

        function updateOrderRowVariant(rowId, newVariantLabel) {
            const row = orderRows.find(r => r.rowId === rowId);
            if (row) { row.variantLabel = newVariantLabel; calculateGrandTotal(); }
        }

        function updateOrderRowQty(rowId, newQty) {
            const row = orderRows.find(r => r.rowId === rowId);
            if (row) { const parsed = parseInt(newQty, 10); row.qty = parsed > 0 ? parsed : 1; calculateGrandTotal(); }
        }

        function removeOrderRow(rowId) {
            if (orderRows.length <= 1) return;
            orderRows = orderRows.filter(r => r.rowId !== rowId);
            renderOrderRows();
        }

        function calculateGrandTotal() {
            let grandTotal = 0, totalQty = 0;
            orderRows.forEach(row => {
                const product = products.find(p => p.id === row.productId);
                if (product) { const variant = getSelectedVariant(product, row.variantLabel); grandTotal += variant.price * row.qty; totalQty += row.qty; }
            });
            document.getElementById('order-total-price').textContent = formatRupiah(grandTotal);
            document.getElementById('order-total-items-count').textContent = orderRows.length + ' jenis kue (Total ' + totalQty + ' toples/paket)';
            const badge = document.getElementById('nav-cart-badge');
            if (totalQty > 0) { badge.textContent = totalQty; badge.classList.remove('hidden'); } else { badge.classList.add('hidden'); }
        }

        function getFormattedTargetWa() {
            let raw = (storeSettings.waNumber || '08819665411').replace(/\\D/g, '');
            if (raw.startsWith('0')) raw = '62' + raw.substring(1);
            else if (!raw.startsWith('62')) raw = '62' + raw;
            return raw;
        }

        function submitOrderToWhatsApp(event) {
            event.preventDefault();
            const buyerName = document.getElementById('order-name').value.trim();
            const paymentMethod = document.getElementById('order-payment').value;
            const address = document.getElementById('order-address').value.trim() || '-';
            let itemsTextList = '', grandTotal = 0, validCount = 0;
            orderRows.forEach((row, idx) => {
                const product = products.find(p => p.id === row.productId);
                if (product) {
                    validCount++;
                    const variant = getSelectedVariant(product, row.variantLabel);
                    const subtotal = variant.price * row.qty;
                    grandTotal += subtotal;
                    itemsTextList += (idx + 1) + '. *' + product.name + '* (' + variant.label + ')\\n   Jumlah: ' + row.qty + ' x ' + formatRupiah(variant.price) + ' = *' + formatRupiah(subtotal) + '*\\n';
                }
            });
            if (validCount === 0) { showToast('Silakan pilih minimal 1 jenis kue.', 'error'); return; }
            const paymentDetailLine = paymentMethod === 'Transfer Bank'
                ? '\\n• Rekening Tujuan: ' + formatBankSummary()
                : '\\n• Keterangan Bayar: Tunai saat pesanan diterima (COD)';
            const message = "Assalamu'alaikum *" + storeSettings.storeName + "* 🌙✨\\nSaya ingin memesan kue kering Idul Fitri:\\n\\n*Data Pemesan:*\\n• Nama: " + buyerName + "\\n• Metode Pembayaran: *" + paymentMethod + "*" + paymentDetailLine + "\\n\\n*Rincian Pesanan Kue:*\\n" + itemsTextList + "\\n*Total Estimasi Harga: " + formatRupiah(grandTotal) + "*\\n\\n*Alamat / Catatan:*\\n" + address + "\\n\\nMohon konfirmasi ketersediaan & proses pesanannya ya. Terima kasih! 🙏";
            showToast('Mengarahkan ke WhatsApp penjual...', 'success');
            window.location.href = 'https://wa.me/' + getFormattedTargetWa() + '?text=' + encodeURIComponent(message);
        }

        function chatDirectWhatsApp() {
            const text = encodeURIComponent("Assalamu'alaikum " + storeSettings.storeName + ", saya ingin bertanya mengenai pesanan kue kering Lebaran.");
            window.open('https://wa.me/' + getFormattedTargetWa() + '?text=' + text, '_blank', 'noopener,noreferrer');
        }

        function copyWaNumber() { copyTextToClipboard(storeSettings.waNumber || '08819665411', 'Nomor WhatsApp berhasil disalin!'); }

        function populateProfileForm() {
            document.getElementById('edit-store-name').value = storeSettings.storeName;
            document.getElementById('edit-store-subtitle').value = storeSettings.storeSubtitle;
            document.getElementById('edit-wa-number').value = storeSettings.waNumber;
            document.getElementById('edit-tagline').value = storeSettings.tagline;
            document.getElementById('edit-hero-title').value = storeSettings.heroTitle;
            document.getElementById('edit-store-bio').value = storeSettings.storeBio;
            document.getElementById('edit-bank-name').value = storeSettings.bankName || defaultSettings.bankName;
            document.getElementById('edit-bank-account').value = storeSettings.bankAccount || defaultSettings.bankAccount;
            document.getElementById('edit-bank-holder').value = storeSettings.bankHolder || defaultSettings.bankHolder;
            const activeLogo = persistentPhotos.logoDataUrl || storeSettings.logoUrl || '';
            document.getElementById('edit-logo-url').value = activeLogo;
            updateLogoPreview(activeLogo);
        }

        function refreshLogoBadge() {
            const badge = document.getElementById('logo-persistent-badge');
            if (!badge) return;
            if (persistentPhotos.logoDataUrl) { badge.textContent = 'Logo Tersimpan Permanen (Bisa Diganti)'; badge.className = 'text-[11px] font-semibold px-2.5 py-1 rounded-full bg-emerald-100 text-emerald-800'; }
            else if ((storeSettings.logoUrl || '').trim()) { badge.textContent = 'Menggunakan URL / File Logo'; badge.className = 'text-[11px] font-semibold px-2.5 py-1 rounded-full bg-amber-100 text-amber-800'; }
            else { badge.textContent = 'Ikon Bawaan'; badge.className = 'text-[11px] font-semibold px-2.5 py-1 rounded-full bg-stone-200 text-stone-600'; }
        }

        function updateLogoPreview(val) {
            const trimmed = (val || '').trim();
            const img = document.getElementById('preview-logo-img');
            const icon = document.getElementById('preview-logo-icon');
            if (trimmed) { img.src = trimmed; img.classList.remove('hidden'); icon.classList.add('hidden'); }
            else { img.classList.add('hidden'); icon.classList.remove('hidden'); }
            refreshLogoBadge();
        }

        function handleLogoUpload(event) {
            const file = event.target.files && event.target.files[0];
            if (!file) return;
            compressImageFile(file, 360, 0.82, dataUrl => {
                persistentPhotos.logoDataUrl = dataUrl; storeSettings.logoUrl = dataUrl;
                document.getElementById('edit-logo-url').value = dataUrl;
                savePersistentPhotos(); updateLogoPreview(dataUrl); applyStoreSettings(); rebuildGeneratedHtmlCode(false);
                showToast('Logo toko tersimpan permanen & tetap bisa diganti!', 'success');
            });
            event.target.value = '';
        }

        function clearLogoPhoto() {
            persistentPhotos.logoDataUrl = ''; storeSettings.logoUrl = '';
            document.getElementById('edit-logo-url').value = '';
            savePersistentPhotos(); updateLogoPreview(''); applyStoreSettings(); rebuildGeneratedHtmlCode(false);
            showToast('Logo toko dihapus.', 'info');
        }

        function saveFullStoreProfile(event) {
            event.preventDefault();
            storeSettings.storeName = document.getElementById('edit-store-name').value.trim() || defaultSettings.storeName;
            storeSettings.storeSubtitle = document.getElementById('edit-store-subtitle').value.trim() || defaultSettings.storeSubtitle;
            storeSettings.waNumber = document.getElementById('edit-wa-number').value.trim() || '08819665411';
            storeSettings.tagline = document.getElementById('edit-tagline').value.trim() || defaultSettings.tagline;
            storeSettings.heroTitle = document.getElementById('edit-hero-title').value.trim() || defaultSettings.heroTitle;
            storeSettings.storeBio = document.getElementById('edit-store-bio').value.trim() || defaultSettings.storeBio;
            storeSettings.bankName = document.getElementById('edit-bank-name').value.trim() || defaultSettings.bankName;
            storeSettings.bankAccount = document.getElementById('edit-bank-account').value.trim() || defaultSettings.bankAccount;
            storeSettings.bankHolder = document.getElementById('edit-bank-holder').value.trim() || defaultSettings.bankHolder;
            const enteredLogo = document.getElementById('edit-logo-url').value.trim();
            storeSettings.logoUrl = enteredLogo;
            persistentPhotos.logoDataUrl = enteredLogo.startsWith('data:image/') ? enteredLogo : '';
            syncAllData(true); switchToPublicView();
            showToast('Perubahan profil, logo & rekening disimpan ke Mode Publik!', 'success');
        }

        function renderAdminProducts() {
            const list = document.getElementById('admin-product-list');
            list.innerHTML = '';
            products.forEach(item => {
                const fallbackImg = 'https://placehold.co/600x400/064e3b/fbbf24?text=' + encodeURIComponent(item.name);
                const imgUrl = (item.image || '').trim() || fallbackImg;
                const isPermanentPhoto = Boolean(persistentPhotos.productsById[item.id]);
                const price500Text = Number(item.price500) > 0 ? ' • 500gr: ' + formatRupiah(item.price500) : '';
                const card = document.createElement('div');
                card.className = 'bg-white rounded-3xl overflow-hidden shadow-sm border border-stone-200 flex flex-col justify-between';
                card.innerHTML = '<div><div class="relative h-44 bg-stone-100"><img src="' + imgUrl + '" alt="' + item.name + '" onerror="this.onerror=null;this.src=\\'' + fallbackImg + '\\';" class="w-full h-full object-cover"><span class="absolute top-3 left-3 px-2.5 py-1 rounded-full bg-emeraldRaya-950/85 text-white text-[11px] font-semibold">' + item.category + '</span>' + (isPermanentPhoto ? '<span class="absolute top-3 right-3 px-2.5 py-1 rounded-full bg-goldRaya-400 text-emeraldRaya-950 text-[10px] font-bold">Foto Permanen</span>' : '') + '</div><div class="p-5"><h3 class="font-bold text-base text-stone-800 mb-1">' + item.name + '</h3><p class="text-xs text-stone-500 mb-2">' + item.weight + ': <strong class="text-emeraldRaya-800">' + formatRupiah(item.price) + '</strong>' + price500Text + '</p><p class="text-xs text-stone-600 line-clamp-2">' + item.desc + '</p></div></div><div class="px-5 pb-5 pt-3 border-t border-stone-100 flex gap-2"><button type="button" onclick="openProductModal(\\'' + item.id + '\\')" class="flex-1 py-2 rounded-xl bg-amber-100 hover:bg-amber-500 text-amber-800 hover:text-white font-semibold text-xs transition flex items-center justify-center gap-1.5"><i class="fa-solid fa-pen"></i> Edit & Ganti Foto</button><button type="button" onclick="confirmDeleteProduct(\\'' + item.id + '\\')" class="px-3.5 py-2 rounded-xl bg-red-100 hover:bg-red-600 text-red-600 hover:text-white font-semibold text-xs transition"><i class="fa-solid fa-trash"></i></button></div>';
                list.appendChild(card);
            });
        }

        function openProductModal(productId = null) {
            const modal = document.getElementById('product-modal');
            const title = document.getElementById('modal-title');
            document.getElementById('product-form').reset();
            document.getElementById('edit-product-id').value = '';
            if (productId) {
                const product = products.find(p => p.id === productId);
                if (product) {
                    title.textContent = 'Edit Kue & Foto Permanen';
                    document.getElementById('edit-product-id').value = product.id;
                    document.getElementById('prod-name').value = product.name;
                    document.getElementById('prod-price').value = product.price;
                    document.getElementById('prod-weight').value = product.weight;
                    document.getElementById('prod-price-500').value = product.price500 || '';
                    document.getElementById('prod-badge').value = product.badge || '';
                    document.getElementById('prod-category').value = product.category;
                    document.getElementById('prod-image').value = product.image || '';
                    document.getElementById('prod-desc').value = product.desc;
                    updateProductModalPreview(product.image || '', Boolean(persistentPhotos.productsById[product.id]));
                }
            } else {
                title.textContent = 'Post Kue Kering Baru';
                document.getElementById('prod-price-500').value = '85000';
                updateProductModalPreview('', false);
            }
            modal.classList.remove('hidden'); modal.classList.add('flex');
        }

        function closeProductModal() {
            const modal = document.getElementById('product-modal');
            modal.classList.add('hidden'); modal.classList.remove('flex');
        }

        function updateProductModalPreview(val, isSavedPermanent = false) {
            const trimmed = (val || '').trim();
            const img = document.getElementById('preview-prod-img');
            const statusEl = document.getElementById('prod-photo-status');
            if (trimmed) { img.src = trimmed; img.classList.remove('hidden'); } else { img.classList.add('hidden'); }
            if (isSavedPermanent || trimmed.startsWith('data:image/')) { statusEl.textContent = 'Permanen (Bisa Diganti)'; statusEl.className = 'text-[11px] font-semibold px-2 py-0.5 rounded-full bg-emerald-100 text-emerald-800'; }
            else if (trimmed) { statusEl.textContent = 'File / URL'; statusEl.className = 'text-[11px] font-semibold px-2 py-0.5 rounded-full bg-amber-100 text-amber-800'; }
            else { statusEl.textContent = 'Kosong'; statusEl.className = 'text-[11px] font-semibold px-2 py-0.5 rounded-full bg-stone-200 text-stone-600'; }
        }

        function handleProductPhotoUpload(event) {
            const file = event.target.files && event.target.files[0];
            if (!file) return;
            const currentId = document.getElementById('edit-product-id').value || ('kue-' + Date.now());
            document.getElementById('edit-product-id').value = currentId;
            compressImageFile(file, 720, 0.82, dataUrl => {
                persistentPhotos.productsById[currentId] = dataUrl;
                document.getElementById('prod-image').value = dataUrl;
                savePersistentPhotos(); updateProductModalPreview(dataUrl, true);
                showToast('Foto kue tersimpan permanen & tetap bisa diganti!', 'success');
            });
            event.target.value = '';
        }

        function clearProductPhoto() {
            const currentId = document.getElementById('edit-product-id').value;
            if (currentId && Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, currentId)) {
                delete persistentPhotos.productsById[currentId]; savePersistentPhotos();
            }
            document.getElementById('prod-image').value = ''; updateProductModalPreview('', false);
            showToast('Foto kue dikosongkan.', 'info');
        }

        function saveProduct(event) {
            event.preventDefault();
            const editId = document.getElementById('edit-product-id').value || ('kue-' + Date.now());
            const imgInputVal = document.getElementById('prod-image').value.trim();
            if (imgInputVal.startsWith('data:image/')) persistentPhotos.productsById[editId] = imgInputVal;
            else if (Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, editId)) delete persistentPhotos.productsById[editId];

            const newProductData = {
                id: editId,
                name: document.getElementById('prod-name').value.trim(),
                price: parseInt(document.getElementById('prod-price').value, 10) || 45000,
                weight: document.getElementById('prod-weight').value.trim() || 'Toples 250gr',
                price500: parseInt(document.getElementById('prod-price-500').value, 10) || 0,
                category: document.getElementById('prod-category').value,
                badge: document.getElementById('prod-badge').value.trim(),
                image: imgInputVal,
                desc: document.getElementById('prod-desc').value.trim()
            };
            const existingIndex = products.findIndex(p => p.id === editId);
            if (existingIndex !== -1) { products[existingIndex] = newProductData; showToast('Data kue & foto diperbarui!', 'success'); }
            else { products.unshift(newProductData); showToast('Kue baru berhasil diposting!', 'success'); }
            syncAllData(true); renderAdminProducts(); closeProductModal();
        }

        let productToDeleteId = null;
        function confirmDeleteProduct(id) {
            productToDeleteId = id;
            const modal = document.getElementById('delete-modal');
            modal.classList.remove('hidden'); modal.classList.add('flex');
            document.getElementById('confirm-delete-btn').onclick = () => {
                products = products.filter(p => p.id !== productToDeleteId);
                if (Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, productToDeleteId)) delete persistentPhotos.productsById[productToDeleteId];
                syncAllData(true); renderAdminProducts(); closeDeleteModal();
                showToast('Produk kue telah dihapus.', 'info');
            };
        }

        function closeDeleteModal() {
            const modal = document.getElementById('delete-modal');
            modal.classList.add('hidden'); modal.classList.remove('flex'); productToDeleteId = null;
        }

        function resetDefaultData() {
            storeSettings = { ...defaultSettings, logoUrl: persistentPhotos.logoDataUrl || '' };
            products = defaultProducts.map(item => ({
                ...item,
                image: Object.prototype.hasOwnProperty.call(persistentPhotos.productsById, item.id) ? persistentPhotos.productsById[item.id] : item.image
            }));
            syncAllData(true); populateProfileForm(); renderAdminProducts();
            showToast('Katalog & pengaturan dikembalikan ke default!', 'info');
        }

        function escapeInlineScriptJson(obj) { return JSON.stringify(obj, null, 2).replace(/<\\/script>/gi, '<\\\\/script>'); }

        function rebuildGeneratedHtmlCode(notifyUser = false) {
            const textarea = document.getElementById('generated-html-output');
            if (!textarea) return;
            textarea.value = document.documentElement.outerHTML;
            if (notifyUser) showToast('Kode HTML disegarkan sesuai data terbaru!', 'info');
        }

        function copyGeneratedHtmlCode() {
            rebuildGeneratedHtmlCode(false);
            copyTextToClipboard(document.getElementById('generated-html-output').value, 'Kode HTML terbaru berhasil disalin!');
        }

        function downloadGeneratedHtmlFile() {
            rebuildGeneratedHtmlCode(false);
            const blob = new Blob([document.getElementById('generated-html-output').value], { type: 'text/html;charset=utf-8' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url; a.download = 'index.html';
            document.body.appendChild(a); a.click(); a.remove();
            URL.revokeObjectURL(url);
            showToast('File index.html terbaru berhasil diunduh!', 'success');
        }

        function compressImageFile(file, maxSize, quality, callback) {
            const reader = new FileReader();
            reader.onload = e => {
                const img = new Image();
                img.onload = () => {
                    let w = img.width, h = img.height;
                    if (w > h && w > maxSize) { h = Math.round((h * maxSize) / w); w = maxSize; }
                    else if (h >= w && h > maxSize) { w = Math.round((w * maxSize) / h); h = maxSize; }
                    const canvas = document.createElement('canvas');
                    canvas.width = w; canvas.height = h;
                    const ctx = canvas.getContext('2d');
                    ctx.drawImage(img, 0, 0, w, h);
                    callback(canvas.toDataURL('image/jpeg', quality));
                };
                img.src = e.target.result;
            };
            reader.readAsDataURL(file);
        }

        function formatRupiah(angka) {
            return new Intl.NumberFormat('id-ID', { style: 'currency', currency: 'IDR', minimumFractionDigits: 0 }).format(angka || 0);
        }

        function formatPhoneDisplay(num) {
            const cleaned = ('' + (num || '')).replace(/\\D/g, '');
            if (cleaned.startsWith('0') && cleaned.length >= 10) return cleaned.slice(0, 4) + '-' + cleaned.slice(4, 8) + '-' + cleaned.slice(8);
            return cleaned;
        }

        function copyTextToClipboard(text, successMessage) {
            if (navigator.clipboard && navigator.clipboard.writeText) {
                navigator.clipboard.writeText(text).then(() => showToast(successMessage, 'success')).catch(() => fallbackCopy(text, successMessage));
            } else { fallbackCopy(text, successMessage); }
        }

        function fallbackCopy(text, successMessage) {
            const helper = document.createElement('textarea');
            helper.value = text; helper.setAttribute('readonly', ''); helper.style.position = 'absolute'; helper.style.left = '-9999px';
            document.body.appendChild(helper); helper.select(); document.execCommand('copy'); document.body.removeChild(helper);
            showToast(successMessage, 'success');
        }

        function showToast(message, type = 'info') {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');
            let bgClass = 'bg-emeraldRaya-900 border-goldRaya-500/40 text-white';
            let icon = 'fa-circle-info text-goldRaya-400';
            if (type === 'success') { bgClass = 'bg-emeraldRaya-800 border-emerald-400 text-white'; icon = 'fa-circle-check text-goldRaya-300'; }
            else if (type === 'error') { bgClass = 'bg-red-800 border-red-400 text-white'; icon = 'fa-circle-exclamation text-red-200'; }
            toast.className = 'pointer-events-auto flex items-center gap-3 px-4 py-3 rounded-2xl border shadow-xl text-xs sm:text-sm font-medium transform transition-all duration-300 ' + bgClass;
            toast.innerHTML = '<i class="fa-solid ' + icon + ' text-base"></i><span>' + message + '</span>';
            container.appendChild(toast);
            setTimeout(() => { toast.classList.add('opacity-0', '-translate-y-2'); setTimeout(() => toast.remove(), 300); }, 3000);
        }
    `;
                mainScript.textContent = updatedScriptBody;
            }

            textarea.value = '<!DOCTYPE html>\n' + docClone.outerHTML;
            if (notifyUser) {
                showToast('Kode HTML disegarkan sesuai data terbaru!', 'info');
            }
        }

        function copyGeneratedHtmlCode() {
            rebuildGeneratedHtmlCode(false);
            copyTextToClipboard(document.getElementById('generated-html-output').value, 'Kode HTML terbaru berhasil disalin!');
        }

        function downloadGeneratedHtmlFile() {
            rebuildGeneratedHtmlCode(false);
            const blob = new Blob([document.getElementById('generated-html-output').value], { type: 'text/html;charset=utf-8' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'index.html';
            document.body.appendChild(a);
            a.click();
            a.remove();
            URL.revokeObjectURL(url);
            showToast('File index.html terbaru berhasil diunduh!', 'success');
        }

        // =====================================================================
        // KOMPRESI FOTO, FORMAT & UTILITAS
        // =====================================================================
        function compressImageFile(file, maxSize, quality, callback) {
            const reader = new FileReader();
            reader.onload = e => {
                const img = new Image();
                img.onload = () => {
                    let w = img.width;
                    let h = img.height;
                    if (w > h && w > maxSize) {
                        h = Math.round((h * maxSize) / w);
                        w = maxSize;
                    } else if (h >= w && h > maxSize) {
                        w = Math.round((w * maxSize) / h);
                        h = maxSize;
                    }
                    const canvas = document.createElement('canvas');
                    canvas.width = w;
                    canvas.height = h;
                    const ctx = canvas.getContext('2d');
                    ctx.drawImage(img, 0, 0, w, h);
                    callback(canvas.toDataURL('image/jpeg', quality));
                };
                img.src = e.target.result;
            };
            reader.readAsDataURL(file);
        }

        function formatRupiah(angka) {
            return new Intl.NumberFormat('id-ID', {
                style: 'currency',
                currency: 'IDR',
                minimumFractionDigits: 0
            }).format(angka || 0);
        }

        function formatPhoneDisplay(num) {
            const cleaned = ('' + (num || '')).replace(/\D/g, '');
            if (cleaned.startsWith('0') && cleaned.length >= 10) {
                return `${cleaned.slice(0, 4)}-${cleaned.slice(4, 8)}-${cleaned.slice(8)}`;
            }
            return cleaned;
        }

        function copyTextToClipboard(text, successMessage) {
            if (navigator.clipboard && navigator.clipboard.writeText) {
                navigator.clipboard.writeText(text)
                    .then(() => showToast(successMessage, 'success'))
                    .catch(() => fallbackCopy(text, successMessage));
            } else {
                fallbackCopy(text, successMessage);
            }
        }

        function fallbackCopy(text, successMessage) {
            const helper = document.createElement('textarea');
            helper.value = text;
            helper.setAttribute('readonly', '');
            helper.style.position = 'absolute';
            helper.style.left = '-9999px';
            document.body.appendChild(helper);
            helper.select();
            document.execCommand('copy');
            document.body.removeChild(helper);
            showToast(successMessage, 'success');
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

            toast.className = `pointer-events-auto flex items-center gap-3 px-4 py-3 rounded-2xl border shadow-xl text-xs sm:text-sm font-medium transform transition-all duration-300 ${bgClass}`;
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
