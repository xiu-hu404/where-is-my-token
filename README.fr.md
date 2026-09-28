# Where is my token

[简体中文](README.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [日本語](README.ja.md) · **Français** · [Deutsch](README.de.md) · [한국어](README.ko.md)

[Télécharger la bêta macOS](https://github.com/xiu-hu404/where-is-my-token/releases/tag/v0.1.0-beta.4) · [Signaler un problème ou proposer une amélioration](https://github.com/xiu-hu404/where-is-my-token/issues)

**Suivez vos tokens et estimez vos coûts Codex sur macOS.**

La tâche n’est pas terminée, mais le compteur de tokens continue de monter. Où passent-ils ? Where is my token garde sous vos yeux la consommation de chaque conversation, le taux de succès du cache et la part du contexte utilisée. Une faible réutilisation du cache ou des journaux qui grossissent vous donnent des pistes pour revoir votre façon d’utiliser Codex.

![Exemple de travail dans Codex avec le suivi des tokens au-dessus de la conversation](docs/images/codex-workflow-en.jpg)

L’espace de travail Codex est une illustration. La barre provient de l’interface réelle ; la conversation et les chiffres sont des exemples. Les visuels de présentation sont en anglais.

## À quoi ça sert ?

- **Comprendre sa consommation.** Consultez le total de chaque conversation ou projet sans fouiller dans les journaux.
- **Repérer ce qui mérite un examen.** La barre vous signale un taux de succès du cache durablement bas ou une croissance soutenue des journaux.
- **Faire le point sur les coûts.** Estimez le montant aux tarifs API connus et retrouvez, sur un ticket, la consommation par modèle et les tours les plus gourmands.
- **Garder la main.** Les calculs sont locaux. Aucun appel de modèle supplémentaire, aucun message ajouté à la conversation, aucun changement automatique de modèle ni suppression de fichiers.

Épinglez une conversation, suivez les nouveaux messages utilisateur envoyés après l’activation du suivi, ou affichez le total du projet associé. Le moniteur démarre et s’arrête avec les fenêtres de Codex. Il suit la langue de macOS et propose sept langues : français, anglais, chinois simplifié et traditionnel, japonais, allemand et coréen. ChatGPT, Codex et les noms des modèles conservent leur nom d’origine.

## Tickets et alertes

![Ticket récapitulant les tokens, la durée, le coût estimé aux tarifs API et les principaux tours](docs/images/receipt-showcase-en.jpg)

Créez un ticket quand vous en avez envie. Choisissez une conversation ou un projet, les N tours les plus consommateurs ou tous les tours, un papier de 58 ou 80 mm, et l’affichage ou non du montant API. L’impression est désactivée par défaut. Une fois activée, vous pouvez choisir un appareil Bluetooth classique déjà jumelé ou une imprimante système, puis confirmer dans la fenêtre d’impression de macOS.

![Point orange signalant un faible taux de succès du cache et texte de son infobulle](docs/images/advisory-showcase-en.jpg)

Le point orange signale une faible réutilisation récente du cache. Le texte de son infobulle est reproduit à droite. C’est une piste à examiner, pas la preuve que des tokens ont été gaspillés.

## Installation et arrêt

Version actuelle : **0.1.0-beta.4**. Nécessite un **Mac avec puce Apple et macOS 15 ou ultérieur**. L’environnement d’exécution est inclus : inutile d’installer Python ou Xcode. 

Si vous disposez du paquet de test :

1. Décompressez `Where-is-my-token-0.1.0-beta.4-macOS-arm64.zip`.
2. Ouvrez `Where is my token.app` et choisissez l’installation avec démarrage.
3. Pour désactiver le moniteur, lancez `Disable.command`. Vos réglages et statistiques sont conservés.

Fermer la dernière fenêtre normale de Codex arrête le moniteur et la collecte ; ouvrir une nouvelle fenêtre les relance. Réduire une fenêtre ne les arrête pas. Un petit processus reste en arrière-plan pour détecter la réouverture. Le bouton × replie la barre en un bouton W·T ; cliquez dessus pour la réafficher.

Cette bêta ne dispose pas encore d’une signature Developer ID ni de la notarisation Apple. C’est un outil local qui accompagne Codex, pas un ZIP à importer dans son dossier de plugins. Aucun hook Codex n’est à activer.

## Confidentialité et limites actuelles

- Seules les statistiques nécessaires sont conservées à partir des enregistrements Codex accessibles sur ce Mac. Les conversations complètes ne sont pas copiées et les statistiques ne sont pas envoyées en ligne. Les données résident dans `~/Library/Application Support/Where is my token/`.
- Le suivi se base sur les nouveaux messages envoyés, pas sur la conversation sélectionnée à l’écran ni sur les brouillons.
- Le taux de succès du cache ne mesure pas la justesse des réponses. La quantité de contexte utilisée ne permet pas de juger sa pertinence ; une occupation élevée ne déclenche pas d’alerte à elle seule.
- Les données manquantes apparaissent sous la forme « — ». Le moniteur ne déduit pas un solde de tokens du forfait et ne couvre que les enregistrements collectés localement.
- Le montant API est une estimation, pas un prélèvement réel. La saisie des frais d’abonnement et leur répartition par mois passent actuellement par les commandes de gestion ; les tickets de l’interface affichent principalement le montant API.
- Les alertes sur les journaux reposent sur la taille et la date de modification des fichiers, pas sur une mesure des écritures physiques sur le disque. Les conseils sur le moment d’exécuter les tests ne sont pas encore intégrés à la barre.
- L’impression Bluetooth nécessite une file d’impression macOS compatible. Les protocoles propres aux fabricants et l’impression sur papier restent à vérifier. Le démarrage et l’arrêt ont été testés avec une fenêtre isolée ; la compatibilité avec les différentes versions de Codex reste à valider.

## Licence et retours

Logiciel gratuit, à code source fermé, réservé à un **usage non commercial**. L’utilisation interne en entreprise n’est pas autorisée. La copie, la modification, le reconditionnement et la redistribution sont permis gratuitement à des fins non commerciales. La revente, l’inclusion dans une offre payante et la facturation de l’accès aux fonctions du logiciel sont interdites. Consultez la [licence](LICENSE).

[Signaler un problème ou proposer une amélioration](https://github.com/xiu-hu404/where-is-my-token/issues) · [Confidentialité](docs/privacy.md) · [Mentions relatives aux tiers](THIRD_PARTY_NOTICES.md)
