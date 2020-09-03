<template>
  <div>
    <slot />
  </div>
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