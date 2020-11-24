<script lang="ts">
	import Card from '../components/Card.svelte';
	const cardData = [
    {
      id: "one",
      title: "Starting a Business",
      content: [
        "Set up your bookkeeping systems correctly from the start! Kim will create a clear and efficient process for your financial reporting using QuickBooks.",
        "Once your books are set up, Kim expertly manages your payroll, state tax filings, and annual reports."
      ]
    },
    {
      id: "two",
      title: "A Growing Business",
      content: [
        "Hiring professional services like accounting and legal experts is important to help your business grow. Maturing start-up businesses need their books set up correctly to maintain accuracy for IRS compliance and tax filing.",
        "Kim provides financial & tax guidance in addition to fully managing all of your financial filing & reporting."
      ]
    },
    {
      id: "three",
      title: "Notary Public",
      content: [
        "In addition to accounting services, Kim Randolph is a mobile notary public officer, serving the Sequim, WA area.",
        "Kim will travel to you and notarize business forms, contracts, titles, mortgages, loans, and much more."
      ]
    }
	];
	const pricingData = [
		{
			title: "Basic Bookkeeping",
			copy: "$45/hr. A monthly rate will be considered after 3 months of services provided"
		},
		{
			title: "Excise Tax Returns",
			copy: "$65 each, $10 additional for each city"
		},
		{
			title: "Quarterly Payroll Tax Filings",
			copy: "$125 each (includes federal & state agencies)"
		},
		{
			title: "W-2 Prep",
			copy: "$75 each (up to 10 employees), additional employees $5 each"
		},
		{
			title: "1099 Prep",
			copy: "$10 for each."
		},
		{
			title: "Payroll Run",
			copy: "$25 (up to 3 employees) additional employees $10 each"
		},
		{
			title: "Payroll Set Up Fee",
			copy: " $45/hr",
		},
		{
			title: "Notary Services",
			copy: "$10 per signature for Mobile Notary services, $100-$150 for mortgages"
		},
	];
</script>

<div class="row" id="row1">
	<h1>Honest, Approachable, & Experienced</h1>
	<p class="para">Navigate financial decisions with dependable guidance. Kim combines superior tools and training with a personal and collaborative experience to empower small business owners to operate efficiently and legally.</p>
</div>

<div id="row-wrap">
	<div class="row" id="row2">
		<h1>The Expertise You Need</h1>
		<p class="para">Kim helps business owners understand more about their finances to make informed decisions and find potential savings. Using an Enrolled Agent like Kim with 18 years experience in accounting and 15 years working with CPA firms ensures that reporting is done correctly to avoid liability.</p>
		<p class="para">Businesses who need to work with state and federal agencies are more likely to reach more favorable audit outcomes when using a professional that understands complex tax laws.</p>
		<a href="/" class="button lt-button">contact kim today</a>
		<div class="card-grid inset-row">
			{#each cardData as card}
				<Card {...card}/>
			{/each}
		</div>
	</div>

	<div class="row" id="row3">
		<h1>Accounting & Notary Pricing</h1>
		<div id="columns">	
			{#each pricingData as { title, copy }}
				<p><span>{ title } </span>{ copy }</p>
			{/each}
		</div>
	</div>
</div>
<div class="row" id="row4">
	<h1>Focusing on Your Success</h1>
	<p class="para">Tax advice & financial reports are optimized for each client’s individual needs over time. Kim Randolph Accounting and Notary Services believes in building long term relationships with businesses and owners in order to produce better results through better relationships.</p>
	<img src="images/people.svg" alt="people">
</div>

<style>
	#row1 {
		text-align: center;
		margin: 2rem;
	}

	#row2 {
		text-align: center;
		padding: 3rem;
		margin: 0 -3rem;
		background-image: linear-gradient(to top, #ffffff20, #131313ba), url('/images/row-2-bg.jpg');
		background-size: cover;
		background-position: center;
	}

	#row2 > h1 {
		color: var(--white);
		font-size: 4rem;
	}

	#row2 > p {
		color: var(--white);
	}

	#row3 {
		text-align: center;
		background: var(--teal);
		margin: 0 -3rem;
		min-height: 400px;
	}

	#row3 > h1 {
		font-size: 3rem;
		padding: 2rem;
		margin: -1rem;
		color: var(--white);
		font-style: normal;
		background: var(--darkteal);
		/* max-width: 90vw; */
	}

	#row-wrap {
		clip-path: ellipse(calc(150% + 35vw) 50% at 50% 50%);
		margin-top: 4rem;
	}

	.card-grid {
		/* display: grid; */
		/* grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); */
		gap: 2rem;
		margin: 2rem auto;
	}

	#columns{
		columns: 3; 
		text-align: left;
		margin: 4rem;
		margin-top: 5rem;
		gap: 5.5rem;
		padding-bottom: 2rem;
	}

	#columns > p {
		font-size: 1.4rem;
		line-height: 1.4;
		margin-bottom:1rem;
		-webkit-column-break-inside: avoid;
          page-break-inside: avoid;
               break-inside: avoid;
	}

	#columns > p > span {
		color: var(--white);
	}

	#row4 {
		text-align: center;
	}

	#row4 > h1 {
		font-size: 4rem;
	}

	#row4 > p {
		font-size: 1.1rem;
	}

	#row4 > img {
		max-width: 75vw;
		margin-bottom: -150px;
	}

	@media screen and (max-width: 900px){
		.card-grid {
			display: block;
		}
	}

	@media screen and (max-width: 700px){
		#columns {
			columns: 2;
			margin-top: 2rem;
		}
	}

	@media screen and (max-width: 500px){
		#columns {
			columns: 1;
		}
	}
</style>



