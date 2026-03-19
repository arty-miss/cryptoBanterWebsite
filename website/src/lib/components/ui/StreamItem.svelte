<!-- reused list element visible on desktop version of streams section -->

<script>
    const { title = ""} = $props();
</script>

<div class="item">
<!-- &nbsp; is a non-breaking space -->
    ▶ &nbsp; {title}
</div>

<style>
    .item {
        font-family: 'Noyh Geometric', sans-serif;
        text-align: center;
        padding: 15px;
        border-radius: 20px 20px 0 0;
        background: linear-gradient(rgb(51, 51, 51),rgb(0, 0, 0));
        font-size: 23px;

        line-height: 1.2;
        /* 2 lines * line-height + top+bottom padding (20+20) */
        height: calc(2 * 1.2em + 40px); 
        display: flex;
        align-items: center; 
        justify-content: center;      

        cursor: pointer;
        transition: all 0.15s ease-in-out;
    }

    .item:hover {
        background: red;
        border-radius: 20px 20px 0 20px;
    }
</style>