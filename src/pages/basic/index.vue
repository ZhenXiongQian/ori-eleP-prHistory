<template>
  <router-view />
  <div class="router-link">
    <div>
      <router-link class="text-router-link" to="/basic/affix_basic"
        >affix_basic</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/alert_basic"
        >alert_basic</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/alert_description"
        >alert_description</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/avatar_fallback"
        >avatar_fallback</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/avatar_fit"
        >avatar_fit</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/badge_basic"
        >badge_basic</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/border_radius"
        >border_radius</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/badge_customize"
        >badge_customize</router-link
      >
    </div>
    <div>
      <router-link class="text-router-link" to="/basic/badge_max"
        >badge_max</router-link
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "Index",
};
</script>

<layout>
layout: home
</layout>
