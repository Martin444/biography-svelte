<script>
    import { link } from 'svelte-routing';
    import ButtonPrimary from '../components/button_primary.svelte';
    import ManuelitoImg from '../../assets/manuelito.jpg';

    let messageManuelito = `Hola joven patriota`;
</script>

<div class="container-manuelito">
    <h1 class="title">BELGERANISIMO</h1>
    <div class="bubble-container">
        <div class="bubble b r hb">
                <p class="messagito">
                    {messageManuelito}
                </p>
        </div>
    </div>
    <img src={ManuelitoImg} alt="manuelito" class="manuel-img"/>
    <p class="item-desc">
        Demos un paseo por la historia.
    </p>
    <a href="/manuel" use:link>
        <ButtonPrimary/>
    </a>
</div>

<style>

    .title {
        position: absolute;
        font-size: 3em;
        top: 10%;
        font-weight: bold;
        color: #fff;
        margin-bottom: 20px;
        z-index: 1;
    }
    .messagito {
        padding: 10px;
        display: block;
        font-family: monospace;
        margin: 0;
        /* border-right: 4px solid #000; */
        width: 20ch;
        animation: typing 2s steps(40), blink .5s infinite step-end alternate;
        overflow: hidden;
    }

    @keyframes typing {
        from {
            width: 0;
        }
    }

    @keyframes blink {
        50% {
            border-color: transparent;
        }
    }


    .container-manuelito {
        background-color: white;
        border-radius: 10px;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .manuel-img {
        width: 20vw;
        height: auto;
    }


    .b {
        border: 0.5vmin solid black;
    }

    .r {
        border-radius: 100%;
    }

    .hb::before {
        content: "";
        display: block;
        position: absolute;
    }

    .bubble {
        width: 20vw;
        height: 25%;
        left: 63%;
        top: 11vh;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        font-size: 3vmin;
        background: #ffd;
        box-shadow: 0 -0.25vmin, 0 0.125vmin;
        font-family: "Comic Sans", "Comic Neue", sans-serif;
    }

    .bubble-container {
        position: absolute;
        top: 42%;
        left: 67%;
        transform: translate(-70%, -50%);
        width: fit-content;
        height: 57vmin;
    }

    .bubble::before {
        width: 40%;
        height:20%;
        top: 13%;
        border-radius: 50%;
        left: -25%;
        box-shadow: 0.5vmin 0, 2vmin -0.5vmin #ffd, 2vmin -0.5vmin 0 0.5vmin;
        clip-path: polygon(0% 49%, 130% 48%, 150% 100%, 0% 100%);
    }

    @media (max-width: 1000px) {
        .bubble {
            width: 10em;
        }
        .bubble-container {
            top: 45%;  
            left: 66%;
        }
        
        .item-desc {
            padding: 10px;
            font-family: monospace;
            white-space: nowrap;
            text-align: center;
            font-size: 15pt;
            margin: 0;
            width: 30ch;
            animation: typing 2s steps(40), blink .5s infinite step-end alternate;
            overflow: hidden;
        }
    }

    @media (max-width: 830px) {
        .bubble {
            width: 10em;
        }
        .bubble-container {
            top: 47%;  
            left: 70%;
        }
    }

    @media (max-width: 730px) {
        .bubble {
            width: 10em;
        }

        .bubble-container {
            top: 49%;  
            left: 74vw;
        }

  
    }


    .item-desc {
        padding: 10px;
        font-family: monospace;
        white-space: nowrap;
        text-align: center;
        font-size: 4vmin;
        margin: 0;
        width: 30ch;
        animation: typing 2s steps(40), blink .5s infinite step-end alternate;
        overflow: hidden;
    }

</style>