<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="Emblème DAWWW-CORE" width="180" />

# DAWWW-CORE

### Une station de production musicale local-first construite pour le navigateur.

**Composez. Séquencez. Arrangez. Mixez. Automatisez. Exportez.**  
Sans installation lourde. Sans paiement sur Desktop. Sans rendre le cloud obligatoire pour posséder vos créations.

[![Desktop](https://img.shields.io/badge/Desktop-DISPONIBLE%20MAINTENANT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Prix](https://img.shields.io/badge/Desktop-SANS%20PAIEMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Android](https://img.shields.io/badge/Android-%C3%80%20VENIR%20%7C%20ABONNEMENT-111827?style=for-the-badge)](#desktop-aujourdhui--android-ensuite)
[![Cross-device](https://img.shields.io/badge/Projets-100%25%20CROSS--DEVICE-111827?style=for-the-badge)](#desktop-aujourdhui--android-ensuite)
[![Format projet](https://img.shields.io/badge/Projets-.dw-111827?style=for-the-badge)](#dw--votre-projet-est-un-fichier)

[**Ouvrir le studio**](https://dawww-core-local.com/app) · [Produit](https://dawww-core-local.com/fr/studio) · [Guides](https://dawww-core-local.com/fr/docs) · [Tutoriels](https://dawww-core-local.com/fr/tutorials) · [English](README.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="Lanceur de projets local DAWWW-CORE" width="100%" />
</p>

## Le navigateur peut être un vrai studio

DAWWW-CORE part d'une idée simple : **ouvrir un navigateur ne devrait pas signifier accepter un workflow musical réduit**.

Le produit vise une vraie expérience de station audionumérique desktop, organisée autour des étapes qui comptent réellement pour transformer une idée en morceau : gestion de projet, séquençage, édition de notes, arrangement, sound design, effets, automation, mixage et export.

La version Desktop est celle que l'on peut utiliser **aujourd'hui**, directement depuis le web et **sans paiement**. La session reste centrée sur un projet portable `.dw`, plutôt que sur un stockage cloud obligatoire.

La suite du modèle plateforme étend ce même projet à Android. La future version Android sera proposée sur abonnement et vise une compatibilité **100 % cross-device avec Desktop**.

> **Un projet. Un format. Deux plateformes. Pas deux workflows séparés.**

## En un coup d'œil

| | DAWWW-CORE |
| --- | --- |
| **Desktop Web** | Disponible maintenant — **sans paiement** |
| **Android** | **À venir** — sur abonnement |
| **Objectif cross-device** | **100 % de continuité projet Desktop ↔ Android** |
| **Format projet** | Sessions portables `.dw` |
| **Philosophie stockage** | Local-first ; le cloud n'est pas obligatoire pour le contenu créatif |
| **Workflow de production** | Séquenceur, piano roll, arrangeur, mixeur, instruments, effets, automation |
| **Sorties** | Export audio, master et workflows de stems selon les capacités disponibles |
| **Technologies principales** | TypeScript, React, Vite, Web Audio API, AudioWorklet, PWA |
| **Code de production** | Privé — ce dépôt est la vitrine publique du produit |

## À l'intérieur du studio

DAWWW-CORE n'est pas présenté ici comme une simple liste de fonctionnalités. L'interface actuelle expose déjà des surfaces dédiées pour écrire, éditer et mixer.

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034101.png" alt="Séquenceur DAWWW-CORE" width="100%" /><br />
      <sub><b>Séquenceur</b> — construire des patterns, organiser les pistes et passer rapidement d'une session vide à une idée structurée.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034231.png" alt="Édition détaillée du séquenceur DAWWW-CORE" width="100%" /><br />
      <sub><b>Édition détaillée des steps</b> — vélocité, probabilité, gate, ratchets, articulation et timing restent directement liés au pattern.</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034213.png" alt="Mixeur DAWWW-CORE" width="100%" /><br />
      <sub><b>Mixeur</b> — routage, niveaux, canaux et master restent dans le même environnement que la composition.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="Piano roll et éditeur d'instrument DAWWW-CORE" width="100%" /><br />
      <sub><b>Piano roll + éditeur d'instrument</b> — modifier les notes tout en gardant l'instrument et ses contrôles directement dans le contexte.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="Éditeur Electric Piano DAWWW-CORE" width="82%" /><br />
      <sub><b>Instruments dédiés</b> — sound shaping, enveloppes, contrôles de jeu et interaction MIDI sans quitter le projet.</sub>
    </td>
  </tr>
</table>

## De l'idée à l'export final

DAWWW-CORE est pensé pour garder la création dans un flux continu plutôt que de disperser chaque étape entre plusieurs outils.

```text
Créer / importer un projet
          ↓
Patterns & séquenceur
          ↓
Piano roll / édition des notes
          ↓
Arrangeur & timeline
          ↓
Instruments intégrés + effets
          ↓
Automation
          ↓
Mixeur & routage
          ↓
Master / stems / export audio
          ↓
Projet portable .dw
```

Commencez par un pattern. Affinez les notes dans le piano roll. Développez la structure dans l'arrangeur. Façonnez les sons, automatisez des paramètres, routez les canaux, construisez le mix et préparez l'export sans changer de modèle de projet en cours de route.

## Ce que le studio rassemble

### Séquenceur

Construisez des patterns rythmiques et mélodiques, organisez les pistes et travaillez avec des comportements musicaux détaillés par step plutôt qu'avec une simple grille on/off.

### Piano roll

Éditez les notes dans une surface dédiée à l'écriture musicale. Timing, durée, structure et précision restent reliés au même projet et au même contexte d'instrument.

### Arrangeur

Passez d'un pattern à une structure complète. L'arrangeur apporte la timeline nécessaire pour organiser sections, répétitions, transitions et progression du morceau.

### Mixeur

Travaillez niveaux, routage et traitements sans quitter le projet. Le mix fait partie du workflow, il n'est pas un écran isolé ajouté à la fin.

### Instruments intégrés

DAWWW-CORE propose des instruments et éditeurs dédiés afin qu'un nouveau projet puisse devenir immédiatement jouable sans imposer une collection de plugins externes pour commencer.

### Effets & automation

Les traitements et mouvements de paramètres utilisent le même modèle de production. Filtres, dynamique, transitions et textures évolutives peuvent être écrits dans le projet au lieu d'être reproduits manuellement à chaque lecture.

### Export

Une session n'a de valeur que si elle peut sortir du studio. DAWWW-CORE prend en charge le rendu audio avec des workflows orientés master et stems selon les capacités de la plateforme.

## `.dw` : votre projet est un fichier

Le format `.dw` est l'une des décisions produit centrales de DAWWW-CORE.

Un projet web ne devrait pas être prisonnier d'un onglet ni dépendre définitivement d'une base distante. `.dw` est conçu comme **le contenant portable d'une session DAWWW-CORE** : le sauvegarder, le déplacer, le restaurer et le transporter entre surfaces compatibles.

Cette portabilité sert deux objectifs :

- préserver une vraie sortie locale pour le travail créatif ;
- fournir le contrat commun nécessaire à la continuité Desktop ↔ Android.

Les services cloud peuvent être utiles autour du produit. Ils n'ont pas à devenir le propriétaire technique de la musique elle-même.

## Local-first par conception

DAWWW-CORE part d'un principe volontairement différent d'une station cloud-first : **le contenu créatif existe d'abord sur l'appareil de l'utilisateur**.

Le cœur du workflow est donc pensé autour du stockage local, de la portabilité et de la récupération des projets. Des services réseau peuvent exister autour du produit, mais ils ne constituent pas la source primaire de la session musicale.

Concrètement, l'objectif est simple : moins de dépendances réseau inutiles, des chemins de récupération compréhensibles, des projets transportables et davantage de contrôle direct sur le travail créé.

## Desktop aujourd'hui · Android ensuite

### Desktop Web — disponible maintenant, sans paiement

Desktop est aujourd'hui la surface principale de DAWWW-CORE. Elle est conçue pour les grands écrans, les contrôles denses et les sessions prolongées entre séquenceur, piano roll, arrangeur et mixeur.

**Il n'y a pas de parcours de paiement sur la version Desktop.** Le studio navigateur est le point d'entrée direct du produit.

[**Lancer DAWWW-CORE Desktop →**](https://dawww-core-local.com/app)

### Android — à venir sur abonnement

Android n'est pas conçu comme un produit séparé ni comme un simple lecteur compagnon. La future version est pensée comme **le prolongement mobile du même projet DAWWW-CORE**.

Elle sera proposée **sur abonnement** et construite autour d'une compatibilité `.dw` complète avec Desktop :

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

L'objectif produit est une continuité **100 % cross-device** tout en conservant l'approche local-first. Cross-device ne signifie pas cloud obligatoire ; le projet portable reste le contrat commun entre les plateformes.

## Pourquoi construire un DAW pour le web ?

Parce qu'un navigateur moderne est une plateforme applicative, pas seulement une surface de contenu.

DAWWW-CORE utilise **Web Audio API** et **AudioWorklet** pour le traitement audio temps réel, tandis que TypeScript, React et Vite construisent la couche applicative autour du moteur et de l'interface de production.

L'objectif n'est pas de reproduire pixel par pixel une station traditionnelle. Il est de préserver ce qui compte dans une production sérieuse — contrôle, continuité, précision, vitesse et portabilité — tout en utilisant le web pour l'accès immédiat et la distribution.

## Stack publique

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · stockage local navigateur

Le produit contient également des couches dédiées à la QA, à la compatibilité projet, à la récupération, à l'observabilité et à la distribution. Les détails sensibles restent privés.

## Fiabilité avant chiffres vitrine

Un DAW ne se juge pas uniquement sur des captures. Une belle interface ne compense pas une lecture instable, une restauration fragile ou un export peu fiable.

Le développement se concentre donc fortement sur les chemins critiques : transport, playback, persistance projet, portabilité `.dw`, restauration, routage, export et comportement plateforme.

Ce dépôt public présente le produit sans transformer les validations QA privées en promesses marketing gonflées.

## État du projet

**DAWWW-CORE Desktop** est activement développé et disponible maintenant **sans paiement**.

**DAWWW-CORE Android** est **à venir**, prévu comme produit **sur abonnement**, avec la continuité **100 % cross-device** avec Desktop comme objectif central.

Les interfaces, fonctionnalités et compatibilités peuvent évoluer avec le développement. Les pages publiques du produit restent la référence pour les informations destinées aux utilisateurs.

## Ressources

- **Site** — https://dawww-core-local.com/fr
- **Studio Desktop** — https://dawww-core-local.com/app
- **Présentation produit** — https://dawww-core-local.com/fr/studio
- **Guides** — https://dawww-core-local.com/fr/docs
- **Tutoriels** — https://dawww-core-local.com/fr/tutorials
- **FAQ** — https://dawww-core-local.com/fr/faq
- **Statut** — https://dawww-core-local.com/fr/status
- **Roadmap** — https://dawww-core-local.com/fr/roadmap
- **Changelog** — https://dawww-core-local.com/fr/changelog
- **Contact** — https://dawww-core-local.com/fr/contact

## À propos de ce dépôt

`Daw-core-desktop` est la **vitrine GitHub publique de DAWWW-CORE**.

L'application de production et le moteur audio restent privés. Ce dépôt sert à présenter le produit, son workflow, ses surfaces publiques et sa direction plateforme ; il ne constitue **pas** une distribution open source du code de production.

Les secrets, configurations de déploiement, contrats fournisseurs, mécanismes de sécurité et autres éléments internes sensibles sont volontairement conservés hors de ce dépôt.

---

<div align="center">

### Ouvrez le studio. Gardez le projet.

**DAWWW-CORE — une production musicale sérieuse sur le web, avec un projet qui reste sous votre contrôle.**

[**Ouvrir DAWWW-CORE Desktop**](https://dawww-core-local.com/app)

</div>