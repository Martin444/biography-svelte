<script>
  import Background from './lib/components/background.svelte';
  import Home from './lib/views/home.svelte';
  import { Router, Route } from 'svelte-routing';
import OtherPage from './lib/views/other_page.svelte';
import NextTime from './lib/views/next_time.svelte';
import ChildHistory from './lib/views/child_history.svelte';
</script>

<main>
  <Router>
    <Route path='/' component="{OtherPage}"/>
    <Route path='/manuel' component="{Home}"/>
    <Route path='/proximamente' component="{NextTime}"/>
    <Route path='/manuelito' component="{ChildHistory}"/>
    <Background></Background>
  </Router>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
  
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell,   'Open Sans', 'Helvetica Neue', sans-serif;
    background-color: #3C6F8E;
    overflow: auto;
  }

  main::-webkit-scrollbar{
    width: 0px;
    overflow: auto;
    /* background: transparent; */
    background-color: #3C6F8E;
  }
  
  main {
    padding: 20px;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: calc(100vh - 40px);
    flex-direction: row;
  }


</style>
