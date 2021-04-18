<script>
  import DocumentForm from "./src/DocumentForm.svelte";
  let doc = {
    amount: 12.34,
    currency: "EUR"
  };
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>

<main>
	<h1>Document de test</h1>
	<h2>Saisir les paramètres du document</h2>
  <DocumentForm document={doc} />
</main>