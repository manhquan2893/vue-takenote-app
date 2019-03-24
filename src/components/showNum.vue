<template>
  <div class="showNum">Count:{{counter}}</div>
</template>
<script>
export default {
  props: ["counter"]
};
</script>
<style >
.showNum {
  width: 50px;
  margin: auto;
}
</style>