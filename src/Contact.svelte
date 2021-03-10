<script>
    let menu = [
        {id: 0, text: "Choose a product..."},
        {id: 1, text: "Budinupi"},
        {id: 2, text: "Tortupi"},
        {id: 3, text: "Galletupi"},
        {id: 4, text: "Tartelupi"},
        {id: 5, text: "Custom"}
    ];

    let selected = {id: 0, text: ""};
</script>

<section id="contact">
    <div class="contactImageMobileContainer"><img src="img/contacto_but.png" alt="contact" class="contactImageMobile"></div>
    <form id="form">
        <h3 class="subtitle">Order</h3>
        <input placeholder="Enter your full name..." required />
        <input placeholder="Enter your email..." required />
        <input type="number" placeholder="Enter your phone..." required />
        <select bind:value={selected} class="input">
            {#each menu as choice}
                <option value={choice}>
                    {choice.text}
                </option>
            {/each}
        </select>
        {#if selected.id > 4}
            <textarea placeholder="Enter your order... i.e. -Budinupi 1" class="input" required />
        {:else if selected.id > 0}    
            <input type="number" placeholder="Enter the amount..." required />
        {/if}
        <button>Order</button>
    </form>
    <img src="img/contacto_but.png" alt="contact" class="contactImage">
    <form id="form">
        <h3 class="subtitle">Contact Us</h3>
        <input type="email" placeholder="Enter your email..." required />
        <input type="text" placeholder="Enter the subject..." required />
        <textarea placeholder="Enter your query..." class="input" required />
        <button>Send</button>
    </form>
</section>

<style>
    #contact{
        position: relative;
        width: 100vw;
        min-height: 100vh;
        background: #15e8e5;
        background-size: cover;
        z-index: 100;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        padding: 25px;
    }

    #form{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        min-height: 50vh;
        min-width: 250px;
        width: 30vw;
        background: #2a2b2c;
        z-index: 110;
        border-radius: 10px;
        margin-top: auto;
        margin-bottom: auto;
        box-shadow: 0 0 15px #000;
        margin: 25px;
    }

    h3{
        text-align: center;
        color: #15e8e5;
    }

    .subtitle{
        font-size: 30px;
    }

    input, .input{
        width: 75%;
        margin-left: auto;
        margin-right: auto;
        resize: vertical;
        min-height: 50px;
        max-height: 200px;
        background: #1a1b1c;
        border: none;
        outline: none;
        color: #fafafa;
        border-bottom: 2px solid #fafafa;
        border-radius: 0;
        transition: 1s;
    }

    input:focus, .input:focus{
        border-bottom: 2px solid #15e8e5;
    }

    textarea{
        height: 100px;
    }

    button{
        width: 50%;
        margin-left: auto;
        margin-right: auto;
        background: #15e8e5;
        border-radius: 10px;
        font-weight: bold;
    }

    .contactImage{
        margin-top: auto;
        margin-bottom: auto;
        height: 50vh;
        width: 25vw;
        min-width: 250px;
    }

    .contactImageMobileContainer{
        display: none;
    }


    /*---Delete arrows from number input---*/
    /* Chrome, Safari, Edge, Opera */
    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
    }

    /* Firefox */
    input[type=number] {
    -moz-appearance: textfield;
    }

    @media screen and (max-width: 875px){
        .contactImage{
            display: none;
        }

        .contactImageMobileContainer{
            display: block;
            width: 100%;
            height: 100px;
            display: flex;
            justify-content: center;
        }

        .contactImageMobile{
            display: block;
            width: 100px;
            height: 100px;
        }
    }
</style>