<script>
    import EduCard from "$lib/components/ui/EduCard.svelte";
    import Countdown from "$lib/components/ui/Countdown.svelte";

    const courses = [
        {
            logo: "/intro-to-crypto-logo.png",
            teacherImage: "/intro-to-crypto-hosts.png",
            smallTitle: "Intro to Crypto",
            date: "1PM, Sept 20, 2026",
            title: "LEARN CRYPTO IN 7 DAYS!",
            description: "Learn about Bitcoin, and how to start investing in crypto safely and confidently with this step-by-step guide.",
            link: "https://introtocrypto.cryptobanter.com/?source=homepage"
        },
        {
            logo: "/sniper-school-logo.png",
            teacherImage: "/sniper-school-host.png",
            smallTitle: "Sniper School",
            date: "9AM, Sept 18, 2026",
            title: "BUILD THE GAME PLAN TO YOUR FIRST $1M",
            description: "Learn Sheldon's 10-day trading system that took him to $1M in less than 7 days.",
            link: "https://sniperschool.cryptobanter.com/?source=homepage"
        },
        {
            logo: "/davidd-school-logo.png",
            teacherImage: "/daviddtech-school-host.png",
            smallTitle: "Daviddtech",
            date: "3PM, Oct 12, 2026",
            title: "CRYPTOCURRENCY AI TRADING",
            description: "Launch Bots That Trade 24/7 In Less Than 7 Days",
            link: "https://daviddtech.cryptobanter.com/?source=homepage"
        }
    ];

    let activeIndex = $state(0);

    // circular wrap around
    function prev() {
        activeIndex = (activeIndex - 1 + courses.length) % courses.length;
    }

    // circular wrap around
    function next() {
        activeIndex = (activeIndex + 1) % courses.length;
    }
</script>

<section class="education" id="education">

    <div class="section-divider"></div>

    <!-- blurred pink gradient at bottom left corner -->
    <div class="pink-blob"></div>

    <h1>TOP CRYPTO MASTERCLASSES</h1>
    <p>
        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo <br/>
        ligula eget dolor. Aenean massa.
    </p>

    <!-- desktop: show all 3 cards -->
    <div class="cards desktop-cards">
        {#each courses as course}
            <EduCard 
                logo={course.logo}
                teacherImage={course.teacherImage}
                smallTitle={course.smallTitle}
                date={course.date}
                title={course.title}
                description={course.description}
                link={course.link}
            >
                {#snippet timer()}
                    <Countdown />
                {/snippet}
            </EduCard>
        {/each}
    </div>

    <!-- mobile: one card at a time -->
    <div class="mobile-carousel">

        <button class="carousel-arrow-left" onclick={prev} aria-label="Previous"><span class="arrow">&#60;</span></button>

        <!-- only one card via its index -->
        <div class="carousel-card">
            <EduCard
                logo={courses[activeIndex].logo}
                teacherImage={courses[activeIndex].teacherImage}
                smallTitle={courses[activeIndex].smallTitle}
                date={courses[activeIndex].date}
                title={courses[activeIndex].title}
                description={courses[activeIndex].description}
                link={courses[activeIndex].link}
            >
                {#snippet timer()}
                    <Countdown />
                {/snippet}
            </EduCard>
        </div>

        <button class="carousel-arrow-right" onclick={next} aria-label="Previous"><span class="arrow">&#62;</span></button>
    </div>

    <!--
    dot indicators for mobile 
    loop through courses and render dots
    -->
    <div class="carousel-dots">
        {#each courses as _, i}
            <button
                class="dot {i === activeIndex ? 'active' : ''}"
                onclick={() => activeIndex = i}
                aria-label="Go to slide {i + 1}"
            ></button>
        {/each}
    </div>

</section>

<style>
    .section-divider {
        transform: translate(0, -70px);
        width: 30%;
        margin-left: 690px;
        height: 1px;
        filter: blur(1.5px);
        background: linear-gradient(
            to right,
            rgba(255, 255, 255, 0) 0%,
            rgba(255, 255, 255, 0.4) 50%,
            rgba(255, 255, 255, 0) 100%
        );
    }

    .education {
        position: relative;
        background: rgba(39, 39, 39);
        padding: 80px 0;
        text-align: center;
        z-index: 1;
        overflow: hidden;
    }

    .pink-blob {
        position: absolute;
        left: -200px;
        bottom: -220px;
        width: 600px;
        height: 600px;
        background: radial-gradient(circle, rgba(217, 33, 107, 1) 100%, rgba(255,80,160,0) 100%);
        filter: blur(120px);
        z-index: -3;
    }

    h1 {
        font-family: "Roboto", sans-serif;
        color: white;
        font-size: 50px;
    }

    p {
        font-family: "Noyh Geometric", sans-serif;
        color: white;
        opacity: 0.8;
        font-size: 25px;
    }

    /* desktop cards */
    .cards {
        margin-top: 60px;
        display: flex;
        justify-content: center;
        gap: 40px;
        align-items: flex-end;
    }

        @media (min-width: 769px) {
        .cards :global(.card-container) {
            flex: 1;
            max-width: 500px;
        }

        .cards :global(.card-container:nth-child(2)) {
            max-width: 580px;
        }

        .cards :global(.card-container:nth-child(3)) {
            max-width: 465px;
        }

        .cards :global(.card-container:nth-child(2) .actions) {
            transform: translate(0, 20px);
        }

        .cards :global(.card-container:last-child .actions) {
            transform: translate(0, 20px);
        }
    }

    /* mobile carousel */
    .mobile-carousel {
        display: none;
    }

    .carousel-dots {
        display: none;
    }

    @media (max-width: 768px) {

        h1 {
            font-size: 28px;
            padding: 0 20px;
        }

        p {
            font-size: 16px;
            padding: 0 20px;
        }

        p br {
            display: none;
        }

        .desktop-cards {
            display: none;
        }

        .mobile-carousel {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 12px;
            margin-top: 40px;
            padding: 0 8px;
        }

        .carousel-card {
            flex: 1;
            min-width: 0;
        }

        .arrow {
            font-family: "Times New Roman", sans-serif;
            font-weight: 1000;
            transform: scaleY(9);
        }

        .carousel-arrow-left {
            flex-shrink: 0;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: white;
            font-size: 20px;
            width: 36px;
            height: 400px;
            border-radius: 30px 7px 7px 30px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background 0.2s ease;
            align-self: center;
            margin-bottom: 300px; /* vertically centres against the card image area */
        }

        .carousel-arrow-right {
            flex-shrink: 0;
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: white;
            font-size: 20px;
            width: 36px;
            height: 400px;
            border-radius: 7px 30px 30px 7px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background 0.2s ease;
            align-self: center;
            margin-bottom: 300px; /* vertically centres against the card image area */
        }

        .carousel-arrow-left:hover, .carousel-arrow-right:hover {
            background: rgba(255, 255, 255, 0.25);
        }

        /*dot indicators */
        .carousel-dots {
            display: flex;
            justify-content: center;
            gap: 8px;
            margin-top: 24px;
        }

        .dot {
            width: 28px;
            height: 4px;
            border-radius: 2px;
            border: none;
            background: rgba(255, 255, 255, 0.3);
            cursor: pointer;
            padding: 0;
            transition: background 0.2s ease, width 0.2s ease;
        }

        .dot.active {
            background: red;
            width: 48px;
        }
    }
</style>