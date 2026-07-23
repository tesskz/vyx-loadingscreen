================================================================
  VYX — LOADING SCREEN  (Hunter x Hunter)
================================================================

CONTENU
  index.html        La page de chargement (design HxH/VYX).
  assets/video.mp4  <- REMPLACE par ta video en boucle (format .mp4, H.264).
  assets/son.mp3    <- REMPLACE par ton son en boucle (format .mp3).

  (Les 2 fichiers dans assets/ sont des PLACEHOLDERS vides : mets tes
   vrais fichiers a la place, en gardant EXACTEMENT les memes noms.
   Si tu veux d'autres noms, edite les <source src="..."> dans index.html.)

--------------------------------------------------------------
1) HEBERGER (gratuit, ~2 min, aucun code)
--------------------------------------------------------------
Le loading screen GMod charge une URL web : il faut donc mettre ce
dossier en ligne. Le plus simple, au choix :

  * Netlify Drop  ->  https://app.netlify.com/drop
      Glisse-depose le dossier "vyx-loading" entier. Il te donne une URL.

  * Cloudflare Pages / GitHub Pages : pareil, upload le dossier.

Ton URL finale ressemblera a :
  https://ton-site.netlify.app/index.html

--------------------------------------------------------------
2) BRANCHER SUR LE SERVEUR
--------------------------------------------------------------
Dans server.cfg (ou via la console serveur) :

  sv_loadingurl "https://ton-site.netlify.app/index.html"

Reboot le serveur. Les joueurs qui rejoignent verront l'ecran.

--------------------------------------------------------------
NOTES
--------------------------------------------------------------
* La VIDEO est muette (obligatoire pour l'autoplay des navigateurs).
* Le SON ne peut pas demarrer tout seul (bloque par les navigateurs) :
  un bouton "Activer le son" est affiche en haut a droite, ET le son
  se lance aussi au 1er clic n'importe ou sur la page.
* La barre de progression + le nom du serveur / carte / mode se
  remplissent automatiquement (API de chargement GMod).
* Poids : garde la video legere (< 15-20 Mo idealement) pour un
  chargement rapide chez les joueurs.
================================================================
