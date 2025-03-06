<script>
    import "../lib/global.css";

    let visible = true;
    function toggleVisible() {
        visible = !visible;
    }
</script>

<div class="index">
    {#if visible}
        <div class="directory">
            <h3>Menu</h3>
            <p>
                <a href="./">Home</a>
                <a href="./store">School Store</a>
                <a href="./milestone">Milestone 7</a>
                <!-- <a href="/maintenance">Maintenance</a><br /> -->
                <a href="./tools">Tool Check</a>
                <!-- <a href="/queue">Help Queue</a> -->
                <a href="./docs">Documentation</a>
            </p>
        </div>
    {/if}
    <button id="bb" class="flipped" on:click={toggleVisible}>
        <img id="M" src="./img/M.png" alt="M" />
    </button>
</div>

<style>
    p {
        line-height: 30px;
    }
    a {
        font-weight: bold;
        color: white;
        margin: 5px;
    }
    a:hover {
        color: red;
    }
    h3 {
        font-size: 30px;
        margin: 20px 0px -10px 0px;
    }
    .index {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-basis: content;
    }
    .directory {
        height: auto;
        width: auto;
        background-color: rgba(255, 255, 255, 0.2);
        color: white;
        border: 0.5vw solid white;
    }
    button {
        background: none;
        border: none;
    }
    #bb {
        margin-left: 2%;
    }
    #M {
        height: 40px;
    }
    #bb.flipped {
        height: 4vh;
        transform: rotateY(180deg);
    }
    @media (max-width: 800px) {
        .index {
            flex-direction: column;
        }
        .directory {
            min-height: 12vh;
            width: 80vw;
            border-top: none;
            text-align: justify;
        }
        #M {
            margin: 2vw 0;
        }
        p {
            padding: 0% 10%;
        }
        h3 {
            padding: 0% 5%;
        }
    }
    @media (min-width: 800px) {
        .index {
            flex-direction: row;
        }
        .directory {
            width: 16vw;
            border-left: none;
        }
        #M {
            margin: 0 2vw;
        }
        p {
            padding: 0% 15%;
        }
        h3 {
            padding: 0% 10%;
        }
    }
</style>
