<script context="module">
	export const prerender = true;
</script>

<script>

</script>



<svelte:head>
	<title>Results</title>
</svelte:head>

<section>
	<h1>
		PC Diagnostic
	</h1>

	<h2>
		Hasil klasifikasi kerusakan:
	</h2>

	<h3>
		HARDWARE
	</h3>
	
	<br/>
Berdasarkan gejala yang telah anda berikan hasil analisis sistem menunjukkan bahwa monitor anda bermasalah. Bila monitor anda tidak dapat menyala, coba pastikan kabel yang terhubung dari monitor ke CPU anda tidak bermasalah. Bila masih tidak dapat menyala, disarankan untuk melalukan pembaharuan driver VGA anda.
<br/>
<br/>
</section>
<button type="submit">
	Kembali
</button>
<style>
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
