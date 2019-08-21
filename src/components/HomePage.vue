<template>
  <h3>{{ title }}</h3>

</template>

<script>
export default {
  name: 'HomePage',
  props: ['title']
}
</script>

<style scoped>
    h3 {
        margin: 40px 0 0;
        font-size: 40px;
    }
</style>
