<template>
  <div id="app" class="app_container app">
    <common-header :title="title" />
    <forum/>
    <common-footer />
  </div>
</template>

<script>
import commonHeader from '@/components/common/Header'
import commonFooter from '@/components/common/Footer'
import Forum from '@/components/Forum'

export default {
  components: {
    commonHeader,
    commonFooter,
    Forum
  },

  data() {
    return {
      title: ''
    }
  },

  async asyncData ({ params }) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          title: 'deepagent'
        })
      })
    });
  }
}
</script>
