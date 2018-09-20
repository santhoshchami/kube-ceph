
Prepare the secret hash from the keyring we have in the ceph folder:
cat /etc/ceph/ceph.client.admin.keyring | grep key|awk '{print $3}' | base64

kubectl create -f ceph-secret.yaml

create now a persistent volume

kubectl create -f ceph-pv.yaml

 persistent volume claim:
 
 kubectl create -f ceph-pv-claim.yaml 
 
 Create deployment:
 
 kubectl create -f ngix.yaml 
