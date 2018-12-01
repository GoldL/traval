- 码云
- [viewport](https://www.cnblogs.com/2050/p/3877280.html)
- reset.css
- 1像素边框
- fastclick
- iconfont
- git
```
git clone url // 克隆项目
git status // 查看当前状态和哪些文件被修改过
git diff // 查看修改内容
git add . // 添加到本地缓存
git commit -m 'project init' // 提交本地 
git push // 提交线上
git pull // 拉分支
git checkout inder-swper // 切换
git merge origin/index-swiper // 合并分支
git branch // 查看分支
```
- [npm切换到淘宝](https://blog.csdn.net/quuqu/article/details/64121812)
```
// 临时使用
npm --registry https://registry.npm.taobao.org install express
// 永久使用
npm config set registry https://registry.npm.taobao.org
```
- vue-awesome-swiper
- [占位宽高](https://segmentfault.com/a/1190000004231995)
```
overfolw: hidden
width: 100%
height: 0
padding-bottom 31.25%

// 样式穿透
 .wrapper >>> swiper-pagination-active
    background: red
```
- `min-width: 0`
- 代理
```
proxyTable: {
    '/api': {
    target: 'http://localhost:8080',
    pathRewrite: {
      '^/api': 'static/mock'
    }
}
```
- 联动
```
handleTouchStart () {
  this.touchStatus = true
},
handleTouchMove (e) {
  if (this.touchStatus) {
    let startY = this.$refs['A'][0].offsetTop
    let touchY = e.touches[0].clientY - 79
    let index = Math.floor((touchY - startY) / 20)
    if (index >= 0 && index <= this.letters.length) {
      this.$emit('change', this.letters[index])
    }
  }
},
handleTouchEnd () {
  this.touchStatus = false
}
```
- 性能优化
```
设置一个timer
if (this.timer) {
  clearTimeout(this.timer)
}
this.timer = setTimeout(() => {
  // 处理相关操作
}, 16)
```
- `keep-alive`保存状态
```
// 当唤醒状态时调用方法。
activated () {
if (this.lastcity !== this.city) {
  this.lastcity = this.city
  this.getHomeInfo()
}
}
```
- css穿透
```
.container >>> .swiper-container
  overflow inherit
```
- vue动画
```
<template>
  <transition>
    <slot></slot>
  </transition>
</template>

<script>
export default {
  name: 'FadeAnimation'
}
</script>

<style lang="stylus" scoped>
.v-enter, .v-leave-to
  opacity 0
.v-enter-active, .v-leave-active
  transition opacity 0.5s
</style>
```
- header渐隐渐现
```
methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
},
// 对scroll监听
mounted () {
    window.addEventListener('scroll', this.handleScroll)
},
// 移除监听
unmounted () {
    window.removeEventListener('scroll', this.handleScroll)
}
```
- 嵌套组件
```
// 在自身标签里直接引用自己命名name。

<template>
  <div>
    <div
      class="item"
      v-for="(item, index) in list"
      :key="index">
        <div
          class="item-title border-bottom">
            <span class="item-title-icon"></span>
            {{item.title}}
        </div>
        <div v-if="item.children" class="item-children">
          <detail-list :list="item.children"></detail-list>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>
```