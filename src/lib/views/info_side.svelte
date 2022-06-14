<script>
import ListYear from "../components/list_year.svelte";
// import Timeline from "../components/timeline.svelte";

</script>

<div class="container">
    <h1 class="name">MANUEL BELGRANO</h1>
    <span class="article">Hagamos un recorrido por la vida del prócer Argentino.</span>
    <ListYear/>
</div>


<style>
    .container {
        display: flex;
        flex-direction: column;
        
        align-items: flex-start;
        justify-content: start;
        margin: 20px 0 0px 0;
        background-color: #3C6F8E;
    }

    .name {
        font-size: 54pt;
        color: #fff;
        font-family: 'Anton';
        margin: 0;
        font-weight: 500;
    }

    .article {
        font-size: 20pt;
        color: #fff;
        font-family: 'Open sans', sans-serif;
        font-weight: 300;
    }
</style>