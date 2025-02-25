Helm Charts Repository

Overview

This repository contains a collection of Helm charts for deploying various applications and services. The charts are designed to be reusable and configurable for different environments.

Prerequisites

Before using these Helm charts, ensure you have the following installed:

Helm (version >= 3.0.0)

Kubernetes cluster (v1.19+ recommended)

Proper cloud provider authentication (if deploying to a managed Kubernetes service)

Repository Structure

├── charts/             # Collection of Helm charts
│   ├── common/         # Reusable Helm chart components
│   ├── nginx/          # Nginx Helm chart
│   ├── postgres/       # PostgreSQL Helm chart
│   └── redis/          # Redis Helm chart
├── templates/          # Common Helm templates
├── values.yaml         # Default values for Helm charts
└── README.md           # Project documentation

Usage

Clone the repository

git clone https://github.com/your-username/your-helm-repo.git
cd your-helm-repo

Add the repository to Helm

helm repo add my-charts https://your-helm-repo-url

Install a chart

helm install my-release my-charts/nginx --values values.yaml

Upgrade a release

helm upgrade my-release my-charts/nginx --values values.yaml

Uninstall a release

helm uninstall my-release

Configuration

Each Helm chart has customizable values. Modify values.yaml or override them with command-line flags:

helm install my-release my-charts/nginx --set replicaCount=3

Best Practices

Use values files to manage configurations per environment.

Store Helm charts in a remote repository for easier version control.

Enable Helm secrets for managing sensitive data.

Use Helm linting and validation before deploying.

Contributing

Feel free to fork this repository and submit a pull request with improvements or new charts.


Author

Adith Mohan
