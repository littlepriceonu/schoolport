<script lang='ts'>
    import {page} from '$app/stores';
</script>

<div class="w-full h-full bg-black text-white flex flex-col items-center justify-center">
    <a href="/" class="hover:underline text-blue-500 font-mono text-5xl font-semibold">
        Woops
    </a>

    <p>
        {$page.status}: {$page.error?.message}
    </p>
</div>