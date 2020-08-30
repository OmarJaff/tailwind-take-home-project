<template>
  <div class="space-y-4">
    <div class="border shadow-sm border-gray-200 rounded-lg p-0.5">
      <img :src="images[0].src" alt="" />
    </div>
    <div class="flex space-x-4">
      <button
        v-for="image in images"
        :key="image.id"
        type="checkbox"
        class="flex justify-center border-gray-200 border rounded-lg shadow-sm h-12 w-28 p-0.5"
      >
        <img :src="image.src" alt="image.title" class="w-16" />
      </button>
    </div>
  </div>
</template>


<script>

const image = require.context('../../public/img', true , /\.jpg$/); 


const images = [
    { 
        id:1,
        title: 'kemper front',
        src: image('./kemper-front.jpg')
    },
    {
        id:2,
        title: 'kemper angle',
        src: image('./kemper-angle.jpg')
       
    },
    {
        id:3,
        title: 'kemper rear',
        src: image('./kemper-rear.jpg')
    }
];

export default {
    name: 'PhotoViewer',
    data: () => ({
        images
    })
}
</script>