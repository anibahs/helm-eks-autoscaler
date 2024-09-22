# helm-eks-autoscaler



helm package autoscaler
helm repo index . 

cp autoscaler-0.1.0.tgz ../../Submissions/helm/ca-helm-registry 
cp index.yaml ../../Submissions/helm/ca-helm-registry 

cd ../../Submissions/helm/ca-helm-registry 
git add .
git commit -m 'feat: New chart version'
git push





cp autoscaler-0.1.0.tgz ../ca-helm-registry 
cp index.yaml ../ca-helm-registry 

cd ../../Submissions/helm/ca-helm-registry 
git add .
git commit -m 'feat: New chart version'
git push



helm repo add autoscaler-repo-main 'https://<>@raw.githubusercontent.com/cyse7125-su24-team11/ca-helm-registry/main/'

helm repo update
helm search repo autoscaler-repo-main





helm install autoscaler autoscaler --set caRoleArn=arn:aws:iam::<>:role/eks-ca --set-file dockerconfigjson=~/.docker/config.json

helm install autoscaler autoscaler --set-file dockerconfigjson=/Users/shabinasingh/.docker/config.json

helm uninstall autoscaler

aws eks update-kubeconfig --region us-east-1 --name cve-eks --role-arn arn:aws:iam::533267343403:role/eks-cluster-role
