<script>
    const { icon = "", label = ""} = $props();
</script>

<!-- all nav items look the same so it's just a matter of setting the image and text-->

<div class="nav-item">
    <img src={icon} alt={label} />
    <span>{label}</span>
</div>


<!-- css styling -->
<style>
    .nav-item {
        display: flex;
        align-items: center;
        gap: 8px;

        padding: 10px 14px;
        border-radius: 12px;

        cursor: pointer;
        transition: all 0.2s ease;
    }

    /* white highlight when hovering over item */
    .nav-item:hover {
        background: rgba(255, 255, 255, 0.08);
        border: 1px solid rgba(255, 255, 255, 0.15)
    }

    img {
        width: 18px;
        height: 18px;
    }

    span {
        font-size: 14px;
        color: white
    }
</style>