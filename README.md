# connect-to-kubernetes-cluster-from-localterminal
You can connect to your cluster via command-line or using a dashboard. 
Open the terminal and copy paste the below commad line access from gcp kubernetes engine console by pressing "connect".
Configure kubectl command line access by running the following command on your terminal:
Below command will be different at your gcp dashboard
For ex:
```
gcloud container clusters get-credentials standard-cluster-1 --zone us-central1-a --project elegant-expanse-90876
````
Now you are able to connect from terminal to gcp cluster. Run below command: 
```
kubectl get nodes
```
If you face an error that it can't find ```kubectl``` then check if it is installed:
```
gcloud components list
```
If it is not there then install it:
```
gcloud install components  kubectl
```
If it is still not there run below command and see in which folder it is located :
```
find / -type f -name kubectl 2>/dev/null
```
Copy the output you see from the above command and now make sure to put it inside of ```vim ~/.bash_profile```
````
export PATH=/usr/local/Caskroom/google-cloud-sdk/latest/google-cloud-sdk/bin:$PATH

````
Run below ```source ~/.bash_profile```, 
see if it there ```which kubectl```
Final step:
``` kubectl get nodes```
