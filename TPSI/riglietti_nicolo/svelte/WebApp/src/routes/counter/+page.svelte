
<script>
    import Counter from "$lib/components/counter.svelte";
    import DoubleCounter from "$lib/components/double_counter.svelte";
    // let contatore = 0;
    let contatore2 = 0;
    let numeri = [1, 7, 2, 6, 9, 10]
    let sottolineato = true

    $: doppio = contatore2 * 2
    $: sottolineato = contatore2 % 2 == 0 


    function gestisci_evento(evento) {
        alert(`${evento.detail.tipo} -- ${evento.detail.valore}`)
    }
</script>

<!-- <h1>Pagina Counter!!!</h1>
<h2>Il valore del contatore vale {contatore}</h2>

<Counter bind:counter={contatore} /> 
 -->


<h1>Double Counter</h1>

<!-- {#if contatore2 < 5}
    <h2 class="rosso", cla>Il valore del contatore vale {contatore2}</h2>
{:else}
    <h2 class="verde">Il valore del contatore vale {contatore2}</h2>
{/if} -->

<!-- <h2 class={contatore2 < 5 ? 'rosso' : 'verde'}>Il valore del contatore vale {contatore2}</h2> -->

<h2 class:sottolineato>Il valore del contatore vale {contatore2}</h2>
<h2>il suo doppio è {doppio}</h2>
<DoubleCounter bind:counter={contatore2} on:contatore={gestisci_evento}/>




<ul>
    {#each numeri as numero, indice}
        <li>numeri[{indice}]: {numero}</li>
    {/each}
    
</ul>

<style>
    /* .rosso {color: red;}
    .verde {color: green;} */
    .sottolineato { text-decoration: underline; }
</style>