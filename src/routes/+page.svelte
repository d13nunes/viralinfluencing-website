<script lang="ts">
  import Card from '$lib/Card.svelte';
  import { Send, Calendar, Folder, MessageSquare, Lightbulb, Pencil, Hash, Mail } from "@lucide/svelte";

  const features = [
    {
      icon: Send,
      title: 'Effortless Publishing',
      description: 'Save time and reach a wider audience by posting your content to all your social networks with just a single click.'
    },{
      icon: Lightbulb,
      title: 'Endless Inspiration',
      description: 'Never run out of inspiration with AI-powered suggestions for viral video topics and post themes tailored to your niche.'
    },
    {
      icon: Pencil,
      title: 'One Click Captions',
      description: 'Craft engaging, platform-specific captions that grab attention and drive engagement, all with a single click.'
    },
    {
      icon: Hash,
      title: 'Perfect Hashtags',
      description: 'Maximize your reach and get discovered by new audiences with AI-recommended hashtags for your content.'
    },
    {
      icon: Calendar,
      title: 'Content Scheduling',
      description: 'Automate your posting schedule to engage your audience at the perfect time, so you can focus on creating great content.'
    },
    //   {
    //   icon: Folder,
    //   title: 'Centralized Content Hub',
    //   description: 'Keep your media organized and accessible in one place, making it easy to repurpose content and maintain a consistent brand.'
    // },
    {
      icon: MessageSquare,
      title: 'Unified Engagement',
      description: 'Manage all your comments and messages in one inbox, so you can interact with your community more efficiently.'
    },
    
  ];
</script>

<div class="w-full h-full">

  <header class="text-center pt-8 px-8">
    <h1 class="h1 text-4xl md:h-28 md:text-8xl bg-clip-text text-transparent  bg-gradient-to-r from-primary-500 to-tertiary-500 ">Viral Influencing</h1>
  </header>
  <div class="text-center px-8 pb-2 md:pb-8 pt-0 md:pt-8">
    <p class="text-surface-500-400-token text-xl mt-2 md:mt-0 md:text-2xl leading-none">Your new social media management tool<br>powered by Artificial Intelligence</p>
  </div>
  
  <div class="container mx-auto max-w-4xl p-8 h-full  ">
    <section class="grid  md:grid-cols-2 gap-8 ">
    
    <!-- <div class="card preset-filled-surface-100-900 light:border-1 border-surface-200 px-8 pt-6 pb-6 md:pb-8 flex flex-col items-center text-center rounded-lg shadow-md md:col-span-2"  >
      <div class="w-16 h-16 mb-4 rounded-full flex items-center justify-center preset-filled-secondary-500">
        <Mail class="w-8 h-8 text-white" />
      </div>
      <p class="mb-4 text-balance  leading-tight">Join our inner circle and get a front-row seat! Be the first to experience new features and shape the future of our tool.</p>
      <form class="flex w-full max-w-lg mx-auto">
        <input class="input  border-surface-200-800 preset-surface-50-950 rounded-r-none" type="email" placeholder="Enter your email" />
        <button type="submit" class="btn preset-filled-secondary-500 rounded-l-none hover:brightness-110 md:col-span-2 lg:col-span-2">Subscribe</button>
      </form>
      <p class="mt-4 text-justify-center  leading-tight">Subscribe our newsletter</p>
    </div> -->
      {#each features as feature}
        <Card title={feature.title} description={feature.description} > 
          {#snippet icon()}
            <feature.icon class="w-8 h-8 text-white" />
          {/snippet}
        </Card>
      {/each}
    </section>
    <div class="h-16"></div>
  </div>
</div>