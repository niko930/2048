<template>
  <div id="app">
    <ul id="wrap">
      <span class="scort">总分：{{scort}}</span>
      <li class='box'
          v-for="num in nums"
          v-text="num"
          v-getclass="num"
          track-by="$index">
      </li>
    </ul>

    <div class="mask" v-show='show===1' @click='show=0' transition='show'>
      <div>{{msg}}</div>
    </div>
    <button @click="reset">重置</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      scort : 0,
      show : 0,
      msg : '',
      nums : [],

    }
  },
  mounted() {
  }


}
</script>

<style>
  @import url(./main.css);
</style>
