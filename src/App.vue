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
    <div>
      <p class="text-gray-500 text-sm">Starting at</p>
      <h1 class="text-gray-900 font-extrabold leading-tight text-5xl">
        $1,799
      </h1>
      <div class="space-y-4 mt-4">
        <p class="text-gray-900 font-medium">
          The KEMPER PROFILER™ is the leading-edge digital guitar amplifier and
          all-in-one effects processor.
        </p>
        <p class="text-gray-500">
          Hailed as a game-changer by guitarists the world over, the PROFILER™
          is the first digital guitar amp to really nail the full and dynamic
          sound of a guitar or bass amp.
        </p>
        <p class="text-gray-500">
          This is made possible by a radical, patented technology and concept
          which we call "PROFILING".
        </p>
      </div>
    </div>

    <div class="my-10 space-y-2">
      <h4 class="text-gray-800 text-xl font-medium">Form Factor</h4>
      <ul class="space-y-4">
        <li class="border border-gray-300 rounded-lg py-4 px-6 space-y-1">
          <h5 class="text-gray-900 font-medium text-sm">Profiler Head</h5>
          <p class="text-gray-500 text-sm">
            Compact amplifier head, perfect for a speaker cabinet or desk.
          </p>
        </li>
        <li class="border border-gray-300 rounded-lg py-4 px-6 space-y-1">
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
        <li class="border border-gray-300 rounded-lg py-4 px-6 space-y-1">
          <h5 class="text-gray-900 font-medium text-sm">None</h5>
          <p class="text-gray-500 text-sm">
            Use in the studio or with your own power amp.
          </p>
        </li>
        <li class="border border-gray-300 rounded-lg py-4 px-6 space-y-1">
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
        <li class="border border-gray-300 rounded-lg py-4 px-6 space-y-1">
          <div class="flex justify-between">
            <h5 class="text-gray-900 font-medium text-sm">None</h5>
            <span class="text-gray-900 text-sm flex-none font-medium"
              >+ $449</span
            >
          </div>
        </li>
        <li class="border border-gray-300 rounded-lg py-4 px-6 space-y-1">
          <div class="flex justify-between">
            <h5 class="text-gray-900 font-medium text-sm">
              Profiler Remote Foot Controller
            </h5>
          </div>
        </li>
      </ul>
    </div>

    <div>
      <table class="flex flex-col max-w-full space-y-2 divide-y">
        <tr>
          <th class="font-medium text-xl">
            Specifications
          </th>
          <th></th>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Amp Models
          </td>
          <td class="text-xs">
            200
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Effects Loop
          </td>
          <td class="text-xs">
            Yes
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Inputs
          </td>
          <td class="text-xs">
            2 x 1/4”
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Outputs
          </td>
          <td class="text-xs">
            1 x 1/4”, 2 x XLR, 2 x 1/4”
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            MIDI I/O
          </td>
          <td class="text-xs">
            In/Out/Thru
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Height
          </td>
          <td class="text-xs">
            8.54”
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Width
          </td>
          <td class="text-xs">
            14.88”
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Depth
          </td>
          <td class="text-xs">
            6.81”
          </td>
        </tr>
        <tr
          class="justify-between flex font-medium text-sm py-4 items-baseline"
        >
          <td>
            Weight
          </td>
          <td class="text-xs">
            11.73 lbs
          </td>
        </tr>
      </table>
    </div>

    <div class="bg-gray-50 fixed h-20 inset-0 top-auto p-4">
      <div class="flex justify-end items-center space-x-6">
        <p class="text-gray-900 font-bold text-3xl">$2,717</p>
        <button class="text-white text-sm bg-cool-gray-900 rounded-md h-9 w-24">
          Buy now
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import PhotoViewer from './components/PhotoViewer';

export default {
  name: 'App',
  components: {PhotoViewer},
}
</script>