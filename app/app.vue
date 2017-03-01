<template lang="html">
  <div class="app">
    <div class="section page">
        <div class="results">
          <div class="panel">
            <song-item v-for="item in tracks" v-bind:songs="item"></song-item>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import SongItem from './song-item.vue';

export default {

  components: {
    SongItem,
  },

  created() {
    fetch('https://api.spotify.com/v1/search?query=griz&type=track&offset=0&limit=20')
      .then(t => t.json())
      .then((trax) => {
        this.tracks = trax.tracks.items;
      });
  },

  data() {
    return {
      tracks: [
        {
          artists: [
            {
              name: 'GRiZ',
            }
          ],
          name: 'Get Down',
        },
      ]
    };
  },

  methods: {

  },
};
</script>
