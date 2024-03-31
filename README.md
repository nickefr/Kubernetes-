# Kubernetes- cheatsheet⚙️
## Commands for GitHub README

| Emoji | Description |
|-------|-------------|
| 🚀 | Kubernetes |
| ⚙️ | K8s |
| 🐳 | Docker |
| 🏗️ | Pods |
| 🌐 | Services |
| 🔍 | ReplicaSets |
| 🧩 | Deployments |
| 🔧 | ConfigMaps |
| 🔒 | Secrets |
| 🔗 | Ingress |
| 📦 | Helm |
| 🛠️ | Operators |
| 🔥 | Rolling updates |
| 🔄 | Rolling back |
| 📊 | Metrics |
| 📡 | Load Balancer |
| 🖥️ | Nodes |
| 🌱 | Persistent Volumes |
| 💾 | Persistent Volume Claims |
| 📝 | Annotations |
| 📋 | Labels |
| 🔐 | RBAC |
| 🕸 | Namespaces |
| 🛡️ | Security Policies |
| 📡 | Network Policies |
| 🚥 | Pod Disruption Budgets |
| 🔁 | CronJobs |
| ⏰ | Scheduling |
| 📈 | Horizontal Pod Autoscaling |
| 📉 | Vertical Pod Autoscaling |
| 🔀 | StatefulSets |
| 🎛️ | Custom Resource Definitions (CRDs) |
| 📦 | Operators |
| 📡 | Service Mesh (Istio, Linkerd) |
| 🔒 | Security Contexts |

You can copy and paste this table directly into your README file on GitHub. Adjust the formatting as needed!

### Basic Commands

| Command | Description |
|---------|-------------|
| `$ kubectl run my-nginx --image nginx` | Run nginx container |
| `$ kubectl get pods` | Get information about pods |
| `$ kubectl create deployment my-nginx --image nginx` | Create a deployment named my-nginx |
| `$ kubectl get all` | List all resources in the cluster |

---

### Scaling and Describing Deployments

| Command | Description |
|---------|-------------|
| `$ kubectl scale deploy/my-apache --replicas 2` | Scale deployment my-apache to 2 replicas |
| `$ kubectl get all` | List all resources in the cluster |
| `$ kubectl describe deploy/my-apache` | Describe the deployment my-apache |

---

### Pods Information

| Command | Description |
|---------|-------------|
| `$ kubectl get pods` | Get information about pods |
| `$ kubectl describe pod/my-apache-5bd7979764-5g2sp` | Describe a specific pod |
| `$ kubectl get deploy/my-apache -o wide` | Get wide output for a deployment |
| `$ kubectl get deploy/my-apache -o yaml` | Get YAML output for a deployment |

---

### Nodes Information

| Command | Description |
|---------|-------------|
| `$ kubectl get nodes` | Get information about nodes |
| `$ kubectl get node docker-desktop -o wide` | Get detailed information about a specific node |
| `$ kubectl describe node docker-desktop` | Describe a specific node |

---

### Watching Resources

| Command | Description |
|---------|-------------|
| `$ kubectl get pods -w` | Watch for changes in pods |
| `$ kubectl delete pod my-apache-5bd7979764-5g2sp` | Delete a specific pod |
| `$ kubectl get pods -w` | Watch for changes in pods |
| `$ kubectl get events --watch-only` | Watch events in real-time |

---

### Logs Management

| Command | Description |
|---------|-------------|
| `$ kubectl logs deploy/my-apache` | Get logs for a deployment |
| `$ kubectl logs deploy/my-apache --follow --tail 1` | Follow logs for a deployment |
| `$ kubectl get pods` | Get information about pods |
| `$ kubectl logs pod/my-apache-` | Get logs for a specific pod |
| `$ kubectl logs pod/my-apache-5bd7979764-9v5p5 -c httpd` | Get logs for a specific container in a pod |
| `$ kubectl logs deploy/my-apache` | Get logs for a deployment |
| `$ kubectl logs deploy/my-apache --all-containers=true` | Get logs for all containers in a deployment |
| `$ kubectl logs -l app=my-apache` | Get logs for pods with a specific label |
| `$ stern my-apache` | Tail logs for multiple pods with the same label |

---

### Service Management

| Command | Description |
|---------|-------------|
| `$ kubectl get service` | Get information about services |

---

### Deployment and Job Management

| Command | Description |
|---------|-------------|
| `$ kubectl create deployment test --image nginx --dry-run=client` | Create a deployment named test (dry run) |
| `$ kubectl create deployment test --image nginx --dry-run=client -o yaml` | Create a deployment named test with YAML output (dry run) |
| `$ kubectl create job test --image nginx --dry-run=client -o yaml` | Create a job named test with YAML output (dry run) |
| `$ kubectl create deployment test --image nginx` | Create a deployment named test |
| `$ kubectl expose deployment/test --port 80 --dry-run=client -o yaml` | Expose a deployment named test on port 80 (dry run) |
