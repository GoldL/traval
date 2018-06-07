<template>
  <div class="list">
    <div class="area">
      <div class="title border-topbottom">当前城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">热门城市</div>
      <div class="button-list">
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
        <div class="button-wrapper">
          <div class="button">北京</div>
        </div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">A</div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">阿拉蕾</div>
      </div>
    </div>
    <div class="area">
      <div class="title border-topbottom">B</div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
      <div class="item-list">
        <div class="item border-bottom">北京</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CityList'
}
</script>

<style lang="stylus" scoped>
.list
  .title
    line-height: .54rem
    background: #eee
    padding-left: .2rem
    color: #666
    font-size: .26rem
  .button-list
    overflow: hidden
    padding: .1rem .6rem .1rem .1rem
    .button-wrapper
      float: left
      width: 33.33%
      .button
        margin: .1rem
        padding: .1rem 0
        text-align: center
        border: .02rem solid #ccc
        border-radius: .06rem
  .item-list
  .item
    line-height: .76rem
    padding-left: .2rem
</style>
