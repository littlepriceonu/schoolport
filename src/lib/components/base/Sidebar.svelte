<script lang="ts">
    import Showcase from "./Showcase.svelte";

    let showcase = false
    let showcaseKind: "videos" | "images"

</script>

<div class="w-full h-full overflow-hidden flex flex-col">
    <h1 class="text-right text-4xl sm:text-6xl pr-6 font-mono text-white font-bold">PROJECTS</h1>
    <div class="w-full h-[40%] sm:h-[35%] pt-2 pr-6 flex flex-col items-end ">
        <h1 class="text-right text-white font-mono font-bold text-2xl sm:text-5xl">
            VIDEOS
        </h1>


        <button on:click={()=>{showcase = true; showcaseKind = "videos"}} class="backdrop-invert w-56 h-72 border transition-all duration-500 ease-in-out flex items-center justify-center border-neutral-700 bg-black bg-opacity-40 hover:scale-[1.02] active:scale-95 backdrop-blur-2xl rounded-md text-white font-semibold">
            Click To Showcase Videos
        </button>
    </div>
    
    <div class="w-full h-1/2 pr-6 pt-2 flex flex-col items-end justify-center">
        <h1 class="text-right text-white font-mono font-bold text-2xl sm:text-5xl">
            IMAGES
        </h1>

        <button on:click={()=>{showcase = true; showcaseKind = "images"}} class="backdrop-invert w-56 h-72 border transition-all duration-500 ease-in-out flex items-center justify-center border-neutral-700 bg-black bg-opacity-40 hover:scale-[1.02] active:scale-95 backdrop-blur-2xl rounded-md text-white font-semibold">
            Click To Showcase Images
        </button>

    </div>

    
    <h2 class="text-right pr-6 text-white mt-auto text-sm sm:text-lg font-semibold">
        PORTFOLIO - MEDIA ARTS 9/10  BLOCK C
    </h2>
</div>

<Showcase bind:show={showcase} kind={showcaseKind}/>