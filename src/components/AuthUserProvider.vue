<template>
  <div>
    <slot v-bind="{ user: { first: 'Illia', last: 'Sakovich' } }"/>
  </div>
</template>

<script>
export default {}
</script>