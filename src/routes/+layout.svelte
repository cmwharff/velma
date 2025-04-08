<script lang="ts">
    import Index from "$lib/Index.svelte";
    import { onMount } from "svelte";

    onMount(() => {
        console.log(`index: ${window.document.getElementsByClassName("index")}`);
        window.document.getElementsByTagName("index")[0].classList.add("site");
        document.getElementsByTagName("directory")[0].classList.add("site");
        return () => {
            document.getElementsByTagName("index")[0].classList.remove("site");
            document
                .getElementsByTagName("directory")[0]
                .classList.remove("site");
        };
    });
</script>

<svelte:head>
    <title>VELMA</title>
</svelte:head>

<div class="page">
    <Index></Index>
    <slot></slot>
</div>
