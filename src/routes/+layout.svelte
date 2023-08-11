<script>
  import "../app.css";
  import Navbar from "../components/navbar.svelte";
  import Footer from "../components/footer.svelte";
</script>


<Navbar />

<div class="">
<slot />
</div>
<Footer />
