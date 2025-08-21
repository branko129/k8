This is repo with real world examples

To deploy ArgoCD and basic configuration (check patch.yaml), navigate to argocd folder and execute:

kubectl create ns argocd
kubectl apply -n argocd -k . 

Check if ArgoCD is deployed:

kubectl get all -n argocd


To use app-of-apps pattern, create app-of-apps argocd application:

kubectl apply -f app-of-apps.yaml


This application will deploy all of your apps stored in defined repo (folder apps).
Each application defined in apps folder will create it's own resources.

