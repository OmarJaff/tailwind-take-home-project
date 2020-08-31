<!-- eslint-disable -->

<template>
  <div class="space-y-4 flex-col flex-wrap">
    <div class="border shadow-sm border-gray-200 rounded-lg p-0.5 w-full">
      <img :src="images[0].src" alt="" />
    </div>
    <div class="">
      <ListBox class="flex flex-row space-x-4 lg:space-x-2 justify-between">
        <ListBoxOptions
          v-for="image in images"
          :key="image.id"
          class="justify-center w-1/3 border-2 border-gray-200 rounded-lg px-3"
        >
          <img :src="image.src" alt="image.title" class="" />
        </ListBoxOptions>
      </ListBox>
    </div>
  </div>
</template>



<script>

import ListBox from './ListBox';
import ListBoxOptions from './ListBoxOptions';

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
    components: {
        ListBox,
        ListBoxOptions
    },
    data: () => ({
        images
    })
}
</script>