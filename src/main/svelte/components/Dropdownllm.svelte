<script>
    import { Dropdown } from "carbon-components-svelte";
  </script>
  
  <Dropdown
    titleText="Model"
    selectedId="0"
    items={[
      { id: "0", text: "Flan-T5" },
      { id: "1", text: "Llama-2" },
      { id: "2", text: "Flan-T5-XL" },
      { id: "3", text: "GPT" },
    ]}
  />