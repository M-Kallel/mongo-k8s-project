# MongoDB + Mongo Express on Kubernetes

This project demonstrates how to deploy a MongoDB database along with Mongo Express (a web-based MongoDB admin interface) on a Kubernetes cluster using YAML configuration files.

---

## Project Structure

- `mongodb-deployment.yaml` — Deployment and Service for MongoDB  
- `mongo-express.yaml` — Deployment and Service for Mongo Express  
- `mongo-configmap.yaml` — ConfigMap for Mongo Express configuration  
- `mongodb-secret.yaml` — **Real secret file (ignored by Git, keep local only)**  
- `mongodb-secret-example.yaml` — Dummy secret file (safe to push to GitHub)  
- `.gitignore` — Ignores sensitive files and system files  

---

## How to Use

1. **Clone the repository**  
   ```bash
   git clone https://github.com/M-Kallel/mongo-k8s-project.git
   cd mongo-k8s-project

2.Create your own secret file

cp mongodb-secret-example.yaml mongodb-secret.yaml
# Then edit mongodb-secret.yaml to add your real username and password

3.Apply Kubernetes resources

kubectl apply -f mongodb-deployment.yaml
kubectl apply -f mongo-configmap.yaml
kubectl apply -f mongo-express.yaml

4.Access Mongo Express

minikube service mongo-express-service
M
