# Requirements Document - Pichincha Bank (January 30, 2024)

## Revision History

| Name | Date | Reason for Changes | Version |
|------|------|--------------------|---------| 
| Cache Money Inc | Jan-30-24 | Initial document creation | 1.0.0 |
| Cache Money Inc | Feb-03-24 | Merging team members independent sections into doc | 1.0.1 |
| Cache Money Inc | Feb-04-24 | Merging team members independent sections into doc | 1.0.2 |
| Cache Money Inc | Feb-04-24 | Formatting changes and document review | 1.1.0 |
| Cache Money Inc | Feb-04-24 | Iteration 1 RD submission | 2.0.0 |  


## Table Of Contents  

* 1.0 Overview  
* 2.0 Business Requirements  
   * 2.1 Background  
   * 2.2 Business Opportunity  
   * 2.3 Business Objectives  
   * 2.4 Success Metrics  
   * 2.5 Product Vision Statement  
* 3.0 Scope and Limitations  
   * 3.1 Major Features  
   * 3.2 Project Scope  
   * 3.3 Limitations and Exclusions  
* 4.0 Context Description  
   * 4.1 User Classes and Characteristics  
   * 4.2 Operating Environment  
   * 4.3 Design and Implementation Constraints  
   * 4.4 Assumptions and Dependencies  
   * 4.5 Glossary of Terms  
   * 4.6 References

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

* **Improve Staff Productivity:** By eliminating the need for customers to physically visit the bank to process an international transfer, teller resources can be better allocated to resolving customer inquiries that require an in-person visit. 

* **Reduce Wait Times:** Having a digital method of filling out the RTA form reduces the necessity for customers to meet with a teller, thus lowering the amount of customers requiring an in-person visit and reducing the wait time for customers to meet with a teller. 
      
* **Customer and Employee Satisfaction:** Improving the accessibility and clarity of the international transfer system will reduce transaction processing time, and thus reduce complaints and improve employee and customer satisfaction. 
      
* **Reduction of Successive Bank Visits:** Introducing a user-friendly interface in the mobile app, coupled with straightforward instructions that provides customers with information to address inquiries and reduce unnecessary visits.  

## 2.4 Success Metrics  
The following success metrics are indicators that allow Pichincha Bank stakeholders to measure the overall success of the implemented solution: 

* **80% of International Transfers to be Completed Digitally:** International transfers are currently completed through a system that requires customers to physically visit the bank. Digital completion of 80% of international transfers would increase bank efficiency, financial profits and customer satisfaction. 
   
* **90% Success Rate of International Transfers via App:** With customers running into issues through filling out the RTA form or accessing the required security codes, international transfers are delayed or may include errors that further delay the transaction. This metric can be validated through a reduction in the number of customer inquiries and request-to-fund transfer times.   
   
* **Increase Customer Base to 2 million:** Internationally, Pichincha Bank has roughly 1.5 million members. Stakeholders aim to increase this number to approximately 2 million, which shall increase the rate of transactions and further increase company profits. This metric can be attained through increased customer satisfaction, in doing so, customers may refer Pichincha Bank to their family and friends and therefore increase the total number of customers intending to process international transfers with Pichincha Bank.  

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
* **International Transfer Security Pin:** A 4-digit pin must be entered upon each attempt to enter the International Transfer section of the bank app. The pin must be changed in the current app’s user settings page.
* **Transfer Status Notifications:** After a teller marks a transfer as either completed or rejected (see employee facing features for details), the ordering customer will receive a notification (via either email or SMS depending on preferred method selected in user settings). The notification must state success status, and next steps for failed transfers.
* **Help Information:** Help text is displayed containing more information about what is required to be entered in each data entry box on the digital RTA form.
      
The major features for the teller facing side are:  

