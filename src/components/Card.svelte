<script lang="ts">
  export let title:string;
  export let content:string[] = [];
  export let id:string;
</script>

<div id="{id}" class="card ">
  <h1>{ title }</h1>
  {#each content as para}
    <p>{ para }</p>
  {/each}
</div>

<style>
  h1 {
    color: var(--white);
    font-size: 1.6rem;
    background: var(--teal);
    padding: .5rem;
    font-family: var(--subheading);
    font-style: unset;
  }
  
  #three > h1{
    background: var(--purple);
  }

  p {
    padding: 2rem;
    padding-top: .2rem;
    text-align: left;
    margin: 0;
    line-height: 1.3;
  }

  .card {
    background: var(--gray);
    box-shadow: 0px 0px 30px var(--shadow);
    width: 30%;
    margin: 0 auto;
  }

  @media screen and (max-width: 900px){
    .card {
      width:100%;
      margin-bottom: 2rem;
    }
  }
</style>