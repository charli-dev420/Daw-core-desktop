<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="Emblème DAWWW-CORE" width="180" />

# DAWWW-CORE

### Ouvrez-le comme un site. Travaillez comme dans une station. Repartez avec votre projet.

DAWWW-CORE est un **environnement de production musicale Desktop qui fonctionne dans le navigateur** et garde le projet créatif dans une logique local-first.

Le studio Desktop est disponible **maintenant, sans parcours de paiement**. Android arrivera ensuite comme produit **sur abonnement**, avec pour objectif une **compatibilité projet 100 % avec Desktop**.

[![Desktop](https://img.shields.io/badge/Desktop-DISPONIBLE%20MAINTENANT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Accès Desktop](https://img.shields.io/badge/Desktop-SANS%20PAIEMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Android](https://img.shields.io/badge/Android-%C3%80%20VENIR%20%7C%20ABONNEMENT-111827?style=for-the-badge)](#desktop-maintenant--android-ensuite)
[![Compatibilité projet](https://img.shields.io/badge/Projet-OBJECTIF%20100%25%20CROSS--DEVICE-111827?style=for-the-badge)](#desktop-maintenant--android-ensuite)
[![Format projet](https://img.shields.io/badge/Projet-.dw-111827?style=for-the-badge)](#dw-est-au-centre-du-produit)

[**Ouvrir DAWWW-CORE Desktop**](https://dawww-core-local.com/app) · [Produit](https://dawww-core-local.com/fr/studio) · [Guides](https://dawww-core-local.com/fr/docs) · [Tutoriels](https://dawww-core-local.com/fr/tutorials) · [English](README.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="Lanceur local de projets DAWWW-CORE" width="100%" />
</p>

## Ce qu'est réellement DAWWW-CORE

DAWWW-CORE n'est pas un service musical cloud auquel on aurait ajouté un séquenceur, et ce n'est pas non plus un petit sketchpad navigateur uniquement pensé pour fabriquer quelques loops.

C'est une application de type DAW construite autour d'un cycle de vie complet du projet local.

Quand on ouvre l'application Desktop, la première surface est le **lanceur de projets** : créer une session, importer un `.dw` existant ou restaurer un projet local. Une fois dans le Studio, ce même projet passe par le séquenceur, le piano roll, l'arrangeur, les instruments, les effets, l'automation et le mixeur jusqu'au rendu ou à l'export.

Le point important est que ces surfaces ne sont pas une collection de mini-outils indépendants. Elles travaillent sur la même session et le même modèle de projet.

Une session DAWWW-CORE ressemble concrètement à ceci :

```text
Créer / importer / restaurer
          ↓
Choisir un instrument
          ↓
Écrire un pattern dans le séquenceur
          ↓
Affiner les notes ou le comportement des steps
          ↓
Construire le morceau dans l'arrangeur
          ↓
Façonner instruments + effets + automation
          ↓
Router et équilibrer dans le mixeur
          ↓
Exporter l'audio / les stems
          ↓
Conserver ou déplacer le projet en .dw
```

C'est le produit résumé en une phrase : **un workflow de production dans le navigateur où la session musicale reste un projet portable au lieu de devenir indissociable d'un compte hébergé.**

## Un workflow volontairement concret

Le Browser n'est pas seulement une liste de fichiers. Il expose les instruments disponibles dans le projet et les regroupe par rôle musical. Un instrument peut être amené dans le workflow d'écriture, programmé dans le séquenceur puis édité plus finement sans changer d'application ni de contexte projet.

Le séquenceur va aussi plus loin qu'une simple grille on/off. Chaque step peut porter des comportements musicaux comme la **vélocité, la probabilité, la longueur de gate, le ratchet, l'articulation et le décalage de timing**. On peut donc introduire de la variation, casser la rigidité d'un pattern et travailler le détail rythmique avant même de passer au piano roll ou à l'arrangeur.

Pour les éléments mélodiques, le **piano roll** fournit l'édition au niveau de la note. Pour le sound design, les instruments disposent de leurs propres éditeurs dédiés au lieu de forcer tous les sons dans un panneau générique identique. Electric Piano, drums, synthés, voix orchestrales et autres familles peuvent ainsi présenter des contrôles adaptés au son réellement édité.

Une fois la matière écrite, le projet passe naturellement dans l'**arrangeur** pour la structure du morceau, puis dans le **mixeur** pour le routage, les niveaux, les traitements et le master. L'automation reste intégrée à cette même session, ce qui permet d'écrire les variations d'effets ou de paramètres directement dans le projet plutôt que de les reproduire manuellement à chaque lecture.

## Plus qu'une coquille vide de DAW

Un projet DAWWW-CORE neuf dispose déjà d'une palette sonore interne importante. Le registre intégré actuel contient **plus de 50 moteurs d'instruments**, auxquels s'ajoute un sampler, répartis notamment dans les familles suivantes :

- **Drums** — kick, snare, hand clap, closed/open hi-hat, low/mid/high toms, cowbell, rimshot, claves et maracas.
- **Basses** — sub bass, acid bass et Reese bass.
- **Electronic** — mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys et noise/transition FX.
- **Pads** — warm, glass, choir, evolving et ambient.
- **Keys & bells** — acoustic piano, electric piano, clavinet, tonewheel organ, celesta, music box et tubular bell.
- **Guitares** — nylon, steel-string, clean electric et driven electric.
- **Orchestre** — moteurs dédiés pour cordes, cuivres et bois : violin, viola, cello, contrabass, trumpet, French horn, trombone, tuba, flute, oboe, clarinet et bassoon.

Le but n'est pas de prétendre remplacer tous les plugins externes possibles. Le but est qu'**un nouveau projet puisse immédiatement devenir une vraie esquisse musicale ou une production complète sans exiger une collection de plugins séparée simplement pour commencer à faire du son.**

La couche de traitement intégrée comporte actuellement **16 effets** : EQ paramétrique 8 bandes, compressor, convolution reverb, delay synchronisé au tempo, chorus, flanger, phaser, distortion, filter, gate, limiter, saturator, tremolo, vibrato, bitcrusher et utility.

## À l'intérieur du Studio actuel

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034101.png" alt="Séquenceur DAWWW-CORE" width="100%" /><br />
      <sub><b>Séquenceur</b> — pistes, patterns et accès direct au browser d'instruments dans la même surface de production.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034231.png" alt="Éditeur détaillé des steps DAWWW-CORE" width="100%" /><br />
      <sub><b>Détail du step</b> — vélocité, chance, gate, ratchets, articulation et timing peuvent être édités individuellement.</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034213.png" alt="Mixeur DAWWW-CORE" width="100%" /><br />
      <sub><b>Mixeur</b> — canaux, routage, inserts, niveaux et master restent connectés au même projet.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="Piano roll et éditeur Hand Clap DAWWW-CORE" width="100%" /><br />
      <sub><b>Piano roll + éditeur de device</b> — éditer les données musicales tout en gardant l'instrument lui-même directement accessible.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="Éditeur Electric Piano DAWWW-CORE" width="82%" /><br />
      <sub><b>Interfaces d'instrument dédiées</b> — l'Electric Piano expose tone shaping, tremolo, enveloppe et contrôles MIDI au lieu d'un éditeur générique unique.</sub>
    </td>
  </tr>
</table>

## `.dw` est au centre du produit

Le format `.dw` n'est pas simplement une option d'export située à la fin de l'interface. C'est la représentation portable d'un projet DAWWW-CORE.

L'application Desktop conserve la session de travail dans une logique local-first, mais un projet doit aussi pouvoir quitter le navigateur proprement. `.dw` fournit ce chemin : **le sauvegarder, le déplacer, l'archiver, le réimporter ou le restaurer sur une autre surface DAWWW-CORE compatible.**

C'est important parce que beaucoup d'applications web font d'une base distante l'unique copie faisant autorité sur un projet. DAWWW-CORE choisit volontairement de ne pas faire de cela le contrat créatif du produit.

Le modèle est plutôt :

```text
Projet de travail local
        +
Projet portable .dw
        =
Une session qui n'a pas besoin d'un stockage cloud obligatoire pour exister
```

Des comptes et services en ligne peuvent exister autour de l'application, mais le projet créatif n'est pas conçu pour devenir un objet appartenant techniquement au serveur simplement parce que la station tourne dans un navigateur.

## Desktop maintenant · Android ensuite

### Desktop — disponible maintenant, sans paiement

La version Desktop Web est aujourd'hui la surface principale de DAWWW-CORE. Elle est conçue pour les écrans larges et les contrôles denses nécessaires au séquenceur, au piano roll, à l'arrangeur, aux éditeurs de devices et au mixeur.

Il n'y a **aucun parcours de paiement sur Desktop**. Le Studio peut être ouvert directement depuis le web, et l'architecture orientée PWA permet au navigateur de se rapprocher d'un comportement d'application installée lorsque la plateforme le permet.

[**Lancer le Studio Desktop →**](https://dawww-core-local.com/app)

### Android — à venir sur abonnement, avec le même projet

La version Android n'est pas prévue comme un jouet mobile séparé ni comme une application compagnon en lecture seule. Elle est développée comme le prolongement mobile du même workflow DAWWW-CORE.

Android sera proposé **sur abonnement**, avec comme cible produit une **compatibilité projet Desktop ↔ Android à 100 %**. Le même contrat `.dw` sert de base à cette continuité :

```text
Projet Desktop
      ↓
     .dw
      ↓
Projet Android
      ↓
     .dw
      ↓
Retour sur Desktop
```

Le cross-device ne signifie donc pas qu'un projet doit obligatoirement être envoyé dans un cloud avant de pouvoir changer d'appareil. Le projet portable reste une partie du design.

## Pourquoi mettre autant d'un DAW dans un navigateur ?

Parce que le navigateur apporte à DAWWW-CORE deux choses à la fois : **un accès immédiat** et un runtime applicatif moderne.

La couche audio utilise **Web Audio API** et **AudioWorklet** pour le traitement temps réel, tandis que TypeScript, React et Vite construisent la couche applicative et l'interface autour du moteur. Le stockage local navigateur et le pipeline `.dw` prennent en charge la persistance et la portabilité du projet. Le support PWA rapproche le modèle de distribution d'une application Desktop installée sans imposer un installeur traditionnel comme unique point d'entrée.

L'objectif n'est pas de faire « un DAW en JavaScript » comme démonstration technique. L'objectif est d'utiliser le web là où il est réellement utile — distribution, accès, portabilité et mises à jour rapides — sans abandonner les structures attendues d'un outil de production.

## Ce que DAWWW-CORE ne prétend pas être aujourd'hui

La direction produit actuelle est volontairement cadrée. DAWWW-CORE n'est **pas aujourd'hui construit autour** d'une synchronisation cloud obligatoire des projets, de collaboration temps réel, d'iOS ou d'une marketplace de plugins.

Ces absences font partie du scope public, ce ne sont pas des fonctions volontairement cachées derrière cette vitrine. La priorité reste la station elle-même : playback, écriture, instruments, effets, automation, mixage, récupération du projet, portabilité `.dw` et export.

## Stack publique

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · stockage local navigateur

Le code de production contient également des outils dédiés à la QA, à la récupération des projets, à la compatibilité, à l'observabilité et à la release. Cette implémentation reste privée ; ce dépôt présente le produit sans exposer les éléments opérationnels ou sensibles pour la sécurité.

## Modèle plateforme actuel

| Surface | Statut | Modèle d'accès | Modèle projet |
| --- | --- | --- | --- |
| **Desktop Web** | **Disponible maintenant** | **Sans paiement** | Local-first + `.dw` portable |
| **Android** | **À venir** | **Abonnement** | Même contrat `.dw`, objectif 100 % cross-device |
| **Sync cloud** | Non obligatoire | — | L'existence du projet n'en dépend pas |
| **Code de production** | Privé | — | Ce dépôt est la vitrine publique |

## Ressources

- **Studio Desktop** — https://dawww-core-local.com/app
- **Présentation produit** — https://dawww-core-local.com/fr/studio
- **Documentation** — https://dawww-core-local.com/fr/docs
- **Tutoriels** — https://dawww-core-local.com/fr/tutorials
- **FAQ** — https://dawww-core-local.com/fr/faq
- **Statut** — https://dawww-core-local.com/fr/status
- **Roadmap** — https://dawww-core-local.com/fr/roadmap
- **Changelog** — https://dawww-core-local.com/fr/changelog
- **Contact** — https://dawww-core-local.com/fr/contact

## À propos de ce dépôt

`Daw-core-desktop` est la **vitrine produit publique de DAWWW-CORE**.

L'application de production et le moteur audio sont développés dans un codebase privé. Ce dépôt existe pour rendre le produit compréhensible depuis l'extérieur : ce qu'il fait, comment se déroule une session, ce qui est disponible aujourd'hui et où la plateforme va ensuite.

Il ne s'agit **pas** d'une distribution open source du moteur de production. Les configurations de déploiement, artefacts QA privés, contrats fournisseurs, mécanismes de sécurité et autres détails internes sensibles restent hors de ce dépôt.

---

<div align="center">

### Créez localement. Travaillez comme dans un DAW. Gardez le projet.

[**Ouvrir DAWWW-CORE Desktop**](https://dawww-core-local.com/app)

</div>
