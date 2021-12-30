<template>
  <div>
    <div style="position: fixed;top: 50px;left: 50px">
      <router-link class="text-router-link" to="/">home</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import { reactive } from 'vue'
import { useRouter } from 'vue-router'

export default {
  name: 'Default',
  setup() {
    const sourceOpitons = reactive([
      {
        title: 'github',
        link: 'https://github.com/originjs/origin.js'
      },
      {
        title: 'docs',
        link: 'https://originjs.github.io/docs/'
      }
    ])

    const router = useRouter()
    const { currentRoute } = router

    return { currentRoute, sourceOpitons }
  }
}
</script>
