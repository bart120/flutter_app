# 📱 TP Flutter – CityWeather (2 jours, binôme)

## 🎯 Objectif
Développer une application Flutter fonctionnelle permettant :

1. **Recherche de ville** via l’API ouverte *Open-Meteo Geocoding*.  
2. **Affichage de la météo** de la ville via *Open-Meteo Forecast*.  
3. **Utilisation du GPS** du téléphone (lat/lon en temps réel).  
4. **Ouverture de l’application de cartes** (Google Maps / Plans) via `url_launcher`.  
5. Présentation de l’application le **Jour 2** (10 minutes par binôme).
6. **Si le groupe est composé de 3 étudiants** :  
Ajouter une fonctionnalité **“Villes favorites”** persistée en **SQLite** :
   - possibilité d’**enregistrer jusqu’à 10 villes** en favoris,
   - affichage d’une **liste des villes favorites**,
   - possibilité de supprimer un favori.

---

## 🌐 API utilisées (gratuites, sans clé)

### 🔎 Géocodage (recherche de ville)
https://geocoding-api.open-meteo.com/v1/search?name=Paris&count=5&language=fr

### 🌤️ Météo
https://api.open-meteo.com/v1/forecast?latitude=48.85&longitude=2.35&current=temperature_2m,wind_speed_10m

---

## 🧰 Packages Flutter obligatoires

```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^1.2.0
  geolocator: ^12.0.0
  url_launcher: ^6.3.0
```

---

## 🧱 Architecture conseillée

```
lib/
├─ main.dart
├─ models/
│  ├─ city.dart
│  └─ weather.dart
├─ services/
│  └─ api_service.dart
├─ pages/
│  ├─ search_page.dart
│  └─ city_detail_page.dart
└─ widgets/
   └─ (optionnel)
```

---

## 🗓️ Déroulé pédagogique

### 📅 Jour 1 – API, recherche, navigation

- Création projet : `flutter create cityweather`
- Appel API geocoding
- Écran de recherche (TextField + FutureBuilder)
- Résultats cliquables
- Navigation vers détails

---

### 📅 Jour 2 – GPS, Maps, finition & présentation

- Localisation GPS (geolocator)
- Météo de la position actuelle
- Ouverture dans Maps (url_launcher)
- Design + gestion erreurs
- Présentation de 10 minutes

---

## 🧾 Barème (40 points)

### 🔧 Réalisation technique – 20 pts
- API geocoding + météo : 4  
- Météo position actuelle : 4  
- GPS + permissions : 3  
- Maps : 3  
- Code propre : 3  
- UX / erreurs : 3  

### 🎤 Présentation orale – 20 pts
- Pitch : 5  
- Démo : 5  
- Répartition binôme : 3  
- Explication technique : 5  
- Respect du temps : 2  

---

## 📦 Livrables
- Code complet
- Démo en fin de Jour 2
- README.md (objectifs, installation, difficultés)
