---
uid: About_the_Catalog_module
---

# About the Catalog module

As part of dataminer.services, the Catalog module allows Skyline customers and DataMiner Strategic Partners to browse and deploy available DataMiner connectors, packages, Visio drawings, Automation scripts, dashboards, and more.

![Catalog](~/user-guide/images/DataMiner_Catalog.png)<br>*DataMiner Catalog in DataMiner 10.4.6*

## Accessing the Catalog module

There are several ways to access the Catalog module:

- Go directly to <https://catalog.dataminer.services/>.

- Go to <https://dataminer.services>, [sign in](xref:Logging_on_to_the_DataMiner_Cloud_Platform), and click *Catalog* on the landing page.

- In DataMiner Cube, go to *Apps* > *Catalog* (from DataMiner 10.2.9/10.3.0 onwards).

> [!NOTE]
> While you do not have to sign in to view Catalog items, not all functionality will be available if you are not signed in. To sign in, click the button in the top-right corner of the Catalog UI.

## About Catalog items

A Catalog item is a small package that contains one or more artifacts that can be deployed on a DataMiner System. [Different types of Catalog items](#supported-catalog-item-types) are supported. For example, an item could be a single connector, or it could be an application package containing multiple dashboards, Automation scripts, and connectors.

### Public and private Catalog items

**Public** Catalog items are items that are available for anyone within the community to use.

**Private** Catalog items are items that are only available within your own organization. This gives users the possibility to develop app packages, Automation scripts, or any type of Catalog item and redeploy them within their organization on various systems.

### Versioning of Catalog items

Catalog items can have multiple versions. To make sure that the versioning of items is easy to understand for everyone, [Semver](https://semver.org/) versioning is enforced. Extra labels can be assigned to versions to indicate that a certain version is not an official release (e.g. 1.2.3-alpha).

> [!NOTE]
> For items of type Connector, the version must have the format mentioned under [Protocol version semantics](xref:ProtocolVersionSemantics).

### Supported Catalog item types

At present, the following types of Catalog items are supported:

| Type | Description |
|--|--|
| Solution | A DataMiner Solution is a deployable package containing a set of components as well as deployment-specific code to install those components and if applicable also automatically perform any further actions required to create a specific solution on the target DataMiner System.<br/>As such, a DataMiner Solution can be used for a broad range of purposes, from simply delivering a set of components all the way to creating a complete DataMiner setup from scratch (infrastructure as code). |
| Testing Solution | Testing solutions are DataMiner Solutions specifically designed for automated testing and validation purposes, or to facilitate and accelerate the design of other testing solutions by DevOps teams. |
| Sample Solution | Sample solutions are DataMiner Solutions that are meant to be used for training and education purposes, or as a template to boost productivity of DevOps teams to create their own DataMiner Solutions, or to serve as a reference or blueprint for best practices. |
| Standard Solution | Standard solutions are DataMiner Solutions that are out-of-the-box solutions for specific use cases or applications. They are designed to require as little configuration and setup work as possible. Standard solutions are typically owned and managed by a Product Owner, who will release updates and evolutions of the standard solutions. If you want to benefit from those future updates and new versions, you should therefore not alter or change standard solutions. |
| Visual Overview | Contains a [Microsoft Visio design](xref:visio), intended to be used for the DataMiner Visual Overview bubble-up and drill-down graphical UI. Deploying the component will make it available on the target DataMiner System, where it then needs to be assigned to the desired views, elements, or services. Optionally, you can further adapt or evolve the design to your own specific needs or preferences. |
| Dashboard | Contains a [DataMiner dashboard](xref:newR_D). This can be a standard out-of-the-box dashboard or a sample dashboard, which can for example be used for training and reference purposes or to serve as a quick start template. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| Low-Code App | Contains a [DataMiner low-code app](xref:Application_framework). This can be a standard low-code app ready to be used on any DataMiner System, or a sample low-code app, which can for example be used for training and reference purposes or as a quick start template. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| ChatOps Extension | Contains a [ChatOps](xref:ChatOps) extension, which provides new custom commands to be used in Microsoft Teams ChatOps, enabling users to interact with DataMiner through chat.  Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| User-defined API | Contains a [user-defined API](xref:UD_APIs), which adds a new endpoint to your DataMiner System tailored to a specific use case, and which enables third-party applications to consume selective data from your DataMiner System. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. You will then have to make that new user-defined API accessible by generating and sharing a token with the intended party. |
| Data Transformer | Contains a data transformer, which allows you to transform data queried from DataMiner through a [GQI data query](xref:About_GQI) prior to serving it to users in low-code apps or dashboards. Deployment of the component will make it available on the target DataMiner System, where it can be used as is, as part of your GQI data queries, or where you can further adjust it to meet your specific needs. |
| Data Query | Contains a [GQI data query](xref:About_GQI) to extract data from DataMiner, to transform it, and to serve it to users in low-code apps or dashboards. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| Life cycle Service Orchestration Script (LSO) | Contains a DataMiner Automation script designed to [manage the life cycle of a service](xref:srm_scripting#life-cycle-service-orchestration-lso-script), orchestrated by the DataMiner SRM framework. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| Profile-Load Script (PLS) | Contains a DataMiner Automation script designed to [load a standard DataMiner profile](xref:srm_scripting#profile-load-script-pls) onto a specific third-party product, leveraging the DataMiner SRM framework. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| Automation Script | Contains a general-purpose [DataMiner Automation script](xref:automation) to execute automation routines, triggered either on demand by users, based on a time schedule, or based on specific events that occur. Deploying the component will make it available on the target DataMiner System, where it can be used as is, or where you can further adjust it to meet your own specific needs. |
| Function Definition | Contains a [DataMiner function definition](xref:srm_definitions#virtual-function), which maps data and controls from a specific target DataMiner connector to generate a DataMiner function required for orchestration by the DataMiner SRM framework. Deployment of the component will make it available on the target DataMiner System. |
| SLA Model | Contains a [DataMiner Service Level Agreement (SLA) model](xref:sla), which allows you to create SLA management objects linked to your services to track the current and historical performance of your services, weighted against your actual service level agreements configured in the SLA model. Deploying the component will make it available on the target DataMiner System, allowing you to create SLA management objects based on the SLA model. SLA models provided by Skyline are subject to updates. If you want to benefit from these updates, you should therefore not alter these SLA models. |
| Enhanced Service Model | Contains a [DataMiner enhanced service model](xref:About_services#enhanced-services), which allows you to create a DataMiner enhanced service object to track the status of a service in your operation by aggregating data from various products across your operational ecosystems involved in the delivery of that service. An enhanced service, as compared to a standard service, provides real-time service-level metrics, derived from metrics of the underlying and included managed objects. Deploying the component will make it available on the target DataMiner System, allowing you to create enhanced service objects based on the enhanced service model.  Enhanced service models provided by Skyline are subject to updates. If you want to benefit from these updates, you should therefore not alter these enhanced service models. |
| Connector | Contains a [DataMiner XML connector](xref:Protocols1), integrating a specific third-party product with DataMiner for monitoring and control of that third-party product. Deploying the component will make it available on the target DataMiner System, where it can be used to create new elements. Connectors provided by Skyline are subject to updates. If you want to benefit from these updates, you should therefore not alter these connectors. |
| Scripted Connector | Contains a [DataMiner scripted connector](xref:Scripted_Connectors), enabling DataMiner to extract data from a third-party product for monitoring purposes. Deployment of the component will make it available on the target DataMiner System, where it can be used to create new elements. Scripted connectors provided by Skyline are subject to updates. If you want to benefit from these updates, you should therefore not alter these scripted connectors. |
| Ad Hoc Data Source | Contains a [DataMiner ad hoc data source integration](xref:Configuring_an_ad_hoc_data_source_in_a_query), which allows you to make data from third-party products and various data sources available for ad hoc display in DataMiner low-code apps and dashboards. Data from an ad hoc data source is not continuously extracted from the third-party product, so it cannot be used for fault management, performance management, and various other background functions in DataMiner. Deploying the component will make it available on the target DataMiner System. Ad hoc data sources provided by Skyline are subject to updates. If you want to benefit from these updates, you should therefore not alter these ad hoc data sources. |
| Best Practices Analyzer | Contains a [DataMiner Best Practices Analysis (BPA) test](xref:Running_BPA_tests), which is targeted to facilitate the management, troubleshooting, configuration, and optimization of your DataMiner System. Deploying the component will make it available on the target DataMiner System, where it can be accessed from the BPA UI on the Agents page in the System Center of the DataMiner Cube client. |
