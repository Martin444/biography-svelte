<script>
  import Background from './lib/components/background.svelte';
  import Home from './lib/views/home.svelte';
</script>

<main>
  <Home/>
  <Background></Background>
</main>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Anton&display=swap');
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell,   'Open Sans', 'Helvetica Neue', sans-serif;
    background-color: #3C6F8E;
    overflow: hidden;
  }

  main::-webkit-scrollbar{
    width: 0px;
    overflow: hidden;
    background: transparent;
  }
  
  main {
    height: 100vh;
    padding: 20px;
    margin: 0;
    display: flex;
    flex-direction: row;
    -ms-overflow-style: none;
    scrollbar-width: none;
    overflow-y: hidden; 
  }

    



  /* @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  } */
</style>
