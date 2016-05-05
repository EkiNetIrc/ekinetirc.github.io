---
layout: page
title: Utiliser les services
---

*[WIP] Cette page est en cours de constructions !*

Afin d'améliorer l'expérience de nos utilisateurs, EkiNetIrc dispose de services sur son réseau présentés sous forme de robots.

## NickServ
**NickServ** est un service de gestion des pseudos qui vous permet d'enregistrer votre pseudo et ainsi empêcher d'autres personnes de l'utiliser.


### Enregistrer son pseudo
Afin d'enregistrer votre pseudo pour le protéger, exécutez cette commande sur IRC :
<pre><code>/ns register <u>mot de passe</u> <u>e-mail</u>
</code></pre>

**Note :** Vous devez remplacer la/les partie(s) <u>soulignée(s)</u> ci-dessus par leur correspondance.  
**Note :** Cette commande s'exécute en prenant en compte le pseudo que vous utilisez lorsque vous exécutez la commande.  
**Note :** <u>mot de passe</u> est sensible à la casse.

**Astuce :** Vous pouvez aussi enregistrer votre pseudo par [l'interface web](http://services.ekinetirc.com/register).


### Ajouter un autre pseudo à son compte
NickServ utilise un système de compte (aussi appelé groupe) qui permet de réunir plusieurs pseudos partageant la même configuration.
Un groupe est automatiquement créer lors de la [création du pseudo](#enregistrer-son-pseudo).

Afin d'ajouter un pseudo à votre compte, exécutez cette commande sur IRC :
<pre><code>/ns group <u>compte</u> <u>mot de passe</u>
</code></pre>

**Note :** Vous devez remplacer la/les partie(s) <u>soulignée(s)</u> ci-dessus par leur correspondance.  
**Note :** Cette commande s'exécute en prenant en compte le pseudo que vous utilisez lorsque vous exécutez la commande.  
**Note :** <u>mot de passe</u> est sensible à la casse.  
**Note :** Le mot de passe doit-être celui de votre compte !


### Réinitialiser son mot passe
Il arrive parfois que l'on oublie son mot de passe et que l'on ne puisse plus se connecter à son compte.
Pour le changer, il suffit d'utiliser la commande resetpass qui s'utilise comme ceci :
<pre><code>/ns resetpass <u>pseudo</u> <u>e-mail</u>
</code></pre>

**Note :** Vous devez remplacer la/les partie(s) <u>soulignée(s)</u> ci-dessus par leur correspondance.

Cette commande va vous envoyer un email vous décrivant la marche à suivre pour changer de mot de passe.


### Récupérer la liste des utilisateurs
Il existe une commande permettant de récupérer une liste d'utilisateurs selon le filtre transmis :
<pre><code>/ns list <u>filtre</u>
</code></pre>

**Note :** Vous devez remplacer la/les partie(s) <u>soulignée(s)</u> ci-dessus par leur correspondance.  
**Astuce :** Si vous mettez une **\* (étoile)** cette commande vous affichera tous les utilisateurs enregistrés.  
**Astuce :** Le filtre peut être une [expression régulière](https://fr.wikipedia.org/wiki/Expression_rationnelle) PCRE :
il suffit de la mettre entre deux **/ (slash)**.

*Une documentation plus complète est accessible à l'aide de la commande `/ns help list`.*

**EXEMPLE :** `/ns list #51-100` affichera tous les pseudos enregistrés dont le l'identifiant se trouve entre 51 et 100.
