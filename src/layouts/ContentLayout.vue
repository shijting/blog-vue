<template>
  <div class="my-mt">
    <div class="container">
      <div class="row">
        <div  class="col-12 col-sm-12 col-md-9 home pl-0">
          <router-view></router-view>
        </div>
        <Sidebar></Sidebar>
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from '../components/sidebar/Sidebar'
export default {
  name: 'ContentLayout',
  components: {
    Sidebar
  },
  created () {
    // console.log('status1', this.status)
  },
  computed: {
    getStatus () {
      let status = this.$store.state.contentLoader.showContent
      console.log('status', status)
      return status
    }
  }
}
</script>

<style  lang="less" scoped>
.container {
  padding: 0;
}
</style>
