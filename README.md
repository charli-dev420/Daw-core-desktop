<div align="center">

# DAWWW-CORE

### Studio de production musicale web, local-first

Composez, séquencez, arrangez, mixez et exportez directement depuis votre navigateur desktop — sans imposer le cloud au cœur de votre workflow créatif.

[![Desktop Web](https://img.shields.io/badge/platform-desktop%20web-111827?style=flat-square)](https://dawww-core.com/studio)
[![Local-first](https://img.shields.io/badge/design-local--first-111827?style=flat-square)](https://dawww-core.com)
[![Project format](https://img.shields.io/badge/projects-.dw-111827?style=flat-square)](https://dawww-core.com/docs)
[![Source](https://img.shields.io/badge/source-private-111827?style=flat-square)](#à-propos-de-ce-dépôt)

[Ouvrir DAWWW-CORE](https://dawww-core.com/studio) · [Guides](https://dawww-core.com/docs) · [Statut](https://dawww-core.com/status) · [English](README.en.md)

</div>

---

## DAWWW-CORE, c'est quoi ?

DAWWW-CORE est une station audionumérique pensée pour le navigateur desktop. Le projet cherche à rapprocher la rapidité d'accès d'une application web d'un workflow de production musicale structuré : écrire une idée, construire des patterns, organiser une timeline, travailler le son, mixer puis exporter sans installation lourde.

Le produit suit une approche **local-first** : les projets et contenus créatifs restent d'abord sous le contrôle de l'utilisateur. Le compte et les services en ligne servent de couche d'accès ; ils ne constituent pas la source primaire de vos créations.

## Le studio

| Surface | Ce qu'elle apporte |
| --- | --- |
| **Séquenceur** | Construction de patterns et organisation rythmique/mélodique. |
| **Piano roll** | Édition des notes et programmation MIDI. |
| **Arrangeur** | Construction du morceau sur une timeline. |
| **Mixeur** | Routage, niveaux, traitements et organisation du mix. |
| **Instruments intégrés** | Création sonore directement dans le studio. |
| **Effets** | Chaînes de traitement intégrées au workflow de mixage. |
| **Automation** | Évolution temporelle des paramètres du projet. |
| **Export audio** | Rendu du morceau et workflows d'export selon les capacités de la plateforme. |
| **Projet `.dw`** | Format portable pour sauvegarder, déplacer et restaurer un projet. |

## Un workflow local-first

```text
Créer / importer
      ↓
Séquenceur + Piano roll
      ↓
Arrangeur
      ↓
Instruments + Effets + Automation
      ↓
Mixeur
      ↓
Export audio / sauvegarde .dw
```

Le format `.dw` joue un rôle central : il fournit une sortie portable pour conserver et déplacer un projet sans dépendre d'une synchronisation cloud obligatoire.

## Pensé pour le desktop web

DAWWW-CORE s'appuie sur les capacités modernes du navigateur pour proposer une expérience de création audio riche tout en gardant un accès immédiat depuis le web.

Principes de conception :

- **local-first** pour les projets et contenus créatifs ;
- **portabilité** grâce au format de projet `.dw` ;
- **workflow complet** du pattern à l'export ;
- **interface desktop** conçue pour une utilisation musicale dense ;
- **audio web moderne** avec Web Audio et AudioWorklet ;
- **progressive web app** pour rapprocher l'expérience web d'une application installée ;
- **compatibilité projet** pensée entre les différentes surfaces DAWWW-CORE lorsque celles-ci partagent le même contrat de projet.

## Stack produit

La surface desktop est construite principalement autour de :

`TypeScript` · `React` · `Vite` · `Web Audio API` · `AudioWorklet` · `PWA` · stockage local navigateur

L'application utilise également des services spécialisés pour les fonctions qui ne relèvent pas du contenu créatif local, notamment l'accès au compte, la facturation, l'observabilité et la distribution web.

## Confidentialité par conception

Le principe produit est simple : **un projet musical n'a pas besoin d'être stocké dans un cloud pour exister**.

DAWWW-CORE privilégie donc le stockage local du contenu créatif et la possibilité d'exporter un projet portable. Les services de compte ou de paiement restent séparés du contenu musical utilisé comme source primaire.

## État du projet

DAWWW-CORE est un produit activement développé. La priorité est donnée à la fiabilité du moteur audio, à la portabilité des projets, au workflow desktop et à la validation des chemins critiques avant les changements purement visuels.

Les fonctionnalités, limites de plateforme et conditions d'accès peuvent évoluer pendant le développement. Les pages publiques du produit restent la référence pour l'état visible par les utilisateurs.

## Liens

- **Site** — https://dawww-core.com
- **Studio** — https://dawww-core.com/studio
- **Guides** — https://dawww-core.com/docs
- **Tutoriels** — https://dawww-core.com/tutorials
- **FAQ** — https://dawww-core.com/faq
- **Statut** — https://dawww-core.com/status
- **Roadmap** — https://dawww-core.com/roadmap
- **Changelog** — https://dawww-core.com/changelog
- **Contact** — https://dawww-core.com/contact

## À propos de ce dépôt

Ce dépôt est la **présentation publique de DAWWW-CORE Desktop**.

Il sert à présenter le produit, son positionnement, ses capacités et ses liens publics. **Le code source de production n'est pas distribué dans ce dépôt** et le contenu présent ici ne doit pas être interprété comme une publication open source du moteur ou de l'application.

Les détails d'architecture interne, secrets, configurations de déploiement, contrats fournisseurs et éléments de sécurité restent volontairement hors de cette vitrine publique.

---

<div align="center">

**DAWWW-CORE** — faire de la musique dans le navigateur sans céder le contrôle de ses projets.

</div>
