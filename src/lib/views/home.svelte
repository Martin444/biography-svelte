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
        justify-content: center;
        /* height: 100vh; */
        padding: 0;
        margin: 0;
        background-color: #3C6F8E;
    }

    @media(max-width: 700px) {
        section {
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
    }
</style>