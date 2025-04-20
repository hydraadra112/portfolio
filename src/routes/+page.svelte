<script lang="ts">
	import Me from '$lib/images/me.svelte';
	import Project from '$lib/components/Project.svelte';
	import projects from '$lib/_data/projects';
	
	import flutter from '$lib/images/techstack/flutter.svg';
	import github from '$lib/images/techstack/github.svg';
	import matplotlib from '$lib/images/techstack/matplotlib.svg';
	import python from '$lib/images/techstack/python.svg';
	import pytorch from '$lib/images/techstack/pytorch.svg';
	import react from '$lib/images/techstack/react.svg';
	import sklearn from '$lib/images/techstack/sklearn.svg';
	import streamlit from '$lib/images/techstack/streamlit.svg';
	import tailwind from '$lib/images/techstack/tailwind.svg';

	import FB from '$lib/images/icons/Facebook.svg';
	import In from '$lib/images/icons/LinkedIn.svg';
	import GitColor from '$lib/images/icons/GitHub.svg';
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

<section id='projects' class="mt-[7rem] flex flex-col">
	<h1 class="text-center">PROJECTS</h1>
	<div class="flex flex-col gap-y-10">
		{#each projects as project (project.ProjectIndex)}
		<Project
		  ProjectIndex={project.ProjectIndex}
		  ProjectName={project.ProjectName}
		  ProjectDescription={project.ProjectDescription}
		  IMGPath={project.IMGPath}
		/>
	  	{/each}
	</div>
</section>

<section id='contacts' class="h-[35rem] mt-[3rem] px-20 flex flex-row justify-between">
	<div class="w-[28rem]">
		<h1>Collab?</h1>
		<p>If you are looking for someone that can wear multiple hats, then I'm your guy!</p>
		<div class="flex flex-row mt-[3rem] items-center">
			<img src={FB} alt="Facebook Logo">
			<img src={In} alt="LinkeIn Logo">
			<img src={GitColor} alt="GitHub Logo">
		</div>
	</div>
	
	<div class="mt-[8rem] w-[35rem] flex flex-col gap-y-4" >
		<div class="flex flex-row gap-x-5">
			<img src={python} alt="Python">
			<img src={pytorch} alt="Pytorch">
			<img src={github} alt="github">
		</div>

		<div class="flex flex-row gap-x-5">
			<img src={react} alt="react">
			<img src={matplotlib} alt="matplotlib">
			<img src={flutter} alt="flutter">
		</div>

		<div class="flex flex-row gap-x-5">
			<img src={tailwind} alt="tailwind">
			<img src={streamlit} alt="streamlit">
			<img src={sklearn} alt="sklearn">
		</div>

	</div>
</section>



<style lang="postcss">
	@reference "tailwindcss";
	.bg-primary {
		background-color: #232432;
	}

	.color-accent {
		color: #EAEEFF; 
	}

</style>