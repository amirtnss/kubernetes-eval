dans le dossier build:
docker build -t amir-react .
docker images

docker tag amir-react:latest amirs/amir-react:latest
docker push amirs/amir-react:latest

kubectl apply -f amir-front-service.yaml

kubectl create -f amir-react-deployment.yaml kubectl create -f amir-react-service.yaml


