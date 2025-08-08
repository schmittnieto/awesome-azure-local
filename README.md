# Awesome Azure Local

A curated list of links and resources for **Azure Local** and its related technologies. This repository centralizes knowledge for professionals building or operating hybrid cloud and edge solutions.

---

## Table of Contents

- [Official](#official)  
  - [Azure Local](#azure-local)  
  - [AVD](#avd)  
  - [AKS](#aks)  
  - [Backup and Disaster Recovery](#backup-and-disaster-recovery)  
  - [GitHub Repositories](#github-repositories)
- [OEMs](#oems)  
  - [Dell](#dell)  
  - [HPE](#hpe)  
  - [Lenovo](#lenovo)  
  - [DataON](#dataon)
- [Community](#community)  
  - [Blog](#blog)  
  - [Chats](#chats)  
  - [Events](#events)

---

## Official  
*Only official links published or maintained by Microsoft or Azure.*

### Azure Local

- [Azure Local Product Page](https://azure.com/hci)  
  Official product page for Azure Local on the Azure website.  
- [What is Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/overview)  
  Introduction to Azure Local (formerly Azure Stack HCI) and its core components.  
- [What is new in Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/whats-new)  
  Lists the latest features and improvements available in Azure Local.  
- [Azure Local Deployment (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/deploy/deployment-introduction)  
  First article in a series that describes how to deploy Azure Local.  
- [Azure Local Pricing](https://azure.microsoft.com/en-us/pricing/details/azure-local/)  
  Overview of licensing options, cost model, and subscription details.  
- [Azure Local Hardware Catalog](https://azurelocalsolutions.azure.microsoft.com/#/catalog)  
  Certified hardware from Microsoft partners.  
- [Azure Local Sizer](https://azurelocalsolutions.azure.microsoft.com/#/sizer)  
  Tool that estimates hardware requirements based on selected parameters.  
- [Azure Hybrid Benefit on Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/windows-server/get-started/azure-hybrid-benefit?tabs=azure-local#getting-azure-hybrid-benefit)  
  Link describing the contractual requirements for using Azure Hybrid Benefit with Azure Local. 

### AVD

- [Azure Virtual Desktop documentation (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/virtual-desktop/)  
  Complete documentation for deploying and managing Azure Virtual Desktop.  
- [Deploying AVD on Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/virtual-desktop/deploy-azure-virtual-desktop)  
  Step-by-step guide for running Azure Virtual Desktop in an Azure Local environment.  
- [AVD on Azure Local pricing](https://azure.microsoft.com/en-us/pricing/details/virtual-desktop/)  
  To view pricing for Azure Virtual Desktop on Azure Local, open the "Pricing overview tab" (the rate is currently "*$0.01 per virtual core per hour*").  

### AKS

- [Architecture overview for AKS on Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/aks/aksarc/cluster-architecture)  
  Architecture overview for running AKS clusters on Azure Local.  
- [AKS Deployment on Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/aks/aksarc/aks-create-clusters-portal)  
  How to create a Kubernetes cluster in the Azure portal; clusters are Azure Arc-connected by default.  
- [SQL Managed Instance enabled by Azure Arc (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-arc/data/managed-instance-overview)  
  Azure SQL Managed Instance that runs on your infrastructure of choice through Arc Data Services inside an AKS cluster.  

### Backup and Disaster Recovery

- [Back up Azure Local virtual machines with Azure Backup Server (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/backup/back-up-azure-stack-hyperconverged-infrastructure-virtual-machines)  
  How to back up virtual machines on Azure Local by using Microsoft Azure Backup Server.  
- [Azure Site Recovery on Azure Local (preview) (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/manage/azure-site-recovery)  
  Guide to protect Windows and Linux workloads on Azure Local during a disaster.  

### GitHub Repositories

- [Arc Jumpstart source code](https://github.com/microsoft/azure_arc)  
  Source for Arc Jumpstart automation scripts and tools, supporting the official documentation site.  
- [Azure Local Supportability Forum](https://github.com/Azure/AzureLocal-Supportability)  
  Central repository for troubleshooting guides, known issues, and feedback used by support teams and the community.  
- [Azure Local sample repository](https://github.com/Azure-Samples/AzureLocal)  
  Samples covering SDN training, security baselines, and alternate OS image download links such as the [OS image tracking table](https://github.com/Azure-Samples/AzureLocal/blob/main/os-image/os-image-tracking-table.md).  
- [MSLab](https://github.com/microsoft/MSLab)  
  Scripts and resources to create nested Hyper-V labs, ideal for testing Azure Local in a virtual environment.  

---

## OEMs  
Resources from key original equipment manufacturers with dedicated Azure Local content.

### Dell

- [Dell - Azure Local Landing Page](https://www.dell.com/en-us/shop/ax-system-for-azure-local/sf/ax-system-for-azure-local)  
  Dell landing page for Azure Local.  
- [Dell - Deployment Guides for Azure Local](https://infohub.delltechnologies.com/de-de/t/guides-azure-stack-hci-os-24h2-or-ws-2025-and-later/)  
  Technical guides for Dell AX System for Azure Local or Dell AX System for Windows Server with operating system version 24H2 or Windows Server 2025 and later.  
- [Dell - Azure Local Hands on Labs (GitHub)](https://github.com/DellGEOS/AzureLocalHOLs)  
  Detailed guides on building a lab for Azure Local, tips, and deep dives.  
- [Dell - Dell Technologies Solutions for Microsoft Azure - Azure Local](https://dell.github.io/azurestack-docs/docs/hci/)  
  Website backed by the Dell GitHub repository that lists supported versions and architectural guidance for Azure Local.  
- [Dell - Azure Local InfoHub](https://infohub.delltechnologies.com/t/microsoft-hci-solutions-from-dell-technologies-1/)  
  Main page that aggregates the Dell Azure Local resources mentioned above.  
- [Dell - SBE Page](https://www.dell.com/support/kbdoc/en-us/000224407/dell-for-microsoft-azure-stack-hci-ax-hardware-updates-release-notes)  
  Page for managing firmware and driver updates on Dell hardware.  

### HPE

- [HPE - Azure Local Landing Page](https://www.hpe.com/us/en/alliance/microsoft/azurelocal.html)  
  HPE landing page for Azure Local.  
- [HPE - ProLiant for Azure Local Integrated Systems User Guide](https://support.hpe.com/hpesc/public/docDisplay?docId=sd00006156en_us&docLocale=en_US)  
  Management guide for HPE ProLiant for Azure Local, aimed at administrators who install, manage, and troubleshoot servers.  
- [HPE - Solutions for Azure Local - Deployment Guide](https://www.hpe.com/psnow/doc/a50008245enw)  
  Technical white paper with solution guidelines and example configurations for Azure Local HCI on HPE ProLiant, Alletra, and Edgeline servers.  
- [HPE - SBE Page](https://myenterpriselicense.hpe.com/cwp-ui/product-details/SBE_UPDATES/-/sw_free)  
  Page for managing firmware and driver updates on HPE hardware.  

### Lenovo

- [Lenovo - Azure Local Landing Page](https://www.lenovo.com/us/en/resources/streams/microsoft-azure-stack-hci)  
  Lenovo landing page for Azure Local.  
- [Lenovo - ThinkAgile MX Series for Microsoft Azure Local](https://lenovopress.lenovo.com/servers/thinkagile/mx-series)  
  Installation and deployment guides for Azure Local and related services on Lenovo hardware.  
- [Lenovo - SBE Page](https://pubs.lenovo.com/thinkagile-mx/de/mx_sbe)  
  Page for managing firmware and driver updates on Lenovo hardware.  

### DataON

- [DataON - Azure Local Landing Page](https://www.dataonstorage.com/azurestackhci/)  
  DataON landing page for Azure Local.  
- [DataON - Azure Local Knowledge Base](https://dataon.io/knowledge-base-categories/azure-stack-hci/)  
  Extensive knowledge base with articles covering many Azure Local services and components.  
- [DataON - Azure Local Quick Reference Guide](https://dataon.io/dataon-quick-reference-guides/)  
  Set of reference guides that compare Azure Local solutions and services.  
- [DataON - SBE Page](https://dataon.io/apply-updates-to-your-azure-stack-hci-cluster-with-the-solution-builder-extension-sbe/)  
  Page for managing firmware and driver updates on DataON hardware.  

---

## Community

### Blog

- *Placeholder for community blog link 1*  

### Chats

- *Placeholder for chat or forum link*  

### Events

- [Microsoft Ignite - Azure Hybrid Sessions](https://ignite.microsoft.com/en-US/home)  
- *Placeholder for past or upcoming community event*  

---

> Contributions are welcome. Please submit a pull request or an issue with verified links or improvements.
