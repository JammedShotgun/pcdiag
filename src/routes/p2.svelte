<script context="module">
	export const prerender = true;
</script>

<script>
    let newItem = '';
	
    let todoList = [{text: 'Monitor', status: false},
                    {text: 'RAM', status: false},
];
	
	function addToList() {
		todoList = [...todoList, {text: newItem, status: false}];
		newItem = '';
	}
	
	function removeFromList(index) {
		todoList.splice(index, 1)
		todoList = todoList;
    }

</script>



<svelte:head>
	<title>Component</title>
</svelte:head>

<section>
	<h1>
		PC Diagnostic
	</h1>

	<h2>
		Komponen yang diidentifikasi mengalami kerusakan berdasarkan gejala yang diberikan:
	</h2>
	

</section>
<div class="cum">
    {#each todoList as item, index}
    <input bind:checked={item.status} type="checkbox">
    <span class:checked={item.status}>{item.text}</span>
    <br/>
    <br/>
    {/each} 
  
</div>
<button type="submit">
	Submit
</button>
<style>
    .cum {
    margin-left: auto;
    margin-right: auto;
    }
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
	.checked {
        font-weight: bold;
    }
    button {
		width: fit-content;
		margin-left: auto;
    	margin-right: auto;
	}
</style>
