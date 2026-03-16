<script>
    import Navbar from "$lib/components/layout/Navbar.svelte";
    import Hero from "$lib/components/sections/Hero.svelte";
    import Education from "$lib/components/sections/Education.svelte";
    import Products from "$lib/components/sections/Products.svelte";
    import Streams from "$lib/components/sections/Streams.svelte";
    import Footer from "$lib/components/layout/Footer.svelte";
</script>

<Navbar />

<main>
    <!-- hero section -->
    <Hero />
    <Education />
    <Products />
    <Streams />
</main>

<Footer />

<style>

</style>
