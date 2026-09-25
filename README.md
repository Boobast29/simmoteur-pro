# SimMoteur Pro

Simulateur pédagogique de gestion moteur essence, 100 % hors ligne : ouvrir `SimMoteur-Pro.html` dans un navigateur.

Moteur 1.6 16V à injection multipoint séquentielle, calculateur moteur, boîte automatique ou manuelle, réseau CAN. Public : CAP / Bac Pro Maintenance des véhicules.

## Ce que fait le simulateur

- **Un vrai calculateur.** Chaque capteur produit une tension à partir de la grandeur physique (CTN, piézorésistif, inductif 60-2, Hall, sonde lambda à saut de tension, potentiomètres doubles). Le calculateur décode ces tensions, contrôle leur plausibilité, enregistre les codes défaut et bascule sur des valeurs de substitution, comme un calculateur réel.
- **Stratégies réelles** : synchronisation dent manquante + AAC, régulation de ralenti (papillon + réserve d'avance), boucle fermée lambda avec corrections court et long terme, enrichissements (démarrage, froid, accélération, pleine charge), coupure en décélération, limiteur, anti-cliquetis, protection catalyseur, modes dégradés.
- **Conduite** : pédales qu'on enfonce à la souris ou au doigt (retour ressort), cale-pied, clavier. Boîte automatique P / R / N / D avec convertisseur, lock-up et kick-down, ou boîte manuelle 5 vitesses + marche arrière à embrayage piloté (grille en H, aide au passage des rapports).
- **Moteur en coupe animé** : pistons, soupapes, injection, étincelle et temps moteur de chaque cylindre, ratés visibles.
- **Oscilloscope 2 voies** : capteur régime, AAC, injecteurs, primaires de bobines, cliquetis, sondes lambda, MAP, pistes papillon et pédale, avec mesures automatiques.
- **Multiplexage CAN** : schéma du réseau, trames en direct avec décodage, trame dessinée bit par bit (vrai CRC-15 et bit stuffing), mesures atelier (60 Ω, tensions CAN-H / CAN-L), pannes de réseau.
- **Boîte automatique** : chaîne de transmission animée, lois de passage avec point de fonctionnement, tableau d'engagement, capteurs et électrovannes, cours.
- **Multimètre virtuel** : voltmètre (continu, alternatif) et ohmmètre sur 34 points (composants, continuité et isolement des faisceaux, réseau CAN). Mesure de résistance refusée contact mis.
- **Enregistreur** : 4 courbes au choix parmi 20 paramètres sur 3 min, lecture au survol, export CSV.
- **Analyse des gaz** : CO, CO₂, HC, O₂, NOx et λ calculé (Brettschneider), catalyseur qui chauffe et fenêtre catalytique, test pollution du contrôle technique guidé avec verdict.
- **Valise de diagnostic** : calculateurs présents, codes défaut avec contexte d'apparition, paramètres en direct, tests actionneurs.
- **Cartographies** : temps d'injection, avance, calcul du temps d'injection pas à pas, courbes couple / puissance.
- **29 missions atelier** : panne cachée, parole du client, indices, score.
- **Cours, glossaire, abréviations, contrôle technique** (repris de la version 7).
- **Son moteur** optionnel.

## Corrections par rapport à la version 7

La version 7 est conservée dans `archives/SimMoteur-Pro-v7.html`.

- Le régime et les grandeurs moteur étaient des formules « cibles » : le moteur est maintenant simulé (couple, inertie, remplissage, dépression, convertisseur, véhicule).
- Codes défaut incohérents avec leur description : P0118 était présenté comme un court-circuit « lit très chaud » (c'est un circuit ouvert qui lit très froid), P0117 inversé de la même façon, P0113 présenté comme un court-circuit.
- Pas de réseau CAN, pas de décodage des signaux : ajoutés.
