<script>
	import Carousel from './Carousel.svelte';
    import Gallery from './Gallery.svelte';
    import Menu from './Menu.svelte';
    import Contact from './Contact.svelte';
    import Footer from './Footer.svelte';

    const images = [
        {path: 'img/menu/carousel1.png', id: 'image1'},
        {path: 'img/menu/carousel2.jpeg', id: 'image2'},
        {path: 'img/menu/carousel3.jpeg', id: 'image3'},
        {path: 'img/menu/carousel4.png', id: 'image4'},
        {path: 'img/menu/carousel5.jpeg', id: 'image5'},
        {path: 'img/menu/carousel6.jpeg', id: 'image6'},
        {path: 'img/menu/carousel7.jpeg', id: 'image7'}
    ];

    const galleryImages = [
        {path: 'img/menu/carousel1.png', id: 'image1'},
        {path: 'img/menu/carousel2.jpeg', id: 'image2'},
        {path: 'img/menu/carousel3.jpeg', id: 'image3'},
        {path: 'img/menu/carousel4.png', id: 'image4'},
        {path: 'img/menu/carousel5.jpeg', id: 'image5'},
        {path: 'img/menu/carousel6.jpeg', id: 'image6'},
        {path: 'img/menu/carousel7.jpeg', id: 'image7'},
        {path: 'img/menu/carousel5.jpeg', id: 'image8'},
        {path: 'img/menu/carousel6.jpeg', id: 'image9'},
        {path: 'img/menu/carousel7.jpeg', id: 'image10'}
    ]
</script>

<main>
    <Carousel 
        {images}
    />
    <Gallery 
        {galleryImages} 
    />
    <Menu />
    <Contact />
    <Footer />
</main>

<style>
    main{
        width: 100vw;
        margin: 0;
        padding: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        overflow-x: hidden;
    }

    
</style>
