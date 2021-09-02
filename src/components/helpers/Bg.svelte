<script>
    export let slug;
    export let name;
</script>
<div class="flex coinbg"><amp-img layout="flex-item" src="https://img.okno.rs/coins/256/{slug}256.png" alt="{name} BackGround"></amp-img></div>
<style>
    .coinbg{
        position:fixed;
        width: 100%;
        height:100%;
        filter: blur(2px) opacity(0.24);
        -webkit-filter:  blur(2px) opacity(0.24);
        pointer-events:none;
        bottom:-1.62vh;
        left:-1.62vh;
        transform: scale(4) translate(2vh, 0) skew(38deg, 0deg);
        z-index:-1;
    }
</style>