* **International Transfer Processing Portal:** An interface in which a bank teller will view all requested international transfers and the RTA form corresponding to the transfer. The portal must sort all requested transfers into four categories: Unprocessed (new beneficiary), Unprocessed (existing beneficiary), In processing, and Completed.
* **Claim a Transfer:** A teller claims a transfer from the unprocessed transfers to show that they will be verifying the information in the transfer form and entering the information into the SWIFT alliance system to send a transfer. Once a transfer is claimed the software will sort it into the “in processing” category.
* **Complete a Transfer:** After an international transfer is successfully deposited to the beneficiary the teller processing that transfer will manually mark the transfer as complete. The software then sorts the transfer into the “completed” category.
* **Reject Transfer:** If there is an issue with the transfer which prevents it from being deposited the teller will manually reject the transfer. The software then sorts the transfer into the “completed” category.
* **Auto-Reject Transfer:** Whenever a new transfer is requested the software will automatically check if there is an insufficient balance in the account for the transfer, then if there is insufficient balance label the transfer as rejected and sort it into “completed”. If there is sufficient balance the system will sort the transfer into the correct “unprocessed" category.
* **Dealing with Rejected Transfers:** If a customer contacts the bank to fix a rejected transfer, a teller will claim the transfer and the system will move it to “in processing”.
         
## 3.2 Project Scope  
The project should deliver an addition to the current Pichincha Bank app which facilitates international transfers. Customer and bank teller interfaces must be created to allow for the various tasks undertaken by different user groups. The purpose of the software is to allow for international transfers to be made digitally, lowering strain on the brick and mortar bank while increasing ease of use for customers. 

The final product will support the business goals described in Section 2.  

* **Improve Staff Productivity:** The software will improve staff productivity by allowing customers to make international transfers without direct interaction with staff. The “Help Information” feature will provide additional helpful information to ordering customers. This will save the tellers time to spend on other important tasks.
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
|CON~1|Hardware Platform|The operating environment for the system encompasses mobile devices and web browsers. For users accessing the Pinchincha Bank mobile app, the platform includes mobile devices. Meanwhile, ordering customers accessing the application through the website utilize a laptop or desktop computer.|
|CON~2|Operating Environment |The supported operating environments include operating systems iOS and Android. Specifically, the system is designed to function seamlessly on the latest versions of both iOS and Android. Additionally, compatibility is maintained across various browsers such as Chrome, Microsoft Edge, Safari, and others for ordering customers accessing the application through the website.|
|CON~3|Software Applications|The system is integrated into an environment where it must integrate with the existing Pichincha Bank web and mobile app. The primary application is the Pichincha Bank mobile app, an existing app tailored for banking services. Additionally, the system interacts with the SWIFT Alliance system.|

## 4.3 Design and Implmentation Constraints  
||||
|-|-|-|
|CON~4|Existing System Integration|The designed system should conform and integrate seamlessly with the existing online banking application, as well as integrating with the current technology infrastructure and databases employed by Pichincha Bank. The responsibility for maintaining the app post-delivery will rest with the current app maintainers|
|CON~5|Application Languages|The software is mandated to support both English and Spanish languages. This linguistic flexibility is essential to cater to a diverse user base and enhance accessibility for customers who communicate in either language.|
|CON~6|Parallel Operations|The system must be capable of executing international transfer transactions concurrently. This constraint emphasizes the need for efficient parallel processing, ensuring that multiple international transfer operations committed within the same time frame can be executed simultaneously.|
|CON~7|Security Considerations|Security is a top priority, requiring robust measures to safeguard user data and financial transactions. The software must implement encryption protocols for secure data transmission, preventing unauthorized access. Additional security features include the introduction of the PIN for completing new forms related to international transfers, with provisions to change the PIN. Moreover, the use of Docusign for filling signatures on forms contributes to the overall security and authentication of transactions.|    

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
|Claim a Transfer|The action taken by a teller to indicate they are verifying the information for a transfer and will be processing it through the SWIFT system.|
|Complete a Transfer|The marking of a transfer as finished by a teller after successfully depositing the funds into the beneficiary account.|
|Customer Facing Side|The part of the app used by ordering customers to initiate and manage international transfers.|
|Digital Transaction Platform|The proposed solution for improving the international money transfer process, involving a digital feature integrated into Pichincha Bank's existing mobile and web applications to facilitate faster and more accurate transactions.|
|Docusign|A document signing software that you can use to legally—and securely—collect approvals online in minutes.|
|Help Information|Text displayed within the app providing guidance on how to complete the digital RTA form and other related queries.|
|Ordering Customer|The individual or entity initiating an international money transfer. This party is responsible for providing the necessary information and funds for the transfer.|
|Pichincha Bank|A private banking institution based in Ecuador, offering a range of services including investments, account management, and money transfers.|
|Reject Transfer|The action taken by a teller when a transfer cannot be processed due to issues with the information provided, leading to its cancellation.|
|RTA Form|(*Request for Transfer Abroad form*) The request form used by Pichincha Bank to enact a transfer of funds internationally.|
|SWIFT|(*Society for Worldwide Interbank Financial Telecommunication*) A global member-owned cooperative providing secure messaging services and interface software for financial transactions among its members.|
|SWIFT Alliance System|The digital platform used by Pichincha Bank to process international money transfers through the SWIFT network.|
|Teller|A customer facing bank employee that helps customer issues and requests in person.|  
|Teller Facing Side|The interface used by bank tellers to process requested international transfers, including verifying information and entering it into the SWIFT Alliance system.|

