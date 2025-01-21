
<script lang="ts">
import img1 from '$lib/assets/custom/img-1.png';
import img2 from '$lib/assets/custom/img-2.png';
// Import images from different folders
    const mobileSvgModules = import.meta.glob('$lib/assets/mobilesvg/*.svg', { eager: true });
    const mobilePngModules = import.meta.glob('$lib/assets/mobilepng/*.png', { eager: true });
    const desktopPngModules = import.meta.glob('$lib/assets/desktoppng/*.png', { eager: true });
    const desktopSvgModules = import.meta.glob('$lib/assets/desktopsvg/*.svg', { eager: true });

    // Extract image URLs for each category
    const mobileSvgImages = Object.values(mobileSvgModules).map((module: any) => module.default);
    const mobilePngImages = Object.values(mobilePngModules).map((module: any) => module.default);
    const desktopPngImages = Object.values(desktopPngModules).map((module: any) => module.default);
    const desktopSvgImages = Object.values(desktopSvgModules).map((module: any) => module.default);
</script>

<div>
    <h1 class="text-lg font-semibold py-2">Mobilesvg</h1>
    <div class="w-full flex  items-center gap-2 justify-between overflow-x-auto menu-container scrollbar-hidden snap-x scroll-smooth">
        {#each mobileSvgImages as image}
            <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={image} alt="mobilesvg" />
        {/each}
    </div>
</div>

<div>
    <h1 class="text-lg font-semibold py-2">Mobilepng</h1>
    <div class="w-full flex  items-center gap-2 justify-between overflow-x-auto menu-container scrollbar-hidden snap-x scroll-smooth">
        {#each mobilePngImages as image}
            <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={image} alt="mobilepng" />
        {/each}
    </div>
</div>

<div>
    <h1 class="text-lg font-semibold py-2">Desktopsvg</h1>
    <div class="w-full flex  items-center gap-2 justify-between overflow-x-auto menu-container scrollbar-hidden snap-x scroll-smooth">
        {#each desktopSvgImages as image}
            <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={image} alt="desktopsvg" />
        {/each}
    </div>
</div>

<div>
    <h1  class="text-lg font-semibold py-2">Desktoppng</h1>
    <div class="w-full flex  items-center gap-2 justify-between overflow-x-auto menu-container scrollbar-hidden snap-x scroll-smooth">
        {#each desktopPngImages as image}
            <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={image} alt="desktoppng" />
        {/each}
    </div>
</div>
<div>
    <h1  class="text-lg font-semibold py-2">Custom images</h1>
    <div class="w-full flex  items-center gap-2  overflow-x-auto menu-container scrollbar-hidden snap-x scroll-smooth">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img1} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img2} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img1} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img2} alt=""><img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img1} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img2} alt=""><img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img1} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img2} alt=""><img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img1} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img2} alt=""><img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img1} alt="">
        <img class="h-[35px] md:w-[120px] md:h-[45px]  lg:w-[168px] lg:h-[64px] menu-t snap-start" src={img2} alt="">
    </div>
</div>
