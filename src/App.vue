<template>
  <v-app style="
    background-image: url('https://free4kwallpapers.com/uploads/originals/2021/05/09/anime-scenery-of-bluish-cloud-wallpaper.jpg');
     /* background-color: #8f2c2c; */
    height: 100vh;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;">
    <v-app-bar
      app
      color="gray"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="My logo"
          class="shrink mr-2"
          contain
          src="https://icons-for-free.com/download-icon-shikimori-1324440229724855502_512.png"
          transition="scale-transition"
          width="50"
        />

        <v-img
          alt="Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://www.userlogos.org/files/logos/32637_njio/shiki_dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://shikimori.one"
        target="_blank"
        text
      >
        <span class="mr-2">Сайт shikimori</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-btn
                block
                rounded
                class="mb-1"
                color="white"
                background="black"
                @update-data="updateData"
               >
             <span class="mr-2">Случайный выбор аниме</span>
        </v-btn>
      <v-container 
      > <AnimeList/> </v-container>
    </v-main>
     <v-bottom-navigation v-model="value"
      background-color="#272727">
       <v-btn value="Devloper" 
       align="left"
       href="https://vk.com/grigori_kov" 
       target="_blank" color="blue">
       <span class="ma-0">Разработчик</span>
        <v-img class="shrink mt-1 hidden-sm-and-down"
         max-height="25"
         max-width="25" 
         src="https://upload.wikimedia.org/wikipedia/commons/2/21/VK.com-logo.svg"/>
    </v-btn>
    </v-bottom-navigation>
  </v-app>    
</template>

<script>
import AnimeList from './components/AnimeList'

export default {
  name: 'App',

  components: {
    AnimeList,
  },
  data: () => ({
  }),
  methods:
  {
    
  }
};
</script>
