.. FriendlyBot documentation master file, created by
   sphinx-quickstart on Fri Apr 24 15:38:40 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.



##########################################
La documentation officielle de FriendlyBot
##########################################

*******************
**Le commencement**
*******************

**Préface**
===========

| Bienvenue sur la documentation officielle de FriendlyBot.
| Tu trouveras ici toutes les informations nécessaires à l'utilisation de FriendlyBot.
| *( aka FB )*
| Mais également sur `le Discord`_ ! 😎
| ( Pense à le partager à tes potes pour agrandir la famille de FriendlyBot )

.. _le Discord: https://discord.gg/DEUuavq

**Introduction**
================

*L'histoire d'un bot Dofus...*

Le Staff
--------

* Nigoco, tout simplement ZI BOSS
* Aursen, le traducteur AS3 vers C# jusqu'au bout de la nuit.
* MrLucifer, heureusement que "Le second degré n'est pas qu'une température".
* Vok, le dév' Web qu'on aime.

Les membres premium
-------------------

   *Nicogo dixit „ les gens cools 😎 “*

* Dampen59, le couteau suisse informatique.
* TheFrenchCoder, l'homme de la documentation, qui pose 40 12 milles questions.
* Kritune, le dév' de plugins du „ TURFU “.
* Théo, le gentleman de la sécurité des lignes de codes de FriendlyBot.

**Foire aux questions (FAQ)**
================================

   Si vous avez un problème avec FriendlyBot, pensez à jeter un petit coup d’œil par ici, avant de poster une demande d'aide sur le forum.
      1. Cela vous évitera d'écrire pour rien.
      2. Cela permettra aux administrateurs de se concentrer sur des soucis encore non résolus.

**1. J'ai une erreur d'identification lorsque je me connecte sur le logiciel.**
-------------------------------------------------------------------------------

   * Vous avez entré des identifiants erronés.
   * Vous avez récemment fermé le logiciel, vous devez attendre quelques minutes avant de le rouvrir.
   
**2. J'essaie d'ouvrir l'éxécutable FriendlyBot.exe mais rien ne se passe.**
----------------------------------------------------------------------------

   * Suprimer le fichier temporaire de FriendlyBot :
      * ``Windows + R`` >> ``%appdata%`` >> ``Entrer``.
      * Remonter d'un dossier.
      * Chercher le dossier „ FriendlyBot “ et supprimer le.
   * Supprimer le dossier „ plugins “ situe à côté de l'éxécutable.

****************
**Installation**
****************

**Pré-requis**
==============

| FriendlyBot nécessite certains logiciels externes pour fonctionner correctement.
| FriendlyBot est développé en C#, un langage informatique multiplateformes et est donc disponible sous Windows, Linux et Mac. 
| Rendez vous sur le site `dotnet.microsoft.com`_ pour télécharger .NET, vous aurez deux choix :

* Vous souhaitez utiliser FriendlyBot de façon classique, installez :
   **Run Apps .NET Core Runtime**
* Si vous souhaitez développer vos propres plugins pour FriendlyBot, installez :
   **Buils Apps .NET Core SDK**

.. note::

   ▶️ : Veillez à choisir la version correspondant à votre système d'exploitation, Windows, Linux ou OSX.*

.. _dotnet.microsoft.com: https://dotnet.microsoft.com/download

*****************
**FriendlySuite**
*****************

**Langage de programmation**
============================

| Vous voilà sur le premier chapitre de la section traitant "Les Trajets".
| Que vous soyez débutant ou expert en programmation, cette section vous expliquera tout ce que vous devez savoir sur le LUA.

**Le LUA, quèsaco ?**
---------------------

| *LUA est un langage de script [...] conçu de manière à pouvoir être embarqué au sein d'autres applications afin d'étendre celles-ci.*
| `Wikipédia - LUA`_

.. _`Wikipédia - LUA`: https://fr.wikipedia.org/wiki/Lua

| Nous allons te présenter le langage LUA afin que vous puissiez
| réaliser vos rêves sur **Le Monde des Douze**.

**Le type de fichier**
----------------------

| En informatique, les fichiers possèdent tous une extension, cela permet d'identifier le format du fichier via ce suffixe.
| On peut noter que le fichier de texte basique se termine en .txt , un fichier sonore en .mp3, un fichier exécutable en .exe et ainsi de suite.
 
| Le lua fonctionne lui avec des fichiers en .lua

| FriendlyBot ne prend en charge que les .lua pour ses trajets,
| vous allez devoir développer votre code en lua et donc avec l'extension .lua.

