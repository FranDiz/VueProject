<template>
    <div>
        <Header />
        <div class="menu">
            <Dashboard />
            <SearchList />
        </div>
    </div>
</template>

<script>
import Header from "../components/Header.vue";
import SearchList from "../components/SearchList.vue";
import Dashboard from "../components/Dashboard.vue";

export default {
    components: {
        Header,
        SearchList,
        Dashboard,
    },
};
</script>

<style scoped>
.menu {
    display: flex;
    justify-content: space-between; /* Esto distribuirá los elementos a los extremos */
    padding: 1em;
    height: 100%;
    border: 4px solid #ccc;
}

</style>