## Construye la imagen de la aplicación Next.js
docker build -t mi-usuario/nextjs-app .
  
## Construye la imagen del servidor NGINX
cd nginx
docker build -t mi-usuario/nginx-app .
  
## Publica las imágenes en Docker Hub
docker push mi-usuario/nextjs-app
docker push mi-usuario/nginx-app

## Ejecutar archivos yaml
en el servidor que tiene kubernetes, entrar al directorio k8s
kubectl apply -f namespace.yaml
kubectl apply -f .