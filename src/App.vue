<template>
  <div id="app" class="antialiased mx-4">
    <div class="flex flex-col divide-y divide-gray-300 space-y-6">
      <div class="flex mt-12">
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
      <div class="flex flex-col">
        <div class="my-8">
          <PhotoViewer />
        </div>
      </div>
    </div>

    <div></div>
  </div>
</template>

<script>
import PhotoViewer from './components/PhotoViewer';

export default {
  name: 'App',
  components: {PhotoViewer},
}
</script>