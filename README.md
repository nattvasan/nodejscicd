# nodejscicd

Variables needed:
  - SONAR_URL
  - SONAR_KEY
  - USERNAME -- Username of the docker registry
  - CI_REGISTRY -- Docker registry URL
  - REGISTRY_PASSWORD -- Docker registry password

We have four stages 
  - build
  - test
  - scan
  - deploy

Once the build, test, code scan stages are successful. We have implemented stage to build the docker image, push it to our registry and deploy the application in Kubernetes cluster. 

.build-image.gitlab-ci.yml
.kube-deploy.gitlab-ci.yml

After docker image build is successful, script to update "service-deployment.yaml" image's field with the latest commit code i.e tag name used to build docker images.

