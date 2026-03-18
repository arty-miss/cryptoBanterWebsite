<script>
    const { days = "03", hours = "22", minutes = "09", seconds = "32" } = $props();
</script>

<div class="big-border">
    <span class="next">NEXT MASTERCLASS</span>
    <div class="time">
        <span>{days}</span>
        <span>{hours}</span>
        <span>{minutes}</span>
        <span>{seconds}</span>
    </div>
    <div class="units">
        <span>DAYS</span>
        <span>HRS</span>
        <span>MIN</span>
        <span>SEC</span>
    </div>
</div>

<style>

    .big-border {
        transform: scale(1.25) translate(25px, -10px);
        width: 175px;
        border-radius: 50px;

        background: radial-gradient(circle, rgba(255,255,255,0) 40%, rgba(255,255,255,1) 300%);
        backdrop-filter: blur(3px);

        font-family: "Roboto", sans-serif;

        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .next {
        margin-top: 4px;
        color: white;
        font-size: 8px;
        line-height: 2;
    }

    .time {
        font-family: "Noyh Geometric", sans-serif;
        color: white;
        display: flex;
        gap: 12px;
        font-size: 25px;
        line-height: 1;
    }

    .units {
        padding-bottom: 5px;
        color: white;
        display: flex;
        gap: 19px;
        font-size: 8px;
    }

    @media (max-width: 768px) {
        .big-border {
            transform: scale(2) translate(60px, -30px);
        }
    }
</style>