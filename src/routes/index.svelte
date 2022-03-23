<script context="module">
	export const prerender = true;
</script>

<script>
    let newItem = '';
	
    let todoList = [{text: 'Monitor tidak menyala', status: false},
                    {text: 'Bau gosong', status: false},
                    {text: 'Komputer tidak hidup', status: false},
					{text: 'Komputer hidup tapi tidak boot', status: false},
                    {text: 'Komputer booting ke safe mode', status: false},
                    {text: 'Blue Screen', status: false},
					{text: 'RAM tidak terdeteksi', status: false},
                    {text: 'Tampilan rusak dan hang', status: false},
                    {text: 'Komputer sering hang', status: false},
					{text: 'Tampilan layar bergaris', status: false},
                    {text: 'Processor tidak terdeteksi', status: false},
                    {text: 'Tampilan monitor gelap', status: false},
					{text: 'Muncul tulisan "NTFS FILE SYSTEM"', status: false},
					{text: 'Missing dll32', status: false},
					{text: 'Muncul tulisan "Operating system not found"', status: false},
                    {text: 'Hard Disk bad sector', status: false},
                    {text: 'Masalah BIOS', status: false},
					{text: 'CPU mengeluarkan bunyi beep', status: false},
                    {text: 'Muncul tulisan "Memory test fail"', status: false},
                    {text: 'Lampu power tidak menyala, kipas menyala', status: false},
					{text: 'Lampu power tidak menyala, kipas tidak menyala', status: false},
                    {text: 'Muncul tulisan "Hard disk error/failure"', status: false},
                    {text: 'Tidak dapat masuk ke BIOS', status: false},
                    {text: 'Muncul tulisan "Memory Management Error"', status: false},];
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
	<title>Pc Diagnostic</title>
</svelte:head>

<section>
	<h1>
		PC Diagnostic
	</h1>

	<h2>
		Pilih beberapa gejala yang dialami
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
        text-decoration: line-through;
    }
	button {
		width: fit-content;
		margin-left: auto;
    	margin-right: auto;
	}
</style>
