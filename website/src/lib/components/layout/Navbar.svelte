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
        <NavItem icon="/education.png" label="Education" />
        <NavItem icon="/products.png" label="Products" />
        <NavItem icon="/careers.png" label="Careers" />
        <NavItem icon="/community.png" label="Community" />
    </div>

    <!-- livestream button on right side -->
    <div class="live-stream">
        <LiveStreamButton />
    </div>

</nav>

<style>
    .navbar {
        display: flex;
        align-items: center;
        justify-content: space-between;

        padding: 16px 40px;

        width: 100%;
    }

    .logo img {
        height: 120px;
        cursor: pointer;
    }

    .nav-items {
        display: flex;
        gap: 14px;
    }

</style>