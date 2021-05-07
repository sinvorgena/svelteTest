<script>
	import Block from "./Block.svelte";
	let blocks = [
		{ id: 1, color: 'red', opacity: 'opacity'},
		{ id: 2, color: 'blue', opacity: 'opacity'},
		{ id: 3, color: 'green', opacity: 'opacity'},
	]
	function setOpacity (e){
		console.log(blocks[e.target.id-1])
		if(blocks.some(el => el.opacity === "opacity")){
			if(blocks[e.target.id-1].opacity == "opacity"){
				blocks[e.target.id-1].opacity = "notOpacity"
			} else {
				blocks[e.target.id-1].opacity = "opacity"
			}
		} else{
			blocks = blocks.map(el=>{
				el.opacity="opacity"
				return el
			})
			console.log(blocks)
		}

	}
</script>

<div on:click={setOpacity} class="container">
	{#each blocks as block}
	<Block  color={block.color} id={block.id} opacity={block.opacity}/>
	{/each}
</div>



<style>
	.container {
		width: 100px;
		height: 300px;
	}
</style>