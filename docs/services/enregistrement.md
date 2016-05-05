---
layout: page
title: Enregistrer un pseudo/canal
---

L'enregistrement permet de "réserver" et protégrer un nom d'utilisateur ou un canal.

* Dans le cas des noms d'utilisateurs, cela permet d'empêcher quelqu'un d'autre d'utiliser votre pseudo et vous permet aussi d'enregistrer un canal.
* Dans le cas des canaux, cela permet de conserver vos droits sur le canal (par défaut, un canal non-enregistré est détruit lorsqu'il n'y a plus personne; la première personne qui s'y reconnecte est alors considérer comme fondatrice et obtient alors les droits d'administration).

**Note :** Si vous n'êtes pas habituer à IRC, sachez qu'une commande comemnce toujours par un slash. Sinon, ce que vous entrez est considérer comme un message. Attention à ne pas mettre d'espace avant le slash lorsque vous tapez une commande.

## Eneregistrer un pseudo (nom d'utilisateur)

### Via l'interface web (plus simple)
C'est la méthode la plus simple ! Connectez-vous sur [services.ekinetirc.com](https://services.ekinetirc.com/). Vous disposez d'un formulaire permettant d'enregistrer votre pseudo simplement et en quelques secondes.  
**Note :** Le mot de passe est sensible à la casse.

Un e-mail vous est ensuite envoyé pour vérifier votre adresse. Ce dernier contient une commande (à exécuter sur IRC) qui permet de confirmer l'enregistrement.

### Via le robot NickServ sur IRC (plus compliqué)
Afin d'enregistrer le pseudo sous lequel vous êtes actuellement connecté, il suffit de tapez cette commande :
<pre><code>/msg nickserv register <u>mot de passe</u> <u>e-mail</u>
</code></pre>

**Note :** Vous devez remplacer la/les partie(s) <u>soulignée(s)</u> ci-dessus par leur correspondance.  
**Note :** <u>mot de passe</u> est sensible à la casse.

Un e-mail vous est ensuite envoyé pour vérifier votre adresse. Ce dernier contient une autre commande qui permet de confirmer l'enregistrement.

**Astuce :** Vous pouvez abréger `/msg nickserv` en `/ns` lorsque vous tapez votre commande.

### Connexion
Une fois votre pseudo enregistrer, vous devez vous connecter avec votre mot de passe, sinon vous ne pourrez pas l'utiliser (il sera modifié automatiquement après **60 secondes**).

Pour cela, il suffit généralement de cochez une case (`J'ai un mot de passe`) si vous vous connectez depuis votre navigateur internet. Sinon, vous pouvez utiliser cette commande :
<pre><code>/identify <u>pseudo</u> <u>mot de passe</u>
</code></pre>

**Note :** Le pseudo est facultatif. Si il n'est pas spécifié, le serveur tentera de vous identifier avec le pseudo sous lequel vous êtes connecté.

### Paramètrage
Si vous souhaitez paramètrer votre pseudo, n'hésitez pas à consulter ce que retourne cette commande :
<pre><code>/query NickServ help <u>commande</u>
</code></pre>

Cela donnera le détail d'une commande. Si vous ne spécifiez pas de commande, cela va lister toutes les commandes disponible et leur rôle.  
**ATTENTION :** Toutes les commandes qui sont données via l'aide doivent être envoyées en privé à NickServ ou préfixées par `/nickserv`

Quelques paramètres sont aussi accessibles via l'interface web (incomplet !).

## Enregistrer un canal
Avant d'enregistrer un canal, vous devez être connecté dessus et y être opérateur (avec un `@` devant votre pseudo).
Il n'est pas possible d'enregistrer un canal via l'interface web. Vous devez donc ensuite exécuter cette commande :
<pre><code>/msg chanserv register <u>#canal</u> <u>description</u>
</code></pre>

**Note :** Vous devez remplacer la/les partie(s) <u>soulignée(s)</u> ci-dessus par leur correspondance.  
**Note :** La description est facultative.

Le canal est désormais enregistrer sous votre pseudo.

**Astuce :** Vous pouvez abréger `/msg chanserv` en `/cs` lorsque vous tapez vos commandes.

### Paramètrage
Afin de paramètrer votre canal, n'hésitez pas à consulter ce que retourne cette commande :
<pre><code>/query chanserv help <u>commande</u>
</code></pre>

Cela donnera le détail d'une commande. Si vous ne spécifiez pas de commande, cela va lister toutes les commandes disponible et leur rôle.  
**ATTENTION :** Toutes les commandes qui sont données via l'aide doivent être envoyées en privé à ChanServ ou préfixées par `/chanserv`

Quelques paramètres sont aussi accessibles via l'interface web (incomplet !).

## Obtenir de l'aide
Si vous avez un problème, n'hésitez pas à demande de l'aide sur [#EkiNetIrc](irc://irc.ekinetirc.com/#EkiNetIrc) (`/join #EkiNetIrc`). Nous nous ferons une joie de vous aider.
