<template>
  <section>
    <h2>{{ model.label }}</h2>
    <div v-for="modelItemPro in model.allProData" class="projects">
      <h3>
        <span>{{ modelItemPro.companyDate.company }}</span> |
        <span>{{ modelItemPro.companyDate.position }}</span> |
        <span>{{ modelItemPro.companyDate.address }}</span> |
        <span>{{ modelItemPro.companyDate.date }}</span>
      </h3>
      <div class="project" v-for="modelItem in modelItemPro.proData">
        <div class="pro-title">
          <span class="pro-name">{{ modelItem.proTitle }}</span>
          <span class="pro-date">
           {{ modelItem.startTime }}
          </span>
          <a v-show="modelItem.proLink" target="_blank" :href="modelItem.proLink" class="pro-link">{{ modelItem.proLink }}</a>
        </div>
        <ul class="info">
          <li v-for="item in modelItem.data">
            {{ item }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'project',
  props: {
    model: {
      type: Object
    }
  },
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../common/stylus/variable";

  .pro-title
    margin-left: 15px
    border-left: 4px solid $borderColor
    & > span
      display: inline-block;
    .pro-name
      padding: 5px
      font-size: 20px
      font-weight: bold

</style>