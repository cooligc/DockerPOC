
# Notes on Kubernates

##### For Installation https://kubernetes.io/docs/getting-started-guides/kubeadm/  

``kubeadm init --token 123456.1234567890123456 --api-advertise-addresses 192.168.204.134`` 

``kubeadm reset --> to reset the kubeadm``  

``kubectl apply -f https://git.io/weave-kube`` 

##### For network https://kubernetes.io/docs/admin/addons/
``kubectl join --token=<b>TOKEN</b> <b>MASTER_IP</b>``  
``kubectl describe po <b>POD_NAME</b>`` --> will describe about the pods  
``kubectl create -f <b>YML_file</b>`` --> YML file for the pods  



```RUN kubeadm init``` -> On the master node only  
take the file /etc/kubernates/admin.conf to the childs and get all the commands executed e.g  
```kubectl --kubeconfig <admin.conf location> ``` get nodes
	

