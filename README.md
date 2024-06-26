# Local Kubernetes Manifests

This repository contains Kubernetes manifest YAML files for deploying and managing services, deployments, and replicasets in a local Kubernetes cluster.

## Contents

- `deploy.yml`: YAML file for Kubernetes Deployments
- `service.yml`: YAML file for Kubernetes Services
- `replicaset.yml`: YAML file for Kubernetes ReplicaSets
- `config/`: ConfigMaps and Secrets (comming soon!)

## Prerequisites

- Kubernetes cluster (e.g., Kind, Docker Desktop with Kubernetes, or k3s)
- kubectl CLI tool

## Usage

1. Clone this repository:
   
   ```bash
    git clone https://github.com/shawakash/k8s/
    cd k8s
    ```
   
3. Apply the manifests to your local cluster:
   
    ```bash
    kind create clusters --config cluster.yml --name local
    kubectl apply -f deploy.yml
    kubectl apply -f service.yml
    ```
    
3. Verify the resources are created:

   ```bash
   kubectl get deployments
   kubectl get services
   kubectl get pods
   ```

4. Checkout ```localhost:30007```


## Customization

Modify the YAML files to suit your specific needs. Update image names, resource limits, and other configurations as required.


## Contributing

Feel free to submit issues or pull requests for improvements or additional manifests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
