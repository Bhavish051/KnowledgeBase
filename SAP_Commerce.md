Product Content Management, Customer Experience, Order Management and Commerce Capabilites into one platform: SAP Commerce
Accelerators: Ready to use commerce solutions, Ready Made storefronts

Platform: Core of Commerce Cloud
Product Content Mangement: Product related info
Web Content Management: Websites and stuff
Customer Support: Returns, cancellations etc
Order: Order Fulfilment 
Store Locators
Search Functionality
Payment frameworks

B2C Accelerator: For customers clothing etc
Checkout Process comes with every accelerator

B2B Acceleratior: B2C Plus Some more such as Order Approval, Quote Mangement, Scheduled order replenishment, Self-service Organization Management
Option to schedule replishment such as a weekly delivery etc

Web Content Mangement: SAP Experience Management
Smart Edit: Drag and drop components
Advanced Edit for components shared accross multiple pages
Customise components for a target group of customers

Universal Back Office:  Search for managing search results
                        Admin Cockpit for technical information
                        Customer Support for customer information
                        Order Fulfilment for order related information


Adaptive Search Module for personalised search profiles

Platform: Main funcationality
            Persistence framework for data storing
            Business services: Cart handling, Back orders
            System services: Model handling, Session handling
            Infrastructure services: Export, Import, Internalization

            Extensibilty: 
                Module: Set of Extensions



SAP Commerce uses Azure to host the web applications and the servers which can be remotely logged in using just a browser

3 Environments
Dev: 250GB 2*F8 VMs 1*S1
Staging: 250GB 3*F8 VMs 1*S3
Production: 500GB-1TB 4*F8 VMs 1*P1

Use build manifest.json file to configure which properties to be used for dev, test and prod env

3 Layers
Commerce Application: Layer where customization is done
Environment: allocation of platform resources and services to run application
Infrastructure: Provision Envirnment in Azure


Runtime Architecture: 
Cloud Portal: WebUI to set up and deploy SAP Commerce in cloud
Cloud Automation Engine: Core, Automatic DevOps Pipeline: Environment provisioning, Build and deployment of SAP Commerce solution, Scaling


4 Layers of General Software
Presentation
Business
Persistence
Database

Build and Deploy Process: 
Link a git repo
Builds a docker image from the git repo and the SAP Code Repo
One for each component such as storefront, Solr, Apache,etc
Cloud poral for basic build information such as git repo etc
Manifest.json at root of repo for build config
Operator is responsible for building docker container into a kubernetes cluster on top of VMs in Azure
Horizontal Scaling only determined by application alerts automatically

Cloud Portal: Self Service Portal for customers
Cloud Automation Engine handles: Environment Management, Build Management, Deployment Management, Logging, Backups and Snapshots, Disaster Recovery, Scaling, Monitoring 

2 Types of accelerators
Industry Accelerators: Specific to a particular industry like Telco, Utilities, Financial, Citizen Engagement, Travel
Normal Accelerators: B2B or B2C


Software Architecture: 
Azure for cloud infrastructure
SAP Business Technology Platform to host SAP applications 
Kubernetes: To manage Docker nodes


Spartacus JS for decoupled Frontend
Data Hub for to import/ export master data

Cloud Hot Folders: File-based integration strategy for SAP Commerce Cloud for storing data in Azure Blob Storage which is then passed into the backend which gives the result to SAP Commerce Cloud.
FileName mapping is important as otherwise if no match is found then Spring will keep on trying to match the same file and not moving ahead or change cloud.hotfolder.storage.header.router.resolution.required .


SAP Commerce Accelerator

Web Request Application Server Node
Presentation Layer:
* Servlet Components: Filters, Listeners, Dispatcher Servlet, Media Servlet
* Spring MVC: Dispatcher Servlet, Controller, Interceptors
* View: JSP/ JSTL
Service Layer:
* Facades
* Services
* Data Access Objects (DAO)
Persistence Layer:
* items.xml: Types of data access objects 

Back Office Application Server Node
Administration
* Management Console
* Admin Web
* Business and Admin Cockpits ex Admin cockpit, Product cockpit, etc
* Customer Service Cockpit
Service Layer
* Cron jobs: Tasks which are regularly done after some time ex backups, updating products etc
* Task Process and Actions: Enalbe time based events or event based actions
* Hot Folder Data import
* DAO
* SOLR Indexer
Persistence Layer:
* items.xml: Types of data access objects 


CMS: Content Mangement System
CMS Cockpit handles what data is shown to the customer on the website

ERP Is the Product Data Source otherwise there has to be a seperate systme with the product etc master data to be integrated with SAP Commerce

Uses a 3rd party payment service provider 2 options: 
* Either route the use to the 3rd party site starightaway to avoid handling sensitive data
* Either get credit card data from use and send it as a form to the 3rd party service provider

SAP Commerce has a Fraud Detection service in built which checks the order and the customer and marks a score and checks it 

B2B
4 Roles
* Admin b2badmingroup
* Manager b2bmanagergroup
* Approver b2bapprovergroup
* Customer b2bcustomergroup

Add functionalities in localextensions.xml

ant modulegen to create custom modules from templates
ant extgen to create custom extensions from templates

add <meta key="extgen-template-extension" value="true"/> to the extensioninfo.xml file to enable to make an extension or module into a customer one

Catalog Versions are made of multiple categories,
A Catalog is made of different catalog versions and only one catalog version can be active at a particular time.
For multiple webfronts set up multiple catalogs

PCM: Product Content Management
PIM: Product Information Management

PCM to hold basic data like title and description whereas PIM has a wider set of features to distribute the data into retail and marketplace channels

SAP Product Content Hub:
    PIM Component 
    Cloud Data Feed Management and Data Syndication service