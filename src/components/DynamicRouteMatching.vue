<template>
  <div>USER: {{$route.params.id}}</div>
</template>

<script>
export default {
  name: "DynamicRouteMatching",
  watch: {
    $route(to, from) {
      console.log(`路由已经改变`);
    }
  }
};
</script>
