<script lang="ts">
    import Sidebar from './../lib/components/base/Sidebar.svelte';
</script>

<svelte:head>
    <title>
        Portfolio
    </title>
</svelte:head>

<div class="w-full h-full flex">
    <div class="flex items-center justify-center w-full h-full absolute left-0 top-0 overflow-hidden">
        <img src="/imgs/Render.png" alt="Blender 3D Render" class="h-full w-full object-cover">
    </div>

    <div class="w-1/4 h-full flex flex-col items-center justify-center z-10">
        <div class="backdrop-invert w-full h-[90%] mask ml-12 sm:ml-24"/>
    </div>

    <div class="w-3/4 h-full z-10">
        <Sidebar />
    </div>
</div>

<style lang="postcss">
    .vertical {
        writing-mode: vertical-rl;
        text-orientation: upright;
    }

    .mask {
        mask: url('/masks/lp.svg') no-repeat;
    }
</style>