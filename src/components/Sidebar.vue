<template>

  <div class="sidebar">
    <div v-if="notes.length">
      <note v-for="note in notes" :key="note.id" :note="note"></note>
    </div>
    <div class="sidebar__content" v-else>
      Boo, no notes... Write something
    </div>
    <div class="sidebar__content">
      <a href="#" @click.prevent="clearCurrentNote">Start a new note</a>
    </div>
  </div>

</template>

<script>
  import Note from './Note'
  import { mapGetters, mapActions } from 'vuex'

  export default {
    computed: {
      ...mapGetters([
        'notes'
      ])
    },

    methods: {
      ...mapActions([
        'clearCurrentNote'
      ])
    },

    components: {
      Note
    }
  }
</script>

<style lang="scss" scoped>

  .sidebar {
    background-color: #f9f9f9;
    flex: 1;
    height: 100%;
    max-width: 25%;
    border-right: 2px solid #eee;
    overflow-y: auto;

    &__content {
      padding: 30px;

      a {
        text-decoration: none;
        color:inherit;
      }
    }
  }

</style>
