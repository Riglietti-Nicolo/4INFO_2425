<svelte:head> 
<link href="https://fonts.googleapis.com/css2? 
family-Material+Symbols+Dutlined:opsz,wght, FILL, GRAD@48,400,0,0" rel="stylesheet" /> 
<link href="https://fonts.googleapis.com/css?family=Bungee+Spice&display=swap"
rel="stylesheet"> 
</svelte:head> 

<script>
    let counter = 0;
</script>

<h1>Pagina Counter!!!</h1>

<div class="container">
    <div class="pulsante">
        <button on:click={() => counter--}>
            <span class="material-symbols-outlined icon">-</span>
        </button>
    </div>

    <div class="number">
        {counter}
    </div>

    <div class="pulsante">
        <button on:click={() => counter++}>
            <span class="material-symbols-outlined icon">+</span>
        </button>
    </div>   
</div>

<style>    
    .container { 
        border: 4px solid #043C2F; 
        display: flex; 
        justify-content: space-between; 
        border-radius: 30px; 
        width: 300px; 
        padding: 10px; 
    }
    .pulsante { 
        display: flex; 
        align-items: center; 
    } 

    button { 
        border: none; 
        background: none; 
    } 
    .icon { 
        font-size: 2.5rem; 
        color: #F89C00;
        font-weight: bolder; 
    } 
    .icon:hover { 
        color: #04302F;
        cursor: pointer; 
    } 

    .icon:active { 
        text-shadow: 1px 1px 10px #043C2F; 
    } 

    .number {
        font-size: 4rem; 
        font-family: 'Bungee Spice', cursive; 
    } 

</style>