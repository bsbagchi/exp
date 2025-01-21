<script lang="ts">
    export let title: string;
    export let images: string[];
</script>

<div>
    <h1 class="text-lg font-semibold py-2">{title}</h1>
    <div class="w-full flex items-center gap-2 justify-between overflow-x-auto menu-container scrollbar-hidden snap-x scroll-smooth">
        {#each images as image}
            <img class="h-[35px] md:w-[120px] md:h-[45px] lg:w-[168px] lg:h-[64px] menu-t snap-start" src={image} alt={title} />
        {/each}
    </div>
</div> 