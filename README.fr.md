# Palais Mental

**Français** · [English](README.en.md)

Un outil de mémorisation par palais mental et répétition espacée, contenu dans **un seul fichier HTML**. Pas d'installation, pas de compte, pas de serveur, pas de connexion requise.

Version 7.0

---

## Démarrage rapide

1. Téléchargez `palais-mental.html`
2. Ouvrez-le dans Firefox — ou dans Chrome et Edge, voir « Plateformes et navigateurs »
3. C'est tout

Pour vos élèves, l'application produit un **fichier de lecture** autonome, à distribuer comme n'importe quel fichier.

**Un mot vous échappe ?** Le **Glossaire**, dans le menu latéral, définit chaque terme de l'application en une phrase et dit où le trouver.

---

## Vie privée, hors ligne, sécurité

**Tout reste sur votre appareil.** L'application ne contacte aucun serveur au démarrage : ni Google, ni mesure d'audience, ni police téléchargée, ni bibliothèque externe. Tout le nécessaire est dans le fichier.

**Tout fonctionne sans connexion**, application comme fichier élève : création, révision, rappels, import et export de tableurs, sauvegardes, archives ZIP.

Seules quelques fonctions **facultatives** passent par internet, et uniquement quand vous les déclenchez : la génération d'images, la recherche de photos libres et de définitions, et les boutons qui ouvrent une IA depuis le générateur de prompt.

**Le contenu importé est traité comme non fiable.** Un tableur ou une sauvegarde piégés ne peuvent pas exécuter de code : le texte est neutralisé avant affichage, et seules les adresses web `https://` ou `http://` peuvent être ouvertes.

---

## Plateformes et navigateurs

| Plateforme | Fichier ouvert depuis le disque | Fichier servi par une adresse web |
|---|---|---|
| **Windows, macOS, Linux — Firefox** | Complet | Complet |
| **Windows, macOS, Linux — Chrome, Edge** | Capacité réduite, voir ci-dessous | Complet |
| **Android — Firefox, Chrome** | Complet | Complet |
| **iPad, iPhone** | Non pris en charge | Non pris en charge |

**Chrome et Edge** refusent le stockage complet aux fichiers ouverts depuis le disque. L'application bascule alors sur un stockage de secours et l'annonce par un bandeau : tout fonctionne, mais la capacité tombe à quelques mégaoctets, vite insuffisante avec des images. Deux solutions : ouvrir le fichier avec **Firefox**, ou le servir depuis une adresse web — un petit serveur local suffit.

**Le fichier de lecture** n'a pas cette limite : la progression d'un élève pèse quelques kilooctets, le stockage de secours la conserve sans difficulté.

**Sur un lecteur réseau**, utilisez une lettre de lecteur (`Z:`) ou une adresse web, plutôt qu'un chemin `\\serveur\partage` que certains navigateurs bloquent. Les données ne sont jamais écrites sur le partage : chaque utilisateur a les siennes, sur son poste, et vingt élèves peuvent ouvrir le même fichier en même temps.

**Sur iPad et iPhone**, l'aperçu de l'app Fichiers n'exécute pas le JavaScript : l'application ne peut pas démarrer depuis un fichier local. Un message l'explique au lieu d'afficher une page vide.

---

## Deux formes

| | **L'application** | **Le fichier de lecture** |
|---|---|---|
| Pour qui | L'enseignant | Les élèves |
| Créer, modifier, supprimer | Oui | Non |
| Réviser, parcourir, se programmer des rappels | Oui | Oui |
| Progression enregistrée | Sur votre appareil | Sur l'appareil de l'élève, sans jamais toucher à votre version |

---

# Première partie — L'application

## 1. La structure

Trois niveaux, du plus large au plus fin :

- **Palais** — une matière, un programme, un thème. *« Histoire-géographie 3e »*
- **Salle** — un chapitre, une notion. *« La Seconde Guerre mondiale »*
- **Objet** — une fiche, une chose à retenir. *« Débarquement de Normandie »*

Un objet porte un **titre** (la question), une **information à retenir** (la réponse), et éventuellement une **image**, une **phrase mnémotechnique**, des **étiquettes** et un **document joint**.

Le tri choisi sur l'accueil s'applique à toutes les listes de palais de l'application.

## 2. Créer du contenu

Quatre voies :

