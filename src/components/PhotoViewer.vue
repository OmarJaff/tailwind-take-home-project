<template>
  <div>
    <img :src="imageSources[0].src" alt="" />
  </div>
</template>


<script>

const images = require.context('../../public/img', true , /\.jpg$/); 


const imageSources = [
    { 
        id:1,
        title: 'kemper angle',
        src: images('./kemper-angle.jpg')
    },
    {
        id:2,
        title: 'kemper front',
        src: images('./kemper-front.jpg')
    },
    {
        id:3,
        title: 'kemper rear',
        src: images('./kemper-rear.jpg')
    }
];

export default {
    name: 'PhotoViewer',
    data: () => ({
        imageSources
    })
}
</script>