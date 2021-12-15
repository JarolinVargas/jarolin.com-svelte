<script>
    import me from '../assets/jarolin-vargas.svg';
    import Bio from '../components/Bio.svelte';
</script>

<div class="general-container">
    <div class="content-container">
        <div class="me-col">
            <img src={me} alt="Jarolin Vargas"/>
        </div>
        <div style="align-self: center;">
            <Bio/>
        </div>
    </div>
</div>

<style>
    img {
        position: absolute;
        height: 110%;
        left: -100px;
        bottom: -30px;
        z-index: 5;
    }

    @media screen and (max-width: 940px) {
        .content-container {
            grid-template-columns: 1fr;
        }

        .me-col {
            height: fit-content;
            border-bottom: 3px solid hsla(0,0%,100%,.03);
            background-color: rgba(0, 0, 0, 0.2);
        }

        img {
            position: relative;
            height: 300px;
            left: 10px;
            right: 0;
            bottom: 0px;
            margin: 0 auto;
            vertical-align: bottom;
        }
    }
</style>