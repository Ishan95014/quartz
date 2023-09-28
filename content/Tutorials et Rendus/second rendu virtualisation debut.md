# Compte-rendu du TP2 : Découverte de Kubernetes

## Objectifs
- Découverte du cluster Kubernetes avec Minikube
- Utilisation de la commande `kubectl`
- Déploiement de ressources et services
- Utilisation de fichiers YAML pour la configuration

## Activités Réalisées

### Initialisation du Cluster avec Minikube
- Démarrage de Minikube:

```
26/09/2023 09:54:44 minikube start
```

- Vérification de l'état de Minikube:

```
26/09/2023 10:03:33 minikube status
```

### Exploration du Cluster
- Liste des nœuds:
```
26/09/2023 10:07:07 kubectl get nodes
```

- Liste des services:

```
26/09/2023 10:07:26 kubectl get services
```

### Déploiement d'une Application (nginx)

- Création du déploiement:

```
26/09/2023 10:08:54 kubectl create deployment zorgbots --image=nginx
```

- Liste des déploiements, ReplicaSets et Pods:

```
26/09/2023 10:09:10 kubectl get deployment

26/09/2023 10:09:26 kubectl get replicaset
26/09/2023 10:09:32 kubectl get pod
```

### Exposition d'un Service
- Exposition du service nginx:

```
26/09/2023 10:14:44 kubectl expose deployment zorgbots --type=NodePort --port=8080 --target-port=80
```

- Vérification de l'exposition du service:

```
26/09/2023 10:23:11 minikube service zorgbots --url
```
### Mise à l'Échelle du Déploiement
- Mise à l'échelle du déploiement nginx:
```
26/09/2023 10:16:56 kubectl scale deployment zorgbots --replicas=3
```

- Vérification des Pods:
```
26/09/2023 10:17:17 kubectl get pods
```
### Déploiement avec YAML

- Application de la configuration depuis un fichier YAML:

```
26/09/2023 11:04:30 kubectl apply -f nginx-dep.yaml
```
