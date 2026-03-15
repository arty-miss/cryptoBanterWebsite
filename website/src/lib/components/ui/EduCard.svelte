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
            <button class="learn-more">Learn More</button>
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

        margin-left: 50px;
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
    }

    .small-title-date {
        color: rgb(170, 170, 170);
        font-size: 14px;
    }

    h3 {
        margin: 8px 0;
    }

    .description {
        color: rgb(204, 204, 204);
        font-size: 14px;
    }

    .actions {
        margin-top: 16px;
        display: flex;
        gap: 12px;
    }

    .signup {
        padding: 10px 18px;
        border: 1px solid rgb(136, 136, 136);
        background: transparent;
        color: white;
        border-radius: 8px;
    }
</style>