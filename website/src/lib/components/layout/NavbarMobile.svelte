<!-- mobile version of navbar has very different layout, easier with separate file instead of just some css changes -->

<script>
    import LiveStreamButton from "$lib/components/ui/LiveStreamButton.svelte";
    import NavItem from "$lib/components/ui/NavItem.svelte";

    // open/close navbar menu when clicking on hamburger icon 
    let menuOpen = $state(false);

    function toggleMenu() {
        menuOpen = !menuOpen;
    }

    function closeMenu() {
        menuOpen = false;
    }
</script>

<!-- clicking outside of navbar while open automatically closes it -->
{#if menuOpen}
    <div class="backdrop" onclick={closeMenu}></div>
{/if}

<nav class="navbar">
    <!-- logo on left -->
    <div class="logo">
        <img src="/logo.png" alt="Crypto Banter" />
    </div>

    <!-- hamburger button on right -->
    <button class="explore" onclick={toggleMenu} aria-label="Toggle menu">
        <span>Explore</span>
        <span class="hamburger-icon">≡</span>
    </button>
</nav>

<!-- slide-down drawer if menu-open set to true, else, no drawer-->
{#if menuOpen}
    <div class="drawer">
        <div class="drawer-items">
        <NavItem icon="/education-icon.png" label="Education" link="#education" />
        <NavItem icon="/products-icon.png" label="Products" link="#products" />
        <NavItem icon="/careers-icon.png" label="Careers" />
        <NavItem icon="/community-icon.png" label="Community" />
        </div>
        <div class="drawer-live">
        <!-- add livestream button to hamburger menu -->
        <LiveStreamButton />
        </div>
    </div>
{/if}

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
        box-sizing: border-box;
        padding: 0 20px;
    }

    .logo img {
        height: 140px;
        cursor: pointer;
        transition: all 0.2s ease-in-out;
    }

    .logo img:hover {
        transform: scale(1.03);
    }

    .explore {
        display: flex;
        align-items: center;
        gap: 8px;
        padding: 13px 16px;
        background: rgba(255, 255, 255, 0.25);
        border: none;
        border-radius: 17px 17px 0 17px;
        cursor: pointer;
        color: white;
        font-family: "Noyh Geometric", sans-serif;
        font-size: 30px;
        font-weight: 500;
        transition: all 0.2s ease-in-out;
        backdrop-filter: blur(4px);
    }

    .explore:hover {
        background: rgba(255, 255, 255, 0.45);
    }

    .hamburger-icon {
        transform: translate(0, 2px);
        font-size: 32px;
        line-height: 1;
    }

    /* backdrop to close menu on outside click */
    .backdrop {
        position: fixed;
        inset: 0;
        z-index: 998;
        background: transparent;
    }

    /* slide-down drawer */
    .drawer {
        position: absolute;
        top: 118px;
        left: 0;
        width: 100%;
        z-index: 999;
        background: linear-gradient(rgb(97, 21, 95), rgb(192, 19, 100));
        backdrop-filter: blur(12px);
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        padding: 16px 20px 24px;
        box-sizing: border-box;
        border-bottom-left-radius: 16px;
        border-bottom-right-radius: 16px;
        box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);

        /* short animation */
        animation: slideDown 0.22s ease-out;
    }

    /* like blender */
    @keyframes slideDown {
        from {
        opacity: 0;
        transform: translateY(-10px);
        }
        to {
        opacity: 1;
        transform: translateY(0);
        }
    }

    .drawer-items {
        display: flex;
        flex-direction: column;
        width: 100%;
        gap: 4px;
    }

    .drawer-live {
        margin-top: 20px;
        padding-left: 14px;
    }
</style>