<template>
  <div id="app" class="antialiased mx-4 sm:mx-10">
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
      <ul class="space-y-4 sm:flex sm:space-y-0 sm:space-x-4">
        <li
          class="border border-gray-300 rounded-lg py-4 px-6 sm:w-72 space-y-1"
        >
          <h5 class="text-gray-900 font-medium text-sm">Profiler Head</h5>
          <p class="text-gray-500 text-sm">
            Compact amplifier head, perfect for a speaker cabinet or desk.
          </p>
        </li>
        <li
          class="border border-gray-300 rounded-lg py-4 px-6 sm:w-72 space-y-1"
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

    <table class="flex flex-col max-w-full space-y-2 divide-y mb-32 sm:mb-48">
      <tr>
        <th class="font-medium text-xl">
          Specifications
        </th>
        <th></th>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Amp Models
        </td>
        <td class="text-xs">
          200
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Effects Loop
        </td>
        <td class="text-xs">
          Yes
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Inputs
        </td>
        <td class="text-xs">
          2 x 1/4”
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Outputs
        </td>
        <td class="text-xs">
          1 x 1/4”, 2 x XLR, 2 x 1/4”
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          MIDI I/O
        </td>
        <td class="text-xs">
          In/Out/Thru
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Height
        </td>
        <td class="text-xs">
          8.54”
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Width
        </td>
        <td class="text-xs">
          14.88”
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Depth
        </td>
        <td class="text-xs">
          6.81”
        </td>
      </tr>
      <tr class="justify-between flex font-medium text-sm py-4 items-baseline">
        <td>
          Weight
        </td>
        <td class="text-xs">
          11.73 lbs
        </td>
      </tr>
      <tr></tr>
    </table>

    <div
      class="bg-gray-50 fixed h-20 sm:h-28 inset-0 top-auto p-4 sm:py-6 sm:px-10"
    >
      <div class="flex flex-row-reverse justify-between">
        <div class="flex justify-end items-center space-x-6">
          <div class="flex flex-col">
            <p class="text-gray-900 font-bold text-3xl flex self-end">
              $2,717
            </p>
            <div>
              <span href="#" class="hidden sm:block text-gray-500 text-sm"
                >Need a financing? <a href="#" class="underline">Learn more</a>
              </span>
            </div>
          </div>

          <button
            class="text-white text-sm bg-cool-gray-900 rounded-md h-9 w-24"
          >
            Buy now
          </button>
        </div>
        <div class="hidden sm:block">
          <div class="flex-row space-y-4">
            <div class="flex space-x-2 items-center">
              <svg
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M10 18C14.4183 18 18 14.4183 18 10C18 5.58172 14.4183 2 10 2C5.58172 2 2 5.58172 2 10C2 14.4183 5.58172 18 10 18ZM4.33179 8.02741C4.70542 6.95361 5.37558 6.01864 6.24421 5.32056C6.51209 5.72966 6.97449 5.99991 7.50001 5.99991C8.32844 5.99991 9.00001 6.67148 9.00001 7.49991V7.99991C9.00001 9.10448 9.89545 9.99991 11 9.99991C12.1046 9.99991 13 9.10448 13 7.99991C13 7.05979 13.6487 6.27118 14.5228 6.05719C15.4428 7.11161 16 8.49069 16 9.99992C16 10.3407 15.9716 10.6748 15.917 11.0001H15C13.8954 11.0001 13 11.8955 13 13.0001V15.1973C12.1175 15.7078 11.0928 15.9999 9.99992 15.9999V14C9.99992 12.8954 9.10448 12 7.99992 12C6.89535 12 5.99992 11.1046 5.99992 10C5.99992 9.00849 5.27841 8.1855 4.33179 8.02741Z"
                  fill="#9FA6B2"
                />
              </svg>
              <span class="text-sm text-gray-900 font-medium">
                Free Shipping
              </span>
            </div>
            <div class="flex space-x-2 items-center">
              <svg
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M2.16611 4.99891C5.17437 4.95809 7.91528 3.81033 10 1.94446C12.0847 3.81033 14.8256 4.95809 17.8339 4.99891C17.9431 5.64968 18 6.31821 18 7.00003C18 12.2249 14.6608 16.6698 10 18.3172C5.33923 16.6698 2 12.2249 2 7.00003C2 6.31821 2.05686 5.64968 2.16611 4.99891ZM13.7071 8.70711C14.0976 8.31658 14.0976 7.68342 13.7071 7.29289C13.3166 6.90237 12.6834 6.90237 12.2929 7.29289L9 10.5858L7.70711 9.29289C7.31658 8.90237 6.68342 8.90237 6.29289 9.29289C5.90237 9.68342 5.90237 10.3166 6.29289 10.7071L8.29289 12.7071C8.68342 13.0976 9.31658 13.0976 9.70711 12.7071L13.7071 8.70711Z"
                  fill="#9FA6B2"
                />
              </svg>
              <span class="text-sm text-gray-900 font-medium">
                2 Year Warranty
              </span>
            </div>
          </div>
        </div>
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