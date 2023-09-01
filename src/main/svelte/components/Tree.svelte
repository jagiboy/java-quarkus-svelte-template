<script>
    import { TreeView } from "carbon-components-svelte";
  
    export let activeId = "";
    let selectedIds = [];
    let size = "compact";
    let children = [
      { id: 0, text: "AI / Machine learning" },
      {
        id: 1,
        text: "Analytics",
        children: [
          {
            id: 2,
            text: "IBM Analytics Engine",
            children: [
              { id: 3, text: "Apache Spark" },
              { id: 4, text: "Hadoop" },
            ],
          },
          { id: 5, text: "IBM Cloud SQL Query" },
          { id: 6, text: "IBM Db2 Warehouse on Cloud" },
        ],
      },
      {
        id: 7,
        text: "Blockchain",
        children: [{ id: 8, text: "IBM Blockchain Platform" }],
      },
      {
        id: 9,
        text: "Databases",
        children: [
          { id: 10, text: "IBM Cloud Databases for Elasticsearch" },
          { id: 11, text: "IBM Cloud Databases for Enterprise DB" },
          { id: 12, text: "IBM Cloud Databases for MongoDB" },
          { id: 13, text: "IBM Cloud Databases for PostgreSQL" },
        ],
      },
      {
        id: 14,
        text: "Integration",
        disabled: true,
        children: [{ id: 15, text: "IBM API Connect", disabled: true }],
      },
    ];
  </script>
  
  <div class="component-one">
  <TreeView 
    labelText="Cloud Products"
    {children}
    bind:activeId
    bind:selectedIds
    on:select={({ detail }) => console.log("select", detail)}
    on:toggle={({ detail }) => console.log("toggle", detail)}
    on:focus={({ detail }) => console.log("focus", detail)}
  />
  <!--
  <div>Active node id: {activeId}</div>
  <div>Selected ids: {JSON.stringify(selectedIds)}</div>
    -->
</div>

  
  
  <style>
    .component-one{
    /* padding: 1rem; */
    /* background: rgb(10, 173, 194); */
    color: rgb(255, 255, 255);
    display:  flex; 
    gap: 1rem;
    flex-direction: column;
    }
  </style>  
  