<script>
    const { src = "", alt = "", size = 45, circle = true} = $props();
</script>

<div
    class="icon"
    style="width:{size}px;height:{size}px"
    class:circle
>
    <img src={src} alt={alt} />
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
        width: 55%;
        height: 55%;
        object-fit: contain;
    }

    .circle {
        border-radius: 50%;
        background: rgba(185, 185, 185);
    }
</style>