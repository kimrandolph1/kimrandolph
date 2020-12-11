<script>
  import FaPhone from 'svelte-icons/fa/FaPhone.svelte';
  import FaFax from 'svelte-icons/fa/FaFax.svelte'
</script>

<footer>
  <div id="email-form-cont" class="flex-row">
    <div id="inner-text" class="column">
      <h1>Reach Out!</h1>
      <p>Use the contact form to schedule a free consultaion, or to find out more about how Kim Randolph, Enrolled Agent can help your business.</p>
      <div id="number-wrap">
        <a href="tel:3604061623" class="mini-wrap">
          <div class="icon-invert">
            <FaPhone />
          </div>
          360-406-1623
        </a>
        <p class="mini-wrap">
          <span class="icon-invert">
            <FaFax />
          </span>
          360-477-4444
        </p>
      </div>
    </div>

    <form method="post" action="submit.php" name="Email" class="column">
      <input class="antispam" type="text" name="URL">
      <input type="text" for="Email" name="name" placeholder="Name" />
      <input type="email" for="Email" name="email" placeholder="Email" />
      <textarea for="Email" name="message" placeholder="Message" />
      <input type="submit" for="Email" value="Send" />
    </form>
  </div>
  <hr>    
  <p id="foot">2020 Kim Randolph  |  Design & Development by <a href="https://bythebootstrap.us">Bootstrap</a></p>
</footer>

<style>
  .antispam {
    display: none;
  }
  footer {
    background: var(--lightpurple);
    background: linear-gradient(0deg, var(--white) 0%, var(--lightpurple) 100%);
    clip-path: ellipse(calc(100% + 50vw) 100% at 50% 100%);
    /* min-height: 450px; */
    padding: 0 3rem;
    padding-top: 4rem;
  }

  #email-form-cont {
    margin: 1rem 3rem;
  }

  #inner-text {
    max-width: 90vw;
    
  }

  #inner-text > h1{
    font-size: 3.2rem;
    color: var(--white);
  }

  #number-wrap {
    display: flex;
    flex-direction: column;
  }

  #number-wrap > p, #number-wrap > a {
    font-size: 1.25rem;
  }

  .mini-wrap {
    display: flex;
    gap: .5rem;
    color: var(--black);
  }

  form {
    flex: 2;
    width: 100%;
    display: grid;
    grid-template-rows: 2rem 2rem 8rem 2rem;
    grid-template-columns: auto;
    gap: 2rem;
  }

  form > *{
    display: block;
    max-width: 90vw;
    height: 100%;
    font-size: 1rem;
    padding-left: .3rem;
    font-family: var(--body);
    font-style: italic;
  }

  form > [name=message] {
    padding: .5rem;
  }

  form > [type=submit] {
    width: 200px;
    justify-self: end;
    font-family: var(--subheading);
    background: var(--purple);
    color: var(--white);
    font-style: normal;
    border: none;
    font-size: .8rem;
    font-weight: lighter;
  }

  form > [type=submit]:hover{
    cursor: pointer;
  }

  textarea {
    border: none;
    resize: none;
    outline: none;
  }

  hr {
    width: 95%;
    opacity: 60%;
  }

  #foot {
    width: 100%;
    margin: 2rem auto;
    text-align: center;
  }

  @media screen and (max-width:768px){
    #email-form-cont {
      /* grid-template-columns: 1fr; */
      margin: 0;
    }

    #inner-text {
      text-align: center;
    }

    #number-wrap {
      flex-direction: row;
      width: 100%;
      justify-content: space-between;
      align-items: center;
      margin-top: 1rem;
    }
  }

  @media screen and (max-width:500px){
    #number-wrap {
      flex-direction: column;
      gap: .5rem;
      
    }
  }
</style>