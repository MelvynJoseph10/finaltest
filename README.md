# Project Workflow and CI/CD with Docker

## Continuous Integration and Continuous Deployment (CI/CD)

CI/CD is an automated software development approach that ensures quicker, consistent, and reliable delivery of applications.

## Docker

Docker is a platform for creating, delivering, and using apps inside containers, making them manageable and portable.

## Deployment Workflow

1. **EC2 Instance Setup:**
   - Created an EC2 instance with Linux 2.
   - Configured inbound and outbound rules for traffic.
   - Updated the server, installed necessary software like Docker, and started Docker on the instance.

2. **GitHub Repository:**
   - Created a GitHub repository to store code.
   - Uploaded webpages to the repository.

3. **Secrets and Variables:**
   - Created secrets for variables used in the Docker image.
   - Variables include EC2 host DNS, EC2 name, Docker account details, target directory, and keypair details.

4. **Dockerfile:**
   - Created a `Dockerfile` specifying the base image and setting up the web server with local directory files.

5. **Docker Image:**
   - Created a Docker image using a `.yml` file that configures the image using GitHub repository variables.

6. **GitHub Actions:**
   - Workflow can be viewed in GitHub Actions.
   - Testing CI/CD by pushing changes to the README.md file from GitHub Desktop.

## Issues Faced

1. **File Upload Limitation:**
   - Dragging and dropping files (webpages) was not possible in a single push for more than 100 files.
   - Solution: Used GitHub Desktop to clone the repository, uploaded files, committed changes, and pushed to GitHub.

2. **Caching Webpages:**
   - Changes were not reflecting even when using a new repo with a previously used EC2 instance.
   - Solution: Created a new EC2 instance to see changes reflected.

