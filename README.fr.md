<div align="center">

# DAWWW-CORE

### Une vraie station de production musicale dans le navigateur.

**Composez. Séquencez. Arrangez. Mixez. Automatisez. Exportez.**  
Sans installation lourde, sans paiement sur Desktop et sans rendre le cloud obligatoire pour posséder vos projets.

[![Desktop](https://img.shields.io/badge/Desktop-disponible%20sans%20paiement-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Android](https://img.shields.io/badge/Android-%C3%A0%20venir%20%7C%20abonnement-111827?style=for-the-badge)](#desktop-aujourdhui--android-ensuite)
[![Cross-device](https://img.shields.io/badge/projets-100%25%20cross--device-111827?style=for-the-badge)](#desktop-aujourdhui--android-ensuite)
[![Local-first](https://img.shields.io/badge/architecture-local--first-111827?style=for-the-badge)](#local-first-par-conception)
[![Project format](https://img.shields.io/badge/projets-.dw-111827?style=for-the-badge)](#dw--un-projet-qui-vous-appartient)

[**Ouvrir le studio**](https://dawww-core-local.com/app) · [Guides](https://dawww-core-local.com/fr/docs) · [Tutoriels](https://dawww-core-local.com/fr/tutorials) · [Roadmap](https://dawww-core-local.com/fr/roadmap) · [English](README.md)

</div>

---

## Le navigateur peut être un vrai studio

DAWWW-CORE est une station audionumérique desktop construite autour d'une idée simple : **ouvrir un navigateur ne devrait pas signifier accepter un workflow musical simplifié**.

Le studio réunit dans le même espace les étapes essentielles d'une production : création de patterns, édition de notes, arrangement, instruments, effets, automation, mixage et export. L'objectif n'est pas de proposer une démo de DAW ou un petit bloc-notes musical, mais un environnement cohérent dans lequel une idée peut devenir un morceau.

La version **Desktop est disponible sans paiement**. Vous ouvrez le studio depuis le web, travaillez sur votre projet, puis conservez ce travail dans un format portable `.dw` qui reste sous votre contrôle.

DAWWW-CORE est également conçu pour aller plus loin : une version **Android est à venir sur abonnement**, avec une continuité de projet **100 % cross-device** entre Desktop et Android.

> Un même projet. Un même format. Deux plateformes. Pas deux workflows séparés.

## En un coup d'œil

| | DAWWW-CORE |
| --- | --- |
| **Desktop Web** | Disponible maintenant, **sans paiement** |
| **Android** | **À venir**, proposé sur abonnement |
| **Continuité** | **100 % cross-device Desktop ↔ Android** |
| **Projet** | Format portable `.dw` |
| **Philosophie** | Local-first, cloud non obligatoire pour le contenu créatif |
| **Studio** | Séquenceur, piano roll, arrangeur, mixeur, instruments, effets, automation |
| **Sorties** | Export audio, master et workflows de stems selon les capacités disponibles |
| **Technologies principales** | TypeScript, React, Vite, Web Audio API, AudioWorklet, PWA |
| **Code de production** | Privé — ce dépôt est la vitrine publique du produit |

## De l'idée au morceau, dans le même workspace

DAWWW-CORE est pensé pour garder la création dans un flux continu plutôt que de disperser les étapes entre plusieurs outils.

```text
Nouvelle idée / import
        ↓
Patterns & séquenceur
        ↓
Piano roll / édition musicale
        ↓
Arrangeur & timeline
        ↓
Instruments + effets
        ↓
Automation
        ↓
Mixeur & routage
        ↓
Master / stems / export audio
        ↓
Sauvegarde portable .dw
```

Vous pouvez commencer par un pattern, développer la structure dans l'arrangeur, reprendre les notes dans le piano roll, façonner les sons, automatiser des paramètres, construire le mix et préparer l'export sans quitter le studio.

## Ce que le studio rassemble

### Séquenceur

Construisez rapidement des patterns rythmiques et mélodiques, organisez les éléments musicaux et transformez une première boucle en matière exploitable pour l'arrangement.

### Piano roll

Éditez les notes avec une vue dédiée à l'écriture MIDI : placement, durée, structure et précision musicale restent accessibles sans sortir du projet.

### Arrangeur

Passez du pattern au morceau complet. La timeline sert de vue centrale pour structurer les sections, faire évoluer le projet et garder une lecture claire de l'ensemble.

### Mixeur

Travaillez niveaux, routage et traitements dans une surface dédiée au mix. Le mixeur s'intègre au reste du studio plutôt que d'être un outil isolé ajouté en fin de chaîne.

### Instruments intégrés

DAWWW-CORE embarque ses propres instruments et éditeurs afin de permettre la création sonore directement dans le projet, sans imposer une dépendance à une collection de plugins externes pour commencer à produire.

### Effets

Les traitements audio s'intègrent aux chaînes de mixage et aux workflows d'automation. Filtres, dynamique et autres traitements peuvent participer directement à la construction du son.

### Automation

Faites évoluer les paramètres dans le temps : mouvements de mix, effets, transitions ou changements de texture peuvent être écrits comme une partie du morceau plutôt que reproduits manuellement à chaque lecture.

### Export audio

Une session n'a de valeur que si elle peut sortir du studio. DAWWW-CORE prévoit les workflows d'export de master et de stems selon les capacités disponibles sur la plateforme.

## `.dw` : un projet qui vous appartient

Le format `.dw` est l'un des éléments centraux de DAWWW-CORE.

Un projet ne doit pas être condamné à rester dans un onglet, dépendre d'une base distante ou devenir inutilisable parce qu'un service de synchronisation n'est plus disponible. Le format `.dw` est conçu comme **le contenant portable du projet** : il permet de sauvegarder, déplacer, restaurer et transférer une session.

Cette portabilité remplit deux rôles importants :

- préserver une sortie locale pour vos créations ;
- fournir le contrat commun nécessaire au futur workflow Desktop ↔ Android.

Le cloud peut être utile pour des services autour du produit. Il n'est pas traité comme le propriétaire technique de votre musique.

## Local-first par conception

DAWWW-CORE part d'un principe volontairement différent d'un workflow cloud-first : **le contenu créatif existe d'abord sur l'appareil de l'utilisateur**.

Cela signifie que le cœur du produit est pensé autour du stockage local, de la portabilité et de la récupération des projets. Les services en ligne éventuels restent périphériques à cette logique et ne constituent pas la source primaire du projet musical.

Ce choix vise plusieurs choses très concrètes : garder le contrôle sur ses fichiers, limiter les dépendances inutiles au réseau, rendre les projets transportables et préserver un chemin de récupération compréhensible.

## Desktop aujourd'hui · Android ensuite

### Desktop Web — disponible maintenant

La version Desktop est la surface principale de DAWWW-CORE. Elle est pensée pour les grands écrans, les workflows denses et une utilisation prolongée de la timeline, du piano roll et du mixeur.

**Il n'y a plus de parcours de paiement sur la version Desktop.** L'objectif est que cette version puisse être utilisée comme le point d'entrée direct du studio web.

Elle repose sur les technologies modernes du navigateur et peut tirer parti d'une expérience PWA pour se rapprocher du confort d'une application installée tout en conservant le modèle de distribution web.

### Android — à venir sur abonnement

Android n'est pas présenté comme un produit séparé ou un simple lecteur mobile. La version à venir est conçue comme **le prolongement cross-device du même studio**.

Elle sera proposée **sur abonnement** et son contrat produit vise une compatibilité totale des projets avec Desktop : ouvrir le même `.dw`, poursuivre le travail sur Android et pouvoir revenir sur Desktop sans convertir le projet vers un second format.

```text
Desktop
   ↓
 projet .dw
   ↓
Android
   ↓
 même projet .dw
   ↓
Desktop
```

L'objectif est une continuité **100 % cross-device** au niveau du projet, tout en conservant l'approche local-first. Cross-device ne signifie donc pas « cloud obligatoire » : la portabilité du projet reste un mécanisme fondamental.

## Pourquoi un DAW web ?

Parce que le web donne accès à une plateforme de distribution immédiate, multi-environnement et continuellement améliorable, tout en disposant aujourd'hui de briques audio suffisamment avancées pour construire beaucoup plus qu'un simple lecteur ou séquenceur de démonstration.

DAWWW-CORE s'appuie notamment sur **Web Audio API** et **AudioWorklet** pour déplacer une partie du travail audio dans une architecture adaptée au traitement temps réel du navigateur.

L'enjeu n'est pas de copier une station desktop traditionnelle pixel par pixel. Il est de conserver ce qui compte dans un vrai workflow de production — contrôle, continuité, précision, portabilité — tout en profitant du modèle d'accès du web.

## Stack publique

La surface Desktop repose principalement sur :

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · stockage local navigateur

Le produit comporte également des couches dédiées aux tests, à l'observabilité, à la compatibilité de projet et à la distribution. Les détails d'architecture sensibles ou internes ne sont volontairement pas publiés dans ce dépôt.

## Fiabilité avant effet vitrine

Un DAW ne peut pas être jugé uniquement sur une capture d'écran. Une belle interface ne compense pas un transport instable, une restauration de projet fragile ou un export qui échoue.

Le développement de DAWWW-CORE donne donc une place importante aux chemins critiques : transport et lecture, stabilité des principaux modules, format `.dw`, restauration, export, routage audio et comportement des surfaces Desktop/Android concernées.

Cette vitrine publique ne transforme pas les validations internes en promesses marketing chiffrées. Elle présente le produit ; les détails de QA et les mécanismes de release restent dans les espaces de développement privés.

## Pour qui ?

DAWWW-CORE s'adresse particulièrement aux personnes qui veulent :

- commencer une session rapidement depuis un navigateur desktop ;
- disposer d'un workflow plus complet qu'un simple sketchpad musical ;
- garder leurs projets dans un format portable ;
- produire sans rendre une synchronisation cloud obligatoire ;
- passer de la composition au mix puis à l'export dans la même interface ;
- préparer un workflow où le même projet pourra continuer sur Android.

## État du projet

**DAWWW-CORE Desktop** est activement développé et constitue aujourd'hui la plateforme accessible du produit. La version Desktop est disponible **sans paiement**.

**DAWWW-CORE Android** est une plateforme **à venir**, proposée **sur abonnement**, avec pour objectif produit une continuité **100 % cross-device** avec Desktop.

Le produit continue d'évoluer : interfaces, fonctionnalités, compatibilités et limites peuvent changer. Les pages publiques officielles restent la référence pour les informations destinées aux utilisateurs.

## Ressources

- **Site** — https://dawww-core-local.com/fr
- **Studio Desktop** — https://dawww-core-local.com/app
- **Produit** — https://dawww-core-local.com/fr/studio
- **Guides** — https://dawww-core-local.com/fr/docs
- **Tutoriels** — https://dawww-core-local.com/fr/tutorials
- **FAQ** — https://dawww-core-local.com/fr/faq
- **Statut** — https://dawww-core-local.com/fr/status
- **Roadmap** — https://dawww-core-local.com/fr/roadmap
- **Changelog** — https://dawww-core-local.com/fr/changelog
- **Contact** — https://dawww-core-local.com/fr/contact

## À propos de ce dépôt

`Daw-core-desktop` est la **vitrine GitHub publique de DAWWW-CORE**.

Le dépôt documente le produit, sa vision, ses principales surfaces et son modèle de plateforme. **Le code source de production du moteur et de l'application reste privé** : ce dépôt ne constitue pas une distribution open source de DAWWW-CORE.

Les secrets, configurations de production, détails de déploiement, contrats fournisseurs, mécanismes internes de sécurité et autres éléments sensibles ne sont pas publiés ici.

---

<div align="center">

### Open the studio. Keep the project.

**DAWWW-CORE — music production on the web, with your project still under your control.**

[Ouvrir DAWWW-CORE](https://dawww-core-local.com/app)

</div>