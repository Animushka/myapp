<template>
  <v-container >
    <v-row class="white--text text-center">
      <v-col cols="12">
         <v-btn
                v-on:click="UpdateBtn"
                rounded
                class="mb-1"
                color="white"
                background="black"
               >
             <span class="mr-2">Случайный выбор аниме</span>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

  export default {
    name: 'UpdateBtn',
    data: () => ({
      return :true
    }),
  }
</script>
