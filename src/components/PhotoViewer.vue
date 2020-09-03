<!-- eslint-disable -->

<template>
  <div class="space-y-4 flex-col flex-wrap">
    <div class="border shadow-sm border-gray-200 rounded-lg p-0.5 w-full">
      <img :src="images[imageIndex].src" alt="" />
    </div>
    <div class="">
      <ListBox
        role="list"
        class="flex flex-row space-x-4 lg:space-x-2 justify-between"
      >
        <ListOptions
          v-for="(image, index) in images"
          :key="image.id"
          :title="image.title"
          @onToggle="
            {
              handleImageToggle(index);
            }
          "
        >
          <img :src="image.src" :alt="image.title" />
        </ListOptions>
      </ListBox>
    </div>
  </div>
</template>



<script>

import ListBox from './ListBox';
import ListOptions from './ListBoxOptions';

const image = require.context('../../public/img', true , /\.jpg$/); 


const images = [
    { 
        id:1,
        title: 'kemper front photo',
        src: image('./kemper-front.jpg')
    },
    {
        id:2,
        title: 'kemper angle photo',
        src: image('./kemper-angle.jpg')
       
    },
    {
        id:3,
        title: 'kemper rear photo',
        src: image('./kemper-rear.jpg')
    }
];

export default {
    name: 'PhotoViewer',
    components: {
        ListBox,
        ListOptions
    },
    data: () => ({
        images,
        imageIndex: 0,
    }), 
    methods: {
      handleImageToggle(index) {
          return this.imageIndex = index;
      }
    }
}
</script>