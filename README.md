# 🚀 Pod with CPU and Memory Requests/Limits (Minikube Example)

This project demonstrates how to create a Kubernetes pod with CPU and memory resource requests and limits using Minikube.

---

## 📄 Step 1: Create YAML File

Create a file named `resource-pod.yaml`:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: resource-limited-pod
spec:
  containers:
  - name: nginx
    image: nginx
    resources:
      requests:
        memory: "128Mi"
        cpu: "100m"
      limits:
        memory: "256Mi"
        cpu: "250m"
```

---

## 🚀 Step 2: Apply the YAML

Run the following command to create the pod:

```bash
kubectl apply -f resource-pod.yaml
```

---

## 🔍 Step 3: Verify the Pod

Check if the pod is running:

```bash
kubectl get pod resource-limited-pod
```

Describe the pod to see the resource details:

```bash
kubectl describe pod resource-limited-pod
```

---

## 📸 Screenshot

Add the following line to display your screenshot in the README ():

```markdown
![Pod Resources Screenshot](screenshots/resource-pod-output.jpg)
```

> 📁 Store your screenshot inside a `screenshots/` folder.

---

## 🧹 Step 4: Delete the Pod (Optional Cleanup)

```bash
kubectl delete pod resource-limited-pod
```

---

## 📁 Project Structure

```
.
├── README.md
├── resource-pod.yaml
└── screenshots/
    └── resource-pod-output.jpg
```

---

## 📝 License

MIT License – Use for educational or DevOps project documentation.
