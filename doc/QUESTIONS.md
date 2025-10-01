# Questions

## 1) Expliquer la procédure pour réserver un nom de domaine chez OVH avec des captures d'écran (arrêtez-vous au paiement)

Je vais sur le site d'OVH et je cherche si le nom de domaine que je veux est disponible. Si oui je peux le commander en choisissant la durée et quelques options de base. Ensuite je créé un compte si j'en ai pas déjà un et je valide le panier. Je m'arrête là avant de payer, sachant qu'un domaine coûte entre 6 et 15€ par an selon l'extension.

## 2. Comment faire pour qu'un nom de domaine pointe vers une adresse IP spécifique ?

Il faut modifier la configuration DNS du domaine. Dans l'interface OVH je vais dans la gestion de mon domaine et je créé ce qu'on appelle un enregistrement A qui fait le lien entre le nom de domaine et l'IP du serveur. Après ça peut prendre quelques heures avant que ça fonctionne partout à cause de la propagation DNS.

## 3. Comment mettre en place un certificat SSL ?

J'utilise Let's Encrypt parce que c'est gratuit et automatique. Y'a un outil qui s'appelle Certbot qui s'occupe de tout, il génère le certificat et configure le serveur web pour utiliser le HTTPS. Le certificat doit être renouvelé régulièrement mais ça peut être automatisé avec une tâche planifiée.
