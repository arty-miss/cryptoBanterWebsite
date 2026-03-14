<script>
    import NavItem from "$lib/components/ui/NavItem.svelte";
    import LiveStreamButton from "$lib/components/ui/LiveStreamButton.svelte";
</script>

<nav class="navbar">

    <!-- logo on left side -->
    <div class="logo">
        <img src="/logo.png" alt="Crypto Banter" />
    </div>

    <!-- nav items in middle -->
    <div class="nav-items">
        <NavItem icon="/education-icon.png" label="Education" />
        <NavItem icon="/products-icon.png" label="Products" />
        <NavItem icon="/careers-icon.png" label="Careers" />
        <NavItem icon="/community-icon.png" label="Community" />
    </div>

    <!-- livestream button on right side -->
    <div class="live-stream">
        <LiveStreamButton />
    </div>

</nav>

<style>
    .navbar {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1000;
        background: transparent;
        
        display: flex;
        align-items: center;
        justify-content: space-between;

        width: 100%;
    }

    .logo img {
        height: 120px;
        cursor: pointer;
        padding-left: 50px;
        transition: all 0.2s ease-in-out;
    }

    .logo img:hover {
        transform: scale(1.03);
    }

    .nav-items {
        display: flex;
        align-items: center;
        gap: 18px;
    }

    .live-stream {
        padding-right: 55px;
    }

</style>