<template>
  <div class="home">
    <Staff v-bind:note="note" />
    <NoteReveal v-bind:note="note" v-on:nextNote="nextNote"/>
  </div>
</template>

<script>
// @ is an alias to /src
import NoteReveal from '@/components/NoteReveal.vue';
import Staff from '@/components/Staff.vue';
import notes from '../notes';

function nextNote(notesList) {
  if (! notesList || notesList.length === 0) {
    notesList = [].concat(notes);
  }
  const index = Math.floor(Math.random() * notesList.length);
  const note = notesList[index];
  notesList.splice(index, 1);

  return {
    note,
    notesList
  };
}

export default {
  name: 'home',
  components: {
    NoteReveal,
    Staff,
  },

  data() {
    const { note, notesList } = nextNote();

    return {
      note,
      notesList,
    };
  },

  methods: {
    nextNote() {
      const { note, notesList } = nextNote(this.notesList);

      this.note = note;
      this.notesList = notesList;
    },
  },
};
</script>
