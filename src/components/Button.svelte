<script>
    export let href = "";
    export let type = "primary";
    export let active = false;
    export let disabled = false;
    export let outline = false;
    export let ghost = false;
    export let square = false;
    export let pill = false;
    export let icon = false;
    // export let handleClick = {};
</script>

<a
    {href}
    class="btn btn-{outline ? 'outline-' : ghost ? 'ghost-' : ''}{type} 
    {square ? 'btn-square' : ''}{pill ? 'btn-pill' : ''} {icon
        ? 'btn-icon'
        : ''}"
    class:active
    class:disabled
    on:click
>
    <slot />
</a>
