# RocketChat KOTS Appliance
This repository houses all the config needed to deploy a RocketChat KOTS appliance.

## Embedded Cluster Installation Steps

1. Create a VM
1. SSH into the VM and run the cluster installation script
```bash
curl -sSL https://k8s.kurl.sh/rocket-community | sudo bash
```
1. Follow the instructions provided at the completion of the installation script
1. Wait for the app to start successfully, then click `Launch Rocket.chat`

## Existing Cluster Installation Steps

```bash
curl https://kots.io/install | bash
kubectl kots install rocket-community
```

## Preflight Checks
Checks that must pass before the KOTS appliance can come online
- K8s cluster version must be higher than `1.15.0`
- 1 CPU core required. 2 CPU cores recommended
- 1GB of RAM required. 2GB of RAM recommended
- 20GB of disk capacity for the root partition required. 40GB recommended

## Config Options
- RocketChat DNS Hostname
- MongoDB Root Password
- MongoDB RocketChat Password
- MongoDB Volume Size

## Support Bundle
- Retrieve cluster info and resources
- Retrieve RocketChat API health status
- Retrieve MongoDB version
- Ping Google DNS address
- Ping Google IP Address
