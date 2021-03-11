<script>
    import {flip} from 'svelte/animate';
    import Header from './Header.svelte';
    export let images;

    const rotateRight = e =>{
        images = [...images.slice(1, images.length), images[0]];
    }

    function rotateRightAuto(){
        setTimeout(function(){
            rotateRight();
            rotateRightAuto();
        }, 7500);
    }

    rotateRightAuto();
    
</script>

<div class="carousel" id="top">
    <Header />
    <div id="darkenCarousel"></div>
    <div id="carousel-container">
        <div id="carousel-images">
            {#each images as image (image.id)}
                <img 
                    src={image.path} 
                    alt={image.id}
                    class="image"
                    animate:flip={{duration: 500}}
                />
            {/each}
        </div>
    </div>
</div>

<style>
    .carousel{
        position: relative;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        z-index: 100;
    }

    #carousel-container{
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        overflow: hidden;
    }

    #carousel-images{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .image{
        min-width: 100%;
        height: 100vh;
    }

    #darkenCarousel{
        width: 100vw;
        height: 100vh;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 1;
        background: #000a;
    }

    @media screen and (max-width: 600px){
        .carousel{
            height: auto;
            min-height: 175px;
        }

        .image{
            height: 100%;
            min-height: 175px;
        }
    }
</style>