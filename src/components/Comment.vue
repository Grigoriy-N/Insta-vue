<template>
  <div class="comment">{{ text }}</div>
</template>

<script>
export default {
  props: ["text"]
};
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
}
.comment {
  padding-bottom: 15px;
  padding-left: 15px;
}
</style>
