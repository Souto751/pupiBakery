<script>
    let src = 'img/pupi_logo.png';
</script>

<header class="header">
    <img src={src} alt="bakery logo" class="logo" />
    <div class="linksDiv">
        <a href="#top" >Home</a>
        <a href="#gallery" >Gallery</a>
        <a href="#menu" >Menu</a>
        <a href="#contact" >Contact</a>
    </div>
</header>

<style>
    .header{
        position: fixed;
        z-index: 100;
        left: 0;
        top: 0;
        width: 100%;
        height: 100px;
        display: flex;
        justify-content: space-between;
    }

    .logo{
        height: 100%;
    }

    .linksDiv{
        height: 100%;
        display: flex;
        gap: 15px;
        margin-right: 15px;
    }

    a{
        color: #eee;
        text-decoration: none;
        font-size: 30px;
        line-height: 90px;
        font-weight: 500;
        font-family: Helvetica, Arial, sans-serif;
    }

    a:hover{
        color: #14d2cf;
    }

    @media screen and (max-width: 600px){
        .linksDiv{
            display: none;
        }
        
        .header{
            width: 100%;
            height: 175px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .logo{
            width: 150px;
            height: 100px;
            margin: auto;
        }
    }
</style>