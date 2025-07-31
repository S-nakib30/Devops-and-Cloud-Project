Objective: To implement a CI/CD pipeline using GitHub Actions, including testing, artifact management, and deployment to a self-hosted runner.

Application: https://github.com/roy35-909/OSTAD-Assignment-module-3

Steps:

Repository Setup:

Clone the provided repository.

Create a new repository on your GitHub account.

Add your new repository as a remote origin and push the code.

GitHub Actions Workflow:

Create a workflow file in .github/workflows.

Define two jobs: test and deploy.

Test Job:

Perform application testing.

Capture test results to a file.

Upload the test results as an artifact.

Deploy Job:

Ensure dependency on the test job.

Download the test results artifact.

Display the artifact content.

Deploy the Node.js application to a self-hosted runner.

Self-Hosted Runner Setup:

Configure a self-hosted runner.

Ensure the runner has the necessary environment.

Utilize runner labels as needed.

Deployment:

Create a deployment mechanism.

Integrate the deployment mechanism into the deploy job.

Deliverables:

Link to your GitHub repository (application and workflow file).

Evidence of successful workflow execution:

Test job results.

Artifact download and display.

Successful application deployment.

A description of challenges encountered and solutions.

## Prerequisites

- Node Version 22


### 1. For Run This Applications
```bash
# install packages
npm install 

# Testing The Applications
npm run check

# For Run the application
npm start
```


### Deployment Process
1. **Cleanup**: Removes existing process if running
   ```bash
   pm2 delete node-app || true
   ```

2. **Start Application**: Launches with absolute path
   ```bash
   pm2 start "./src/server.js" --name node-app
   ```

3. **Save Process List**: Persists PM2 configuration
   ```bash
   pm2 save
   ```

### About The Applications
1. **Route**: This Application has 2 route
   ```bash
   / # this will show a hello world page
   ```
      ```bash
   /api # this will response a json
   ```

2. **Default Port**: By Default this application will run on port 3000



