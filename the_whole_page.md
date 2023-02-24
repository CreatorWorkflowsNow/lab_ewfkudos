![](RackMultipart20230224-1-8f1srq_html_a850bf160c903d38.png)

# AppEngineStudio – System AdministratorGuide
{: .fs-10 }

## Tokyo
{: .fs-10 }

##

## Release
{: .fs-10 }

**Table Contents**

[AppEngineStudioOverview3](#_bookmark0)

[PersonasandRoles4](#_bookmark1)

[PrepareenvironmentsforAppEngineStudio6](#_bookmark2)

[Reviewplatformrequirements6](#_bookmark3)

[Defineinstancestrategy6](#_bookmark4)

[HowdoIinstallAppEngineStudio?7](#_bookmark5)

[Opt-inandmanageentitlements7](#_bookmark6)

[Install AppEngineStudio application7](#_bookmark7)

[HowdoIconfigure AppEngineStudio?8](#_bookmark8)

[AppEngineStudioGuided Setup9](#_bookmark9)

[PipelineandDeploymentGuidedSetup15](#_bookmark10)

[ApplicationIntakeGuidedSetup26](#_bookmark11)

[How doImanageAppEngineStudioaccess?29](#_bookmark12)

[Grantandrevokeaccess29](#_bookmark13)

[Managecollaborationanddelegateddevelopment30](#_bookmark14)

[HowdoImanage applicationintakerequests?31](#_bookmark15)

[Configuretheapplicationintakerequestform32](#_bookmark16)

[Accessandreviewapplicationintakerequests32](#_bookmark17)

[ChoosingtherightapplicationsforAppEngineStudio32](#_bookmark18)

[HowdoImanageapplicationdeploymentrequests?33](#_bookmark19)

[Promoteanapplicationinapipeline34](#_bookmark20)

[Reviewandtestanapplication35](#_bookmark21)

[Rejectanapplication35](#_bookmark22)

[HowdoIdeployapplicationstoproductioninAppEngineStudio?36](#_bookmark23)

[HowdoIcreateapplicationtemplates?37](#_bookmark24)

[HowdoImanageAppEngineStudioproperties and processes?38](#_bookmark25)

[FAQs40](#_bookmark26)

# AppEngineStudioOverview

#### _The __content__ in __this__ guide __applies__ to __App__ Engine __Studio__ Version__22.0.3_

App Engine, powered by the Now Platform, fuels rapid delivery of Creator Workflows with great experiences for everyone. With more people building with less complexity, App Engine allows developers to create low-code apps fast, and safely scale cross-enterprise experiences thatusers love.

AppEngine Studio isavailable withAppEngine and isdesigned from the ground up to address low-codedevelopment needs. AppEngine Studio enables professional developers, line of business technologists (citizen developers), and low-code developers to build applications individually orincollaborativeteams onthesameplatform,resultinginfastertimeto valueand better applications that scale without sprawl.

With guidance-driven development flows and pre-configured application templates, developersacrosstheenterprisecanbuildanddeliverappsquickly.Developerscanleverage manyout-of-boxcomponents availablethrough drag-and-dropinterfaces tocreatefulfilling userexperiencesthatarecriticaltoend-useradoption.

Administratorscontrolwhichapplicationstodeploybyreviewingandtestingapplications createdbyAppEngineStudiodevelopers–andbydelegatingdevelopmenttobusinessunitsin yourorganization,administratorsarefreeduptoaddressmorestrategic,system-wideissues.

![](RackMultipart20230224-1-8f1srq_html_c01da20658fb5bfd.jpg)

_\* App Engine Studio_ _a __p__ p __l__ i __c__ a __t__ i __o__ n __t__ e __m__ p __l__ a __t__ e __s__ are not captured in update sets, however_ _m __o__ d __i__ f __i__ c __a__ t __i__ o __ns__ to_ _t __e__ m __p__ l __a__ t __e__ s__will be captured_

AppEngine Studio isthe ideal ServiceNow developmentenvironmentfor no-codeand low- code application development for developers of all skill levels. Pro-code developers can useApp Engine Studio as a starting point for application development and easily transfer their applicationstoServiceNowStudiowhenadvancedconfigurationsarenecessary.

Sincedevelopmentissupportedbetweenthetwoenvironments,low-codeandpro-code developerscan easily collaborate to deliver custom applications.

Allconfigurationstoanapplication,whetherperformedinAppEngineStudioor ServiceNow Studio,canbecapturedinthesameprivateapplicationscope.Applicationartifactsconfigured in App Engine Studio can also be managed in ServiceNow Studio. However, some application artifacts canonlybe accessedandconfigured inServiceNow Studio. These include business rules,notifications,andserviceportalpages.

# Personas and Roles

**System**** Administrator**

Responsibilities:

- InstallandconfigureAppEngineStudioanddependencies
- DefineEnvironmentsandconfigurePipelines
- ProvisionAppEngineStudioadministratorgroupaccess
- UpgradetheAppEngineStudioapplication,whenapplicable
- Define guardrails for which App Engine Studio Administrators can approve or reject application intake requests
- Collaborate with professional ServiceNow developers to create Instance Scandefinitions for the platform
- Collaborate with App Engine Studio Administrator(s) to resolve application conflicts that arise on the platform

Rolerequired: **admin**

**App**** Engine ****Studio**** Administrator**

Responsibilities:

- ManageAppEngineStudioprocessesandproperties
- Review and approve / reject submitted application requests, based on intake guardrails defined by System Administrator
- ProvisionAppEngineStudiouseraccess
- ReviewsubmittedAppEngineStudioapplications
- ManageDeploymentRequests
- ManagepromotionofAppEngineStudioapplicationsacrossinstances
- ExecuteATFtests/ suitesintestinginstance

- EnsureInstanceScanisrunwithproperdefinitions
- Collaborate with System Administrator to resolve application conflicts that arise on the platform

Role(s)required:

- **sn\_app\_eng\_studio.admin**
- **atf\_test\_designer**
- **scan\_admin**

**Professional**** ServiceNow ****Developer**

Responsibilities:

- BuildandtestapplicationsinServiceNowStudioandAppEngineStudio
- Collaborate with citizen developers, on an as-needed basis, to deliver applications in App Engine Studio, including:
  - Ensureapplicationdevelopmentandorganizationalbestpracticesare followed by citizen developers
  - AssistinreviewandtestingofsubmittedAppEngineStudio applications
- Buildcomplexconfigurations involvingUIBuilder, MobileAppBuilder, FlowDesigner, or other builder tools
- Create ATFtests/suitesfor applications
- Collaborate with system administrator to create Instance Scan definitions for the platform

Role(s)required:

- **delegated\_developer**
- **sn\_app\_eng\_studio.user**
- **atf\_test\_admin**
- **scan\_admin**

**Low-Code /**** Citizen ****Developer**

Responsibilities:

- SubmitrequestsfornewcustomapplicationstobuildinAppEngineStudio
- UnderstandServiceNowandapplicationdevelopment bestpractices
- BuildandtestapplicationsinAppEngineStudio
- SubmitdevelopedAppEngineStudioapplicationsforITreview
- Maintain and modify the application during its lifecycle if determined during the intake process

Rolerequired: **sn\_app\_eng\_studio.user**

# PrepareenvironmentsforAppEngineStudio

Before installing App Engine Studio, review all platform requirements and define an organizational instance strategy to prepare for successful installation and configuration.

## Reviewplatformrequirements

- AppEngineStudioVersion **22.0.3**
- AppEnginelicenserequired

- _Contact __your__ ServiceNow __Account__ Manager __for__ a __dd__ it __io__ n __a__ l __information__ on App Engine, or see_ [_ServiceNow App Engine_](https://www.servicenow.com/products/now-platform-app-engine.html)

- InstancesmustbeonTokyorelease
- **admin** role is requiredinall instances toinstall AppEngine Studio and dependent applications from the ServiceNow Store

## Defineinstancestrategy

WhendefiningtheinstancestrategyforAppEngineStudio,itisrecommendedtoleverageone production instance and at least two sub-production instances – however App Engine Studio cansupport any number of sub-productioninstances as part of aninstance strategy.

Applicationsaredeployedtotheproductioninstanceoncedevelopedandsuccessfullytested in sub-production instances. One sub-production instance will serve as the development environment, and the other as the test environment.

If your organization uses sandbox or staging environments in addition to test and development, theycanbeincorporatedtotheinstancestrategyaccordinglybasedonorganizationalneeds.

![](RackMultipart20230224-1-8f1srq_html_9df5e1fc96e64b47.png)

_E __x__ a __m__ p __l__ e __instance__ strategy __with__ one __p__ r __o__ d __u__ c __t__ i __o__ n __instance__ and __three__ sub- __p__ r __o__ d __u__ c __t__ i __o__ n__instances_

Sub-production instances that are most similarly configured to your production instance are the best candidates for test and stage environments. This way, administrators can more accurately find issues that may arise if the application is deployed to production.

_For __more__ information,__see_[_Product__Documentation: __Instance__ strategy __for__ App __Engine__ Studio_](https://docs.servicenow.com/csh?topicname=aes-instance-strategy.html)

# HowdoIinstallAppEngineStudio?

## Opt-inandmanageentitlements

BeforeinstallingtheapplicationfromtheServiceNowStore,verifytheinstancehasvalid ServiceNow entitlements.

IntheServiceNowStore,usethesearchcriteriatofindAppEngineStudio.

![](RackMultipart20230224-1-8f1srq_html_7f48982365c8283e.png)

Click **Opt-in** andagreetotheServiceNowtermsandconditionstoverifyentitlements.

Click **Manage**** Entitlements **andsetthe'EntitlementType'valueto** Entitle ****all**** Instances**(_if __you prefer__ to __manually__ select __which__ instances __which__ will __be__ affected, __select__ Entitle_ _Selected_ _Instances)._

## InstallAppEngineStudioapplication

ToinstalltheAppEngineStudioapplication(_ **com.snc.app-engine-studio** _),logintoyour developmentinstanceandnavigatetotheServiceNowStore.

UsethesearchcriteriatofindtheAppEngineStudioapplication.Click **Install**** / ****Update**** All**.

![](RackMultipart20230224-1-8f1srq_html_427cf7485e3d8a66.jpg)

The App Engine Studio bundle will be installed in the development instance– including the App EngineStudioapplication andalldependentapplications.

Repeatthisprocesson allinstancesforcloningpurposes.

_For __more__ information,__see:_

- [_ServiceNow __Store:__ In __s__ t __a__ ll __a__ ServiceNow__Product_](https://store.servicenow.com/%24appstore.do%23!/store/help?article=KB0030186)
- [_Product __Documentation:__ Install __App__ Engine__Studio_](https://docs.servicenow.com/csh?topicname=install-aes.html)

# HowdoIconfigureAppEngineStudio?

![](RackMultipart20230224-1-8f1srq_html_7fdebf8d2db10f64.jpg)

_ **\*\*** __Repeat__ steps __across__ a __ll__ sub- __p__ r __o__ d __u__ c __t__ i __o__ n __instances,__ as__necessary_

_ **Note:** __If__ you __plan__ on cloning your production __instance to one or more sub-production__ instances,_ _in __s__ t __a__ ll __a__ ll __App Engine Studio plugins on_ _a__ ll __instances prior to cloning, and enable ATF and Instance Scan properties in your production instance. Additionally, the AEMC plugin must be installed on_ _a__ ll__instances to appropriately collect application and developer data on development. For more information, see_ [_Product Documentation: System clone_](https://docs.servicenow.com/csh?topicname=c_SystemClone.html)

TheAppEngineStudiobundlehasthreeGuidedSetupmodulestoassistinconfiguration:

-
### AppEngineStudioGuidedSetup

  - Configurefoundationalapplicationcomponentsandprovisioninitialuseraccess
-
### PipelineandDeploymentGuidedSetup

  - Configurepipelinestodeployapplicationsacrossinstanceswithconfidence
-
### ApplicationIntakeGuidedSetup

  - Configureapplicationintakecatalogitemandprocesstoenablebusinessusersto submitapplicationrequestsfromanexistingserviceportal

_ **Note:** _ _App Engine Management Center is dependent on the configuration of Pipelines and Deployment __Guided__ Setup, __and__ optionally __Application__ Intake __Guided__ Setup_

_For __more__ information,__see_[_Product__Documentation: __Using__ guided__setup_](https://docs.servicenow.com/csh?topicname=guided-setup.html)

**App**** Engine ****Studio**** Guided ****Setup**

Navigate to **App Engine Studio \> Configuration \> Guided Setup** in your development instance to accesstheAppEngineStudioGuidedSetup.

![](RackMultipart20230224-1-8f1srq_html_dbb984441261522f.png)

_ **Note** __: Before__ beginning __App__ Engine __Studio__ Guided __Setup,__ ensure __your__ application __scope__ is __set__ to_

'_App __Engine__ Studio'. __If__ not, __use__ the application __picker__ to __change__ the current __session's__ scope_

![](RackMultipart20230224-1-8f1srq_html_43882ff7b99a542e.jpg)

1. **Review**** and ****set**** up ****tooling**** in ****the**** development ****instance**

Reviewandupdate AppEngineStudiodeveloperaccesstobuildertoolsduring development.

  1. **Connect**** spokes ****in**** development**

AspokeisascopedapplicationthatcontainsFlowDesignerorIntegrationHub actions or sub-flows.

SystemAdministratorscanconnectIntegrationHubspokestoAppEngineStudio, allowingdeveloperstointegratecustomapplicationswiththird-partysystems.For example – connecting the Slack spoke allows developers to post a message containingIncident details toaspecificSlackchanneleachtimea highpriority Incident is created.

ManyIntegrationHubspokesareavailable,butnot allneedtobeconnectedto AppEngineStudio.Reviewsomeofthecommonspokesbelowandinstallbased on organizational needs.

| **IntegrationHubspoke** | **Installingthisspokeprovidesdevelopers…** |
| --- | --- |
|
Microsoft Teams | Actions to support cross-functional communications and collaborations in Microsoft Teams. |
|
Slack | Actions to automate the management of Slack channels,users, and software subscriptions. |
| --- | --- |
|


Jira |
ActionstoautomatetasksinJiraformanagingusers,issues, projects,and software development lifecycle.Synchronize data in ServiceNow with Jira to increase collaborationbetweenServiceNowusersandDevOpsteams. |
| --- | --- |

|
Gmail | Actionsto automateemailand labelmanagementin GoogleGmail. |
| --- | --- |
|
MicrosoftAzureAD |
Actions to automate Microsoft Azure Active Directory tasks for user management, authentication, and group membership. |
|
Twitter | Actions to automateposting messages and media content to a corporateTwitter news feed. |
|
Microsoft365 Excel | Actions to automate worksheet, table, and cell managementin Microsoft Excel. |

Thisstepisnotrequiredaspartoftheinitialapplicationsetup.

Asyourorganization'scitizendevelopmentprogrammaturesandscales, additional spokes can be installed and connected based on application demand and use cases.

_For __more__ information __on__ integrations __with__ third-party __systems,__ see_[_Product_](https://docs.servicenow.com/csh?topicname=integrationhub.html)[_Documentation: Integration Hub_](https://docs.servicenow.com/csh?topicname=integrationhub.html)

  1. **Review**** Flow ****Designer**** access ****settings from**** App ****Engine Studio**** in ****development**

Reviewandupdate AppEngineStudiodeveloperaccesssettingstoFlow Designer Resources and update as necessary.

DeveloperscanleverageFlowDesignercapabilitieswhilecreatinglogicand automation for custom applications.

Consider restricting developer access to Flow Designer Resources using content filtering for Flow Designer. This allows administrators to manage access to Flow Designer resources and specify which features App Engine Studio users can leverage while building applications.

![](RackMultipart20230224-1-8f1srq_html_21b6a3a9ae1ecba3.jpg)

Thisstepisnotrequiredaspartoftheinitialapplicationsetup.

FlowDesigneraccessfromAppEngineStudiocanbeupdatedlatertoprovide developerstheeditingcapabilitiesthatbestsuittheirexperienceandneeds.

_For more information on Flow Designer resources, see_ [_Product Documentation:_](https://docs.servicenow.com/csh?topicname=content-filtering-flow-designer.html)[_Content Filtering for Flow Designer_](https://docs.servicenow.com/csh?topicname=content-filtering-flow-designer.html)

  1. **Review**** Service ****Catalog**** access ****settings**** in ****development**

ReviewAppEngineStudiodeveloperaccess totheCatalogBuildertool's catalog item templates and catalogs / categories,and update access as necessary.

By default,App EngineStudiodeveloperscan leveragecatalogtemplatesto quickly create record producers or catalog items. Developers can also publishcatalog items to anycatalog. If youwishto limit access to templates or restrict publishingaccesstocatalogsorcategories,updatetheaccessaccordinglyin Catalog Builder.

![](RackMultipart20230224-1-8f1srq_html_f6f632ff36ef394d.png)

Thisstepisnotrequiredaspartoftheinitialapplicationsetup.

Catalog access fromAppEngine Studio canbe updatedat alater point to modify developer access to App Engine Studio catalogs, categories, and catalog templates.

_For more information __on__ creating or editing_ _c __a__ t __a__ l __o__ g __items,__ see_ [_Product_](https://docs.servicenow.com/csh?topicname=catalog-builder.html)[_Documentation: Catalog Builder_](https://docs.servicenow.com/csh?topicname=catalog-builder.html)

  1. **Configure**** Instance ****Scan**** definitions**

Deploy custom applicationswith confidence bysetting up Instance Scan definitions to monitor instance health throughout the deployment process. Instance scans interrogate your instance for configurations and health issues, allowing administrators an opportunity to address best practices and to avoid similar configuration issues in the future.

Instance Scan definitions are executed automatically when App Engine Studio applications are promoted to the **Testing** instance. Instance Scan results will be loggedintheNotessectionoftheDeploymentRequestrecord.

TheAppEngineStudioapplicationdoesnotshipwithanyout-of-boxInstance Scandefinitions(howeverafewInstanceScandefinitionsareinstalledwiththe Deployment Pipeline plugin to run basic performance checks).

Work with professional ServiceNow developers to configure Instance Scan definitions and enforce best practices in your environments.

![](RackMultipart20230224-1-8f1srq_html_fedff5b2e274543c.jpg)

#### _Enable and configure Instance Scan properties in your production instance if you_ plan to clone!

_For __more__ information __on__ managing __instance__ health __scans,__ see_[_Product_](https://docs.servicenow.com/csh?topicname=hs-landing-page.html)[_Documentation: Instance Scan_](https://docs.servicenow.com/csh?topicname=hs-landing-page.html)

1. **Set**** up ****user**** access**

ConfiguretheadmingroupandothergeneralsettingsforAppEngineStudiousers.

  1. **Set**** up ****administrator**** group ****in**** development**

Configure App Engine Studio administrator group membership in the developmentinstancetomanagedevelopmentactivitiesthatoccurinthe development environment.

![](RackMultipart20230224-1-8f1srq_html_2f90ed05737ac883.jpg)

While development activities will be managed in the development instance, administrators manage application intake, collaboration, and deploymentrequests in production.

Groupmembership doesnotsyncacross instances;therefore,system administratorsarerequiredtoaddusersinboththedevelopmentandproduction instances.

_ **Note** __:__ Group __membership__ does __not__ sync __across__ instances, __therefore__ App __Engine Studio__ administrator __group__ membership __will__ also __need__ to __be__ provisioned __in__ the_ _production __instance__ as __part__ of __the__ Pipelines __and__ Deployment __or__ Application Intake Guided Setup activities_

  1. **Grant**** access ****to**** current ****developers**** in ****development**

Allow existing application developers who are already assigned the **delegated\_developer** role access to the App Engine Studio application by adding them to the 'App Engine Studio Users' assignment group.

_ **Note:** __If__ you __wish__ to __grant multiple__ developers access at one __time, advance__ to__the next step to manage access more efficiently_

  1. **Grant**** access ****to**** other ****users**** in ****development**

After provisioning access for existing developers, grant App Engine Studio access to other users within the organization by adding them to the 'App Engine Studio Users' group.

![](RackMultipart20230224-1-8f1srq_html_69e7adfdf425b772.png)

**Pipeline**** and ****Deployment**** Guided ****Setup**

OnceAppEngineStudioGuidedSetuphasbeencompleted,administrators mustcompletethe Pipeline and Deployment Guided Setup activities.

Pipelinesenableyoutoautomatethepropagationandinstallationofyourapplicationsfrom one instance to another. Pipelines are powered bythe ServiceNowCI /CD spoke, which enables you to automate processes such as publishing applications to the application repository,installingthemontargetinstances,andrunningATFtestsand/orinstancescans.

ToaccessthePipelineandDeploymentGuidedSetup,navigateto **App**** Engine ****Studio**** \> Pipelines ****and**** Deployment ****\>**** Guided ****Setup**.

PipelineandDeploymentGuidedSetupactivitiesdonotsyncacrossinstancesandPipeline configurationactivitiesarerequiredonallinstances(productionandsub-production).

Refer to the process flow on page **9** for an overview of the Pipeline and Deployment GuidedSetup.

![](RackMultipart20230224-1-8f1srq_html_c89fcf3874e23c1b.jpg)

_ **Note** __:__ Before __beginning__ Pipelines and __Deployment Studio__ Guided __Setup,__ ensure__your_ _application_

_scope is set __to '__ **Deployment** __**Pipeline**__'. If not, use the__application picker to change the current session's scope_

![](RackMultipart20230224-1-8f1srq_html_ea716e3330d82282.png)

1. **Configure**** your ****production**** instance**

In the production instance, complete the following steps to configure environments anddeploymentpipelinestostreamlineyourapplication deploymentprocess **.**

**Complete**** these tasks ****only**** if ****you**** are ****logged**** into your ****production**** instance.**

  1. **Install 'Deployment**** Pipeline' ****plugin**** in ****production instance**

ToinstalltheDeploymentPipelineplugin,(_ **com.snc.deployment-pipeline** __)_, login to your production instance and navigate to **System Definition \> Plugins.**

Usethesearchcriteriatofindtheapplication.Click **Install**.

![](RackMultipart20230224-1-8f1srq_html_f385314bae755024.png)

_ **Note:** __If__ you __have__ already __installed__ the __App__ Engine __Studio__ bundle __in__ the development instance and promoted up to production, skip this step_

  1. **Configure**** credentials ****in**** production ****instance**

Credentials allow your production instance to communicate with sub- production instances.

In production, navigate to Connections & Credentials \> Connection &CredentialAliases.

OnlyusersassignedtheadminrolecancreateandupdateCredential Alias records.

![](RackMultipart20230224-1-8f1srq_html_a7beafa98433e87.png)

CredentialAlias

| Field | Description |
| --- | --- |
| Name | NameoftheCredentialAlias.ThisaliasassociatestoCredentialdata only and resolves the application integration for each environment.
An alias can only contain alpha, number, or underscorecharacters.Thisshouldbeaneasilyidentifiablename,asitwillbe referenced when creating Environment records in later steps (PipelineCredentials, |
| Type | Ensurethe'Type'valueissettoCredentialwhencreatingCredentialAliasrecordsforAppEngine Studio. |
| --- | --- |

|
 | The default value is Connection and Credentialand will need to be updated. |
| --- | --- |
| Application | The application scope against which the CredentialAlias is assigned.Ensure the value in the 'Application' field shows as App Engine Studio. Ifthe'Application' field is not populating as expected, use the application picker to change the current session's scope. |
| ID | TheuniqueidentifierfortheCredentialAliasrecord.This value auto-populates after record creation based on the format scope\_name.alias\_name and is read-only. |

Basedonthecredentialinformation,taketheappropriateapproachin configuring Credential Alias records:

- If all environments in the Deployment Pipeline will use the samecredentialinformation(sameusername/password),thenonlyoneCredentialAliasrecordwillbeconfiguredinproduction
  - i.e.,singleCredentialAliasrecordnamed'_Pipeline__Credentials'_
- However, if eachenvironment inthe Deployment Pipeline will use different credentials (different usernames / passwords), then CredentialAlias records will be created for each instance in the production instance
  - i.e.,multipleCredentialAliasrecords named'Dev Credentials', 'Test Credentials', 'Stage Credentials', and 'Prod Credentials'

OncethenecessaryCredentialAliasrecord(s)havebeencreated,navigate

tothe'Credentials'RelatedListandclickNewtoaddcredentialdetails.

Select Basic Auth Credentials to populate the Basic Auth Credentialform (currently,this is theonlyCredentialtypesupportedbyAppEngine Studio).

![](RackMultipart20230224-1-8f1srq_html_1a2d2f11c19c8bca.jpg)

It is recommended to use a username / password for a service account sothat the password does not expire or change. The account must exist in thetarget instance(s) and have admin permissions.

![Shape3](RackMultipart20230224-1-8f1srq_html_18bf0cd24437eb87.gif)

_For __more__ information,__see_[_Product__Documentation: __Create__ a __Connection__ &_](https://docs.servicenow.com/csh?topicname=connection-alias.html)[_C __re__ d __e__ n __t__ i __a__ l__Alias_](https://docs.servicenow.com/csh?topicname=connection-alias.html)

  1. **Configure**** environments ****in production**** instance**

Set up and configure the environments that will be included within your pipelines. These will be referenced when building your pipelines.

Your production instance is where your pipeline configurations reside and will be your controller instance.

**The****'Is ****Controller?'**** box ****will**** be ****checked**** on ****your**** production ****instance**** only. ****This**  **box**** will ****be**** unchecked ****for**** all ****sub-production**** Environment ****records.**

![](RackMultipart20230224-1-8f1srq_html_1287913cf74d1d42.jpg)

**Environments**

| **Field** | **Description** |
| --- | --- |
| Name | Nameoftheenvironment. |
| InstanceType | PurposetheinstanceservesintheDeploymentPipeline(i.e., sandbox, development, testing, staging, production). |
| --- | --- |
| InstanceURL | URLfortheinstance.Mustbegin with **http://** or **https://** |
| --- | --- |
| InstanceID | Auto-generatedIDvaluebased onInstanceURL |
| --- | --- |
| Application | ApplicationscopeagainstwhichtheEnvironmentisassigned.
Ensure the value in the 'Application' field shows as **App Engine Studio**. If the 'Application' field is not populating as expected, use theapplicationpickertochangethecurrentsession'sscope. |
| --- | --- |
| Instancecredential | ID of the CredentialAlias record (displays as **scope\_name.alias\_name** ). This should point to the CredentialAlias recordforthe environmentbeingsetup.
Forexample,creatinganEnvironmentrecordforadevelopment instance: |
| --- | --- |

|
 |
- **Name** :MyCompany'sDevInstance
- **Instance**** Type: ****'** Development'
- **Instance**** URL:**[https://mycompanydev.service-now.com](https://mycompanydev.service-now.com/)
- **Instance**** Credential:**DevAESPipelineCredential
- **Is**** C ****o**** n ****t**** r ****o**** l ****l**** e ****r**?:Unchecked
 |
| --- | --- |
| IsController? | IndicatestheControllerinstanceofapipeline.
The Controlleris the instance where pipeline configurations are captured, sub-flows run, and where all App Engine Studio requests arecreated.Thisfieldshouldonlybe checkedforaninstance oftype **Production**! |

_For more__information, see_[_Product__Documentation: __Define__ environments_](https://docs.servicenow.com/csh?topicname=create-environment.html)

  1. **Configure**** pipelines ****in**** production ****instance**

Apipelinedefinesthepathanapplicationtakesfromthedevelopmentto productionenvironmentsandallowsadministratorstoquicklymove applications across instances.

Set up and configure your pipelines by specifying the environments to include along with their position in the pipeline.

![](RackMultipart20230224-1-8f1srq_html_3d4aec2ef344b74b.png)

**Pipelines**

| **Field** | **Description** |
| --- | --- |
| Name | Nameofthepipeline. |
| PipelineType | Purposeofthedevelopmentpipeline. |
| --- | --- |
| SourceEnvironment | The environment where development activities take place in the deploymentpipeline. |
| --- | --- |

|
 |
EachpipelinemusthaveauniqueSourceenvironment. |
| --- | --- |
| Application | ApplicationscopeagainstwhichthePipelinerecordisassigned.
Ensure the value in the 'Application' field shows as **App Engine Studio**. If the 'Application' field is not populating as expected, use theapplicationpickertochangethecurrentsession'sscope. |
| Active | Optiontoactivatethepipeline.
The 'Submit' button will not beavailable forApp Engine Studio developers unless there is an active pipeline where the source environment is the instance where the App Engine Studio application is installed. |

Onceapipelinehasbeencreated,usethe **Pipeline**** Environments ****Order** RelatedList onthe Pipeline recordto configure the instance order for the pipeline. Create a record in the related list for all instances _except_the development instance and specify the environment's order within the pipeline.

Application movement across pipelines is dictated by the order of the environments inthePipeline Environment Orderrelatedlist,andapplications arepromotedbasedonascending'Order'values.

Besuretheenvironment orderisconsistent withthedefinedinstancestrategy. The production instance should have the highest 'Order' value _(i.e., Testing: 100, Staging: 200, Production: 300)._

![](RackMultipart20230224-1-8f1srq_html_d1e5f33a2607b146.jpg)

_ **Note:** __Since__ the __development__ environment __is__ already __identified__ as __the__'Source Environment' on the Pipeline record, a Pipeline Environment Order related record is not required_

**Pipeline**** Environment ****Orders**

| **Field** | **Description** |
| --- | --- |
| Pipeline | Referstothepipelinetype. |
| Environment | Theenvironmentbeingaddedaspartofthedeploymentpipeline. |
| --- | --- |
| Order | Orderinwhichtheenvironmentexistsinthepipeline.
Applicationsmovethroughthepipelineinisascendingorder. |
| --- | --- |
| Application | Application scope against which the Pipeline Environment Order record is assigned.
Ensure the value in the 'Application' field shows as **App Engine Studio**. If the 'Application' field is not populating as expected, use theapplicationpickertochangethecurrentsession'sscope. |
| --- | --- |

_For __more__ information,__see_[_Product__Documentation: __Create__ a__pipeline_](https://docs.servicenow.com/csh?topicname=create-pipeline.html)

  1. **Add users to the App Engine**** Studio Administrators group in production **** instance**

Configure App Engine Studio administrator group membership in the productioninstancetomanageapplicationintakeanddeploymentrequests.

Ensure the group membership in production is consistent with the App Engine Studio administrators identified in the development instance.

Groupmembershipdoesnotsyncbetweenenvironmentsandmustbe updated in both production and development.

_ **Note:** _ _If group membership is empty in the production instance, or if the Deployment Pipeline plugin is not installed, the system will refer to App Engine Studio __Administrator__ group __membership__ in __the__ development__instance_

1. **Configure**** sub-production ****instances**

Followthe steps belowto install the 'Deployment Pipeline' plugin ineachsub-production instance.

Once installed, you will be required to configure an environment record in each instance which points to the production (controller) instance.

YouwillalsoenablethesystempropertiesthatwillallowtheAutomatedTest Framework (ATF) suite to run during the deployment process.

#### _Complete __these__ tasks __only__ if __you__ are __logged__ into __a__ sub-production__instance._

  1. **Install**** the ****'Deployment**** Pipeline' ****plugin**** in ****each**** sub-production ****instance**

Toinstall the Deployment Pipeline plugin, (_com.snc.deployment-pipeline)_, logintoanysub-productioninstanceandnavigateto **System**** Definition ****\>**  **Plugins.**

Usethesearchcriteriatofindtheapplication.Click **Install**.

Repeat and install the Deployment Pipeline plugin in each sub-production instance.

![](RackMultipart20230224-1-8f1srq_html_3994d8cd8c3cfc44.png)

_ **Note:** __If__ you __have__ already __installed__ the __App__ Engine __Studio__ bundle __in__ the development instance and promoted up to production, skip this step_

#### _Repeat this task __on each sub-production__ instance that will be part of__a_pipeline,

  1. **Configure**** credentials ****in**** each ****sub-production**** instance**

Ineachsub-productioninstance,createaCredentialAliasrecordand associate the Credentials for the production instance.

NavigatetoConnections&Credentials\>Connection&CredentialAliases.

Basedonthecredentialinformation,taketheappropriateapproachin configuring Credential Alias records:

![](RackMultipart20230224-1-8f1srq_html_a7beafa98433e87.png)

- If all environments in the Deployment Pipeline will use the samecredentialinformation(sameusername/password),thencreatea

single CredentialAlias record withthe same details as the CredentialAlias created in the production instance

  - i.e.,singleCredentialAliasrecordnamed'_Pipeline__Credentials'_
- If each environment in the Deployment Pipeline will use different credentials (different usernames / passwords), then create a single CredentialAlias records withthecredentialdetails fortheproduction instance
  - i.e.,singleCredentialAliasrecordsnamed'_Prod__Credentials'_

_Repeat_ _this_ _task on each sub-production instance that_ _will_ _be part of a_ _pipeline,_

_ **Note** __:__ Ensure __the__ username(s) __and__ password(s) __provided__ exist __in__ the production instance and the User is assigned the correct roles._

  1. **Configure**** the controller ****instance**** in ****each**** sub-production ****instance**

Ineachsub-productioninstance,setupandconfiguretheEnvironment recordwhich will point to the controller instance (production instance), where the Deployment Pipeline configurations reside.

All deployment requestsare routed through the controller instance. Until this isconfigured,yourdeveloperswillnotbeabletosubmitdeploymentrequests.

IfaCredentialAliasrecordforthecontroller(production)instancehasnot beencreatedineachsub-productioninstance,youmustcreateaCredential Aliasrecordpointingtothecontrollerinstanceineachsub-production instance.

If App Engine Studio is the only application using the Credentials table, consider creating data preservers for CredentialAlias, Basic Auth, and Discoverycredentials – otherwise,ensure that these tables are not overwritten whentheproductioninstanceiscloneddowntosub-productioninstances.

AppEngineStudiohasdatapreserversonthefollowingtables:

- Pipeline Instance
- RequestAuthorization Key
- Deployment Request
- DeploymentEnvironmentRequest

To ensure application and developer data is not lost in development environments during a clone, add **data preservers** tothe following:

- CollaborationDescriptortables:

- AppCollaborationDescriptors**[sys\_appcollab\_descriptor]**

- AppCollaborationDescriptorPermissions

**[sys\_appcollab\_permission\_m2m]**

- CollaborationUsersandGroupstables:

- AppCollaborationUsers**[sys\_appcollab\_user]**
- AppCollaborationGroups**[sys\_appcollab\_group]**

Additionally, add **clone excludes** for the following Collaboration Descriptor tables. so that data in these tables are preserved after cloning and that no data from the source instance gets copied over. It is ok to have data merge from source and target for collaboration users and groups tables.

- AppCollaborationDescriptors**[sys\_appcollab\_descriptor]**
- AppCollaborationDescriptorPermissions

**[sys\_appcollab\_permission\_m2m]**

Aftercloning,apost-cloneclean-upscript isneeded toreassignusers and groupstheappropriatedelegateddevelopmentpermissions.Weassumethat in-development applications arebackedup beforecloningandusers/groups are same between target and source instance.

#### _Repeat this task __on each sub-production__ instance that will be part of__a_pipeline,

_ **Note:** _ _New App Engine Studio customers__(Tokyo +) will only__have__data preservers on the tables listed above. Existing customers (pre-Tokyo) will also have data preservers on the_ _f__o __ll__ o __w__ i __n__ g __tables : Pipeline, Environment. Pipeline__ Environment Order, Pipeline Types_

  1. **Enable**** Automated ****Test**** Framework****(ATF)****properties****(**_ **testing** __**instance**__ **only** _**)**

EnablethesystempropertiesthatwillallowtheATFsuitetoruninthetesting instance as part of the deployment process.

App Engine Studio ships with an out-of-box test suite as a placeholder, howeveryouareresponsibleforconfigurationoftheATFtests.Iftheout-of- boxsuiteisnotmodified,theywillstillrunbutwillnotimpacttheflow.

![](RackMultipart20230224-1-8f1srq_html_ea12307de0d79639.jpg)

- **Enable**** test ****/**** test ****suite**** execution **_** (sn\_atf.runner.enabled)**_
  - Check this box on the _ **testing** _instance to enable automated tests to run as part of the application deployment process
  - ThedefaultvalueisfalsesothatATFtestsdonotrunon production instances
  - This property is private; changes to its value will not move between instances
- **Enable**** scheduled ****test**** suite ****execution** _**(sn\_atf.schedule.enabled)**_
  - The'Enabletest/testsuiteexecution'propertymustbe

enabledtoenablethisproperty

  - Check this box on the _ **testing** _instance to enable scheduled automated test suites to run as part of the application deployment process
  - ThedefaultvalueisfalsesothatATFtestsdonotrunon production instances
  - This property is private; changes to its value will not move between instances

If you do not enable these properties on the testing instance you will receive a warning during the deployment process, but you will be able to continue with deployment and the flow will continue.

#### _Enable __ATF__ properties __in__ your __production__ instance __if__ you __plan__ to__clone!_

_ **Note** __:__ Ensure __that__ the __controller__ instance __was__ configured __on__ a __ll__ sub-production instances that are part of a pipeline!_

**Application**** Intake ****Guided**** Setup**

Navigate to **App**** Engine Studio \> Application Intake \> Guided ****Setup** inyour productioninstance toaccesstheApplicationIntakeGuidedSetup.

![](RackMultipart20230224-1-8f1srq_html_941a6da8b579d52b.jpg)

_ **Note** __:__ Before __beginning Application__ Intake __Guided__ Setup, __ensure__ your application __scope is__ set__to_

'_Application __Intake'.__ If __not,__ use __the__ application __picker__ to __change__ the__current session's_ _scope_

![](RackMultipart20230224-1-8f1srq_html_be5525438f918e78.png)

1. **Turn on and**** configure ****the**** intake ****request process**** in ****production**

You'll need to activate the catalog item on your **production instance** and configure settings to enable auto-provisioning of users to a development instance if their intake request is approved.

  1. **Activate**** the ****catalog**** item ****where**** developers ****will**** submit ****their**** application ****ideas**

![](RackMultipart20230224-1-8f1srq_html_a90877efe8cbe5eb.jpg)

Activatethe'ApplyforCitizenDevelopment'catalogitemandallowdevelopers to submit applicationideas for screening bythe App Engine Studio Administrators.

The applicationintakerequest is usedtocapture informationfrombusiness users submitting application ideas to the App Engine Studio Administrators group for review.

Administrators can modify the out-of-box catalog item in Catalog Builder according to organizational needs so that all necessary information is captured from requestors.

  1. **Activate**** user provisioning**

![](RackMultipart20230224-1-8f1srq_html_21c384ae8a15d4bd.jpg)

Activatethepropertyonyourproductioninstancetoallowthesystemto provisionuserstotheAppEngineStudioUsersgroupinatargetdevelopment instance upon the approval of an application intake request.

Setthevalueofthe **sn\_app\_intake.instance\_can\_provision\_users** systemproperty to **true**.

1. **Configure**** development ****environments**** for ****users**

You'll need to activate the catalog item on your **production instance** and configure settings to enable auto-provisioning of users to a development instance if their intake request is approved.

  1. **Create**** environment****record(s)****for ****development**** instances ****in**** production**

In the production instance, create new Environment records for each development environment you would like to provision users to upon approving application intake requests. For the user provisioning to work on the target instances, the 'Instance Type' value must be set to **Development**.

If these records have already been setup as part of the Pipelines and Deployment Guided Setup, skip this step

_ **Note:** __For__ the __Application__ Intake __plugin__ to __work__ correctly, __App__ Engine __Studio__ must__be installed on the production instance_

# HowdoImanageAppEngineStudioaccess?

## Grantandrevokeaccess

When user provisioning has been configured as part of the Application Intake Guided Setup,users are automatically added to the App Engine Studio Users assignment group (in the target developmentinstance)upontheapprovalofasubmittedapplicationintakerequest.

Additionally,systemadministratorscanmanuallymanagegroupmembershiptothe'App Engine Studio Users assignment group by navigating to **All \> User Administration \> Groups** and openingthe'AppEngineStudioUsers'record.

Onceaddedtothegroup,membersareassignedthe **sn\_app\_eng\_studio.user** role,allowing them to access and build in App Engine Studio.

Beforegrantingaccessto theApp EngineStudioapplication, ensureusershavecompleted theappropriatecitizen developmentlearningpathsandtrainingsavailablein Now Learning!

![](RackMultipart20230224-1-8f1srq_html_8091b17f4d335f1b.png)

**Considerations**** for ****development**** security:**

- Ensureanapplicationownerandsupportteam(s)havebeenidentifiedtoownand support the application once in production
- Adduserstothe'AppEngineStudioUsers'assignmentgroupinsteadofassigningthe

**sn\_app\_eng\_studio.user** roletousersdirectly

- Considercreating multiple App Engine Studiodevelopergroups toaccommodate developersofdifferentskill/experiencelevels
  - i.e.,oneassignmentgroupforexperienceddeveloperswithenhanced permissions,andanothergroupforlessexperienceddeveloperswith restricted access to platform features – managed via delegated development

_For __more__ information,__see_[_Product__Documentation: __Grant__ access __to__ App __Engine__ Studio_](https://docs.servicenow.com/csh?topicname=grant-aes-access.html)

## Managecollaborationand delegateddevelopment

InAppEngineStudio,applicationownerscansubmitcollaborationrequeststohaveotherusers addedascollaboratorstoassist themindeliveringapplications.

AppEngineStudio'scollaborationfeatureusesdelegateddevelopment,allowingapplication

ownerstopickthelevelofaccesscollaboratorshavetoanapplication.

The **admin** role is required to create custom App Engine Studio roles available to developers when adding collaborators.

![](RackMultipart20230224-1-8f1srq_html_6da759c8c9363f87.jpg)

Whena collaboration requestissubmitted and thecollaboratoralready hasaccesstoApp Engine Studio (belongs to the 'App Engine Studio Users' group), then the request will be approved automatically.

Iftherequestedcollaboratordoesnotalreadyhaveaccess,AppEngineStudioadministrators areresponsibleforreviewingassignedCollaborationTaskdetails.Whenapproved,thesystem will automatically grant App Engine Studio access for the requested collaborator in the specified target development instance

AppEngine Studio administrators can access CollaborationRequests in the production instancefrom the App Engine Management Center or by navigating to **App Engine**  **\>**  **Collaboration**  **\>**  **Collaboration**** Tasks.**

Formoreinformation,see:[_Product __Documentation:__ Delegated __development__ in __App__ Engine_](https://docs.servicenow.com/csh?topicname=aes-app-dev-workflow.html)[_Studio_](https://docs.servicenow.com/csh?topicname=aes-app-dev-workflow.html)

# HowdoImanageapplicationintakerequests?

_ **Note** __:__ Before __editing__ the __Application__ Intake __process,__ ensure __your__ application __scope__ is __set__ to_

'_ **Application** __**Intake'**__. __If__ not, __use__ the __application__ picker __to__ change __the__ current __session's__ scope_

![](RackMultipart20230224-1-8f1srq_html_1753a79e93acd0dd.png)

## Configuretheapplicationintakerequestform

Administrators can configure the out-of-box application intake request form to capture the necessary information from custom application requestors, according to organizational needs. The intakeformis installedwiththe **Application Intake** pluginandcanbe modifiedinCatalog Builder.

## Accessandreviewapplicationintakerequests

Whenapplicationideasaresubmittedbyrequestors,approvalrecordsarecreatedand assignedtousersintheAppEngineStudioAdministratorsgroup.

App Engine Studio administratorscan access assigned requests in the production instance fromthe App Engine Management Center or by navigating to **Self**  **Service**  **\>**  **Requested**  **Items**.

App Engine Studio Administrators will receive an email notification when intake requests are submitted.Administrators are responsible for reviewing thesubmittedapplicationrequests to determine if they are a suitable use case for development in App Engine Studio.

## ChoosingtherightapplicationsforAppEngineStudio

Thefirst stepinevaluatingapplicationrequestsistomakesuretherequestisnotalreadysatisfied by anexistingapplicationorwillnotbeaddressedaspartofanupcomingServiceNowrelease.

Administrators are thenresponsible for determining if App Engine Studiois the appropriate development environment for the application.

IdealusecasesforAppEngineStudiodevelopmentinclude:

- UsecaseswhereanapplicationtemplatealreadyexistsinAppEngineStudio
- Simpleprocessesthatareeasilytranslatedtoautomatedworkflows
- Departmentalprocessesmanagedbysubjectmatterexperts
- Applicationswithsimplethird-partyintegrations
- Noconfidentialorsensitivedatainvolved

Evenif anapplicationrequiresadvanceddevelopment,thefoundationalapplicationworkcan be completed in App Engine Studio, and pro-code developers can easily transfer applications toServiceNowStudiotoperformcomplexdevelopment activities.

Iftheproposed application isa good candidatefordevelopmentinAppEngineStudio, click **Approve.** Therequestorwillreceiveanemailnotificationinforming of therequest approval. App Engine Studio administrators are responsible for manually provisioning App Engine Studio access for requestors so they can begin building their applications.

Before approving an application, be sure the application requestor has identified the applicationownerandsupportteam(s)responsibleforowningandmanagingtheapplication once it is in production.

If the requestis not viable, click **Reject.** The requestor will receive an emailnotification informingof the rejection.

_ **Note** __: Consider creating_ _an_ _assessment_ _and_ _risk profile to assist__ in screening application requests. __An__ assessment __can__ be __configured__ to __capture__ the __application__ details. __Based__ on __the__ development effort required, application inputs / outputs, or other factors, a risk score will_ _be_ _generated __for__ the __application__ request._

_Using the_ _risk_ _score, define a threshold_ _for_ _applications that are good_ _c __a__ n __d__ i __d__ a __t__ es __for_ _App Engine Studio, or_ _if_ _they should__ instead __be developed__ in_ _ServiceNow__Studio_ _(i.e., if risk_ _score is Low__or Medium, the application __will_ _be__ approved_ _for_ _App Engine Studio __development__ –_ _if__the_ _risk_ _score is High, consider building the application_ _in_ _ServiceNow Studio)._

_For more information, see_ [_Product Documentation: Intake request process for application_](https://docs.servicenow.com/csh?topicname=intake-request.html&intake-request)[_development ideas_](https://docs.servicenow.com/csh?topicname=intake-request.html&intake-request)

# HowdoImanageapplicationdeploymentrequests?

DeploymentRequestsareusedtotrackandmanageanapplication'smovementacross

instances.

AppEngine StudioAdministrators can access deployment requests in the production instance from the App Engine Management Center or by navigating to **App Engine Studio**  **\> Configuration**** \> ****App**** Deployment ****Request**.

When an application is submitted for IT review, the system generates and assigns a Deployment Request record to the App Engine Studio Administrators group.

Administrators can review application, requestor, and deployment details from the Deployment Request.Pipelineandenvironmentinformationforapplicationsareavailableinthe 'Deployment Details' section of the request form.

![](RackMultipart20230224-1-8f1srq_html_706337e4115974f6.png)

**Deployment**** Request ****States**

| **State** | **Description** |
| --- | --- |
| New | An application has been submitted for IT review by an App Engine Studio developer.
The State will automatically changefrom **New** to **In**** Review** once thefirstsub-flowintheDeploymentPipelinehasfinishedexecuting. |
| InReview | Application is under review by the App Engine Studio administrators.
ReviewandtestingactivitiesoccurintheTestinginstance. |
| --- | --- |
| Closed–Published | Application has been successfully published to the production instance. |
| --- | --- |
| Closed–Rejected | Application has failed testing and is not ready to be published to the production instance. |
| --- | --- |
| Closed–Failed | Indicatesasub-flowintheDeploymentPipelinefailed. |
| --- | --- |
| Cancelled | TheDeploymentRequestwascancelled. |
| --- | --- |

## Promoteanapplicationinapipeline

When application developers submit an application for IT review, App Engine Studio administrators are assigned Approval records for the Deployment Requests.

Applications are promoted to the next instance in the Deployment Pipeline when administrators approve a request. Only one administrator is required to approve or reject a request.

If arequest is approved,the systemwill trigger asub-flowtopromote the applicationtothe next environment, as defined by Deployment Pipeline configuration.

Each timean application is promoted to a new instanceadministrators will be assigned a new Approval record. When approved, the applicationwill be promoted to the next instance in thepipeline. This continues until the application is promoted to the production instance.

## Reviewandtestanapplication

Once an application has been promoted to theTesting instance, it should bethoroughly tested andreviewedbytheapplicationdeveloper,experiencedServiceNowdevelopers,and functional IT resources to ensure that the application works as expected and existing platform functionality is not impacted. Assign application roles in the test environment appropriately so that users can complete necessary testing activities.

As part of the application deployment process, Automated Test Framework (ATF) tests / suites and Instance Scan definitions will automatically run when the application is promoted to an instanceofType=Testing(ifmultipleinstancesareconfiguredwithType=Testing,thenthetest suites and definitions will run on each instance). ATF and Instance Scan results will be logged in the Notes section of the Deployment Request and available in the 'Deployment EnvironmentResults' related list.

As your citizen development program scales, consider implementing an application 'risk profile' to dictate the level of testing required to more efficiently allocate testing resources. For example, an application containing a Script Include will have a higher risk profile than an application built with a template and minimal configurations, and therefore will require more rigorous testing).

## Rejectanapplication

If anapplicationfails testing or requires additional development work,administrators canreject anapplicationbyclicking **'** Reject'ontheassignedapprovalrecord.

If you reject an application,provide clear feedbackto developer(s) so they can quickly correct the configurations. The Deployment Request 'State' will change to **Closed – Rejected** and the requestor will receive an email notification informing of the rejection.

Application developerscan incorporatefeedbackand continueto submittheapplication forIT review.

_For __more__ information,__see:_

- [_Product __Documentation:__ Deployment __Request__ form_](https://docs.servicenow.com/csh?topicname=deployment-request-form.html)
- [_Product __Documentation:__ Move __an__ application __to__ your __test__ environment_](https://docs.servicenow.com/csh?topicname=move-app-instance.html)
- [_Product __Documentation:__ Reject __an__ application_](https://docs.servicenow.com/csh?topicname=approve-reject-app.html)

# HowdoIdeployapplicationstoproductioninAppEngine Studio?

Once an application has successfullycompleted all testing activities fromrequiredreviewers, it is ready to be promoted to the production instance.

Whenadministratorsapproveanapplicationtopromoteanapplicationtoproduction,the DeploymentRequest'State'willchangeto **Closed**** – ****Published**.Theapplicationwillbepublished totheapplicationrepositoryandinstalledontheproductioninstance.Assignrolesappropriately sothatuserscanaccesstheapplicationacrossinstances,asnecessary.

![](RackMultipart20230224-1-8f1srq_html_bc8c67e4adfef4af.png)

Formoreinformation,see:

[_Product __Documentation:__ Deploy __an__ application_](https://docs.servicenow.com/csh?topicname=deploy-app.html)[_Product Documentation: Application sharing_](https://docs.servicenow.com/csh?topicname=c_SharingApplications.html)

[_Product __Documentation:__ Publish __an__ application __to__ the __application__ repository_](https://docs.servicenow.com/csh?topicname=t_PublishAppsToTheAppRepository.html)

# HowdoIcreateapplicationtemplates?

AppEngineStudiooffersdeveloperspre-configuredapplicationtemplatesthatcanbeusedto jumpstartdevelopmentandacceleratetimetovalue.Inadditiontotheout-of-boxtemplates, AppEngineStudioAdministratorscanconfigurecustomtemplatesfortheirdevelopers.

![](RackMultipart20230224-1-8f1srq_html_e319c3307b993233.png)

Thesetemplatescanbeconfiguredwithpre-definedData,Experiences,LogicandAutomation, and Security features, based on common use cases across the organization.

![](RackMultipart20230224-1-8f1srq_html_5a034cc8a475c277.jpg)

Customapplicationtemplatescanbecreatedfromexistingapplications,orfromscratch.Once atemplatehasbeenconfigured,makeitavailabletodevelopersbypublishingitinAppEngine Studio.

_For __more__ information,__see_[_Product__Documentation: __Custom__ templates_](https://docs.servicenow.com/csh?topicname=work-custom-templates.html)

# HowdoImanageAppEngineStudiopropertiesand processes?

**Manage**** applications ****created**** in ****App**** Engine ****Studio**

DetailsforapplicationscreatedinAppEngineStudioareaccessiblebynavigatingto

**System**** Applications ****\> My**** Company ****Applications.**

Administratorscanaccessthefollowingcustomapplicationdata:applicationfiles, version,scope,dependencies,roles,andnavigation.Applicationscanbepublishedtoan update set, if needed.

**App**** Engine ****Studio**** Properties**

AdministratorscanmanagetheAppEngineStudioapplicationpropertiesinAppEngineStudiobynavigatingto **App**** Engine Studio \> ****Configuration**** \> ****Properties.**

**Pipelines**

Pipelines dictate the deployment path for App Engine Studio applications from development to production.

To create or edit pipeline configurations, navigate to **App Engine Studio \> Pipelines and Deployments**** \> ****Pipelines.**

**Environments**

Definetheenvironmentsusedindeploymentpipelinestomoveapplicationsacrossan organization. To create or edit environments, navigate to **App Engine Studio \> Pipelines and**** Deployments ****\>**** Environments.**

**Application**** Intake ****Process**

Refine the intake request form by modifying the related Service Catalog items and customize the application intake approval process by modifying the approval flow for the item.

_For more information, see_ [_Product Documentation: Service catalog items_](https://docs.servicenow.com/csh?topicname=c_IntroductionToCatalogItems.html)_For more information, see_ [_Product Documentation: Flows_](https://docs.servicenow.com/csh?topicname=flows.html)

**Integrations**** and ****Spokes**

Manageintegrationswiththird-partysystemsviaIntegrationHub.Integrationspokescan be downloaded from the ServiceNow Store and must be installed to connect to App Engine Studio.

_For more__information, see_ [_Product__Documentation:_ _IntegrationHub_](https://docs.servicenow.com/csh?topicname=integrationhub.html)

**Instance**** Scans**

ConfigureInstanceScandefinitionstoensureadherencetoapplicationdevelopment and organizational best practices.

InstanceScandefinitionsareexecutedwhenAppEngineStudioapplicationsare promoted to the test instance and can also be executed ad-hoc.

_For __more__ information,__see_[_Product__Documentation: __Instance__ Scan_](https://docs.servicenow.com/csh?topicname=hs-landing-page.html)

**Automated**** Test ****Framework**** (ATF)**

Automatetestingactivitiesbycreating ATFsuitesandtestsforcustomapplications.

At aminimum,simple regressiontests shouldberequiredforallcitizen-developed applications.

ATFsuitesandtestsareexecutedwhenAppEngineStudioapplicationsarepromotedto the test instance and can also be executed ad-hoc.

_For __more__ information,__see_[_Product__Documentation: __Automated__ Test__Framework_ _(ATF)_](https://docs.servicenow.com/csh?topicname=automated-test-framework.html)

# FAQs

### CanapplicationsbeaccessedfromAppEngineStudiotoServiceNowStudio,andvice-versa?

Yes.ApplicationsbuiltinAppEngineStudioareaccessiblefromServiceNowStudio.

All application configurations are captured in the application scope, regardless of the development studio the configurations are performed in.

There are several capabilities available in ServiceNow Studio that are not accessible from App Engine Studio, including business rules, client scripts, and notifications.

**Does**** App ****Engine**** Studio ****support**** domain ****separation?**

DomainseparationisnotsupportedforAppEngineStudio.Thedomainfieldmayexiston datatables, but there is no business logic to manage the data.

**Can App**** Engine Studio applications be integrated ****with other applications outside of**  **ServiceNow?**

Yes, App Engine Studios can interact with third-party systems by leveraging IntegrationHub spokes / actions exposed through Flow Designer.

**How**** can ****I**** safely ****expose**** third-party ****integrations**** in ****App**** Engine ****Studio?**

Consider pre-configuring authorized sub-flows for application developers to use when sharing data with third-party systems instead of allowing App Engine Studio developers to access IntegrationHub actions via Flow Designer.

This way, developers are not directly accessing any third-party systems, and data is shared and presented in a consistent manner across all applications built in App Engine Studio.

**How**** are Deployment ****Requests created**** and ****managed?**

DeploymentRequestsaregeneratedandassignedtoAppEngineStudioAdministrators in the production instance when application developers submit an application for IT review.

**How to**** enable ****other**** applications ****to**** read ****data**** in the ****application's**** table(s)?**

Updatethe'ApplicationAccess'propertyforeachtableinanapplicationtomakeits data accessible to other applications.

**Are**** App ****Engine Studio**** applications built ****in**** a ****private application**** scope?**

Yes,eachapplicationisdevelopedinitsownscope.

**How**** do ****I**** upgrade ****the**** App ****Engine**** Studio ****application?**

AdministratorscanupdatetheAppEngineStudioapplicationintheServiceNowStore.

**How**** can ****I**** manage ****developers**** of ****varying**** experience ****and**** skill ****in**** App ****Engine**** Studio?**

Consider creating multiple development groups in App Engine Studio for developers ofdifferent skill levels. Leverage delegated development to modify group access to builder tools accordingly.

Experienced developers may have more freedom with App Engine Studio tools and featuresthanlow-codedevelopers,whomayhavefewerpermissionsintheapplication.

**Can**** I ****integrate**** App ****Engine**** Studio ****with Source**** Control?**

Yes,applicationdeveloperscanintegratewithaGitSourceControlrepositorytosave and manage multiple versions of an application from a sub-production instance.

_For __more__ information,__see:_

- [_Product __Documentation:__ Source __C__ o __n__ t __r__ o __l__ integration __in__ App __Engine__ Studio_](https://docs.servicenow.com/csh?topicname=aes-source-control-integration.html)
- [_Home __-__ ServiceNow__Developers_](https://developer.servicenow.com/)

**Can**** I ****turn**** off ****the**** automatic execution ****of**** ATF ****tests and**** Instance Scan ****definitions?**

No, unless a new flow is created and the 'Deployment Environment Type Flow' Decision Table[**sys\_decision**]isupdatedtopointtothenewflowforenvironmentswithinstance type of 'Testing'.

If the ATFsystemproperties are not enabled inthe testing instance as part of the guided setup, you will receive a warning during deployment, however the flow will continue.

Iftheout-of-boxtestsuiteisnotmodified,theywillrunbutwillalsonotaffecttheflow.

**Can**** I ****change**** the ****instance**** where ****ATF**** tests ****and**** Instance ****Scan**** definitions ****are**** executed?**

Yes, this can be accomplished by updating the 'Instance Type' value for an Environmentrecord to 'Testing'. Alternatively, the decision table can bemodified tomake thedecision for 'Instance Type = Staging' (for example) point to the Testing sub-flow.

1

©2022ServiceNow,Inc.Allrightsreserved.ServiceNow,theServiceNowlogo,Now,NowPlatform,andotherServiceNowmarksaretrademarksand/orregisteredtrademarksofServiceNow,Inc. in the United States and/or other countries. Othercompany and product names may betrademarks of the respective companies with which they areassociated.