<!-- eslint-disable -->
<template>
  <div id="app" class="antialiased mx-4 sm:mx-12 md:mx-28 lg:mx-10 xl:mx-28">
    <div class="mt-12 flex mx-auto container relative">
      <h1
        class="text-gray-900 font-extrabold text-4xl leading-10 tracking-tight"
      >
        Get your Kemper Profiling Amp
        <p
          class="text-gray-500 font-normal mt-3.5 leading-normal tracking-tight text-xl"
        >
          All your favorite amps and effects, together in one little box.
        </p>
      </h1>
    </div>

    <div
      class="flex flex-col flex-no-wrap lg:flex-none lg:grid lg:grid-cols-2 lg:my-10 lg:gap-8 mx-auto container"
    >
      <div>
        <div class="flex">
          <div class="flex flex-col divide-y divide-gray-300 space-y-6">
            <div class="flex flex-col">
              <div
                class="my-8 lg:my-0 xl:px-4 custom-width"
                :class="{ 'lg:fixed lg:top-0 lg:pt-8': isLocked }"
              >
                <PhotoViewer />
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="flex flex-col">
        <div>
          <div>
            <p class="text-gray-500 text-sm">Starting at</p>
            <h1 class="text-gray-900 font-extrabold leading-tight text-5xl">
              $1,799
            </h1>
            <div class="space-y-4 mt-4">
              <p class="text-gray-900 font-medium">
                The KEMPER PROFILER™ is the leading-edge digital guitar
                amplifier and all-in-one effects processor.
              </p>
              <p class="text-gray-500">
                Hailed as a game-changer by guitarists the world over, the
                PROFILER™ is the first digital guitar amp to really nail the
                full and dynamic sound of a guitar or bass amp.
              </p>
              <p class="text-gray-500">
                This is made possible by a radical, patented technology and
                concept which we call "PROFILING".
              </p>
            </div>
          </div>

          <div class="my-10 space-y-2">
            <h4 class="text-gray-800 text-xl font-medium">Form Factor</h4>
            <ul class="space-y-4 sm:flex sm:space-y-0 sm:space-x-4">
              <li
                class="border border-gray-300 rounded-lg py-5 px-6 space-y-1 sm:w-96"
              >
                <h5 class="text-gray-900 font-medium text-sm">Profiler Head</h5>
                <p class="text-gray-500 text-sm">
                  Compact amplifier head, perfect for a speaker cabinet or desk.
                </p>
              </li>
              <li
                class="border border-gray-300 rounded-lg py-5 px-6 space-y-1 sm:w-96"
              >
                <h5 class="text-gray-900 font-medium text-sm">Profiler Rack</h5>
                <p class="text-gray-500 text-sm">
                  3U rackmount version of the classic profiling amplifier.
                </p>
              </li>
            </ul>
          </div>

          <div class="my-10 space-y-2">
            <h4 class="text-gray-800 text-xl font-medium">Power Amp</h4>
            <ul class="space-y-4">
              <li class="border border-gray-300 rounded-lg py-5 px-6 space-y-1">
                <h5 class="text-gray-900 font-medium text-sm">None</h5>
                <p class="text-gray-500 text-sm">
                  Use in the studio or with your own power amp.
                </p>
              </li>
              <li class="border border-gray-300 rounded-lg py-5 px-6 space-y-1">
                <h5 class="text-gray-900 font-medium text-sm">Powered</h5>
                <div class="flex justify-between">
                  <p class="text-gray-500 text-sm">
                    Built-in 600W solid state power amp.
                  </p>
                  <span class="text-gray-900 text-sm flex-none font-medium"
                    >+ $449</span
                  >
                </div>
              </li>
            </ul>
          </div>

          <div class="my-10 space-y-2">
            <h4 class="text-gray-800 text-xl font-medium">Foot Controller</h4>
            <ul class="space-y-4">
              <li class="border border-gray-300 rounded-lg py-5 px-6 space-y-1">
                <div class="flex justify-between">
                  <h5 class="text-gray-900 font-medium text-sm">None</h5>
                  <span class="text-gray-900 text-sm flex-none font-medium"
                    >+ $449</span
                  >
                </div>
              </li>
              <li class="border border-gray-300 rounded-lg py-5 px-6 space-y-1">
                <div class="flex justify-between">
                  <h5 class="text-gray-900 font-medium text-sm">
                    Profiler Remote Foot Controller
                  </h5>
                </div>
              </li>
            </ul>
          </div>

          <div>
            <SpesificationsTable />
          </div>
        </div>
        <div
          class="bg-gray-50 fixed h-20 sm:h-28 inset-0 top-auto p-4 sm:py-6 sm:px-12 md:px-28 lg:px-10 xl:px-28"
        >
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<style  scoped>
.custom-width {
  width: 100%;
}
@media (min-width: 1024px) {
  .custom-width {
    width: 30rem;
  }

  @media (min-width: 1276px) {
    .custom-width {
      width: 39rem;
    }
  }
}
</style>
<script>
import PhotoViewer from './components/PhotoViewer';
import Footer from './components/Footer';
import SpesificationsTable from './components/SpesificationsTable';


export default {
  name: 'App',
  components: {PhotoViewer , Footer , SpesificationsTable},
  data: () => ({
      isLocked: false,
      scrollY: 0
  }),
  created () {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed () {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY;
      this.scrollY >= 130 ? this.isLocked = true : this.isLocked = false;
      
      return this.isLocked;
    },
    
  }

}
</script>