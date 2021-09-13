<script>
    import Checkbox from "./Checkbox.svelte";

    export let disabled = false;
    export let items = [];
    export let group = [];
</script>

{#each items as item}
    <Checkbox
        {disabled}
        bind:group
        value={item.value}
        checked={group.includes(item.value)}
    >
        {item.text}
    </Checkbox>
{/each}
