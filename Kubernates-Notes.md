
#Notes on Kubernates

#####For Installation https://kubernetes.io/docs/getting-started-guides/kubeadm/
<br/>
kubeadm init --token 123456.1234567890123456 --api-advertise-addresses 192.168.204.134
<br/>
kubeadm reset --> to reset the kubeadm
<br/>
kubectl apply -f https://git.io/weave-kube
<br/>
#####For network https://kubernetes.io/docs/admin/addons/
<br/>
kubectl join --token=<b>TOKEN</b> <b>MASTER_IP</b>
<br/>
kubectl describe po <b>POD_NAME</b> --> will describe about the pods
<br/>
kubectl create -f <b>YML_file</b> --> YML file for the pods
<br/><br/><br/><br/><br/><br/>


RUN kubeadm init -> On the master node only<br/>
take the file /etc/kubernates/admin.conf to the childs and get all the commands executed e.g<br/>
	kubectl --kubeconfig <admin.conf location> get nodes
	

