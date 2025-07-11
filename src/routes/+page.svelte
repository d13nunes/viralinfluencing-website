<script lang="ts">
  import Card from '$lib/Card.svelte';
  import { Send, Calendar, Folder, MessageSquare, Lightbulb, Pencil, Hash, Mail } from "@lucide/svelte";
	import { m } from '$lib/paraglide/messages.js';
  const features = [
    {
      icon: Send,
      title: m.features_send_title(),
      description: m.features_send_description()
    },{
      icon: Lightbulb,
      title: m.features_lightbulb_title(),
      description: m.features_lightbulb_description()
    },
    {
      icon: Pencil,
      title: m.features_pencil_title(),
      description: m.features_pencil_description()
    },
    {
      icon: Hash,
      title: m.features_hash_title(),
      description: m.features_hash_description()
    },
    {
      icon: Calendar,
      title: m.features_calendar_title(),
      description: m.features_calendar_description()
    },
    // {
    //   icon: Folder,
    //   title: m.features_folder_title,
    //   description: m.features_folder_description
    // },
    {
      icon: MessageSquare,
      title: m.features_message_square_title(),
      description: m.features_message_square_description()
    },
    
  ];
</script>

<div class="relative w-full h-full ">
  <div class="absolute inset-0 bg-no-repeat bg-cover bg-center"
  style="background-image: url('/landing.png');">
<div class="absolute inset-0 bg-gradient-to-b from-transparent to-white"></div>
</div>

<div class="relative z-10 p-8">
  <header class="text-center pt-8 px-8 z-90">
    <!-- <h1 class="h1 text-4xl md:h-28 md:text-7xl lg:text-8xl bg-clip-text text-transparent  bg-gradient-to-r from-primary-100 to-secondary-500 ">Viral Influencing</h1> -->
    <h1 class="h1 text-5xl sm:text-6xl md:text-7xl lg:text-8xl text-primary-700 text-shadow-lg text-bold text ">Viral Influencing</h1>
  </header>
  
  <div class="container mx-auto max-w-4xl z-90 lg:max-w-7xl p-8 h-full  ">
    <section class="grid  md:grid-cols-2 gap-8 lg:grid-cols-3 ">
    
    <div class="card bg-surface-50 dark:bg-surface-950
    lg:col-span-3
    light:border-1 border-surface-200 px-4 md:px-8 pt-6 pb-6 md:pb-8 flex flex-col items-center text-center rounded-lg shadow-md md:col-span-2"   >
      <div class="w-16 h-16 mb-4 rounded-full flex items-center justify-center bg-primary-400">
        <Mail class="w-8 h-8 text-surface-800 dark:text-surface-950 " />
      </div>
      <div class="max-w-2xl px-8 mt-2 mb-5">
        <p class="text-2xl md:text-3xl leading-none text-justify-center">{m.main_description1()} {m.main_description2()}</p>
      </div>
      <div class="max-w-2xl px-1">
        <p class="mb-4 text-justify-center leading-tight">{m.newsletter_title()}</p>
        <form class="flex w-full max-w-lg mx-auto">
          <input class="input  border-surface-200-800 bg-surface-50 dark:bg-surface-950 rounded-r-none" type="email" placeholder="Enter your email" />
          <button type="submit" class="btn bg-primary-400 text-surface-50 dark:text-surface-950 rounded-l-none hover:brightness-110 md:col-span-2 lg:col-span-2">{m.newsletter_button()}</button>
        </form>
        <p class="mt-4 text-justify-center  leading-tight">{m.newsletter_cta()}</p>
      </div>
    </div>
      {#each features as feature}
        <Card title={feature.title} description={feature.description} > 
          {#snippet icon()}
            <feature.icon class="w-8 h-8 " />
          {/snippet}
        </Card>
      {/each}
    </section>
    <div class="h-16"></div>
  </div>
</div>
</div>