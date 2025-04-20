<script lang="ts">
	import Me from '$lib/images/me.svelte';
	import Project from '$lib/components/Project.svelte';
	import projects from '$lib/_data/projects';
	
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



<style lang="postcss">
	@reference "tailwindcss";
	.bg-primary {
		background-color: #232432;
	}

	.color-accent {
		color: #EAEEFF; 
	}
</style>