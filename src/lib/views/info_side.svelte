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
        margin: 20px 0 0px 0;
        z-index: 1;
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
    @media(max-width: 700px) {
        .container {
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .name {
            font-size: 23pt;
            text-align: center;
            
        }
        
        .article {
            font-size: 12pt;
            text-align: center;
        }
    }
</style>