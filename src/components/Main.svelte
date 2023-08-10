<script lang="ts">
  import Tabs from "./Tabs.svelte";
  import Project from "./Project.svelte";
  import Form from "./ContactForm.svelte";

  let tabItems = ["About", "Projects", "Contact"];
  let activeItem = "About";

  const triggerTabChange = (event: CustomEvent) => {
    activeItem = event.detail;
  };
</script>

<div class="container">
  <Tabs {tabItems} {activeItem} on:tabChange={triggerTabChange} />
  {#if activeItem === "About"}
    <p class="text-sm">
      I've always had an eye for art, even as a kid when I would build and paint
      model cars. I decided to pursue pixel art because it was accessible and
      fun! I have 2 projects on the Unity Asset Store and many other unlisted
      projects, I'm keen to work with you so please get in touch!
    </p>
  {:else if activeItem === "Projects"}
    <ul>
      <li>
        <Project
          link="https://assetstore.unity.com/packages/2d/characters/2d-pixel-rpg-monsters-icon-pack-174649"
          imgSrc="proj1.png"
          headerTxt="RPG Monsters Icon Pack"
          subTxt="96 inanimate monster icons to use in your game!"
        />
      </li>
      <li>
        <Project
          link="https://assetstore.unity.com/packages/2d/characters/pixel-heroes-editor-250116"
          imgSrc="proj2.png"
          headerTxt="Pixel Heroes Editor"
          subTxt="Build custom characters in the editor and save sprite sheets!"
        />
      </li>
    </ul>
  {:else}
    <Form />
  {/if}
</div>

<style>
  .container {
    margin: 40px auto;
  }
</style>
