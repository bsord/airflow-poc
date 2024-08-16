1) install kind
2) install kubectl
3) install helm
4) create namespace 'airflow-cluster'
4) create github secret for git-sync
kubectl create secret generic airflow-ssh-git-secret --type=string --namespace=airflow-cluster --from-file=id_rsa=./id_rsa_airflow_poc --dry-run=client
6) install airflow ( using kube operator, making sure to use the local yaml config)