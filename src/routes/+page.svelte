<div class="text" id="Text">
    <h1>VELMA</h1>
    <div class="apps">
        <div class="app">
            <a href="/store">
                <img src="/img/store.png" alt="app" height="150px" />
            </a>
            School Store
        </div>
        <div class="app">
            <a href="/milestone">
                <img src="/img/milestone.png" alt="app" height="150px" />
            </a>
            Milestone 7
        </div>
        <div class="app">
            <a href="/maintenance">
                <img src="/img/maintenance.png" alt="app" height="150px" />
            </a>
            Maintenance
        </div>
        <div class="app">
            <a href="/tools">
                <img src="/img/tools.png" alt="app" height="150px" />
            </a>
            Tool Check
        </div>
        <div class="app">
            <a href="/queue">
                <img src="/img/queue.png" alt="app" height="150px" />
            </a>
            Help Queue
        </div>
        <div class="app">
            <a href="/docs">
                <img src="/img/docs.png" alt="app" height="150px" />
            </a>
            Documentation
        </div>
    </div>
</div>

<style>
    .apps {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }
    .apps .app {
        text-align: center;
        display: flex;
        flex-direction: column;
        height: auto;
        margin: 0% 5%;
        margin-bottom: 3%;
    }
    @media (max-width: 800px) {
        .apps {
            width: 75%;
        }
        .apps .app {
            width: 15vh;
        }
    }

    @media (min-width: 800px) {
        .apps {
            width: 100%;
        }
        .apps .app {
            width: 15vw;
        }
    }
</style>
