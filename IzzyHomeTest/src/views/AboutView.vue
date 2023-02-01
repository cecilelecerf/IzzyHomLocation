<template>
  <div id="about">
    <h1>Exercice frontend – izzyhom</h1>
    <legend>Durée conseillée : max. 4 heures</legend>

    <section>
      <h2>Énoncé</h2>
      <p>Nous te proposons de développer une page listant des annonces immobilières à
      destination de locataires potentiels (un peu comme sur SeLoger/leboncoin/etc.).
      Pour cela, tu devras te servir du jeu de données que nous te fournissons plus bas
      (contenant 67 annonces).</p>

      <p>Compte tenu du nombre important d'annonces, la page devra permettre au locataire de
      filtrer dynamiquement les annonces selon différents critères. Tu as la liberté de choisir quels
      filtres tu souhaites faire apparaître et comment les faire apparaître (select, slider, zone de
      texte, etc.) selon ce qui te semble être le plus pertinent.</p>

      <p>Tout en respectant les contraintes listées ci-dessous, et si tu es à l'aise, tu es totalement
      libre d'aller au-delà du sujet pour mettre en valeur ce que tu sais faire et qui te semble
      pertinent de nous montrer.</p>
    </section>

    <section>
      <h2>Contraintes imposées</h2>
      <ul>
        <li>Tu dois utiliser le jeu de données que nous te fournissons.</li>
        <li>Ne perds pas de temps à développer un backend : sers-toi simplement de la variable
        fournie dans le fichier JavaScript (voir plus bas) comme source de données.</li>
        <li>Tu devras utiliser un framework JavaScript tel que React, Vue.js ou Angular par
        exemple. Si tu maîtrises plusieurs de ces frameworks, nous avons une préférence
        pour React.</li>
        <li>Tu peux utiliser toute librairie JavaScript additionnelle qui te serait utile. De même, tu
        peux faire ton développement en TypeScript.</li>
        <li>Nous accorderons plus d'importance à la structure/lisibilité du code
        JavaScript/TypeScript qu'à l'apparence/design de la page.</li>
        <li>Essaie de te limiter à 4 heures pour réaliser l'exercice.</li>
      </ul>
    </section>

    <section>
      <h2>Rendu</h2>
      <p>Tu pourras nous remettre ton travail par email à l'adresse hiring@izzyhom.io :</p>
      <ul>
        <li>soit dans un fichier .zip (n'oublie pas de supprimer le répertoire node_modules/ pour
        limiter la taille du fichier .zip) ;</li>
        <li>soit dans un repo git public dont tu nous communiqueras l'adresse.</li>
      </ul>
      <p>Dans tous les cas, tu devras inclure un fichier README nous expliquant comment installer
      et lancer ton projet en local.</p>
    </section>

    <section>
      <h2>Jeu de données</h2>
      <p>Le jeu de données est récupérable dans le fichier JavaScript data.js que tu peux télécharger
      en cliquant ici.</p>
      Voici une description succincte des données disponibles :
      <table>
        <thead>
          <tr>
            <th>Nom du champ</th>
            <th>Description</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th>id</th>
            <th>Identifiant unique de l'annonce</th>
          </tr>
          <tr>
            <th>type</th>
            <th>Type de bien (valeurs possibles : flat ou house)</th>
          </tr>
          <tr>
            <th>title</th>
            <th>Titre de l'annonce</th>
          </tr>
          <tr>
            <th>main_picture</th>
            <th>URL de la photo principale de l'annonce</th>
          </tr>
          <tr>
            <th>living_area</th>
            <th>Surface habitable (en m2)</th>
          </tr>
          <tr>
            <th>rooms_count</th>
            <th>Nombre de pièces</th>
          </tr>
          <tr>
            <th>bedrooms_count</th>
            <th>Nombre de chambres</th>
          </tr>
          <tr>
            <th>address.postal_code</th>
            <th>Code postal</th>
          </tr>
          <tr>
            <th>address.city</th>
            <th>Ville</th>
          </tr>
          <tr>
            <th>is_furnished</th>
            <th>Si true, le bien est loué meublé</th>
          </tr>
          <tr>
            <th>full_rent_price</th>
            <th>Loyer mensuel, charges comprises</th>
          </tr>
        </tbody>
      </table>
    </section>

  </div>
</template>

<style>

</style>
