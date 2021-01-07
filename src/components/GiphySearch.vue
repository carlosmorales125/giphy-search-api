<template>
    <div class="section">
        <form @submit.prevent="executeSearchGiphy" class="field is-grouped">
            <div class="control is-expanded">
                <input v-model="searchText" class="input" type="text" placeholder="Find a repository">
            </div>
            <div class="control">
                <input type="submit" class="button is-info" value="Search" />
            </div>
        </form>

        <div class="section">

        </div>
    </div>
</template>
<script>
    import searchGiphy from '../api/search-giphy';

    export default {
        name: 'GiphySearch',
        data: () => {
            return {
                searchText: '',
            };
        },
        methods: {
            async executeSearchGiphy() {
                const giphyData = await searchGiphy(this.searchText);
                console.log(giphyData);
            },
        },
    };
</script>