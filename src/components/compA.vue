<template>
  <div>
    <span>{{ msgg }}</span>
    <button @click="change">点击换字</button>
    <slot name="default"></slot>
  </div>
</template>

<script>
export default {
  name: 'comA',
  props: ['msg'],
  data() {
    return {
      msgg: this.msg,
      flag: false,
    }
  },
  methods: {
    change() {
      this.flag = !this.flag
      this.msgg = this.flag ? 'this is component A' : '这是组件A'
    },
  },
}
</script>
