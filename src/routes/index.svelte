<script>
  import RadioGroup from "../components/RadioGroup.svelte";
  import CheckboxGroup from "../components/CheckboxGroup.svelte";
  import Checkbox from "../components/Checkbox.svelte";
  import Modal from "../components/_Modal.svelte";
  import Button from "../components/Button.svelte";
  import Alert from "../components/Alert.svelte";
  import Pagination from "../components/_Pagination.svelte";
  import Table from "../components/_Table.svelte";
  import Tab from "../components/Tab.svelte";
  import Tabs from "../components/Tabs.svelte";
  import Switch from "../components/Switch.svelte";
  import Text from "../components/Text.svelte";
  import Icon from "../components/Icon.svelte";

  let radioValue = "1";
  let items = [
    { value: "1", text: "One scoop" },
    { value: "2", text: "Two scoop" },
  ];

  let items2 = [
    { value: "One scoop", text: "One scoop" },
    { value: "Two scoop", text: "Two scoop" },
  ];
  let checkValues = ["One scoop"];

  let show = false;

  let checked = false;
  let bag = { option1: true };
</script>

<div class="page-wrapper">
  <div class="container-xl">
    <!-- Page title -->
    <div class="page-header d-print-none">
      <div class="row align-items-center">
        <div class="col">
          <h2 class="page-title">Form Components</h2>
        </div>
      </div>
    </div>
  </div>
  <div class="page-body">
    <div class="container-xl">
      <h1><Icon name="user" /></h1>

      <Switch bind:checked={bag.option1}>Options1</Switch>
      {bag.option1}

      <Text bind:value={radioValue} label={"asdf"} placeholder={"asdf"} />

      <RadioGroup {items} bind:group={radioValue} />
      radioValue={radioValue}

      <Checkbox bind:checked value={"123"}>asdf</Checkbox>
      checked={checked}

      <Checkbox disabled bind:checked value={"123"}>asdf</Checkbox>
      checked={checked}

      <CheckboxGroup items={items2} bind:group={checkValues} />
      checkValues=[{checkValues}]

      <div class="card-body">
        <Button type="primary" href="form">primary</Button>
        <Button type="secondary" on:click={() => alert("asdf")}
          >secondary</Button
        >
        <Button type="success">success</Button>
        <Button type="warning">warning</Button>
        <Button type="danger">danger</Button>
        <Button type="info">info</Button>
        <Button type="light">light</Button>
        <Button type="dark">dark</Button>
        <Button type="primary"
          ><svg
            xmlns="http://www.w3.org/2000/svg"
            class="icon icon-tabler"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path stroke="none" d="M0 0h24v24H0z" fill="none" />
            <path d="M2 9a10 10 0 1 0 20 0" />
            <path d="M12 19a10 10 0 0 1 10 -10" />
            <path d="M2 9a10 10 0 0 1 10 10" />
            <path d="M12 4a9.7 9.7 0 0 1 2.99 7.5" />
            <path d="M9.01 11.5a9.7 9.7 0 0 1 2.99 -7.5" />
          </svg></Button
        >
      </div>

      <Alert type="warning">
        All icons come from the Tabler Icons set and are MIT-licensed. Visit
        <a href="https://tabler-icons.io" target="_blank">tabler-icons.io</a>,
        download the icons you need in SVG, PNG or React and use them in your
        favourite design tools.
      </Alert>


      <Table />
      <Pagination />

      <Button
        type="light"
        on:click={() => {
          show = !show;
        }}>Simple modal {show}</Button
      >
      <!-- <Modal bind:show header={"Modal title"}
    >Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci animi
    beatae delectus deleniti dolorem eveniet facere fuga iste nemo nesciunt
    nihil odio perspiciatis, quia quis reprehenderit sit tempora totam unde.</Modal
> -->
      <!-- svelte-ignore a11y-label-has-associated-control -->

      <Modal bind:show header={"Modal title"} on:close={() => (show = false)}
        ><div class="modal-body">
          <div class="mb-3">
            <label class="form-label">Name</label>
            <input
              type="text"
              class="form-control"
              name="example-text-input"
              placeholder="Your report name"
            />
          </div>
          <label class="form-label">Report type</label>
          <div class="form-selectgroup-boxes row mb-3">
            <div class="col-lg-6">
              <label class="form-selectgroup-item">
                <input
                  type="radio"
                  name="report-type"
                  value="1"
                  class="form-selectgroup-input"
                  checked=""
                />
                <span
                  class="form-selectgroup-label d-flex align-items-center p-3"
                >
                  <span class="me-3">
                    <span class="form-selectgroup-check" />
                  </span>
                  <span class="form-selectgroup-label-content">
                    <span class="form-selectgroup-title strong mb-1"
                      >Simple</span
                    >
                    <span class="d-block text-muted"
                      >Provide only basic data needed for the report</span
                    >
                  </span>
                </span>
              </label>
            </div>
            <div class="col-lg-6">
              <label class="form-selectgroup-item">
                <input
                  type="radio"
                  name="report-type"
                  value="1"
                  class="form-selectgroup-input"
                />
                <span
                  class="form-selectgroup-label d-flex align-items-center p-3"
                >
                  <span class="me-3">
                    <span class="form-selectgroup-check" />
                  </span>
                  <span class="form-selectgroup-label-content">
                    <span class="form-selectgroup-title strong mb-1"
                      >Advanced</span
                    >
                    <span class="d-block text-muted"
                      >Insert charts and additional advanced analyses to be
                      inserted in the report</span
                    >
                  </span>
                </span>
              </label>
            </div>
          </div>
          <div class="row">
            <div class="col-lg-8">
              <div class="mb-3">
                <label class="form-label">Report url</label>
                <div class="input-group input-group-flat">
                  <span class="input-group-text">
                    https://tabler.io/reports/
                  </span>
                  <input
                    type="text"
                    class="form-control ps-0"
                    value="report-01"
                    autocomplete="off"
                  />
                </div>
              </div>
            </div>
            <div class="col-lg-4">
              <div class="mb-3">
                <label class="form-label">Visibility</label>
                <select class="form-select">
                  <option value="1" selected="">Private</option>
                  <option value="2">Public</option>
                  <option value="3">Hidden</option>
                </select>
              </div>
            </div>
          </div>
        </div></Modal
      >
    </div>
  </div>
</div>
