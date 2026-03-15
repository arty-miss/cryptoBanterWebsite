<script>
    const { videoId = "", title = "", length = "" } = $props();
</script>

<div class="video">
    <img src={`https://img.youtube.com/vi/${videoId}/maxresdefault.jpg`} alt={title} />
    <span class="length">{length}</span>
    <p>{title}</p>
</div>

<style>
    .video {
        position: relative;
    }

    img {
        width: 100%;
        border-radius: 10px;
    }

    .length {
        position: absolute;
        bottom: 8px;
        right: 8px;
        background: black;
        color: white;
        padding: 3px 6px;
        font-size: 12px;
        border-radius: 4px;
    }

    p {
        margin-top: 10px;
    }
</style>