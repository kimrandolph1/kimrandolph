<script lang="ts">
  export let title:string;
  export let content:string[] = [];
  export let id:string;
</script>

<div id="{id}" class="card">
  <h1>{ title }</h1>
  {#each content as para}
    <p>{ para }</p>
  {/each}
</div>

<style>
  h1 {
    color: var(--white);
    font-size: 1.3rem;
    background: var(--teal);
    padding: .5rem;
    font-family: var(--subheading);
    font-style: unset;
  }
  
  #three > h1{
    background: var(--purple);
  }

  p {
    padding: 1.2rem;
    text-align: left;
    margin: 0;
  }

  .card {
    background: var(--gray);
    box-shadow: 0px 0px 30px var(--shadow);
  }
</style>