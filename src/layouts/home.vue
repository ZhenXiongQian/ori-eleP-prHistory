<template>
  <div>
    <div style="position: fixed;top: 30px;left: 30px">
      <img
          alt="Origin.js logo"
          src="../assets/originjs.png"
          class="logo logo-large"
          style="width: 50px;height: 50px"
      >
      <p>created by origin.js</p>
      <sources :list="sourceOpitons" />
    </div>

    <h2>pr demos for element-plus:</h2>
    <router-view />
    <p class="text-component-desc text-route">
      {{ $t("currentRoute") }}: '{{ currentRoute.fullPath }}'
    </p>
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
