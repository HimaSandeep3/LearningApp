## 🚀 GitHub-Azure Web Apps Integration: Automated CI/CD

This guide walks you through setting up **Continuous Integration/Continuous Deployment (CI/CD)** from your GitHub repository directly to an Azure Web App. This process eliminates manual publishing, ensuring your web app is automatically updated every time you push changes to the specified branch.

---

### Prerequisites

Before starting, ensure you have:

* An active **Azure subscription**.
* An existing **Azure Web App** (or create one).
* A **GitHub repository** containing your application code.

---

### Step-by-Step Integration Guide

Follow these steps within the **Azure Portal** to configure the automatic deployment:

#### 1. Locate the Deployment Center

1.  Navigate to the **Azure Portal**.
2.  Search for and select your target **Azure Web App** service.
3.  In the left-hand menu, under the **Deployment** section, select **Deployment Center**.

#### 2. Configure Deployment Settings

Under the **Settings** tab in the Deployment Center:

* **Source:** Select **GitHub** from the available options.
* **Build Provider:** Select **App Service Build Service** (recommended for beginners) or **GitHub Actions**.

#### 3. Authorize GitHub Access

* You will be prompted to sign in with your **GitHub Account**.
* Select your account, and then you must **Authorize AppService** to access your repositories.

#### 4. Specify Repository Details

Once authorized, select the specific details for the deployment:

* **Organization:** Choose your **GitHub organization** or personal account name.
* **Repository:** Select the **repository** you want to integrate.
* **Branch:** Select the deployment branch (e.g., **`master`**, **`main`**, or **`dev`**).

#### 5. Save the Configuration

* Click the **Save** button. Azure will initiate the first sync and deployment.

---

### ✨ Benefits of CI/CD Integration

| Benefit | Description |
| :--- | :--- |
| **Automation** | Eliminates the need for manual publishing. |
| **Continuous Deployment** | Any **`git push`** to the configured branch automatically triggers a new build and deployment. |
| **Version Control** | Ensures the code running in production is always the latest version committed. |

---

### 💡 What Happens When You Push Code?

1.  Code changes are pushed to your specified GitHub repository branch.
2.  GitHub notifies Azure (via a webhook).
3.  Azure takes the modified code.
4.  An **Automatic Build** runs.
5.  The code is **Deployed** to your Azure Web App. Your application is now updated!

---
