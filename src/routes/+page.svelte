<script lang="ts">
	import Me from '$lib/images/me.svelte';
	
</script>

<svelte:head>
	<title>Manns Portfolio</title>
	<meta name="description" content="Manns' Portfolio" />
</svelte:head>

<nav class="sticky bg-white h-12 flex flex-row items-center gap-x-9">
	<a href="/">About Me</a>
	<a href="/">Projects</a>
	<a href="/">Contact</a>
</nav>

<section id='about me' class="mt-[3rem] px-20 flex flex-row justify-between">
	<div class="w-[35rem]">
		<h1>About Me</h1>
		<p>I’m Manuel, and I am an aspiring AI engineer and researcher, eager to boost industries to make an impact.</p>
		<button id="download resume" class="mt-9 w-[15rem] h-[3.5rem] bg-primary">
			<p class="color-accent">Download Resume</p>
		</button>
	</div>

	<Me />
</section>

<style lang="postcss">
	@reference "tailwindcss";
	.bg-primary {
		background-color: #232432;
	}

	.color-accent {
		color: #EAEEFF; 
	}

	p, a {
		color: #2B2B2B;
	}

	h1 {
		color: #232432;
	}
</style>