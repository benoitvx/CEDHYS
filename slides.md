---
title: "L'IA dans l'État"
subtitle: "Rendre les données publiques AI-ready & vibe coding"
author: "Benoit Vinceneux"
role: "EIG & CPO Données & MCP @ Services du Premier Ministre"
organization: "Direction interministérielle du numérique"
date: "26 Mars 2026"
avatar: "./images/benoitvinceneux.png"
---

# Contexte

## Qui suis-je

> Part builder, part hacker, part dealmaker

- DINUM (depuis Jan. 2026) — IA + Data + MCP
- Présidence de la République (2024 - 2025) — Plateforme d'intelligence décisionnelle
- Entrepreneur d'Intérêt Général (depuis 2024) — 35 recrutements dans toute l'administration
- NotreSanté (2017 - 2020) — Fondateur startup santé B2C
- Resopharma (2016 - 2018) — Déploiement de services en pharmacie (ex. réservation de produits)
- Laboratoires Pierre Fabre (2011 - 2017) — Espace Pro B2B + refonte des sites de marques
- Agences Web (2007 - 2013) — Libération, Panasonic, Novotel, The Kooples, etc.

## Le département IA dans l'État

Un département de la DINUM **entièrement consacré à l'IA** depuis 2025.

**3 missions :**

1. **Piloter la stratégie IA** pour le secteur public, en lien avec la DITP, la DGAFP et les référents IA ministériels
2. **Construire un socle technique mutualisé** : applications, outils et infrastructures que toutes les administrations peuvent utiliser
3. **Accompagner les projets IA** à travers l'incubateur ALLiaNCE

&nbsp;

> On résout les problèmes communs une fois pour toutes, pour que chaque administration se concentre sur son métier.

## Le socle IA interministériel

**Le problème :** chaque administration repartait de zéro — quelle infrastructure GPU ? Quel modèle souverain ? Comment gérer SecNumCloud ? Comment respecter la loi SREN ?

**3 piliers du socle :**

| Pilier | Ce qu'il apporte |
|--------|-----------------|
| **Albert API** | GPU mutualisés, modèles LLM (open-weight & Mistral), API aux standards OpenAI |
| **Plateforme de données** | Données publiques prêtes pour l'IA |
| **Applications** | Assistant IA, Docs, Visio, Fichiers, etc. |

# Rendre les données publiques AI-ready

## La conviction de départ

La performance d'un système d'IA dépend directement de la **qualité du contexte** qu'on lui fournit.

C'est ce qu'on appelle le **context engineering** : avant de choisir un modèle, il faut préparer et exposer ses données.

:::callout[Notre mission]
Rendre la donnée publique consommable par l'IA — pas dans un seul format, mais dans un **écosystème multi-formats** adapté à chaque usage.
:::

- **Datasets vectorisés** — fichiers Parquet prêts à l'emploi
- **RAG** — collections documentaires publiques & privées
- **MCP** — connecter et faire interagir des systèmes d'IA
- **Skills** — fournir les standards de l'État aux assistants de code
- **CLI** — outils en ligne de commande pour les agents et les développeurs

## Datasets vectorisés — MediaTech

Des **collections de données publiques** nettoyées, découpées et vectorisées, distribuées en Parquet sur HuggingFace et data.gouv.fr.

**9 collections disponibles :**

- Legifrance (codes et lois)
- service-public.fr (guides usagers)
- Catalogue data.gouv.fr
- Travail & emploi
- CNIL
- Annuaires des administrations
- Conseil constitutionnel

## RAG

**Collections publiques mutualisées**
Legifrance, service-public.fr… accessibles à toutes les administrations via Albert API.

**Collections privées par administration**
Espaces documentaires dédiés pour les données métier sensibles.

**3 niveaux selon la sensibilité :**

| Niveau | Usage | Données |
|--------|-------|---------|
| Mutualisé | Collections partagées | Non sensibles |
| Single-tenant | Espace ministériel dédié | Sensibles |
| On-premise | Hébergé par l'administration | Confidentielles |

## Model Context Protocol (MCP)

