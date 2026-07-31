# bi85rj_medicore-secure-cloud-infrastructure
UOS DTS202 Assignment

DTS202 - Data Governance and Compliance

## Cloud Service Provider

Amazon Web Services (AWS)

## Data Storage Region

Europe (London) - eu-west-2

## Project Overview

As part of DTS202, assignment 1, this is a secure cloud infrastructure design for MediCore Health Systems supporting the processing of NHS clinical data in accordance with regulatory and security requirements as set out in UK GDPR, NHS DSPT and Cyber Essentials Plus requirements.

## Architecture

![Architecture Diagram](Screenshots/Architecture/00.%20Medicore_AWS_Architecture.png)

## How To Access This Deployment In AWS

The implementation of the Medicore VPC was completed using AWS and the following Read-Only account has been provided to allow it to be viewed. MFA is disabled to allow ease of access for the assignment marker however in a real world deployment MFA would be mandatory.

Account Alias or ID: 839765241584

Console Sign-In URL: https://839765241584.signin.aws.amazon.com/console

Username: Clinical.ReadOnly@Medicore

Password: ee%N3^'N

## Note On Docker File

An example Dockerfile is included in the repository to demonstrate containerisation best practices and vulnerability scanning. However, as the infrastructure deployment was implemented entirely through the AWS Management Console, this file is for demonstration purposes only and is not used to trigger an automated container build.
