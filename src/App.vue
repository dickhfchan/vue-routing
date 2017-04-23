<template>
  <div id="app">
      <md-whiteframe>
        <md-toolbar md-theme="blue">
        <md-button class="md-icon-button" @click.native="toggleLeftSidenav">
          <md-icon>menu</md-icon>
        </md-button>


          <h2 class="md-title" style="flex: 1">Green Safety</h2>


          <md-button class="md-icon-button">
            <md-icon>more_vert</md-icon>
          </md-button>

          <md-button class="md-icon-button">
            <md-icon>view_module</md-icon>
          </md-button>
        </md-toolbar>

      </md-whiteframe>
     

      <md-sidenav md-theme="blue" class="md-left" ref="leftSidenav" @open="open('Left')" @close="close('Left')">
          <md-toolbar class="md-large">
            <div class="md-toolbar-container">
              <h3 class="md-title">Green Safety</h3>
            </div>
          </md-toolbar>
          <div class="demo-drawer mdl-layout__drawer mdl-color--blue-grey-900 mdl-color-text--blue-grey-50">

          <div class="phone-viewport">
            <md-list>
              <md-list-item>
                <md-icon>whatshot</md-icon>
                <span>News</span>

                <md-list-expand>
                  <md-list>
                    <md-list-item class="md-inset">World</md-list-item>
                    <md-list-item class="md-inset">Americas</md-list-item>
                    <md-list-item class="md-inset">Europe</md-list-item>
                  </md-list>
                </md-list-expand>
              </md-list-item>

              <md-list-item>
                <md-icon>videogame_asset</md-icon>
                <span>Games</span>

                <md-list-expand>
                  <md-list>
                    <md-list-item class="md-inset">Console</md-list-item>
                    <md-list-item class="md-inset">PC</md-list-item>
                    <md-list-item class="md-inset">Phone</md-list-item>
                  </md-list>
                </md-list-expand>
              </md-list-item>

              <md-list-item>
                <md-icon>video_library</md-icon>
                <span>Video</span>

                <md-list-expand>
                  <md-list>
                    <md-list-item class="md-inset">Humor</md-list-item>
                    <md-list-item class="md-inset">Music</md-list-item>
                    <md-list-item class="md-inset">Movies</md-list-item>
                    <md-list-item class="md-inset">TV Shows</md-list-item>
                  </md-list>
                </md-list-expand>
              </md-list-item>

              <md-list-item href="http://localhost:8080/#/Users">
                <md-icon>users</md-icon>
                <span>Users</span>
              </md-list-item>

              <md-list-item href="http://localhost:8080/#/">
                <md-icon>home</md-icon>
                <span>Home</span>
              </md-list-item>

            </md-list>
          </div>

          </div>
      </md-sidenav>
 
       <router-view></router-view>
  </div>
</template>

<script>

export default {
  data () {
    return {
    }
  },
  methods: {
    toggleLeftSidenav() {
      this.$refs.leftSidenav.toggle();
    },
    toggleRightSidenav() {
      this.$refs.rightSidenav.toggle();
    },
    closeRightSidenav() {
      this.$refs.rightSidenav.close();
    },
    open(ref) {
      console.log('Opened: ' + ref);
    },
    close(ref) {
      console.log('Closed: ' + ref);
    }
  }
}



</script>

  <style src="vue-material/dist/vue-material.css">

</style>



