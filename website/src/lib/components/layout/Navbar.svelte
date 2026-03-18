<script>
    import NavItem from "$lib/components/ui/NavItem.svelte";
    import LiveStreamButton from "$lib/components/ui/LiveStreamButton.svelte";
    import NavbarMobile from "./NavbarMobile.svelte";
</script>

<!-- Desktop navbar (hidden on mobile via CSS) -->
<div class="desktop-nav">
    <nav class="navbar">
        <div class="logo">
            <img src="/logo.png" alt="Crypto Banter" />
        </div>
        <div class="nav-items">
            <NavItem icon="/education-icon.png" label="Education" link="#education"/>
            <NavItem icon="/products-icon.png" label="Products" link="#products"/>
            <NavItem icon="/careers-icon.png" label="Careers" />
            <NavItem icon="/community-icon.png" label="Community" />
        </div>
        <div class="live-stream">
            <LiveStreamButton />
        </div>
    </nav>
</div>

<!-- mobile navbar (hidden on desktop via CSS) -->
<div class="mobile-nav">
    <NavbarMobile />
</div>

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

    .mobile-nav { display: none; }

    @media (max-width: 768px) {
        .desktop-nav { display: none; }
        .mobile-nav { display: block; }
    }

</style>