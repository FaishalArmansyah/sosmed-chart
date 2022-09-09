# sosmed-app

1 - Push code
> git remote add origin https://github.com/FaishalArmansyah/sosmed.git

> git push -u origin main


2 - Build docker image
> docker build -t "image-name:tag" .

- example:
> docker build -t nubie13/web-profilpage:3 .


3 - Publish docker image to dockerhub
> docker login

> docker push "image-name:tag"

- example:
> docker push nubie13/web-profilpage:2

4 - Kubernetes Deployment
- source helm chart:
> https://github.com/FaishalArmansyah/sosmed-chart

- restore dump.sql (from git app source) to RDS.

- Deploy to namespace default (production)
> helm install sosmed sosmed-chart/ --values sosmed-chart/values.yaml

- Deploy to namespace staging
> helm install sosmed sosmed-chart/ --values sosmed-chart/values-staging.yaml -n staging
