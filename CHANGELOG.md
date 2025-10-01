# Changelog

## [1.1.0] - 2025-10-01

### Sécurité
- Ajout de guards admin sur les routes d'administration
- Les mots de passe sont maintenant hashés avec password_hash()
- échappement HTML avec htmlspecialchars() dans les templates
- Requétes SQL préparées pour éviter les injections

### Docker
- Configuration de l'environnement avec Docker Compose
- Nginx + PHP-FPM + MySQL + PHPMyAdmin

### Documentation
- Guide de déploiement sur VPS Debian avec docker
- cours docker