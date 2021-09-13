<script>
    export let disabled = false;
    export let value = "";
    export let group = "";
</script>

<label class="form-check">
    <input
        class="form-check-input"
        type="radio"
        {disabled}
        {value}
        bind:group
    />
    <span class="form-check-label"><slot /></span>
</label>
