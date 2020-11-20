<script lang="ts">
  import FaPhone from 'svelte-icons/fa/FaPhone.svelte';
  import FaPencilAlt from 'svelte-icons/fa/FaPencilAlt.svelte';

  let vw; 
</script>

<svelte:window bind:innerWidth={vw}/>

<header>
  <div id="header-top">
    <div class="header-item">
      <div class="icon">
        <FaPhone />
      </div>
      <a href="tel:3604061623">360-406-1623</a>
    </div>
    <div class="header-item">
      <a href="mailto:kim@kim-randolph.com">kim@kim-randolph.com</a>
      <div class="icon">
        <FaPencilAlt />
      </div>
    </div>
  </div>
  <div id="logo-cont">
    {#if vw <= 768}
      <img src="./images/mobilelogo.png" alt="Mobile Logo" class="logo"/>
    {:else}
      <img src="./images/desktoplogo.png" alt="Desktop Logo" class="logo"/>  
    {/if}
  </div>
  <div class="hero">
    <div id="hero-card">
      <div class="inner-text">
        <h1>A complete solution for your small business accounting needs</h1>
        <p>From setting up and maintaining bookkeeping systems to working with state and federal agencies, as an Enrolled Agent, Kim Randolph provides the accounting expertise you need, and the credibility you want.</p>
        <a href="/" class="button">schedule a free consultation</a>
      </div>
      <img id="calc" src="./images/calculator.png" alt="">
    </div>
  </div>
</header>

<style>
header {
  background: var(--lightpurple);
  background: linear-gradient(0deg, var(--lightpurple) 0%, var(--white) 100%);
  clip-path: ellipse(calc(100% + 150vw) 100% at 50% 0%);
}

h1 {
  text-align: right;
  margin: 0;
}

p {
  font-family: var(--body);
  text-align: right;
  font-size: 1.2rem;
  margin-top: 0;
}

#header-top {
  display: flex;
  padding: 1rem;
  justify-content: space-between;
}

#logo-cont {
  width: 100%;
  display:grid;
}

.logo {
  width: 100%;
  max-width: 400px;
  justify-self: center;
  margin: 2rem;
}

.header-item {
  display: flex;
  align-items: center;
}

.header-item > a {
  margin: .5rem;
  font-size: .70rem;
  white-space: nowrap;
}

.hero {
  min-height: 700px;
  margin-top: 200px;
}
#calc {
  transform: scale(.90) translate(0%, -30%);
  filter: drop-shadow(0px 0px 32px var(--shadow));
}

#hero-card {
  margin: 2rem auto;
  padding: 2rem;
  background: white;
  display: grid;
  grid-template-columns: 400px 1fr;
  grid-template-rows: auto;
  max-height: 450px;
  max-width: 850px;
}

.inner-text {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  height: max-content;
}

@media screen and (min-width: 500px) {
  .header-item > a {
    font-size: 1rem;
  }
}

@media screen and (min-width: 768px) {
  .header-item > a {
    font-size: 1.2rem;
  }

  .logo {
    max-width: 500px;
  }
}

@media screen and (max-width: 900px) {
  #hero-card {
    max-width: 80vw;
  }

  .hero {
    margin-top: 100px;
  }
  
  #calc {
    transform: scale(.84) translate(5%, -30%);
  }
}
</style>