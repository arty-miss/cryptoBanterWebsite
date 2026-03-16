<script> 
    import StreamHeading from "$lib/components/ui/StreamHeading.svelte";
    import StreamThumbnail from "$lib/components/ui/StreamThumbnail.svelte";
    import StreamItem from "$lib/components/ui/StreamItem.svelte";
    import SubscribeButton from "$lib/components/ui/SubscribeButton.svelte";

    const streams = [
        {
            channel:"CHART HACKERS",
            video: {
            id: "5LbXeMK5-fg",
            title: "Crypto Live Trading | With Chart Hackers Team",
            length: "1:12:39"
            },
            items: [
            "DON'T WAIT! Powell Just FLIPPED Crypto Hard!",
            "Crypto Live Trading | Altcoin Trades You Can't Miss!",
            "PROTECT YOUR CRYPTO! Major 24 Hour Volatility!"
            ]
        },

        {
            channel: "CRYPTO BANTER",
            video: {
            id: "01F0611dlJo",
            title: "This $2.7B Whale Dump Just SHATTERED The Bitcoin Market Cycle!",
            length: "36:12"
            },
            items: [
            "Don't Let This Bitcoin TRAP Fool You! [HUGE Bounce Loading...]",
            "URGENT: Crypto FAILED The EXACT Level We Said... [Now This Is Next...]",
            "I've Got Inside Info On Trump's New Crypto! [$WLFI Launch]"
            ]
        },

        {
            channel: "247 CRYPTO LIVE",
            video: {
            id: "IDgMfFJgdP4",
            title: "WAIT! The U.S WON'T BUY Bitcoin! What It Means For Crypto",
            length: "21:34"
            },
            items: [
            "If You HATE Money, Ignore This Cypto Major Narrative! [I'm Buying]",
            "Crypto Banana Zone Is NOW! [Here's What I'm Buying]",
            "CRUCIAL CPI: CRYPTO WILL *UMP!! [Here's How I'm Trading It]"
            ]
        }
    ];
</script>

<section class="streams">

    <!-- blurred blue gradient at top right corner -->
    <div class="blue-blob"></div>

    <StreamHeading
    title="CRYPTO+ STREAMS"
    description="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa."
    />

    <div class="grid">

        {#each streams as stream}

            <div class="column">

                <div class="top">
                    <h3>{stream.channel}</h3>
                    <SubscribeButton/>
                </div>

                <StreamThumbnail
                    videoId={stream.video.id}
                    title={stream.video.title}
                    length={stream.video.length}
                />

                <div class="list">

                    {#each stream.items as item}
                        <StreamItem title={item}/>
                    {/each}

                </div>

            </div>

        {/each}

    </div>

    <button class="more">See More Streams</button>

</section>

<style>

    .streams {
        color: white;
        background: rgb(34, 34, 34);
        padding: 50px 40px;
        position: relative;
        overflow: hidden;
    }

    .blue-blob {
        position: absolute;
        right: -200px;
        top: -220px;

        width: 600px;
        height: 600px;

        background: radial-gradient(circle, rgb(97, 127, 193) 50%, rgba(255,80,160,0) 50%);
        filter: blur(120px);
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 40px;
        margin-top: 40px;
    }

    .top {
        font-family: "Roboto", sans-serif;
        font-size: 30px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 0;
    }

    .list {
        display: flex;
        flex-direction: column;
        gap: 10px;
        margin-top: 10px;
    }

    .more {
        margin: auto;
        margin-top: 50px;
        display: block;
        padding: 12px 20px;
        border-radius: 8px;
    }

</style>