<template>

  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="max-w-3xl">
        <h1 data-aos="fade-down" class="text-4xl md:text-7xl font-bold mb-6">The one link developers need</h1>
        <p class="mb-10">Merj streamlines your online presence with a single, customized link that directs visitors to all your profiles and platforms. Level up your online presence with Merj.</p>
        <div class="flex flex-col px-40">
          <form>
            <div class="relative">
              <input
                type="search"
                id="search"
                class="block w-full p-4 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-primary focus:border-primary"
                placeholder="Your Email Address"
                required
              />
                <button
                  type="submit"
                  class="btn btn-sm btn-primary absolute top-0 right-0 mt-3 mr-3"
                >
                  <span class="tooltip" data-tip="No credit card required!">
                    Start free
                  </span>
                </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>

  <generic-panel></generic-panel>

</template>

<script>
import { useHead } from '#app';
import { definePageMeta } from '#imports';
import GenericPanel from '~/components/commons/GenericPanel';
import ogBanner from '../assets/images/nuxtwind-daisy-og-banner.jpg';

export default {
  components: {
    GenericPanel,
  },
  setup () {
    definePageMeta({
      layout: 'default',
    });

    useHead({
      title: 'Merj',
      description: 'The one linke developers need',
      link: [
        { rel: 'icon', type: 'image/png', href: '/favicon.png' },
      ],
      meta: [
        {
          hid: 'og:image',
          name: 'og:image',
          property: 'og:image',
          content: ogBanner,
        },
      ],
    });

    return {};
  },
};
</script>
