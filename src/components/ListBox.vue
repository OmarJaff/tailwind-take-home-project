<template>
  <ul>
    <slot />
  </ul>
</template>


<script>

export default {
    props: {
        // items: {type: Array, required: true}
    },
    data: () => ({
        selected: false,
    })
}
</script>