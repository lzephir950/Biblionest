<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

You may also try the [Laravel Bootcamp](https://bootcamp.laravel.com), where you will be guided through building a modern Laravel application from scratch.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[WebReinvent](https://webreinvent.com/)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Jump24](https://jump24.co.uk)**
- **[Redberry](https://redberry.international/laravel/)**
- **[Active Logic](https://activelogic.com)**
- **[byte5](https://byte5.de)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

_____________________________________________________________________________________________

# 📚 Biblionest – Application de gestion de bibliothèque numérique

**Développé par Ludmilla ZEPHIR (2023 – 2025)**  
Gestion complète des livres, emprunts, pénalités et utilisateurs au sein d'une bibliothèque.

---

## 🚀 Présentation

**Biblionest** est une application web destinée aux employés de bibliothèque pour gérer efficacement les ouvrages, les emprunts, les pénalités de retard et les statistiques d’activité.  
Elle propose une interface intuitive, sécurisée, responsive, et intègre un tableau de bord interactif.

---

## 🎯 Fonctionnalités principales

- 🔍 **Livres**
  - Ajouter, modifier, supprimer et rechercher des livres
  - Classement par catégorie
- 🔄 **Emprunts**
  - Enregistrement et suivi des emprunts/retours
  - Détéction automatique des retards
- ⚠️ **Pénalités**
  - Application automatique des pénalités
  - Gestion du statut "payée/non payée"
- 👥 **Utilisateurs**
  - Authentification (Laravel Breeze)
  - Gestion des rôles : Admin / Employé
- 📊 **Dashboard**
  - Statistiques en temps réel (livres, emprunts, retards)
  - Export PDF des données

---

## 🧰 Stack Technique

| Élément       | Technologie              |
|--------------|--------------------------|
| Frontend     | Blade + TailwindCSS      |
| Backend      | Laravel 10 (PHP)         |
| Authentification | Laravel Breeze       |
| Base de données | MySQL                |
| Planificateur | Laravel Scheduler       |
| Hébergement  | O2Switch                 |
| Nom de domaine | [https://app.biblionest.fr](https://app.biblionest.fr) |

---

## 🗂️ Architecture MVC

**Modèles :** `Book`, `Category`, `Borrowing`, `Penalty`, `User`  
**Contrôleurs :** `BookController`, `BorrowingController`, `PenaltyController`, `UserController`  
**Vues Blade :** Pages pour les livres, emprunts, pénalités, dashboard

---

## 🛠️ Installation locale

```bash
git clone https://bitbucket.org/tonutilisateur/biblionest.git
cd biblionest
cp .env.example .env
composer install
php artisan key:generate
php artisan migrate
php artisan serve
