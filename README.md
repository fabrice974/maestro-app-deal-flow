# maestro-app-deal-flow

Application **Deal flow** (simulée) de la PoC Maestro : enregistre les occasions d'investissement et
réalise les tâches du deal flow (qualification, analyse, approbations, structuration, juridique,
assignation du mandat).

Elle ne connaît ni Camunda ni le BPMN : elle parle uniquement à la passerelle du backbone
([maestro-v2](https://github.com/fabrice974/maestro-v2)) via le SDK
[`@maestro/sdk`](https://github.com/fabrice974/maestro-sdk-ts) (épinglé sur une étiquette).

## Lancer

```bash
npm install
cp .env.example .env     # facultatif : valeurs par défaut = démo locale
npm start                # http://localhost:4101
```

Prérequis : la passerelle de maestro-v2 démarrée (`npm run passerelle` dans maestro-v2), ou tout
l'écosystème : `npm run ecosysteme -- demarrer` depuis maestro-v2.

## Ce qui appartient à cette équipe

- Les écrans propres (`src/main.ts` : formulaire « Nouvelle occasion », pipeline).
- La version du SDK utilisée (`package.json`).

Ce qui n'en dépend pas : le déroulement du processus, les règles d'affaires, les rôles et la sécurité
(backbone), ainsi que la boîte de tâches et le formulaire générique (SDK).
