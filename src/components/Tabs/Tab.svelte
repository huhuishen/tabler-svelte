<script>
    export let selected = undefined;
    export let id = null;
</script>

{#if selected === id}
    <div class="tab-pane active show" {id}>
        <slot />
    </div>
{/if}
