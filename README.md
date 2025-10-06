# 🎲 Dé 3D Animé

Un dé à six faces en 3D avec animation de rotation continue, créé uniquement avec HTML et CSS.

## 🌟 Fonctionnalités

- **Animation 3D fluide** : Rotation continue sur tous les axes
- **Design réaliste** : Chaque face affiche le bon nombre de points (1 à 6)
- **Effets visuels** : Bordures néon et effet de flou d'arrière-plan
- **Responsive** : S'adapte à différentes tailles d'écran
- **Performance optimisée** : Utilise uniquement CSS pour les animations

## 🎥 Aperçu

Le dé effectue une rotation complète en 8 secondes, montrant toutes ses faces avec leurs configurations de points traditionnelles :
- Face 1 : 1 point au centre
- Face 2 : 2 points en diagonale
- Face 3 : 3 points en diagonale
- Face 4 : 4 points aux coins
- Face 5 : 4 points aux coins + 1 au centre
- Face 6 : 6 points en deux colonnes

## 🚀 Installation et utilisation

### Prérequis
- Un navigateur web moderne supportant CSS3 et les transformations 3D

### Lancement local
1. Clonez ou téléchargez ce projet
2. Ouvrez le fichier `index.html` dans votre navigateur
3. Profitez de l'animation !

### Avec un serveur local
```bash
# Si vous utilisez Python
python -m http.server 8000

# Si vous utilisez Node.js
npx serve .

# Avec Laragon (déjà configuré)
# Accédez à http://localhost/3D_Dice
```

## 📁 Structure du projet

```
3D_Dice/
├── index.html      # Structure HTML du dé
├── style.css       # Styles CSS et animations
└── README.md       # Documentation du projet
```

## 🎨 Personnalisation

### Couleurs
Modifiez les variables CSS dans `style.css` :
```css
:root {
    --primary: #ff6b6b;    /* Couleur principale */
    --secondary: #4ecdc4;  /* Couleur des bordures */
}
```

### Vitesse d'animation
Changez la durée dans la règle `@keyframes` :
```css
.cube {
    animation: cubeRotate 8s infinite linear; /* Modifiez 8s */
}
```

### Taille du dé
Ajustez les dimensions :
```css
.cube {
    width: 200px;  /* Largeur */
    height: 200px; /* Hauteur */
}
```

## 🛠️ Technologies utilisées

- **HTML5** : Structure sémantique
- **CSS3** : 
  - Transformations 3D (`transform-style: preserve-3d`)
  - Animations (`@keyframes`)
  - Grid Layout pour le positionnement des points
  - Effets visuels (backdrop-filter, box-shadow)

## 🎯 Fonctionnalités techniques

- **Perspective 3D** : Utilise `perspective: 1000px` pour l'effet de profondeur
- **Six faces** : Chaque face est positionnée avec `translateZ` et `rotate`
- **Animation fluide** : Rotation sur les axes X, Y et Z simultanément
- **Points du dé** : Positionnés avec CSS Grid pour un alignement précis
