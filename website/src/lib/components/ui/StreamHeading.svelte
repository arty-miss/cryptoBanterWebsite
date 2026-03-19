<!-- heading moved to separate file for less bloat in streams section, and made atomic -->

<script>
    const { title = "", description = ""} = $props();
</script>

<div class="heading">
    <h2>{title}</h2>
    <p>{description}</p>
</div>

<style>
    .heading {
        color: white;
        text-align: center;
        margin-top: 100px;
    }

    h2 {
        font-family: "Roboto", sans-serif;
        font-size: 50px;
        font-weight: 700;
        margin-bottom: 25px;
    }

    p {
        font-family: "Noyh Geometric", sans-serif;
        opacity: 0.75;
        max-width: 850px;
        margin: auto;
        font-size: 30px;
    }


    @media (max-width: 768px) {
        p {
            padding: 0 18px;
            font-size: 40px;
            height: auto;
        }

        .heading {
            margin-top: 55px;
        }
    }
</style>