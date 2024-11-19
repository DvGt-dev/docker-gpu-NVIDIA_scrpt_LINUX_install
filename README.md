# Installation et Configuration de Docker avec Support GPU NVIDIA sur Linux

Ce script Bash automatise l'installation et la configuration de Docker avec le support GPU NVIDIA sur un système Linux. Il est particulièrement utile pour les utilisateurs de WSL (Windows Subsystem for Linux) qui souhaitent utiliser Docker avec des capacités GPU.

## Fonctionnalités

1. **Suppression des paquets Docker existants** :

   - Le script commence par supprimer les paquets Docker existants pour éviter les conflits.

2. **Mise à jour des paquets système** :

   - Il met à jour les paquets système pour s'assurer que toutes les dépendances sont à jour.

3. **Installation des paquets nécessaires** :

   - Il installe les paquets nécessaires tels que `ca-certificates` et `curl`.

4. **Ajout de la clé GPG officielle de Docker** :

   - Le script ajoute la clé GPG officielle de Docker pour vérifier l'authenticité des paquets téléchargés.

5. **Ajout du dépôt Docker aux sources Apt** :

   - Il ajoute le dépôt Docker aux sources Apt pour permettre l'installation des paquets Docker.

6. **Installation de Docker** :

   - Le script installe Docker et ses composants associés, y compris `docker-ce`, `docker-ce-cli`, `containerd.io`, `docker-buildx-plugin` et `docker-compose-plugin`.

7. **Test de l'installation de Docker** :

   - Il exécute un conteneur de test pour vérifier que Docker est correctement installé.

8. **Étapes post-installation** :

   - Le script crée un groupe Docker et ajoute l'utilisateur actuel à ce groupe pour permettre l'exécution de Docker sans sudo.
   - Il crée et teste un volume Docker.

9. **Installation du toolkit de conteneur NVIDIA** :

   - Le script installe le toolkit de conteneur NVIDIA pour permettre l'utilisation des GPU NVIDIA avec Docker.

10. **Configuration du toolkit de conteneur NVIDIA** :

    - Il configure le toolkit de conteneur NVIDIA pour Docker, containerd et crio.
    - Il redémarre les services Docker et containerd pour appliquer les configurations.

11. **Test du toolkit de conteneur NVIDIA** :
    - Le script exécute un conteneur de test pour vérifier que le support GPU NVIDIA fonctionne correctement avec Docker.

## Utilisation

Pour utiliser ce script, suivez les étapes ci-dessous :

1. Clonez ce dépôt sur votre machine locale.
2. Exécutez le script avec les permissions sudo :
   ```bash
   sudo bash bash_script_wsl_docker_install_config.sh
   ```

## Remarques

- Assurez-vous que votre système est compatible avec Docker et le toolkit de conteneur NVIDIA.
- Ce script est conçu pour être utilisé sur un système Linux avec WSL. Il peut nécessiter des ajustements pour d'autres environnements.

## Contributions

Les contributions sont les bienvenues ! Si vous avez des suggestions ou des améliorations, n'hésitez pas à ouvrir une issue ou à soumettre une pull request.

## Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.