- **Le générateur de prompt** — la plus simple pour débuter, voir la section suivante.
- **Un tableur**, rempli à la main ou par une IA. Le modèle vierge se télécharge dans Paramètres → Créer et organiser le contenu → Import / export tableur. Une ligne = une fiche ; les palais et salles manquants sont créés à l'import.
- **À la main**, palais par palais.
- **L'import** d'une sauvegarde ou d'une archive, en JSON ou en ZIP.

**Après un import**, un bilan confirme que tout est enregistré — nombre de fiches, détail par palais — et propose, **en option**, d'ajouter des images, avec une estimation de la durée. On peut aussi le faire plus tard.

## 3. Le générateur de prompt

Il rédige pour vous la demande à faire à une IA. Menu latéral → **Générateur de prompt**.

**Trois niveaux de personnalisation :**

| Niveau | Ce qu'on remplit |
|---|---|
| **Express** | Le sujet, le public, le nombre de fiches. L'IA propose le reste. |
| **Guidé** — *par défaut* | + nom du palais, salles, types de contenu, images, favoris |
| **Expert** | + lignes « Méthode » et « Piège », mnémotechniques, longueur des réponses, style d'image, référence à suivre, exclusions |

**Les règles d'une bonne fiche de répétition espacée sont ajoutées d'office**, à tous les niveaux : des faits atomiques, un titre qui ne contient jamais la réponse, des réponses toutes différentes pour la révision à l'envers, l'interdiction d'inventer, aucune carte ni sujet douloureux en image.

**Adapter pour**, à tous les niveaux :
- cinq cases qui se cumulent : **dyslexie et dysorthographie, dyscalculie, dyspraxie, dysphasie, troubles de l'attention** ;
- **élèves allophones (FLS)** : 35 langues d'origine au choix, plus une langue libre, et le niveau de français de A1 à B1. L'IA ajoute la traduction et, si besoin, une transcription en alphabet latin. Faites-la relire par un locuteur quand c'est possible.

**Le résultat** se met à jour en direct. « Copier le prompt », « Télécharger le modèle vierge », puis six IA — ChatGPT, Claude, Gemini, Le Chat, DeepSeek, Copilot : chaque bouton copie le prompt puis ouvre le site. Il reste à joindre le modèle vierge et coller. **« + Ajouter une IA »** permet d'ajouter n'importe quelle autre IA par son adresse.

**Pour les IA gratuites** qui ne savent pas produire de fichier, le prompt leur demande un tableau CSV à points-virgules, que l'application importe aussi.

**La bibliothèque** conserve vos prompts : les recharger dans le formulaire, les renommer, les modifier, les copier, les supprimer.

## 4. Affiner le contenu

Un contenu généré est globalement juste, jamais parfait. Le mode **Parcourir** fait défiler les fiches sans interrogation : c'est le mode de relecture.

- **Modifier** corrige la fiche et vous ramène à la même carte.
- **L'étoile** marque ce qui mérite d'être gardé.

**Le circuit de curation**, pour extraire le meilleur d'un gros palais généré :

1. Dupliquer le palais (menu « Plus »)
2. Parcourir la copie en étoilant ce que vous gardez
3. Dans une salle, cliquer **Favoris** jusqu'à afficher **« Non favoris »**
4. Tout sélectionner, supprimer

La suppression reste annulable douze secondes, et un instantané est pris avant.

## 5. Les images

Trois sources, pour une fiche ou pour un lot :

- **Génération par IA** — Pollinations.ai, gratuit, sans compte, clé facultative
- **Photo libre** — Openverse, Wikimedia Commons ; l'auteur, la source et la licence sont conservés
- **Import** depuis votre appareil

**Le style compte plus que tout.** « Fidèle au sujet » illustre la notion ; les autres styles créent des scènes décalées, efficaces pour un mot isolé. En lot, le style est fixé pour toute la série.

**Images en lot** : Paramètres → Images et services en ligne → Images en lot, ou menu « Plus » d'un palais.

## 6. Les documents joints

Chaque fiche peut porter un PDF ou un document bureautique. Le PDF s'ouvre pendant la révision, même hors connexion ; les autres formats s'ouvrent dans le logiciel de l'élève. Un import en lot associe chaque fichier à la fiche dont le titre correspond à son nom.

## 7. Réviser

La révision est espacée : une fiche sue revient plus tard, une fiche manquée revient vite.

**Au-dessus de chaque question**, une ligne indique d'où vient la fiche — *● Histoire-géographie 3e › La Seconde Guerre mondiale* — avec la couleur du palais. On sait toujours où l'on est, même dans une révision qui mélange plusieurs salles.

