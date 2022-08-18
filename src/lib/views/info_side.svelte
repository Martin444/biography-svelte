<script>
import ListYear from "../components/list_year.svelte";
import Aurora from '../../assets/cancionau.mp3'
import AudioPlayer from "../components/audio_player.svelte";

</script>

<div class="container">
    <h1 class="name" >MANUEL BELGRANO</h1>
    <span class="article">Hagamos un recorrido por la vida del prócer Argentino.</span>
    <AudioPlayer src={Aurora} />
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
            font-size: 27pt;
            text-align: center;
            
        }
        
        .article {
            font-size: 15pt;
            text-align: center;
        }
    }
</style>