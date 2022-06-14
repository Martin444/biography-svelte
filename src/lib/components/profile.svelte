<script>
    import Manu from '../../assets/agapitalogo.jpeg';
</script>

<img src={Manu} class="manuel" alt="manuel" />

<style>
    .manuel {
        width: 25em;
        height: 15em;
        margin: 30px;
        border-radius: 20px;
        /* position: absolute; */
        box-shadow: 0px 10px 30px 10px rgba(0, 0, 0, 0.2);
    }
    
    @media(max-width: 700px) {
        .manuel {
            width: 30vw;
            height: 30vw;
            object-fit: cover;
            border-radius: 15%;
            margin: 0;
            z-index: 9999;
        }
    }
    </style>