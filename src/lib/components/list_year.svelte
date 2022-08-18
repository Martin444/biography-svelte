<script>
    import { link } from 'svelte-routing';
    import data from '../../assets/manuel.json';
    import Timeline from './timeline.svelte';
    import YearTile from './year_tile.svelte';
    import { yearSelected } from '../store/store.js';
     
    let yearIsSelect = data['data'][0]['year'];
    let y;

    function handleSelect(event) {
        yearSelected.update(n =>  n  = event.detail.year);
        yearSelected.subscribe(year => {
            // console.log(year);
            yearIsSelect = year;
        });
        // console.log(yearSelected);
    }

</script>

<div>
    <a href="/manuelito"  use:link>Mira la version para niños</a>
    <div class="list"> 
        <!-- TODO: Implementar una lista de años -->
        {#if y > 300}
        <ul class="sticked">
            {#each data['data'] as moor (moor['id'])}
                <YearTile year={moor['year']} on:onselect={handleSelect} select={yearIsSelect == moor['year']} ></YearTile>
            {/each}
        </ul>
    
        {:else}
        <ul >
            {#each data['data'] as moor (moor['id'])}
                <YearTile year={moor['year']} on:onselect={handleSelect} select={yearIsSelect == moor['year']} ></YearTile>
            {/each}
        </ul>
        {/if}
    
        <Timeline  yearSelected={yearIsSelect}/>
    
    </div>

</div>


<svelte:window bind:scrollY={y} />

<style>

    .sticked{
        width: fit-content;
        position: sticky;
        padding: 10px;
        z-index: 1;
        top: 0pc;
        background-color: #3C6F8E;
        right: 0;
    }
    .list {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        align-self: start;
        justify-content: start;
        margin: 0;
        padding: 0;
    }
    .list ul {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: start;
        margin: 0;
        /* margin-top: 20px; */
        padding: 0;
    }

    @media(max-width: 700px) {

        .sticked {
            width: fit-content;
            position: sticky;
            padding: 10px;
            z-index: 1;
            top: 0pc;
            background-color: transparent;
            right: 0;
        }

        .list {
            flex-direction: row;
            justify-content: center;
        }
        .list ul {
            flex-direction: column;
            align-items: center;
            overflow-y: auto;
        }
    }

</style>