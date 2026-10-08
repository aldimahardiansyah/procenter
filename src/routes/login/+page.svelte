<script lang="ts">
  import Shield from 'lucide-svelte/icons/shield';
  import ArrowRight from 'lucide-svelte/icons/arrow-right';
</script>

<svelte:head>
  <title>Login - Procenter Dashboard</title>
</svelte:head>

<div class="min-h-screen bg-slate-50 flex flex-col justify-center py-12 sm:px-6 lg:px-8">
  <div class="sm:mx-auto sm:w-full sm:max-w-md">
    <a href="/" class="flex justify-center items-center gap-2 mb-6 hover:opacity-80 transition-opacity">
      <Shield class="w-10 h-10 text-blue-600" />
      <span class="text-3xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-blue-700 to-cyan-600">Procenter</span>
    </a>
    <h2 class="mt-6 text-center text-3xl font-extrabold text-slate-900">
      Masuk ke akun Anda
    </h2>
    <p class="mt-2 text-center text-sm text-slate-600">
      Atau
      <a href="/register" class="font-medium text-blue-600 hover:text-blue-500">
        daftar akun baru gratis
      </a>
    </p>
  </div>

  <div class="mt-8 sm:mx-auto sm:w-full sm:max-w-md">
    <div class="bg-white py-8 px-4 shadow-xl shadow-slate-200/50 sm:rounded-2xl sm:px-10 border border-slate-100">
      <form class="space-y-6" onsubmit={(e) => e.preventDefault()}>
        <div>
          <label for="email" class="block text-sm font-medium text-slate-700">
            Alamat Email
          </label>
          <div class="mt-1">
            <input id="email" name="email" type="email" autocomplete="email" required class="appearance-none block w-full px-3 py-2 border border-slate-300 rounded-lg shadow-sm placeholder-slate-400 focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm">
          </div>
        </div>

        <div>
          <label for="password" class="block text-sm font-medium text-slate-700">
            Kata Sandi
          </label>
          <div class="mt-1">
            <input id="password" name="password" type="password" autocomplete="current-password" required class="appearance-none block w-full px-3 py-2 border border-slate-300 rounded-lg shadow-sm placeholder-slate-400 focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm">
          </div>
        </div>

        <div class="flex items-center justify-between">
          <div class="flex items-center">
            <input id="remember-me" name="remember-me" type="checkbox" class="h-4 w-4 text-blue-600 focus:ring-blue-500 border-slate-300 rounded">
            <label for="remember-me" class="ml-2 block text-sm text-slate-900">
              Ingat saya
            </label>
          </div>

          <div class="text-sm">
            <a href="#" class="font-medium text-blue-600 hover:text-blue-500">
              Lupa sandi?
            </a>
          </div>
        </div>

        <div>
          <button type="submit" class="w-full flex justify-center py-2.5 px-4 border border-transparent rounded-lg shadow-sm text-sm font-medium text-white bg-blue-600 hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 transition-colors">
            Masuk
          </button>
        </div>
      </form>
    </div>
  </div>
</div>
