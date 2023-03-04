# LAB 0 informations supplémentaires

Une fois que votre environnement de travail est setup en suivant les infos dans le cours, vous pouvez vous passer de l'utilisation de MobaXterm pour accéder à vos services de type node port ou au services exposés via port forwarding.

Pour ce faire, il faut customiser le démarrage de minikube et d'esposer les ports de votre machine.

## Start minikube
Pour le demarrage de minikube, utiliser la commande

`
minikube start --apiserver-ips=<ip-machine-virtuelle> –driver=none –kubernetes-version v1.20.2
`

Votre machine virtuelle et votre machine réelle doivent communiquer ensemble pour que cette manip fonctionne. Vous devez configurer un acces par pont sur la carte réseau de votre machine virtuelle.

## Firewall config
Vu que l'on est dans un env de développement on peut juste désactiver le firewall de Centos 7 pour pourvoir accéder à tous les ports de notre machine virtuelle

`
sudo systemctl stop firewalld
`
