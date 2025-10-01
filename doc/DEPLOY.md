# Procédure de Déploiement

Décrivez ci-dessous votre procédure de déploiement en détaillant chacune des étapes. De la préparation du VPS à la méthodologie de déploiement continu.

## Préparation du VPS

VPS Debian 12 fourni par l'école (IP : 172.17.4.26)

J'ai installé Docker + Docker Compose pour containeriser l'application. j'ai installé Apache2 par erreur en pensant que j'en avais besoin pour docker, je l'ai arrêté car il occupait le port 80.

```bash
ssh root@172.17.4.26
apt update && apt upgrade -y
apt install -y docker-ce docker-ce-cli containerd.io git
systemctl stop apache2 && systemctl disable apache2
cd /var/www
git clone https://github.com/Metz-Numeric-School/habit-tracker-buggy-web-app-bloc-4-dfs-2025-bis-Clemboubou.git monprojet
cd monprojet
```

## Méthode de déploiement

J'utilise Docker avec 4 conteneurs :
- **Nginx** (port 80) : serveur web
- **PHP 8.3-FPM** : exécute le code PHP
- **MySQL 5.7** : base de données
- **PHPMyAdmin** (port 8080) : admin de la base

Nginx reçoit les requêtes et les transmet à PHP qui se connecte à MySQL. Tout communique via un réseau Docker interne (`habittracker-network`).

voilà, j'ai aussi perdu du temps sur la clé ssh personnel de github qu'on doit mettre en fait à la place de password
