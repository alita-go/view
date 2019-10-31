<template>
  <div id="app" class="app_container app">
    <common-header :title="title" />
    <question/>
    <common-footer />
  </div>
</template>

<script>
/**
 * 首页
 */
import commonHeader from '@/components/common/Header'
import commonFooter from '@/components/common/Footer'
import Question from '@/components/Question'

export default {
  components: {
    commonHeader,
    commonFooter,
    Question
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
