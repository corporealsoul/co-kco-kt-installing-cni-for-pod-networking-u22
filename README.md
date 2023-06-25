### Installing CNI for POD networking, Installing a Pod network add-on ,

**Note: The parameter pod-network-cidr changes as per the network option.**

https://kubernetes.io/docs/concepts/cluster-administration/addons/

**Example:** The suggested CIDR for flannel and canal networks is 10.244.0.0/16 and for calico network it could be 192.168.0.0/16 , The default range that Weave Net would like to use is 10.32.0.0/12

It is not necessary to provide the parameter –pod-network-cidr for other network options like Contiv, Romana and Weavenet. However, it is must for the networks Romana and Weavenet to set /proc/sys/net/bridge/bridge-nf-call-iptables to 1 by running "sysctl net.bridge.bridge-nf-call-iptables=1" to pass bridged IPv4 traffic to iptables’ chains.


https://github.com/containernetworking/cni

https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/#pod-network

https://kubernetes.io/docs/concepts/cluster-administration/networking/

https://github.com/kubernetes/design-proposals-archive/blob/main/network/networking.md

https://kubernetes.io/docs/concepts/cluster-administration/addons/#networking-and-network-policy

https://kubernetes.io/docs/tasks/administer-cluster/network-policy-provider/

<br>

### Weave works,

https://www.weave.works/docs/net/latest/kubernetes/kube-addon/

**Integrating Kubernetes via the Addon,**

`[anup@rhel-92-04 ~]$ kubectl apply -f https://github.com/weaveworks/weave/releases/download/v2.8.1/weave-daemonset-k8s.yaml`

<br>
