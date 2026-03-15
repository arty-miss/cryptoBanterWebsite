<script> 
    import StreamHeading from "$lib/components/ui/StreamHeading.svelte";
    import StreamThumbnail from "$lib/components/ui/StreamThumbnail.svelte";
    import StreamItem from "$lib/components/ui/StreamItem.svelte";
    import SubscribeButton from "$lib/components/ui/SubscribeButton.svelte";

    const streams = [
        {
            channel:"CHART HACKERS",
            video: {
            id: "VIDEO_ID_1",
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
            id: "VIDEO_ID_2",
            title: "This $2.7B Whale Dump Just SHATTERED The Bitcoin Market Cycle!",
            duration: "36:12"
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
            id: "VIDEO_ID_3",
            title: "WAIT! The U.S WON'T BUY Bitcoin! What It Means For Crypto",
            duration: "21:34"
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

    <StreamHeading
    title="CRYPTO+ STREAMS"
    description="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor."
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
        padding: 50px 40px;
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
    }

</style>