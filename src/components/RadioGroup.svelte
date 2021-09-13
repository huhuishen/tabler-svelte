<script>
    import RadioButton from "./Radio.svelte";

    export let disabled = false;
    export let items = [];
    export let group = "";
</script>

{#each items as item}
    <RadioButton {disabled} bind:group value={item.value}
        >{item.text}</RadioButton
    >
{/each}
