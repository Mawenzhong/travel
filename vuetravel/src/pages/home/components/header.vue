<template>
<div class="btn">
<div class="btn-left">
<div class="iconfont back-icon">&#xe624;</div>
</div>
<div class="btn-input">
<span class="iconfont">&#xe632;</span>
输入城市/景点/游玩主题
</div>
<router-link to="/city" >
<div class="btn-right">
{{this.city}}
<span class="iconfont back-right">&#xe6aa;</span>
</div>
</router-link>
</div>
</template>
<script>
import {mapState} from 'vuex'
export default {
  name: 'homeheader',
  computed: {
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
 @import '~@/assets/styles/varbless.styl'
.btn
  display:flex
  height:.86rem
  background:$bgcolor
  color:#fff
  line-height:.86rem
.btn-left
  width:.64rem
  float:left
.back-icon
  text-align:center
  font-size:.4rem
.btn-input
  height:.64rem
  padding-left:.2rem
  line-height:.64rem
  margin-top:.12rem
  margin-left:.2rem
  flex:1
  background:#fff
  border-radius:.1rem
  color:#ccc
.btn-right
  min-width:1.24rem
  float:right
  text-align:center
  color:#fff
  padding:0 .1rem
.back-right
  font-size:.1rem
</style>
