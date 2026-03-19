<!-- found at top right of page, on navbar-->

<div class="live">
    <!-- red dot icon -->
    <div class="dot"></div>
    <!-- dedicated link -->
    <a href="#streams">Live Streams</a>
</div>

<style>
    .live {
        display: flex;
        align-items: center;
        gap: 7px;

        padding: 10px 18px;

        background: white;
        /* bottom right corner is not soft like the rest */
        border-radius: 10px 10px 0 10px;

        font-weight: 500;
        cursor: pointer;

        /* ensure smooth transition without flickering by already scaling to 1 */
        transform: scale(1);
        transition: all 0.2s ease-in-out;
    }

    .live:hover {
        transform: scale(1.05);
    }


    .dot {
        width: 17px;
        height: 17px;

        background: red;
        border-radius: 50%;
        /* prevent flickering */
        transform: scale(1);
        transition: all 0.2s ease-in-out;
    }

    a {
        /* text colour */
        color: black;
        font-family: "Noyh Geometric", sans-serif;
        font-size: 20px;

        transform: scale(1);
        transition: all 0.2s ease-in-out;
        text-decoration: none;
    }
</style>