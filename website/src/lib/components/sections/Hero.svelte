<section class="hero">
    <div class="hero-overlay">

        <div class="hero-content">

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

        <div class="partners">
            <div class="partner">
                <img src="/crypto-school-logo.png" alt="Crypto School Logo">
            </div>

            <div class="partner">
                <img src="/banter-bubbles-icon.png" alt="Banter Bubbles Logo">
            </div>

            <div class="partner">
                <img src="/banter-capital.png" alt="Banter Logo Capital">
            </div>

            <div class="partner-discord">
                <img src="/discord-logo.png" alt="Discord Logo">
            </div>
        </div>

        <p class="section-footer">
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum <br />
            sociis natoque penatibus et magnis dis parturient montes, nascetur.
        </p>

        <div class="section-divider"></div>

    </div>

</section>

<style>
    .hero {
        position: relative;
        min-height: 100vh;

        /* add background image */
        background-image: url("/hero-bg-img.png");
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
        /*transform: scale(.85, 1);*/
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
        font-weight: 500;;

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

    .partner-discord img {
        height: 40px;
        margin-left: 20px;
        opacity: 0.8;
        transition: opacity 0.2s ease;
    }


    .partner img:hover {
        opacity: 1;
        cursor: pointer;
    }

    .partner-discord img:hover {
        opacity: 1;
        cursor: pointer;
    }

    /* divider */
    .partner:not(:last-child)::after {
        content: "";
        position: absolute;
        top: -25%;
        right: 0;
        height: 150%;
        width: 3px;
        /* create the pointed stroke look of template */
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

    .section-divider {
        width: 200%;
        margin-left: 400px;
        height: 3px;
        background: linear-gradient(
            to right,
            rgba(255, 255, 255, 0) 0%,
            rgba(255, 255, 255, 0.4) 50%,
            rgba(255, 255, 255, 0) 100%
        );
    }
</style>