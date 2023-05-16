# Deploy MongoDB_MongoExpress_using_Kubernetes

This project deploys a MongoDB database and MongoExpress UI using Kubernetes.

## What's Included
Persistent Volume for MongoDB data
Persistent Volume Claim used by MongoDB
MongoDB deployment
MongoDB service
MongoExpress deployment
MongoExpress service
ConfigMap for MongoExpress environment variables
Secret for MongoDB password


## How to Deploy


Apply the ConfigMap:

Copy
kubectl apply -f ConfigMap.yaml
````

Apply the Secret:

Copy
kubectl apply -f secret.yaml
````

Apply the Persistent Volume:

Copy
kubectl apply -f pv.yaml
````

Apply the Persistent Volume Claim:

Copy
kubectl apply -f pvc.yaml
````

Apply the MongoDB resources:

Copy
kubectl apply -f mongodb-deployment.yml
````

Apply the MongoExpress resources:

Copy
kubectl apply -f mongoExpress-deployment.yml  
````


Get the MongoExpress URL:

Copy
kubectl get svc mongo-express
````

Access the MongoExpress UI in your browser.

The MongoDB data will now persist across pod restarts using the Persistent Volume.

