<script>
import TitleDetail from '../UI/TitleDetail.svelte'

export let activeTitle
export let titles

let firstMount = true

setTimeout(() => {
    firstMount = false
}, 2300)

</script>

<style>
	.detail {
		margin-top: 2rem;
		max-width: 80%;
		position: relative;
	}
</style>

<div class="detail">
    {#each titles as title}
        {#if title.title === activeTitle}
            <TitleDetail title={title} firstMount={firstMount} />
        {/if}
    {/each}
</div>
