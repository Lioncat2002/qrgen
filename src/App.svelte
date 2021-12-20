<script>
	let url=''
	let fullurl=`https://qrtag.net/api/qr_4.png?url=https://www.qrtag.net`
	let toggle=false
	function submit() {
		fullurl=`https://qrtag.net/api/qr_4.png?url=${url}`
		toggle=true
	}
</script>


<input type="text" bind:value={url} placeholder="Enter url">

<button on:click={submit}>Submit</button>
<br>
<style>
	img{
		display: grid;
		justify-content: center;
	}
</style>
{#if toggle}
<img src={fullurl} alt="qrtag">
{/if}

