<script>
    export let value = "";
    export let label = "";
    export let placeholder = "";
    export let disabled = false;
    export let readonly = false;
</script>

<div class="mb-3">
    <!-- svelte-ignore a11y-label-has-associated-control -->
    <label class="form-label">{label}</label>
    <input
        type="text"
        class="form-control"
        name="example-text-input"
        {placeholder}
        {disabled}
        {readonly}
        bind:value
    />
</div>
