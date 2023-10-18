<template>
  <div>Bar Slug is: {{ bar }}</div>
</template>

<script>
export default {
  name: "BarSlug",
  async asyncData({ params, store, route, auth }) {
    console.log(params);
    const bar = params.bar.toLowerCase();
    return { bar: bar };
  },
  data() {
    return {
      bar: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>
