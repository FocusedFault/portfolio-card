<script lang="ts">
  export let link: string;
  export let imgSrc: string;
  export let headerTxt: string;
  export let subTxt: string;
</script>

<a href={link} class=" visited:text-purple-600 hover:text-blue-600">
  <div
    class="mb-2 bg-slate-100 border-slate-200 border-2 rounded p-4 hover:bg-slate-200 flex flex-col justify-center"
  >
    <img class="w-24 h-24" src={imgSrc} alt="pixel-art-monster" />
    <h3 class="text-xl">{headerTxt}</h3>
    <p class="text-sm">{subTxt}</p>
  </div>
</a>

<style>
</style>
