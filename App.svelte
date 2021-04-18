<script>
  import DocumentForm from "./src/DocumentForm.svelte";
  let doc = {
    doc: {
      type: "Devis",
      refence: "9999-999",
      date: "JJ/MM/AAAA"
    },
    object: "Honoraires Mmm AAAA",
    amount: 1.2,
    currency: "EUR",
    from: {
      name: "my company",
      mail: "mail",
      phone: "phone",
      address: "23 rue Émille Flombard\n75001 Paris\nFrance"
    },
    to: {
      name: "to company name",
      address: "10 rue de la poupée qui toiusse\n75004 Paris\nFrance",
      siren: "999 999 999"
    }
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