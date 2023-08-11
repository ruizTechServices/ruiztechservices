<script>
    let showMobileNav = false;
  
    function toggleMobileNav() {
      showMobileNav = !showMobileNav;
    }
  </script>
  
  <nav class="bg-blue-600 p-4 text-white">
    <div class="container mx-auto flex justify-between items-center">
      <h1 class="text-2xl font-bold">
        ruizTechServices<span id="blinking">|</span>
      </h1>
      <ul class="hidden md:flex space-x-4">
        <li><a href="#home" class="hover:underline">Home</a></li>
        <li><a href="#about" class="hover:underline">About</a></li>
        <li><a href="#contact" class="hover:underline">Contact</a></li>
        <li><a href="#blog" class="hover:underline">Blog</a></li>
        <li>
          <a href="#privacy-policy" class="hover:underline">Privacy Policy</a>
        </li>
        <li><a href="#login" class="hover:underline">Login</a></li>
      </ul>
      <!-- Hamburger menu for smaller screens -->
      <div class="md:hidden flex items-center">
        <button on:click={toggleMobileNav} class="text-white">☰</button>
      </div>
    </div>
    <!-- Mobile Nav Menu -->
    {#if showMobileNav}
    <div class="w-full bg-blue-500">
      <ul class="flex flex-col space-y-2 py-2">
        <li><a href="#home" class="block px-4 py-2 hover:underline">Home</a></li>
        <li><a href="#about" class="block px-4 py-2 hover:underline">About</a></li>
        <li><a href="#contact" class="block px-4 py-2 hover:underline">Contact</a></li>
        <li><a href="#blog" class="block px-4 py-2 hover:underline">Blog</a></li>
        <li><a href="#privacy-policy" class="block px-4 py-2 hover:underline">Privacy Policy</a></li>
        <li><a href="#login" class="block px-4 py-2 hover:underline">Login</a></li>
      </ul>
    </div>
    {/if}
  </nav>
  
  <div class="navbar bg-base-100" />
  
  <style>
    @keyframes blink {
      0% {
        opacity: 1;
      }
      50% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
    #blinking {
      animation: blink 1s infinite;
    }
  </style>
  