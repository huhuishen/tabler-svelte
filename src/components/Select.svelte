<script>
    export let options = [];
    export let selected;
</script>

<select bind:value={selected} class="form-select">
    {#each options as item}
        <option value={item.value ? item.value : item}
            >{item.text ? item.text : item}</option
        >
    {/each}
</select>
