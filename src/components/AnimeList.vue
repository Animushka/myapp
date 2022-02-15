<template>
    <v-simple-table fixed-header
    height="50%" width="auto" dark
    >
    <template v-slot:default>
      <thead>
        <tr>
         <th class="text-left" target="_blank">
            Картинка
          </th>
          <th class="text-left">
            Название
          </th>
          <th class="text-left">
            Название на русском
          </th>
          <th class="text-left" target="_blank">
            Сылка
          </th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in animelist"
          :key="item.id">
          <td>
            <v-img class="grey lighten-2"
                height="auto"
                width="50%"
                :src="`https://shikimori.one${item.image.original}`"
            ></v-img>
          </td>
          <td>{{ item.name }}</td>
           <td>{{ item.russian }}</td>
          <td>
            <v-btn 
                target="_blank" 
                :href="`https://shikimori.one${item.url}`"
                >
            Link</v-btn>
          </td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
</template>

<script> 

import Vue from 'vue';
import axios from 'axios'
import VueAxios from 'vue-axios'


Vue.use(VueAxios, axios)
export default {
    name: "AnimeList",
    data()
    {
        return {
            animelist:[]}
    },
    update()
    {
        this.$emit('update-data', updateData())
    },
    mounted()
    { 
        this.$nextTick(function updateData() {
            Vue.axios.get('https://shikimori.one/api/animes?order=random&limit=5')
            .then((resp)=>{
            this.animelist=resp.data
            })
        })
    }
}
</script>