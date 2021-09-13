<script>
    import Checkbox from "../Checkbox.svelte";

    export let checkbox = false;
    export let index = undefined;
    export let item = {};
    export let columns = [];
    export let group = [];
</script>

<tr>
    {#if checkbox}
        <td>
            <Checkbox
                value={index}
                aria="Select invoice"
                classes="m-0 align-middle"
                bind:group
            />
        </td>
    {/if}
    {#each columns as column, i}
        <td>
            {#if column.component}
                <svelte:component
                    this={column.component}
                    {...column.componentProps
                        ? column.componentProps(item)
                        : {}}
                />
            {:else if column.value}
                {@html column.value(item)}
            {:else}
                {@html item[column.field]}
            {/if}
        </td>
    {/each}
    <!-- <td class="text-end">
        <span class="dropdown">
            <button
                class="btn dropdown-toggle align-text-top"
                data-bs-boundary="viewport"
                data-bs-toggle="dropdown">Actions</button
            >
            <div class="dropdown-menu dropdown-menu-end">
                <a class="dropdown-item" href="#"> Action </a>
                <a class="dropdown-item" href="#"> Another action </a>
            </div>
        </span>
    </td> -->
</tr>
