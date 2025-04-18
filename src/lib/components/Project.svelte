<script>
    export let ProjectIndex = 1;
    export let ProjectName = 'Unknown Project';
    export let ProjectDescription = ""; 
    export let IMGPath = '';
</script>

<div class="flex flex-row items-center gap-x-10">
    <h1>{ProjectIndex}</h1>
    <img src={IMGPath} alt={ProjectName} class="h-[14rem] w-auto rounded-[4rem]"/>
    <div class="ml-2 w-[40rem]">
        <h1>{ProjectName}</h1>
        <p>{ProjectDescription}</p>
    </div>
</div>

<style lang="postcss">
	@reference "tailwindcss";
	p {
		color: #2B2B2B;
	}

	h1 {
		color: #232432;
	}
</style>
