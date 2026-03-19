<!-- introduction section after navbar -->

<script>
    // hardcode logos
    const partners = [
        { src: "/crypto-school-logo.png", link: "https://cryptoschool.cryptobanter.com/" },
        { src: "/banter-bubbles-icon.png", link: "https://banterbubbles.com/" },
        { src: "/banter-capital.png", link: null },
        { src: "/discord-logo.png", link: "https://discord.com/" }
    ]
</script>

<section class="hero">
    <div class="hero-overlay">

        <div class="hero-content">

            <!-- little red rectangle with text next to it -->
            <div class="tags">
                <span class="hero-tag">LOREM IPSUM</span>
                <p class="hero-subtag">Lorem Ipsum Dolor</p>
            </div>

            <h1>
                LOREM IPSUM DOLOR <br />
                SIT AMET, CONS
            </h1>

            <p class="hero-description">
                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean <br />
                commodo ligula eget dolor. Aenean massa. Cum sociis natoque <br />
                penatibus et magnis dis.
            </p>

            <div class="hero-buttons">
                <button class="get-started">Get Started</button>
                <a href="/">Call to action</a>
            </div>
            
        </div>

        <!-- batch load logos from hardcode -->
        <div class="partners">
            {#each partners as p}
                <!-- images with links -->
                <a href={p.link} target="_blank" rel="noopener noreferrer" class="partner">
                    <img src={p.src} alt="partner logo">
                </a>
            {/each}
        </div>

        <p class="section-footer">
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum <br />
            sociis natoque penatibus et magnis dis parturient montes, nascetur.
        </p>

    </div>

</section>

<style>
    /* desktop version */
    .hero {
        position: relative;
        min-height: 100vh;

        background-image:
            linear-gradient(
                to bottom,
                rgba(39,39,39,0) 80%,
                rgba(39,39,39,0.6) 90%,
                rgba(39,39,39,1) 100%
            ),
            /* load hero image */
            url("/hero-bg-img.png");

        background-size: cover;
        background-position: center;

        display: flex;
        align-items: center;

        color: white;
    }

    .hero-overlay {
        max-width: 620px;
        margin-left: 57px;
        margin-top: 125px;
        font-family: "Noyh Geometric", sans-serif;
    }

    .hero-content {
        max-width: 620px;
    }

    .tags {
        display: flex;
        align-items: center;
        gap: 11px;
        font-family: "Roboto", sans-serif;
        font-weight: 500;
    }

    .hero-tag {
        background: red;
        padding: 7px 10px;
        font-size: 1rem;
        border-radius: 7px 7px 0 7px;
    }

    .hero-subtag {
        margin: 0;
        opacity: 0.7;
    }

    h1 {
        white-space: nowrap;
        font-family: "Roboto", sans-serif !important;
        font-size: 5rem;
        font-weight: 800;
        margin: 15px 0;
        margin-top: 20px;
        line-height: 1.1;        
    }

    .hero-description {
        opacity: 0.8;
        font-size: 25px;
    }

    .hero-buttons {
        margin-top: 30px;
        display: flex;
        gap: 20px;
        align-items: center;
    }

    .get-started {
        padding: 12px 22px;
        border: 2px solid white;
        background: transparent;
        color: white;
        border-radius: 6px;

        font-size: 15px;
        font-weight: 500;

        cursor: pointer;
        transition: all 0.25s ease-in-out;
    }

    .get-started:hover {
        background: white;
        color: black;
    }

    .hero-buttons a {
        color: white;
        text-decoration: none;
        font-size: 20px;
        font-weight: 1000;

        transition: all 0.25s ease-in-out;
        transform: scale(1);
    }

    .hero-buttons a:hover {
        transform: scale(1.15);
    }

    .partners {
        display: flex;
        align-items: center;
        margin-top: 70px;
    }

    .partner {
        position: relative;
        padding: 0 30px;
    }

    .partner img {
        height: 90px;
        opacity: 0.8;
        transition: opacity 0.2s ease;
    }

    /* slightly scale down discord logo to fit with rest */
    .partner:last-child img {
        height: 40px;
        margin-left: 20px;
        opacity: 0.8;
        transition: opacity 0.2s ease;
    }

    .partner img:hover {
        opacity: 1;
        cursor: pointer;
    }

    /* vertical divider - after each partner except discord */
    .partner:not(:last-child)::after {
        content: "";
        position: absolute;
        top: -25%;
        right: 0;
        height: 150%;
        width: 3px;
        background: linear-gradient(
            to bottom,
            rgba(255,255,255,0) 0%,
            rgba(255,255,255,0.6) 50%,
            rgba(255,255,255,0) 100%
        );
    }

    .section-footer {
        font-size: 19px;
        opacity: 0.6;
        padding-top: 65px;
        padding-bottom: 30px;
    }

    /* mobile */
    @media (max-width: 768px) {

        .hero {
            /* stack vertically */
            flex-direction: column;
            align-items: stretch;
            min-height: 100vh;

            background-image:
                linear-gradient(
                    to bottom,
                    rgba(39,39,39,0)    0%,
                    rgba(39,39,39,0)   45%,
                    rgba(39,39,39,0.85) 58%,
                    rgba(39,39,39,1)   68%,
                    rgba(39,39,39,1)  100%
                ),
                url("/hero-bg-img.png");

            background-position: top center;
            background-size: cover;

            /* content below hero image */
            padding-top: 55vw;
        }

        .hero-overlay {
            max-width: 100%;
            margin-left: 0;
            margin-top: 0;
            padding: 240px 50px 0;
        }

        .hero-content {
            max-width: 100%;
        }

        .tags {
            gap: 10px;
        }

        .hero-tag {
            font-size: 1.3rem;
            padding: 10px 9px;
            border-radius: 12px 12px 0 12px;
        }

        .hero-subtag {
            font-size: 1.3rem;
        }

        h1 {
            /* allows wrapping on small screens */
            white-space: normal;
            font-size: 3.4rem;
            margin-top: 40px;
            line-height: 1.05;
        }

        .hero-description {
            font-size: 30px;
            line-height: 1.6;
        }

        /* remove breaks on mobile */
        .hero-description br {
            display: none;
        }

        .hero-buttons {
            margin-top: 28px;
            gap: 18px;
        }

        .get-started {
            padding: 22px 26px;
            font-size: 23px;
            border-radius: 8px;
        }

        .hero-buttons a {
            font-size: 25px;
        }

        .partners {
            margin-top: 48px;
            /* allow wrapping if logos overflow */
            flex-wrap: wrap;
            gap: 0;
            /* align to left edge with padding */
            padding: 0;
        }

        .partner {
            padding: 0 16px;
        }

        .partner img {
            height: 72px;
        }

        .partner:last-child img {
            height: 26px;
            margin-left: 8px;
        }

        .section-footer {
            font-size: 25px;
            padding-top: 40px;
            padding-bottom: 24px;
            line-height: 1.6;
        }

        .section-footer br {
            display: none;
        }
    }
</style>