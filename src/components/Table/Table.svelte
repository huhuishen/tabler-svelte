<script>
    import Row from "./Row.svelte";
    import Checkbox from "../Checkbox.svelte";

    export let checkbox = false;
    export let columns = [];
    export let header = undefined;
    export let data = [];
    export let group = [];
    export let selectAll = false;
</script>

<div class="card">
    {#if header}
        <div class="card-header">
            <h3 class="card-title">{header}</h3>
        </div>
    {/if}

    <!-- <div class="card-body border-bottom py-3">
        <div class="d-flex">
            <div class="text-muted">
                Show
                <div class="mx-2 d-inline-block">
                    <input
                        type="text"
                        class="form-control form-control-sm"
                        value="8"
                        size="3"
                        aria-label="Invoices count"
                    />
                </div>
                entries
            </div>
            <div class="ms-auto text-muted">
                Search:
                <div class="ms-2 d-inline-block">
                    <input
                        type="text"
                        class="form-control form-control-sm"
                        aria-label="Search invoice"
                    />
                </div>
            </div>
        </div>
    </div> -->
    <div class="table-responsive">
        <table class="table card-table table-vcenter text-nowrap datatable">
            <thead>
                <tr>
                    {#if checkbox}
                        <th class="w-1">
                            <Checkbox
                                bind:value={selectAll}
                                aria="Select all invoice"
                                classes="m-0 align-middle"

                            />
                        </th>
                    {/if}
                    <th class="w-1"
                        >No. <!-- Download SVG icon from http://tabler-icons.io/i/chevron-up -->
                        <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="icon icon-sm text-dark icon-thick"
                            width="24"
                            height="24"
                            viewBox="0 0 24 24"
                            stroke-width="2"
                            stroke="currentColor"
                            fill="none"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            ><path
                                stroke="none"
                                d="M0 0h24v24H0z"
                                fill="none"
                            /><polyline points="6 15 12 9 18 15" /></svg
                        >
                    </th>
                    <th>Invoice Subject</th>
                    <th>Client</th>
                    <th>VAT No.</th>
                    <th>Created</th>
                    <th>Status</th>
                    <th>Price</th>
                    <th />
                </tr>
            </thead>
            <tbody>
                {#each data as item, index}
                    <slot name="item" {item} {index}>
                        <Row {index} {item} {columns} {checkbox} bind:group />
                    </slot>
                {/each}
            </tbody>
        </table>
    </div>
    <div class="card-footer d-flex align-items-center">
        <p class="m-0 text-muted">
            Showing <span>1</span> to <span>8</span> of <span>16</span> entries
        </p>
        <ul class="pagination m-0 ms-auto">
            <li class="page-item disabled">
                <a
                    class="page-link"
                    href="#"
                    tabindex="-1"
                    aria-disabled="true"
                >
                    <!-- Download SVG icon from http://tabler-icons.io/i/chevron-left -->
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="icon"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        stroke-width="2"
                        stroke="currentColor"
                        fill="none"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        ><path
                            stroke="none"
                            d="M0 0h24v24H0z"
                            fill="none"
                        /><polyline points="15 6 9 12 15 18" /></svg
                    >
                    prev
                </a>
            </li>
            <li class="page-item"><a class="page-link" href="#">1</a></li>
            <li class="page-item active">
                <a class="page-link" href="#">2</a>
            </li>
            <li class="page-item"><a class="page-link" href="#">3</a></li>
            <li class="page-item"><a class="page-link" href="#">4</a></li>
            <li class="page-item"><a class="page-link" href="#">5</a></li>
            <li class="page-item">
                <a class="page-link" href="#">
                    next <!-- Download SVG icon from http://tabler-icons.io/i/chevron-right -->
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        class="icon"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        stroke-width="2"
                        stroke="currentColor"
                        fill="none"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        ><path
                            stroke="none"
                            d="M0 0h24v24H0z"
                            fill="none"
                        /><polyline points="9 6 15 12 9 18" /></svg
                    >
                </a>
            </li>
        </ul>
    </div>
</div>
