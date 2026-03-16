<script>
    const { videoId = "", title = "", length = "" } = $props();

    let open = $state(false);

    function openVideo() {
        open = true;
    }

    function closeVideo() {
        open = false;
    }
</script>


<div class="video" onclick={openVideo}>
    <img src={`https://img.youtube.com/vi/${videoId}/maxresdefault.jpg`} alt={title} />
    <span class="length">{length}</span>
    <p>{title}</p>
</div>

{#if open}
    <div class="modal" onclick={closeVideo}> 
        <div class="modal-content" onclick={(e) => e.stopPropagation()}>
            <iframe
                width="900"
                height="506"
                src={`https://www.youtube.com/embed/${videoId}?autoplay=1`}
                title={title}
                frameborder="0"
                allow="autoplay; encrypted-media"
                allowfullscreen>
            </iframe>
        </div>
    </div>
{/if}

<style>
    .video {
        position: relative;
        cursor: pointer;
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
        font-family: "Noyh Geometric", sans-serif;
        font-size: 35px;
        margin-top: 10px;
    }

    .modal {
        position: fixed;
        inset: 0;
        background: rgba(0, 0, 0, 0.8);
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 999;
    }

    .modal-content {
        max-width: 90%;
    }
</style>