<script>
    const { days = 3, hours = 22, minutes = 9, seconds = 32 } = $props();
</script>

<span class="next">NEXT MASTERCLASS</span>
<div class="countdown">
    <span>{days}DAYS</span>
    <span>{hours}HRS</span>
    <span>{minutes}MIN</span>
    <span>{seconds}SEC</span>
</div>

<style>
    .next {
        color: white;
    }
    .countdown {
        color: white;
        display: flex;
        gap: 8px;
        background: rgba(0, 0, 0, 0.6);
        padding: 8px 12px;
        font-size: 12px;
    }
</style>