<script>
    export let active = false;
    export let disabled = false;
</script>

<div
    class="card {active ? 'card-active' : ''} {disabled ? 'card-inactive' : ''}"
>
    <slot />
</div>
