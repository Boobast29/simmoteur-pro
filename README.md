# SimMoteur Pro

Simulateur pédagogique de gestion moteur essence, 100 % hors ligne : ouvrir `SimMoteur-Pro.html` dans un navigateur.

Cinq moteurs essence et diesel (atmosphériques, turbo wastegate, turbo à géométrie variable) plus un générateur de moteurs, calculateur moteur, boîte automatique ou manuelle, réseau CAN. Public : CAP / Bac Pro Maintenance des véhicules, BTS.

## Ce que fait le simulateur

- **Scène de conduite** : la voiture roule sur une route animée (pente, feux stop et de recul, phares). La fumée d'échappement suit les gaz calculés : suies, vapeur à froid. Ordinateur de bord : consommation instantanée et moyenne, trajet, réservoir, autonomie, panne sèche.
- **Route réaliste** : pente de −12 à +15 %, chargement jusqu'à 1 200 kg, carburant consommé en litres.
- **Côté jeu** : chronomètre 0-100 km/h et 400 m départ arrêté avec records par moteur, 20 badges, niveaux (d'Apprenti à Ingénieur motoriste), notifications, bandeau « Premiers pas ».
- **Côté pro** : fiche de diagnostic à remplir pendant chaque mission (défauts lus insérés automatiquement, copie en texte, bonus de points). Cas à plusieurs pannes. Espace professeur : composer un cas (moteur, pannes, parole du client, froid ou chaud) et générer un code à donner aux élèves.
- **Navigation** en 5 espaces : Conduire, Mesurer, Réseau & diag, Ingénierie, Former.

- **Moteurs** : essence 1.6 atmosphérique, 1.4 turbo, 2.0 sport, diesel 1.6 et 2.0 common rail turbo. Générateur de moteur (cylindrée, alésage/course, taux de compression, suralimentation, régimes) avec fiche technique calculée (couple, puissance, PME, vitesse de piston, consommation spécifique) et alertes de conception.
- **Modèle physique** : le couple vient de la masse d'air, du carburant brûlé et du rendement indiqué lié au taux de compression, moins les frottements et le pompage. Turbo avec inertie, remplissage variable selon le régime.
- **Diesel common rail** : préchauffage et post-chauffage, pression de rampe (doseur + régulateur), injection pilote / principale / post-injection, limiteur de fumées, régulateur de régime, turbo à géométrie variable, EGR régulée sur le débitmètre, filtre à particules et régénération, opacité.
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
- **Banc de puissance** : frein asservi en régime, mesure pleine charge palier par palier (couple, puissance, consommation spécifique, λ, suralimentation, T° échappement) comparée à la courbe théorique. Une panne se voit sur la courbe.
- **Combustion** : pression cylindre calculée (modèle une zone, loi de Wiebe, prémélange + diffusion en diesel), diagramme p-V, PMI, CA50, gradient de pression, rendement indiqué, cylindre par cylindre.
- **Cartographies** : temps d'injection, avance, calcul du temps d'injection pas à pas, courbes couple / puissance.
- **40 missions atelier** (essence, diesel, turbo) : panne cachée, parole du client, indices, score.
- **Cours, glossaire, abréviations, contrôle technique** (repris de la version 7).
- **Son moteur** optionnel.

## Corrections par rapport à la version 7

La version 7 est conservée dans `archives/SimMoteur-Pro-v7.html`.

- Le régime et les grandeurs moteur étaient des formules « cibles » : le moteur est maintenant simulé (couple, inertie, remplissage, dépression, convertisseur, véhicule).
- Codes défaut incohérents avec leur description : P0118 était présenté comme un court-circuit « lit très chaud » (c'est un circuit ouvert qui lit très froid), P0117 inversé de la même façon, P0113 présenté comme un court-circuit.
- Pas de réseau CAN, pas de décodage des signaux : ajoutés.
