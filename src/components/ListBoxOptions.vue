<template>
  <li
    tabindex="1"
    role="option"
    class="border-2 border-gray-200 rounded-lg px-3"
    @click="$emit('onToggle')"
  >
    <slot />
  </li>
</template>




<script>
export default {
    
}
</script>