<script>

import Profile from '../components/profile.svelte';
import InfoSide from './info_side.svelte';

</script>

<section>
    <Profile/>
    <InfoSide/>
       
</section>


<style>
    section {
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        justify-content: space-between;
        height: 100vh;
        padding: 0;
        margin: 0;
        background-color: #3C6F8E;
        overflow: none;
    }
</style>