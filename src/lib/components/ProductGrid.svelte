<script lang="ts">
    import ProductCard from './ProductCard.svelte';

    const products = [
        {
            badge: "Signature",
            code: "CT",
            title: "Contrast Therapy",
            image: "/generated/image-person-in-guided-ice-bath-with-peaceful--1766714812512-1.webp", 
            price: "₱2,500"
        },
        {
            badge: "Popular",
            code: "IR",
            title: "Infrared Sauna",
            image: "/generated/image-infrared-sauna-room-with-warm-amber-ligh-1766714815448-2.webp", 
            price: "₱2,000"
        },
        {
            badge: "Advanced",
            code: "HBO",
            title: "Hyperbaric Oxygen",
            image: "/generated/image-modern-hyperbaric-oxygen-chamber-in-clea-1766714818482-3.webp",
            price: "₱4,500"
        },
        {
            badge: "Wellness",
            code: "IV",
            title: "IV Therapy",
            image: "/generated/image-iv-therapy-session-in-private-luxury-roo-1766714821265-4.webp",
            price: "₱3,500"
        }
    ];
</script>

<section class="bg-gray-950 py-24">
    <div class="container mx-auto px-6 md:px-12">
        <div class="flex flex-col md:flex-row justify-between items-end mb-16 text-white">
            <div class="max-w-xl">
                <h2 class="text-4xl md:text-[44px] leading-tight font-light tracking-tight mb-6">Transformative recovery through science and ritual.</h2>
                <p class="text-[17px] text-white/80 font-light max-w-md leading-relaxed">Evidence-based modalities that restore cellular health, enhance performance, and promote profound vitality.</p>
            </div>
            <a href="/" class="hidden md:inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors mt-6 md:mt-0 tracking-wide uppercase">
                All Modalities <span class="ml-2">→</span>
            </a>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
            {#each products as product}
                <ProductCard {...product} isDark={true} />
            {/each}
        </div>

        <div class="mt-12 text-center md:hidden">
            <a href="/" class="inline-flex items-center text-[13px] font-bold border-b border-white/30 pb-0.5 hover:border-white transition-colors text-white tracking-wide uppercase">
                All Modalities <span class="ml-2">→</span>
            </a>
        </div>
    </div>
</section>
