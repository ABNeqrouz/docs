<template>
  <div>
    <v-bottom-sheet>
      <v-btn slot="activator">Click me</v-btn>
      <v-list>
        <v-subheader>Open in</v-subheader>
        <v-list-tile v-for="tile in tiles" :key="tile.title" @click="">
          <v-list-tile-avatar>
            <v-avatar size="32px" tile>
              <img :src="`/static/doc-images/bottom-sheets/${tile.img}`" :alt="tile.title">
            </v-avatar>
          </v-list-tile-avatar>
          <v-list-tile-title>{{ tile.title }}</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-bottom-sheet>
  </div>
</template>

<script>
  export default {
    data: () => ({
      tiles: [
        { img: 'keep.png', title: 'Keep' },
        { img: 'inbox.png', title: 'Inbox' },
        { img: 'hangouts.png', title: 'Hangouts' },
        { img: 'messenger.png', title: 'Messenger' },
        { img: 'google.png', title: 'Google+' },
      ]
    })
  }
</script>
