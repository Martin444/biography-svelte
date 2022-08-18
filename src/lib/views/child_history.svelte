<script>
    import Profile from "../components/profile.svelte";
    import M1 from '../../assets/manuelito1.jpeg'
    import M2 from '../../assets/M2.jpeg'
    import M3 from '../../assets/M3.jpeg'
    import M4 from '../../assets/M4.jpeg'
    import M5 from '../../assets/M5.jpeg'
    import M6 from '../../assets/M6.jpeg'
    import M7 from '../../assets/M7.jpeg'
    import M8 from '../../assets/M8.jpeg'
    import M9 from '../../assets/M9.jpeg'
    import M10 from '../../assets/M10.jpeg'
    import M11 from '../../assets/M11.jpeg'
    import M12 from '../../assets/m1763.jpeg'
    import M13 from '../../assets/m1810.jpeg'

</script>
<div class="box-vtn">
    <div class="scroll-ctn">
        <div class="item">
            <img src="{M3}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M12}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M5}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M2}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M1}" alt="m1"/>
        </div>

        <div class="item">
            <img src="{M6}" alt="m1"/>
        </div>

        <div class="item">
            <img src="{M8}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M9}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M10}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M11}" alt="m1"/>
        </div>
        <div class="item">
            <img src="{M13}" alt="m1"/>
        </div>

    </div>
</div>

<style>

    .box-vtn {
        box-sizing: border-box;
    }

    .scroll-ctn {
        display: flex;
        overflow-x: scroll;
        padding: 24px;
        scroll-snap-type: x mandatory;
        scroll-padding: 24px;
        border-radius: 20px;
        gap: 12px;
    }

    .scroll-ctn .item {
        flex: 0 0 100%;
        padding: 0;
        margin: 2px;
        border-radius: 4pc;
        scroll-snap-align: start;
    }

    .item img {
        width: 100%;
        height: max-content;
    }
    
    @media(max-width: 700px) {
        .box-vtn {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        .scroll-ctn {
            display: flex;
            overflow-x: scroll;
            padding: 0px;
            scroll-snap-type: x mandatory;
            scroll-padding: 24px;
            border-radius: 10px;
            gap: 12px;
        }

        .scroll-ctn .item {
            flex: 0 0 95%;
            padding: 0;
            margin: 2px;
            border-radius: 4pc;
            scroll-snap-align: start;
        }

        .item img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

    }
</style>