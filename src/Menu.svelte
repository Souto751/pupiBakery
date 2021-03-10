<script>
    
</script>

<section id="menu">
    <h2>Menu</h2>
    <div class="budines">   <!--Change class name-->
        <h3>Budines</h3>   <!--Change txt-->
        <div class="justifyCards">
            <div class="menuCard">
                <img src="img/menu/budin.jpeg" alt="menu" class="menuCardImg"/>
                <div class="menuCardInfo">
                    <div class="menuCardInfoTop">
                        <p>Budinupi</p>
                        <p class="price">$500</p>
                    </div>
                    <div class="menuCardInfoBottom">
                        <p>Ingredients...</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="tortas">   <!--Change class name-->
        <h3>Tortas</h3>   <!--Change txt-->
        <div class="justifyCards">
            <div class="menuCard">
                <img src="img/menu/carousel4.png" alt="menu" class="menuCardImg"/>
                <div class="menuCardInfo">
                    <div class="menuCardInfoTop">
                        <p>Tortupi</p>
                        <p class="price">$900</p>
                    </div>
                    <div class="menuCardInfoBottom">
                        <p>Ingredients...</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="galletas">   <!--Change class name-->
        <h3>Galletas</h3>   <!--Change txt--> 
        <div class="justifyCards">
            <div class="menuCard">
                <img src="img/menu/cookie.jpeg" alt="menu" class="menuCardImg"/>
                <div class="menuCardInfo">
                    <div class="menuCardInfoTop">
                        <p>Galletupi</p>
                        <p class="price">$200 / kg</p>
                    </div>
                    <div class="menuCardInfoBottom">
                        <p>Ingredients...</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="tarteletas">   <!--Change class name-->
        <h3>Tartaletas</h3>   <!--Change txt-->
        <div class="justifyCards">
            <div class="menuCard">
                <img src="img/menu/tartaleta.jpeg" alt="menu" class="menuCardImg"/>
                <div class="menuCardInfo">
                    <div class="menuCardInfoTop">
                        <p>Tartelupi</p>
                        <p class="price">$325</p>
                    </div>
                    <div class="menuCardInfoBottom">
                        <p>Ingredients...</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    #menu{
        position: relative;
        width: 100vw;
        min-height: 100vh;
        background: #eee;
        z-index: 1000;
        padding-bottom: 50px;
    }

    h2, h3{
        text-align: center;
    }

    h2{
        text-align: center;
        font-family: 'Brush Script MT', cursive;
        font-size: 50px;
        line-height: 50px;
    }

    .budines{
        display: flex;
        flex-direction: column;
    }

    .menuCard{
        display: flex;
        width: 20vw;
        min-width: 200px;
        box-shadow: 0 0 10px #15e8e5;
        border-radius: 10px;
        min-height: 100px;
        transition: transform .2s;
    }

    .menuCard:hover {
        transform: scale(1.25);
    }

    .justifyCards{
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        width: 80%;
        margin-left: auto;
        margin-right: auto;
    }

    .menuCardImg{
        width: 80px;
        height: 80px;
        border-radius: 50%;
        margin: auto;
        margin-left: 7.5px;
    }

    .menuCardInfo{
        width: 70%;
        border-left: 2px solid #2a2b2c75;
        padding-left: 5px;
        padding-right: 5px;
        margin-left: 5px;
        display: flex;
        flex-direction: column;
    }

    .menuCardInfoTop{
        display: flex;
        justify-content: space-between;
        color: #2a2b2c;
        font-weight: bold;
    }

    .price{
        border-bottom: 1px solid #2a2b2c;
    }

    .menuCardInfoBottom{
        color: #2a2b2c;
        font-weight: bold;
        height: 50%;
        font-style: italic;
    }

    @media screen and (max-width: 1050px){
        .menuCardInfoTop{
            text-align: center;
            flex-direction: column;
        }

        .price{
            border-top: 1px solid #2a2b2c;
            text-align: center;
        }

        .menuCardInfoBottom{
            text-align: center;
            font-weight: 300;
        }

        .menuCard:hover {
            transform: scale(1.15);
        }
    }
</style>