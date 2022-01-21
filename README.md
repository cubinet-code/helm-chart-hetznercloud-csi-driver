# Hetzner Cloud CSI Helm Chart

This is a Helm Chart for Container Storage Interface driver for Hetzner Cloud

The chart only has few values to be configured:

values.yaml:
```
api:
  # Your Hetzner API token (required)
  token: TOKEN              
storageclass:
  # Name of the storage class to be configured
  name: hcloud-volumes      
  # true or false. Will the storageclass be the default class for the cluster? 
  isDefault: true           
```
After that PVCs referring to this storage class will spawn Hetzner Volumes based on the pvc manifest.
The minimum storage capacity provisioned will 10Gi, regardless of what is set in the pvc manifest.

The original manifests and additonal documentation is located in the [Hetznercloud GitHub Pages](https://github.com/hetznercloud/csi-driver/).

