<script>
  export let id = "";
  export let show = false;
  export let header = "";

  import { createEventDispatcher, onDestroy } from "svelte";

  const dispatch = createEventDispatcher();
  const close = () => dispatch("close");

  let modal;

  const handle_keydown = (e) => {
    if (e.key === "Escape") {
      close();
      return;
    }

    if (e.key === "Tab") {
      // trap focus
      const nodes = modal.querySelectorAll("*");
      const tabbable = Array.from(nodes).filter((n) => n.tabIndex >= 0);

      let index = tabbable.indexOf(document.activeElement);
      if (index === -1 && e.shiftKey) index = 0;

      index += tabbable.length + (e.shiftKey ? -1 : 1);
      index %= tabbable.length;

      tabbable[index].focus();
      e.preventDefault();
    }
  };

  const previously_focused =
    typeof document !== "undefined" && document.activeElement;

  if (previously_focused) {
    onDestroy(() => {
      previously_focused.focus();
    });
  }
</script>

<div
  class="modal modal-blur fade{show ? ' show modal-open' : ''}"
  {id}
  tabindex="-1"
  aria-modal="true"
  role="dialog"
  on:click={close}
>
  <div
    class="modal-dialog modal-lg modal-dialog-centered"
    role="document"
    bind:this={modal}
  >
    <div class="modal-content">
      <div  class="modal-header">
        <h5 class="modal-title">{header}</h5>
        <button
          type="button"
          class="btn-close"
          data-bs-dismiss="modal"
          aria-label="Close"
          on:click={() => {
            show = false;
          }}
        />
      </div>
      <div class="modal-body">
        <slot />
      </div>
      <div class="modal-body">
        <div class="row">
          <div class="col-lg-6">
            <div class="mb-3">
              <label class="form-label">Client name</label>
              <input type="text" class="form-control" />
            </div>
          </div>
          <div class="col-lg-6">
            <div class="mb-3">
              <label class="form-label">Reporting period</label>
              <input type="date" class="form-control" />
            </div>
          </div>
          <div class="col-lg-12">
            <div>
              <label class="form-label">Additional information</label>
              <textarea class="form-control" rows="3" />
            </div>
          </div>
        </div>
      </div>
      <div class="modal-footer">
        <a href="#" class="btn btn-link link-secondary" data-bs-dismiss="modal">
          Cancel
        </a>
        <a href="#" class="btn btn-primary ms-auto" data-bs-dismiss="modal">
          <!-- Download SVG icon from http://tabler-icons.io/i/plus -->
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
            ><path stroke="none" d="M0 0h24v24H0z" fill="none" /><line
              x1="12"
              y1="5"
              x2="12"
              y2="19"
            /><line x1="5" y1="12" x2="19" y2="12" /></svg
          >
          Create new report
        </a>
      </div>
      <div class="modal-footer">
        <button
          type="button"
          class="btn me-auto"
          on:click={() => {
            show = false;
          }}>Close</button
        >
        <button
          type="button"
          class="btn btn-primary"
          on:click={() => {
            show = false;
          }}>Save changes</button
        >
      </div>
    </div>
  </div>
</div>

<svelte:window on:keydown={handle_keydown} />

<!-- <div class="modal" role="dialog" aria-modal="true" >
  <slot name="header" />
  <hr />
  <slot />
  <hr />


  <button autofocus on:click={close}>close modal</button>
</div> -->
<style>
  :global(.modal-open) {
    display: block;
    overflow: hidden;
    padding-right: 0;
    background-color: #cdcdcd7a;
  }
</style>
