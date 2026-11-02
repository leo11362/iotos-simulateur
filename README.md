# Simulateur IoToS

Simulateur web et guide d'**IoToS**, le micro-OS pour Arduino UNO R4 de Jean-Marc Biechy.

**Site : https://leo11362.github.io/iotos-simulateur/**

## Ce que contient la page

- **Terminal (KiTTY)** : le démarrage de la carte, l'aide, les 42 commandes, en Série ou en Telnet. Tab, historique et message « Invalid command » reprennent la bibliothèque CmdLine.
- **Page web de la carte** : la commande de la LED (rafraîchie par AJAX) et la page de configuration IP, avec le login du site.
- **Guide** : le matériel (avec schéma), le démarrage, les services, toutes les commandes, des pas à pas, la différence RAM / EEPROM / réseau actif, le dépannage, les pièges du code et des pistes d'amélioration.
- **Démo guidée** : un bouton « ▶ Démo guidée » déroule en 9 étapes un scénario complet (démarrage, aide, LED, page web, changement d'IP), pas à pas ou en lecture automatique. La carte est remise dans son état d'origine à la fin.
- **Réglages de la carte simulée** : taille de la carte SD, IP DHCP, temps de ping, paquets perdus, etc.

## Sources

- Le code d'IoToS v72 (programme principal, Shell, ServeurWEB, utils, Driver Ethernet).
- La bibliothèque CmdLine v20 et sa documentation.
- Les fichiers de la carte SD (`index.htm`, `ConfIP.htm`, fichiers CSV).
- Des captures d'écran de la vraie carte.

## Reproduit et approximé

Tout ce qui est écrit dans le code est reproduit. Ce qui dépend de la vraie carte ou du réseau (adresses DHCP, temps de `ping`, taille de la carte SD, chemin de `tracert`) est approximé et réglable dans la page. Le simulateur n'a pas été comparé en direct à une carte réelle. Il n'exécute pas le firmware d'origine : c'est une reproduction de son comportement en JavaScript.

## Réalisé avec l'aide d'une IA

Le code du simulateur et la rédaction du guide ont été réalisés avec l'aide de **Claude** (IA d'Anthropic), à partir des sources ci-dessus fournies par Leo.

## Auteur d'IoToS et licence

IoToS est l'œuvre de **Jean-Marc Biechy**, sous licence GNU LGPL v2.1 : [iotos.dsmynas.org](http://iotos.dsmynas.org/). Ce dépôt ne contient pas le firmware d'origine, seulement une reproduction indépendante de son comportement.

Ce simulateur reproduit des messages et un comportement issus d'IoToS : il est donc distribué sous la même licence, **GNU LGPL v2.1** (voir le fichier [LICENSE](LICENSE)).

## Utiliser

Ouvrir le site ci-dessus, ou télécharger `index.html` et l'ouvrir dans un navigateur : c'est un fichier unique, sans installation.
