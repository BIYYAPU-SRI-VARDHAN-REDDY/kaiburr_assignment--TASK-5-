# kaiburr_assignment--TASK-5-
Task 5. CI-CD Pipeline
Create a CI-CD pipeline for a sample application using any CI-CD tool of your choice like
Jenkins, Azure DevOps, Gitlab, Github Actions, AWS CodePipeline or any other tool of your
choice. Include a code build and a docker build step in your pipeline

# steps for the solution for task-5
CI/CD pipeline using GitLab CI/CD for the application you created in Task #3.

Prerequisites:

    A GitLab account and a GitLab project with your application code
    Docker and Kubernetes CLI installed on the build machine
    Access to a Kubernetes cluster

Steps:

    Create a .gitlab-ci.yml file in the root of your project repository
    Define the stages of your pipeline. For this example, we will use build, test, deploy.
    Define the jobs for each stage
    Define the script for each job
