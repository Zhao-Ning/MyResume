<template>
  <section>
    <h2>{{ model.label }}</h2>
    <ul class="info url-con">
      <li v-for="item in model.data">
        {{ item.label }} <a target="_blank" :href="item.url">{{ item.url }}</a>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'urlItem',
  props: {
    model: {
      type: Object
    }
  },
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../common/stylus/variable";

  .url-con 
    padding-left: 20px
    li
      list-style: none
      line-height: 24px
</style>