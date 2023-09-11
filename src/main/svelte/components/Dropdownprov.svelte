<script>
    import { Dropdown } from "carbon-components-svelte";
  </script>
  
  <Dropdown
    on:select
    titleText="Model Provider"
    selectedId="0"
    items={[
      { id: '0', text: "AWS" },
      { id: '1', text: "Azure" },
      { id: '2', text: "Watsonx" },
    ]}
  />