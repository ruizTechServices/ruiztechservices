<script>
    let currentYear = new Date().getFullYear();
</script>

<footer class="bg-blue-600 p-4 text-white mt-10">
    <div class="container mx-auto text-center">
        &copy; <span>{currentYear}</span> ruizTechServices<span id="blinking">|</span>
        <div class="mt-4">
            <h2 class="font-bold">Quick Menu</h2>
            <ul class="flex flex-wrap justify-center space-x-4 mt-2">
                <li><a href="#home" class="hover:underline">Home</a></li>
                <li><a href="#about" class="hover:underline">About</a></li>
                <li><a href="#contact" class="hover:underline">Contact</a></li>
                <li><a href="#blog" class="hover:underline">Blog</a></li>
                <li><a href="#privacy-policy" class="hover:underline">Privacy Policy</a></li>
                <li><a href="#login" class="hover:underline">Login</a></li>
            </ul>
        </div>
    </div>
</footer>

<style>
    @keyframes blink {
        0% { opacity: 1; }
        50% { opacity: 0; }
        100% { opacity: 1; }
    }
    #blinking {
        animation: blink 1s infinite;
    }
</style>