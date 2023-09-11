<script>
  import {
    Header,
    HeaderUtilities,
    HeaderGlobalAction,
    HeaderAction,
    HeaderPanelLinks,
    HeaderPanelDivider,
    HeaderPanelLink,
    HeaderNav,
    HeaderNavItem,
    HeaderNavMenu,
    SkipToContent,
    Content,
    Grid,
    Row,
    Column,
  } from "carbon-components-svelte";
  import Theme from "./Theme.svelte";
  import SettingsAdjust from "carbon-icons-svelte/lib/SettingsAdjust.svelte";
  import UserAvatarFilledAlt from "carbon-icons-svelte/lib/UserAvatarFilledAlt.svelte";

  let isSideNavOpen = false;
  let isOpen1 = false;
  let isOpen2 = false;
</script>



<Header company="IBM" platformName="ATOM" bind:isSideNavOpen>
  <svelte:fragment slot="skip-to-content">
    <SkipToContent />
  </svelte:fragment>
  


   <HeaderUtilities > 
    
    <HeaderAction
      bind:isOpen={isOpen1}
      icon={SettingsAdjust}
      closeIcon={SettingsAdjust}
    >
      <HeaderPanelLinks>
        <HeaderPanelLink><Theme/></HeaderPanelLink>
       
      </HeaderPanelLinks>
    </HeaderAction>
   </HeaderUtilities>


   
</Header>

  

