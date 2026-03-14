<script>
    const { teacherImage = "", logo = "", title = "", description = "", date = ""} = $props();
</script>

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


    <div class="content">
        <p class="date">{date}</p>
        <h3>{title}</h3>
        <p class="description">{description}</p>

        <div class="actions">
            <button class="signup">Sign Up</button>
            <button class="learn-more">Learn More</button>
        </div>
    </div>
</div>

<style>

    .card {
        width: 360px;
        border-radius: 20px;
        overflow: hidden;
        background: #1c1c1c;
        transition:  transform .25 ease;
    }

    card:hover {
        transform: scale(1.05);
    }

    .image-wrapper {
        position: relative;
    }

    .teacher {
        width: 100%;
        display: block;
    }

    .free-badge {
        position: absolute;
        top: 16px;
        left: 16px;
        background: red;
        color: white;
        font-size: 12px;
        padding: 6px 10px;
        border-radius: 6px;
    }

    .logo {
        position: absolute;
        top: 50%;
        left: 20px;
    }

    .logo img {
        height: 40px;
    }

    .timer {
        position: absolute;
        bottom: 16px;
        left: 20px;
    }

    .content {
        padding: 20px;
    }

    .date {
        color: #aaa;
        font-size: 14px;
    }

    h3 {
        margin: 8px 0;
    }

    .description {
        color: #ccc;
        font-size: 14px;
    }

    .actions {
        margin-top: 16px;
        display: flex;
        gap: 12px;
    }

    .signup {
        padding: 10px 18px;
        border: 1px solid #888;
        background: transparent;
        color: white;
        border-radius: 8px;
    }
</style>