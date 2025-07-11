<script lang="ts">
	import Card from '$lib/Card.svelte';
	import {
		Send,
		Calendar,
		Folder,
		MessageSquare,
		Lightbulb,
		Pencil,
		Hash,
		Mail,
		ArrowRight,
		Star,
		Zap
	} from '@lucide/svelte';
	import { m } from '$lib/paraglide/messages.js';

	let showModal = $state(false);

	const features = [
		{
			icon: Send,
			title: m.features_send_title(),
			description: m.features_send_description(),
			gradient: 'from-blue-500 to-cyan-500'
		},
		{
			icon: Lightbulb,
			title: m.features_lightbulb_title(),
			description: m.features_lightbulb_description(),
			gradient: 'from-yellow-500 to-orange-500'
		},
		{
			icon: Pencil,
			title: m.features_pencil_title(),
			description: m.features_pencil_description(),
			gradient: 'from-green-500 to-emerald-500'
		},
		{
			icon: Hash,
			title: m.features_hash_title(),
			description: m.features_hash_description(),
			gradient: 'from-purple-500 to-pink-500'
		},
		{
			icon: Calendar,
			title: m.features_calendar_title(),
			description: m.features_calendar_description(),
			gradient: 'from-red-500 to-pink-500'
		},
		{
			icon: MessageSquare,
			title: m.features_message_square_title(),
			description: m.features_message_square_description(),
			gradient: 'from-indigo-500 to-purple-500'
		}
	];

	function openModal() {
		showModal = true;
	}

	function closeModal() {
		showModal = false;
	}
</script>

