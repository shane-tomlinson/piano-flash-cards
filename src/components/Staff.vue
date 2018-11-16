<template>
  <div class="staff-container">
    <img class="staff" src="../assets/Grand_staff.svg" alt="Grand Staff"/>
    <img class="note" v-bind:class="note" src="../assets/quarter_note.svg" alt="Note"/>
  </div>
</template>

<script>
export default {
  name: 'Staff',
  props: {
    note: String,
  },
};
</script>

<style scoped lang="scss">

$treble-offset: 15px;
$bass-offset: 342px;
$note-interval: 18px;

.staff-container {
  height: 681px + 160px;
  width: 700px;
  display: block;
  margin: 0 auto;
  position: relative;

  > img {
    position: absolute;
    top: 0;
    left: 0
  }

  > .staff {
    padding-top: 160px;
    width: 100%;
  }

  > .note {
    left: 50%;
    height: 160px;
  }

  > .note-reverse {
    left: calc(50% + 32px);
    transform: rotateY(-180deg);
  }

  .treble-c3 {
    top: $treble-offset + ($note-interval * 0)
  }

  .treble-b3 {
    top: $treble-offset + ($note-interval * 1)
  }

  .treble-a3 {
    top: $treble-offset + ($note-interval * 2)
  }

  .treble-g2 {
    top: $treble-offset + ($note-interval * 3)
  }

  .treble-f2 {
    top: $treble-offset + ($note-interval * 4)
  }

  .treble-e2 {
    top: $treble-offset + ($note-interval * 5)
  }

  .treble-d2 {
    top: $treble-offset + ($note-interval * 6)
  }

  .treble-c2 {
    top: $treble-offset + ($note-interval * 7)
  }

  .treble-b2 {
    top: $treble-offset + ($note-interval * 8)
  }

  .treble-a2 {
    top: $treble-offset + ($note-interval * 9)
  }

  .treble-g1 {
    top: $treble-offset + ($note-interval * 10)
  }

  .treble-f1 {
    top: $treble-offset + ($note-interval * 11)
  }

  .treble-e1 {
    top: $treble-offset + ($note-interval * 12)
  }

  .treble-d1 {
    top: $treble-offset + ($note-interval * 13)
  }

  .treble-c1 {
    top: $treble-offset + ($note-interval * 14)
  }

  .treble-b1 {
    top: $treble-offset + ($note-interval * 15)
  }

  .treble-a1 {
    top: $treble-offset + ($note-interval * 16)
  }

  .bass-e3 {
    top: $bass-offset + ($note-interval * 0)
  }

  .bass-d3 {
    top: $bass-offset + ($note-interval * 1)
  }

  .bass-c3 {
    top: $bass-offset + ($note-interval * 2)
  }

  .bass-b3 {
    top: $bass-offset + ($note-interval * 3)
  }

  .bass-a3 {
    top: $bass-offset + ($note-interval * 4)
  }

  .bass-g2 {
    top: $bass-offset + ($note-interval * 5)
  }

  .bass-f2 {
    top: $bass-offset + ($note-interval * 6)
  }

  .bass-e2 {
    top: $bass-offset + ($note-interval * 7)
  }

  .bass-d2 {
    top: $bass-offset + ($note-interval * 8)
  }

  .bass-c2 {
    top: $bass-offset + ($note-interval * 9)
  }

  .bass-b2 {
    top: $bass-offset + ($note-interval * 10)
  }

  .bass-a2 {
    top: $bass-offset + ($note-interval * 11)
  }

  .bass-g1 {
    top: $bass-offset + ($note-interval * 12)
  }

  .bass-f1 {
    top: $bass-offset + ($note-interval * 13)
  }

  .bass-e1 {
    top: $bass-offset + ($note-interval * 14)
  }

  .bass-d1 {
    top: $bass-offset + ($note-interval * 15)
  }

  .bass-c1 {
    top: $bass-offset + ($note-interval * 16)
  }

  .bass-b1 {
    top: $bass-offset + ($note-interval * 17)
  }

  .bass-a1 {
    top: $bass-offset + ($note-interval * 18)
  }
}


</style>
