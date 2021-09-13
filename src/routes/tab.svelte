<script>
    import Text from "../components/Text.svelte";
    import Page from "../components/Page.svelte";
    import Tab from "../components/Tabs/Tab.svelte";
    import Tabs from "../components/Tabs/Tabs.svelte";

    let selected = "1";
</script>

<Page name={"Tab"}>
    <Tabs
        bind:selected
        items={[
            { id: "1", text: "Cats" },
            { id: "2", text: "Kittens" },
            { id: "3", text: "Kitties" },
        ]}
    >
        <Tab id="1" {selected}>
            <div>
                Cursus turpis vestibulum, dui in pharetra vulputate id sed non
                turpis ultricies fringilla at sed facilisis lacus pellentesque
                purus nibh
            </div>
        </Tab>
        <Tab id="2" {selected}>
            <div>
                Fringilla egestas nunc quis tellus diam rhoncus ultricies
                tristique enim at diam, sem nunc amet, pellentesque id egestas
                velit sed
            </div>
        </Tab>
        <Tab id="3" {selected}><div>asdf</div></Tab>
    </Tabs>

    <Text bind:value={selected} />
</Page>
