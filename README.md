# kubernetes

Kubernetes desde cero a experto

## Secrets

### Sustitución de secretos

1.- Crear configuración de secretos utilizando placeholder en un archivo yaml.

2.- Exportar variables de entorno.

- export username=USERNAME
- export password=PASSWORD

  3.- Realizar la sustución de valores en el archivo yaml.

- envsubst < SOURCE FILE > TARGET FILE

  4.- Aplicar

kubectl apply -f TARGET FILE
