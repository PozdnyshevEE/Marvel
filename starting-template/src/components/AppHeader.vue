<template>
    <nav class="navbar navbar-dark bg-dark">
        <div class="container-fluid">
            <a href="#" class="navbar-brand">Marvel</a>
            <form class="d-flex">
                <input class="form-control me-2" 
                type="search" 
                placeholder="Поиск" 
                aria-label="Search" 
                v-model="search" 
                @input="charactersSearch(search)" 
                @keypress.enter.prevent>
                <button class="btn btn-danger" 
                type="reset" 
                @click="search = ''; charactersSearch(search)">Искать</button>
            </form>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "AppHeader",
        props: ['charactersSearch'],
        data() {
            return {
                search: '',
            }
        },
    }
</script>

<style scoped>

</style>
