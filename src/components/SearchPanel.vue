<template>
    <form @submit.prevent="search">
        <input class="input-songs" type="text" v-model="query" placeholder="Search for a song" />
        <button type="submit" class="button-search">Search</button>
   </form>
</template>

<script>
export default {

}
</script>

<style>

</style>