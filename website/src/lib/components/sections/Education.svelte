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
            logo: "/sniper-school-host.png",
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
    <h2>TOP CRYPTO MASTERCLASSES</h2>

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