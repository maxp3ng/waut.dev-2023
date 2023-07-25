
<!-- <script> import { onMount } from 'svelte' ; import { goto } from '@roxi/routify' ; onMount ( ( ) => { setTimeout ( ( ) => { goto ( '/home' ) ; } , 5000 ) ; } ) ; </script> -->

<script>

</script>

<div class="w-full h-full bg-black absolute z-40 fadeOut">

</div>

<video class="w-full h-full absolute z-50 fadeOut" id="splash-screen"  autoplay muted>

<source src="splash.mp4" type="video/mp4">

Your custom message or video.mp4 is not supported.

</video>


<style>
    .fadeOut{ animation: fade 20s; }

    @keyframes fade {
        0% { opacity: 1; }
        70% { opacity: 1; }
        100% { opacity: 0; }
    }

</style>