## 4.6 References  
|ID|Reference|
|--|---------|
|[1]|“Banco Pichincha,” Wikipedia, Jan. 28, 2024. https://es.wikipedia.org/wiki/Banco_Pichincha (accessed Feb. 02, 2024).|

---

# 5.0 System Features (Due Iteration 2 and beyond)  
This template illustrates organizing the functional requirements for the product by system features, the major services provided by the product. You may prefer to organize this section by use case, mode of operation, user class, object class, functional hierarchy, or combinations of these, whatever makes the most logical sense for your product.
   
   1. **System Feature 1**  
      State the feature name in just a few words.

      1. **Description and Priority**  
      Provide a short description of the feature and indicate whether it is high, medium, or low priority.
  
      2. **Functional Requirements**  
      Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available.
      Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature.
      Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

       REQ-1:

       REQ-2:

      3. **Use cases associated with the feature or functional requirement**  
      This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.

   2. **System Feature 2 (and so on)**  

6. **Data Requirements**  
      
   1. **Logical data model**  
   E.g., entity-relationship diagrams and UML class diagrams. You may provide a data model for the business operations or the data that the system modifies. Not the same thing as a database design data model. 
   2. **Data dictionary**  
   Composition of data strucutres, meaning, data type, length, format, and allowed values. 
   3. **Reports**  
   If your system will generate reports, then describe the attributes of those reports. You can detail the layout of the report.
   4. **Data acquisition, integrity, retention, and diposal**  
   If possible, describe how data is acquired, retained, and later on disposed. Describe the requirements for protecting the integrity of the data.  

7. **External Interface Requirements**  

   1. **User Interfaces**  
   Describe the logical characteristics of each interface between the software product and the users. This may include sample screen images, any GUI standards or product family style guides that are to be followed, screen layout constraints, standard buttons and functions (e.g., help) that will appear on every screen, keyboard shortcuts, error message display standards, and so on. Define the software components for which a user interface is needed.
      
   2. **Hardware Interfaces**  
   Describe the logical and physical characteristics of each interface between the software product and the hardware components of the system. This may include the supported device types, the nature of the data and control interactions between the software and the hardware, and communication protocols to be used.
   
   3. **Software Interfaces**  
   Describe the connections between this product and other specific software components (name and version), including databases, operating systems, tools, libraries, and integrated commercial components. Identify the data items or messages coming into the system and going out and describe the purpose of each. Describe the services needed and the nature of communications. Identify data that will be shared across software components.
       
   4. **Communication Interfaces**  
   Describe the requirements associated with any communications functions required by this product, including e-mail, web browser, network server communications protocols, electronic forms, and so on.

8. **Software Quality Attributes**  
Sepcify requirements that include performance, security, reusability, maintainability, usability, availability, interoperability, etc.

9. **Analysis Models**  

10. **Appendix**
