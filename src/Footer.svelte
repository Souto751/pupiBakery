<script>

</script>

<div class="footer">
    <div class="infoDiv">
        <h4 class="color centered">Pupi's Bakery</h4>
        <p class="color">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis inventore minima eius id alias? Voluptatibus recusandae velit natus enim, fugiat voluptatum non, deleniti accusamus doloribus repellendus ducimus laboriosam sequi quae?</p>
        <p class="color centered">pupi@bakery.com</p>
    </div>
    <div class="openDiv">
        <h4 class="color centered">Open Hours</h4>
        <div class="dayDiv">
            <p class="color">Monday</p>
            <p class="color">8:00 - 19:00</p>
        </div>
        <div class="dayDiv">
            <p class="color">Tuesday</p>
            <p class="color">8:00 - 19:00</p>
        </div>
        <div class="dayDiv">
            <p class="color">Wednesday</p>
            <p class="color">8:00 - 19:00</p>
        </div>
        <div class="dayDiv">
            <p class="color">Thursday</p>
            <p class="color">8:00 - 19:00</p>
        </div>
        <div class="dayDiv">
            <p class="color">Friday</p>
            <p class="color">8:00 - 19:00</p>
        </div>
    </div>
</div>

<style>
    .footer{
        position: relative;
        width: 100%;
        min-height: 200px;
        height: auto;
        background: #2a2b2c;
        z-index: 100;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 50px;
    }

    .infoDiv{
        width: 30%;
        min-width: 200px;
    }

    .openDiv{
        width: 15%;
        min-width: 200px;
    }

    .color, .centered{
        text-align: center;
        color: #eee;
    }

    .dayDiv{
        display: flex;
        justify-content: space-between;
        height: 45px;
        margin-top: -15px;
    }
</style>