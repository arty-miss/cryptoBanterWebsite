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
            description: "Learn about Bitcoin, and how to start investing in crypto safely and confidently with this step-by-step guide."
        },
        {
            logo: "/sniper-school-logo.png",
            teacherImage: "/sniper-school-host.png",
            smallTitle: "Sniper School",
            date: "9AM, Sept 18, 2026",
            title: "BUILD THE GAME PLAN TO YOUR FIRST $IM",
            description: "Learn about Bitcoin, and how to start investing in crypto safely and confidently with this step-by-step guide."
        },
        {
            logo: "/davidd-school-logo.png",
            teacherImage: "/daviddtech-school-host.png",
            smallTitle: "Daviddtech",
            date: "3PM, Oct 12, 2026",
            title: "CRYPTOCURRENCY AI TRADING",
            description: "Launch Bots That Trade 24/7 In Less Than 7 Days"
        }
    ];
</script>

<section class="education">

    <div class="section-divider"></div>

    <!-- blurred pink gradient at bottom left corner -->
    <div class="pink-blob"></div>

    <h1>TOP CRYPTO MASTERCLASSES</h1>
    <p>
        Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo <br/>
        ligula eget dolor. Aenean massa.
    </p>

    <div class="cards">
        {#each courses as course}
            <EduCard 
            logo={course.logo}
            teacherImage={course.teacherImage}
            smallTitle={course.smallTitle}
            date={course.date}
            title={course.title}
            description={course.description}
            >
            <Countdown slot="timer"/>
            </EduCard>
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

        background: radial-gradient(circle, rgba(255,80,160,0.45) 0%, rgba(255,80,160,0) 70%);
        filter: blur(120px);

        z-index: 0;
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

    .cards {
        margin-top: 60px;
        display: flex;
        justify-content: center;
        gap: 40px;
        /* cards are aligned at the bottom and not top */
        align-items: flex-end;
    }

    /* change card size */
    .cards :global(.card-container) {
        flex: 1;
        max-width: 500px;
    }

    /* middle card bigger */
    .cards :global(.card-container:nth-child(2)) {
        max-width: 580px;    
    }

    .cards :global(.card-container:nth-child(3)) {
        max-width: 465px;    
        transform: translate(0, -20px);
    }

    /* move last card's buttons down */
    .cards :global(.card-container:last-child .actions) {
        transform: translate(0, 20px);
    }
</style>