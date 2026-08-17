<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="Emblème DAWWW-CORE" width="170" />

# DAWWW-CORE

### Un seul DAW. Un seul projet. Desktop et Android.

DAWWW-CORE est une **station de production musicale local-first dans le navigateur**, pensée autour d’un projet complet qui peut passer de Desktop à Android sans changer de format, perdre ses devices ou basculer vers un workflow mobile réduit.

[![Desktop](https://img.shields.io/badge/Desktop-DISPONIBLE%20MAINTENANT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Accès Desktop](https://img.shields.io/badge/Desktop-SANS%20PAIEMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Cross-device](https://img.shields.io/badge/Desktop%20↔%20Android-100%25%20CROSS--DEVICE-111827?style=for-the-badge)](#un-seul-projet-entre-desktop-et-android)
[![Instruments](https://img.shields.io/badge/Instruments%20intégrés-51-111827?style=for-the-badge)](#instruments-et-synthèse)
[![Effets](https://img.shields.io/badge/Effets%20intégrés-16-111827?style=for-the-badge)](#effets)
[![Android](https://img.shields.io/badge/Android-À%20VENIR%20%7C%20ABONNEMENT-111827?style=for-the-badge)](#un-seul-projet-entre-desktop-et-android)

[**Ouvrir le studio Desktop**](https://dawww-core-local.com/app) · [Produit](https://dawww-core-local.com/fr/studio) · [Documentation](https://dawww-core-local.com/fr/docs) · [Statut](https://dawww-core-local.com/fr/status) · [English](README.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="Lanceur de projets Desktop DAWWW-CORE" width="100%" />
</p>

## Un seul projet entre Desktop et Android

Le cross-device n’est pas une fonction de synchronisation ajoutée autour de DAWWW-CORE. Il fait partie du modèle projet lui-même.

Le même projet `.dw` est prévu pour contenir l’état nécessaire à la réouverture de la session sur l’une ou l’autre plateforme : arrangement, notes et patterns, instruments, réglages d’effets, automation, routage et contenu sampler référencé. Desktop et Android utilisent **le même format de projet**, pas deux variantes partiellement compatibles.

L’échange est donc direct :

```text
Desktop  →  .dw  →  Android  →  .dw  →  Desktop
```

Aucune conversion. Aucun format Android réduit. Aucun mode compagnon ou viewer. Un projet créé sur une surface reste le même projet DAWWW-CORE sur l’autre.

La synchronisation cloud n’est pas nécessaire à cette compatibilité. Un `.dw` peut être déplacé indépendamment ; des services en ligne peuvent exister autour du workflow sans devenir l’autorité qui fait exister le projet.

| Plateforme | Disponibilité | Modèle d’accès | Support projet |
| --- | --- | --- | --- |
| **Desktop Web** | Disponible maintenant | **Sans paiement** | Projet DAWWW-CORE complet |
| **Android** | À venir | **Abonnement** | Même projet `.dw` complet |
| **Desktop ↔ Android** | Continuité native du projet | — | **Aucune conversion / aucun format réduit** |

## Modules de production

DAWWW-CORE est organisé autour de modules de production séparés qui travaillent tous sur le même projet.

| Module | Ce qu’il apporte |
| --- | --- |
| **Transport** | Position de lecture, tempo et timing projet partagés |
| **Séquenceur** | Écriture par patterns et programmation par steps |
| **Éditeur de step** | Vélocité, probabilité, gate, ratchets, articulation et décalage timing |
| **Piano roll** | Édition MIDI au niveau des notes pour le contenu mélodique |
| **Arrangeur** | Structure du morceau et organisation sur timeline |
| **Mixeur** | Niveaux, routage, traitements et contrôle master |
| **Automation** | Évolution des paramètres d’instruments, d’effets et de mix dans le temps |
| **Devices instruments** | Interfaces dédiées aux moteurs sonores intégrés |
| **Effets** | Traitements intégrés directement au workflow projet/mixeur |
| **I/O projet** | Sauvegarde/restauration locale et import/export `.dw` |
| **Export audio** | Workflows orientés master et stems |

L’objectif n’est pas de tout enfermer dans un éditeur unique. Patterns, édition de notes, arrangement, sound design et mixage restent des surfaces de travail distinctes tout en partageant le même état projet.

## Instruments et synthèse

DAWWW-CORE intègre actuellement **51 instruments** : 50 moteurs de synthèse dédiés plus un sampler.

Plutôt que d’utiliser un synthé générique décliné en dizaines de presets renommés, les moteurs sont regroupés par rôle musical et plusieurs familles disposent de leurs propres éditeurs.

| Famille | Moteurs intégrés |
| --- | --- |
| **Orchestre · 12** | Violon, alto, violoncelle, contrebasse, trompette, cor, trombone, tuba, flûte, hautbois, clarinette, basson |
| **Drums · 12** | Kick, snare, clap, hi-hat fermé/ouvert, tom bas/mid/aigu, cowbell, rimshot, claves, maracas |
| **Bass · 3** | Sub, acid, Reese |
| **Electronic · 7** | Mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys, noise/transition FX |
| **Pads · 5** | Warm, glass, choir, evolving, ambient |
| **Keys & bells · 7** | Piano acoustique, piano électrique, clavinet, orgue tonewheel, celesta, music box, tubular bell |
| **Guitares · 4** | Nylon, steel-string, clean electric, driven electric |
| **Sampler · 1** | Workflow d’instrument basé sur des échantillons |

Les panels dédiés permettent à chaque instrument d’exposer des contrôles cohérents avec son modèle sonore au lieu de forcer tous les moteurs dans la même interface générique. L’Electric Piano possède par exemple ses propres réglages de tone, tremolo et enveloppe, tandis que les percussions exposent des paramètres plus adaptés au travail des transitoires.

## Effets

Le set actuel comprend **16 effets intégrés** :

`EQ paramétrique 8 bandes` · `Compressor` · `Convolution Reverb` · `Delay synchronisé au tempo` · `Chorus` · `Flanger` · `Phaser` · `Distortion` · `Filter` · `Gate` · `Limiter` · `Saturator` · `Tremolo` · `Vibrato` · `Bitcrusher` · `Utility`

Les effets font partie du projet, pas d’une étape de post-traitement extérieure. Leurs réglages peuvent rester liés à la session, participer au routage et à l’automation, puis voyager avec le même `.dw` entre les surfaces DAWWW-CORE compatibles.

## Surfaces actuelles du Studio

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034101.png" alt="Séquenceur DAWWW-CORE" width="100%" /><br />
      <sub><b>Séquenceur</b> — pistes de pattern, accès aux instruments et programmation par steps.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034231.png" alt="Éditeur de step DAWWW-CORE" width="100%" /><br />
      <sub><b>Éditeur de step</b> — vélocité, probabilité, gate, ratchets, articulation et timing.</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034213.png" alt="Mixeur DAWWW-CORE" width="100%" /><br />
      <sub><b>Mixeur</b> — niveaux, routage, traitements et étage master.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="Piano roll et éditeur d'instrument DAWWW-CORE" width="100%" /><br />
      <sub><b>Piano roll + instrument</b> — édition des notes et contrôles sonores dans le même contexte projet.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="Éditeur Electric Piano DAWWW-CORE" width="82%" /><br />
      <sub><b>Éditeur d’instrument dédié</b> — contrôles adaptés à l’instrument plutôt qu’un panneau universel.</sub>
    </td>
  </tr>
</table>

## Local-first par conception

Sur Desktop, le moteur audio s’exécute directement sur la machine de l’utilisateur grâce aux capacités audio modernes du navigateur. La lecture normale ne dépend pas d’un service distant de rendu audio.

Les projets restent locaux pendant le travail et peuvent être exportés en `.dw`. DAWWW-CORE dispose ainsi de deux niveaux de persistance :

- **stockage de travail local** pour les sessions courantes ;
- **projet portable `.dw`** pour archiver, déplacer ou rouvrir la session sur une autre surface DAWWW-CORE.

L’application Desktop est web et orientée PWA : elle reste accessible directement depuis le navigateur tout en pouvant se rapprocher du comportement d’une application installée sur les systèmes compatibles.

## Ce qui est testé

Le code de production utilise des validations automatisées et des scénarios ciblés sur les éléments les plus importants pour un DAW.

La couverture actuelle comprend notamment :

- sauvegarde, restauration, import et portabilité des projets `.dw` ;
- compatibilité et aller-retour projet Desktop ↔ Android ;
- transport et synchronisation de lecture ;
- séquenceur, piano roll, arrangeur et mixeur ;
- routage, sends et chemins de traitement ;
- instruments, effets et automation ;
- export master/stems ;
- sessions longues et scénarios orientés stress ;
- contrôles E2E et performance navigateur.

Le dépôt public ne détaille volontairement pas les noms de gates, scripts internes ou mécanismes de release. L’information utile publiquement est la couverture : **portabilité projet, continuité audio, modules, effets, routage et export sont traités comme des comportements vérifiables du produit.**

## Taille des sessions et limites actuelles

DAWWW-CORE n’impose pas un plafond marketing arbitraire du type « X pistes » ou « Y minutes », car le moteur Desktop tourne localement.

La limite réelle d’un projet dépend principalement de la machine et du contenu actif :

- beaucoup de voix de synthèse simultanées augmentent la charge CPU ;
- de gros ensembles de samples augmentent l’usage mémoire et stockage local ;
- des chaînes d’effets longues et un routage complexe augmentent le coût temps réel ;
- les exports de nombreux stems ou de longues durées demandent davantage de temps de rendu et de mémoire temporaire ;
- la capacité de stockage locale varie selon le navigateur, le système et l’appareil.

Un projet léger de 30 pistes peut donc être plus simple à faire tourner qu’un projet plus petit utilisant beaucoup de polyphonie, plusieurs reverbs et des traitements lourds. **La complexité de la session compte davantage qu’un simple nombre de pistes.**

Pour les projets importants, un export `.dw` régulier est recommandé, particulièrement avec de grosses bibliothèques de samples, car le stockage local du navigateur reste soumis aux règles de l’environnement hôte.

### Export et différences entre navigateurs

**WAV** constitue le chemin d’export de base. La disponibilité **MP3 dépend des capacités de la plateforme/runtime** et n’est pas garantie par un encodeur universel embarqué.

Latence audio, quota de stockage, support codec et complexité maximale pratique peuvent également varier entre navigateurs et systèmes d’exploitation. DAWWW-CORE est conçu pour fonctionner dans le navigateur, mais le comportement matériel ne peut pas être identique dans tous les environnements.

## Desktop maintenant, Android ensuite

**Desktop Web** est la surface publique actuelle de DAWWW-CORE et ne comporte **aucun parcours de paiement**.

**Android** arrive ensuite comme **version sur abonnement**. Il ne s’agit pas d’un produit léger séparé : la version Android utilise le même modèle projet complet, le même état instruments/effets et la même compatibilité `.dw` décrits plus haut.

La différence est donc commerciale et liée à la plateforme, pas au contenu créatif :

> **Desktop et Android sont deux endroits où travailler sur le même projet DAWWW-CORE.**

## Stack publique

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · stockage local navigateur · `Capacitor` pour Android

## Périmètre actuel

Le produit actuel ne dépend pas de :

- synchronisation cloud obligatoire des projets ;
- collaboration temps réel ;
- iOS ;
- marketplace de plugins tiers.

Le cœur reste le DAW lui-même : modules, instruments, effets, automation, mixage, export, propriété locale du projet et continuité complète Desktop ↔ Android.

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

`Daw-core-desktop` est la vitrine publique de DAWWW-CORE. Le code source de production reste privé.

Ce dépôt présente les usages, les outils disponibles, le modèle cross-device, l’approche de validation et les limites pratiques actuelles sans exposer l’architecture interne, les détails de déploiement ou les éléments sensibles de sécurité.

---

<div align="center">

### Un projet. Un workflow DAW complet. Desktop et Android.

[**Ouvrir DAWWW-CORE Desktop**](https://dawww-core-local.com/app)

</div>
