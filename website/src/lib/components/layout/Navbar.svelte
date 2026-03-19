<!-- navigation bar on top of page -->
<!-- when viewing on small screens, renders NavbarMobile.svelte instead (css) -->

<script>
    import NavItem from "$lib/components/ui/NavItem.svelte";
    import LiveStreamButton from "$lib/components/ui/LiveStreamButton.svelte";
    import NavbarMobile from "./NavbarMobile.svelte";
</script>

<!-- desktop navbar (hidden on mobile via css) -->
<div class="desktop-nav">
    <nav class="navbar">
        <!-- logo on left -->
        <div class="logo">
            <img src="/logo.png" alt="Crypto Banter" />
        </div>
        <!-- nav items in middle -->
        <div class="nav-items">
            <NavItem icon="/education-icon.png" label="Education" link="#education"/>
            <NavItem icon="/products-icon.png" label="Products" link="#products"/>
            <NavItem icon="/careers-icon.png" label="Careers" />
            <NavItem icon="/community-icon.png" label="Community" />
        </div>
        <!-- live stream button on right -->
        <div class="live-stream">
            <LiveStreamButton />
        </div>
    </nav>
</div>

<!-- mobile navbar (hidden on desktop via css) -->
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

    /* block mobile on desktop sizes */
    .mobile-nav { 
        display: none; 
    }

    /* render only mobile on small screens */
    @media (max-width: 768px) {
        .desktop-nav {
            display: none; 
        }

        .mobile-nav { 
            display: block; 
        }
    }

</style>