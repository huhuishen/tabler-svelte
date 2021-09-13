<script>
    import TabItem from "./TabItem.svelte";

    export let selected = undefined;
    export let items = [];
</script>

<div class="card">
    <ul class="nav nav-tabs">
        {#each items as item}
            <TabItem bind:selected id={item.id} text={item.text} />
        {/each}
    </ul>
    <div class="card-body">
        <div class="tab-content">
            <slot />
        </div>
    </div>
</div>