| Sur Windows, vous ne pouvez par défaut pas voir voir et modifier les extensions des fichiers.
| Vous pouvez affic| her les extensions après le nom du ficher et obtenir cette syntaxe :
| ``<nom du fichier>.<extension du fichier>``, cela peux vous être utile en dehors du botting 🙂

**Afficher les extensions**
---------------------------

* Ouvrez votre "Explorateur de fichiers"
* Appuyez sur le bouton "Affichage" présent en haut de la fenêtre.
* Cochez la case " Extensions de noms de fichiers "
* Rendez-vous où vous voulez sur votre ordinateur et constatez l'apparition des extensions à la suite du nom des fichiers.

*Une image arrive prochainement 💋 TheFrenchCoder*

**Création du fichier .lua**
----------------------------

Maintenant que vous pouvez voir toute la beauté des extensions des fichiers présents sur votre ordinateur,
vous allez pouvoir créer votre premier fichier en .lua afin d'y placer tous le code nécessaire pour
réaliser un trajet avec FriendlyBot.

* Ouvrez le dossier dans lequel se situe votre exécutable „ FriendlyBot.exe “.
* Faîtes un clique droit > „ Nouveau “ > „ Document Texte “.
* Rentrer son nom „ MonScript.lua “.

.. warning::

   *Pensez à enlever l'ancienne extension : .txt.*

* Répondez „ Oui “ à „ Voulez-vous vraiment modifier l'extension ? “.

.. note::

   ▶️ Il s'agit d'un sécurité de Windows, car l'extension renseigne également sur le formatage du fichier, ne vous en souciez pas.

| Vous avez maintenant un fichier .lua près à être rempli pour réaliser votre
| premier trajet avec FriendlyBot.

**Structure**
=============

**Vue générale**
----------------------------

| Voici un trajet simpliste, dépourvu de toutes instructions contenant
| toutes les instructions indispensables :

.. code-block:: lua

   function movePath()
      return {
         -- Les actions que le bot devra éxécuter : les déplacements,
         -- les récoltes, les combats
      }
   end

   function bankPath()
      return {
         -- Le trajet à réaliser pour aller en banque lorsque
         -- l'inventaire du personnage est plein
      }
   end

   function lostPath()
      return {
         -- Le trajet et les actions à réaliser lorsque le bot
         -- est perdu
      }

   function deadPath()
      return {
         -- Le trajet à réaliser pour aller au phenix lorsque le
         -- personnage est en "fantôme"
      }
   end

**Fonction « movePath »**
^^^^^^^^^^^^^^^^^^^^^^^^^


La fonction movePath contient toutes les actions exécutées à chaque changement de map. C'est la fonction basique, elle est appelée par défaut.

**Fonction « bankPath »**
^^^^^^^^^^^^^^^^^^^^^^^^^

La fonction bankPath contient toutes les actions permettant de se rendre à la banque ou dans une maison afin de vider son inventaire.
Elle est appelée lorsque l'inventaire du joueur dépasse un pourcentage fixée dans le fichier de configuration.

**Fonction « lostPath »**
^^^^^^^^^^^^^^^^^^^^^^^^^

La fonction bankPath contient toutes les actions permettant au bot de retrouver son chemin. Si le bot est perdu, il exécute les actions contenues ici. Une fois qu'il se retrouve sur un chemin, celui de movePath en général, celui de bankPath s'il est considéré comme "full" ou encore celui de deadPath s'il est en fantôme.

**Fonction « deadPath »**
^^^^^^^^^^^^^^^^^^^^^^^^^

| *PAS ENCORE IMPLÉMENTÉE* 😢
| C'est qu'un beta fermée, déso la plèbe 🙃

**Fonctions personnalisées**
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Il est bien évidemment possible de rajouter ses propres fonctions au sein du fichier .lua et de les utiliser au sein des fonctions "primaires".

Maintenant que vous avez bien en tête la structure des fichiers de trajets en LUA et leurs fonctions, il va falloir fournir ces quatre fonctions d'actions afin d'expliquer au bot ce que l'on attend lui, c'est ce que nous allons voir dans le prochain chapitre « Actions ».

**Actions**
===========

**Mise au point**
----------------------------

Comme vu dans le chapitre précédent, les fonctions écrites en LUA retournent à FriendlyBot les actions à réaliser elles-mêmes regroupées au sein de tables qui sont situées entre les crochets du mot clé ``return`` :

* Le mot clé ``return``  renvoie les tables.

* Les tables contiennent les actions à réaliser sur une ou plusieurs maps.

   * Les tables sont séparées par une virgule pour expliquer à FriendlyBot qu'il y'a encore d'autres tables après.

   * La table finale ne se "termine" donc pas avec une virgule.


