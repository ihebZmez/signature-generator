<template>
  <div id="integrations">
    <h2>Pour configurer la signature dans Gmail</h2>
    <span
      >Vous pouvez demander à au service Marcketing ou bien au service IT de configurer
      la signature pour vous:</span
    >
    <ol>
      <li>houeida@kibocommunication.com</li>
      <li>khdija@kibocommunication.com</li>
      <li>support@cfacgroup.com</li>
    </ol>

    <div class="instructions">
      <h3>Instructions pour la signature email :</h3>
      <ul>
        <li>Vous pouvez écrire ou choisir de la liste le "Job Title".</li>
        <li>Vous pouvez insérer du texte dans les champs "Phone number".</li>
        <li>
          Pour revenir à la ligne dans la partie "Address", il suffit de faire
          <strong>double espace</strong>.
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "SignatureIntegrations",
};
</script>

<style scoped>
#integrations {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  padding: 20px;
}

.instructions {
  margin-top: 30px;
  padding: 15px;
  background-color: #f9f9f9;
  border-radius: 8px;
  border-left: 4px solid #4caf50;
}

.instructions h3 {
  margin-top: 0;
  color: #333;
}

.instructions ul {
  padding-left: 20px;
}

.instructions li {
  margin-bottom: 10px;
}

strong {
  color: #4caf50;
}
</style>