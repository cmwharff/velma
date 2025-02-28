<script>
    import Identity from "././t_identity.svelte";
    import Password from "././t_password.svelte";

    let tabs = [
        { name: "Identity", comp: Identity },
        { name: "Password", comp: Password },
    ];

    let cur = tabs[0];
</script>

<div class="text">
    {#each tabs as tab}
        <button class:selected={cur === tab} on:click={() => (cur = tab)}>
            {tab.name}
        </button>
    {/each}
    <svelte:component this={cur.comp} />
</div>

<style>
    button {
        cursor: pointer;
        padding: 0.5rem 1rem;
        border: 1px solid transparent;
        margin-bottom: -1px;
        background-color: #fff;
        border-bottom-color: #abc;
    }
    button.selected {
        border-top-right-radius: 8px;
        border-top-left-radius: 8px;
        border-top-width: 8px;
        border-color: #b0b #abc #fff;
    }
    .text {
        font-size: 1rem;
        padding: 2rem;
        display:block;
    }
</style>
