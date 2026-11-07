# tac-velo

Site vitrine « TAC Vélo » de Julien Vaugoude, mécanicien vélo à Gif-sur-Yvette
(entreprise individuelle, SIRET 990 844 326 00019). Servi par GitHub Pages
(dépôt `svaug12345/tac-velo`) sur **tac-velo.fr**.

Repris le 07/11/2026 de `julien/` du dépôt `svaug12345.github.io` (baiji.fr/julien/,
v1.6.1), qui doit devenir une simple redirection vers tac-velo.fr une fois le
domaine en ligne.

## Fichiers
- `index.html` — toute la page (une seule page). Réglages dans le `<script>` en bas :
  objet `JULIEN` (tél., WhatsApp, e-mail, zone, horaires), `SERVICES` (tarifs
  indicatifs À FAIRE VALIDER par Julien), `ASTUCES`, diagnostic `DIAG_*`,
  assistant vocal `AGENT_RAYON`. Version dans le commentaire d'en-tête et `VERSION`.
- `manifest.webmanifest`, `sw.js`, `icones/` — page installable (PWA). Chemins
  relatifs (`./`) pour marcher aussi bien sur baiji.fr/tac-velo/ que sur tac-velo.fr/.

## Règles
- À chaque modification : augmenter `VERSION` et ajouter une ligne à l'historique
  en tête de `index.html` (sinon les téléphones gardent l'ancienne version en cache).
- Code commenté en français : l'auteur apprend en lisant.
- Nom affiché : « TAC Vélo », Julien présenté comme le mécanicien. Ne jamais écrire « Juju ».
- Adresse de l'atelier NON publiée (donnée au téléphone).
- Reste en `noindex` tant que Julien n'a pas validé les tarifs.
- Rayon (agent ElevenLabs `agent_9901m6b24af2f15s8fxy0ezqm92c`) : ses tarifs et
  coordonnées sont aussi dans son prompt (à modifier en même temps que la page).
  Domaines autorisés : baiji.fr (+ tac-velo.fr et www.tac-velo.fr à ajouter quand le
  domaine est actif). Ne PAS activer « Require origin header » : erreur 3000
  « domaine non autorisé » (incident corrigé le 07/11/2026).
- Pas de compteur de visites : `/journal.js` de baiji.fr ne compte que baiji.fr.

## Domaine (OVH, zone DNS de tac-velo.fr)
Au 07/11/2026, le domaine n'était pas encore enregistré à l'AFNIC (commande OVH en cours).
Une fois actif :
- `tac-velo.fr` : 4 enregistrements A → 185.199.108.153, 185.199.109.153,
  185.199.110.153, 185.199.111.153 (GitHub Pages)
- `www.tac-velo.fr` : CNAME → `svaug12345.github.io.` (remplace `ghs.googlehosted.com.`)
- puis fichier `CNAME` (= `tac-velo.fr`) dans le dépôt et « Enforce HTTPS » dans les réglages Pages.
