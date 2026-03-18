<script>
    const {title = ""} = $props();
</script>

<div class="newsletter">

    <div>
        <img src="/newsletter-signup-icon.png" alt="newsletter icon" />
    </div>

    <div class="content">
        <div class="title">{title}</div>
        <div class="signup">Sign Up</div>
    </div>
</div>

<style>
    .newsletter {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 25px;
        width: 250px;
        display: flex;
        align-items: center;
        gap: 16px;

        padding: 18px;
        border-radius: 16px;

        border: 1px solid rgba(255,255,255,0.08);
        background: rgba(255,255,255,0.02);

        cursor: pointer;
        transition: all 0.2s;
    }

    .newsletter:hover {
        background: rgba(255,255,255,0.05);
    }

    img {
        background: linear-gradient(30deg, rgb(104, 104, 104) 0%, rgba(104, 104, 104, 0) 100%);
        border-radius: 10px;
        width: 45px;
        height: 45px;
    }

    .title {
        font-weight: 600;
    }

    .signup {
        font-size: 20px;
        opacity: 0.7;
    }

    @media (max-width: 768px) {
        .newsletter {
            font-size: 30px;
            width: 340px;
            padding: 15px;
        }

        img {
            width: 85px;
            height: 85px;
        }
    }
</style>