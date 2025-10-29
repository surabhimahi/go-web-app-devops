**End-to-End DevOps CI/CD Pipeline — Automated Deployment using Argo CD, Helm, EKS, and GitHub Actions**

**Project Overview**

This project demonstrates a complete DevOps automation pipeline that builds, tests, and deploys an application from code to production using cloud-native tools.

It covers the entire CI/CD lifecycle — from source code integration to container deployment on AWS EKS — fully automated through GitHub Actions, Helm, and Argo CD.

**Architecture Workflow**
Developer → GitHub → GitHub Actions (CI) 
→ Docker Hub → Helm (values.yaml update)
→ Argo CD → AWS EKS (CD)

**Workflow Steps:**

  Code Commit (GitHub):
  
  Developer commits code to the main branch.
  
  Continuous Integration (GitHub Actions):
  
  The pipeline triggers automatically.
  
  Application is built into a Docker image.
  
  Image is tagged with a unique version (like v1.0.2).
  
  The image is pushed to Docker Hub.

**Continuous Delivery (Helm + Argo CD):**

  The Helm values.yaml file is automatically updated with the new image tag.
  
  Argo CD continuously monitors this Helm chart repo.
  
  Once it detects a change, it automatically deploys the new image to EKS.

**Cloud Deployment (AWS EKS):**

  Argo CD syncs the Kubernetes manifests.
  
  The updated pods are rolled out in the EKS cluster.
  
  New version is live within minutes — no manual intervention.

🛠️ Tech Stack
Category	Tool
Source Control	GitHub
Containerization	Docker
Orchestration	Kubernetes (EKS / Minikube)
Packaging & Versioning	Helm
Continuous Integration	GitHub Actions
Continuous Delivery	Argo CD
Cloud Provider	AWS
Local Testing	Minikube

**CI/CD Pipeline Overview**

  Stage	          Tool	                       Description
  Build	          Docker	                     Build and tag application image
  Test	          GitHub Actions	             Run unit/build checks
  Push	          Docker Hub	                 Push image with new tag
  Deploy	        Helm + Argo CD	             Auto-deploy new version to EKS cluster
  Monitor	        Argo CD	                     Detect drift, ensure GitOps sync

**How It Works**

  Push code to GitHub → triggers CI.
  
  GitHub Actions builds and pushes a Docker image.
  
  Helm chart’s values.yaml updates with new image tag.
  
  Argo CD detects change → syncs to EKS automatically.
  
  Application deployed instantly in the cluster.

**Key Learnings**

  Implemented CI/CD using GitOps principles.
  
  Built a self-healing deployment process using Argo CD sync.
  
  Automated version control for Helm and image updates.
  
  Used EKS for cloud orchestration and Minikube for local testing.
  
  Achieved complete automation from commit → deployment


(Example: GitHub → Docker Hub → Helm → Argo CD → AWS EKS)

**Connect with Me**

GitHub: github.com/surabhimahi

LinkedIn: linkedin.com/in/surabhi-mahendran-a4751a20a

Email: surabhimahendran040@gmail.com

🏁 Conclusion

This project demonstrates a real-world production-ready DevOps pipeline, integrating CI/CD, container orchestration, and GitOps automation.
It shows how a single code commit can automatically roll out to cloud infrastructure — achieving true Continuous Delivery.


