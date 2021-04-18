<script>
  export let document = {
    typeDoc: 'Facture',
    invoiceNb = '9999-999',
    dateIssued = 'JJ/MM/AAAA',
    object: 'Honoraires Mmm AAAA',
    amount: 1.2,
    currency: 'EUR',
    from: {
      name: 'my company',
      mail: 'mail',
      phone: 'phone',
      address: '23 rue Émille Flombard\n75001 Paris\nFrance'
    },
    to: {
      name: 'to company name',
      address: '10 rue de la poupée qui toiusse\n75004 Paris\nFrance',
      siren: '999 999 999'
    }
  };
</script>

<form>
  <fieldset>
    <legend>Destinataire</legend>
      <label>Nom<label>
      <input type="text" bind:value={document.to.name} />
      <input type="text" bind:value={document.to.siren} />
  </fieldset>
  <fieldset>
    <legend>Montant</legend>
      <input type="number" step="0.01" bind:value={document.amount} />
      <input type="text" maxlength="3" bind:value={document.currency} />
  </fieldset>
</form>