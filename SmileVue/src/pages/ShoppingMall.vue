<template>
    <div>
      {{msg}}
      <van-row>
        <van-col span="8">span: 8</van-col>
        <van-col span="8">span: 8</van-col>
        <van-col span="8">span: 8</van-col>
      </van-row>
    </div>
</template>

<script>
export default {
  name: 'ShoppingMall',
  data () {
    return {
      msg: 'Shopping Mall'
    }
  }
}
</script>

<style scoped>

</style>
