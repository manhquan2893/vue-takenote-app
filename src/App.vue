<template>
  <div id="app">
    <listNote :notes="notes" :timestamps="timestamps"></listNote>
    <inputComponent @add-note="addNote"></inputComponent>
    <showNum :counter="counter"></showNum>
  </div>
</template>
<script>
import listNote from "./components/listNote.vue";
import inputComponent from "./components/inputComponent.vue";
import showNum from "./components/showNum.vue";
export default {
  data() {
    return {
      notes: [],
      timestamps: [],
      counter: 0
    };
  },
  components: {
    listNote,
    inputComponent,
    showNum
  },
  methods: {
    addNote(event) {
      this.notes.push(event.note);
      this.timestamps.push(event.timestamp);
      this.counter++;
    }
  }
};
</script>