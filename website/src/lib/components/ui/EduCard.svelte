<script>
    const { logo = "", teacherImage = "", smallTitle = "", date = "", title = "", description = ""} = $props();
</script>

<div class="card-container">
    <div class="card">
    <div class="image-wrapper">
        <img class="teacher" src={teacherImage} alt="teacher" />

        <div class="free-badge">AVAILABLE FOR FREE</div>

        <div class="logo">
            <img src={logo} alt="company logo" />
        </div>

        <div class="timer">
            <slot name="timer" />
        </div>
    </div>
</div>

    <div class="content">
        <p class="small-title-date">{smallTitle} | {date}</p>
        <h3>{title}</h3>
        <p class="description">{description}</p>

        <div class="actions">
            <button class="signup">Sign Up</button>
            <a href="/">Learn More</a>
        </div>
    </div>
</div>


<style>

.card-container {
    display: flex;
    flex-direction: column;
}

    .card {
        width: 100%;
        border-radius: 35px;
        overflow: hidden;
        background: rgba(255, 255, 255, 0.1);
        transition:  transform .25s ease;
    }

    .card:hover {
        transform: scale(1.05);
    }

    .image-wrapper {
        position: relative;
    }

    .teacher {
        margin-left: 58px;
        width: 90%;
        height: auto;
        display: block;
    }

    .free-badge {
        font-family: "Roboto", sans-serif;
        position: absolute;
        top: 30px;
        left: 30px;
        background: red;
        color: white;
        font-size: 16px;
        padding: 6px 10px;
        border-radius: 6px 6px 0 6px;
    }

    .logo {
        position: absolute;
        height: 200px;
        top: 35%;
        left: 20px;
    }

    .logo img {
        height: auto;
    }

    .timer {
        position: absolute;
        bottom: 16px;
        left: 20px;
    }

    .content {
        padding: 20px;
        text-align: left;
    }

    .small-title-date {
        color: rgb(170, 170, 170);
        font-size: 14px;
    }

    h3 {
        color: white;
        font-size: 23px;
        margin-bottom: 40px;
    }

    .description {
        color: rgb(204, 204, 204);
        font-size: 14px;
        margin-bottom: 50px;
    }

    .actions {
        margin-top: 16px;
        display: flex;
        gap: 12px;
        font-family: "Noyh Geometric", sans-serif;
    }

    .actions a {
        color: white;
        margin-top: 13px;
        margin-left: 11px;
        text-decoration: none;
        font-weight: 1000;
        font-size: 20px;

        transition: all 0.25s ease-in-out;
        transform: scale(1);
    }

    .actions a:hover {
        transform: scale(1.15);
    }

    .signup {
        z-index: 2;
        padding: 12px 22px;
        border: 2px solid white;
        background: transparent;
        color: white;
        border-radius: 6px;

        font-size: 15px;
        font-weight: 500;;

        cursor: pointer;
        transition: all 0.25s ease-in-out;
    }

    .signup:hover {
        background: white;
        color: black;
    }


</style>