<template lang="html">
  <div class="song-item">
    <div class="track">
      <div class="panel-block media">
        <div class="media-left">
          <img src="{{songs.images[0].url}}" alt="" class="track__media track__frame">
        </div>
        <div class="media-content">
          <h4 class="track__artist">{{songs.artists[0].name}}</h4>
          <p class="track__name">{{songs.name}}</p>
        </div>
        <div class="media-right">
          <a href="{{songs.href}}" class="fa fa-spotify track__frame"></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['songs'],

  data() {
    return {
    };
  },

  methods: {

  },
};
</script>
