<template>
  <div class="searchlist">
  <form @submit.prevent="search">
    <input class="input-songs" type="text" v-model="query" placeholder="Search for a song" />
    <button type="submit" class="button-search">Search</button>
  </form>
  <div v-if="results">
    <ul class="results">
      <li v-for="result in results" :key="result.id">
        <div class="songs">
          <div class="portrait">
          <img :src="result.album.images[0].url" alt="Album cover" class="portrait-img"/>
          {{ result.name }} by {{ result.artists[0].name }}
          </div>
        </div>
      </li>
    </ul>
  </div>
  </div>
</template>



<script setup>
import { ref, watchEffect } from 'vue'
import axios from 'axios'
import '../assets/styles/SearchList.css'

const query = ref('')
const results = ref(null)
const token = ref('')


const CLIENT_ID = 'b94ff936eb4b484397fabf9f5822d61d'
const CLIENT_SECRET = '23237797c4354eae8b699e6691d8efa2'
watchEffect(() => {
  let parametrosAutor = {
    method: 'POST',
    headers: {
      'Content-Type': 'application/x-www-form-urlencoded'
    },
    body: 'grant_type=client_credentials&client_id=' + CLIENT_ID + '&client_secret=' + CLIENT_SECRET
  }
  fetch('https://accounts.spotify.com/api/token',parametrosAutor)
      .then(result => result.json())
      .then(data => token.value = data.access_token)
})


const search = async () => {
  const response = await axios.get(`https://api.spotify.com/v1/search?type=track&q=${query.value}`, {
    headers: {
      'Authorization': `Bearer ${token.value}`
    }
  })
  results.value = response.data.tracks.items
  console.log(results)
}
</script>