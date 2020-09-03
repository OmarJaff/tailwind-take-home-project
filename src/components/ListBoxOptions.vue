<template>
  <button
    role="tab"
    class="border-2 border-gray-200 rounded-lg px-3"
    @click="$emit('onClick')"
    @keyup.left="$emit('onArrowLeftPressed')"
    @keyup.right="$emit('onArrowRightPressed')"
  >
    <slot />
  </button>
</template>




<script>
export default {
    
}
</script>