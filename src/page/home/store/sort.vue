<template>
  <div class="container">
    <Select @changeText="changeText" />
  </div>
</template>
<script>
import Select from '@/components/select.vue'
export default {
  data(){
    return {
      tag: '全部',
    }
  },
  components: {
    Select
  },
  methods: {
    changeText(tag) {
      this.tag = tag
      this.$emit("changeText", 'sort', this.tag)
    }
  }
}
</script>
<style lang="sass" scoped>
</style>
