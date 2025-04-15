# ClickHouse Cluster Deployment Tool

This tool allows you to deploy a fully configured ClickHouse cluster without any code modifications.

## How to Deploy Your ClickHouse Cluster

1. Click the "Actions" tab at the top of this repository
2. Select the "Launch ClickHouse Deployment" workflow from the left sidebar
3. Click the "Run workflow" button
4. Fill in your deployment parameters:

   **Hardware Configuration:**
   - CPU cores per node
   - RAM in GB per node
   
   **Cluster Configuration:**
   - ClickHouse version
   - Cluster name
   - Number of shards
   - Number of replicas per shard
   
   **Server Information:**
   - Keeper IPs (comma separated)
   - Server IPs (comma separated)
   - SSH user
   - SSH private key (base64 encoded)
   
   **Environment Settings:**
   - Environment type
   - Hardware profile
   - SSL enabled

5. Click "Run workflow" to start the deployment

## SSH Key Setup

You need to provide your SSH private key in base64 format. To encode your key:

```bash
cat ~/.ssh/id_rsa | base64 -w 0
