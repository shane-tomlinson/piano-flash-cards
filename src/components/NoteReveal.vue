<template>
  <div>
    <button @mousedown="show">Show</button>
    <div v-if="isVisible" class="note">{{formattedNote}}</div>
  </div>
</template>

<script>
const SHOW_TIME_MS = 1500;

export default {
  name: 'NoteReveal',

  data() {
    return {
      isVisible: false,
    };
  },

  computed: {
    formattedNote() {
      return this.note.split('-')[1].slice(0, 1).toUpperCase();
    },
  },

  props: {
    note: String,
  },

  methods: {
    show(e) {
      e.preventDefault();
      this.isVisible = true;
      setTimeout(() => {
        this.isVisible = false;
        this.$emit('nextNote');
      }, SHOW_TIME_MS);
    },
  },
};
</script>

<style scoped lang="scss">
.note {
  font-size: 40px;
  font-weight: 500;
}
</style>
