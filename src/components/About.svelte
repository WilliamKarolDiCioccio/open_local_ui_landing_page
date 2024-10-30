<script>
  import { Icon } from 'svelte-materialdesign-icons'

  // Step 1: Define the array of objects
  const cards = [
    {
      icon: '🤖',
      title: 'Open Source & Free',
      description: `OpenLocalUI is an open-source project by William Karol Di Cioccio. 
                    Our goal is to make interacting with large language models (LLMs) locally accessible to everyone, 
                    without any cost. 🆓`
    },
    {
      icon: '🔒',
      title: 'Privacy & Security',
      description: `We prioritize your privacy and community needs, allowing users to harness powerful AI tools 
                    without compromising their data. Our commitment is to high-quality, secure software. 💪`
    },
    {
      icon: '⭐️',
      title: 'Support & Contribution',
      description: `Your support is invaluable! For us GitHub stars are on par with financial donations, 
                    so don't hesitate to visit the 
                    <a href="https://github.com/WilliamKarolDiCioccio/open_local_ui" 
                    class="text-purple-500 underline hover:text-purple-300 transition">
                    Official Repository</a>.`
    }
  ]
</script>

<section id="about" class="py-20">
  <div class="container mx-auto px-6 lg:px-12">
    <div class="text-center">
      <h2
        class="text-2xl md:text-4xl font-bold mb-12"
        data-aos="fade-up"
        data-aos-delay="0"
      >
        About OpenLocalUI
      </h2>

      <!-- Step 2: Use {#each} to generate cards -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
        {#each cards as card}
          <div
            class="p-0.5 rounded-lg relative overflow-hidden shining-card-border-animation"
            data-aos="fade-up"
            data-aos-delay={cards.indexOf(card) * 150}
          >
            <div
              class="p-6 w-full h-full rounded-lg bg-gradient-to-br from-gray-800 via-stone-900 to-gray-700 border border-white border-opacity-25"
            >
              <div class="text-3xl mb-4">{card.icon}</div>
              <h3 class="text-xl font-semibold mb-2">{card.title}</h3>
              <p class="text-gray-300 text-sm md:text-base">
                {@html card.description}
              </p>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>
