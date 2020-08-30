<template>
  <li>
    <slot />
  </li>
</template>


<script>
export default {
    props: {
        items: {type: Array, required: true}
    },
}
</script>