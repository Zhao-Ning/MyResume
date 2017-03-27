<template>
  <section>
    <h2>{{ model.label }}</h2>
    <ul class="info">
      <li v-for="item in model.data">
        {{ item }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'Ability',
  props: {
    model: {
      type: Object
    }
  },
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../common/stylus/variable";


</style>