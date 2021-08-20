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


3 Layers of General Software
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
