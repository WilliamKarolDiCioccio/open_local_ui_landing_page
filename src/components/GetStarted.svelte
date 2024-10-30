<script>
  import { Icon } from 'svelte-materialdesign-icons'
  import { Modals, closeModal, openModal, modals } from 'svelte-modals'
  import Modal from './DownloadsModal.svelte'

  function handleOpen() {
    openModal(Modal, {})
  }
</script>

<section id="get-started" class="py-20">
  <div class="container mx-auto px-6 lg:px-12">
    <div class="text-center">
      <h2
        class="text-2xl md:text-4xl font-bold mb-12"
        data-aos="fade-up"
        data-aos-delay="0"
      >
        Get Started
      </h2>

      <!-- Call to Action Button -->
      <div class="mt-12" data-aos="fade-up" data-aos-delay="900">
        <button
          id="cta-button"
          type="button"
          class="text-white px-6 py-3 rounded-full font-semibold transition-all duration-300 p-2 group"
          on:click={() => handleOpen()}
          data-aos="fade-up"
          data-aos-delay="600"
        >
          <div class="flex flex-row items-center">
            Download the Installer

            <!-- Alpha Version Warning -->
            <div
              class="ml-2 text-xs bg-stone-900 text-white px-2 py-1 rounded-full"
            >
              Alpha
            </div>

            <div
              class="ml-0 w-0 overflow-hidden transition-all duration-300 group-hover:ml-2 group-hover:w-5"
            >
              <Icon class="w-5 h-5" name="download" />
            </div>
          </div>
        </button>
      </div>
    </div>
  </div>
</section>
