<script>
	import Accord from "./Accord.svelte"
	let rows=[
		{
			img:"/images/icon-arrow-down.svg",
			id:1,
		 	question: " How many team members can I invite?",
			answer: "You can invite up to 2 additional users on the Free plan. There is no limit on team members for the Premium plan.",
		},
		{
			img:"/images/icon-arrow-down.svg",
			id:2,
		 	question: " What is the maximum file upload size?",
			answer: "No more than 2GB. All files in your account must fit your allotted storage space."
		},
		{
			img:"/images/icon-arrow-down.svg",
			id:3,
		 	question: " How do I reset my password?",
			answer: "Click “Forgot password” from the login page or “Change password” from your profile page. A reset link will be emailed to you."
		},
		{
			img:"/images/icon-arrow-down.svg",
			id:4,
		 	question: "Can I cancel my subscription?",
			answer: "Yes! Send us a message and we’ll process your request no questions asked."
		},
		{
			img:"/images/icon-arrow-down.svg",
			id:5,
		 	question: " Do you provide additional support?",
			answer: " Chat and email support is available 24/7. Phone lines are open during normal business hours."
		},
	]

</script>

<main>
	<div class="container">
		<div class="grid">
			<div class="first">
				
				<div class="image">
					<img src="/images/illustration-woman-online-desktop.svg" alt="">
					<img class="box" src="/images/illustration-box-desktop.svg" alt="">
				</div>
			</div>
			<div class="second">
				<h1>FAQ</h1>
				{#each rows as {img , question , answer}}
					<Accord {img} {question} {answer}/>
				{/each}
			</div>
		</div>
	</div>
</main>

<style>
	.image{
		position: absolute;
	}
	.box{
		width: 49%;
    top: 64%;
    transform: translateX(-50%) translateY(-50%);
    position: absolute;
    left: 0px
	}
	img{
		transform: translateX(-2.8rem);
    width: 100%;
    height: auto;
    max-width: 400px
	}
	.second{
		padding-inline: 3rem;
	}
	main {
		overflow: hidden;
		align-items: center;
    height: auto;
    display: grid;
    /* place-items: center; */
    max-width: 986px;
    margin: 0 auto;
	}
	.grid{
		background: url(/images/bg-pattern-desktop.svg) no-repeat;
		margin-top:5rem;
		background-position: -13% center;
		background-size: 50%;
		border: 1px solid rgba(0,0,0,.125);
		border-radius:8px;
		background-color: white;
		padding:2rem 0;
		display:grid;
		grid-template-columns: repeat(2, 1fr);
	}

	@media (max-width: 640px) {
		.image{
			top: 63px;
    max-width: 100%;
    left: 54%;
    transform: translateY(-46%) translateX(-48%);
		}
		.container {
			max-width: none;
		}
		.grid{
			padding: 7rem 0;
			justify-content: center;
			grid-template-columns: repeat(1 , 1fr);
		}
	} 
	@media (max-width: 450px) {
		.image{
			top: 72px;
		}
	}
	@media (max-widh: 375px){
		.image{
			top: 77px;
    max-width: 100%;
    left: 57%;
    transform: translateY(-46%) translateX(-44%);
		}
	}
</style>