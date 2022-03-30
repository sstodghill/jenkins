# Jenkins on Kubernetes

Below are the steps to install Jenkins on microk8s from
https://www.jenkins.io/doc/book/installing/kubernetes/
`kc create namespace jenkins
helm repo add jenkinsci https://charts.jenkins.io
sudo mkdir -p /data/jenkins-volume
sudo chown 1000:1000 /data/jenkins-volume
kubectl apply -f jenkins-volume.yaml
kubectl apply -f jenkins-sa.yaml
chart=jenkinsci/jenkins
helm install jenkins -n jenkins -f jenkins-values.yaml $chart`

