<template>
  <div>
    <grid></grid>
  </div>
</template>

<script>
export default {
  components: {
    grid: () => import(/* webpackChunkName: "Index" */ './weather/WeatherGrid')
  },
  data: () => ({
    
  }),
};
</script>
