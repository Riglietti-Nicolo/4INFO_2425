<script>
    let nome, cognome, eta, confermato;
</script>

<h1>input page</h1>

Nome <input bind:value={nome}>
Cognome <input bind:value={cognome}>
Età <input type="number" bind:value={eta}>

<br><br>

Confermato <input type="checkbox" bind:checked={confermato}>

<br><br>

Io sono {nome} {cognome} ed ho {eta} anni

<br><br>

<button disabled={!confermato}>Invia</button>