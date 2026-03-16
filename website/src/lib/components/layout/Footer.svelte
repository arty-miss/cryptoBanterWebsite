<script>
    import IconButton from "$lib/components/ui/IconButton.svelte";
    import NewsletterCard from "$lib/components/ui/NewsletterCard.svelte";
</script>

<footer class="footer">

    <div class="top">

        <!-- logos and social media icons on left -->
        <div class="brand">
            <img src="/logo.png" alt="Crypto Banter logo" class="logo"/>

            <p class="copyright">
                © 2022 - 2026 Crypto Banter.<br />
                All Rights Reserved.
            </p>

            <div class="socials">
                <IconButton src="youtube-icon.png" alt="youtube"/>
                <IconButton src="twitter-icon.png" alt="twitter"/>
                <IconButton src="message-icon.png" alt="telegram?"/>
                <IconButton src="instagram-icon.png" alt="instagram"/>
                <IconButton src="facebook-icon.png" alt="facebook"/>
            </div>
        </div>


        <!-- inks section in middle -->
        <div class="links">
            <h4>EDUCATION</h4>
            <a>Intro to Crypto</a>
            <a>DAVIDD Tech School</a>
            <a>Trading Xcelerator</a>
            <a>Sniper School</a>
            <a>+ 2 more</a>
        </div>

        <div class="links">
            <h4>PRODUCTS</h4>
            <a>Crypto School</a>
            <a>Banter Bubbles</a>
            <a>Banter Capital</a>
            <a>VIP Communities</a>
        </div>

        <div class="links">
            <h4>COMPANY</h4>
            <a>Host Profiles</a>
            <a>Work with us</a>
        </div>


        <!-- newsletter signup on right -->
        <div class="newsletter">
            <h4>NEWSLETTER SIGN UP</h4>

            <NewsletterCard
                title="Good Morning Crypto"
            />

            <NewsletterCard
                title="The Daily Candle"
            />
        </div>

    </div>


    <!-- bottom -->
    <div class="bottom">

        <div class="siteby">
            Site by <strong>UNOMENA</strong>
        </div>

        <div class="legal">
            <a>Our Ethics</a>
            <a>Fulfillment Policy</a>
            <a>Terms of Service</a>
            <a>Privacy Policy</a>
        </div>

    </div>

</footer>


<style>
    .footer {
        padding: 80px 60px 30px;
        color: #dcdcdc;
        background: linear-gradient(#141414, #0f0f0f);
    }

    .top {
        display: grid;
        grid-template-columns: 1.5fr 1fr 1fr 1fr 1.6fr;
        gap: 60px;
    }

    .logo {
        width: 180px;
        margin-bottom: 20px;
    }

    .copyright {
        font-size: 14px;
        opacity: 0.7;
        margin-bottom: 20px;
    }

    .socials {
        display: flex;
        gap: 12px;
    }

    .links h4,
    .newsletter h4 {
        font-size: 13px;
        letter-spacing: 1px;
        margin-bottom: 16px;
        opacity: 0.6;
    }

    .links {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .links a {
        font-size: 15px;
        cursor: pointer;
        opacity: 0.85;
    }

    .newsletter {
        display: flex;
        flex-direction: column;
        gap: 16px;
    }

    .bottom {
        display: flex;
        justify-content: space-between;
        margin-top: 60px;
        padding-top: 20px;
        border-top: 1px solid rgba(255,255,255,0.08);
        font-size: 14px;
    }

    .legal {
        display: flex;
        gap: 24px;
        opacity: 0.7;
    }

</style>