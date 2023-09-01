<script>
    import { Dropdown } from "carbon-components-svelte";
  </script>
  
  <Dropdown
    titleText="Model Provider"
    selectedId="0"
    items={[
      { id: "0", text: "Watsonx" },
      { id: "1", text: "Azure" },
      { id: "2", text: "AWS" },
      { id: "3", text: "OpenAI" },
    ]}
  />