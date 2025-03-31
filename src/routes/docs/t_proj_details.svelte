<script lang="ts">
    import Arena from "./proj_details/t_arena.svelte";
    import Awards from "./proj_details/t_awards.svelte";
    import MS5 from "./proj_details/t_ms5.svelte";
    import MS6 from "./proj_details/t_ms6.svelte";
    import MS7 from "./proj_details/t_ms7.svelte";
    import Product from "./proj_details/t_product.svelte";

    let tabs = [
        { name: "Arena Specifications", comp: Arena },
        { name: "Design Awards", comp: Awards },
        { name: "Milestone 5", comp: MS5 },
        { name: "Milestone 6", comp: MS6 },
        { name: "Milestone 7", comp: MS7 },
        { name: "Product Specifications", comp: Product }
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
        font: inherit;
    }
    button.selected {
        border-top-right-radius: 8px;
        border-top-left-radius: 8px;
        border-top-width: 8px;
        border-color: #e21833 #abc #fff;
    }
    .text {
        font-size: 1rem;
        display:block;
        background-color: white;
        margin: 0;
    }
</style>
