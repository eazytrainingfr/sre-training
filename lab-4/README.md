# TP-4 informations supplémentaires

## Rajouter le repo bitnami avant l'installation de wordpress

```
helm repo add bitnami <https://charts.bitnami.com/bitnami>
helm repo list
```

## update version wordpress

La version 8.1.0 n'existe plus pour le chart wordpress chez bitnami. Utilisez la version **15.2.44** pour l'installation

`
helm install wordpress bitnami/wordpress -f wordpress-values.yaml --version 15.2.44
`
