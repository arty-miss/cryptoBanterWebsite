<script>
    const { title = ""} = $props();
</script>

<div class="item">
    ▶ {title}
</div>

<style>
    .item {
        padding: 12px;
        border-radius: 8px;
        background: linear-gradient(rgb(28, 28, 28),rgb(17, 17, 17));
        font-size: 12px;
    }

    .item:hover {
        background: red;
    }
</style>