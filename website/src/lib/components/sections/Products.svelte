<section class="content">

    <div class="text">

        <h1 class="title">
            Lorem ipsum dolor sit <br />
            amet, consectetuer
        </h1>

        <p class="description">
            Lorem ipsum dolor sit amet, consectetuer <br />
            adipiscing elit. Aenean commodo ligula eget <br />
            dolor. Aenean massa.
        </p>

        <button 
            class="banter-bubbles"
            onclick={() => window.open("https://play.google.com/store/apps/details?id=com.cryptobanter.banterbubbles&hl=en_ZA", "_blank")}
        >
        Get Banter Bubbles
        </button>

    </div>

    <div class="image">
        <img 
            src="/bubbles-feature-img.png" alt="product"
            onclick={() => window.open("https://play.google.com/store/apps/details?id=com.cryptobanter.banterbubbles&hl=en_ZA", "_blank")}
        />
    </div>

</section>

<style>
    .content {
        background: white;
        height: 800px;
        margin-top: 0;
        margin-bottom: 0;
        margin-left: 130px;
        display: flex;
        justify-content: space-between;
        align-items: flex-end;
        overflow: hidden;
    }

    h1 {
        font-family: "Roboto", sans-serif;
        font-size: 80px;
        font-weight: 500;
    }

    p {
        font-family: "Noyh Geometric", sans-serif;
        font-size: 40px;
    }

    .banter-bubbles {
        margin-bottom: 200px;
        margin-left: 50px;

        padding: 15px;
        border-radius: 20px;
        background: red;

        color: white;
        font-size: 20px;   
        
        border: none;
        outline: none;
        box-shadow: none;

        cursor: pointer;
        transition: all 0.25s ease-in-out;
    }

    .banter-bubbles:hover {
        transform: scale(1.15);
        box-shadow: 10px 5px 5px rgba(255, 0, 0, 0.404);
    }

    .image {
        margin-right: 130px;
        display: flex;
        align-items: flex-end;
        height: 100%;
    }

    .image img {
        transform: translate(0, 3px);
        height: 100%;
        transition: all 0.4s ease-in-out;
        cursor: pointer;
    }

    /* cool */
    .image img:hover {
        transform: rotate(-5deg) translate(0, 60px) scale(1.15);
    }

</style>