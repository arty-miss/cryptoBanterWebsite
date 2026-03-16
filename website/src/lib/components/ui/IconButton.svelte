<script>
    const { src = "", alt = "", size = 40, circle = true} = $props();
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
    }

    .icon img {
        width: 55%;
        height: 55%;
        object-fit: contain;
    }

    .circle {
        border-radius: 50%;
        background: rgba(255,255,255,0.08);
    }
</style>