![Awesome Azure Local](/img/awesome_azure_local.png)
# Awesome Azure Local

A curated list of links and resources for **Azure Local** and its related technologies. Inspired by [Awesome Azure Architecture](https://aka.ms/AwesomeAzureArchitecture), which follows a similar model for Azure architecture links, this repository centralizes knowledge for professionals building or operating hybrid cloud and edge solutions.

---

## Table of Contents

- [Official](#official)  
  - [What's new in Azure Local?](#whats-new-in-azure-local-version-2510)
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
  - [Fujitsu](#fujitsu)  
- [Third Party](#third-party)  
  - [Backup Management](#backup-management)  
    - [Veeam](#veeam)  
    - [Commvault](#commvault)  
  - [AVD Management](#avd-management)  
    - [Nerdio](#nerdio)  
    - [Hydra by Login VSI](#hydra-by-login-vsi)
    - [Citrix](#citrix)
  - [Sizing](#sizing)  
    - [Acuutech](#acuutech)
- [Community](#community)  
  - [Blog](#blog)  
  - [LinkedIn](#linkedin)  
  - [YouTube](#youtube)  
  - [Github Repos & Tools](#github-repos--tools)  
  - [Chats & Channels](#chats--channels)  
  - [Trainings](#trainings)
  - [Events](#events)

---
<!-- AWESOMEAZURELOCAL:START -->
## Official  
*Only official links published or maintained by Microsoft or Azure.*

### What's new in Azure Local (version 2510)

[What's new in Azure Local?](https://learn.microsoft.com/en-us/azure/azure-local/whats-new?view=azloc-2510)

This release introduces several important updates and improvements across the platform:

#### OS changes
- All new Azure Local deployments now run on **OS version 26100.6899** (based on Windows Server 2025).  
  You can download the 2510 OS image from the Azure portal.  
- Requires compatible drivers for **26100.6899** or Windows Server 2025. If unavailable, you can use the 2503 image.  
- Existing deployments remain on **OS version 25398.1913**. See the [Release information summary](https://learn.microsoft.com/en-us/azure/azure-local/release-information-23h2).  
- Integrated System and Premier solution hardware from the [Azure Local Catalog](https://aka.ms/AzureStackHCICatalog) ship with preinstalled OS.  
  Contact your OEM for images compatible with **12.2510.1002.88** and the required drivers.

#### .NET updates
- The build now includes **.NET 8.0.21** for both .NET Runtime and ASP.NET Core.  
  Learn more at [Download .NET 8.0](https://dotnet.microsoft.com/download/dotnet/8.0).

#### Rack Aware Clustering (Preview)
- Azure Local now supports **rack aware clustering**, enabling local availability zones based on physical racks to improve resilience against rack-level failures.  
  More details at [Rack aware clustering](https://learn.microsoft.com/en-us/azure/azure-local/concepts/rack-aware-cluster-overview).

#### Upgrade
- Upgrades from **11.2510 to 12.2510** are now generally available and no longer require opt-in.

#### Azure Local VM updates
- **Software Defined Networking (SDN)** is now **GA**, allowing creation and management of NSGs and network security rules for Azure Local VMs through Azure Arc.  
  More info: [SDN enabled by Azure Arc](https://learn.microsoft.com/en-us/azure/azure-local/concepts/sdn-overview).  
- **Trusted Virtual Machine (Trusted VM) guest attestation (Preview)** introduces verification for Trusted Launch VMs, ensuring boot integrity across firmware, OS boot loader, and drivers.  
  More info: [Trusted VM guest attestation](https://learn.microsoft.com/en-us/azure/azure-local/manage/trusted-launch-guest-attestation).

#### Azure Local deployment using local identity
- The **Local Identity deployment** feature has moved from Limited Preview to **Preview** with improved documentation and Key Vault guidance.  
  Includes new FAQs and compatibility sections.  
  See [Deploy Azure Local using local identity with Azure Key Vault](https://learn.microsoft.com/en-us/azure/azure-local/deploy/deployment-local-identity-with-key-vault).

#### VMware migration to Azure Local
- Now **GA**, allowing VMware VM migration to Azure Local via **Azure Migrate**.  
  Learn more: [Migrate VMware VMs to Azure Local](https://learn.microsoft.com/en-us/azure/azure-local/migrate/migration-azure-migrate-vmware-overview).

#### OEM image support for registration
- **OEM images** are now supported for registering Azure Local machines with or without proxy.  
  See [Register with Arc gateway](https://learn.microsoft.com/en-us/azure/azure-local/deploy/deployment-with-azure-arc-gateway) and  
  [Register without Arc gateway](https://learn.microsoft.com/en-us/azure/azure-local/deploy/deployment-without-azure-arc-gateway).
  


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
- [Azure Local Solutions Category](https://azurelocalsolutions.azure.microsoft.com/#/Learn)  
  Overview of Azure Local solution types, outlining the differences between Validated Systems, Integrated Systems, and Premier solution.
- [Azure Local Security Book (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/security-book/overview)  
  The Azure Local security book discusses in detail the built-in security layers found in Azure Local, from core to cloud.
- [Optimize Azure Local using insights from a Well-Architected Review Assessment](https://techcommunity.microsoft.com/blog/AzureArchitectureBlog/optimize-azure-local-using-insights-from-a-well-architected-review-assessment/4458433)  
  Guidance on evaluating Azure Local environments with the Well-Architected Framework assessment to identify risks, measure maturity, and improve architecture quality.
- [Azure Local Baseline Architecture](https://learn.microsoft.com/en-us/azure/architecture/hybrid/azure-local-baseline)  
  Baseline reference architecture providing workload-agnostic guidance for configuring Azure Local 2311 and later, ensuring a reliable platform for highly available virtualized and containerized workloads.  
- [Architecture Best Practices for Azure Local](https://learn.microsoft.com/en-us/azure/well-architected/service-guides/azure-local)  
  Guidance aligned with the Azure Well-Architected Framework that outlines architectural recommendations for Azure Local and Azure Arc, supporting hybrid and edge deployments across validated hardware.  
- [Rack Aware Cluster (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/concepts/rack-aware-cluster-overview?view=azloc-2510)  
  This article provides an overview of the **Azure Local rack aware clustering** feature, including its benefits, use cases, supported configurations, and deployment requirements. Applies only to new deployments of Azure Local.  
- [SDN enabled by Arc on Azure Local (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/concepts/sdn-overview?view=azloc-2510)  
  This article explains **Software Defined Networking (SDN)** enabled by Azure Arc on Azure Local. It describes SDN management methods, guidance on when to use each approach, and outlines supported and unsupported SDN scenarios.  

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
- [KAITO - Kubernetes AI toolchain operator (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/aks/aksarc/deploy-ai-model?tabs=portal)  
  This article describes how to deploy an AI model on AKS enabled by Azure Arc with the Kubernetes AI toolchain operator (KAITO). 
- [Azure Kubernetes Service (AKS) Baseline Architecture for AKS on Azure Local](https://learn.microsoft.com/en-us/azure/architecture/example-scenario/hybrid/aks-baseline)  
  Scenario describing how to design and implement a baseline architecture for Azure Kubernetes Service (AKS) running on Azure Local.  
- [Deploy and operate apps with AKS enabled by Azure Arc on Azure Local](https://learn.microsoft.com/en-us/azure/architecture/example-scenario/hybrid/aks-hybrid-azure-local)  
  Recommendations for building an app deployment pipeline for containerized workloads using AKS enabled by Azure Arc on Azure Local, with guidance for GitOps-based operations.

### Backup and Disaster Recovery

- [Back up Azure Local virtual machines with Azure Backup Server (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/backup/back-up-azure-stack-hyperconverged-infrastructure-virtual-machines)  
  How to back up virtual machines on Azure Local by using Microsoft Azure Backup Server.  
- [Azure Site Recovery on Azure Local (preview) (Microsoft Docs)](https://learn.microsoft.com/en-us/azure/azure-local/manage/azure-site-recovery)  
  Guide to protect Windows and Linux workloads on Azure Local during a disaster.  

### GitHub Repositories

- [Jumpstart Local Box](https://jumpstart.azure.com/azure_jumpstart_localbox/getting_started)   
  LocalBox is a turnkey solution that provides a complete sandbox for exploring Azure Local capabilities and hybrid cloud integration in a virtualized environment (hosted on Azure).  
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
*Resources from key original equipment manufacturers with dedicated Azure Local content.*

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
- [Dell - External Storage with PowerFlex for Azure Local (White Paper)](https://www.delltechnologies.com/asset/en-us/products/converged-infrastructure/technical-support/reliable-performance-at-scale-white-paper.pdf)  
  White paper explaining the possibility and results of adding external storage to Azure Local as Cluster Storage using Dell PowerFlex (currently the only supported option).
- [Dell - How to Expand a CSV in PowerShell and Windows Admin Center](https://www.dell.com/support/kbdoc/en-us/000195872/how-to-expand-a-csv-in-ps-and-wac)  
  Guide explaining how to expand a Cluster Shared Volume (CSV) or Virtual Disk in Storage Spaces Direct (S2D) using PowerShell and Windows Admin Center.


### HPE

- [HPE - Azure Local Landing Page](https://www.hpe.com/us/en/alliance/microsoft/azurelocal.html)  
  HPE landing page for Azure Local.  
- [HPE - ProLiant for Azure Local Integrated Systems User Guide](https://support.hpe.com/hpesc/public/docDisplay?docId=sd00006156en_us&docLocale=en_US)  
  Management guide for HPE ProLiant for Azure Local, aimed at administrators who install, manage, and troubleshoot servers.  
- [HPE - Solutions for Azure Local - Deployment Guide](https://www.hpe.com/psnow/doc/a50008245enw)  
  Technical white paper with solution guidelines and example configurations for Azure Local HCI on HPE ProLiant, Alletra, and Edgeline servers.  
- [HPE - SBE Page](https://myenterpriselicense.hpe.com/cwp-ui/product-details/SBE_UPDATES/-/sw_free)  
  Page for managing firmware and driver updates on HPE hardware.  
- [HPE - ProLiant for Azure Local Firmware and Software Compatibility Guide](https://support.hpe.com/hpesc/public/docDisplay?docId=sd00003953en_us&page=GUID-86C4BE9C-0B69-4596-B333-69D099B3DC65.html)  
  A list of components, drivers and their status for system installation, especially useful for Validated Systems.


### Lenovo

- [Lenovo - Azure Local Landing Page](https://www.lenovo.com/us/en/resources/streams/microsoft-azure-stack-hci)  
  Lenovo landing page for Azure Local.  
- [Lenovo - ThinkAgile MX Series for Microsoft Azure Local](https://pubs.lenovo.com/thinkagile-mx/)  
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
  Page for managing firmware and driver updates on DataON Hardware. 

### Fujitsu

- [Fujitsu - Azure Local Landing Page](https://www.fujitsu.com/de/products/computing/integrated-systems/azure-stack-hci.html)  
  Fujitsu landing page for Azure Local with product information and references.
- [Fujitsu - Azure Local Infographic](https://docs.ts.fujitsu.com/dl.aspx?id=6c594a34-97fa-46b4-a0e8-1a78887524e9)  
  Infographic that summarizes the Azure Local solution from Fujitsu.

---

## Third Party  

*Independent vendors offering backup or AVD management solutions for Azure Local environments.*

### Backup Management  

*Software commonly used to perform backups of Azure Local infrastructure.*

#### Veeam

- [Veeam - Veeam Support for Azure Stack HCI](https://www.veeam.com/kb4047)  
  Documentation covering backup, restore, and replication of virtual machines on the initial Azure Stack HCI by Veeam Backup & Replication.  
- [Veeam - VBR step by step configure Azure Stack HCI OS - Azure Local Backup](https://community.veeam.com/blogs-and-podcasts-57/guide-vbr-step-by-step-configure-azure-stack-hci-os-azure-local-backup-10827)  
  Community article offering a deeper technical implementation of Veeam Backup for Azure Local.  

#### Commvault

- [Commvault - Azure Local Configuration and Documentation](https://documentation.commvault.com/11.42/essential/azure_local.html)  
  Guide to install and configure Commvault for protecting workloads on Azure Local.  
- [Commvault - Blueprint for Azure Local (PDF)](https://www.commvault.com/download-pdf/536787)  
  Document explaining core concepts and Commvault capabilities for backing up Azure Local infrastructure.  

### AVD Management  

*Software used to manage Azure Virtual Desktop infrastructure on Azure Local.*

#### Nerdio

- [Nerdio - Azure Local Landing Page](https://getnerdio.com/azure-local/)  
  Objective overview of Azure Local, covering architecture, edge scenarios, security, connectivity, and pricing.  
- [Nerdio - Integrate AVD resources provisioned to Azure Local with Nerdio Manager](https://nmehelp.getnerdio.com/hc/en-us/articles/34054417281165-How-can-I-integrate-AVD-resources-provisioned-to-Azure-Local-Stack-HCI-with-Nerdio-Manager)  
  Guide to integrate existing AVD infrastructure on Azure Local into Nerdio Manager for simpler management.  
- [Nerdio - AVD for Azure Local and Nerdio Manager](https://nmehelp.getnerdio.com/hc/en-us/articles/25499377328909-AVD-for-Azure-Local-and-Nerdio-Manager)  
  How to configure Nerdio to manage tasks on Azure Local, including golden images and host pool configuration.  

#### Hydra by Login VSI

- [Hydra - Landing Page](https://euc.loginvsi.com/hydra-by-login-vsi)  
  Hydra product overview from Login VSI.  
- [Hydra - Imaging, Rollout and Manage Azure Virtual Desktop on Azure Local](https://blog.itprocloud.de/AVD-Hydra-For-Azure-Stack-HCI-Deplyoment-Management/)  
  Article by Marcel Meurer on configuring Hydra for Azure Local.  

#### Citrix

- [Citrix Virtual Desktop / App - Connecting Azure Local](https://docs.citrix.com/en-us/citrix-virtual-apps-desktops/2507-ltsr/install-configure/connections/connection-azure-local)  
  As of August 22, 2025, Citrix has published a guide on how to use Citrix Virtual Desktop and Apps with Azure Local.

### Sizing

*Tools to estimate Azure Local sizing and choose the right hardware.*

#### Acuutech
- [Acuutech - Azure Local Landing Page](https://www.acuutech.com/azurelocal/)  
  Objective overview of Azure Local, covering architecture, edge scenarios, security, connectivity and pricing.  
- [Acuutech - Scopesys Azure Local Sizing Tool](https://www.acuutech.com/scopesys/)  
  Make the design, configuration and ordering of Azure Local or Windows Server solutions easy, by removing the technical complexity associated with scoping Azure Local or Windows Server environments.  

---

## Community  

*Resources that do not come from Microsoft, OEMs, or the vendors listed in the Third Party section.*

### Blog  

*To avoid an excessive list, only entire blogs are referenced, not individual posts.*

- [schmitt-nieto.com](https://schmitt-nieto.com/tags/#azure-local)  
  Yes, naming my own blog first is bad form, but here I share hands-on content about Azure Local implementation and management.  
- [hybridcore.ca](https://hybridcore.ca/posts/adopting-azlocal-vms/)  
  Blog by [Tiberiu Radu](https://www.linkedin.com/in/rtiberiu/)  featuring, in my opinion, the best article on how to adopt (indirectly migrate) a VM from Hyper-V to Azure Local.
- [darifer.net](https://www.darifer.net/index.php/category/azure-local/)  
  Blog by [David Rivera](https://www.linkedin.com/in/davidriverafer) with detailed posts in Spanish on Azure Local, covering version upgrades, deployment and comparisons with Windows Server.
- [mikemdm.de](https://mikemdm.de/tag/azure-local/)  
  Blog by MVP [Michael Meier](https://www.linkedin.com/in/michael-meier-ba3b72210/) covering the topic Azure Local and AVD Labs.
- [blog.graa.dev](https://blog.graa.dev/tags/azure-local/)  
  Blog by MVP [Erik Grina Raassum](https://www.linkedin.com/in/erikgraa/) focused on Azure Local and PowerShell implementations.  
- [jtpedersen.com](https://jtpedersen.com/)  
  Blog by MVP [Jan-Tore Pedersen](https://www.linkedin.com/in/jan-tore-pedersen-4863a82/) covering Azure Local troubleshooting and insights.  
- [azurelab.blog](https://www.azurelab.blog/)  
  Italian-language blog by [Luigi Pandolfino (MVP)](https://www.linkedin.com/in/pandolfino/) and others about Azure Local and related topics.  
- [chkja.dk](https://www.chkja.dk/)  
  Blog by [Christoffer Klarskov Jakobsen](https://www.linkedin.com/in/christoffer-klarskov-jakobsen-7b168266/) featuring Azure Local implementations.  
- [thisismydemo.cloud](https://thisismydemo.cloud/tags/azure-local/)  
  Blog by MVP [Kristopher Turner](https://www.linkedin.com/in/kristopherjturner/) on Azure Local and infrastructure solutions.  
- [francescomolfese.it](https://francescomolfese.it/en/)  
  Blog by MVP [Francesco Molfese](https://www.linkedin.com/in/francescomolfese/) focused on Azure Local and IaC.  
- [auxiliumtechtalk.com](https://www.auxiliumtechtalk.com/home/categories/azure-local)  
  Blog by [Alyn Peden](https://www.linkedin.com/in/alyn-p-0989975b/) discussing real-world Azure Local scenarios.  
- [jakewalsh.co.uk](https://jakewalsh.co.uk/tag/azure-local/)  
  Blog by MVP [Jake Walsh](https://www.linkedin.com/in/jakewalsh90/) on Azure Local implementations.  
- [silviodibenedetto.com](https://www.silviodibenedetto.com/)  
  Blog by MVP [Silvio Di Benedetto](https://www.linkedin.com/in/silviodibenedetto/) on Azure Local and related topics.  
- [hciharrison.com](https://www.hciharrison.com/)  
  Blog by MVP [Lee Harrison](https://www.linkedin.com/in/lee-harrison-749b7215/) covering all things Azure Local.  
- [kennylowe.org](https://kennylowe.org/)  
  Blog by MVP [Kenny Lowe](https://www.linkedin.com/in/kennylowe1/) on Azure Local and infrastructure.  
- [erniecosta.com](https://www.erniecosta.com/blog/)  
  Blog by MVP [Ernie Costa](https://www.linkedin.com/in/erniecosta/) focusing on Azure Local, Storage Spaces Direct and services. 
- [thomasmaurer.ch](https://www.thomasmaurer.ch/)  
  Blog by former Microsoft employee [Thomas Maurer](https://www.linkedin.com/in/thomasmaurer2/) (Principal Program Manager & Chief Evangelist for Azure Hybrid) covering a wide range of Azure services, including Azure Local.  

### LinkedIn  

*Most day-to-day news on Azure Local arrives first on LinkedIn. Here are two profiles worth following.*

- [Darryl van der Peijl](https://www.linkedin.com/in/darrylvanderpeijl/)  
  One of the most active MVPs posting news and technical content. He also runs the [Azure Local Insider](https://www.linkedin.com/newsletters/7094952705042841602/) newsletter, which I recommend.  
- [Dino Bordonaro](https://www.linkedin.com/in/dinobordonaro/)  
  The MVP who brought me into this space. Practical content, including the article *[Why Expensive Azure Local Hardware Becomes Datacenter Decoration (7 Mistakes That Turn Investment Into Inventory)](https://www.linkedin.com/pulse/why-expensive-azure-local-hardware-becomes-datacenter-dino-bordonaro-mw0ie/)*.  
- [Sven Langenfeld](https://www.linkedin.com/in/svenlangenfeld/)  
  Former Microsoft Senior Azure Local Commercial Sales Specialist (DACH) who leads a large Azure Local community across technical and business topics. Founder of the LinkedIn group [Azure Local Tech Talk](https://www.linkedin.com/groups/12885745/).  
- [Manfred Helber](https://www.linkedin.com/in/manfredhelber/)  
  Germany-based MVP active in community events and live streams.  
- [Karl Wester-Ebbinghaus](https://www.linkedin.com/in/karl-wester-ebbinghaus-a41507153/)  
  Germany-based MVP who contributes extensively to the Azure Local Tech Talk channel.  
- [Flo Fox](https://www.linkedin.com/in/florianklaffenbach/)  
  Former Microsoft Senior Technical Program Manager (Azure Risk) who runs the Hybrid Friends YouTube channel.  

### YouTube  

*Channels that focus primarily on Azure Local rather than hosting only an occasional video.*

- [The Hybrid Friends](https://www.youtube.com/@thehybridfriends)  
  Practical use cases and deep dives in the Azure Local space.  
- [Manfred Helber](https://www.youtube.com/@ManfredHelber)  
  German- and English-language channel by MVP Manfred Helber featuring *Azure Local Show*, a weekly update on Azure Local news.  
- [Carsten Rachfall](https://www.youtube.com/@CarstenRachfahl)  
  German-language channel by MVP Carsten Rachfall streaming Azure Local and Azure Virtual Desktop implementations.
- [I am IT Geek - Shabaz Darr](https://youtube.com/playlist?list=PLJBGLF8tZlXNPqodqi33xXokfBH3gd4yx&si=ZByGRqDkgJlFnyRu)  
  Practical use cases by MVP Shabaz Darr covering topics like Azure Arc and Hybrid Kubernetes.  

### Github Repos & Tools

- [schmittnieto - AzSHCI (GitHub)](https://github.com/schmittnieto/AzSHCI)   
  This repository brings together multiple scripts, each with its own purpose and structure, allowing you to spin up a fully functioning Azure Local environment quickly.  
- [bfrankMS - AzureLocal_AzStackHCI (GitHub)](https://github.com/bfrankMS/AzureLocal_AzStackHCI)  
  Azure Local repository with findings on automating installations of HCI, AKS, and AVD.  
- [Azure Local Sizing Guides (GitHub)](https://github.com/jonathan-vella/azure-local-sizing-guides)  
  Azure Local Sizing Guides provides comprehensive documentation, best practices, and tools for deploying and managing Azure services, such as AKS, AVD, and Arc-enabled SQL Managed Instance, on Azure Local. This repository is maintained by [Jonathan Vella](https://www.linkedin.com/in/jonathanvella/), Senior Cloud Solution Architect at Microsoft.
- [VMWare to Hyper-V VM Conversion tool in Windows Admin Center (Tool)](https://techcommunity.microsoft.com/blog/windowsservernewsandbestpractices/introducing-the-vm-conversion-tool-in-windows-admin-center-%E2%80%93-public-preview/4446604)  
  This agentless, cost-free tool streamlines the conversion of virtual machines from VMware to Windows Server with Hyper-V.
- [S2D Capacity Calculator (Tool)](https://s2d-calculator.com/)  
  Use this Storage Spaces Direct Calculator to estimate storage capacity, resiliency, and hardware requirements for your Storage Spaces Direct (S2D) deployment.  
- [Azure Local Calculator (Tool)](https://schmitt-nieto.com/azurelocal-calculator/)  
  A calculator currently focused mainly on pricing, since storage is covered by S2D Calculator and CPU is a separate track; created by me and available open source at [Azure Local Calculator](https://github.com/schmittnieto/AzureLocal-Calculator).  
- [AVD - FSLogix Profile Status (Tool)](https://www.linkedin.com/posts/drazen-nikolic-816906142_avd-microsoft-azurevirtualdesktop-ugcPost-7364022385827557376-NEle)  
  After the deprecation of FXTray, it became difficult to check the status of FSLogix profiles. With this PowerShell script, it is once again possible to verify profile status in a simple and centralized way.



### Chats & Channels

- [Azure Local Slack Channel](https://aka.ms/azurelocal-slack)  
  Slack channel (the real Community) managed by Darryl van der Peijl that provides community support for all Azure Local questions.  

### Trainings
- [Azure Local Accreditation 2025](https://learn.microsoft.com/en-us/training/paths/azure-local-accreditation-2025/)  
  Part of the official Microsoft Learn documentation, this training path helps you get in touch with Azure Local and its core capabilities.
- [Azure Local Training](https://360.articulate.com/review/content/6c4554d6-8ccc-4b9b-bc6b-328c7429efce/review)   
  Training module covering how to deploy and register Azure Local using OEM licenses, among other key topics.  

### Events

| Name                               | Description                                                                 | Price                | Remote | Date |
|------------------------------------|-----------------------------------------------------------------------------|----------------------|--------|------|
| ~~[AVD Tech Fest - Berlin (Germany)](https://www.controlup.com/de/avd-techfest-2025/)~~ | Community-driven event focused on Azure Virtual Desktop and Azure Local integration. | ~~99 €~~ | ~~No~~ | ~~September 10-11, 2025~~ |
| [Microsoft Ignite - San Francisco (USA)](https://register.ignite.microsoft.com/) | Flagship Microsoft conference featuring hybrid cloud and Azure Local sessions. | 2325 $ | Yes (Digital pass are **Free**) | November 17-21, 2025 |
| [Microsoft Ignite 2025 - Breakout Session BRK147](https://ignite.microsoft.com/en-US/sessions/BRK147?source=sessions) | Discover what's new in Azure Local, see a live demo, and hear from a customer modernizing operations and enabling AI in a regulated environment. | Included in Ignite pass | Yes | November 18, 2025 |
| [HybrIT - Würzburg (Germany)](https://www.manfredhelber.de/hybrit-conference-2025/) | Two-day conference in **German** on Microsoft hybrid infrastructure (Windows Server, Azure Local, and Azure Arc). | 299–599 € | No | November 26-27, 2025 |


<!-- AWESOMEAZURELOCAL:END -->
---

> Contributions are welcome. Please submit a pull request or an issue with verified links or improvements.
