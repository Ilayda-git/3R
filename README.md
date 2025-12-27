# Mobilité professionnelle et salaires – Analyse économétrique

**Auteurs** : Chloé Martin · Ilayda Yilmaz · Thomas Barat  

---

## Objectif

Ce projet vise à analyser l’impact des **différentes formes de mobilité professionnelle** (intra-entreprise, inter-entreprise et géographique) sur les **dynamiques salariales**, en mettant l’accent sur les **différences de trajectoires entre les femmes et les hommes**.  
L’enjeu est d’identifier dans quelle mesure la mobilité constitue un **investissement en capital humain** et comment ses rendements varient selon les profils individuels.

---

## Données

- **Source** : Enquête Emploi Insee  
- **Taille initiale** : 90 088 individus · 689 variables  
- **Échantillon final** : ~29 000 individus · 16 variables sélectionnées  
- **Types de données** : numériques et catégorielles  
- **Variables clés** :
  - `salmee` : salaire mensuel (log-transformé)
  - `mment` : mobilité professionnelle (intra / inter / autres)
  - `age`, `age²`, `ancienneté`
  - `diplôme`, `CSP`, `secteur`, `région`, `sexe`

Un travail approfondi de **nettoyage des données** a été réalisé, notamment sur la gestion des **valeurs manquantes**, très présentes pour les variables de salaire et de mobilité.

---

## Cadre théorique

Le projet s’appuie sur :
- la **théorie du capital humain** (Becker 1975 ; Mincer 1974),
- les travaux de **Simonnet (1996)** sur la mobilité professionnelle et les différences de genre,
- les apports de **Margirier (2006)** sur la mobilité géographique et le biais de sélection.

La mobilité est interprétée comme un mécanisme d’ajustement permettant une meilleure valorisation du capital humain, sous réserve de coûts économiques et sociaux.

---

## Méthodologie

1. **Analyse descriptive**
   - Étude de la distribution des salaires, âges, diplômes, ancienneté
   - Analyse de la structure socio-professionnelle et sectorielle
   - Mise en évidence d’une forte hétérogénéité salariale

2. **Modélisation économétrique**
   - Estimation de modèles **MCO (moindres carrés ordinaires)**
   - Spécifications séparées pour :
     - l’échantillon total
     - les hommes
     - les femmes
   - Variable dépendante : `ln(salaire)`
   - Variables explicatives : âge, ancienneté, diplôme, mobilité, CSP, région, secteur

3. **Interprétation**
   - Analyse des rendements du diplôme et de l’expérience
   - Comparaison des effets de la mobilité selon le genre
   - Discussion des limites liées à l’**endogénéité** et au **biais de sélection**

---

## Résultats principaux

- Le salaire suit un **profil concave avec l’âge**, avec un plafonnement plus précoce pour les femmes.
- Le **diplôme** génère des rendements croissants, plus élevés chez les femmes.
- La **mobilité inter-entreprise** est associée à un **gain salarial d’environ 10 %**, pour les hommes comme pour les femmes.
- L’**absence de mobilité** ou certaines formes atypiques (travail familial) sont plus pénalisantes pour les femmes.
- Le secteur public réduit les écarts salariaux de genre par rapport au secteur privé.

Les résultats sont globalement cohérents avec la littérature, mais doivent être interprétés avec prudence en raison de l’absence de correction explicite de l’endogénéité.

---

## Limites et perspectives

- Fort taux de **données manquantes** pour la variable de mobilité
- Absence de correction du biais de sélection dans les estimations MCO
- Perspectives :
  - modèles à correction de sélection (Heckman),
  - données longitudinales,
  - meilleure prise en compte des **coûts non monétaires** de la mobilité.

---

## Technologies utilisées

- **Langage** : R, Power BI

---
