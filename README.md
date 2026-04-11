# 🎧​ Spotify Hit Prediction 🎶​

<p align="left">
  <img src="image.png" width="380"/>
</p>

Dataset source : Hugging Face (Faizasb/spotify-tracks-dataset)

---

## 🎯​ Objectif du projet

Ce projet a pour objectif de prédire si un morceau peut devenir un "hit" à partir de ses 
caractéristiques audio extraites de Spotify.

---

## 💼​ Problématique métier

Comprendre les facteurs qui influencent le succès d’un morceau afin d'aider les maisons de disques à :
- optimiser la production musicale
- améliorer les stratégies marketing
- mieux positionner les artistes

---

## 📊​ Dataset

Le dataset contient **114 000 morceaux** issus de l’API Spotify.

Chaque morceau est décrit par des caractéristiques musicales telles que le caractère dansant, énergie, tempo, volume, etc.

---

## 📃​ Description des variables

### 💠​ Variables d’identification
- **track_id** : identifiant unique Spotify
- **track_name** : nom du morceau
- **artists** : artiste(s)
- **album_name** : album

---

### 💠​ Variables métier
- **popularity** : score Spotify basé sur les écoutes et interactions (0 à 100)

> ⚠️ IMPORTANT : cette variable a servi à créer la cible `is_hit`. Elle est donc exclue du modèle afin d’éviter de biaiser les prédictions.

- **duration_ms** : durée du morceau en millisecondes.
- **track_genre** : genre musical.

---

### 💠​ Variables audio
- **danceability** : capacité à danser (0 à 1).
- **energy** : intensité du morceau (0 à 1).
- **loudness** : volume sonore (dB).
- **speechiness** : présence de paroles parlées.
- **acousticness** : caractère acoustique.
- **instrumentalness** : présence ou non de voix.
- **liveness** : probabilité d’un enregistrement live.
- **valence** : positivité musicale (triste --> joyeux).
- **tempo** : vitesse du morceau (BPM).

---

### 💠​ Variables musicales techniques
- **key** : tonalité (0 à 11)

***C (Do), C# (Do#), D (Ré), D# (Ré#), E (Mi), F (Fa), F# (Fa#), G (Sol), G# (Sol#), A (La), A# (La#), B (Si)***

- **mode** : 0 = mineur (triste), 1 = majeur (joyeux)
- **explicit**: indique si le morceau contient des paroles explicites (True = Oui, False = Non ou inconnu)
- **time_signature** : mesure rythmique (exemple : 4/4)

---

## 🎯 Variable cible (target)

- `is_hit` : indique si le morceau fait partie des 20% les plus populaires
  - True : hit
  - False : non-hit

---

## ⚙️ Méthodologie

- Analyse exploratoire des données (EDA).
- Sélection des variables pertinentes.
- Prétraitement des données (encodage, normalisation).
- Modélisation avec XGBoost.
- Optimisation des hyperparamètres.
- Évaluation des performances du modèle.

## 🔍 Conclusions principales (EDA)

*Cette section sera complétée après la finalisation de l’analyse exploratoire des données.*