.. code-block:: lua

   function movePath()
      return {
         {<ma_première_table> }, -- première, 1ère table => 1 virgule
         {<ma_deuxième_table> }, -- médiane, 2ème table => 1 virgule
         {<ma_troisème_table> }, -- médiane, 3ème table => 1 virgule
         {<ma_troisième_table>}  -- dernière, 4ème table => ∅ virgule
      }
   end

.. code-block:: lua

   -- Une table ressemble à ceci
   {maps, actions}

**Les actions**
---------------

Il existe différents types d'actions, c'est ce que nous allons voir maintenant :

**Maps**
^^^^^^^^
Le mot clé ``maps`` peut utiliser à la fois les **coordonnées** (abscisse, ordonnée) de la map obtenable en regardant sur la carte de Dofus mais aussi son id appelé le **mapId** obtenable en exécutant dans le tchat du jeu ou via la console de FrienldyBot **/mapid**.
Il est possible de définir les maps une à une ou via une liste (une table en LUA), si l'on souhaite réaliser plusieurs fois la même action :

.. code-block:: lua

   return {
      -- Une map pour les gouverner tous ^^
      {maps = "[4,-19]"},
      -- Une map  ? Mais moi, j'en ai plusieurs :)
      {maps = {"[5,-22]", "192416776"}}
   }

**Les tables**
^^^^^^^^^^^^^^

Le mot clé ``actions`` renseigne toutes les actions à réaliser au sein des maps définies dans ``maps``. (Le code suivant serra sous la forme de „ vue en éclaté “)

.. code-block:: lua

   return {
      {maps = "[0,0]", actions = changeMap("bottom")},
      {
         maps = {
               "[0,1]",
               "192416776"
         },
         actions = {
               gather(),
               changeMap("left")
         }
      }
   }

.. caution::

   La lecture des actions à effectuer par FriendlyBot se fait de gauche à droite.
   Dans le second exemple, on commence par appeler la fonction gather()
   puis l'on appelle la fonction changeMap() avec comme argument "left", ce qui donne changeMap("left").
   (Pour lui dire de se déplacer vers la gauche.)

**Déplacements simples**
^^^^^^^^^^^^^^^^^^^^^^^^
Pour commencer, il va falloir réaliser un déplacement basique sur une map adjacente.

.. code-block:: lua

   {map = "[0,0]", actions = changeMap("bottom || left || right || top")}

Cette ligne contient plusieurs informations :
* ``map`` représente les coordonnées de la carte où l'on souhaite exécuter les actions suivantes.
Cette emplacement peut être exprimé en coordonnées ou en ``mapids`` obtenable via ``/mapid``.
* ``changeMap`` permet de se déplacer sur une map adjacente à celle où l'on se situe. Attention, elle ne permet pas l'utilisation d'objets interactifs comme les entrées de mine, les portails, etc...  
``changeMap`` peut contenir les valeurs suivantes : ``bottom``, ``left``, ``right`` et ``top``.

Si vous souhaitez vous déplacer sur une cellule sur la map où vous vous situez, il faut utiliser ceci :

.. code-block:: lua

   {map = "[0,0]", actions = move("c<CELL_ID>")}

**Récoltes et combats**
^^^^^^^^^^^^^^^^^^^^^^^

Pour récolter des ressources, il suffit de mettre l'action ``gather`` dans l'état ``true``.
Le personnage ne récoltera que les ressources présentes dans le fichier de configuration.

.. code-block:: lua

   {map = "[0,0]", actions = gather(true)}
   -- Equivalent à --
   {map = "[0,0]", actions = gather()}

Il est aussi possible de récolter les éléments récoltables via :

.. code-block:: lua

   {map = "[0,0]", actions = gather("i<ElemTypeId>")}

Pour combattre des monstres, il suffit de mettre l'action ``fight`` dans l'état ``true``.
Le personnage ne combattra que les groupes suivants les données présentes dans le fichier de configuration.

.. code-block:: lua

   {map = "[0,0]", actions = fight = true}

.. note::

   Si vous souhaitez récolter les ressources ou combattre les monstres présents sur la map où vous avez lancé le trajet, il suffit de mettre ceci :

.. code-block:: lua

   {map = "any", actions = {fight(), gather()}}

**Objets interactifs**
^^^^^^^^^^^^^^^^^^^^^^

