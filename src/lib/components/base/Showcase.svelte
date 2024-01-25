<script lang="ts">
    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import '@splidejs/svelte-splide/css';

    const images = [
        '/imgs/PhotoshopChallenge/Zoom In.png', '/imgs/PhotoshopChallenge/Unit.png', '/imgs/PhotoshopChallenge/HOPE.png', '/imgs/PhotoshopChallenge/BEAST OF THE CENTURY.png', '/imgs/PhotoshopChallenge/AWAKEN THE BEAST.png',
        '/imgs/The Mon(k)ey.png',
        '/imgs/Restraunt/Meat Masters Logo.png', '/imgs/Restraunt/Meat Masters Menu.png', '/imgs/Restraunt/Meat Masters Instagram Post.png'
    ]

    const videos = [
        '/videos/BBB [EXTRA FINAL].mp4', '/videos/News Report.mp4'
    ]

    export let show = false 
    export let kind: "videos" | "images" 

</script>

<div class="w-full h-full absolute top-0 left-0 flex flex-col items-center justify-center bg-black bg-opacity-40 backdrop-blur-2xl" style="opacity: {show ? "1" : "0"}; pointer-events: {show ? "auto" : "none"}">
    <div class="absolute w-full h-[10%] sm:h-[5%] flex items-center justify-end px-6 top-0">
        <p class="mr-auto text-white text-lg font-semibold font-mono">
            {kind}
        </p>
        
        <button on:click={()=>{show = false;}} class="text-4xl  scale-x-125 z-10 transition-all duration-500 ease-in-out text-red-600 hover:text-red-800">
            X
        </button>
    </div>

    {#if kind == "images"}
        <Splide options={{rewind: true, arrows: true, autoplay: true, interval: 3500, pagination: false}} class="h-full w-full flex items-center justify-center">
            {#each images as image}
                <SplideSlide class="flex items-center justify-center">
                    <img src="{image}" alt="One of my project's works." class='w-[80%] sm:w-[70%] md:w-[52.5%] lg:w-[35%] xl:w-[25%] 2xl:w-[30%] transition-all duration-500 ease-in-out'>
                </SplideSlide>
            {/each}
        </Splide>
    {:else}


        <Splide options={{rewind: true, arrows: true, autoplay: true, interval: 3500, pagination: false}} class="h-full w-full flex items-center justify-center">
            {#each videos as video}
                <SplideSlide class="flex items-center justify-center">
                    <!-- svelte-ignore a11y-media-has-caption -->
                    <video class="w-[80%] sm:w-[70%] md:w-[52.5%] lg:w-[35%] xl:w-[25%]" src="{video}" controls playsinline></video>
                </SplideSlide>
            {/each}
        </Splide>

    {/if}
</div>