<div class="relative min-h-screen w-full overflow-hidden">
	<!-- Background with enhanced gradient -->
	<div class="from-primary-50 to-secondary-50 absolute inset-0 bg-gradient-to-br via-white">
		<div
			class="absolute inset-0 bg-[url('/landing.webp')] bg-cover bg-center bg-no-repeat opacity-20"
		></div>
		<div class="absolute inset-0 bg-gradient-to-b from-transparent via-white/80 to-white"></div>
	</div>

	<!-- Floating elements for visual interest -->
	<div class="pointer-events-none absolute inset-0 overflow-hidden">
		<div
			class="bg-primary-200 absolute top-20 left-10 h-32 w-32 animate-pulse rounded-full opacity-30 blur-3xl"
		></div>
		<div
			class="bg-secondary-200 absolute top-40 right-20 h-24 w-24 animate-pulse rounded-full opacity-40 blur-2xl delay-1000"
		></div>
		<div
			class="bg-tertiary-200 absolute bottom-40 left-20 h-40 w-40 animate-pulse rounded-full opacity-20 blur-3xl delay-2000"
		></div>
	</div>

	<div class="relative z-10">
		<!-- Enhanced Header -->
		<header class="px-8 pt-8 pb-0 text-center sm:pt-16 md:pb-8">
			<div class="relative mb-8">
				<!-- Background glow effect -->
				<div
					class="from-primary-500/20 via-secondary-500/20 to-tertiary-500/20 absolute inset-0 scale-150 transform rounded-full bg-gradient-to-r blur-3xl"
				></div>

				<!-- Main title with enhanced styling -->
				<h1
					class="from-primary-600 via-secondary-600 to-tertiary-600 relative mb-6 bg-gradient-to-r bg-clip-text px-4 text-5xl leading-tight font-black tracking-tight text-transparent sm:text-6xl md:text-7xl lg:text-8xl"
				>
					<span class="block">Viral Influencing</span>
				</h1>

				<!-- Subtitle with enhanced styling -->
				<div class="relative">
					<p
						class="text-surface-600 mx-auto max-w-4xl text-xl leading-relaxed font-medium md:text-2xl lg:text-3xl"
					>
						{m.hero_subtitle1()}
						<span class="text-primary-600 font-semibold">{m.hero_subtitle2()}</span>
						{m.hero_subtitle3()}
						<span class="text-secondary-600 font-semibold">{m.hero_subtitle4()}</span>
						{m.hero_subtitle5()}
					</p>
				</div>

				<!-- Decorative elements -->
				<div
					class="from-primary-400 to-primary-600 absolute -top-4 -left-4 h-8 w-8 animate-pulse rounded-full bg-gradient-to-br opacity-60"
				></div>
				<div
					class="from-secondary-400 to-secondary-600 absolute -right-4 -bottom-4 h-6 w-6 animate-pulse rounded-full bg-gradient-to-br opacity-60 delay-1000"
				></div>
				<div
					class="from-tertiary-400 to-tertiary-600 absolute top-1/2 -left-8 h-4 w-4 animate-pulse rounded-full bg-gradient-to-br opacity-40 delay-2000"
				></div>
				<div
					class="from-primary-400 to-primary-600 absolute top-1/2 -right-8 h-4 w-4 animate-pulse rounded-full bg-gradient-to-br opacity-40 delay-3000"
				></div>
			</div>

			<!-- Call to action badge -->
			<!-- <div class="inline-flex items-center gap-3 px-6 py-3 bg-gradient-to-r from-primary- -->
		</header>

		<!-- Main Content -->
		<div class="container mx-auto max-w-7xl px-8 pb-16">
			<!-- Hero Section with enhanced design -->
			<section class="mb-20">
				<div
					class="relative rounded-3xl border border-white/20 bg-gradient-to-br from-white/80 to-white/40 p-8 shadow-2xl backdrop-blur-sm md:p-12"
				>
					<div
						class="from-primary-500/5 to-secondary-500/5 absolute inset-0 rounded-3xl bg-gradient-to-r"
					></div>
					<div class="relative z-10 flex flex-col items-center gap-12 lg:flex-row">
						<div class="flex-1 text-center lg:text-left">
							<div
								class="bg-primary-100 text-primary-700 mb-6 inline-flex items-center gap-2 rounded-full px-4 py-2 text-sm font-medium"
							>
								<Zap class="h-4 w-4" />
								<span>{m.hero_badge()}</span>
							</div>
							<h2
								class="text-surface-900 mb-6 text-3xl leading-tight font-bold md:text-4xl lg:text-5xl"
							>
								{m.main_description1()}
								<span class="text-primary-600">{m.main_description2()}</span>
							</h2>
							<p class="text-surface-600 mb-8 max-w-2xl text-lg leading-relaxed">
								{m.hero_description()}
							</p>
							<div class="flex flex-col justify-center gap-4 sm:flex-row lg:justify-start">
								<button
									onclick={openModal}
									class="group from-primary-500 to-primary-600 relative inline-flex transform items-center gap-3 rounded-xl bg-gradient-to-r px-8 py-4 font-semibold text-white shadow-lg transition-all duration-300 hover:-translate-y-1 hover:shadow-xl"
								>
									<span>{m.newsletter_button()}</span>
									<ArrowRight
										class="h-5 w-5 transition-transform duration-300 group-hover:translate-x-1"
									/>
								</button>
								<div class="text-center lg:text-left">
									<p class="text-surface-500 mb-2 text-sm">{m.newsletter_cta()}</p>
									<div class="flex items-center justify-center gap-1 lg:justify-start">
										<Star class="h-4 w-4 fill-current text-yellow-500" />
										<Star class="h-4 w-4 fill-current text-yellow-500" />
										<Star class="h-4 w-4 fill-current text-yellow-500" />
										<Star class="h-4 w-4 fill-current text-yellow-500" />
										<Star class="h-4 w-4 fill-current text-yellow-500" />
										<!-- <span class="text-sm text-surface-600 ml-2">Join 10,000+ creators</span> -->
									</div>
								</div>
							</div>
						</div>
						<!-- <div class="flex-1 flex justify-center">
              <!-- <div class="relative"> -->
						<!-- <div class="w-20 h-20 rounded-2xl bg-gradient-to-br from-primary-400 to-primary-600 flex items-center justify-center shadow-xl">
                  <Mail class="w-10 h-10 text-white" />
                </div> -->
						<!-- <div class="absolute -top-2 -right-2 w-6 h-6 bg-secondary-500 rounded-full flex items-center justify-center">
                  <span class="text-white text-xs font-bold">!</span>
                </div> -->
						<!-- </div> -->
						<!-- </div> -->
					</div>
				</div>
			</section>

			<!-- Features Grid with enhanced cards -->
			<section class="mb-20">
				<div class="mb-16 text-center">
					<h2 class="text-surface-900 mb-6 text-4xl font-bold md:text-5xl">
						{m.features_section_title()}
					</h2>
					<p class="text-surface-600 mx-auto max-w-3xl text-xl">
						{m.features_section_subtitle()}
					</p>
				</div>

				<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
					{#each features as feature, index}
						<div class="group relative h-full">
							<div
								class="from-primary-500/20 to-secondary-500/20 absolute inset-0 rounded-2xl bg-gradient-to-r opacity-0 blur-xl transition-opacity duration-500 group-hover:opacity-100"
							></div>
							<Card
								title={feature.title}
								description={feature.description}
								class="hover:border-primary-200/50 relative h-full border border-white/20 bg-white/80 backdrop-blur-sm transition-all duration-300 hover:-translate-y-2 hover:shadow-2xl"
							>
								{#snippet icon()}
									<div
										class="h-16 w-16 rounded-2xl bg-gradient-to-br {feature.gradient} flex items-center justify-center shadow-lg transition-shadow duration-300 group-hover:shadow-xl"
									>
										<feature.icon class="h-8 w-8 text-white" />
									</div>
								{/snippet}
							</Card>
						</div>
					{/each}
				</div>
			</section>
		</div>
	</div>

	<!-- Enhanced Modal -->
	{#if showModal}
		<div
			class="fixed inset-0 z-50 flex items-center justify-center bg-black/50 p-4 backdrop-blur-sm"
			onclick={closeModal}
		>
			<div
				class="w-full max-w-2xl scale-100 transform rounded-2xl bg-white shadow-2xl transition-all duration-300"
			>
				<div class="border-surface-200 flex items-center justify-between border-b p-6">
					<h3 class="text-surface-900 text-2xl font-bold">{m.modal_title()}</h3>
					<button
						onclick={closeModal}
						class="bg-surface-100 hover:bg-surface-200 flex h-10 w-10 items-center justify-center rounded-full transition-colors duration-200"
					>
						<span class="text-surface-600 text-2xl font-light">×</span>
					</button>
				</div>
				<div class="p-6">
					<iframe
						width="100%"
						height="600"
						src="https://de6b105f.sibforms.com/serve/MUIFAB2EPZlx5SgwDqQZL7U6kGq6aZGAYTXzm1DWLlbqiKiAGo4pE0FV0xawCjqVhVoO3zmg_36tI9VNMFzpTsvu4GavNnnu3rZVzDBG0oVzfLrR57iAt7F6c7vMFWCGACMimOIoJg0MgMldg3rXBcT1fZwzzmA1bu0eSn6wUgMmi9BbxpytzOpv9LB8rFEY1KhAzheoYgtZB4FY"
						frameborder="0"
						scrolling="auto"
						allowfullscreen
						style="display: block; margin: 0 auto; max-width: 100%; border-radius: 12px;"
					></iframe>
				</div>
			</div>
		</div>
	{/if}
</div>

<style>
	@keyframes float {
		0%,
		100% {
			transform: translateY(0px);
		}
		50% {
			transform: translateY(-20px);
		}
	}

	.animate-float {
		animation: float 6s ease-in-out infinite;
	}

	.animate-pulse {
		animation: pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite;
	}

	.delay-1000 {
		animation-delay: 1s;
	}

	.delay-2000 {
		animation-delay: 2s;
	}
</style>
