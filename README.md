---
description: Naviguez l'API privée d'EcoleDirecte avec le module de vos rêves...
---

# edjs-docs

{% hint style="warning" %}
Cette documentation peut être incomplète.
{% endhint %}

`ecoledirecte.js` est un node\_module qui vous permet d'interagir avec EcoleDirecte en un claquement de doigts. Son objectif n'est pas seulement de vous offrir les informations, mais de les formater avant de vous les présenter. Les données d'origine au format brut, parfois plus complètes, restent toujours disponibles.

`ed.js` est construit avec TypeScript et toutes les réponses de l'API EcoleDirecte sont hard-typed, pour que tout ce que vous faites soit couvert par votre IntelliSense et le pouvoir de TypeScript.

Chaque fonctionnalité prend du temps à être implémentée. Mais nous préférons proposer un minimum de décence et d'approndonfissement pour chaque nouvelle intégration.

```javascript
import { Session } from "ecoledirecte.js"

async function main() {
    const session = new Session("EDELEVE", "0")
    const account = await session.login()
    if (account.type !== "student") return;
    
    const someHomework = await account.getHomework("2021-01-14")
    console.log("Hi,", someHomework[0].prof)
};

main()
```

