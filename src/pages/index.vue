<template>
  <router-view />
  <div class="router-link">
    <div>
      <router-link class="text-router-link" to="/202112">2021-12</router-link>
    </div>
    <div>
      <router-link class="text-router-link" to="/202201">2022-01</router-link>
    </div>
    <div>
      <router-link class="text-router-link" to="/202202">2022-02</router-link>
    </div>
    <div>
      <router-link class="text-router-link" to="/basic">basic</router-link>
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
