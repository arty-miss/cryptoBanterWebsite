<!-- youtube video thumbnails that are clickable and open in a popup -->

<script>
    const { videoId = "", title = ""} = $props();

    let open = $state(false);

    function openVideo() {
        open = true;
    }

    function closeVideo() {
        open = false;
    }
</script>

<!-- thumbnail image -->
<div class="video" onclick={openVideo}>
    <img src={`https://img.youtube.com/vi/${videoId}/maxresdefault.jpg`} alt={title} />
</div>

<p class="title">{title}</p>

<!-- open popup when clicking on thumbnail-->
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
        border-radius: 25px;
        position: relative;
        cursor: pointer;
        transition: all 0.25s ease-in-out;
        overflow: hidden;
    }

    /* cool shine animation - https://www.youtube.com/watch?v=bukHY2N3ips */
    .video::before {
        content: "";
        position: absolute;
        top: 0;
        left: -75%;
        width: 50%;
        height: 100%;

        background: linear-gradient(
            120deg,
            transparent,
            rgba(255, 255, 255, 0.35),
            transparent
        );

        transform: skewX(-25deg);
    }

    .video:hover::before {
        animation: shine 0.8s ease;
    }

    @keyframes shine {
        100% {
            left: 125%;
        }
    }

    img {
        width: 100%;
    }

    p {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 35px;
        margin-top: 10px;
        line-height: 1.2;
        height: 75px;
        overflow: hidden;
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