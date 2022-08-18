<script>
    import data from '../../assets/manuel.json';
    export let yearSelected = data['data'][0]['year'];

    $: info = data['data'].filter(function(item) {
        return item['year'] == yearSelected;
    });
</script>

<div class="container">
    <!-- Left vertical line -->
    <div class="container__line"></div>
    
    <!-- The timeline items container -->
    <ul class="container__items">
        
        <!-- Each timeline item -->
        {#each info as moreInfo}   
            {#each moreInfo['info'] as detail} 
                <li class="container__item">
            <!-- The circle and title -->
                    <div class="container__top">
                        <!-- The circle -->
                        <div class="container__circle"></div>
                        <!-- The title -->
                        <div class="container__title">
                            <h2>{detail['legen']}</h2>
                            <div class="container-imagedetail">
                                <img src="{detail['imagesrc']}" alt="IMageIlustrrative" class="image-title">
                                <span class="detail-title">{detail['imagedescript']}</span>
                            </div>
                        </div>
                    </div>
                    <!-- <div class="container__desc">
                    </div> -->
                </li>
            {/each}
        {/each}
        
    </ul>
</div>

<style>
    .container {
        /* Used to position the left vertical line */
        position: relative;
        /* max-width: fit-content; */
        margin-top: 20px;
        /* overflow: auto; */
    }
    .container__line {
        /* Border */
        border-right: 2px dashed #fff;
        left: 12px;
        position: absolute;
        top: 0px;
        height: 100%;
    }

    .container__items {
        /* Reset styles */
        list-style-type: none;
        margin: 0px;
        padding: 0px;
    }
    .container__item {
        margin-bottom: 18px;
    }
    .container__top {
        /* Center the content horizontally */
        align-items: flex-start;
        display: flex;
    }
    .container__circle {
        /* Rounded border */
        background-color: #DBBB46;
        border-radius: 9999px;
        /* Size */
        height: 22px;
        width: 22px;
        margin-left: 2px;
        z-index: 99;
    }

    .container__title {
        /* flex:0; */
        display: flex;
        margin-left: 38px;
        padding: 20px;
        background: #4281a8;
        justify-content: start;
        align-items: flex-start;
        align-self: start;
        font-family: 'Open sans', sans-serif;
        color: #fff;
        font-size: 14pt;
        font-weight: 200;
        border-radius: 20px;
    }
    .container__title h2 {
        flex: 3;
        font-family: 'Open sans', sans-serif;
        color: #fff;
        text-align: justify;
        font-size: 17pt;
        font-weight: 200;
        border-radius: 20px;
    }
    .image-title {
        width: 100%;
        height: 300px;
        border-radius: 10px;
        object-fit: cover;
        margin-top: 10px;
        margin-bottom: 10px;
    }

    .detail-title {
        font-size: 14pt;
        font-weight: 200;
        font-family: 'Open sans', sans-serif;
        font-style: italic;
        margin-top: 10px;
        margin-bottom: 10px;
    }

    .container-imagedetail {
        flex: 3;
        width: 50%;
        margin-left: 20px;
    }
    @media (max-width: 700px) {
        .container {
            /* Used to position the left vertical line */
            max-width: 80%;
        }
        .container__title {
            flex: 5;
            margin-left: 10px;
            flex-direction: column;
            background: #4281a8;
            justify-content: center;
            align-items: center;
            align-self: center;
            font-family: 'Open sans', sans-serif;
            color: #fff;
            font-size: 14pt;
            font-weight: 200;
            border-radius: 20px;
        }
        .container__title h2 {
            flex: 3;
            font-family: 'Open sans', sans-serif;
            color: #fff;
            font-size: 14pt;
            font-weight: 200;
            border-radius: 20px;
        }
        .container-imagedetail {
            flex: 1;
            margin-left: 0px;
        }
    }
</style>