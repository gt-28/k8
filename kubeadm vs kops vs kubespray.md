# Kubernetes cluster

Comparision:

> Tools Include:
    ` kubeadm, kops, kubespray`

These tools allow to build and configure `k8's` cluster up and running in a simple way. 

**Note:** All these tools are supported and maintained by `kubernetes community`.

1. **Kops:**
    kops, enables users to create, update, delete prod level HA k8 clusters through CLI. 
    It is being maintained by K8 team.

    _Pros:_
        High chances to become a default method to deploy HA cluster in near future.
        Automated infrastrcuture provisioning. 
        supports all native features of cloud providers.
        supports all future upgrades and updates.
        custom add-ons.

    _Availability:_
        Kops is available for:
            AWS
            GCP (Beta relase)
            VMware VSphere (Alpha)


2. **Kubeadm:**
    It is designed to simplify k8 bootstrapping and cluster configuration along with add-ons.


    _Pros:_
        well suites for `bare metal` K8 cluster.
        Trying K8s for first time users.
        Testing applications.
        balances flexibility and ease of use.

    _Cons:_
        tool cannot be used against VM's.


3. **Kubespray:**
    it is designed to deploy the K8 cluster either on cloud or on-prem.
    Works based on `Ansible playbook`.

    _Pros:_
        HA cluster deployment from Ansible playbook.
        Choice of different `Network plugins`
        supports Jenkins for CI deployment of K8 cluster.
        `Kubeadm` under the hood.

    _Cons:_
        It dosent automatically creates VM's.

    _Availability:_
        AWS
        GCP
        AZURE
        OpenStack
        Bare Metal
    
    _Recommended Usage:_
        Spin Vm's using `Terraform`
        Apply the `kubespray` via `Ansible Playbook`
