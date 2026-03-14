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
            <img src="/crypto-school-logo.png" alt="Crypto School Logo" />
            <img src="/banter-bubbles-icon.png" alt="Banter Bubbles Logo" />
            <img src="/banter-capital.png" alt="Banter Logo Capital" />
            <img src="/discord-logo.png" alt="Discord Logo" />
        </div>

        <p class="section-footer">
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum <br />
            sociis natoque penatibus et magnis dis parturient montes, nascetur.
        </p>

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
        width: 100%;
        padding: 120px 8%;
        font-family: "Noyh Geometric", sans-serif;
    }

    .hero-content {
        max-width: 620px;
    }

    .hero-tag {
        background: red;
        padding: 4px 10px;
        font-size: 0.8rem;
        font-weight: 1000;
        border-radius: 7px 7px 0 7px;
    }

    .hero-subtag {
        margin-top: 8px;
        opacity: 0.7;
    }

    h1 {
        font-size: 4rem;
        font-weight: 800;
        margin: 20px;
        line-height: 1.1;        
    }

    .hero-description {
        opacity: 0.8;
        margin-bottom: 25px;
    }

    .hero-buttons {
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

    .partners {
        margin-top: 80px;
        display: flex;
        gap: 4px;
        align-items: center;
        opacity: 0.9;
    }

    .partners img {
        height: 90px;
        opacity: 0.8;
        transition: opacity 0.2s ease;
    }

    .partners img:hover {
        opacity: 1;
    }

    .section-footer {
        font-size: 19px;
        opacity: 0.6;
    }
</style>