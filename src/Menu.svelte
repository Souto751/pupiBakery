<script>
    let budines = [         //Change name
        {id:"Budin 1", path:"img/menu/budin1.jpeg", price:350, ingredients:"Ingredients..."},
        {id:"Budin 2", path:"img/menu/budin2.jpeg", price:375, ingredients:"Ingredients..."},
        {id:"Budin 3", path:"img/menu/budin3.jpeg", price:330, ingredients:"Ingredients..."}
    ]
    
    let cookies = [         //Change name
        {id:"Cookie 1", path:"img/menu/cookie1.jpeg", price:125, ingredients:"Ingredients..."},
        {id:"Cookie 2", path:"img/menu/cookie2.jpeg", price:200, ingredients:"Ingredients..."},
        {id:"Cookie 3", path:"img/menu/cookie3.jpeg", price:170, ingredients:"Ingredients..."}
    ]

    
    let tarteletas = [         //Change name
        {id:"Tarteleta 1", path:"img/menu/tarteleta1.jpeg", price:240, ingredients:"Ingredients..."}
    ]

    
    let cakes = [         //Change name
        {id:"Cake 1", path:"img/menu/cake1.jpeg", price:500, ingredients:"Ingredients..."},
        {id:"Cake 2", path:"img/menu/cake2.png", price:530, ingredients:"Ingredients..."},
        {id:"Cake 3", path:"img/menu/cake3.jpeg", price:540, ingredients:"Ingredients..."}
    ]
</script>

<section id="menu">
    <h2>Menu</h2>
    <div class="budines">   <!--Change class name-->
        <h3>Budines</h3>   <!--Change txt-->
        <div class="justifyCards">
            {#each budines as budin}
                <div class="menuCard">
                    <img src={budin.path} alt="menu" class="menuCardImg"/>
                    <div class="menuCardInfo">
                        <div class="menuCardInfoTop">
                            <p>{budin.id}</p>
                            <p class="price">${budin.price}</p>
                        </div>
                        <div class="menuCardInfoBottom">
                            <p>{budin.ingredients}</p>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </div>
    <div class="tortas">   <!--Change class name-->
        <h3>Cakes</h3>   <!--Change txt-->
        <div class="justifyCards">
            {#each cakes as cake}
                <div class="menuCard">
                    <img src={cake.path} alt="menu" class="menuCardImg"/>
                    <div class="menuCardInfo">
                        <div class="menuCardInfoTop">
                            <p>{cake.id}</p>
                            <p class="price">${cake.price}</p>
                        </div>
                        <div class="menuCardInfoBottom">
                            <p>{cake.ingredients}</p>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </div>
    <div class="galletas">   <!--Change class name-->
        <h3>Cookies</h3>   <!--Change txt--> 
        <div class="justifyCards">
            {#each cookies as cookie}
                <div class="menuCard">
                    <img src={cookie.path} alt="menu" class="menuCardImg"/>
                    <div class="menuCardInfo">
                        <div class="menuCardInfoTop">
                            <p>{cookie.id}</p>
                            <p class="price">${cookie.price} / kg</p>
                        </div>
                        <div class="menuCardInfoBottom">
                            <p>{cookie.ingredients}</p>
                        </div>
                    </div>
                </div>
            {/each}
        </div>
    </div>
    <div class="tarteletas">   <!--Change class name-->
        <h3>Tarteletas</h3>   <!--Change txt-->
        <div class="justifyCards">
            {#each tarteletas as tarteleta}
                <div class="menuCard">
                    <img src={tarteleta.path} alt="menu" class="menuCardImg"/>
                    <div class="menuCardInfo">
                        <div class="menuCardInfoTop">
                            <p>{tarteleta.id}</p>
                            <p class="price">${tarteleta.price}</p>
                        </div>
                        <div class="menuCardInfoBottom">
                            <p>{tarteleta.ingredients}</p>
                        </div>
                    </div>
                </div>
            {/each}
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
        text-shadow: 0 0 5px #14d2cf;
    }

    h3{
        text-align: center;
        font-family: 'Brush Script MT', cursive;
        font-size: 40px;
        line-height: 40px;
    }

    .budines{
        display: flex;
        flex-direction: column;
    }

    .menuCard{
        display: flex;
        background: #eee;
        width: 20vw;
        min-width: 200px;
        box-shadow: 0 0 10px #14d2cf;
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
        gap: 20px;
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