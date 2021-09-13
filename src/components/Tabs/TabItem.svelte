<script>
    export let id = "";
    export let href = "";
    export let selected = undefined;
    export let text = "";
</script>

<li class="nav-item">
    <a
        {href}
        class="nav-link{selected === id ? ' active' : ''}"
        on:click={() => (selected = id)}
        on:click><slot>{text}</slot></a
    >
</li>
