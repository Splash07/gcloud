```
gcloud auth activate-service-account --key-file /root/.config/ncdevops01-service-account.json
gcloud config set project ncdevops
gcloud container clusters get-credentials --zone asia-southeast1-a ncdevops01
kubectl get node -o wide
```
