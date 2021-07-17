<script>
    let darkMode = false;
	function toggle() {
        darkMode = !darkMode;
        window.document.body.classList.toggle('dark');
    }
</script>
<button on:click={toggle}>
	{#if darkMode }
		Go light mode
	{:else}
		Go dark mode
	{/if}
</button>
<style>
     button{
		font-family: "Space Grotesk";
        background-color: #465773;
        padding:10px;
        margin: 4px 2px;
        border: 1px solid #465773;
        border-radius: 10px;
        text-transform: uppercase;
        cursor:pointer;
        color:white;
    }
    button:hover{
        background-color: #6c7f9e;
        border-radius: 1px solid #6c7f9e;
    }
    button:active{
        background-color: #7b89a1;
        border-radius: 1px solid #7b89a1;
    }
</style>