Le **Model Context Protocol** est un protocole ouvert qui connecte les agents IA à des sources de données et des outils.

**L'analogie :** une prise universelle entre l'IA et vos systèmes d'information.

- **Avant MCP :** chaque intégration IA ↔ donnée = un développement sur mesure
- **Avec MCP :** un protocole standard, l'IA interroge les sources en temps réel

**Adopté par** Anthropic, OpenAI, Google, Microsoft, et un écosystème open source grandissant.

:::callout[Ce que ça change concrètement]
L'IA ne se contente plus de texte pré-indexé. Elle peut chercher, filtrer et interroger vos données à la volée — comme un développeur le ferait avec une API.
:::

## Nos premières briques MCP

**data.gouv.fr** — serveur MCP expérimental

- Développé avec **FastMCP** (framework open source)
- 5 tools exposés : recherche de datasets, métadonnées, interrogation tabulaire, recherche d'APIs
- 3 millions de requêtes dès les premiers jours

**data.education.gouv.fr** — serveur MCP du ministère de l'Éducation nationale

- Développé avec **Huwise** (ex-OpenDataSoft — solution propriétaire)
- Connecte l'IA aux données éducatives

:::callout[Vision cible]
Une MCP Gateway interministérielle + des verticales spécialisées (DILA/Legifrance, INSEE, Éducation…)
:::

## MCP App — l'exemple DVF

Les **Demandes de Valeurs Foncières** (DVF) : données de transactions immobilières, le dataset le plus demandé sur data.gouv.fr.

**Ce qu'on a construit :** une MCP App qui permet à un agent IA de chercher et afficher les transactions immobilières d'une commune.

**Un nouveau format :** des applications construites sur MCP, publiables sur les stores IA (ChatGPT, Claude…).

:::alert[info]
Perspective d'utilisation des MCP par les citoyens — ce n'est pas un projet officiel de l'État, mais une exploration de ce que ce format rend possible.
:::

## Démo — MCP App DVF

![Démo de la MCP App DVF — recherche de transactions immobilières via un agent IA](./images/demo-mcp-app-dvf.gif)

## Skills pour les assistants de code

Des **modules de connaissance réutilisables** pour Claude Code, OpenCode, Mistral Vibe.

**Repo open source contenant :**

- **react-dsfr** — Composants React conformes au Design System de l'État
- **rgaa** — 106 critères d'accessibilité numérique
- **securite-anssi** — 12 règles de sécurité essentielles
- **lasuite-ui-kit** — Composants pour les applications LaSuite
- **datagouv** — Référence des APIs data.gouv.fr

**Objectif :** rendre les standards de l'État exploitables avec des assistants de code.

:::alert[info]
Work in progress — premières initiatives, contributions ouvertes.
:::

## CLI — le format le plus simple

Un **outil en ligne de commande** que l'agent IA peut appeler directement depuis le terminal.

**Pourquoi les CLI comptent :**

- **Familiarité** — les développeurs savent déjà les utiliser, les agents IA aussi
- **Composabilité** — on les chaîne avec des pipes (`|`), on les intègre dans n'importe quel script
- **Efficacité** — 2 à 30x moins coûteux en tokens que MCP pour les requêtes simples (les benchmarks varient)
- **Zéro infra** — pas de serveur, pas de processus persistant

**Exemple :** une CLI `datagouv` qui permet de chercher un dataset, lire ses métadonnées, interroger une ressource tabulaire — en une ligne de commande.

:::callout[CLI et MCP sont complémentaires]
CLI pour l'automatisation personnelle et les requêtes simples. MCP pour les agents en production avec authentification multi-utilisateurs et audit.
:::

## Le prochain challenge — les données authentifiées

Aujourd'hui, on traite de la **donnée ouverte** : textes juridiques, open data, guides publics.

**Ce qu'on n'a pas encore attaqué :**

- SI internes et bases métier protégées
- APIs nécessitant des droits d'accès
- Documents à diffusion restreinte voir secret défense...

**Les enjeux :**

