<script>
    import { Dropdown } from "carbon-components-svelte";
    export let models = [];
</script>
  


<Dropdown
  titleText="Model"
  selectedId="0"
  items={models}
/>
