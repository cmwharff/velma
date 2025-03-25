<script lang="ts">
    import Index from "$lib/Index.svelte";
    // import jQuery from "jquery";
</script>

<svelte:head>
    <title>VELMA</title>
</svelte:head>

<div class="page">
    <Index></Index>
    <slot></slot>
</div>
