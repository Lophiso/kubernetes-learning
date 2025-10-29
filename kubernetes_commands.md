📘 Kubernetes Commands Reference
🧩 Cluster & Minikube

minikube start
minikube stop
minikube delete --all --purge
minikube config set driver kvm2
minikube ip
minikube service <service-name> --url
kubectl config view --minify -o jsonpath='{..namespace}'
kubectl config set-context --current --namespace=<namespace>

🧱 Pods

kubectl run nginx --image=nginx
kubectl get pods -o wide
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl exec -it <pod-name> -- /bin/sh
kubectl delete pod <pod-name>
kubectl get pods -A | grep -i <name>
kubectl get pods -l app=<label>

🏗️ Deployments

kubectl create deployment myapp --image=nginx
kubectl get deployments
kubectl describe deployment <name>
kubectl scale deployment <name> --replicas=3
kubectl set image deployment/<name> <container>=<image>:<tag>
kubectl rollout status deployment/<name>
kubectl rollout history deployment/<name>
kubectl rollout history deployment/<name> --revision=<n>
kubectl rollout undo deployment/<name>
kubectl rollout undo deployment/<name> --to-revision=<n>

♻️ ReplicaSets

kubectl get replicasets
kubectl get replicaset
kubectl delete replicaset <name>

🌐 Services

kubectl get svc
kubectl describe svc <name>
kubectl get endpoints <service-name>
kubectl expose deployment <name> --type=NodePort --port=80
kubectl patch svc <name> -p '{"spec":{"selector":{"app":"<label>"}}}'
curl http://$(minikube ip):<nodePort>

💾 Config & Resources

kubectl apply -f <file>.yaml
kubectl delete -f <file>.yaml
kubectl edit <resource>/<name>
kubectl explain <resource> --api-version=<version>
kubectl get all

🧰 Debugging

kubectl get events --sort-by=.metadata.creationTimestamp
kubectl describe pod <name> | sed -n '/Events/,$p'
kubectl logs <pod> -c <container> --tail=100
kubectl port-forward deploy/<name> 8080:80

🐘 Databases (PostgreSQL, Redis examples)

kubectl exec -it <postgres-pod> -- psql -U postgres
kubectl exec -it <redis-pod> -- redis-cli

💻 Git & Repo Management

git init
git add .
git config --global user.name "Lophiso"
git config --global user.email "lopisofeleke10@gmail.com"
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/Lophiso/<repo>.git
git push -u origin main


🧩 Linux & Shell Basics

cd <directory>
pwd
ls -a
Ctrl + C        # stop process
Ctrl + Z        # suspend process
fg              # resume
kill <PID>      # kill process
curl http://<ip>:<port>

🧠 Other Useful Tools

kubectl get nodes
kubectl cluster-info
kubectl cluster-info dump > dump.txt
kubectl get namespaces
kubectl get api-resources

