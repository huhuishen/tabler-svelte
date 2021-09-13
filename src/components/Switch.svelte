<script>
    export let disabled = false;
    export let value = "";
    export let checked = false;
</script>

<label class="form-check form-switch">
    <input
        class="form-check-input"
        type="checkbox"
        {disabled}
        {value}
        bind:checked
    />
    <span class="form-check-label"><slot /></span>
</label>
