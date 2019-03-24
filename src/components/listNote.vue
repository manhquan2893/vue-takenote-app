<template>
  <div class="listNote">
    <div class="notes">
      <div class="row header">Notes</div>
      <div v-for="(note,index) in notes" :key="index" class="row">{{note}}</div>
    </div>
    <div class="timestamp">
      <div class="row header">Timestamp</div>
      <div v-for="(timestamp,index) in timestamps" :key="index" class="row">{{timestamp}}</div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["notes", "timestamps"]
};
</script>
<style>
.listNote {
  display: flex;
  min-height: 250px;
  width: 500px;
  border: dotted 1px green;
  margin: auto;
  margin-bottom: 20px;
}
.row {
  width: 250px;
  text-align: center;
  padding: 5px 0;
}
.timestamp {
  border-left: dotted 1px green;
}
.header {
  font-weight: 700;
  font-size: 23px;
}
</style>