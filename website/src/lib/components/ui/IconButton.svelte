<!-- reused social media icons for footer -->

<script>
    const { src = "", alt = "", size = 45, circle = true, link = "" } = $props();
</script>

<div
    class="icon"
    style="width:{size}px;height:{size}px"
    class:circle
>
    <a href={link} target="_blank" rel="noopener noreferrer" class="partner">
        <img src={src} alt={alt} />
    </a>
</div>

<style>
    .icon {
        display: flex;
        align-items: center;
        justify-content: center;

        cursor: pointer;
        transition: all 0.35s ease-in-out;
    }

    .icon:hover {
        transform: scale(1.15) rotate(360deg);
        background: white;
    }

    .icon img {
        display: block;
        transform: scale(1.2);
    }

    .partner {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .circle {
        border-radius: 50%;
        background: rgba(185, 185, 185);
    }
</style>