##### Azure App Service Web App Deployment - CI/CD Implementation

####### Project Overview
This project showcases the deployment of a modern Blazor web application (PaaS) using Microsoft Azure App Service. The focus is on demonstrating a complete DevOps lifecycle, from local development to automated cloud deployment, leveraging Azure Repos and Azure Pipelines.

**Live Application URL:** [https://vhido.azurewebsites.net/](https://vhido.azurewebsites.net/)

###### Technologies & Architecture
- **Platform:** Microsoft Azure App Service (PaaS)
- **Runtime Stack:** .NET 10.0
- **Pricing Tier:** Free F1 (Hosting plan)
- **Operating System:** Windows
- **Version Control:** Azure Repos (Git)
- **CI/CD:** Azure Pipelines (YAML)

---

###### Project Goals & Implementation Steps

###### 1. Create App Service Plan & Provision Web App
The App Service Plan was set up using the **Free F1** tier, which provides a shared infrastructure suitable for learning and proof-of-concept applications. The web app was provisioned using the **.NET 10.0** stack.

###### 2. Local Development & First Deployment (Portal)
A Blazor application was developed locally and successfully hosted on a local development server.
- **Initial Portal Deployment:** The app was initially deployed using the Azure Portal. The default "Your web app is running..." placeholder page was visible until the code was uploaded.

###### 3. Deployment Strategy: Visual Studio & Git Integration
To establish version control, the project was connected to **Azure Repos**.
- **Visual Studio Publish:** Direct integration with Azure App Service allowed for a seamless "Publish" workflow directly from the IDE.
- **Git Push:** The code was pushed to the `main` branch of the Azure Repo, which serves as the source of truth for the application.

###### 4. Environment Settings (Configuration)
All application settings and configurations were managed within the application source code. For this tier, no specific environment variables or custom application settings were configured via the Azure portal's Configuration blade.

###### 5. CI/CD Continuous Deployment (Azure Pipelines)
A **YAML-based pipeline** was created in Azure DevOps to automate the build and release process. The pipeline successfully enables automated deployments on every push to the `main` branch.
- **Stages:** Build Stage and Deploy Stage.
- **Outcome:** The app successfully updates automatically without manual intervention.

###### 6. Verify Accessibility & Zero-Downtime
The web application is successfully accessible via its public URL over HTTPS.
- **Note:** Due to the **Free F1** tier restrictions, Deployment Slots (staging, testing) are not available. However, the automated pipeline updates the production environment effectively.

###### 7. Review Monitoring and Scaling
Basic monitoring is available via the Azure Portal. Scaling is limited on the Free tier; to scale horizontally, an upgrade to a higher tier (e.g., Basic or Standard) would be required.

---

#####  Deployment Methods Executed
1. **Manual Upload:** Azure Portal.
2. **IDE Integration:** Visual Studio Publish profile.
3. **Automated CI/CD:** Azure Pipelines (Build & Release via YAML).