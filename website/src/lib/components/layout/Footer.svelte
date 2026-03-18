<script>
    import IconButton from "$lib/components/ui/IconButton.svelte";
    import NewsletterCard from "$lib/components/ui/NewsletterCard.svelte";
</script>

<footer class="footer">

    <div class="section-divider"></div>

    <div class="top">

        <!-- logos and social media icons on left -->
        <div class="brand">
            <img src="/logo-big.png" alt="Crypto Banter logo" class="logo"/>

            <p class="copyright">
                © 2022 - 2026 <span class="banter">Crypto Banter</span>.<br />
                All Rights Reserved.
            </p>

            <div class="socials">
                <IconButton src="youtube-icon.png" alt="youtube" link="https://www.youtube.com/@CryptoBanterGroup"/>
                <IconButton src="twitter-icon.png" alt="twitter" link="https://x.com/crypto_banter"/>
                <IconButton src="message-icon.png" alt="telegram?" link="https://t.me/cryptobantergroup"/>
                <IconButton src="instagram-icon.png" alt="instagram" link="https://www.instagram.com/crypto_banter/"/>
                <IconButton src="facebook-icon.png" alt="facebook"link="https://www.facebook.com/cryptobanter/"/>
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

    <div class="section-divider-second"></div>

    <!-- bottom -->
    <div class="bottom">

        <div class="site-by">
            Site by 
            <a href="https://unomena.com" target="_blank" rel="noopener noreferrer" class="unomena">
                UNOMENA
            </a>
        </div>

        <div class="legal-section">
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
        color: white;
        background: linear-gradient(
            4deg,
            rgb(34, 34, 34) 0%,
            rgb(34, 34, 34) 75%,
            rgb(60, 60, 60) 90%,
            rgb(85, 85, 85) 100%
        );
    }

    .top {
        display: grid;
        grid-template-columns: 1.5fr 1fr 1fr 1fr 1.6fr;
        gap: 30px;
    }

    .logo {
        width: 300px;
        cursor: pointer;
    }

    .copyright {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 25px;
        margin-left: 12px;
        margin-bottom: 20px;
    }

    .banter {
        text-decoration: underline;
        cursor: pointer;
    }

    .socials {
        display: flex;
        margin-left: 12px;
        gap: 5px;
    }

    h4,
    .newsletter h4 {
        font-size: 20;
        font-family: "Roboto", sans-serif;
        letter-spacing: 1px;
        margin-bottom: 16px;
    }

    .links {
        font-family: "Noyh Geometric", sans-serif;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .links a {
        font-size: 20px;
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
        font-size: 14px;
    }

    .site-by {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 22px;
    }

    .site-by a {
        color: inherit;
        cursor: pointer;
        text-decoration: none;
    }

    .unomena {
        font-weight: 800;
        cursor: pointer;
    }

    .legal-section {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 20px;
        display: flex;
        gap: 24px;
        opacity: 0.5;
        cursor: pointer;
    }

    .section-divider {
        transform: translate(0, -80px);
        width: 90%;
        margin-left: 150px;
        height: 1px;
        background: linear-gradient(
            to right,
            rgba(255, 255, 255, 0) 0%,
            rgba(255, 255, 255, 0.4) 50%,
            rgba(255, 255, 255, 0) 100%
        );
    }

    .section-divider-second {
        transform: translate(0, 40px);
        width: 90%;
        margin-left: 150px;
        height: 1px;
        background: linear-gradient(
            to right,
            rgba(255, 255, 255, 0) 0%,
            rgba(255, 255, 255, 0.4) 50%,
            rgba(255, 255, 255, 0) 100%
        );
    }

    @media (max-width: 768px) {

        .footer {
            padding: 60px 24px 30px;
            background: linear-gradient(
                45deg,
                rgb(32, 32, 32) 0%,
                rgb(35, 35, 35) 75%,
                rgb(61, 61, 61) 90%,
                rgb(85, 85, 85) 100%
            );
        }

        .section-divider {
            transform: translate(0, -60px);
            width: 100%;
            margin-left: 0;
        }

        .section-divider-second {
            transform: translate(0, 40px);
            width: 90%;
            margin-left: 50px;
            margin-top: 25px;;
            height: 2px;
            background: linear-gradient(
                to right,
                rgba(255, 255, 255, 0) 0%,
                rgba(255, 255, 255, 0.4) 50%,
                rgba(255, 255, 255, 0) 100%
            );
        }

        .top {
            grid-template-columns: 1fr;
            gap: 0;
            text-align: center;
        }

        .brand {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 8px;
        }

        .logo {
            width: 370px;
        }

        .copyright {
            font-size: 32px;
            margin-left: 0;
            text-align: center;
        }

        .socials {
            margin-left: 0;
            justify-content: center;
            margin-top: 80px;
            margin-bottom: 8px;
            gap: 6px;
            transform: scale(1.2);
        }

        .links {
            align-items: center;
            padding: 24px 0 8px;
        }

        .links h4 {
            font-size: 20px;
        }

        .links a {
            font-size: 33px;
        }

        .newsletter {
            align-items: center;
            margin-top: 24px;
        }

        .newsletter h4 {
            text-align: center;
            font-size: 20px;
        }

        .bottom {
            flex-direction: column;
            align-items: center;
            gap: 16px;
            margin-top: 40px;
        }

        .site-by {
            transform: translate(0, -1385px);
            font-size: 26px;
        }

        .legal-section {
            display: flex;
            flex-wrap: wrap;         
            justify-content: center; 
            gap: 16px;     
            font-size: 25px;
        }

        .legal-section a {
            /* move columns closer together */
            flex: 0 0 40%;      
            text-align: center;      
        }
    }

</style>