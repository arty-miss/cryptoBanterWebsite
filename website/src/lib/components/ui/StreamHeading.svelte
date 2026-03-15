<script>
    const { title = "", description = ""} = $props();
</script>

<div class="heading">
    <h2>{title}</h2>
    <p>{description}</p>
</div>

<style>
    .heading {
        text-align: center;
        margin-bottom: 5px;
    }

    h2 {
        font-size: 25px;
        font-weight: 700;
    }

    p {
        opacity: 0.7;
        max-width: 600px;
        margin: auto;
    }
</style>