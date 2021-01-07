<template>
  <div id="app" class="container">
    <Header/>
    <GiphySearch/>
  </div>
</template>

<script>
import Header from './components/Header';
import GiphySearch from './components/GiphySearch';

export default {
  name: 'App',
  components: {
    Header,
    GiphySearch,
  }
}
</script>

<style>
</style>
