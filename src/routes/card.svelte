<script>
    import Select from "../components/Select.svelte";
    import Card from "../components/Card.svelte";
</script>

<div class="page-wrapper">
    <div class="container-xl">
        <!-- Page title -->
        <div class="page-header d-print-none">
            <div class="row align-items-center">
                <div class="col">
                    <h2 class="page-title">Cards</h2>
                </div>
            </div>
        </div>
    </div>
    <div class="page-body">
        <div class="container-xl">
            <div class="row row-cards">
                <div class="col-md-6 col-xl-4">
                    <div class="row row-cards">
                        <div class="col-12">
                            <Card>
                                <div class="card-body">
                                    <p>This is some text within a card body.</p>
                                </div>
                            </Card>
                        </div>
                        <div class="col-12 border-0">
                            <div class="card">
                                <div class="card-body">
                                    <p>This is a borderless card.</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="card-body">
                                    <h3 class="card-title">
                                        Card with bottom image
                                    </h3>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur
                                        adipisicing elit. Aperiam deleniti fugit
                                        incidunt, iste, itaque minima neque
                                        pariatur perferendis sed suscipit velit
                                        vitae voluptatem.
                                    </p>
                                </div>
                                <div
                                    class="card-img-bottom img-responsive img-responsive-16by9"
                                    style="background-image: url(./static/photos/56614e12b2a7bd68.jpg)"
                                />
                            </div>
                        </div>
                        <div class="col-12">
                            <Card active="true">
                                <div class="card-body">
                                    <p>This is a card with active state.</p>
                                </div>
                            </Card>
                        </div>
                        <div class="col-12">
                            <Card disabled="true">
                                <div class="card-body">
                                    <p>This is some text inactive state.</p>
                                </div>
                            </Card>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="card-body">
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur
                                        adipisicing elit. Aperiam deleniti fugit
                                        incidunt, iste, itaque minima neque
                                        pariatur perferendis sed suscipit velit
                                        vitae voluptatem.
                                    </p>
                                </div>
                                <!-- Card footer -->
                                <div class="card-footer">
                                    <div class="row align-items-center">
                                        <div class="col-auto">
                                            <a href="#">More information</a>
                                        </div>
                                        <div class="col-auto ms-auto">
                                            <label
                                                class="form-check form-switch m-0"
                                            >
                                                <input
                                                    class="form-check-input position-static"
                                                    type="checkbox"
                                                    checked="1"
                                                />
                                            </label>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="card-body">
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur
                                        adipisicing elit. Aperiam deleniti fugit
                                        incidunt, iste, itaque minima neque
                                        pariatur perferendis sed suscipit velit
                                        vitae voluptatem.
                                    </p>
                                </div>
                                <!-- Card footer -->
                                <div class="card-footer">
                                    <div class="row align-items-center">
                                        <div class="col-auto ms-auto">
                                            <div
                                                class="avatar-list avatar-list-stacked"
                                            >
                                                <span
                                                    class="avatar avatar-sm avatar-rounded"
                                                    style="background-image: url(./static/avatars/000m.jpg)"
                                                />
                                                <span
                                                    class="avatar avatar-sm avatar-rounded"
                                                    >JL</span
                                                >
                                                <span
                                                    class="avatar avatar-sm avatar-rounded"
                                                    style="background-image: url(./static/avatars/002m.jpg)"
                                                />
                                                <span
                                                    class="avatar avatar-sm avatar-rounded"
                                                    style="background-image: url(./static/avatars/003m.jpg)"
                                                />
                                                <span
                                                    class="avatar avatar-sm avatar-rounded"
                                                    style="background-image: url(./static/avatars/000f.jpg)"
                                                />
                                                <span
                                                    class="avatar avatar-sm avatar-rounded"
                                                    >+3</span
                                                >
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <ul class="nav nav-tabs card-header-tabs">
                                        <li class="nav-item">
                                            <a class="nav-link active" href="#">
                                                Active
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#">
                                                <!-- Download SVG icon from http://tabler-icons.io/i/star -->
                                                <svg
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    class="icon me-1"
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
                                                    /><path
                                                        d="M12 17.75l-6.172 3.245l1.179 -6.873l-5 -4.867l6.9 -1l3.086 -6.253l3.086 6.253l6.9 1l-5 4.867l1.179 6.873z"
                                                    /></svg
                                                >
                                                Link
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a
                                                class="nav-link disabled"
                                                href="#"
                                                tabindex="-1"
                                                aria-disabled="true"
                                            >
                                                Disabled
                                            </a>
                                        </li>
                                        <li class="nav-item ms-auto">
                                            <a class="nav-link" href="#">
                                                <!-- Download SVG icon from http://tabler-icons.io/i/settings -->
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
                                                    /><path
                                                        d="M10.325 4.317c.426 -1.756 2.924 -1.756 3.35 0a1.724 1.724 0 0 0 2.573 1.066c1.543 -.94 3.31 .826 2.37 2.37a1.724 1.724 0 0 0 1.065 2.572c1.756 .426 1.756 2.924 0 3.35a1.724 1.724 0 0 0 -1.066 2.573c.94 1.543 -.826 3.31 -2.37 2.37a1.724 1.724 0 0 0 -2.572 1.065c-.426 1.756 -2.924 1.756 -3.35 0a1.724 1.724 0 0 0 -2.573 -1.066c-1.543 .94 -3.31 -.826 -2.37 -2.37a1.724 1.724 0 0 0 -1.065 -2.572c-1.756 -.426 -1.756 -2.924 0 -3.35a1.724 1.724 0 0 0 1.066 -2.573c-.94 -1.543 .826 -3.31 2.37 -2.37c1 .608 2.296 .07 2.572 -1.065z"
                                                    /><circle
                                                        cx="12"
                                                        cy="12"
                                                        r="3"
                                                    /></svg
                                                >
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                                <div class="card-body">
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur
                                        adipisicing elit. Aperiam deleniti fugit
                                        incidunt, iste, itaque minima neque
                                        pariatur perferendis sed suscipit velit
                                        vitae voluptatem.
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="card-header">
                                    <ul class="nav nav-pills card-header-pills">
                                        <li class="nav-item">
                                            <a class="nav-link active" href="#">
                                                Active
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a class="nav-link" href="#">
                                                <!-- Download SVG icon from http://tabler-icons.io/i/star -->
                                                <svg
                                                    xmlns="http://www.w3.org/2000/svg"
                                                    class="icon me-1"
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
                                                    /><path
                                                        d="M12 17.75l-6.172 3.245l1.179 -6.873l-5 -4.867l6.9 -1l3.086 -6.253l3.086 6.253l6.9 1l-5 4.867l1.179 6.873z"
                                                    /></svg
                                                >
                                                Link
                                            </a>
                                        </li>
                                        <li class="nav-item">
                                            <a
                                                class="nav-link disabled"
                                                href="#"
                                                tabindex="-1"
                                                aria-disabled="true"
                                            >
                                                Disabled
                                            </a>
                                        </li>
                                        <li class="nav-item ms-auto">
                                            <a class="nav-link" href="#">
                                                <!-- Download SVG icon from http://tabler-icons.io/i/settings -->
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
                                                    /><path
                                                        d="M10.325 4.317c.426 -1.756 2.924 -1.756 3.35 0a1.724 1.724 0 0 0 2.573 1.066c1.543 -.94 3.31 .826 2.37 2.37a1.724 1.724 0 0 0 1.065 2.572c1.756 .426 1.756 2.924 0 3.35a1.724 1.724 0 0 0 -1.066 2.573c.94 1.543 -.826 3.31 -2.37 2.37a1.724 1.724 0 0 0 -2.572 1.065c-.426 1.756 -2.924 1.756 -3.35 0a1.724 1.724 0 0 0 -2.573 -1.066c-1.543 .94 -3.31 -.826 -2.37 -2.37a1.724 1.724 0 0 0 -1.065 -2.572c-1.756 -.426 -1.756 -2.924 0 -3.35a1.724 1.724 0 0 0 1.066 -2.573c-.94 -1.543 .826 -3.31 2.37 -2.37c1 .608 2.296 .07 2.572 -1.065z"
                                                    /><circle
                                                        cx="12"
                                                        cy="12"
                                                        r="3"
                                                    /></svg
                                                >
                                            </a>
                                        </li>
                                    </ul>
                                </div>
                                <div class="card-body">
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur
                                        adipisicing elit. Aperiam deleniti fugit
                                        incidunt, iste, itaque minima neque
                                        pariatur perferendis sed suscipit velit
                                        vitae voluptatem.
                                    </p>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="card-body">
                                    <h3 class="card-title">
                                        Card with progress bar
                                    </h3>
                                    <p>
                                        Lorem ipsum dolor sit amet, consectetur
                                        adipisicing elit. Aperiam deleniti fugit
                                        incidunt, iste, itaque minima neque
                                        pariatur perferendis sed suscipit velit
                                        vitae voluptatem.
                                    </p>
                                </div>
                                <div class="progress progress-sm card-progress">
                                    <div
                                        class="progress-bar"
                                        style="width: 38%"
                                        role="progressbar"
                                        aria-valuenow="38"
                                        aria-valuemin="0"
                                        aria-valuemax="100"
                                    >
                                        <span class="visually-hidden"
                                            >38% Complete</span
                                        >
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="empty">
                                    <div class="empty-img">
                                        <img
                                            src="./static/illustrations/undraw_quitting_time_dm8t.svg"
                                            height="128"
                                            alt=""
                                        />
                                    </div>
                                    <p class="empty-title">No results found</p>
                                    <p class="empty-subtitle text-muted">
                                        Try adjusting your search or filter to
                                        find what you're looking for.
                                    </p>
                                    <div class="empty-action">
                                        <a href="./." class="btn btn-primary">
                                            <!-- Download SVG icon from http://tabler-icons.io/i/search -->
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
                                                /><circle
                                                    cx="10"
                                                    cy="10"
                                                    r="7"
                                                /><line
                                                    x1="21"
                                                    y1="21"
                                                    x2="15"
                                                    y2="15"
                                                /></svg
                                            >
                                            Search again
                                        </a>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <!-- Cards with tabs component -->
                            <div class="card-tabs ">
                                <!-- Cards navigation -->
                                <ul class="nav nav-tabs">
                                    <li class="nav-item">
                                        <a
                                            href="#tab-top-1"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 1</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-top-2"
                                            class="nav-link active"
                                            data-bs-toggle="tab">Tab 2</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-top-3"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 3</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-top-4"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 4</a
                                        >
                                    </li>
                                </ul>
                                <div class="tab-content">
                                    <!-- Content of card #1 -->
                                    <div
                                        id="tab-top-1"
                                        class="card tab-pane show"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #1
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #2 -->
                                    <div
                                        id="tab-top-2"
                                        class="card tab-pane active"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #2
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #3 -->
                                    <div id="tab-top-3" class="card tab-pane">
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #3
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #4 -->
                                    <div id="tab-top-4" class="card tab-pane">
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #4
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <!-- Cards with tabs component -->
                            <div class="card-tabs border-0">
                                <!-- Cards navigation -->
                                <ul class="nav nav-tabs">
                                    <li class="nav-item">
                                        <a
                                            href="#tab-borderless-1"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 1</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-borderless-2"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 2</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-borderless-3"
                                            class="nav-link active"
                                            data-bs-toggle="tab">Tab 3</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-borderless-4"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 4</a
                                        >
                                    </li>
                                </ul>
                                <div class="tab-content">
                                    <!-- Content of card #1 -->
                                    <div
                                        id="tab-borderless-1"
                                        class="card tab-pane show"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #1
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #2 -->
                                    <div
                                        id="tab-borderless-2"
                                        class="card tab-pane"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #2
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #3 -->
                                    <div
                                        id="tab-borderless-3"
                                        class="card tab-pane active"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #3
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #4 -->
                                    <div
                                        id="tab-borderless-4"
                                        class="card tab-pane"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #4
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <!-- Cards with tabs component -->
                            <div class="card-tabs ">
                                <div class="tab-content">
                                    <!-- Content of card #1 -->
                                    <div
                                        id="tab-bottom-1"
                                        class="card tab-pane show"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #1
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #2 -->
                                    <div
                                        id="tab-bottom-2"
                                        class="card tab-pane"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #2
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #3 -->
                                    <div
                                        id="tab-bottom-3"
                                        class="card tab-pane"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #3
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                    <!-- Content of card #4 -->
                                    <div
                                        id="tab-bottom-4"
                                        class="card tab-pane active"
                                    >
                                        <div class="card-body">
                                            <div class="card-title">
                                                Content of tab #4
                                            </div>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Adipisci, alias aliquid
                                                distinctio dolorem expedita,
                                                fugiat hic magni molestiae
                                                molestias odit.
                                            </p>
                                        </div>
                                    </div>
                                </div>
                                <!-- Cards navigation -->
                                <ul class="nav nav-tabs nav-tabs-bottom">
                                    <li class="nav-item">
                                        <a
                                            href="#tab-bottom-1"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 1</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-bottom-2"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 2</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-bottom-3"
                                            class="nav-link"
                                            data-bs-toggle="tab">Tab 3</a
                                        >
                                    </li>
                                    <li class="nav-item">
                                        <a
                                            href="#tab-bottom-4"
                                            class="nav-link active"
                                            data-bs-toggle="tab">Tab 4</a
                                        >
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 col-xl-8">
                    <div class="row row-cards">
                        <div class="col-12">
                            <div class="card">
                                <div class="row row-0">
                                    <div class="col-3">
                                        <img
                                            src="./static/photos/2854fd67ddbd6217.jpg"
                                            class="w-100 h-100 object-cover"
                                            alt="Card side image"
                                        />
                                    </div>
                                    <div class="col">
                                        <div class="card-body">
                                            <h3 class="card-title">
                                                Card with left side image
                                            </h3>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Aperiam deleniti fugit incidunt,
                                                iste, itaque minima neque
                                                pariatur perferendis sed
                                                suscipit velit vitae voluptatem.
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card">
                                <div class="row row-0">
                                    <div class="col-3 order-md-last">
                                        <img
                                            src="./static/photos/de6d0fd1feebb6a2.jpg"
                                            class="w-100 h-100 object-cover"
                                            alt="Card side image"
                                        />
                                    </div>
                                    <div class="col">
                                        <div class="card-body">
                                            <h3 class="card-title">
                                                Card with right side image
                                            </h3>
                                            <p>
                                                Lorem ipsum dolor sit amet,
                                                consectetur adipisicing elit.
                                                Aperiam deleniti fugit incidunt,
                                                iste, itaque minima neque
                                                pariatur perferendis sed
                                                suscipit velit vitae voluptatem.
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="card-group">
                                <a
                                    href="#"
                                    class="card card-inactive text-center"
                                >
                                    <div class="card-body">
                                        <p>This is first card</p>
                                    </div>
                                </a>
                                <a
                                    href="#"
                                    class="card card-active text-center"
                                >
                                    <div class="card-body">
                                        <p>This is second card</p>
                                    </div>
                                </a>
                                <a href="#" class="card text-center">
                                    <div class="card-body">
                                        <p>This is third card</p>
                                    </div>
                                </a>
                            </div>
                        </div>
                        <div class="col-12">
                            <div class="row row-cards">
                                <div class="col-xl-6">
                                    <div class="row row-cards">
                                        <div class="col-12">
                                            <div class="card">
                                                <div
                                                    class="card-img-top img-responsive img-responsive-16by9"
                                                    style="background-image: url(./static/photos/9f36332564ca271d.jpg)"
                                                />
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with top image
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with button link
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                    <div class="card-text">
                                                        <a
                                                            href="#"
                                                            class="btn btn-primary"
                                                            >Go somewhere</a
                                                        >
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div
                                                    class="card-status-top bg-danger"
                                                />
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with top status
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div
                                                    class="card-status-bottom bg-success"
                                                />
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with bottom status
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div
                                                    class="card-status-start bg-primary"
                                                />
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with side status
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card card-stacked">
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Stacked card
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-body">
                                                    <div class="mb-3">
                                                        <div class="form-label">
                                                            Card number
                                                        </div>
                                                        <input
                                                            type="text"
                                                            name="input-mask"
                                                            class="form-control"
                                                            data-mask="0000 0000 0000 0000"
                                                            data-mask-visible="true"
                                                            autocomplete="off"
                                                        />
                                                    </div>
                                                    <div class="mb-3">
                                                        <div class="form-label">
                                                            Card name
                                                        </div>
                                                        <input
                                                            type="text"
                                                            class="form-control"
                                                        />
                                                    </div>
                                                    <div class="row">
                                                        <div class="col-8">
                                                            <div class="mb-3">
                                                                <label
                                                                    class="form-label"
                                                                    >Expiration
                                                                    date</label
                                                                >
                                                                <div
                                                                    class="row g-2"
                                                                >
                                                                    <div
                                                                        class="col"
                                                                    >
                                                                        <Select
                                                                            options={[
                                                                                1,
                                                                                2,
                                                                                3,
                                                                                4,
                                                                                5,
                                                                                6,
                                                                                7,
                                                                                8,
                                                                                9,
                                                                                10,
                                                                                11,
                                                                                12,
                                                                            ]}
                                                                            selected={3}
                                                                        />
                                                                    </div>
                                                                    <div
                                                                        class="col"
                                                                    >
                                                                        <Select
                                                                            options={[
                                                                                {
                                                                                    value: 2020,
                                                                                    text: "2020",
                                                                                },
                                                                                {
                                                                                    value: 2021,
                                                                                    text: "2021",
                                                                                },
                                                                            ]}
                                                                            selected={2021}
                                                                        />
                                                                    </div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                        <div class="col">
                                                            <div class="mb-3">
                                                                <div
                                                                    class="form-label"
                                                                >
                                                                    CVV
                                                                </div>
                                                                <input
                                                                    type="number"
                                                                    class="form-control"
                                                                />
                                                            </div>
                                                        </div>
                                                    </div>
                                                    <div class="mt-2">
                                                        <a
                                                            href="#"
                                                            class="btn btn-primary w-100"
                                                        >
                                                            Pay now
                                                        </a>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <div class="col-xl-6">
                                    <div class="row row-cards">
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card title
                                                    </h3>
                                                    <div class="card-subtitle">
                                                        Card subtitle
                                                    </div>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-header">
                                                    <h3 class="card-title">
                                                        Header title
                                                    </h3>
                                                </div>
                                                <div class="card-body">
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with footer
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                                <!-- Card footer -->
                                                <div class="card-footer">
                                                    This is standard card footer
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with footer button
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                                <!-- Card footer -->
                                                <div class="card-footer">
                                                    <a
                                                        href="#"
                                                        class="btn btn-primary"
                                                        >Go somewhere</a
                                                    >
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="card">
                                                <div class="card-body">
                                                    <h3 class="card-title">
                                                        Card with footer buttons
                                                    </h3>
                                                    <p>
                                                        Lorem ipsum dolor sit
                                                        amet, consectetur
                                                        adipisicing elit.
                                                        Aperiam deleniti fugit
                                                        incidunt, iste, itaque
                                                        minima neque pariatur
                                                        perferendis sed suscipit
                                                        velit vitae voluptatem.
                                                    </p>
                                                </div>
                                                <!-- Card footer -->
                                                <div class="card-footer">
                                                    <div class="d-flex">
                                                        <a
                                                            href="#"
                                                            class="btn btn-link"
                                                            >Cancel</a
                                                        >
                                                        <a
                                                            href="#"
                                                            class="btn btn-primary ms-auto"
                                                            >Go somewhere</a
                                                        >
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <footer class="footer footer-transparent d-print-none">
        <div class="container">
            <div class="row text-center align-items-center flex-row-reverse">
                <div class="col-lg-auto ms-lg-auto">
                    <ul class="list-inline list-inline-dots mb-0">
                        <li class="list-inline-item">
                            <a href="./docs/index.html" class="link-secondary"
                                >Documentation</a
                            >
                        </li>
                        <li class="list-inline-item">
                            <a href="./license.html" class="link-secondary"
                                >License</a
                            >
                        </li>
                        <li class="list-inline-item">
                            <a
                                href="https://github.com/tabler/tabler"
                                target="_blank"
                                class="link-secondary"
                                rel="noopener">Source code</a
                            >
                        </li>
                        <li class="list-inline-item">
                            <a
                                href="https://github.com/sponsors/codecalm"
                                target="_blank"
                                class="link-secondary"
                                rel="noopener"
                            >
                                <!-- Download SVG icon from http://tabler-icons.io/i/heart -->
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    class="icon text-pink icon-filled icon-inline"
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
                                    /><path
                                        d="M19.5 13.572l-7.5 7.428l-7.5 -7.428m0 0a5 5 0 1 1 7.5 -6.566a5 5 0 1 1 7.5 6.572"
                                    /></svg
                                >
                                Sponsor
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-12 col-lg-auto mt-3 mt-lg-0">
                    <ul class="list-inline list-inline-dots mb-0">
                        <li class="list-inline-item">
                            Copyright © 2021
                            <a href="." class="link-secondary">Tabler</a>. All
                            rights reserved.
                        </li>
                        <li class="list-inline-item">
                            <a
                                href="./changelog.html"
                                class="link-secondary"
                                rel="noopener">v1.0.0-beta3</a
                            >
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</div>
