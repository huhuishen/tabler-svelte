<script>
    // import { createEventDispatcher } from "svelte";

    export let value = "";
    export let aria = "";
    export let classes = "";
    export let label = "";
    export let checked = false;
    export let disabled = false;
    export let group = [];

    // bind:group doesn't work in component
    // also set prop checkbox state when group value change
    let groupstate = group.includes(value);

    $: {
        const groupHasValue = group.includes(value);

        // check if group array has changed, or something else
        if (groupHasValue === groupstate) {
            // add to group array if checked
            if (checked && !groupHasValue) {
                group = group.concat([value]);
                groupstate = true;
                // remove from group array if unchecked
            } else if (!checked && groupHasValue) {
                group = [...group.filter((v) => v !== value)];
                groupstate = false;
            }
        } else {
            // group array has changed. Click box
            groupstate = groupHasValue;
            check();
        }
    }

    // const dispatch = createEventDispatcher();

    function check() {
        checked = !checked;
        // dispatch("change", checked);
    }
</script>

{#if label}
    <label class="form-check">
        <input
            class="form-check-input {classes ? classes : ''}"
            type="checkbox"
            aria-label={aria}
            {disabled}
            {value}
            bind:checked
        />
        <span class="form-check-label"><slot>{label}</slot></span>
    </label>
{:else}
    <input
        class="form-check-input {classes ? classes : ''}"
        type="checkbox"
        aria-label={aria}
        {disabled}
        {value}
        bind:checked
    />
{/if}
