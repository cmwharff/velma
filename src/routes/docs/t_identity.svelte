<!-- <iframe
    src="https://docs.google.com/document/d/1hVi1nHB-7MRBvupROdQRsrOxVAwHG8lm9MQs95gMiwc/"
    title="doc"
    style="width:100%; height:100%; top:-57px;background-color:white;overflow:hidden;"
></iframe> -->

<script>
    import Password from "./t_password.svelte";

    let tabs = [
        { name: "Password", comp: Password }
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
        display:block;
        background-color: white;
        margin: 0;
    }
</style>
