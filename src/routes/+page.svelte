<script lang="ts">
  import Card from '$lib/Card.svelte';
  import { Send, Calendar, Folder, MessageSquare, Lightbulb, Pencil, Hash, Mail, ArrowRight, Star, Zap } from "@lucide/svelte";
	import { m } from '$lib/paraglide/messages.js';
  
  let showModal = $state(false);
  
  const features = [
    {
      icon: Send,
      title: m.features_send_title(),
      description: m.features_send_description(),
      gradient: 'from-blue-500 to-cyan-500'
    },{
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
    },
  ];
  
  function openModal() {
    showModal = true;
  }
  
  function closeModal() {
    showModal = false;
  }
</script>

<div class="relative w-full min-h-screen overflow-hidden">
  <!-- Background with enhanced gradient -->
  <div class="absolute inset-0 bg-gradient-to-br from-primary-50 via-white to-secondary-50">
    <div class="absolute inset-0 bg-[url('/landing.webp')] bg-cover bg-center bg-no-repeat opacity-20"></div>
    <div class="absolute inset-0 bg-gradient-to-b from-transparent via-white/80 to-white"></div>
  </div>

  <!-- Floating elements for visual interest -->
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <div class="absolute top-20 left-10 w-32 h-32 bg-primary-200 rounded-full blur-3xl opacity-30 animate-pulse"></div>
    <div class="absolute top-40 right-20 w-24 h-24 bg-secondary-200 rounded-full blur-2xl opacity-40 animate-pulse delay-1000"></div>
    <div class="absolute bottom-40 left-20 w-40 h-40 bg-tertiary-200 rounded-full blur-3xl opacity-20 animate-pulse delay-2000"></div>
  </div>

  <div class="relative z-10">
    <!-- Enhanced Header -->
    <header class="text-center pt-8 sm:pt-16 pb-0 md:pb-8 px-8">
        <div class="relative mb-8">
          <!-- Background glow effect -->
          <div class="absolute inset-0 bg-gradient-to-r from-primary-500/20 via-secondary-500/20 to-tertiary-500/20 blur-3xl rounded-full transform scale-150"></div>
          
          <!-- Main title with enhanced styling -->
          <h1 class="relative text-5xl sm:text-6xl md:text-7xl lg:text-8xl font-black bg-gradient-to-r from-primary-600 via-secondary-600 to-tertiary-600 bg-clip-text text-transparent leading-tight mb-6 tracking-tight px-4">
            <span class="block">Viral Influencing</span>
          </h1>
          
          <!-- Subtitle with enhanced styling -->
          <div class="relative">
            <p class="text-xl md:text-2xl lg:text-3xl text-surface-600 max-w-4xl mx-auto leading-relaxed font-medium">
              {m.hero_subtitle1()}
              <span class="text-primary-600 font-semibold">{m.hero_subtitle2()}</span> 
              {m.hero_subtitle3()}
              <span class="text-secondary-600 font-semibold">{m.hero_subtitle4()}</span> 
              {m.hero_subtitle5()}
            </p>
          </div>
          
          <!-- Decorative elements -->
          <div class="absolute -top-4 -left-4 w-8 h-8 bg-gradient-to-br from-primary-400 to-primary-600 rounded-full opacity-60 animate-pulse"></div>
          <div class="absolute -bottom-4 -right-4 w-6 h-6 bg-gradient-to-br from-secondary-400 to-secondary-600 rounded-full opacity-60 animate-pulse delay-1000"></div>
          <div class="absolute top-1/2 -left-8 w-4 h-4 bg-gradient-to-br from-tertiary-400 to-tertiary-600 rounded-full opacity-40 animate-pulse delay-2000"></div>
          <div class="absolute top-1/2 -right-8 w-4 h-4 bg-gradient-to-br from-primary-400 to-primary-600 rounded-full opacity-40 animate-pulse delay-3000"></div>
        </div>
        
        <!-- Call to action badge -->
        <!-- <div class="inline-flex items-center gap-3 px-6 py-3 bg-gradient-to-r from-primary- -->
    </header>
    
    <!-- Main Content -->
    <div class="container mx-auto max-w-7xl px-8 pb-16">
      <!-- Hero Section with enhanced design -->
      <section class="mb-20">
        <div class="relative bg-gradient-to-br from-white/80 to-white/40 backdrop-blur-sm border border-white/20 rounded-3xl p-8 md:p-12 shadow-2xl">
          <div class="absolute inset-0 bg-gradient-to-r from-primary-500/5 to-secondary-500/5 rounded-3xl"></div>
          <div class="relative z-10 flex flex-col lg:flex-row items-center gap-12">
            <div class="flex-1 text-center lg:text-left">
              <div class="inline-flex items-center gap-2 mb-6 px-4 py-2 bg-primary-100 text-primary-700 rounded-full text-sm font-medium">
                <Zap class="w-4 h-4" />
                <span>{m.hero_badge()}</span>
              </div>
              <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-surface-900 mb-6 leading-tight">
                {m.main_description1()} <span class="text-primary-600">{m.main_description2()}</span>
              </h2>
              <p class="text-lg text-surface-600 mb-8 leading-relaxed max-w-2xl">
                {m.hero_description()}
              </p>
              <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
                <button 
                  onclick={openModal}
                  class="group relative inline-flex items-center gap-3 px-8 py-4 bg-gradient-to-r from-primary-500 to-primary-600 text-white font-semibold rounded-xl shadow-lg hover:shadow-xl transform hover:-translate-y-1 transition-all duration-300"
                >
                  <span>{m.newsletter_button()}</span>
                  <ArrowRight class="w-5 h-5 group-hover:translate-x-1 transition-transform duration-300" />
                </button>
                <div class="text-center lg:text-left">
                  <p class="text-sm text-surface-500 mb-2">{m.newsletter_cta()}</p>
                  <div class="flex items-center gap-1 justify-center lg:justify-start">
                    <Star class="w-4 h-4 text-yellow-500 fill-current" />
                    <Star class="w-4 h-4 text-yellow-500 fill-current" />
                    <Star class="w-4 h-4 text-yellow-500 fill-current" />
                    <Star class="w-4 h-4 text-yellow-500 fill-current" />
                    <Star class="w-4 h-4 text-yellow-500 fill-current" />
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
        <div class="text-center mb-16">
          <h2 class="text-4xl md:text-5xl font-bold text-surface-900 mb-6">
            {m.features_section_title()}
          </h2>
          <p class="text-xl text-surface-600 max-w-3xl mx-auto">
            {m.features_section_subtitle()}
          </p>
        </div>
        
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
          {#each features as feature, index}
            <div class="group relative">
              <div class="absolute inset-0 bg-gradient-to-r from-primary-500/20 to-secondary-500/20 rounded-2xl blur-xl opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
              <Card title={feature.title} description={feature.description} class="relative bg-white/80 backdrop-blur-sm border border-white/20 hover:border-primary-200/50 transition-all duration-300 hover:shadow-2xl hover:-translate-y-2"> 
                {#snippet icon()}
                  <div class="w-16 h-16 rounded-2xl bg-gradient-to-br {feature.gradient} flex items-center justify-center shadow-lg group-hover:shadow-xl transition-shadow duration-300">
                    <feature.icon class="w-8 h-8 text-white" />
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
    <div class="fixed inset-0 bg-black/50 backdrop-blur-sm flex items-center justify-center z-50 p-4" onclick={closeModal}>
      <div class="bg-white rounded-2xl shadow-2xl max-w-2xl w-full transform transition-all duration-300 scale-100" >
        <div class="flex justify-between items-center p-6 border-b border-surface-200">
          <h3 class="text-2xl font-bold text-surface-900">{m.modal_title()}</h3>
          <button 
            onclick={closeModal}
            class="w-10 h-10 rounded-full bg-surface-100 hover:bg-surface-200 flex items-center justify-center transition-colors duration-200"
          >
            <span class="text-2xl font-light text-surface-600">×</span>
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
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-20px); }
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