Pendant une révision : modifier la fiche, l'étoiler, **la mettre de côté** pour reprendre plus tard, afficher la phrase mnémotechnique, masquer les images. Une session interrompue est proposée à la reprise au retour.

**Le mode position** demande de retrouver une fiche à partir de sa salle et de son rang, comme dans un vrai palais mental.

## 8. Les favoris

L'étoile marque une fiche — dans une salle, en révision ou en parcours. Menu latéral → **Favoris** pour les réviser tous, palais confondus ; **« Parcourir les favoris »** pour les relire sans interrogation.

Le filtre d'une salle a trois états : tous, favoris, non favoris. **Retrait en masse** dans Paramètres → Créer et organiser le contenu → Favoris.

## 9. Les rappels

Une série de rappels programme des révisions à dates précises : ce qu'il faut revoir, un point de départ, des délais — J+1, J+3, J+7…

Séries prêtes : **Courbe de l'oubli**, **Progressive**, **Hebdomadaire**, **Avant examen**. Toutes modifiables. L'**Agenda** présente un calendrier à pastilles colorées.

## 10. Sauvegarder, archiver

Paramètres → Exporter et sauvegarder :

- **Sauvegarde & transfert** — la **sauvegarde complète**, en JSON ou en ZIP : palais, images, documents, progression, rappels, fond d'écran, services, bibliothèque de prompts, IA ajoutées. Et l'**archive de palais choisis**, sans aucun réglage : la réimporter ne touche à rien d'autre.
- **Sauvegardes automatiques** — des instantanés pris avant chaque opération risquée, restaurables.

> Les clés d'accès aux services ne sont **jamais** exportées.

## 11. Importer une grosse base

Pendant un import, une fenêtre montre l'étape en cours, la progression et une estimation du temps restant. À la fin, un bilan situe la base : **confortable** sous 3 000 fiches, **chargée** jusqu'à 8 000, **lourde** au-delà. Ce sont des repères estimés, pas des limites : au-delà, tout fonctionne, plus lentement sur téléphone. Archivez alors les matières inactives.

## 12. Exporter pour les élèves

Paramètres → Exporter et sauvegarder → **Exporter en lecture seule** :

1. Dépliez **« Choisir les palais »** et cochez ceux à distribuer
2. Vérifiez la **taille estimée** et l'indicateur de confort
3. Choisissez un nom, ou une des propositions
4. Cochez **« Réinitialiser les statistiques »** si le fichier est pour quelqu'un d'autre
5. Générez

| Taille | Ce que ça donne |
|---|---|
| moins de 8 Mo | Confortable partout |
| 8 à 25 Mo | Ouverture un peu lente sur appareil ancien |
| 25 à 60 Mo | Envoi par messagerie souvent refusé |
| plus de 60 Mo | Risque de blocage sur téléphone |

**Après une correction, régénérez et redistribuez** : un fichier déjà distribué ne se met pas à jour tout seul.

## 13. Le fond d'écran

Paramètres → Apparence → Fond d'écran, trois onglets : **Générer (IA)**, **Photo libre**, **Importer**. Un clic place une image en aperçu ; votre fond actuel reste en place jusqu'à **« Appliquer ce fond »**, et **« Revenir au fond précédent »** annule.

## 14. Paramètres, explications et glossaire

Les Paramètres sont rangés sous **cinq thèmes**, chacun avec sa couleur : créer et organiser le contenu, images et services en ligne, exporter et sauvegarder, apparence, avancé. Chaque section affiche **un résumé d'une ligne**, même repliée.

**Les explications détaillées sont masquées** et s'ouvrent section par section avec le **« ? »**. Pour les afficher partout : Apparence → **« Toujours afficher les explications »**.

**Le Glossaire** — menu latéral — définit une quarantaine de termes en cinq familles, avec une recherche et, pour chaque mot, où le trouver.

---

# Deuxième partie — Le fichier de lecture

*À transmettre aux élèves.*

## Ouvrir

Double-cliquez sur le fichier. Il s'ouvre dans votre navigateur. **Aucune connexion nécessaire**, et rien n'est envoyé nulle part.

Si un message dit que le fichier ne peut pas s'ouvrir ici, c'est qu'il est affiché dans un simple aperçu : ouvrez-le avec Firefox, Chrome ou Edge.

## Ce qu'on peut faire

