---
layout: page
title: Les hôtes virtuels (vhosts)
---

Cette page, explique comme appliquer un vhost (aussi appelé hôte virtuel) à votre connexion sur notre réseau IRC.


## Un hôte virtuel : Kasékoi ?
Avant de parler d'*hôte virtuel*, il faut commencer par parler d'*hôte*.
Un hôte est un nom de domaine, mis en place par votre [Fournisseur d'Accès à Internet (FAI)](https://fr.wikipedia.org/wiki/Fournisseur_d%27acc%C3%A8s_%C3%A0_Internet) et pointant directement vers votre IP.

Par exemple, sur une connexion Orange (livebox), elle ressemble à cela (certaines parties sont masqués par des étoiles) :
<pre><code>ANantes-655-1-***-**.w2-1.abo.wanadoo.fr
</code></pre>

Cela permet donc à n'importe de qui de récupérer votre adresse IP (je tiens à préciser que contrairement à certaines idées reçu, il n'y a quasiment aucun risque à ce que votre adresse IP soit publique. Elle est par ailleurs connu par les administrateurs de tous site internet que vous visitez).  
En effet, votre hôte s'affiche lorsque vous rejoignez ou quittez un canal ainsi qu'a d'autres endroits (dans un `/whois` par exemple).

Afin de masquer votre IP, l'idée est d'appliquer lors de votre connexion un hôte virtuel qui sera diffuser par les serveurs aux autres personnes à la place de votre véritable hôte.  
Cet hôte virtuel se présente sous cette forme :
<pre><code>utilisateur/<u>pseudo</u>
</code></pre>
L'utilisation d'un slash dans l'hôte est volontaire car ce caractère ne pourras jamais se retrouver dans un vrai nom d'hôte.

Si vous faites partie du staff d'un projet/site/*autre* ayant un canal IRC officiel sur notre réseau, nous pouvons appliquer un hôte virtuel ayant cette forme :
<pre><code><u>nom_du_projet</u>/<u>partie_intermédiaire_faculative</u>/<u>pseudo</u>
</code></pre>

Veuillez notez qu'un hôte virtuel ne vous rend pas complètement anonyme. Quelqu'un de déterminer et ayant quelques connaissances peut réussir à retrouver votre adresse IP.  
N'oubliez pas cette règle : Vous n'êtes **JAMAIS** anonyme sur Internet.


## Comment obtenir un hôte virtuel
Afin de garder la main sur l'attribution des hôte virtuel et d'éviter les abus, aucune procédure automatisée n'a été mise en place.

### Prérequis
* Il vous faut d'abord [enregistrer votre pseudo](/docs/services/enregistrement.html). En effet, votre hôte virtuel sera lié à votre compte.
* Si vous faites parti d'un projet nous devrons d'abord avoir la confirmation d'un des responsables du projet avant de mettre en place votre hôte virtuel
(si votre projet ne dispose pas encore de vhost, voir ci-dessous)

### Demande
Votre demande doit-être fait auprès d'un des [administrateurs du réseau](/equipe.html).
Pour cela, rejoignez le canal [#EkiNetIrc](irc://irc.ekinetirc.com/#EkiNetIrc) et effectuez votre demande.

Soyez patient, nous ne sommes pas toujours devant notre PC !

### Attribution
L'attribution de l'hôte virtuel va être effectuer par un des [administrateurs du réseau](/equipe.html). Vous n'avez rien à effectuer de votre côté.
A la seconde où l'administrateur va mettre en place votre hôte virtuel ainsi qu'à chaque fois qu'elle s'activera (ex: à chaque connexion), le serveur enverra un message (qui s'affichera dans la console) :
<pre><code>:hirin.ekinetirc.com 396 pseudo utilisateur/pseudo :is now your hidden host (set by services.ekinetirc.com)
</code></pre>


## Conseils
Votre hôte virtuel ne sera mis en place que si vous êtes identifié avec votre mot de passe. Identifiez-vous donc dès la connexion.
Si vous utilisez un client IRC, vous pouvez utiliser la fonctionnalité SASL si pris en charge. Elle est quasi infaillible pour l'identification.

Si vous vous identifiez lorsque vous avez déjà rejoint un canal, le système vous ferra automatiquement quitter et revenir sur tous les canaux où vous êtes présent.
Pour vous, cet opération est TOTALEMENT invisible. Pour les autres utilisateurs, cela provoquera l'affichage de quelque chose comme ça :
<pre><code>[20:31:47] pseudo [~user@ANantes-655-1-***-**.w2-1.abo.wanadoo.fr] vient de se déconnecter : Changing host
[20:31:47] pseudo [~user@utilisateur/pseudo] a rejoint #Canal
</code></pre>

N'utilisez pas votre hôte virtuel à des fins contraire à notre [netiquette](/netiquette/), sinon un administrateur pourra vous le retirer sur-le-champ.

Rappelez-vous que cela nous vous rend pas totalement anonyme. Les [administrateurs du réseau](/equipe.html) peuvent toujours voir votre adresse IP.
De même nous enregistrons toute connexion à notre réseau avec l'IP réelle pour des raisons légales.


## Hôtes virtuels liés au groupes et aux projets
Cette section décrit l'utilisation des hôtes virtuels pour les groupes et les projets ayant un canal officiel sur notre réseau.

### Inscription
Afin de mettre en place vos vhosts de groupe, un responsable du groupe/projet devrait contacter un [administrateur du réseau](/equipe.html) (Zoddo si possible).

Demandez à chaque membre de votre équipe d'enregistrer son pseudo puis préparez une liste des utilisateurs avec les vhosts correspondantes.
Vous pouvez aussi nous fournir une liste d'autres membres de votre équipe habilités à effectuer des demandes de modifications des vhosts.

### Ajouts, modifications et retraits des vhosts
Un responsable du projet doit contacter un des [administrateurs du réseau](/equipe.html) et effectuer la demande.
Elle sera traité le plus rapidement possible.
