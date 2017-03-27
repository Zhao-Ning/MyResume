<template>
  <section class="user-content border-2px">
    <div class="user-info">
      <div class="name">
        {{ model.name }}
        <span class="sex">({{ model.sex }}/{{ model.year }}岁)</span>
      </div>
      <div class="position">{{ model.position }}-{{ model.workTime }}</div>
    </div>
    <div class="user-info">
      <div class="info">
        {{ model.tel }}
      </div>
      <div class="info">
        {{ model.email }}
      </div>
      <div class="info">
        {{ model.major }}/{{ model.education }}
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'userInfo',
  props: {
    model: {
      type: Object
    }
  },
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
  @import "../common/stylus/variable";

  .user-content
    display: flex
    width: 100%
    height: 66px
    .user-info
      flex: 1
    .user-info:first-child
      background: $color
      color: $fontColor
      padding: 8px
      .name
        font-size: 26px
        & > .sex
          font-size: 16px
      .position
        font-size: 18px
        margin-top: 6px
    .info
      font-size: 16px
      line-height: 22px
      text-align: right

</style>
