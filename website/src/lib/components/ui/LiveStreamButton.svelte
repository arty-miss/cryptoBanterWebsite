<!-- found at top right of page, on navbar-->

<div class="live">
    <div class="dot"></div> <!-- red dot icon -->
    <span>Live Streams</span>
</div>

<style>
    .live {
        display: flex;
        align-items: center;
        gap: 10px;

        padding: 10px 16px;

        background: white;
        /* bottom right corner is not soft like the rest */
        border-radius: 12px 12px 0 12px;

        font-weight: 500;
        cursor: pointer;
    }


    .dot {
        width: 10px;
        height: 10px;

        background: red;
        border-radius: 50%;
    }

    span {
        /* text colour */
        color: black;
    }
</style>