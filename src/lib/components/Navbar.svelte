<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<div class="fixed w-full z-50 transition-colors duration-300 top-0 left-0 font-sans">
  <!-- Top Bar -->
  <div class="bg-gray-950 text-white text-[11px] font-medium tracking-wide text-center py-2.5 flex justify-center items-center gap-1 cursor-pointer hover:underline">
    <span>Experience World-Class Recovery in Rockwell</span>
    <span class="text-[10px]">➜</span>
  </div>

  <!-- Main Nav -->
  <nav class="flex justify-between items-center px-6 py-4 md:px-10 transition-all duration-300 {isScrolled ? 'bg-white/95 backdrop-blur-md shadow-sm py-3 text-gray-950' : 'bg-transparent text-white'}">
    <!-- Left Links -->
    <div class="hidden md:flex items-center gap-8 text-[13px] font-medium tracking-wide">
      <a href="/" class="hover:opacity-60 transition-opacity">Modalities</a>
      <a href="/" class="hover:opacity-60 transition-opacity">Membership</a>
      <a href="/" class="hover:opacity-60 transition-opacity">About</a>
    </div>

    <!-- Logo -->
    <div class="absolute left-1/2 transform -translate-x-1/2">
      <a href="/" class="block flex items-center gap-2">
        <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-6 h-6">
          <path d="M12 2L13.2 9.92154L20.6603 7L14.4 12L20.6603 17L13.2 14.0785L12 22L10.8 14.0785L3.33975 17L9.6 12L3.33975 7L10.8 9.92154L12 2Z" fill="currentColor" />
        </svg>
        <span class="text-xl font-light tracking-wider">CLUB REMEDY</span>
      </a>
    </div>

    <!-- Right Links -->
    <div class="flex items-center gap-6 md:gap-8">
      <a href="/" class="text-[13px] font-medium tracking-wide hover:opacity-60 transition-opacity hidden md:block">Member Login</a>
      <a href="/" class="{isScrolled ? 'bg-gray-950 text-white' : 'bg-white text-gray-950'} px-5 py-2 rounded-full text-[13px] font-bold tracking-wide hover:opacity-90 transition-all shadow-sm">Book Visit</a>
      <button class="md:hidden">
        <!-- Mobile Menu Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg>
      </button>
    </div>
  </nav>
</div>
