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
        border-radius: 15px;

        cursor: pointer;
        /* fade out slowly */
        transition: all 0.5s ease-in-out;
    }

    /* white highlight when hovering over item */
    .nav-item:hover {
        /* fade in quickly */
        transition: all 0.21s ease-in-out;
        background: rgba(255, 255, 255, 0.2);
    }

    img {
        width: 30px;
        height: 30px;
    }

    span {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 20px;
        color: white
    }
</style>