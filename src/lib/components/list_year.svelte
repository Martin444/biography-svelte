<script>
    import {fade} from 'svelte/transition';
    import data from '../../assets/manuel.json';
    import Timeline from './timeline.svelte';
    import YearTile from './year_tile.svelte';
    import { yearSelected } from '../store/store.js';
     
    let yearIsSelect = data['data'][0]['year'];

    function handleSelect(event) {
        yearSelected.update(n =>  n  = event.detail.year);
        yearSelected.subscribe(year => {
            // console.log(year);
            yearIsSelect = year;
        });
        // console.log(yearSelected);
    }

</script>

<div class="list">
    <ul transition:fade='{{ duration: 300}}'>
        {#each data['data'] as moor (moor['id'])}
            <YearTile year={moor['year']} on:onselect={handleSelect} select={yearIsSelect == moor['year']}></YearTile>
        {/each}
    </ul>

    <Timeline  yearSelected={yearIsSelect}/>

</div>

<style>
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
        margin-top: 20px;
        padding: 0;
    }

</style>