Si vous souhaitez interagir avec des objets interactifs (les objets sur lesquelles vous cliquez en temps normal comme c'est le cas avec les des portes, certains escaliers, des leviers, etc...), il suffit de remplacer l'action ``changeMap`` par ``gather`` :

.. code-block:: lua

   {map = "[0, 0]", actions = {fight = true, gather = "c<Cell_ID>"}}
   -- Exemple :
   {map = "[0, 0]", actions = {fight = true, gather = "c459"}}

**PNJ**
^^^^^^^

Si vous souhaitez interagir avec des Personnages Non-Joueurs (PNJ), il suffit d'utiliser l'action ``npc`` qui signifie Non Player Character, l'anglais de PNJ - Personnage Non Joueur :

.. caution::

   *Il n'y qu'une seule action par map, dans les exemples qui suivent, il n'y a donc pas besoin de mettre de {} mais ne les oubliez pas si vous spécifiez plusieures actions.*

.. code-block:: lua

   {map = "[0, 0]", actions = npc(NpcID_or_ActorId, ActionID_or_Index, ReplyID_or_Index1, ReplyID|Index2, ...)}
   -- Exemple :
   {map = "[0, 0]", actions = npc(-20000, -1, -1, -1)}

Se traduit par : 
   | *„ Parle au npc -20 000, avec la première option et ça répond avec les premiers truc possible dans les réponses ^^ “*
   | *Un grand merci à toi, Nicogo pour cet exemple de QUALITAIENT*
   | (La petite réf' 💋 TheFrenchCoder)*


**Craft**
^^^^^^^^^

Si vous souhaitez craft des items, il suffit d'utiliser l'action ``craft``:

.. code-block:: lua

   {map = "[0, 0]", actions = craft(<itemToCraft>, <Amount>)}
                                       (GID)         (int)

**Havre-Sac, Zaap & Zaapi**
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Si vous souhaitez accéder à votre Havre-Sac, il suffit d'écrire:

.. code-block:: lua

   {map="[0, 0]", actions = heavenBag(true)}

Et pour le refermer:

.. code-block:: lua

   {map="any", actions = heavenBag(false)}

Pour accéder à un zaap ou zaapi, il existe deux actions prévues à cet effet:

.. code-block:: lua

   -- Utliser un zaap
   {map="[0, 0]", actions = zaap("<Zaap_ID>")}
   -- Utliser un zaapi
   {map="[0, 0]", actions = zaapi("<Zaapi_ID>")}

**Banque**
^^^^^^^^^^

Pour déposer des items ou des kamas en banque, il suffit d'utiliser l'action ``bank`` comme suit:

.. code-block:: lua

   {map = "[0, 0]", actions = bank(true)} -- pour tous déposer ( Kamas + contenu de l'inventaire )
   {map = "[0, 0]", actions = bank(json)

| Le Json ressemble à ça :

.. note::

   ▶️ Toutes les clés sont optionnelles 

* ItemsToDeposit : (?int[])
   * null : dépose tout
   * Tableau json avec les GID des items à déposer
* ItemsToTake : (?int[])
   * null : rien prendre
   * Tableau json avec les GID des items à prendre
* KamasMove : (int ±)
   * null : rien prendre
   * +x : ... x Kamas
   * -x : ... x Kamas

   (Faites une issue pour préciser le fonctionnement)

.. code-block:: json

   {
      "ItemsToDeposit":null,
      "ItemsToTake":null,
      "KamasMove":0
   }

**Maison**
^^^^^^^^^^

La possibilité d'accéder à une maison, n'est malheureusement pas disponible pour la version bêta. [A venir]

**FonctionCustom**
^^^^^^^^^^^^^^^^^^

| Vous exagérez là, je vais pas vous expliquer comment créer une fonction.
| Bon allez j'suis sympa j'vais vous expliquer !

**Les configurations**
======================

La configuration dont être dans un fichier .lua.

**Combats**
-----------

* Les groupes

Il faut réaliser deux configurations:

   1. Le maître : 

      config-master.lua >>

         .. code-block:: lua

            function master()
               return "true" -- (par défaut)
            end
            function groupName()
               return "<Groupe_Name>"
            end

   2. Le(s) esclave(s) : 

      config-master.lua >>

         .. code-block:: lua

            function master()
               return "false"
            end
            function groupName()
               return "<Groupe_Name>"
            end

.. caution:: ``<Groupe_Name>`` doit être identique entre la config' du maître et celle du/des esclave(s)


* La configuration général

UseWhitelist => true (Use Whitelist) || false (Use Blacklist)
BlackListedMonsters => [] (list of monster's ID)
WhiteListedMonsters => [] (list of monster's ID)
MinMonsters => 1 (par défaut)
MaxMonsters => 8 (par défaut)
MinLife =>