**Parcourir** les palais, les salles et les fiches. **Réviser** : une question, vous cherchez, vous révélez, vous indiquez si vous saviez — la ligne au-dessus de la question rappelle toujours le palais et la salle. **Se programmer des rappels**. **Trier les palais**.

## Ce qu'on ne peut pas faire

Créer, modifier ou supprimer. Le contenu est celui que votre enseignant a validé.

## Votre progression

Elle est enregistrée **dans votre navigateur, sur votre appareil**, et ne remonte à personne. Vous la retrouvez en rouvrant le fichier sur le même appareil et le même navigateur ; elle ne vous suit pas sur un autre poste.

Si le navigateur refuse tout enregistrement, un bandeau vous prévient **avant** que vous ne révisiez pour rien.

---

# Troisième partie — Référence technique

## Formats acceptés

| Usage | Formats |
|---|---|
| Import de contenu | `.xlsx`, `.ods`, `.csv` (virgules ou points-virgules), `.json`, `.zip` |
| Images | `.jpg`, `.png`, `.webp`, `.gif` |
| Documents joints | `.pdf`, `.docx`, `.doc`, `.odt`, `.xlsx`, `.xls`, `.ods`, `.csv`, `.rtf`, `.txt` |

## Limites

- **Document joint** : avertissement au-delà de 2 Mo, refus au-delà de 12 Mo
- **Images** : redimensionnées à 640 px ; fond d'écran à 1600 px
- **Fichier de lecture** : au-delà de 25 Mo, envoi par messagerie souvent refusé

## Où sont les données

Dans le stockage du navigateur, **par adresse** et non par fichier : deux copies de l'application ouvertes depuis la même adresse partagent la même base. Les données survivent à la fermeture, mais pas à un effacement des données du navigateur ni à un changement d'appareil.

**Exportez régulièrement.** C'est la seule vraie sauvegarde.

## Services d'images

- **Pollinations** — génération par IA. Délai imposé par le service gratuit : environ **16 secondes** pour une image, **23 par image en lot**. Avec une clé : 6 et 9 secondes.
- **Photos libres** — Openverse, Wikimedia Commons, et d'autres services à déclarer dans Paramètres → Images et services en ligne → Clés d'accès aux services.

## En cas de problème

| Symptôme | À vérifier |
|---|---|
| Bandeau « Stockage réduit dans ce navigateur » | Chrome ou Edge sur un fichier local : ouvrez-le avec Firefox, ou depuis une adresse web |
| Message « ne peut pas s'ouvrir ici » | Le fichier est affiché dans un aperçu : ouvrez-le dans Firefox, Chrome ou Edge |
| Le fichier élève n'affiche rien | Il vient d'une version ancienne : régénérez-le |
| La génération d'image échoue | Un VPN est souvent bloqué par le service, de même qu'une clé dont le compte est épuisé |
| Des favoris jamais posés | Ils viennent du tableur importé : retrait en masse dans Paramètres → Favoris |
| L'application est lente sur téléphone | Voir le bilan de volume : archivez les matières inactives |
| Une suppression regrettée | Le bandeau d'annulation (douze secondes), sinon un instantané |

## Limites connues

- **iPad et iPhone** : non pris en charge.
- **Chrome et Edge sur un fichier local** : capacité de stockage réduite, voir « Plateformes et navigateurs ».
- **SheetJS 0.18.5**, intégré pour lire les tableurs, présente des failles connues à l'import de fichiers piégés. N'importez pas de tableur d'origine inconnue.

## Ressources fournies avec le projet

| Fichier | Contenu |
|---|---|
| `TUTORIELS.md` | Six parcours pas à pas, de la voie express à la sauvegarde |
| `GUIDE-ELEVE.md` | Une page pour les élèves, à imprimer ou joindre |
| `PROMPT-UNIVERSEL.md` | Le prompt à copier pour faire remplir un tableur par une IA |
| `Palais-Mental-Prompts` (`.xlsx`, `.ods`) | 24 prompts prêts par domaine, et un questionnaire |
| `Palais-Mental-Schemas.drawio` | Cinq schémas modifiables dans draw.io |

## Bibliothèques tierces

Intégrées au fichier, sous leurs licences respectives :

| Bibliothèque | Version | Licence |
|---|---|---|
| Vue | 3.4 | MIT |
| SheetJS | 0.18.5 | Apache-2.0 |
| PapaParse | 5.3.0 | MIT |
| JSZip | 3.10.1 | MIT ou GPLv3, au choix |

## Licence

Voir le fichier `LICENSE`.
