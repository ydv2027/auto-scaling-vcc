# auto-scaling-vcc

This repository contains the code, configurations, and documentation for setting up a Virtual Machine (VM) on Google Cloud Platform (GCP) with auto-scaling policies and security measures. This project was completed as part of an assignment to demonstrate the use of GCP for scalable and secure deployments.

# Project Overview
The goal of this project is to:

Create a VM instance on GCP.

Configure auto-scaling policies based on CPU utilization.

Implement security measures such as IAM roles and firewall rules.

This project demonstrates how to leverage GCP's infrastructure for scalable and secure deployments.

# Deliverables
Document Report: Step-by-step instructions for implementation, including VM creation, auto-scaling configuration, and security measures.

Architecture Design: Diagram showing the VM setup, auto-scaling configuration, and security policies.

Source Code Repository: This GitHub repository containing deployment scripts and configurations.

Video Demo: A recorded video demonstrating the setup and functioning of auto-scaling and security.

# Setup Instructions
Follow these steps to replicate the setup on GCP:

1. Prerequisites
A GCP account with billing enabled.

Basic knowledge of GCP services (Compute Engine, IAM, VPC).

2. Create a VM Instance
Go to Compute Engine > VM Instances.

Click Create Instance.

Configure the VM with the following settings:

Name: auto-scaling-vm

Region/Zone: us-central1-a

Machine Type: e2-micro

Boot Disk: Ubuntu 20.04 LTS

Allow HTTP and HTTPS traffic.

Click Create.

3. Configure Auto-Scaling
Create an instance template:

Go to Compute Engine > Instance Templates.

Create a template named auto-scaling-template.

Create a managed instance group (MIG):

Go to Compute Engine > Instance Groups.

Create a MIG named auto-scaling-group.

Enable autoscaling with:

Minimum Instances: 1

Maximum Instances: 3

Target CPU Utilization: 60%.

4. Implement Security Measures
Set up IAM roles:

Go to IAM & Admin > IAM.

Add a member and assign the Compute Viewer role.

Configure firewall rules:

Go to VPC Network > Firewall.

Create rules to allow HTTP (tcp:80), HTTPS (tcp:443), and SSH (tcp:22) traffic.

Implementation Details
1. Auto-Scaling Configuration
Auto-scaling is based on CPU utilization.

Instances scale up when CPU usage exceeds 60% and scale down when usage drops below the threshold.

2. Security Measures
IAM Roles: Restricted access to the VM using IAM roles.

Firewall Rules: Allowed HTTP, HTTPS, and SSH traffic while restricting access to specific IPs.

3. Architecture Diagram
Architecture Diagram


# Plagiarism Clause
I confirm that this submission is my original work and has not been copied from any other source. Plagiarism will result in the submission being voided.

# License
This project is licensed under the MIT License. See the LICENSE file for details.
