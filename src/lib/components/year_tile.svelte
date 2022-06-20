<script>
import { createEventDispatcher } from "svelte";
    export let year = '18';
    export let select = false;
    const dispatch = createEventDispatcher();
    export function selectYear() {
        dispatch("onselect",{ year: year });
    }
</script>


    {#if select}
        <div class='tile-select' on:click={selectYear}>
            <span>{year}</span>
        </div>
    {:else}
        <div class='tile' on:click={selectYear}>
            <span>{year}</span>
        </div>
    {/if}


<style>
    .tile {
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0;
        padding: 10px;
        background-color: transparent;
        border-radius: 10px;
        cursor: pointer;
    }
    .tile-select {
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 0;
        padding: 10px;
        background-color: #DBBB46;
        border-radius: 10px;
        cursor: pointer;
    }

    .tile:hover {
        transform: scale(1.1);
        transition: all 0.2s ease-in-out;
    }

    .tile-select:hover {
        box-shadow:  0 0 20px 0  rgba(255, 255, 255, 0.2);
    }

    .tile span {
        font-size: 1em;
        color: #fff;
        font-family: 'Open Sans', sans-serif;
        margin: 0;
        font-weight: 500;
    }

    .tile-select span {
        font-size: 1em;
        color: #fff;
        font-family: 'Open Sans', sans-serif;
        margin: 0;
        font-weight: 500;
    }

</style>