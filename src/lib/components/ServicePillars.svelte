<script lang="ts">
	type Pillar = {
		title: string;
		subtitle: string;
		description: string;
		image: string;
	};

	const pillars: Pillar[] = [
		{
			title: "Contrast Therapy",
			subtitle: "Ice & Heat Immersion",
			description: "Experience the transformative power of guided ice baths and infrared saunas. This ancient practice, refined with modern precision, enhances circulation, reduces inflammation, and accelerates recovery.",
			image: "/generated/image-person-experiencing-contrast-therapy-in--1766737643811-0.webp"
		},
		{
			title: "Stretch Lab",
			subtitle: "Assisted Flexibility",
			description: "Personalized one-on-one stretch therapy sessions designed to improve mobility, release tension, and optimize movement patterns. Expert practitioners guide you through targeted techniques for lasting relief.",
			image: "/generated/image-professional-stretch-therapy-session-in--1766737648030-1.webp"
		},
		{
			title: "Core Remedies",
			subtitle: "Advanced Recovery",
			description: "Elevate cellular health with hyperbaric oxygen therapy and precision IV vitamin infusions including NAD+. Science-backed modalities that restore vitality from within and enhance peak performance.",
			image: "/generated/image-luxury-wellness-treatment-room-with-hype-1766737650514-2.webp"
		}
	];
</script>

<section class="bg-white py-20 md:py-32">
	<div class="container mx-auto px-6 md:px-12">
		<div class="max-w-3xl mx-auto text-center mb-16 md:mb-20">
			<h2 class="text-4xl md:text-5xl lg:text-[56px] leading-tight font-light tracking-tight mb-6 text-gray-950">
				Three pillars of profound restoration.
			</h2>
			<p class="text-lg md:text-xl text-gray-600 font-light leading-relaxed">
				Our signature service categories combine ancient wisdom with cutting-edge science, designed exclusively for those who demand excellence in recovery.
			</p>
		</div>

		<div class="grid grid-cols-1 lg:grid-cols-3 gap-8 lg:gap-6">
			{#each pillars as pillar}
				<div class="group">
					<div class="relative aspect-[4/3] overflow-hidden bg-gray-100 mb-6">
						<img 
							src={pillar.image} 
							alt={pillar.title}
							class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
						/>
					</div>
					<div class="space-y-3">
						<div>
							<p class="text-xs font-bold tracking-widest uppercase text-primary-600 mb-2">
								{pillar.subtitle}
							</p>
							<h3 class="text-2xl md:text-3xl font-light tracking-tight text-gray-950">
								{pillar.title}
							</h3>
						</div>
						<p class="text-[15px] leading-relaxed text-gray-600 font-light">
							{pillar.description}
						</p>
					</div>
				</div>
			{/each}
		</div>

		<div class="text-center mt-16">
			<a 
				href="/" 
				class="inline-flex items-center text-sm font-bold border-b-2 border-gray-950 pb-1 hover:border-primary-600 hover:text-primary-600 transition-colors tracking-wide uppercase"
			>
				Explore All Services <span class="ml-2">→</span>
			</a>
		</div>
	</div>
</section>
