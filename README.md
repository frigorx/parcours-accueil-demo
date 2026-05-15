# Parcours d'accueil — Lycée Professionnel

> **Maquette de démonstration** — Document non officiel destiné à présentation/validation par direction d'établissement.

## Objet

Application web autonome (un seul fichier HTML) destinée à l'accueil des nouveaux élèves d'un lycée professionnel. Trois parcours quiz progressifs valident la prise de connaissance du règlement intérieur, des règles de vie, et de la posture professionnelle attendue (sécurité, atelier, PFMP, comportement numérique).

## Caractéristiques

- **65 questions** réparties sur 3 parcours (15 + 25 + 25)
- **Seuils ≈ 92 %** par parcours (objectif ≥ 90 %)
- **Attestation imprimable** avec engagement explicite, double signature (élève + responsable légal pour les mineurs), score précis, référence horodatée unique
- **100 % local** : aucune donnée transmise, aucun appel externe, aucun cookie
- **QR code généré localement** (lib `qrcode-generator` inline, MIT)
- **Signature tactile** sur canvas pour élève et responsable légal
- **RGPD by design**

## Couverture pédagogique

### Parcours 1 — Entrer au lycée professionnel (15 Q)
Ponctualité, respect, téléphone, tenue, École Directe, sanctions de base.

### Parcours 2 — Règles de vie et règlement intérieur (25 Q)
RI, sanctions, harcèlement et cyberharcèlement, droit à l'image, laïcité, vol/racket, fumer & vapoter (cigarette/puff/e-cigarette), alcool/stupéfiants, espace restauration, absentéisme, harcèlement sexiste, discriminations.

### Parcours 3 — Sécurité, comportement et posture professionnelle (25 Q)
EPI, machines, alarme incendie, extincteurs, produits chimiques, PFMP, CCF (triche, absences), plagiat / IA, matériel prêté, convention de stage, discrimination en milieu pro.

## Architecture technique

- 1 fichier HTML autonome (~67 Ko)
- Vanilla JS, aucun framework
- CSS variables pour la charte
- `qrcode-generator` v1.4.4 inline (MIT, K. Arase)
- Canvas API pour signatures
- `window.print()` natif pour impression

## Utilisation

Ouvrir `index.html` dans un navigateur moderne (Chrome, Firefox, Edge, Safari) ou via la version en ligne (GitHub Pages).

## Personnalisation par l'établissement

Avant déploiement officiel, compléter :
- En-tête : nom de l'établissement, adresse, logo officiel
- Liste des classes / formations (objet `CLASSES` en JS)
- Mention RGPD : responsable de traitement (nom + adresse complète)
- Le cas échéant : intégrer le PDF du règlement intérieur officiel dans la modale `showRI()`

## Statut

Maquette en attente de validation par la direction de l'établissement.

## Licence

Code source librement adaptable pour usage pédagogique en lycée professionnel.
