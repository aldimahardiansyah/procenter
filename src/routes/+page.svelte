<script lang="ts">
  import Shield from 'lucide-svelte/icons/shield';
  import Smartphone from 'lucide-svelte/icons/smartphone';
  import Lock from 'lucide-svelte/icons/lock';
  import Cloud from 'lucide-svelte/icons/cloud';
  import Cpu from 'lucide-svelte/icons/cpu';
  import Activity from 'lucide-svelte/icons/activity';
  import ArrowRight from 'lucide-svelte/icons/arrow-right';
  import CheckCircle2 from 'lucide-svelte/icons/check-circle-2';
  import Menu from 'lucide-svelte/icons/menu';
  import X from 'lucide-svelte/icons/x';
  
  let isMenuOpen = $state(false);
</script>

<svelte:head>
  <title>Procenter | Cloud-based Access Control & IoT Security</title>
  <meta name="description" content="Centralized dashboard to monitor and manage physical security infrastructure." />
</svelte:head>

<div class="min-h-screen bg-slate-50 text-slate-900 font-sans">
  <!-- Navigation -->
  <header class="fixed top-0 w-full bg-white/80 backdrop-blur-md z-50 border-b border-slate-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center h-16">
        <div class="flex items-center gap-2">
          <Shield class="w-8 h-8 text-blue-600" />
          <span class="text-xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-blue-700 to-cyan-600">Procenter</span>
        </div>
        
        <!-- Desktop Menu -->
        <nav class="hidden md:flex items-center gap-8">
          <a href="#features" class="text-sm font-medium text-slate-600 hover:text-blue-600 transition-colors">Fitur</a>
          <a href="#how-it-works" class="text-sm font-medium text-slate-600 hover:text-blue-600 transition-colors">Cara Kerja</a>
          <a href="#hardware" class="text-sm font-medium text-slate-600 hover:text-blue-600 transition-colors">Integrasi IoT</a>
          <div class="flex items-center gap-4">
            <button class="text-sm font-medium text-slate-600 hover:text-blue-600 transition-colors">Log in</button>
            <button class="bg-blue-600 text-white px-4 py-2 rounded-lg text-sm font-medium hover:bg-blue-700 transition-colors shadow-sm">Mulai Gratis</button>
          </div>
        </nav>

        <!-- Mobile Menu Button -->
        <button class="md:hidden p-2 text-slate-600" onclick={() => isMenuOpen = !isMenuOpen}>
          {#if isMenuOpen}
            <X class="w-6 h-6" />
          {:else}
            <Menu class="w-6 h-6" />
          {/if}
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    {#if isMenuOpen}
      <div class="md:hidden bg-white border-t border-slate-100 px-4 py-4 space-y-4">
        <a href="#features" class="block text-sm font-medium text-slate-600" onclick={() => isMenuOpen = false}>Fitur</a>
        <a href="#how-it-works" class="block text-sm font-medium text-slate-600" onclick={() => isMenuOpen = false}>Cara Kerja</a>
        <a href="#hardware" class="block text-sm font-medium text-slate-600" onclick={() => isMenuOpen = false}>Integrasi IoT</a>
        <div class="pt-4 flex flex-col gap-3 border-t border-slate-100">
          <button class="w-full text-center py-2 text-sm font-medium text-slate-600 border border-slate-200 rounded-lg">Log in</button>
          <button class="w-full text-center py-2 bg-blue-600 text-white rounded-lg text-sm font-medium">Mulai Gratis</button>
        </div>
      </div>
    {/if}
  </header>

  <!-- Hero Section -->
  <section class="pt-32 pb-20 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
    <div class="grid lg:grid-cols-2 gap-12 items-center">
      <div class="space-y-8">
        <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-blue-50 text-blue-700 text-sm font-medium border border-blue-100">
          <span class="flex h-2 w-2 rounded-full bg-blue-600"></span>
          Procenter Cloud v2.0 Released
        </div>
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight text-slate-900 leading-[1.1]">
          Keamanan Gedung di <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-cyan-500">Ujung Jari Anda.</span>
        </h1>
        <p class="text-lg text-slate-600 leading-relaxed max-w-xl">
          Dashboard terpusat untuk memantau dan mengelola infrastruktur keamanan fisik Anda. Terintegrasi langsung dengan mikrokontroler ESP32, pembaca QR, dan magnetic lock.
        </p>
        <div class="flex flex-col sm:flex-row gap-4">
          <button class="inline-flex justify-center items-center gap-2 bg-blue-600 text-white px-6 py-3 rounded-xl font-medium hover:bg-blue-700 transition-all shadow-lg shadow-blue-600/20">
            Coba Demo Dashboard
            <ArrowRight class="w-4 h-4" />
          </button>
          <button class="inline-flex justify-center items-center gap-2 bg-white text-slate-700 border border-slate-200 px-6 py-3 rounded-xl font-medium hover:bg-slate-50 transition-all">
            Pelajari Dokumentasi API
          </button>
        </div>
        <div class="flex items-center gap-6 pt-4 text-sm text-slate-500 font-medium">
          <div class="flex items-center gap-2"><CheckCircle2 class="w-4 h-4 text-emerald-500"/> No credit card required</div>
          <div class="flex items-center gap-2"><CheckCircle2 class="w-4 h-4 text-emerald-500"/> Free plan available</div>
        </div>
      </div>
      
      <div class="relative">
        <div class="absolute inset-0 bg-gradient-to-tr from-blue-500 to-cyan-300 rounded-3xl blur-3xl opacity-20 animate-pulse"></div>
        <div class="relative bg-white rounded-2xl border border-slate-200 shadow-2xl overflow-hidden">
          <div class="bg-slate-900 px-4 py-3 flex items-center gap-2">
            <div class="w-3 h-3 rounded-full bg-red-500"></div>
            <div class="w-3 h-3 rounded-full bg-yellow-500"></div>
            <div class="w-3 h-3 rounded-full bg-green-500"></div>
            <div class="ml-4 text-xs font-mono text-slate-400">procenter.cloud/dashboard</div>
          </div>
          <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&q=80&w=1000" alt="Dashboard Interface" class="w-full h-auto object-cover border-t border-slate-800/50" />
        </div>
      </div>
    </div>
  </section>

  <!-- Features Section -->
  <section id="features" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-3xl mx-auto mb-16">
        <h2 class="text-3xl font-bold text-slate-900 mb-4">Semua yang Anda butuhkan untuk akses kontrol modern</h2>
        <p class="text-lg text-slate-600">Tinggalkan sistem konvensional. Procenter menghubungkan hardware di lapangan langsung ke cloud untuk manajemen yang efisien dan real-time.</p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Feature 1 -->
        <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 hover:shadow-lg transition-shadow">
          <div class="w-12 h-12 rounded-xl bg-blue-100 flex items-center justify-center mb-6 text-blue-600">
            <Cloud class="w-6 h-6" />
          </div>
          <h3 class="text-xl font-bold text-slate-900 mb-3">100% Cloud-Based</h3>
          <p class="text-slate-600">Pantau dan kelola akses pintu dari mana saja di dunia melalui dashboard web kami. Tanpa perlu server lokal.</p>
        </div>
        <!-- Feature 2 -->
        <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 hover:shadow-lg transition-shadow">
          <div class="w-12 h-12 rounded-xl bg-cyan-100 flex items-center justify-center mb-6 text-cyan-600">
            <Cpu class="w-6 h-6" />
          </div>
          <h3 class="text-xl font-bold text-slate-900 mb-3">Integrasi IoT Seamless</h3>
          <p class="text-slate-600">Kompatibel dengan mikrokontroler populer seperti ESP32. SDK yang mudah digunakan untuk menghubungkan device Anda.</p>
        </div>
        <!-- Feature 3 -->
        <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 hover:shadow-lg transition-shadow">
          <div class="w-12 h-12 rounded-xl bg-emerald-100 flex items-center justify-center mb-6 text-emerald-600">
            <Activity class="w-6 h-6" />
          </div>
          <h3 class="text-xl font-bold text-slate-900 mb-3">Real-time Monitoring</h3>
          <p class="text-slate-600">Dapatkan notifikasi instan setiap kali ada akses, pintu terbuka terlalu lama, atau upaya akses yang gagal.</p>
        </div>
        <!-- Feature 4 -->
        <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 hover:shadow-lg transition-shadow">
          <div class="w-12 h-12 rounded-xl bg-indigo-100 flex items-center justify-center mb-6 text-indigo-600">
            <Smartphone class="w-6 h-6" />
          </div>
          <h3 class="text-xl font-bold text-slate-900 mb-3">Akses via QR Code</h3>
          <p class="text-slate-600">Gunakan smartphone sebagai kunci. Generate QR code sementara untuk tamu atau QR dinamis untuk karyawan.</p>
        </div>
        <!-- Feature 5 -->
        <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 hover:shadow-lg transition-shadow">
          <div class="w-12 h-12 rounded-xl bg-rose-100 flex items-center justify-center mb-6 text-rose-600">
            <Lock class="w-6 h-6" />
          </div>
          <h3 class="text-xl font-bold text-slate-900 mb-3">Kontrol Magnetic Lock</h3>
          <p class="text-slate-600">Atur jadwal penguncian otomatis, buka pintu dari jarak jauh, dan pantau status lock door secara live.</p>
        </div>
        <!-- Feature 6 -->
        <div class="p-6 rounded-2xl bg-slate-50 border border-slate-100 hover:shadow-lg transition-shadow">
          <div class="w-12 h-12 rounded-xl bg-violet-100 flex items-center justify-center mb-6 text-violet-600">
            <Shield class="w-6 h-6" />
          </div>
          <h3 class="text-xl font-bold text-slate-900 mb-3">Keamanan Enterprise</h3>
          <p class="text-slate-600">Enkripsi end-to-end dari device ke cloud. Log audit komprehensif untuk memenuhi standar kepatuhan.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- How It Works Section -->
  <section id="how-it-works" class="py-24 bg-slate-900 text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl font-bold mb-4">Cara Kerja Procenter</h2>
        <p class="text-slate-400 max-w-2xl mx-auto">Arsitektur modern yang memastikan latensi rendah dan keandalan tinggi untuk sistem keamanan fisik Anda.</p>
      </div>
      
      <div class="grid md:grid-cols-4 gap-8 text-center relative">
        <div class="hidden md:block absolute top-12 left-[12.5%] right-[12.5%] h-0.5 bg-slate-800 -z-10"></div>
        
        <div class="relative z-10 flex flex-col items-center">
          <div class="w-24 h-24 rounded-full bg-slate-800 border-4 border-slate-900 flex items-center justify-center mb-6 shadow-xl">
            <Smartphone class="w-10 h-10 text-blue-400" />
          </div>
          <h4 class="text-lg font-bold mb-2">1. Scan QR Code</h4>
          <p class="text-sm text-slate-400">Pengguna memindai kode QR dinamis mereka pada reader di pintu.</p>
        </div>
        
        <div class="relative z-10 flex flex-col items-center">
          <div class="w-24 h-24 rounded-full bg-slate-800 border-4 border-slate-900 flex items-center justify-center mb-6 shadow-xl">
            <Cpu class="w-10 h-10 text-cyan-400" />
          </div>
          <h4 class="text-lg font-bold mb-2">2. ESP32 Memproses</h4>
          <p class="text-sm text-slate-400">Mikrokontroler membaca data dan mengirimkannya ke Procenter API melalui WiFi/Ethernet.</p>
        </div>
        
        <div class="relative z-10 flex flex-col items-center">
          <div class="w-24 h-24 rounded-full bg-slate-800 border-4 border-slate-900 flex items-center justify-center mb-6 shadow-xl">
            <Cloud class="w-10 h-10 text-indigo-400" />
          </div>
          <h4 class="text-lg font-bold mb-2">3. Cloud Validasi</h4>
          <p class="text-sm text-slate-400">Server memvalidasi izin akses dalam milidetik dan merespons kembali ke device.</p>
        </div>
        
        <div class="relative z-10 flex flex-col items-center">
          <div class="w-24 h-24 rounded-full bg-slate-800 border-4 border-slate-900 flex items-center justify-center mb-6 shadow-xl">
            <Lock class="w-10 h-10 text-emerald-400" />
          </div>
          <h4 class="text-lg font-bold mb-2">4. Pintu Terbuka</h4>
          <p class="text-sm text-slate-400">Relay memicu magnetic lock untuk terbuka, log tercatat di dashboard.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section class="py-20 bg-blue-600 relative overflow-hidden">
    <div class="absolute inset-0 bg-[url('https://www.transparenttextures.com/patterns/cubes.png')] opacity-10"></div>
    <div class="max-w-4xl mx-auto px-4 text-center relative z-10">
      <h2 class="text-3xl md:text-4xl font-bold text-white mb-6">Siap Mengamankan Gedung Anda?</h2>
      <p class="text-blue-100 text-lg mb-10 max-w-2xl mx-auto">Mulai gunakan Procenter hari ini dan rasakan kemudahan mengelola ribuan titik akses dari satu layar.</p>
      <div class="flex flex-col sm:flex-row justify-center gap-4">
        <button class="bg-white text-blue-600 px-8 py-4 rounded-xl font-bold text-lg hover:bg-slate-50 transition-colors shadow-xl">
          Daftar Gratis Sekarang
        </button>
        <button class="bg-blue-700 text-white px-8 py-4 rounded-xl font-bold text-lg hover:bg-blue-800 transition-colors border border-blue-500">
          Hubungi Sales
        </button>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-white border-t border-slate-200 pt-16 pb-8">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-5 gap-8 mb-12">
        <div class="col-span-2 lg:col-span-2">
          <div class="flex items-center gap-2 mb-4">
            <Shield class="w-6 h-6 text-blue-600" />
            <span class="text-xl font-bold text-slate-900">Procenter</span>
          </div>
          <p class="text-slate-500 text-sm mb-6 max-w-sm">Platform IoT modern untuk manajemen kontrol akses gedung. Terpusat, aman, dan mudah diintegrasikan dengan hardware existing Anda.</p>
        </div>
        <div>
          <h4 class="font-bold text-slate-900 mb-4">Produk</h4>
          <ul class="space-y-3 text-sm text-slate-500">
            <li><button class="hover:text-blue-600">Dashboard</button></li>
            <li><button class="hover:text-blue-600">Hardware Integration</button></li>
            <li><button class="hover:text-blue-600">Mobile App</button></li>
            <li><button class="hover:text-blue-600">API Documentation</button></li>
          </ul>
        </div>
        <div>
          <h4 class="font-bold text-slate-900 mb-4">Perusahaan</h4>
          <ul class="space-y-3 text-sm text-slate-500">
            <li><button class="hover:text-blue-600">Tentang Kami</button></li>
            <li><button class="hover:text-blue-600">Blog</button></li>
            <li><button class="hover:text-blue-600">Karir</button></li>
            <li><button class="hover:text-blue-600">Kontak</button></li>
          </ul>
        </div>
        <div>
          <h4 class="font-bold text-slate-900 mb-4">Legal</h4>
          <ul class="space-y-3 text-sm text-slate-500">
            <li><button class="hover:text-blue-600">Privacy Policy</button></li>
            <li><button class="hover:text-blue-600">Terms of Service</button></li>
            <li><button class="hover:text-blue-600">Security</button></li>
          </ul>
        </div>
      </div>
      <div class="border-t border-slate-200 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
        <p class="text-sm text-slate-500">© 2026 Procenter.cloud. All rights reserved.</p>
        <div class="flex gap-4">
          <div class="w-8 h-8 rounded-full bg-slate-100 flex items-center justify-center text-slate-400 hover:text-blue-600 cursor-pointer transition-colors"><Shield class="w-4 h-4"/></div>
          <div class="w-8 h-8 rounded-full bg-slate-100 flex items-center justify-center text-slate-400 hover:text-blue-600 cursor-pointer transition-colors"><Cloud class="w-4 h-4"/></div>
        </div>
      </div>
    </div>
  </footer>
</div>
