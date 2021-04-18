<script>
  export let document = {
    doc: {
      type: "Devis",
      refence: "9999-999",
      date: "JJ/MM/AAAA"
    },
    dateIssued: "JJ/MM/AAAA",
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
  legend {
    background-color: rgb(60, 160, 95);
  }
  label::after {
    display: block;
    align: left;
    content: "\A";
  }
</style>

<form>
  <fieldset>
    <legend>Général</legend>
      <label>Date
        <input type="text" bind:value={document.doc.date} />
      </label>
      <label>Type document
        <input type="text" bind:value={document.doc.type} list="lstDocType"/>
        <datalist id="lstDocType">
          <option value="Facture" />
          <option value="Pro-Format" />
          <option value="Devis" />
        </datalist>
      </label>
      <label>Référence
        <input type="text" bind:value={document.doc.refence} />
      </label>
  </fieldset>
  <fieldset>
    <legend>Origine</legend>
      <label>Nom
        <input type="text" bind:value={document.from.name} />
      </label>
      <label>email
        <input type="text" bind:value={document.from.mail} />
      </label>
  </fieldset>
  <fieldset>
    <legend>Destinataire</legend>
      <label>Nom
        <input type="text" bind:value={document.to.name} />
      </label>
      <label>SIREN
        <input type="text" bind:value={document.to.siren} />
      </label>
  </fieldset>
  <fieldset>
    <legend>Montant</legend>
      <label>Montant
        <input type="number" step="0.01" bind:value={document.amount} />
      </label>
      <label>Devise
        <input type="text" maxlength="3" bind:value={document.currency} />
      </label>
  </fieldset>
</form>
