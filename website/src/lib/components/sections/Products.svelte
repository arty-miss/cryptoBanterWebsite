<!-- ad section that showcases banter bubbles app -->

<section class="content" id="products">

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

        padding: 15px;
        border-radius: 20px;
        background: red;
        overflow: visible !important;

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
        overflow: visible !important;
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

    @media (max-width: 768px) {
        .content {
            flex-direction: column-reverse;  
            align-items: center;
            height: auto;
            margin-left: 0;
            padding: 80px 24px 80px;
            overflow: visible;
        }

        .text {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }

        h1 {
            font-size: 47px;
            font-weight: 800;
            line-height: 1.15;
            margin-bottom: -10px;
        }

        h1 br { display: none; }

        p {
            font-weight: 100;
            font-size: 42px;
            line-height: 1.5;
            opacity: 0.6;
        }

        p br { display: none; }

        .banter-bubbles {
            margin-bottom: 0;
            margin-left: 0;
            margin-top: 15px;
            width: 49%;
            padding: 30px 18px;
            border-radius: 14px;
            font-size: 27px;
            font-weight: 500;
        }

        .image {
            margin-right: 0;
            height: auto;
            width: 80%;
            max-width: 320px;
            justify-content: center;
            margin-bottom: 32px;
        }

        .image img {
            height: 450px;
            transform: none;
        }

        /* disable hover tilt on mobile */
        .image img:hover {
            transform: none;
        }
    }

</style>