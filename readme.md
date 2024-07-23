# Validator Rumba Node Installation Guide

This document provides the steps and commands used to set up and configure validator, storage, KV, and DA nodes for Validator Rumba in the 0G project.

## Server Specifications
- **IP:** 95.216.32.244
- **EVM Port:** 8545
- **Storage Port:** 5678
- **KV Port:** 6789
- **DA Port:** 34000
- **DA Client Port:** 51001
- **Validator Address:** 0gvaloper179jwd0d50z4ywymk8wmdgy50448ceqxh033pfg
- **Instance Capacity:**
  - 12 Core CPU
  - 64 GB RAM
  - 1 Gbps Network
  - 3 TB NVMe SSD

## Prerequisites

Before starting, ensure you have the following installed on your server:
- Docker
- Docker Compose
- Git

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/0gproject/0g-nodes.git
cd 0g-nodes
```
## Setup Environment Variables
Create a .env file with the following content:

```
EVM_PORT=8545
STORAGE_PORT=5678
KV_PORT=6789
DA_PORT=34000
DA_CLIENT_PORT=51001
VALIDATOR_ADDRESS=0gvaloper179jwd0d50z4ywymk8wmdgy50448ceqxh033pfg
```
## Validator Node Setup
Follow the instructions in the Validator Node guide:

```
docker-compose -f validator-node/docker-compose.yml up -d
```
## Storage Node Setup
Follow the instructions in the Storage Node guide:

```
docker-compose -f storage-node/docker-compose.yml up -d
```
## KV Node Setup
Follow the instructions in the Storage KV guide:

```
docker-compose -f kv-node/docker-compose.yml up -d
```
## DA Node Setup
Follow the instructions in the DA Node guide:

```
docker-compose -f da-node/docker-compose.yml up -d
```
## DA Client Setup
Follow the instructions in the DA Client guide:
```
docker-compose -f da-client/docker-compose.yml up -d
```
