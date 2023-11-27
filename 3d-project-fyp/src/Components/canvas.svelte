<script>
  let a = true;

  const lights = ["Cube", "Sphere", "Cylinder", "Plane", "Circle"];
  const meshes = [];
  /**
   * @param {Event} e
   */
  function canvasClick(e) {
    a = !a;
    console.log(a);
    e.preventDefault();
  }
</script>

{#if a}
  <div class=" bg-slate-800 absolute">
    <p>Create obj</p>
    <ul></ul>
    <p>create light</p>
    <ul>
      {#each lights as light}
        <li>{light}</li>
      {/each}
    </ul>
  </div>
{:else}{/if}
<canvas class="border" on:contextmenu={canvasClick}></canvas>
