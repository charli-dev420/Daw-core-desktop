<div align="center">

<img src="asset/logos/dawww_core_favicon_symbol_with_bg_edit_213223361277514.png" alt="Emblème DAWWW-CORE" width="170" />

# DAWWW-CORE

### DAW natif navigateur · projets local-first · format portable `.dw`

DAWWW-CORE est une station audionumérique orientée Desktop construite sur **Web Audio API + AudioWorklet**, avec une couche applicative React/TypeScript, un stockage projet local au navigateur et un contrat de projet portable partagé avec la future application Android.

[![Desktop](https://img.shields.io/badge/Desktop-DISPONIBLE%20MAINTENANT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Accès Desktop](https://img.shields.io/badge/Desktop-SANS%20PAIEMENT-111827?style=for-the-badge)](https://dawww-core-local.com/app)
[![Instruments](https://img.shields.io/badge/Instruments%20intégrés-51-111827?style=for-the-badge)](#outils-de-production)
[![Effets](https://img.shields.io/badge/Effets%20intégrés-16-111827?style=for-the-badge)](#outils-de-production)
[![Android](https://img.shields.io/badge/Android-À%20VENIR%20%7C%20ABONNEMENT-111827?style=for-the-badge)](#modèle-cross-device)

[**Ouvrir le studio Desktop**](https://dawww-core-local.com/app) · [Produit](https://dawww-core-local.com/fr/studio) · [Documentation](https://dawww-core-local.com/fr/docs) · [Statut](https://dawww-core-local.com/fr/status) · [English](README.md)

</div>

---

<p align="center">
  <img src="asset/capture/Screenshot_20260817-033954.png" alt="Surface projets Desktop DAWWW-CORE" width="100%" />
</p>

## Vue technique

DAWWW-CORE est conçu comme une **station local-first**, pas comme un séquenceur cloud. La couche compte, le site public et les éventuels services en ligne sont séparés du runtime créatif. La session de travail autoritative reste locale et `.dw` constitue la représentation portable du projet utilisée pour l'export/import, la récupération et la compatibilité cross-device.

| Couche | Implémentation actuelle | Rôle |
| --- | --- | --- |
| **Interface applicative** | TypeScript, React, Vite | Workspace Desktop, vues projet, éditeurs et routage applicatif |
| **Runtime audio** | Web Audio API | Graphe audio, instruments, mixeur, effets et lecture |
| **Timing / DSP workers** | AudioWorklet | Traitements sensibles au timing et tâches audio hors boucle de rendu React |
| **Transport / synchronisation** | Transport partagé + modules de sync | Position de lecture, timing séquenceur/arrangeur et état runtime partagé |
| **Runtime projet** | Services serializer / restorer | Conversion entre état vivant de l'application et représentation persistante |
| **Persistance locale** | Base/stockage local navigateur | Stockage de travail principal des projets et états créatifs |
| **Projet portable** | Pipeline de package `.dw` | Export/import, récupération et transfert indépendant de la plateforme |
| **Distribution Desktop** | Application web + build orienté PWA | Accès direct navigateur sans imposer un installateur traditionnel |
| **Distribution Android** | Build Android Capacitor | Future application sur abonnement utilisant le même contrat projet |
| **Validation** | Vitest, Playwright, scripts de certification/gates | Tests unitaires, intégration, portabilité, playback, modules, stress et release |

La frontière architecturale est volontaire : **React pilote l'application ; Web Audio pilote le graphe audio**. Le rendu UI n'est pas utilisé comme scheduler audio. Les éléments sensibles au timing restent dans la couche audio/runtime, notamment via AudioWorklet et un modèle de transport partagé.

## Runtime audio

Le moteur audio s'exécute entièrement sur la machine de l'utilisateur. Aucun service distant de rendu audio n'est nécessaire pour la lecture Desktop normale.

À l'exécution, DAWWW-CORE construit un graphe Web Audio à partir de l'état du projet : les instruments alimentent les pistes, les pistes passent par le routage et les traitements, puis le mixeur alimente la chaîne master. Le transport et les modules de synchronisation fournissent la référence temporelle commune au séquenceur, à l'arrangeur et à l'état de lecture.

AudioWorklet est utilisé lorsque le scheduling du thread principal du navigateur n'est pas suffisant. Le code contient notamment des chemins worklet dédiés à l'horloge/timing ainsi qu'à certains traitements et analyseurs. Cela réduit la dépendance du timing audio au rendu React ou à l'activité DOM, sans supprimer les limites matérielles : la capacité temps réel finale dépend toujours du navigateur, du CPU, de la mémoire et du périphérique audio.

Le rendu/export est traité comme un chemin technique distinct de la lecture interactive. Le code contient des services dédiés à l'export/rendu ainsi que des tests de parité permettant de vérifier le résultat indépendamment de l'interface.

## Outils de production

La version Desktop expose les principales surfaces d'un DAW sous forme de modules séparés mais partageant le même runtime projet.

| Surface | Capacités disponibles | Validation présente dans le code |
| --- | --- | --- |
| **Transport** | État play/stop, temps projet, timing partagé | Fixtures playback et profils de certification transport |
| **Séquenceur** | Pistes de pattern et programmation par steps | Fixture module + fixture stress |
| **Éditeur de step** | Vélocité, chance/probabilité, gate, ratchet, articulation, décalage timing | Couvert par tests séquenceur/runtime |
| **Piano roll** | Édition MIDI au niveau des notes | Fixture module + fixture stress |
| **Arrangeur** | Timeline et structure du morceau | Fixture module + fixture stress |
| **Mixeur** | Canaux, niveaux, routage, sends/traitements, master | Tests unitaires + scénarios routage/PDC/sends |
| **Automation** | Automation de paramètres et chemins live effets | Scénario dédié automation/effects |
| **I/O projet** | Sauvegarde locale, restauration, import/export `.dw` | Suite de preuve `.dw` + tests serializer/restorer |
| **Export audio** | Master et stems ; WAV de base, MP3 lorsque la capability est disponible | Scénarios export, export long et budgets de performance |

### 51 instruments intégrés

Le registre interne contient actuellement **50 moteurs de synthèse dédiés plus le sampler**. Ils sont organisés par rôle musical, pas simplement comme un synthé générique décliné en presets :

- **12 moteurs orchestraux :** violon, alto, violoncelle, contrebasse, trompette, cor, trombone, tuba, flûte, hautbois, clarinette et basson ;
- **12 moteurs drums :** kick, snare, hand clap, hi-hat fermé/ouvert, tom bas/mid/aigu, cowbell, rimshot, claves et maracas ;
- **3 basses :** sub, acid et Reese ;
- **7 électroniques :** mono lead, poly synth, pluck, arpeggio synth, chiptune, FM keys et noise/transition FX ;
- **5 pads :** warm, glass, choir, evolving et ambient ;
- **7 keys/bells :** piano acoustique, piano électrique, clavinet, orgue tonewheel, celesta, music box et tubular bell ;
- **4 guitares :** nylon, steel-string, clean electric et driven electric ;
- **1 sampler** pour les instruments à base d'échantillons.

Plusieurs familles disposent d'éditeurs dédiés au lieu d'un panneau universel. L'interface peut donc exposer des contrôles liés au modèle de synthèse : par exemple l'Electric Piano possède ses propres contrôles de tone shaping, tremolo et enveloppe, tandis que les percussions utilisent des paramètres adaptés aux transitoires.

### 16 effets intégrés

Le registre de traitements intégré contient actuellement :

`EQ paramétrique 8 bandes` · `Compressor` · `Convolution Reverb` · `Delay synchronisé au tempo` · `Chorus` · `Flanger` · `Phaser` · `Distortion` · `Filter` · `Gate` · `Limiter` · `Saturator` · `Tremolo` · `Vibrato` · `Bitcrusher` · `Utility`

Ces processeurs font partie de l'architecture mixeur/automation et ne constituent pas une application de post-traitement séparée.

## Surfaces actuelles du Studio

<table>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034101.png" alt="Séquenceur DAWWW-CORE" width="100%" /><br />
      <sub><b>Séquenceur</b> — pistes, patterns et routage instrument dans le runtime projet partagé.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034231.png" alt="Propriétés d'un step DAWWW-CORE" width="100%" /><br />
      <sub><b>Propriétés par step</b> — vélocité, chance, gate, ratchets, articulation et décalage timing.</sub>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034213.png" alt="Mixeur DAWWW-CORE" width="100%" /><br />
      <sub><b>Mixeur</b> — routage des canaux, inserts/traitements, niveaux et étage master.</sub>
    </td>
    <td width="50%" valign="top">
      <img src="asset/capture/Screenshot_20260817-034141.png" alt="Piano roll et instrument DAWWW-CORE" width="100%" /><br />
      <sub><b>Piano roll + device</b> — les notes et l'instrument restent connectés au même projet vivant.</sub>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" valign="top">
      <img src="asset/capture/Screenshot_20260817-034152.png" alt="Éditeur Electric Piano DAWWW-CORE" width="82%" /><br />
      <sub><b>Éditeur d'instrument dédié</b> — contrôles propres au moteur de synthèse au lieu d'un dump générique de paramètres.</sub>
    </td>
  </tr>
</table>

## Modèle projet `.dw`

`.dw` constitue la frontière de compatibilité de DAWWW-CORE.

Le runtime projet vivant est sérialisé dans un package portable via la couche `DWFormat` / `DWPackagePipeline`. Le chemin inverse reconstruit l'état runtime depuis le package. Ce pipeline est volontairement séparé de la couche compte afin qu'une création ne soit pas définie par un enregistrement serveur associé à un utilisateur.

La suite de preuve `.dw` couvre notamment la validation du format, les invariants de portabilité, le fuzzing, la vérification d'export, la sérialisation/restauration runtime, le rendu moteur, la parité audio, le **rendu cross-device** et les contrôles de **production parity**.

C'est cette distinction qui définit la stratégie Android : cross-device ne signifie pas « synchroniser la même ligne de base de données sur deux clients ». Cela signifie **deux runtimes qui implémentent le même contrat projet**.

## Modèle cross-device

L'architecture cible est :

```text
Runtime Desktop Web
        │
        ├── ProjectRuntimeSerializer
        │
        ▼
     projet .dw
        │
        ├── ProjectRuntimeRestorer
        │
        ▼
Runtime Android / Capacitor
```

Desktop et Android doivent partager le schéma projet, les règles de sérialisation runtime et les mêmes sémantiques projet/audio. C'est pour cette raison que le code contient déjà des tests de rendu `.dw` cross-device et de production parity avant la sortie publique d'Android.

**« 100 % cross-device » désigne un objectif de compatibilité projet, pas une affirmation selon laquelle l'APK Android actuel est déjà certifié production sur tous les appareils.** La documentation de release conservée sépare explicitement les preuves format/runtime de la validation native réelle.

Le modèle public est donc :

| Surface | État | Accès | Contrat projet |
| --- | --- | --- | --- |
| **Desktop Web** | Disponible maintenant | Sans paiement | Surface de référence actuelle `.dw` |
| **Android** | À venir | Abonnement | Même contrat `.dw` / objectif 100 % compatible |
| **Sync cloud projet** | Non requis | — | N'est pas l'autorité d'existence du projet |

## Persistance, récupération et stockage local

Les projets Desktop sont principalement persistés dans l'infrastructure de stockage/base locale du navigateur. C'est ce qui permet le comportement local-first, mais cela impose des contraintes différentes d'un DAW entièrement hébergé côté serveur.

La stack projet contient des mécanismes explicites de sauvegarde et récupération : sérialisation/restauration, état de confiance de sauvegarde, recovery flows et chemin de réparation de la base locale. `.dw` constitue la frontière externe de récupération : une fois exporté, un projet peut exister indépendamment de la base du navigateur.

Un navigateur ne fournit **pas de quota de stockage universel et fixe**. L'espace disponible et les règles d'éviction dépendent du navigateur, du profil, de la plateforme et de l'appareil. DAWWW-CORE peut raisonner sur l'état du stockage local, mais ne peut pas garantir le même nombre de gigaoctets sur toutes les machines. Les bibliothèques d'échantillons volumineuses et de nombreux projets locaux restent donc bornés par la politique du navigateur.

Pour cette raison, l'export `.dw` n'est pas seulement un mécanisme de partage : il sert aussi de sortie durable de la persistance locale du navigateur.

## Stratégie de validation

Le dépôt de production utilise plusieurs niveaux de validation plutôt qu'un score global unique.

### Tests unitaires et intégration

**Vitest** couvre le moteur audio, le stockage, le format projet, les instruments/effets, la sérialisation, la restauration et les autres composants runtime.

La commande dédiée `test:dw:proof` agrège les tests critiques de portabilité. Le dernier comptage documenté est de **459 tests** et inclut notamment :

- `DWPackagePipeline` ;
- `DWPortabilityInvariants` ;
- `DWFormat` et ses fuzz tests ;
- `DWExportVerification` ;
- `DWCrossDeviceRender` ;
- `DWProductionParity` ;
- `ProjectRuntimeSerializer` / `ProjectRuntimeRestorer` ;
- `EngineRenderService` ;
- `AudioParity.integration` ;
- playback fixture builders et production synth gates.

### Certification modules Desktop

Le dépôt contient des profils explicites pour :

- le séquenceur, l'arrangeur, le piano roll et le mixeur avec des **fixtures module de 1 minute** ;
- des **fixtures stress de 1 minute** dédiées à ces modules ;
- le transport et l'état partagé ;
- des profils de stabilité **1 heure continuous-work**, **1 heure stress** et **1 heure alternating-sync** ;
- un complete gate Desktop et un release-candidate gate scoped.

### E2E et performance

**Playwright** est utilisé pour les scénarios E2E/performance navigateur. Le dépôt contient également un système de rapport de performances, un P5 regression gate et des tests spécifiques de budget export/stems.

### Dernière preuve documentée conservée

Le dernier gel de release documenté conservé dans le dépôt privé date du **18 juillet 2026**. À cette date :

- les 9 composants Desktop suivis étaient verts via preuves composées ;
- le `complete-gate` Desktop visible indiquait **12/12 passés**, `findings=0` et `advisoryFindings=0` ;
- un long gate Desktop avait atteint **55 minutes de lecture** ;
- la preuve export/import `.dw` était conservée ;
- le build web Android et les preflights concernés disposaient de preuves, mais **APK / appareil physique / rendu natif / sortie haut-parleur n'avaient pas été revalidés dans ce gel**.

L'application et l'UI ont ensuite reçu des modifications. Ces chiffres doivent donc être lus comme **preuves techniques conservées**, pas comme certification fraîche du HEAD actuel. Une nouvelle exécution du release gate est nécessaire avant de présenter le build courant comme recertifié.

## Enveloppe de session et limites actuelles

DAWWW-CORE ne publie actuellement **aucun maximum dur certifié** pour le nombre de pistes, de notes, la durée du projet, les voix simultanées ou la taille du fichier projet. Inventer de telles limites serait trompeur puisque le runtime Desktop s'exécute sur la machine de l'utilisateur.

La limite pratique d'une session dépend actuellement de plusieurs budgets :

- **CPU / budget audio temps réel** — davantage de voix synthétiques, effets et routages simultanés augmentent la charge Web Audio ;
- **mémoire** — audio décodé, samples, buffers de rendu et état projet occupent la mémoire du processus navigateur ;
- **quota de stockage navigateur** — projets locaux et assets importés utilisent un espace géré par le navigateur/la plateforme ;
- **charge d'export** — les masters longs ou un grand nombre de stems demandent davantage de temps de rendu et de mémoire temporaire ;
- **implémentation navigateur / périphérique audio** — latence et capacité temps réel stable ne sont pas identiques selon OS, navigateur et interface audio.

Les profils module/stress de 1 minute et stabilité de 1 heure constituent donc des **enveloppes de validation**, pas des garanties de session infinie. La preuve de lecture longue de 55 minutes montre un chemin Desktop prolongé, mais ne signifie pas qu'un projet arbitrairement lourd fonctionnera indéfiniment sur n'importe quelle machine.

Pour les sessions très chargées en samples, polyphonie ou effets, la communication publique doit rester prudente : la complexité dépend du matériel réel et les projets importants doivent être exportés régulièrement en `.dw`.

### Limites d'export

WAV constitue le chemin d'export audio de base. **MP3 est capability-gated** : sa disponibilité dépend de la plateforme/runtime et le produit ne s'appuie pas sur un encodeur runtime LAME/Shine/FFmpeg/libmp3lame embarqué comme fallback universel.

### Compatibilité navigateurs

Le code est natif navigateur, mais les preuves QA conservées ne certifient pas tous les couples navigateur/OS comme équivalents. AudioWorklet, quota de stockage, support codec/export et latence matérielle peuvent varier. Une matrice publique de compatibilité ne devrait mentionner que les environnements explicitement rejoués et vérifiés.

### État Android

Le chemin Android ainsi que les outils de build/audit existent déjà, mais Android reste une **surface produit à venir**. La parité `.dw` et runtime peut être testée avant la sortie ; la validation sur appareils réels doit rester un sujet distinct.

## Scope volontaire actuel

Le produit actuel n'est pas organisé autour de :

- synchronisation cloud obligatoire des projets ;
- collaboration temps réel ;
- iOS ;
- marketplace de plugins tiers.

Ces fonctions sont hors du scope actif actuel. L'effort d'ingénierie reste centré sur le runtime local, le moteur audio, les surfaces principales de production, la portabilité, la récupération et la compatibilité projet Desktop ↔ Android.

## Stack publique

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · `Capacitor` · stockage local navigateur · `Vitest` · `Playwright`

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

`Daw-core-desktop` est la présentation publique technique et produit de DAWWW-CORE. L'application de production et le moteur audio sont développés dans un dépôt privé.

Ce dépôt expose volontairement l'architecture produit, les surfaces disponibles, le modèle de validation, la stratégie plateforme et les limites connues sans publier les secrets, la configuration de déploiement, les artifacts QA privés ni les détails sensibles de sécurité.

---

<div align="center">

**DAWWW-CORE Desktop — disponible maintenant, sans paiement.**

[**Ouvrir le Studio Desktop**](https://dawww-core-local.com/app)

</div>
