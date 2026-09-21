# Palais Mental

**Français** · [English](README.en.md)

Un outil de mémorisation par palais mental, contenu dans **un seul fichier HTML**. Pas d'installation, pas de compte, pas de serveur, pas de connexion requise.

Version 6.0

---

## Démarrage rapide

1. Téléchargez `palais-mental.html`
2. Ouvrez-le dans un navigateur récent — Firefox, Chrome, Edge
3. C'est tout

Pour vos élèves, l'application produit un **fichier de lecture** autonome, à distribuer comme n'importe quel fichier.

---

## Vie privée et fonctionnement hors ligne

**Tout reste sur votre appareil.** L'application ne contacte aucun serveur au démarrage : ni Google, ni mesure d'audience, ni police téléchargée, ni bibliothèque externe. Tout le nécessaire est dans le fichier.

**Tout fonctionne sans connexion**, application comme fichier élève : création, révision, rappels, import et export de tableurs, sauvegardes, archives ZIP.

Seules deux fonctions, **facultatives**, passent par internet — et uniquement quand vous les déclenchez :

- la **génération d'images** par IA
- la **recherche de photos** libres de droits

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

- **Palais** — une matière, un programme, un thème. *« Programme 3e Histoire-Géo »*
- **Salle** — un chapitre, une notion. *« La Seconde Guerre mondiale »*
- **Objet** — une chose à retenir. *« Bataille de Stalingrad »*

