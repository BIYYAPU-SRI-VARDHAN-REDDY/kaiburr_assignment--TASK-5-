# kaiburr_assignment--TASK-5-
Task 5. CI-CD Pipeline
Create a CI-CD pipeline for a sample application using any CI-CD tool of your choice like
Jenkins, Azure DevOps, Gitlab, Github Actions, AWS CodePipeline or any other tool of your
choice. Include a code build and a docker build step in your pipeline

# steps for the solution for task-5
CI/CD pipeline using GitLab CI/CD for the application you created in Task #3.

the steps to create the pipeline:

Create a Github repository for your application and push your code to it.

In your Github repository, create a new file named .github/workflows/main.yml. This file will contain the Github Actions workflow definition.

Add the uploaded code to main.yml file to define the workflow:

This workflow will be triggered on every push to the main branch. It contains a single job named build-and-deploy, which runs on an Ubuntu machine. The job contains the following steps:

    Checkout the repository
    Set up JDK 11
    Build the application using Gradle
    Build a Docker image using the Dockerfile in the repository and push it to your Docker registry
    Deploy the application to Kubernetes by applying the Kubernetes manifests in the k8s/ directory. The Kubernetes configuration is passed as a secret KUBE_CONFIG_DATA.


Create a Dockerfile in the root directory of your application with the following content:

        FROM openjdk:11-jdk

        WORKDIR /app

        COPY build/libs/*.jar app.jar

        EXPOSE 8080

        CMD ["java", "-jar", "app.jar"]

This Dockerfile will be used to build the Docker image for your application.

Create a k8s/ directory in the root directory of your application and create Kubernetes manifests for your application in that directory. You should have at least one Deployment manifest and one Service manifest.

Create a secret named KUBE_CONFIG_DATA in your Github repository settings with the value of your Kubernetes configuration. You can generate the Kubernetes configuration using kubectl config view --flatten.

Commit and push your changes to the Github repository. The CI/CD pipeline should be triggered automatically. You can monitor the progress of the pipeline in the Actions tab of your Github repository.

That's it! we now have a fully automated CI/CD pipeline for your application using Github Actions.
