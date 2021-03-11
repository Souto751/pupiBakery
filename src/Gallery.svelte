<script>
    export let galleryImages;
</script>

<section id="gallery">
    <h2>Gallery</h2>
    <div class="imageContainer">
    {#each galleryImages as image (image.id)}
        <img 
            src={image.path} 
            alt={image.id}
            class="image"
        />
    {/each}
    </div>
</section>

<style>
    #gallery{
        position:relative;
        width: 100vw;
        background: #14d2cf;
        z-index: 1000;
    }

    h2{
        text-align: center;
        font-family: 'Brush Script MT', cursive;
        font-size: 50px;
        line-height: 50px;
    }

    .imageContainer{
        display: flex;
        width: 100%;
        flex-wrap: wrap;
        justify-content: center;
    }

    .image{
        width: 20vw;
        height: 20vw;
        min-width: 100px;
        min-height: 100px;
    }
</style>