<script lang="ts">

import Tree from './components/Tree.svelte'
import Header from './components/Header.svelte';
import Textinput from './components/Textinput.svelte';
import Textarea from './components/Textarea.svelte';
import Dropdownprov from './components/Dropdownprov.svelte';
import Dropdownllm from './components/Dropdownllm.svelte';

let var1:string = "world";
let id='';
</script>

<div class="grid-container">
    <div class="header">
        <Header />
    </div>
    
    <div class="left" >
        
        <Tree
        bind:activeId={id}
        />
        <br/>
       <!-- <div>Active node id: {id}</div> -->

    </div>
    <div class="middle" >

        <Textinput />
        <br/>
        <Textarea />


    </div>  
    <div class="right">
        <Dropdownprov/>
        <br/>
        <Dropdownllm/>

    </div>
    
    <div class="footer">
      <p>Footer</p>
    </div>
  </div>

<style>
    * {
      box-sizing: border-box;
    }
    
    body {
      font-family: Arial, Helvetica, sans-serif;
    }
    
    /* Style the header */
    .header {
      /* grid-area: header; */
      grid-column: 1 / span 3;
      grid-row: 1;
      background-color: #f1f1f1;
      padding: 0px;
      text-align: center;
      font-size: 35px;
    }
    
    /* The grid container */
    .grid-container {
      display: grid;
      grid-template-columns: 300px 900px 250px;
      grid-template-rows: 48px 700px 100px;
      /* grid-template-areas: 
        'header header header header header header' 
        'left middle middle middle middle right' 
        'footer footer footer footer footer footer'; */
      /* grid-column-gap: 10px; - if you want gap between the columns */
    } 
    
    .left,
    .middle,
    .right {
      padding: 10px;
      /*height: 300px; /* Should be removed. Only for demonstration */
    }
    
    /* Style the left column */
    .left {
      /* grid-area: left; */
      grid-column: 1;
      grid-row: 2;
      overflow: auto;
    }
    
    /* Style the middle column */
    .middle {
      /* grid-area: middle; */
      grid-column: 2;
    }
    
    /* Style the right column */
    .right {
      
      /* grid-area: right; */
      grid-column: 3;
    }
    
    /* Style the footer */
    
    .footer {
      grid-column: 1 /span 3;
      grid-row: 3;
      background-color: #f1f1f1;
      padding: 10px;
      text-align: center;
    }
    
    
    /* Responsive layout - makes the three columns stack on top of each other instead of next to each other */
    @media (max-width: 600px) {
      .grid-container  {
        grid-template-areas: 
          'header header header header header header' 
          'left left left left left left' 
          'middle middle middle middle middle middle' 
          'right right right right right right' 
          'footer footer footer footer footer footer';
      }
    }
    </style>
