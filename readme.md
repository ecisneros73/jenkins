sudo mkdir -p /var/lib/jenkins/.kube
sudo cp -r /home/ubuntu/.minikube /var/lib/jenkins/.minikube
sudo cp /home/ubuntu/.kube/config /var/lib/jenkins/.kube/config
sudo chown -R jenkins:jenkins /var/lib/jenkins/.kube /var/lib/jenkins/.minikube
