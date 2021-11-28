<script>
    import me from '../assets/jarolin-vargas.svg';
    import Bio from '../components/Bio.svelte';
</script>

<div class="general-container">
    <div class="content-container">
        <div>
            <img src={me} alt="Jarolin Vargas"/>
        </div>
        <Bio/>
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
</style>