# Implementing Pi-hole on a Synology NAS

## Project Overview

Pi-hole is a powerful DNS sinkhole designed to block ad traffic across a network. By deploying Pi-hole on a Synology NAS via Docker, you can use it as your DNS server and significantly reduce the number of advertisements you encounter while browsing the web. This project focuses on configuring the necessary network settings, setting up the Pi-hole container, and adding blocklists to optimize the ad-blocking experience.

## Detailed Description

### Key Components

1. **Synology NAS Setup**:
   - **SSH Access**: Securely connect to the Synology NAS via SSH to perform network configurations.
   - **Network Configuration**: Set up a macvlan interface for a dedicated IP address and a network bridge interface for seamless container communication.

2. **Pi-hole Configuration**:
   - **Docker Deployment**: Utilize Docker to download, configure, and initialize the Pi-hole container.
   - **Environment Variables**: Establish environment variables for the admin account and network settings.
   - **Blocklists**: Integrate known ad server lists into Pi-hole to enhance ad-blocking capabilities.

### Process

#### Step 1: Connect to Synology NAS via SSH

1. **SSH Access**:
   - Enable SSH on the Synology NAS and connect using an SSH client.
   - Perform network configurations, including creating a macvlan and network bridge interface.

#### Step 2: Configure Network Interfaces

1. **Macvlan Interface**:
   - Create a macvlan interface to assign a dedicated IP address for Pi-hole.

2. **Network Bridge Interface**:
   - Set up a network bridge to facilitate communication between Docker containers and the NAS network.

3. **Resolve.conf File**:
   - Configure the `resolve.conf` file to add nameservers for DNS resolution.

#### Step 3: Download and Configure Pi-hole Container

1. **Download Pi-hole**:
   - Pull the Pi-hole Docker image from the repository.

2. **Initialize Pi-hole Container**:
   - Configure the Pi-hole container with environment variables, including admin account credentials and network settings.
   - Ensure the container points to the network bridge interface.

#### Step 4: Configure Pi-hole and Add Blocklists

1. **Access Pi-hole GUI**:
   - Access the Pi-hole graphical user interface (GUI) via the macvlan IP address.

2. **Admin Account Configuration**:
   - Log in to the Pi-hole GUI and configure the admin account settings.

3. **Add Blocklists**:
   - Add several blocklists to Pi-hole to effectively block advertisements.
   - Fine-tune the blocklists to optimize the browsing experience.

### Security Measures

- **Account Management**: Disable default admin and guest accounts, and apply the principle of least privilege.
- **Authentication**: Enable Adaptive Multi-Factor Authentication (AMFA) for all users.
- **Access Control**: Restrict login attempts and enforce strong password policies.
- **Data Protection**: Use snapshot replication to safeguard against ransomware attacks.

<h2>Pi-hole running and blocking ads:</h2>

<p align="center">
  <img src="https://i.imgur.com/HgWHA4U.jpeg" height="80%" width="80%"/>
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
