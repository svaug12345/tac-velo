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
  validés par Julien le 07/11/2026), `NETTOYAGES` + `SUPPLEMENTS_NETTOYAGE`
  (formules de nettoyage, prix produits compris, validés aussi), `ASTUCES`, diagnostic `DIAG_*`,
  assistant vocal `AGENT_RAYON`. Version dans le commentaire d'en-tête et `VERSION`.
- `manifest.webmanifest`, `sw.js`, `icones/` — page installable (PWA). Chemins
  relatifs (`./`) pour marcher aussi bien sur baiji.fr/tac-velo/ que sur tac-velo.fr/.

## Règles
- À chaque modification : augmenter `VERSION` et ajouter une ligne à l'historique
  en tête de `index.html` (sinon les téléphones gardent l'ancienne version en cache).
- Code commenté en français : l'auteur apprend en lisant.
- Nom affiché : « TAC Vélo », Julien présenté comme le mécanicien. Ne jamais écrire « Juju ».
- Adresse de l'atelier publiée depuis la v1.8.1 (9 avenue Lannes, 91190 Gif-sur-Yvette, « atelier de quartier », sur rendez-vous) : même adresse que la fiche Google.
- Tarifs (réparations + nettoyage) validés par Julien le 07/11/2026 : plus de `noindex` depuis la v1.9.1 (page visible de Google). Toute nouvelle prestation ou nouveau prix : à refaire valider par Julien.
- Référencement (v1.10.0) : nom, adresse et téléphone doivent rester identiques dans
  le JSON-LD (`<head>`), le pied de page et la fiche Google Business Profile.
- Zone validée par Julien : Gif-sur-Yvette, Gometz, Bures-sur-Yvette (bandeau « zone »,
  `JULIEN.zone` et `areaServed` du JSON-LD, qui détaille Gometz-le-Châtel et Gometz-la-Ville).
- Pas d'horaires affichés (choix de Julien) : `JULIEN.horaires` reste vide, pas d'`openingHours`.
- Rayon (agent ElevenLabs `agent_9901m6b24af2f15s8fxy0ezqm92c`) : ses tarifs et
  coordonnées sont aussi dans son prompt (à modifier en même temps que la page).
  Prompt mis à jour le 07/11/2026 (formules de nettoyage v1.9.0 ; TAC Vélo, atelier de quartier 9 avenue Lannes sur
  rendez-vous, « Julien regarde, annonce le prix, le client décide »).
  Limites (07/11/2026) : 30 appels/jour, 4 min max par appel, voix enregistrée,
  audio et transcriptions gardés 30 jours.
  Domaines autorisés : baiji.fr, www.baiji.fr, tac-velo.fr, www.tac-velo.fr. Ne PAS activer « Require origin header » : erreur 3000
  « domaine non autorisé » (incident corrigé le 07/11/2026).
- Pas de compteur `/journal.js` (il ne compte que baiji.fr). Depuis la v1.10.0 : suivi
  Google Analytics 4 + Google Ads, réglé dans l'objet `SUIVI` (dernier gros `<script>`).
  Bandeau cookies CNIL : aucun script Google avant « Accepter », boutons Accepter/Refuser
  identiques, choix gardé 6 mois, lien « Cookies » en pied de page. Ne pas passer en
  « mode avancé » du consentement (pings Google avant accord) sans avis juridique.

## Adresse officielle provisoire (depuis la v1.10.0, 10/11/2026)
Tant que tac-velo.fr n'est pas en ligne, le site est publié sur **https://baiji.fr/julien/**
(dossier `julien/` du dépôt `svaug12345.github.io`) et c'est cette adresse qui est déclarée
partout : `<link rel="canonical">`, `og:url`, `og:image`, JSON-LD (`@id`, `url`, `logo`,
`image`), `sitemap.xml`, ligne `Sitemap:` de `robots.txt`. Le jour où tac-velo.fr marche :
tout remettre sur `https://tac-velo.fr/`, puis rediriger baiji.fr/julien/ vers tac-velo.fr
et déclarer le changement d'adresse dans Search Console. Google Ads (AW-18568190227 depuis la v1.10.2 ; l'ancien compte AW-1041764794 / 110-150-9374 est fermé) et la
conversion « Click to call » ne dépendent pas de l'adresse.

## Domaine (OVH, zone DNS de tac-velo.fr)
Au 07/11/2026, le domaine n'était pas encore enregistré à l'AFNIC (commande OVH en cours).
Une fois actif :
- `tac-velo.fr` : 4 enregistrements A → 185.199.108.153, 185.199.109.153,
  185.199.110.153, 185.199.111.153 (GitHub Pages)
- `www.tac-velo.fr` : CNAME → `svaug12345.github.io.` (remplace `ghs.googlehosted.com.`)
- puis fichier `CNAME` (= `tac-velo.fr`) dans le dépôt et « Enforce HTTPS » dans les réglages Pages.