Un objet porte un **titre** (ce qu'il faut retrouver), une **information à retenir**, et éventuellement une **image**, une **phrase mnémotechnique**, des **étiquettes** et un **document joint**.

Le tri choisi sur l'accueil — ordre de création, alphabétique, plus récents, plus grands — s'applique à **toutes** les listes de palais de l'application.

## 2. Créer le contenu

**Par tableur, la voie la plus rapide pour un gros volume.** Exportez le modèle vierge depuis les Paramètres, remplissez-le, réimportez-le. Une ligne = un objet. Les colonnes `palais`, `salle` et `objet` construisent la structure ; les salles manquantes sont créées.

Un prompt est fourni pour faire générer ce tableur par une IA. Attention : les modèles remplissent la colonne `favori` avec beaucoup d'enthousiasme — voyez la section Favoris.

**À la main**, palais par palais.

**Par import** d'une sauvegarde ou d'une archive, JSON ou ZIP.

## 3. Affiner le contenu

Un contenu généré est globalement juste, jamais parfait. Le mode **Parcourir** fait défiler les objets sans interrogation : c'est le mode de relecture. Deux boutons y servent sans cesse :

- **Modifier** — corrige la fiche et vous ramène exactement à la même carte
- **Favori** — l'étoile marque ce qui mérite d'être gardé

**Le circuit de curation**, pour extraire le meilleur d'un gros palais généré :

1. Dupliquez le palais (menu « Plus »)
2. Parcourez la copie en étoilant ce que vous gardez
3. Dans une salle, cliquez **Favoris** jusqu'à afficher **« Non favoris »**
4. Sélectionnez tout, supprimez

La suppression groupée reste annulable douze secondes, et un instantané est pris avant.

> Dupliquer un palais double son poids, images comprises.

## 4. Les images

Pour un objet ou pour un lot entier :

- **Import** depuis votre appareil
- **Génération par IA** — service Pollinations, gratuit, clé facultative
- **Photo réelle** — Openverse, Wikimedia Commons et autres services libres

**Le style de génération compte plus que tout.** Les styles fournis produisent volontairement des images absurdes : efficaces pour ancrer un mot isolé, inutiles pour illustrer une notion. Le style **« Fidèle au sujet »** s'appuie sur le contenu et la salle.

En génération par lot, le style est fixé une fois pour toute la série : les images d'un même palais se ressemblent.

## 5. Les documents joints

Chaque objet peut porter un PDF, un document Word, Excel ou LibreOffice.

- **PDF** → s'ouvre dans une fenêtre pendant la révision, hors connexion comprise
- **Autres formats** → s'ouvrent dans le logiciel de l'élève, aucun navigateur ne sachant les afficher

**Import en lot** : chaque fichier rejoint l'objet dont le titre correspond à son nom, extension retirée. Un bilan liste ce qui n'a trouvé aucune correspondance.

## 6. Réviser

La révision est espacée : un objet su revient plus tard, un objet manqué revient vite.

Pendant une révision, la barre du haut permet de **modifier** l'objet, de l'**étoiler**, de **mettre la session de côté**, d'afficher la phrase mnémotechnique ou de masquer les images.

Une session interrompue est reprise automatiquement : un bandeau le propose au retour.

## 7. Les favoris

L'étoile marque un objet — dans une salle, en révision ou en parcours. L'entrée **Favoris** du menu latéral les révise tous, palais confondus.

Le filtre d'une salle a trois états : **tous**, **favoris**, **non favoris**.

**Retrait en masse** dans les Paramètres : palais par palais ou en une fois, annulable. Indispensable après un import de tableur généré par IA.

## 8. Les rappels

Une série de rappels programme des révisions à dates précises : **ce qu'il faut revoir** (palais entiers ou salles), un **point de départ** et une **série de délais** — J+1, J+3, J+7, J+14, J+30, ou la vôtre.

Séries toutes faites : **Courbe de l'oubli**, **Progressive**, **Hebdomadaire**, **Avant examen**. Toutes modifiables.

Dans la liste des cibles, chaque palais se plie et se déplie ; **Tout déplier** et **Tout replier** agissent sur l'ensemble.

L'**Agenda** présente un calendrier mensuel à pastilles colorées et la liste des séries en cours.

## 9. Sauvegarder, archiver

**Sauvegarde complète**, JSON ou ZIP : tous les palais, images, documents, progression, rappels, fond d'écran, services personnalisés, révisions mises de côté. Le ZIP est plus léger dès qu'il y a des images.

**Archive de palais choisis**, JSON ou ZIP : seulement les palais cochés, avec leur contenu complet. Elle ne contient **aucun réglage** — la réimporter ne touche ni à vos styles, ni à votre fond d'écran, ni à vos rappels. C'est l'outil pour alléger l'application ou transmettre une matière.

**Instantanés** : pris automatiquement avant chaque opération risquée, restaurables depuis les Paramètres.

**Diagnostic** : vérifie l'intégrité et signale les images orphelines, sans exposer votre contenu.

> Les clés d'accès aux services ne sont **jamais** exportées.

## 10. Importer une grosse base

Pendant un import, une fenêtre indique l'étape en cours, la progression palais par palais, le temps écoulé et une estimation du temps restant.

À la fin, si la base est volumineuse, un bilan la situe :

| Niveau | Nombre d'objets |
|---|---|
| Confortable | moins de 3 000 |
| Chargée | 3 000 à 8 000 |
| Lourde | plus de 8 000 |

Ces seuils sont des **repères estimés**, pas des limites techniques : au-delà, tout fonctionne, plus lentement sur téléphone. Le conseil est alors d'archiver les matières dont vous ne vous servez pas en ce moment, puis de les retirer.

## 11. Exporter pour les élèves

Paramètres → **Exporter en lecture seule**.

1. Dépliez **Choisir les palais** et cochez ceux à distribuer
2. Vérifiez la **taille estimée** et l'indicateur de confort
3. Choisissez un nom, ou une des trois propositions
4. Cochez **« Réinitialiser les statistiques »** si le fichier est pour quelqu'un d'autre
5. Générez

| Taille | Ce que ça donne |
|---|---|
| moins de 8 Mo | Confortable partout, téléphone modeste compris |
| 8 à 25 Mo | Ouverture un peu lente sur appareil ancien |
| 25 à 60 Mo | Envoi par messagerie souvent refusé |
| plus de 60 Mo | Risque de blocage sur téléphone |

Le même panneau **Choisir les palais**, pliable, sert aux trois exports : lecture seule, archive, tableur.

## 12. Le fond d'écran

Paramètres → **Fond d'écran**, trois onglets : **Générer (IA)**, **Photo libre**, **Importer**.

Les propositions s'accumulent dans une galerie. Un clic place une image **en aperçu** : votre fond actuel reste en place tant que vous n'avez pas cliqué **Appliquer ce fond**. Après application, **Revenir au fond précédent** annule le changement.

---

# Deuxième partie — Le fichier de lecture

*À transmettre aux élèves.*

## Ouvrir

Double-cliquez sur le fichier. Il s'ouvre dans votre navigateur. **Aucune connexion nécessaire**, et rien n'est envoyé nulle part.

## Ce qu'on peut faire

**Parcourir** les palais, les salles et les objets.

**Réviser** : une question apparaît, vous cherchez, vous révélez, vous indiquez si c'était su. Les révisions suivantes s'espacent en conséquence.

**Se programmer des rappels** : ce que vous voulez revoir, une date de départ, une série de délais ou un modèle tout fait.

**Trier les palais** : ordre d'origine, alphabétique, plus récents, plus grands.

## Ce qu'on ne peut pas faire

Créer, modifier ou supprimer. Le contenu est celui que votre enseignant a validé.

## Votre progression

Elle est enregistrée **dans votre navigateur, sur votre appareil**, et ne remonte à personne.

Vous la retrouvez en rouvrant le fichier sur le même appareil et le même navigateur. Elle ne vous suit pas sur un autre appareil, et effacer les données du navigateur l'efface aussi.

---

# Troisième partie — Référence technique

## Formats acceptés

| Usage | Formats |
|---|---|
| Import de contenu | `.xlsx`, `.csv`, `.ods`, `.json`, `.zip` |
| Images | `.jpg`, `.png`, `.webp`, `.gif` |
| Documents joints | `.pdf`, `.docx`, `.doc`, `.odt`, `.xlsx`, `.xls`, `.ods`, `.csv`, `.rtf`, `.txt` |

## Limites

- **Document joint** : avertissement au-delà de 2 Mo, refus au-delà de 12 Mo
- **Images** : redimensionnées à 640 px ; fond d'écran à 1600 px
- **Fichier de lecture** : au-delà de 25 Mo, envoi par messagerie souvent refusé

## Où sont les données

Dans le stockage local du navigateur. Elles survivent à la fermeture, mais **pas** à un effacement des données du navigateur, ni à un changement d'appareil.

Le navigateur range les données **par adresse**, pas par fichier : deux copies de l'application ouvertes depuis la même adresse partagent la même base.

**Exportez régulièrement.** C'est la seule vraie sauvegarde.

## Services d'images

Deux familles de services, **gratuits et facultatifs** :

- **Pollinations** — génération par IA. Sans clé, compter environ 23 secondes entre deux images ; avec une clé, environ 9.
- **Photos réelles** — Openverse, Wikimedia Commons, et d'autres à déclarer.

Dans les Paramètres, vous pouvez déclarer vos propres services, les tester, les retirer, et choisir celui utilisé par défaut.

## En cas de problème

| Symptôme | À vérifier |
|---|---|
| Le fichier élève n'affiche rien | Il a été généré avec une version ancienne : régénérez-le |
| La génération d'image échoue | Un VPN est souvent bloqué par le service ; une clé dont le compte est épuisé aussi — retirez-la pour repasser en accès anonyme |
| Le fichier élève est trop lourd | Moins d'images, PDF allégés, ou un fichier par matière |
| Une suppression regrettée | Le bandeau d'annulation (douze secondes), sinon un instantané |
| Des favoris jamais posés | Ils viennent du tableur importé : retrait en masse dans les Paramètres |
| L'application est lente sur téléphone | Voir le bilan de volume : archivez les matières inactives |

## Limites connues

- **iPad et Safari** : un dysfonctionnement du fichier de lecture a été signalé et n'est pas encore diagnostiqué.
- **SheetJS 0.18.5**, intégré pour la lecture des tableurs, présente des failles connues à l'import de fichiers piégés. Le risque est faible tant que vous n'importez que vos propres tableurs. N'importez pas de tableur d'origine inconnue.

## Bibliothèques tierces

Intégrées au fichier, sous leurs licences respectives :

| Bibliothèque | Version | Licence |
|---|---|---|
| Vue | 3 | MIT |
| SheetJS | 0.18.5 | Apache-2.0 |
| PapaParse | 5.3.0 | MIT |
| JSZip | 3.10.1 | MIT ou GPLv3, au choix |

## Licence

Voir le fichier `LICENSE`.