- Gestion fine des droits et des habilitations
- Traçabilité des accès par les agents IA
- Gouvernance : qui autorise quoi, pour quel usage ?

> C'est le palier pour que l'IA soit vraiment utile dans les processus métier quotidiens.

## Convictions terrain

1. **La préparation des données est le vrai bloqueur** — pas l'accès. Les données existent, mais ne sont pas dans un format exploitable par l'IA.

2. **Il faut multiplier les formats d'exposition** — Parquet, RAG, MCP, Skills, CLI… Chaque usage a son format optimal.

3. **La verticalisation par domaine fait sens** — juridique, éducation, santé, économie… Chaque domaine a ses spécificités.

4. **Le RAG mutualisé a ses limites** — chaque cas d'usage est spécifique. La vraie valeur est dans les données pré-préparées, pas dans l'infra RAG elle-même.

# Vibe coding dans l'État

## Le constat — shadow IT massif

**Aujourd'hui dans les administrations :**

- Claude Code, Cursor, Copilot, Lovable utilisés **sans cadre**
- Pas de doctrine sur ce qui est autorisé
- Pas de réponse souveraine

Des CPO prototypent des applications. Des non-développeurs créent des outils internes. Le rapport au code change fondamentalement.

:::alert[warning]
Le shadow IT n'est pas un problème de discipline — c'est le signal d'un besoin non couvert.
:::

## Un exemple concret — l'Observatoire du SPDR

L'**Observatoire du Service Public de la Donnée de Référence** : un tableau de bord de suivi de la conformité de 9 datasets de référence de l'État.

- **Projet bloqué depuis 18 mois** — pas de temps dev disponible, pas de budget
- **Grâce au vibe coding : sorti en quelques jours**

**Mais le vrai problème commence maintenant :**

- Comment passer ça en production ?
- Comment maintenir, faire évoluer, sécuriser ?
- Comment intégrer dans un SI existant ?

> Le vibe coding accélère la création. Il ne résout pas la mise à l'échelle.

## L'Observatoire du SPDR

![Capture d'écran de l'Observatoire du Service Public de la Donnée de Référence](./images/observatoire-spdr.png)

## "Albert Code" — le concept

Un **assistant de code souverain** qui intègre les standards de l'État par défaut.

**L'idée :**

- DSFR, ANSSI, RGAA embarqués — pas ajoutés après coup
- Approche 100% locale — aucune donnée ne sort de la machine
- Le modèle est une commodité — la vraie valeur, ce sont les standards by design

&nbsp;

:::alert[info]
Concept en cours d'exploration — pas encore sorti ni validé. On en est au stade de la recherche utilisateur et du prototypage.
:::

# Enseignements

**Ce qui marche :**

- **Mutualiser l'infra** plutôt que dupliquer les efforts — GPU, modèles, compliance
- **Embarquer les standards dans l'outil** — pas en aval, pas en option
- **Commencer simple et local** — un script d'install, des données prêtes, pas d'usine à gaz
- **Piloter par les usages terrain** — pas par la technologie

**Ce qui est dur :**

- **Souveraineté vs. performance** — le gap entre modèles souverains et commerciaux se réduit, mais existe encore
- **Passage POC → production** — le "valley of death" de l'IA publique, amplifié par le vibe coding
- **Données authentifiées et SI legacy** — le prochain mur à franchir
- **Gouvernance interministérielle** — co-financement, priorisation, contributions entre ministères

## Échanges

<div style="text-align: center;">
<div class="merci-presenter-card">
<div class="merci-avatar"><img src="./images/benoitvinceneux.png" alt="Benoit Vinceneux" /></div>
<div class="merci-info">
<p class="merci-name">Benoit Vinceneux</p>
<p class="merci-role">EIG & CPO Données / MCP — Département IA dans l'État</p>
</div>
</div>

<div class="merci-contact">
<a href="mailto:benoit.vinceneux@numerique.gouv.fr">benoit.vinceneux@numerique.gouv.fr</a>
<a href="https://www.linkedin.com/in/benoitvinceneux/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
</div>
</div>
