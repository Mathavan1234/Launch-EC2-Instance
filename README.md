# Launch-EC2-Instance
This is a repository to Deploy a static website hosted on an **EC2 instance** using Terraform.

---

## 📁 Deploy Static Website using CodeBuild & Terraform

### Overview
- Automate the deployment of a static website hosted on an EC2 instance.
- The pipeline is triggered whenever a new commit is pushed to the GitHub repo.

### Steps

1. **Create IAM User for CodeBuild**
   - Full admin access.
   - Generate AWS CLI credentials (Access Key + Secret).

2. **Terraform Script**
   - Write infrastructure as code to provision the EC2 instance.

3. **Shell Scripts**
   - `install-terraform.sh`: Installs Terraform.
   - `apply-terraform.sh`: Applies the Terraform configuration.
   - `configure-named-profile.sh`: Sets up AWS CLI named profile.

4. **Buildspec**
   - `buildspec.yml`: Defines CodeBuild phases (install, build, post_build).

5. **Create CodeBuild Project**
   - Link GitHub repo with a Personal Access Token (PAT).
   - Add environment variables: AWS credentials, region, profile.
   - On push, CodeBuild runs the Terraform script and provisions the EC2 instance.

---

## ✅ Project Status

- ✅ EC2 Instance is running and hosting the static website.


