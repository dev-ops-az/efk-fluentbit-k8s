Step 1: Create RBAC for the Fluent Bit

kubectl create namespace fluentbit-test
kubectl apply -f rbac.yaml

Step 2: Create a ConfigMap
kubectl apply -f configmap.yaml

Step 3: Deploy Fluent Bit on Minikube
kubectl apply -f daemonset.yaml
