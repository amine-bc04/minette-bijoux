# Minette Bijoux - E-Commerce de Bijoux Luxe

Bienvenue sur **Minette Bijoux**, une plateforme e-commerce moderne et élégante dédiée aux bijoux en rose gold.

## 🌟 Caractéristiques

- **Design Élégant**: Thème rose gold sophistiqué avec Tailwind CSS
- **Catalogue Produits**: Gestion complète des produits avec catégories
- **Panier d'Achat**: Système de panier intuitif
- **Authentification**: Inscription et connexion utilisateur
- **Gestion Commandes**: Suivi des commandes
- **Base de Données**: PostgreSQL avec Prisma ORM
- **API RESTful**: Endpoints pour tous les besoins e-commerce

## 🛠️ Stack Technologique

- **Frontend**: Next.js 14, React 18, Tailwind CSS
- **Backend**: Next.js API Routes
- **Base de Données**: PostgreSQL
- **ORM**: Prisma
- **Authentication**: JWT
- **Styling**: Tailwind CSS avec thème personnalisé

## 📋 Prérequis

- Node.js 18+
- PostgreSQL 12+
- npm ou yarn

## 🚀 Installation

### 1. Cloner le repository
```bash
git clone https://github.com/amine-bc04/minette-bijoux.git
cd minette-bijoux
```

### 2. Installer les dépendances
```bash
npm install
```

### 3. Configurer l'environnement
Créez un fichier `.env.local`:
```bash
DATABASE_URL="postgresql://user:password@localhost:5432/minette_bijoux"
JWT_SECRET="votre_clé_secrète_jwt"
NEXT_PUBLIC_API_URL="http://localhost:3000"
```

### 4. Initialiser la base de données
```bash
npx prisma migrate dev --name init
npx prisma db seed
```

### 5. Lancer le serveur de développement
```bash
npm run dev
```

Ouvrez [http://localhost:3000](http://localhost:3000) dans votre navigateur.

## 📁 Structure du Projet

```
minette-bijoux/
├── app/
│   ├── page.jsx                 # Page d'accueil
│   ├── layout.jsx               # Layout racine
│   ├── globals.css              # Styles globaux
│   ├── api/                     # API Routes
│   │   └── products/
│   ├── products/                # Pages produits
│   ├── cart/                    # Page panier
│   ├── auth/                    # Pages authentification
│   │   ├── login/
│   │   └── register/
│   └── favorites/               # Page favoris
├── components/
│   ├── Header.jsx               # En-tête
│   ├── Footer.jsx               # Pied de page
│   ├── Hero.jsx                 # Section héro
│   └── ProductCard.jsx          # Carte produit
├── lib/
│   └── prisma.js                # Configuration Prisma
├── prisma/
│   └── schema.prisma            # Schéma de base de données
├── public/                      # Fichiers statiques
├── package.json
├── tailwind.config.js
├── next.config.js
└── README.md
```

## 🎨 Couleurs du Thème

- **Rose Gold Principal**: `#B76E79`
- **Rose Gold Clair**: `#D4A5A5`
- **Rose Gold Foncé**: `#8B4F56`
- **Champagne**: `#F5E6D3`
- **Charcoal**: `#2C2C2C`

## 📚 Fonctionnalités Principales

### 1. Accueil
- Section héro attrayante
- Présentation des collections
- Produits vedettes

### 2. Catalogue
- Tous les produits avec filtres par catégorie
- Recherche et tri
- Affichage détaillé des produits

### 3. Panier
- Ajout/suppression de produits
- Modification des quantités
- Résumé de commande

### 4. Authentification
- Inscription utilisateur
- Connexion
- Gestion de profil

### 5. Commandes
- Historique des commandes
- Suivi du statut
- Reçus

## 🔐 Sécurité

- Mots de passe hashés avec bcryptjs
- Authentification JWT
- Protection CSRF
- Validation des données

## 💳 Paiement (À intégrer)

La plateforme est préparée pour l'intégration de **Stripe** pour les paiements en ligne.

## 📝 API Endpoints

### Produits
- `GET /api/products` - Récupérer tous les produits
- `POST /api/products` - Créer un produit (admin)

### Utilisateurs
- `POST /api/auth/register` - Inscription
- `POST /api/auth/login` - Connexion

### Commandes
- `GET /api/orders` - Récupérer les commandes de l'utilisateur
- `POST /api/orders` - Créer une commande

## 🚀 Déploiement

### Sur Vercel (Recommandé)
```bash
vercel deploy
```

### Sur un serveur personnalisé
```bash
npm run build
npm start
```

## 📄 Licence

Ce projet est sous licence MIT.

## 👩‍💼 Auteur

Minette Bijoux - Plateforme e-commerce de bijoux luxe

## 📞 Support

Pour toute question ou problème, contactez: info@minettebijoux.com

---

**Prochaines étapes**:
- ✅ Intégrer la base de données
- ✅ Ajouter plus de pages
- 🔄 Intégrer Stripe pour les paiements
- 🔄 Ajouter la gestion des avis
- 🔄 Implémenter un système de recommandations
- 🔄 Ajouter un panel d'administration
