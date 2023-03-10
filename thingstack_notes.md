<h1>Proposed Thingstack Hosting Implementation</h1>

```diff
+ Where/how does storage integration store data? 

+ Where/how is backup data is stored (not incl. storage integration)?

+ How does Dedicated Cloud handle the above two storage systems differently?

+ How is Dedicated Cloud pricing handled?

+ If we start on the Discovery plan and want to move up to standard, can we do this without modifying our application?

+ The deployment options doc (https://www.thethingsindustries.com/deployment/) lists "Custom domain name and white label console" as only available on the Dedicated Cloud plan. Does that mean we need to go with Dedicated Cloud in order to get our branding on the application  console?

+ Can you please provide a rough DFD for each Cloud plan's internal data flow? 
```

This document summarises two possible approaches to launch our IoT application to a managed SLA hosting plan with ThingStack. The full list of deployment options is broken down [here](https://www.thethingsindustries.com/deployment/).

- [Options Not Under Consideration](#options-not-under-consideration)
- [Options Considered](#options-considered)
  - [Common Factors:](#common-factors)
    - [EULA](#eula)
  - [Option 1: Cloud](#option-1-cloud)
    - [Benefits](#benefits)
    - [Cost Analysis](#cost-analysis)
    - [Security](#security)
    - [Impact To Current Report](#impact-to-current-report)
    - [Data Flow Diagram](#data-flow-diagram)
  - [Option 2: Dedicated Cloud](#option-2-dedicated-cloud)
    - [Benefits](#benefits-1)
    - [Cost Analysis](#cost-analysis-1)
    - [Security](#security-1)
    - [Impact To Current Report](#impact-to-current-report-1)
    - [Data Flow Diagram](#data-flow-diagram-1)
- [Recommendations](#recommendations)

---

## Options Not Under Consideration
Options which have been considered and discarded include: 
- "AWS Launcher" Hosting
- "Enterprise" Hosting (aka, "self-hosted")
- Remaining on "Community" level

This leaves two major options, discussed below:

---

## Options Considered

Two options are under consideration: 

[Option 1: Cloud](#option-1-cloud)  
[Option 2: Dedicated Cloud](#option-2-dedicated-cloud)

### Common Factors:
Some common factors exist between these options which are still important to note here.

#### EULA
The [ThingStack EULA](https://www.thethingsindustries.com/document/eula/) governs the legal rights of Emu while we are using Thingstack services. Important paragraphs within it are called out below:

**Applicable law**:
> ... The Agreement is exclusively governed and construed by Dutch law. If Client is a Consumer, it shall also enjoy the protection of the mandatory provisions of the law applicable where Client has its residence. Unless provided otherwise by mandatory law, any disputes arising from or in connection with the Agreement will be submitted to the competent court in the district in which TTI has its registered office. ...

**SAAS Data and Backups**:
> ... All Client Data processed through the Software will remain the property of Client. TTI will not make any proprietary claims with regard to any such Client Data. Client provides TTI with a non-transferable – and as far as necessary for performance of the Agreement – sublicensable license to use such Client Data for the duration of the Agreement, insofar this is required for the provision of the Services. TTI will make a back-up of all Client Data once every day. These back-ups are made as a precaution for technical failures or disruptions on the side of TTI. Unless agreed otherwise by way of a separate service level agreement, TTI does not provide a back-up service and is not held to restore specific Client Data or on Client’s request (for example when Client has accidentally removed specific Client Data). If TTI nevertheless decides to honor such a request, it may charge Client with all reasonable costs incurred. Upon termination of the Agreement, TTI will have the right to remove or destroy all Client Data. TTI may, at the request of Client, assist in exporting Client Data. However, Client acknowledges that it remains solely responsible for making back-ups of any Client Data it wants to keep past the date of termination of the Agreement. ...



--

### Option 1: Cloud

#### Benefits

#### Cost Analysis

For more detailed info see the ThingStack plan breakdown [here](https://www.thethingsindustries.com/stack/plans/).

The "Discovery" level plan may be viable during the POC. This level is free.

However, as the Discovery plan limits us to one gateway and a maximum of ten devices, if the POC is successful we will need to immediately transition to the "Standard" level plan. This costs €190/month (~$306/month). This would be an ongoing cost.

#### Security

Even without the storage integration enabled, ThingStack stores data for short periods of time. From their [SLA](https://www.thethingsindustries.com/document/sla/):

> TTI creates daily backups of critical (meta)data, including event payloads, security keys, and data about applications, users, gateways, devices and device states. Backups are stored up to 7 days without storage integration enabled and used for possible disaster recovery from TTI's side...

#### Impact To Current Report

#### Data Flow Diagram

--

### Option 2: Dedicated Cloud

#### Benefits

#### Cost Analysis

#### Security

#### Impact To Current Report

#### Data Flow Diagram

---

## Recommendations