# Requirements Document - Pichincha Bank (January 30, 2024)

## Revision History

| Name | Date | Reason for Changes | Version |
|------|------|--------------------|---------| 
| Cache Money Inc | Jan-30-24 | Initial document creation | 1.0.0 |
| Cache Money Inc | Feb-03-24 | Merging team members independent sections into doc | 1.0.1 |
| Cache Money Inc | Feb-04-24 | Merging team members independent sections into doc | 1.0.2 |
| Cache Money Inc | Feb-04-24 | Formatting changes and document review | 1.1.0 |
| Cache Money Inc | Feb-04-24 | Iteration 1 RD submission | 2.0.0 |  
| Cache Money Inc | Feb-07-24 | Revisions and changes from client review | 2.0.1 |
| Cache Money Inc | Feb-11-24 | Revisions and changes from client review | 2.0.2 |  
| Cache Money Inc | Feb-17-24 | Addition of iteration 2 sections | 2.1.0 |  

## Table Of Contents  

* [1.0 Overview](#10-overview)  
* [2.0 Business Requirements](#20-business-requirements)  
   * [2.1 Background](#21-background)  
   * [2.2 Business Opportunity](#22-business-opportunity)  
   * [2.3 Business Objectives](#23-business-objectives)  
   * [2.4 Success Metrics](#24-success-metrics)  
   * [2.5 Product Vision Statement](#25-product-vision-statement)  
* [3.0 Scope and Limitations](#30-scope-and-limitations)  
   * [3.1 Major Features](#31-major-features)  
   * [3.2 Project Scope](#32-project-scope)  
   * [3.3 Limitations and Exclusions](#33-limitations-and-exclusions)  
* [4.0 Context Description](#40-context-description)  
   * [4.1 User Classes and Characteristics](#41-user-classes-and-characteristics)  
   * [4.2 Operating Environment](#42-operating-environment)  
   * [4.3 Design and Implementation Constraints](#43-design-and-implmentation-constraints)  
   * [4.4 Assumptions and Dependencies](#44-assumptions-and-dependencies)  
   * [4.5 Glossary of Terms](#45-glossary-of-terms)  
   * [4.6 References](#46-references)
* [5.0 System Features](#50-system-features)
   * [5.1 International Money Transfer Request (Feature)](#1-international-money-transfer-request)
   * [5.2 Manage Contacts (Feature)](#2-manage-contacts)
   * [5.3 Manage Transfer Status (Feature)](#3-manage-transfer-status)
   * [5.4 Customer Profile (Feature)](#4-customer-profile)
* [6.0 Data Requirements](#60-data-requirements)
   * [6.1 Logical Data Model](#61-logical-data-model)
   * [6.2 Data Dictionary](#62-data-dictionary)
   * [6.3 Reports](#63-reports)
   * [6.4 Data acquisition, integrity, retention, and diposal](#64-data-acquisition-integrity-retention-and-diposal)
* [7.0 External Interface Requirements](#70-external-interface-requirements)
   * [7.1 User Interfaces](#71-user-interfaces)
   * [7.2 Hardware Interfaces](#72-hardware-interfaces)
   * [7.3 Software Interfaces](#73-software-interfaces)
   * [7.4 Communication Interfaces](#74-communication-interfaces)
* [8.0 Software Quality Attributes](#80-quality-attributes)
* [9.0 Analysis Models](#90-analysis-models)
* [10.0 Appendix](#100-appendix)

# 1.0 Overview  
The following requirements document contains the complete set of requirements pertaining to the development of a solution for Pichincha Banks inefficient paper method for performing international fund transfers.  

# 2.0 Business Requirements  

## 2.1 Background 
Pichincha Bank is a private bank based in Ecuador with approximately 1.5 million customers [[1]](https://es.wikipedia.org/wiki/Banco_Pichincha). The Bank offers a variety of online services to its members through its mobile and web banking portals. These services include online investing, bank certificates, credit and debit account management, and domestic money transfers. Pichincha Bank is looking to improve their international money transfer process due to staff productivity and customer satisfaction concerns through the implementation of a digital system.   

Pichincha Bank’s international money transfer process utilizes a paper Request for Transfer Abroad form (RTA) and requires tellers to manually input data from the completed RTA form into the digital Society for Worldwide Interbank Financial Telecommunication (SWIFT) Alliance system. The current process is inefficient for both bank tellers and customers. The following steps further describe the current process:

   1. An ordering customer arrives at a Pichincha Bank location and waits for an available teller  

   2. The customer completes a paper RTA form with information relating to the transfer source account, beneficiary account, monetary amount, and SWIFT code  

   3. A teller verifies this information and manually inputs the data into the SWIFT Alliance system  

   4. A teller initiates a SWIFT transaction  

   5. The beneficiary’s bank receives the transfer and verifies the information  

   6. The funds are deposited into the beneficiary account approximately 7 days after initiation of the SWIFT transaction  

The process outlined above assumes no errors were made by either the customer completing the RTA form, or the bank teller inputting the data. If errors occur and are not resolved before initiation of the SWIFT transaction, it takes approximately 3 weeks to complete the transaction. 

In response to concerns about the efficiency of the current process, Pichincha Bank is seeking to enhance its international fund transfer process. The subsequent segments of Section 2 will further detail Pichincha Bank’s challenges, objectives, and the success metrics of a proposed solution. 
 
## 2.2 Business Opportunity  
The current financial transaction system for international fund tranfers is inefficient and affects both customers and bank tellers.  

* Customers often experience lengthy wait times at the bank and spend a significant amount of time filling out the physical forms. Simultaneously, tellers spend time walking clients through the physical forms and verifying that they contain the correct and appropriate information.
* The long duration of the transaction causes customer dissatisfaction and frustration. The inefficiency of the international transfer process has a detrimental impact on the organization’s reputation, profits, and tellers’ morale and performance as they regularly have to deal with unhappy customers. 

Our team proposes the implementation of a digital transaction. This initiative aims to not only speed up the transaction process but also significantly improve accuracy and productivity. By reducing transaction time and minimizing errors, the new digital process will elevate the overall customer experience and satisfaction as well as foster a positive environment for bank tellers.

## 2.3 Business Objectives  
The business objectives of Pichincha Bank are designed to improve the overall process of international transactions. The following are objectives that are designed to help improve Pichincha Bank’s success through the following means: 

* **Improve Staff Productivity by 25% in Six Months:** By eliminating the need for customers to physically visit the bank to process an international transfer, teller's can better allocate their time to resolving customer inquiries that require an in-person visit. 

* **Reduce Wait Times by 30% in Four Months:** Having a digital method of filling out the RTA form reduces the necessity for customers to meet with a teller, thus lowering the amount of customers requiring an in-person visit and reducing the wait time for customers to meet with a teller. 
      
* **Increase Customer and Employee Satisfaction by 50% in Eight Months:** Improving the accessibility and clarity of the international transfer system will reduce transaction processing time, and thus reduce complaints and improve employee and customer satisfaction. 
      
* **Reduce Bank Visits Per Customer to One in a Year :** Introducing a user-friendly interface in the mobile app, coupled with straightforward instructions that provides customers with information to address inquiries and reduce unnecessary visits.  

## 2.4 Success Metrics  
The following success metrics are indicators that allow Pichincha Bank stakeholders to measure the overall success of the implemented solution: 

* **Increase of International Transfers by 15% Within Six Months:** Through increasing staff productivity by 25%, the amount of international transfers are increased by 15% within the next six months. 
   
* **Reducing international transfer processing time by 30% in Four Months:** By reducing wait times by 30%, processing times of international transfers are reduced by 30% within four months.   
   
* **Increase Customer Base by 20% in Eight Months:** Through increasing customer and employee satisfaction by 50%, the customer base of Pichincha Bank can be increased by 20% within eight months.    

## 2.5 **Product Vision Statement**  
The International Bank Transfer System provides customers the ability to perform international transfers via the existing Pichincha Bank web and mobile applications without the need to meet with a bank employee in person. The system will provide customers the ability to add and store international contacts to which funds can be transferred, as well as provide a digital interface for completing the RTA form, allowing customers to submit the required information to complete an international transfer remotely. The functionality of the system also extends to bank employees, providing a review and processing portal for handling international transfer requests created by a customer. By providing an alternative to in person, paper form international transfers, the International Bank Transfer System aims to direct 80% of the international transfer customer base to a Pichincha Bank application, thus freeing teller resources for tasks requiring in person support.

# 3.0 Scope and Limitations  

## 3.1 Major Features  
The implemented system must be an addition to the current bank app which will facilitate international transfers. There is a customer facing side of the app and a teller facing side which each require different features.

The major features of the customer facing side are:  

* **Digital RTA Form:** A digital form which prompts an ordering customer for the information required to make an international transfer. The digital form will request the same information as the current physical RTA form.
* **Add New International Contact:** Create a new contact will have the ordering customer fill out the digital RTA form for a new beneficiary and then add the new contact to the their contact list.
* **Auto-Fill Form:** Provide the ordering customer with the option to save RTA form data the first time they fill it out to be auto-filled for all future uses. Saved and auto filled information will be data specific to the ordering customer and not the beneficiary.
* **Saved Contacts:** Allow the ordering customer to view a list of contacts they have previously submitted the RTA form for. Each contact must have a contact page which states whether previous transfers were successfully completed, date of transaction, and transaction amount for that contact.
* **Transfer to Saved Contact:** Ordering customer is able to make an international transfer to one of the saved contacts without filling out the RTA form again. Transaction specific information including the transfer amount and reason must be collected.
* **International Transfer Verification PIN:** A 4-digit PIN must be entered upon each attempt to submit the RTA form for an international transfer request. The PIN must be changed in the user profile, when the customer wants to change the PIN.
* **User Profile:** An interface in which the ordering customer may access the data stored about them for international transfers and make changes to it. The specific items which must be editable within this section are the verification PIN and the [Ordering Customer RTA Form Information](#Ordering_Customer_RTA_Form_Section).
* **Transfer Status Notifications:** After a teller marks a transfer as either completed or rejected (see employee facing features for details), the ordering customer will receive a notification (via either email or SMS depending on preferred method selected in user settings). The notification must state success status, and next steps for failed transfers.
* **Help Information:** Help text is displayed containing more information about what is required to be entered in each data entry box on the digital RTA form.
      
The major features for the teller facing side are:  

* **International Transfer Processing Portal:** An interface in which a bank teller will view all requested international transfers and the RTA form corresponding to the transfer. The portal must sort all requested transfers into four categories: Unprocessed (new beneficiary), Unprocessed (existing beneficiary), In processing, Completed, and Rejected.
* **Claim a Transfer:** A teller claims a transfer from the unprocessed transfers to show that they will be verifying the information in the transfer form and entering the information into the SWIFT alliance system to send a transfer. Once a transfer is claimed the software will sort it into the “in processing” category.
* **Complete a Transfer:** After an international transfer is successfully deposited to the beneficiary the teller processing that transfer will manually mark the transfer as complete. The software then sorts the transfer into the “completed” category.
* **Reject Transfer:** If there is an issue with the transfer which prevents it from being deposited the teller will manually reject the transfer. The software then sorts the transfer into the “rejected” category.
* **Auto-Reject Transfer:** Whenever a new transfer is requested the software will automatically check if there is an insufficient balance in the account for the transfer, then if there is insufficient balance label the transfer as rejected and sort it into “rejected”. If there is sufficient balance the system will sort the transfer into the correct “unprocessed" category.
* **Dealing with Rejected Transfers:** If a customer contacts the bank to fix a rejected transfer, a teller will claim the transfer and the system will move it to “in processing”.
         
## 3.2 Project Scope  
The project should deliver an addition to the current Pichincha Bank app which facilitates international transfers. Customer and bank teller interfaces must be created to allow for the various tasks undertaken by different user groups. The purpose of the software is to allow for international transfers to be made digitally, lowering strain on the brick and mortar bank while increasing ease of use for customers. 

The final product will support the business goals described in Section 2.  

* **Improve Staff Productivity:** The software will improve staff productivity by allowing customers to make international transfers without direct interaction with staff. The “Help Information” feature will provide additional helpful information to ordering customers. This will save the tellers' time to spend on other important tasks.
* **Reduce Wait Times:** The software will eliminate wait times to fill out RTA forms for online international transfers by immediately providing online users with RTA forms. The in person wait time to fill out RTA forms will also be reduced as the majority of ordering customers will prefer the benefits that filling out the form online provides. 
* **Customer Satisfaction:** The software will contain numerous features designed to improve customer satisfaction. Ordering customers will not need to travel to the bank to make international transfers, as the software will allow all necessary tasks to be performed online, saving customers valuble time and effort. The saved contacts feature the software provides will provide ordering customers with a more seamless experience when sending money to an international beneficiary repeatedly. Within the new system, customers will be able to save international beneficiary information. This will reduce the time required to fill out the form and thus, shorten the time until the transaction is complete.
* **Employee Satisfaction:** Employee satisfaction will increase as they will not have to work with paper forms for the majority of international transfers. The employee portal will easily allow for information to be read and added to the SWIFT Alliance app, tellers will not need to worry about the confusion of misreading customers’ handwriting.    

## 3.3 Limitations and Exclusions  
The Pichincha Bank international transfer system aims to enhance the efficiency and user-friendliness of international transactions through its mobile and web applications. This initiative is driven by the need to improve customer and staff satisfaction, reduce transaction times, and address the current system's inefficiencies. However, the project's scope is defined by certain limitations and exclusions that are essential to understand for setting realistic expectations and achieving the desired outcomes. Below is an expanded view of the limitations based on the detailed project document and the exclusions that extend beyond the project's scope.

### Limitations  

* **Delayed Interactions with Real-World Bank Tellers:** The project is limited by the inherent delays in interactions with bank tellers, which can extend the processing time for international transfers. This limitation is a consequence of the current reliance on manual verification and data entry processes.

* **Interactions with the SWIFT System:** The efficiency of international transfers is limited by the interactions with the SWIFT system, which is an external dependency with its own processing times and operational constraints.

* **Integration with Existing Banking Systems:** The project must seamlessly integrate with Pichincha Bank's current banking systems and protocols, which may limit the flexibility in implementing certain features or require additional time for compatibility adjustments.

* **Technological Constraints:** The project is limited by the current technological infrastructure of Pichincha Bank, including hardware capabilities, software compatibility, and the operational capacity of the mobile and web platforms.

* **Dependency on External Services:** The reliance on third-party services such as SWIFT Alliance and Docusign introduces limitations related to their availability, reliability, and compatibility with the bank's systems.

### Exclusions

* **Legality and Regulatory Compliance:** Issues related to legality and regulatory compliance, while critical to the banking operations, are excluded from the project's direct scope. These areas are assumed to be addressed by other specialized teams within Pichincha Bank, ensuring compliance with relevant laws and regulations without burdening the project team with areas outside their expertise.

* **Customer Education on Financial Regulations:** Educating customers on the complexities of international financial regulations is outside the scope of this project. While the app aims to simplify the transfer process, the responsibility for understanding the legal implications of international transfers remains with the customers.

By clearly defining these limitations and exclusions, Pichincha Bank sets a realistic framework for the international transfer project, ensuring that stakeholders have a clear understanding of what the project will deliver and the areas that are beyond its immediate scope. This clarity is essential for managing expectations and focusing efforts on achieving the project's primary objectives of improving efficiency, customer satisfaction, and staff productivity within the defined constraints.

# 4.0 Context Description  

## 4.1 User Classes and Characteristics  
The Pichincha Bank international transfer system is designed to cater to a diverse range of users, differentiated by their interaction frequency, technical expertise, security needs, and the specific functionalities they utilize. Given the system's dual focus on facilitating international transfers for both individual customers and businesses, as well as enabling administrative oversight and management, we have identified two primary user classes: the Customer Class and the Administrative Class. Each of these classes is further subdivided to address distinct user needs and priorities.

### Customer Class  

> #### - Subclass 1: Regular User -
> 
> **Characteristics:** Individuals using the system for personal international money transfers. This group is characterized by a wide range of technical expertise, from novice to advanced users, and includes both infrequent and regular users.
>
> **Privileges:** Regular Users are able to initiate and manage their international transfers, access and fill out the digital RTA Form, save beneficiary details for future transactions, and receive status notifications about their transfers.
>
> **Special Considerations:** While Regular Users have access to the full suite of transfer functionalities, their transactions are processed with standard priority, which may result in slightly longer processing times during peak periods compared to Business Users.

> #### - Subclass 2: Business User -
> 
> **Characteristics:** Organizations or entities that require the system for business-related international transfers. This subclass includes small and medium enterprises, large corporations, and other financial entities. Business Users are expected to have a higher volume of transactions and may have increased familiarity with the international transfer processes.  
>
> **Privileges:** See Regular User priviledges.   
>  
> **Special Considerations:** Business Users may require additional support for batch processing of transactions and might benefit from detailed transaction reporting for accounting purposes.  

### Administrative Class

> #### - Subclass 1: Bank Tellers -
>
> **Characteristics:** Bank tellers are responsible for verifying international transfer requests. This subclass possesses a high level of technical expertise and understanding of banking regulations and the SWIFT System.
>
> **Privileges:** Bank Tellers can access and manage incoming transfer requests, verify transaction details, input information into the SWIFT System, and update the transaction status. They play a critical role in ensuring the accuracy and security of transfers.
>
> **Responsibilities:** Their primary responsibility includes inputting customer data into the SWIFT system and providing support to customers as needed.

> #### - Subclass 2: System Administrators -
>
> **Characteristics:** Technical staff responsible for the maintenance, security, and operational integrity of the international transfer system. This group has advanced technical expertise and comprehensive access to the system's backend.
> 
> **Privileges:** System Administrators have the highest level of access, including system configuration, user management, security protocol adjustments, and troubleshooting. They ensure the system's smooth operation and safeguard against technical issues or security threats.
> 
> **Responsibilities:** Monitoring system performance, implementing updates, ensuring compliance with security standards, and addressing any technical issues that arise.

By distinguishing between these user classes and their respective characteristics, Pichincha Bank can tailor the international transfer system to meet the varied needs of its users effectively, ensuring a seamless and secure experience for both customers and administrative personnel.

## 4.2 Operating Environment  

The following outlines the operating environment of the system, providing crucial insights into the hardware, software platforms, and applications with which the system must seamlessly integrate and function. Understanding these constraints and the operating environment is paramount for development teams as they navigate the design, development, and deployment phases of the project.

||||
|-|-|-|
|CON~1|Hardware Platform|The operating environment for the system encompasses mobile devices and web browsers. For users accessing the Pichincha Bank mobile app, the platform includes mobile devices. Meanwhile, ordering customers accessing the application through the website utilize a laptop or desktop computer.|
|CON~2|Operating Environment |The supported operating environments include operating systems iOS and Android. Specifically, the system is designed to function seamlessly on the latest versions of both iOS and Android. Additionally, compatibility is maintained across various browsers such as Chrome, Microsoft Edge, Safari, and others for ordering customers accessing the application through the website.|
|CON~3|Software Applications|The system is integrated into an environment where it must integrate with the existing Pichincha Bank web and mobile app. The primary application is the Pichincha Bank mobile app, an existing app tailored for banking services. Additionally, the system interacts with the SWIFT Alliance system.|

## 4.3 Design and Implementation Constraints  

Design and implementation constraints delineate the parameters within which the development of the international transfer system for Pichincha Bank must operate. These constraints encompass various facets, ranging from integration with existing systems to multilingual support and security considerations. Understanding these constraints is pivotal for ensuring that the final product aligns with the bank's operational standards and regulatory requirements.

||||
|-|-|-|
|CON~4|Existing System Integration|The designed system should conform and integrate seamlessly with the existing online banking application, as well as integrating with the current technology infrastructure and databases employed by Pichincha Bank. The responsibility for maintaining the app post-delivery will rest with the current app maintainers|
|CON~5|Application Languages|The software is mandated to support both English and Spanish languages. This linguistic flexibility is essential to cater to a diverse user base and enhance accessibility for customers who communicate in either language.|
|CON~6|Parallel Operations|The system must be capable of executing international transfer transactions concurrently. This constraint emphasizes the need for efficient parallel processing, ensuring that multiple international transfer operations committed within the same time frame can be executed simultaneously.|
|CON~7|Security Considerations|Security is a top priority, requiring robust measures to safeguard user data and financial transactions. The software must implement encryption protocols for secure data transmission, preventing unauthorized access. Additional security features include the introduction of a PIN for completing new forms related to international transfers, with provisions to change the PIN. Moreover, the use of Docusign for filling signatures on forms contributes to the overall security and authentication of transactions.|    

## 4.4 Assumptions and Dependencies   
The successful implementation of this project relies on several critical assumptions and dependencies. The following factors form the foundation upon which the project’s framework is built:  

* **User Authentication:** We assume that the mechanisms for user authentication in Pichincha Bank's current application are robust and secure. This includes the assumption that the current security protocols are sufficient to protect sensitive financial transactions and personal data against potential cyber threats. Any changes or failures in this area could impact user trust and system integrity.
* **Existing Technological Infrastructure:** We rely on the current app and website’s ability to support the addition of new features without compromising performance. This includes assumptions about the scalability of the current system to handle an increase in user traffic and international transfer demands.
* **Third Party Services:** We depend on the stability and reliability of external platforms like SWIFT Alliance for processing transactions and Docusign for digital signatures. Any significant disruptions in these services could impact the functionality and reliability of the international transfer system.
* **Legal Compliance:** We assume that the addition of international transfers to the existing application will comply with current and future international regulations. Changes in banking regulations could require significant adjustments to the project scope or design. 
* **User Adoption:** We assume that users will readily transition to the new online method for international transfers.
     
These assumptions should be regularly reviewed to ensure they remain valid throughout the project’s development.
   
## 4.5 Glossary of Terms  
|Term|Definition|
|----|----------|
|Auto-Reject Transfer|An automatic system function that rejects a transfer if there is an insufficient balance in the ordering customer's account to cover the transfer amount.|
|Beneficiary|The account or bank receiving money from an international transfer. It is the ultimate destination of the funds sent by the ordering customer.|
|C.C.|(*Carné de Ciudadanía*) National identity card used in Ecuador, serves as offical proof of identity.|
|C.I.|(*Cédula de Identidad*) National identity card used in Ecuador, serves as offical proof of identity.|
|Claim a Transfer|The action taken by a teller to indicate they are verifying the information for a transfer and will be processing it through the SWIFT system.|
|Complete a Transfer|The marking of a transfer as finished by a teller after successfully depositing the funds into the beneficiary account.|
|Contact| Beneficiary which the ordering customer has previously created an international transfer request for. |
|Customer Facing Side|The part of the app used by ordering customers to initiate and manage international transfers.|
|Digital Transaction Platform|The proposed solution for improving the international money transfer process, involving a digital feature integrated into Pichincha Bank's existing mobile and web applications to facilitate faster and more accurate transactions.|
|Docusign|A document signing software that you can use to legally—and securely—collect approvals online in minutes.|
|Help Information|Text displayed within the app providing guidance on how to complete the digital RTA form and other related queries.|
|Ordering Customer|The individual or entity initiating an international money transfer. This party is responsible for providing the necessary information and funds for the transfer.|
|Pichincha Bank|A private banking institution based in Ecuador, offering a range of services including investments, account management, and money transfers.|
|Reject Transfer|The action taken by a teller when a transfer cannot be processed due to issues with the information provided, leading to its cancellation.|
|RTA Form|(*Request for Transfer Abroad form*) The request form used by Pichincha Bank to enact a transfer of funds internationally.|
|RUC|(*Registro Único de Contribuyentes*) Unique identification number assigned to individuals and businesses for tax purposes in Ecuador.|
|SWIFT|(*Society for Worldwide Interbank Financial Telecommunication*) A global member-owned cooperative providing secure messaging services and interface software for financial transactions among its members.|
|SWIFT Alliance System|The digital platform used by Pichincha Bank to process international money transfers through the SWIFT network.|
|Teller|A customer facing bank employee that helps customer issues and requests in person.|  
|Teller Facing Side|The interface used by bank tellers to process requested international transfers, including verifying information and entering it into the SWIFT Alliance system.|


## 4.6 References  

#### Web References  

|ID|Reference|
|--|---------|
|[1]|“Banco Pichincha,” Wikipedia, Jan. 28, 2024. https://es.wikipedia.org/wiki/Banco_Pichincha (accessed Feb. 02, 2024).|  

#### Image References  

|ID|Reference|
|--|---------|
|[2]|"Banco Pichincha Mobile App Page," App Advice, n.d. https://appadvice.com/game/app/pichincha-banca-movil/999191728 (accessed Feb. 14, 2024).|  

# 5.0 System Features  
*This template illustrates organizing the functional requirements for the product by system features, the major services provided by the product. You may prefer to organize this section by use case, mode of operation, user class, object class, functional hierarchy, or combinations of these, whatever makes the most logical sense for your product.*  
   
### 1. International money transfer request

> #### **Description**
> This feature allows customers to request an international transfer and allows tellers to manage and process international transfer requests. Customers shall be able to specify an amount of money to transfer to a contact with an international transfer pin. Tellers shall be able to claim a transfer to review and process a transfer through the SWIFT alliance system with a SWIFT code.
>
> **Priority**: High
>    
> #### **Functional Requirements**
> |||
> |-|-|
> |REQ~1|The customer shall be able to specify the amount of money to transfer|
> |REQ~2|The teller shall be able to input customer's data into the SWIFT alliance system|
> |REQ~3|As a customer, I want to choose a contact that I can send money to|
> |REQ~4|As a customer, I want to specify the amount to transfer and provide data where needed to process a transfer|
> |REQ~5|As a customer, I want to input the international transfer verification pin so I can access the RTA form|
> |REQ~6|The teller shall be able to reject a transfer request if the customer provides insufficient data|
> |REQ~7|The system shall automatically reject a transfer request if the customer has insufficient funds|
> |REQ~8|The customer shall be able to review the status of their transfer request| 

### 2. Manage Contacts  

> #### **Description**  
> This feature allows customers to organize their contacts within the system. Customers shall be able to perform actions such as creating, sorting, viewing, editing, and deleting contacts. Furthermore, as a customer, they shall be able to transfer money to specified contacts.
>
> **Priority**: Medium
> 
> #### **Functional Requirements**  
> |||
> |-|-|
> |REQ~9|The customer shall be able to create a new contact.|
> |REQ~10|The customer shall be able to sort their contacts alphabetically or by date added.|
> |REQ~11|The  customer shall be able to search for a contact from their contact list.|
> |REQ~12|The customer shall be able to view the contact details of a contact.| 
> |REQ~13|The customer shall be able to edit or modify a contact.|
> |REQ~14|The customer shall be able to delete a contact.|
> |REQ~15|The customer shall be able to transfer money to a contact.|
> |REQ~16|As a customer, I want to set a notification preference for a contact so that I can receive either an email or an SMS on receiving money.|
> |REQ~17|As a customer, I want to set a transfer method for a contact so that I can specify how I want to transfer money to them.|
> |REQ~18|The customer shall be able to view the transfer history of a contact.|
> |REQ~19|The customer shall be able to view the transfer status of a contact.|

#### Use Case Description  

| **ID and Name:** | UC-2 Create a Contact |
|------------------|-----------------------|
| **Created By:**  | Matt                |
| **Date Created:**| 10/10/24              |
| **Primary Actor:** | User                |
| **Secondary Actors:** | Contact Database, User Interface |
| **Description:** | The User initiates the process to create a new contact by entering personal details, such as name, address, phone number, and email. The system validates the entered information and stores it in the Contact Database. The User can then use this contact information for various operations like sending messages, making calls, or sharing documents. |
| **Trigger:** | User selects the option to create a new contact in the application. |
| **Preconditions:** | PRE-1. User is logged into the system. <br> PRE-2. User has permission to add new contacts. <br> PRE-3. Contact Database is accessible. |
| **Postconditions:** | POST-1. A new contact is created in the Contact Database. <br> POST-2. User can access and interact with the new contact information. |
| **Normal Flow:** | 1. User selects the option to create a new contact. <br> 2. System presents a form for entering contact details. <br> 3. User fills in the contact's name, address, phone number, and email. <br> 4. System validates the entered information for format and completeness. <br> 5. User confirms the creation of the new contact. <br> 6. System stores the new contact information in the Contact Database. <br> 7. System acknowledges the successful creation of the contact to the User. |
| **Alternative Flows:** | 4.1 Invalid Contact Information <br> 1. System detects invalid or incomplete contact details. <br> 2. System prompts User to correct the information. <br> 3. User updates the contact details and resubmits. <br> 4. Return to step 4 of Normal Flow. |
| **Exceptions:** | 4.1.1 System Cannot Validate Contact <br> 1. System is unable to validate the contact information due to an internal error. <br> 2. System notifies the User of the error and suggests trying again later. <br> 3. User decides to either retry immediately or exit the creation process. <br> 4. If retrying, return to step 2 of Normal Flow; if exiting, system terminates the use case. |
| **Priority:** | Medium |
| **Frequency of Use:** | Varies depending on the number of new contacts a user needs to add; estimated at an average of 5 times per week per user. |
| **Business Rules:** | |
| **Other Information:** | The system should allow for easy input and editing of contact details, with the ability to import from or export to external address books. |
| **Assumptions:** | - The system has a reliable and user-friendly interface for contact creation. <br> - The Contact Database is robust and capable of handling concurrent interactions from multiple users. |  

### 3. Manage Transfer Status  

> #### **Description**  
> This feature involves managing the status of the transfer. It allows a customer to cancel the transfer, allows a bank teller to change the transfer status to be completed or rejected as well as the system functionality to reject the transfer if there is not enough balance on a client’s account. This feature falls into the medium priority level.
>
> **Priority**: Medium
> 

> #### **Functional Requirements**
> |||
> |-|-|
> |REQ~20|The system shall allow a customer to cancel a transfer.|
> |REQ~21|The system shall enable a teller to change transfer status.|
> |REQ~22|The system shall be able to automatically reject a transfer in the event of insufficient funds within a customer account.|
> |REQ~23|As a teller, I want to be able to change the transfer request to be completed, so I can keep track of the progress.|
> |REQ~24|As a teller, I want to be able to change the transfer request to be rejected, so I can notify a client.|
> |REQ~25|As a customer, I want to be able to cancel a transfer before it is sent, so I can recity any inaccurate information.|  

#### Use Case Description  

|||
|-|-|
|ID and Name:|UC-1 Review of an international transfer request by a teller|
|Created By:|Brayden|
|Date Created:|Feb-16-2024|
|Primary Actor:|Teller|
|Secondary Actors:| Customer|
|Description:|The teller selects an international transfer request submitted by a customer for review. The system then provides the teller with the option to accept if the request has been completed properly or to reject if the request has been completed improperly.|
|Trigger:|Teller selects a submitted international transfer request|
|Preconditions:|PRE-1. A customer has submitted an international transfer request <br> PRE-2. An authorized administrative user is accessing the system|
|Postconditions:|POST-1. A notification is sent to the requesting customer specifying the completion status of the transfer request|
|Normal Flow:|**1.0 Teller reviews a valid international transfer request** <br> 1. Teller selects an international transfer request <br> 2. System displays transfer request for teller to review <br> 3. System give Teller the option to accept the transfer request or reject the transfer request (see 1.1) <br> 4. Teller selects the accept option to complete the transfer request <br> 5. System changes the state of the transfer request to accepted|
|Alternative Flow:|**1.1 Teller reviews an invalid international transfer request** <br> 1. System displays transfer request for teller to review <br> 2. Teller finds an issue with the transfer request <br> 3. System give Teller the option to reject the transfer request or accept the transfer request (see 1.0) <br> 4. Teller selects the reject option <br> 5. Teller enters a justification message for the transfer being rejected (see 4.1.E1) <br> 6. System changes the state of the transfer request to rejected|
|Exceptions:|**4.1.E1 No transfer rejection reason entered** <br> 1. System displays message: Missing transfer rejection message entered <br> 2. System prompts Teller to enter a message (3a) or to cancel the transfer review (4a) <br> 3a. Teller enters a justification message <br> 3b. System saves the justification message <br> 3c. System continues previous flow <br> 4a. System closes the transfer request <br> 4b. System returns transfer request to list of open international transfer requests|
|Priority:|high|
|Frequency of Use:|Approximately 10 to 100 times per week depending on the volume of customers|
|Other Information:|A Teller is the main user performing this use case, however, any Administrative user has the capability to perform this use case|
|Assumptions:|- The International Transfer Request has not already been rejected by the system itself|  

### 4. Customer Profile  

> #### **Description**  
> This feature allows the customer to manage their personal information related to international transfers. This information includes the ordering customer data found on the RTA form, such as name, identification, address, phone number, email, and account number to debit, as well as the verification PIN.
>    
> **Priority**: Low
> 
> #### **Functional Requirements**  
> |||
> |-|-|
> |REQ~26|The customer shall be able to add their name, identification (CI, CC, Passport, RUC), address, phone number, email, and the account number to debit for international transfers.|
> |REQ~27|The customer shall be able to edit their name, identification (CI, CC, Passport, RUC), address, phone number, email, and the account number for international transfers.|
> |REQ~28|The customer shall be able to change their international transfer verification PIN.|
> |REQ~29|As a customer, I want to save my personal information for international transfers so that I do not have to re-enter the information each time.|

# 6.0 Data Requirements   
      
## 6.1 Logical data model  

The diagram below depicts the interactions between major International Bank Transfer System entities. The main entities of the system include Ordering Customer, Customer Profile, International Contact Profile, Submitted International Transfer Request, RTA Form, Teller, Account Verification PIN, and SWIFT Alliance. The relationships and cardinalities between entities demonstrates the nature of interactions between the various actors or data objects of the system. As a note, although SWIFT Alliance is an external third-party system, it has been included as an entity in the diagram as it is a crucial aspect of the international transfer process and interacts with International Bank Transfer System actors and data.  

![Entity Relationship Diagram (2)](https://github.com/Uvic-SENG321Spring2024/team2-developer/assets/110196682/b8c6bb05-3bf7-476a-b88f-664f65204c1c)
*Entity Relationship Diagram of International Bank Transfer System*

## 6.2 Data dictionary  

The data dictionary below defines the composition of data structures and their contents as they relate to the project.

| Data Element | Description | Composition or Data Type | Length | Values |
|---|---|---|---|---|
| <a name="Accepted_Declarations"></a> Accepted Declarations | If the ordering customer accepted the declarations required to transfer money internationally. | Boolean | 1 | 0 for false, 1 for true |
| <a name="Account_Verification_PIN"></a> Account Verification PIN| The PIN used to verify that the submitter of an international transfer request is the ordering customer. | Numeric characters | 4 |  |
| <a name="Beneficiary_Account_Number"></a>Beneficiary Account Number | Beneficiary account number to be credited. | Numeric characters  | 17 |  |
| <a name="Beneficiary_Address"></a>Beneficiary Address | Address of the beneficiary. | Alphanumeric characters | 100 |  |
| <a name="Beneficiary_Bank_Address"></a>Beneficiary Bank Address | Address of the beneficiary bank. | Alphanumeric characters | 100 |  |
| <a name="Beneficiary_Bank_City"></a>Beneficiary Bank City | City the beneficiary bank is located in. | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Beneficiary_Bank_Country"></a>Beneficiary Bank Country | Country the beneficiary bank is located in. | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Beneficiary_Bank_Name"></a>Beneficiary Bank Name | Name of the beneficiary bank. | Alphabetic characters | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Beneficiary_Bank_RTA_Form_Section"></a>Beneficiary Bank RTA Form Section | The section of the digital RTA form containing information regarding the beneficiary bank. | [Beneficiary Bank Name](#Beneficiary_Bank_Name) <br>+ [Beneficiary Bank SWIFT Code](#Beneficiary_Bank_SWIFT_Code) <br>+ [Beneficiary Bank Address](#Beneficiary_Bank_Address) <br>+ [Beneficiary Bank Transit Number](#Beneficiary_Bank_Transit_Number) <br>+ [Beneficiary Bank City](#Beneficiary_Bank_City) <br>+ [Beneficiary Bank Country](#Beneficiary_Bank_Country) |  |  |
| <a name="Beneficiary_Bank_SWIFT_Code"></a>Beneficiary Bank SWIFT Code | SWIFT code belonging to the beneficiary bank. | Alphanumeric characters | 11 |  |
| <a name="Beneficiary_Bank_Transit_Number"></a>Beneficiary Bank Transit Number | Transit Number of the beneficiary bank branch | Numeric characters | 5 |  |
| <a name="Beneficiary_City"></a>Beneficiary City | City the beneficiary is located in. | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Beneficiary_Country"></a>Beneficiary Country | Country the beneficiary is located in. | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Beneficiary_Name"></a>Beneficiary Name | First and last name or company name of the beneficiary.  | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Beneficiary_RTA_Form_Section"></a>Beneficiary RTA Form Section | The section of the digital RTA form containing information regarding the beneficiary. | [Beneficiary Name](#Beneficiary_Name) <br>+ [Beneficiary Account Number](#Beneficiary_Account_Number) <br>+ [Beneficiary Address](#Beneficiary_Address) <br>+ [Beneficiary City](#Beneficiary_City) <br>+ [Beneficiary Country](#Beneficiary_Country) |  |  |
| <a name="Contact_List"></a>Contact List | The list of all contacts an ordering customer has. | 1:n{[International Contact Profile](#International_Contact_Profile)} |  |  |
| <a name="Contact_Transfer_History"></a>Contact Transfer History | All previous requested international transfers from the ordering customer to a beneficiary. | 1:n{[Form Completion Date](#Form_Completion_Date)} <br>+ 1:n{[Transfer Value](#Transfer_Value)} <br>+ 1:n{[Transaction Reason Code](#Transaction_Reason_Code)} <br>+ 1:n{[Transfer Reference](#Transfer_Reference)} <br>+ 1:n{ [International Transfer Status](#International_Transfer_Status)} |  |  |
| <a name="Customer_Profile"></a>Customer Profile | Ordering customer’s profile in the international transfer application. | [Ordering Customer Name](#Ordering_Customer_Name) <br>+ [Ordering Customer Identification](#Ordering_Customer_Identification) <br>+ [Ordering Customer Address](#Ordering_Customer_Address) <br>+ [Ordering Customer Postal Code](#Ordering_Customer_Postal_Code) <br>+ [Ordering Customer Phone Number](#Ordering_Customer_Phone_Number) <br>+ [Ordering Customer Email](#Ordering_Customer_Email) <br>+ [Account Verification PIN](#Account_Verification_PIN) |  |  |
| <a name="Employee_ID"></a>Employee ID | Identification number of a Pichincha Bank employee. | Numeric characters | 15 |  |
| <a name="Employee_Name"></a>Employee Name | Name of a Pichincha Bank employee. | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Form_Completion_Date"></a>Form Completion Date | Date RTA form was submitted by ordering customer on. | Numeric Date | 10 | dd/mm/yyyy format in numbers |
| <a name="International_Contact_Profile"></a>International Contact Profile | Profile of a contact who has been a beneficiary to a international transfer from the ordering customer. | [Beneficiary Name](#Beneficiary_Name) <br>+ [Beneficiary Account Number](#Beneficiary_Account_Number) <br>+ [Beneficiary Address](#Beneficiary_Address) <br>+ [Beneficiary City](#Beneficiary_City) <br>+ [Beneficiary Country](#Beneficiary_Country) <br>+ [Beneficiary Bank Name](#Beneficiary_Bank_Name) <br>+ [Beneficiary Bank SWIFT Code](#Beneficiary_Bank_SWIFT_Code) <br>+ [Beneficiary Bank Address](#Beneficiary_Bank_Address) <br>+ [Beneficiary Bank Transit Number](#Beneficiary_Bank_Transit_Number) <br>+ [Beneficiary Bank City](#Beneficiary_Bank_City) <br>+ [Beneficiary Bank Country](#Beneficiary_Bank_Country) <br>+ [Contact Transfer History](#Contact_Transfer_History) |  |  |
| <a name="International_Transfer_Instance_RTA_Form_Section"></a>International Transfer Instance RTA Form Section | The section of the digital RTA form containing data regarding a specific international transfer request. | [Transfer Currency](#Transfer_Currency) <br>+ [Transfer Value](#Transfer_Value) <br>+ [Transaction Reason Code](#Transaction_Reason_Code) <br>+ [Transaction Reason Code](#Transaction_Reason_Code) <br>+ [Transfer Reference](#Transfer_Reference) |  |  |
| <a name="International_Transfer_Status"></a>International Transfer Status | The status of an international transfer request. | Alphabetic characters, spaces, parentheses | 15 | Can be: “Unprocessed (new beneficiary)”, “Unprocessed (existing beneficiary)”, “In processing”, “Completed”, and “Rejected” |
| <a name="Ordering_Bank_SWIFT_Code"></a>Ordering Bank SWIFT Code | SWIFT code belonging to the ordering bank. | Alphanumeric characters | 11 |  |
| <a name="Ordering_Customer"></a>Ordering Customer | Information regarding the ordering customer. | [Ordering Customer Name](#Ordering_Customer_Name) <br>+ 1:n{[Ordering Customer Account Number](#Ordering_Customer_Account_Number)} |  |  |
| <a name="Ordering_Customer_Account_Number"></a>Ordering Customer Account Number | Ordering customer’s account number to be debited. | Numeric characters  | 17 |  |
| <a name="Ordering_Customer_Address"></a>Ordering Customer Address | Address of the ordering customer. | Alphanumeric characters | 100 |  |
| <a name="Ordering_Customer_Email"></a>Ordering Customer Email | Email of the ordering customer. | Alphanumeric characters  | 254 | Can contain certain special characters: !, #, $, %, &, ', *, +, -, /, =, ?, ^, _, {, \|, }, ~, .  |
| <a name="Ordering_Customer_Identification"></a>Ordering Customer Identification | Identification number from ordering customer’s  C.I., C.C., Passport, or RUC. | Numeric characters  | 11 |  |
| <a name="Ordering_Customer_Name"></a>Ordering Customer Name | First and last name or company name of the ordering customer.  | Alphabetic characters  | 100 | can contain blanks, hyphens, apostrophes, accented alphabetic characters |
| <a name="Ordering_Customer_Phone_Number"></a>Ordering Customer Phone Number | Phone number of the ordering customer. | Numeric characters  | 15 |  |
| <a name="Ordering_Customer_Postal_Code"></a>Ordering Customer Postal Code | Postal Code of the ordering customer. | Alphanumeric characters | 6 |  |
| <a name="Ordering_Customer_RTA_Form_Section"></a>Ordering Customer RTA Form Section | The section of the digital RTA form containing information regarding the ordering customer. | [Ordering Customer Name](#Ordering_Customer_Name) <br>+ [Ordering Customer Identification](#Ordering_Customer_Identification) <br>+ [Ordering Customer Address](#Ordering_Customer_Address) <br>+ [Ordering Customer Postal Code](#Ordering_Customer_Postal_Code) <br>+ [Ordering Customer Phone Number](#Ordering_Customer_Phone_Number) <br>+ [Ordering Customer Email](#Ordering_Customer_Email) <br>+ [Ordering Customer Account Number](#Ordering_Customer_Account_Number) |  |  |
| <a name="RTA_Form"></a>RTA Form | The digital form which contains all data necessary to make an international transfer. | [Form Completion Date](#Form_Completion_Date) <br>+ [Ordering Customer RTA Form Section](#Ordering_Customer_RTA_Form_Section) <br>+ [Beneficiary Bank RTA Form Section](#Beneficiary_Bank_RTA_Form_Section) <br>+ [Beneficiary RTA Form Section](#Beneficiary_RTA_Form_Section) <br>+ [International Transfer Instance RTA Form Section](#International_Transfer_Instance_RTA_Form_Section) <br>+ [Accepted Declarations](#Accepted_Declarations) |  |  |
| <a name="Submitted_International_Transfer_Request"></a>Submitted International Transfer Request | The object containing all information related to an international transfer request which has been submitted by the ordering customer. Includes transfer status and teller assignee. | [RTA Form](#RTA_Form) <br>+ [International Transfer Status](#International_Transfer_Status) <br>+ [Teller](#Teller) |  |  |
| <a name="SWIFT_Alliance"></a>SWIFT Alliance | A best assumption of information the SWIFT Alliance Application uses. | [RTA Form](#RTA_Form) <br>+ [International Transfer Status](#International_Transfer_Status) <br>+ [Ordering Bank SWIFT Code](#Ordering_Bank_SWIFT_Code) |  |  |
| <a name="Teller"></a>Teller | Information regarding a teller employed at Pichincha Bank. Including current assigned International Transfer Requests. | [Employee ID](#Employee_ID) <br>+ [Employee Name](#Employee_Name) <br>+ 1:n{[Submitted International Transfer Request](#Submitted_International_Transfer_Request)} |  |  |
| <a name="Transaction_Reason_Code"></a>Transaction Reason Code | Reason for international transfer code. | Numeric characters | 3 |  |
| <a name="Transfer_Currency"></a>Transfer Currency | ISO 4217 currency code for transfer to be made in. | Alphabetic characters | 3 |  |
| <a name="Transfer_Reference"></a>Transfer Reference | Message from the ordering customer to the beneficiary describing reason for transfer and identifies source of transfer. | Alphanumeric characters and special symbols | 300 |  |
| <a name="Transfer_Value"></a>Transfer Value | Monetary value to be transferred to beneficiary. | Numeric characters | 12 |  |

## 6.3 Reports  

The International Bank Transfer System does not generate reports as a part of it's functionality.    

## 6.4 Data acquisition, integrity, retention, and diposal

**Data Acquisition:** The International Bank Transfer System acquires data directly from customers when they submit an International Transfer Request. This data is collected when a customer completes an RTA Form and when a customer creates a new international contact. 

**Data Integrity:** A Teller reviews and verifies the data provided by a customer through a Submitted International Transfer Request before inputting the data into the SWIFT Alliance system for further processing. If a customer provides incorrect or incomplete data, the International Transfer Request is rejected by either the assigned teller, or the SWIFT Alliance system. The system automatically rejects the transfer upon RTA Form submission if the customer has insufficient funds for the transfer.

**Data Retention:** Data critical to the facilitation of future International Transfer Requests such as details from the Ordering Customer RTA Form Section and International Contact Profiles are stored in the system. This data retention strategy is designed to streamline the international transfer process for repeat customers by reducing re-entry of data. Additionally, once an international transfer is successfully completed, the details and status of the request are saved for future review by either a teller or the ordering customer. 

**Data Disposal:** Data disposal is carried out in accordance with legal and regulatory requirements - the details of which are out of the scope of this project as indicated in Section 3.3 (Limitations and Exclusions). 

# 7.0 External Interface Requirements   

## 7.1 User Interfaces  

The user interface for the International Bank Transfer System will coincide with the existing Pichincha Bank mobile and web applications. To maintain consistency throughout the application, a matching design language will be used to seamlessly integrate the new system with the existing applications.   

|||
|-|-|
|EIR~1|The system shall use the same colour codes as the existing application|
|EIR~2.1|The system shall provide a method for a customer to create a new International Transfer Request (ITR)|
|EIR~2.2|The system shall provide a customer the ability to enter RTA form data|
|EIR~2.3|The system shall provide a method for a customer to save the current state of the RTA form|
|EIR~2.4|The system shall provide a method for a customer to open a saved RTA form|
|EIR~3.1|The system shall provide a method for a customer to create a new International Transfer Contact (ITC)|
|EIR~3.2|The system shall provide a method for a customer to edit an ITC|
|EIR~3.3|The system shall provide a method for a customer to delete an ITC|
|EIR~4.1|When an ITR is completed by a customer, the system shall provide a method for an administrator to accept the ITR for review|
|EIR~4.2|The system shall provide a method for an administrator to accept an ITR|
|EIR~4.3|The system shall provide a method for an administrator to reject an ITR|
|EIR~5|The system shall produce an error when a customer inputs a dollar amount into the RTF form that is greater than the current balance of their chosen account to send money from|

#### Existing Application Reference  

Referenced below are images showing examples of the exisitng Pichincha Bank web and mobile applications. these images provide reference for the design language that should be used when implementing the International Bank Transfer System.  

> ![accounts page](./images/accounts_page.png)  
> *The **accounts page** of the Pichincha Bank web application* 

> ![mobile contacts](./images/mobile_app_add_contact.jpeg)   
> *The **contact page** of the Pichincha Bank mobile application*  
> [*[2] "Banco Pichincha Mobile App Page"*](https://appadvice.com/game/app/pichincha-banca-movil/999191728)   
      
## 7.2 Hardware Interfaces  

Due to the integration of the International Bank Transfer System with the existing Pichincha Bank web and mobile applications, the system must be compatible with the hardware devices with which the web and mobile applications are compatible.    

|||
|-|-|
|EIR~6|The system shall be able to operate on multiple device types outlined in Table 1-1|
|EIR~6.1|The system shall be able to operate on Windows devices|
|EIR~6.2|The system shall be able to operate on Mac devices|
|EIR~6.3|The system shall be able to operate on IOS mobile devices|  
|EIR~6.4|The system shall be able to operate on Android mobile devices|  

> **Table 1-1** Requirements for device compatability of the International Bank Transfer System
> |Device Compatability|Requirement|
> |-|-|
> |Windows|.1|
> |Mac|.2|  
> |IOS|.3|  
> |Android|.4|   
   
## 7.3 Software Interfaces  

The International Bank Transfer System will be integrated into the existing Pichincha Bank web and mobile applications. The new system must be able to interact seamlessly with the existing infrastructure. The SWIFT Alliance System is also a critical component in performing an international transfer. The system must also allow an administrative user to interact with the SWIFT system to process and complete a transfer request.  

|||
|-|-|
|EIR~7.1|The system shall be integrated into the existing Pichincha Bank web application|
|EIR~7.2|The system shall be integrated into the existing Pichincha Bank mobile application|
|EIR~8.1|The system shall give an administrator the ability to interact with the SWIFT Alliance System|
|EIR~8.2|(**TBD**) The system shall give an administrator the ability to input *\<data-type\>* into the SWIFT Alliance System|
|EIR~9|The system shall store International Transfer Contact data to the existing Pichincha Bank database|
|EIR~10|The system shall store International Transfer Customer data to the existing Pichincha Bank database|
|EIR~11.1|When a customer submits an RTA form, the system shall send an e-mail notification to the customer notifying them that the system has received their transfer request form|
|EIR~11.2|When an administrator sets the status of an International Bank Transfer request to approved, the system shall send an e-mail notification to the customer notifying them that the transfer request has been approved|
|EIR~11.3|When an administrator sets the status of an International Bank Transfer request to rejected, the system shall send an e-mail notification to the customer notifying them that the transfer request has been rejected|  
       
## 7.4 Communication Interfaces  

The communication interfaces for the International Bank Transfer System must be able to commmunicate relavent information about the status of the transfer request to the requesting customer. This communication can be implemented via e-mail, SMS, or other means such that the customer is easily able to access relavent status about the transfer request. Due to the systems communication with the SWIFT Alliance System, the appropriate communication between the International Bank Transfer System and the SWIFT Alliance system must be used.  

|||
|-|-|
|EIR~12|The system must be able to send e-mail notifications to a customer|
|EIR~13|(**TBD**) The system must communicate with the SWIFT Alliance System via \<communication-type\>|  

# 8.0 Quality Attributes
**8.11 Performance**

- **Response Time:** Transactions and user interactions within the mobile and web applications should be processed within 3 seconds to ensure a smooth user experience.
- **System Efficiency:** The system must efficiently handle the expected load, particularly during peak hours, without compromising on performance, aiming to support the anticipated increase in international transfers by 15% within six months.

 **8.12 Security**

- **Data Protection:** All customer data, including financial information and personal identifiers, must be encrypted in transit and at rest using industry-standard encryption protocols.
- **Access Control:** Implement secure authentication mechanisms for users and bank tellers, including the use of a 4-digit PIN for customers and secure login procedures for bank tellers, to ensure that access to sensitive functionalities is tightly controlled.
- **Audit and Compliance:** The system must log all transactions and user activities to support auditing processes and ensure compliance with financial regulations and SWIFT guidelines.

**8.13 Reusability**

- **Modular Components:** Design the system with reusable modules, particularly for the digital RTA form and international contact management, to facilitate future enhancements or integrations.
- **API Integration:** Ensure the system's architecture supports integration with existing banking systems and can be easily adapted for future banking services or third-party services.

**8.14 Maintainability**

- **Code Quality and Documentation:** Adhere to best coding practices and maintain thorough documentation, especially for the integration with SWIFT Alliance and the mobile and web banking platforms, to facilitate easy updates and maintenance.
- **System Updates:** Develop a structured process for regularly updating the application, including security patches and functionality improvements, with minimal disruption to bank operations.

**8.15 Usability**

- **User Interface Design:** The customer and teller interfaces must be intuitive and user-friendly, supporting a seamless transition from paper-based to digital transactions. This includes clear instructions for filling out the digital RTA form and managing international contacts.
- **Help Features:** Incorporate comprehensive help features and FAQs to assist users in navigating the system and to reduce the need for in-person bank visits.

**8.16 Availability**

- **System Uptime:** Aim for a system uptime of 99.9% to ensure that international transfer functionalities are available to customers and bank staff as needed, reflecting the bank's commitment to improving customer and employee satisfaction.
- **Backup and Recovery:** Implement robust data backup and disaster recovery protocols to ensure data integrity and system availability, minimizing the impact of system failures.

**8.17 Interoperability**

- **Integration with Existing Systems:** The digital solution must integrate seamlessly with Pichincha Bank's existing mobile and web banking platforms, as well as the SWIFT Alliance system, without requiring significant changes to those systems.
- **External Systems Compatibility:** Ensure the system's compatibility with external banking and financial systems, maintaining flexibility for future banking standards and technologies.

**8.18 Supportability**

- **Ease of Operation and Maintenance:** The digital system should be designed with a clear and concise operational manual, ensuring bank staff can easily support day-to-day operations, including handling customer inquiries, processing transfers, and addressing any issues that may arise.
- **Software Updates and Upgrades:** The system should support easy updates and upgrades to incorporate new features, address security vulnerabilities, and ensure compatibility with evolving international banking standards and technologies.
- **Customer Support Integration:** Features should include built-in support mechanisms, such as FAQ sections, help desks, or chatbots within the banking app, to directly address user queries, reducing the need for in-person bank visits and enhancing overall supportability.

**8.19 Testability**

- **Automated Testing Frameworks:** Implementing automated testing frameworks that can simulate a range of scenarios, from single transactions to peak load operations, ensuring the system behaves as expected without failures.
- **Modular Testing:** Given the system's modular approach (e.g., digital RTA form, international transfer processing portal), each component should be designed to be independently testable. This allows for more efficient identification and resolution of issues.
- **User Acceptance Testing (UAT):** Involving actual users (both bank customers and tellers) in the testing process to ensure the system meets real-world usability, performance, and security expectations.

**8.20 Scalability**

- **Handling Increased Transaction Volumes:** The system must be able to scale up to handle increases in international transfer requests without degradation in performance, ensuring transactions are processed efficiently even during peak periods.
- **Flexible Infrastructure:** Utilize cloud services or other scalable infrastructure solutions that allow for dynamic scaling of resources in response to demand fluctuations, ensuring the system remains responsive and reliable.
- **Future Expansion:** Design the system with the future in mind, allowing for easy integration of new features, support for additional international banking standards, and expansion to serve more customers as Pichincha Bank grows.


# 9.0 Analysis Models
The use case diagram, as seen below, displays the proposed International Bank Transfer System functionalities in order to meet the requirements of the client, Pichincha Bank. The use cases specify what actions the various users of the system may take and how those use cases interact with other functionalities and users.
![Use Case Diagram](./images/PichinchaBankUseCaseDiagram.png)  
*Use Case Diagram for Pichincha Bank International Transfer System* 
# 10.0 Appendix
