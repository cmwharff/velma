<script lang="ts">
    import { onDestroy, onMount } from "svelte";

    onMount(() => {
        document.getElementsByTagName("index")[0].classList.add("site");
        document.getElementsByTagName("directory")[0].classList.add("site");
        return () => {
            document.getElementsByTagName("index")[0].classList.remove("site");
            document
                .getElementsByTagName("directory")[0]
                .classList.remove("site");
        };
    });
</script>

<div class="text site">
    <iframe
        src="https://enes100.umd.edu"
        title="tools"
        height="100%"
        width="100%"
        style="background-color: #121B21;"
        sandbox="true allow-same-origin allow-scripts"
    ></iframe>
</div>

<style>
    .text {
        height: 100vh;
        margin: 0;
    }
</style>
