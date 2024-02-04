# Requirements Document - Banco Pichincha (January 30, 2024)

## Revision History

| Name | Date | Reason for Changes | Version |
|------|------|--------------------|---------| 
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |  

1. **Overview**  
Provide an overview of the sections and contents of the document

2. **Business Requirements**  

   1. **Background**  
   Pichincha Bank is a private bank based in Ecuador with approximately 1.5 million customers [1]. The Bank offers a variety of online services to its members through its mobile and web banking portals. These services include online investing, bank certificates, credit and debit account management, and domestic money transfers. Pichincha Bank is looking to improve their international money transfer process due to staff productivity and customer satisfaction concerns through the implementation of a digital system. 

   Pichincha Bank’s international money transfer process utilizes a physical Request for Transfer Abroad form (RTA) and requires tellers to manually input data from the completed RTA form into the digital Society for Worldwide Interbank Financial Telecommunication (SWIFT) Alliance system. The current system is inefficient for both bank employees and customers. The following steps further describe the current system:

1. An ordering customer arrives at a Pichincha Bank location and waits for an available teller
2. The customer completes a paper RTA form with information relating to the transfer source account, beneficiary    account, monetary amount, and SWIFT code
3. A teller verifies this information and manually inputs the data into the SWIFT Alliance system
4. A teller initiates a SWIFT transaction
5. The beneficiary’s bank receives the transfer and verifies the information
6. The funds are deposited into the beneficiary account approximately 7 days after initiation of the SWIFT          transaction

   The process outlined above assumes no errors were made by either the customer completing the RTA form, or the bank teller inputting the data. If errors occur and are not resolved before initiation of the SWIFT transaction, it takes approximately 3 weeks to complete the transaction. 

   In response to concerns about the efficiency of the current system, Pichincha Bank is seeking to enhance its international money transfer process. The subsequent segments of Section 2 will further detail Pichincha Bank’s challenges, objectives, and the success metrics of a proposed solution. 
 

   2. **Business Opportunity**  
   
    The current financial transaction system for internationals is inefficient as it is affecting both customers and employees. 
- Customers often experience lengthy wait times at the bank and spend a significant amount of time filling out the physical forms. Simultaneously, tellers have to spend time walking the clients through the physical forms and making sure that they have enough, correct information. 
- The long duration for the transaction to complete tends to cause customers dissatisfaction, frustration. As a result, it will have a detrimental impact on the organization’s reputation, profits and as well as employees’ performance because they have to deal with unhappy customers. 

    Our team proposes the implementation of a digital transaction. This initiative aims to not only speed up the transaction process but also significantly improve accuracy, productivity. By reducing transaction time and minimizing eros, the new digital feature will elevate the overall client’s experience and satisfaction as well as fostering a positive environment for our employees.


   3. **Business Objectives**  
   The business objectives of Pichincha Bank are designed to help improve the overall process of international transactions. The following are objectives that are designed to help improve Pichincha Bank’s success through    the following means: 

   Improve staff productivity: By eliminating the need for customers to physically visit the bank to process an international transfer, teller resources can be better allocated to resolving customer inquiries that 
   require an in-person visit. 

   Reduce wait times: Having a digital method of filling out the RTA form reduces the necessity for customers to meet with a teller, thus lowering the amount of customers requiring an in-person visit and reducing the 
   wait time for customers to meet with a teller. 
      
   Customer and employee satisfaction: Improving accessibility of processing an international transfer helps reduce processing time for a transactions request to approval system, which will reduce complaints and 
   in turn improve employee and customer satisfaction. 
      
   Reduction of successive bank visits: Introducing a user-friendly interface in the mobile app, coupled with straightforward instructions that provides customers with information to address inquiries and reduce 
   unnecessary visits.  

   4. **Success Metrics**  
   The following success metrics are the indicators that allow stakeholders of Pichincha Bank to measure the overall success of the company: 

   80% of international transfers to be completed digitally: International transfers are currently completed through a system that requires customers to physically visit the bank. This metric allows the company to gauge  
   how increasing the amount of digital transfers to 80% would increase the efficiency of transactions through greater financial profits or customer satisfaction. Implementing this metric is achievable through methods 
   such as reduction of wait times for customers processing transactions through tellers at the bank. 
   
   90% of international transfers through the app are completed on the first try: With customers running into issues through filling out the RTA form or accessing the required security codes, international transfers are 
   delayed or may include errors that further delay the transaction. This metric can be implemented through methods such as dedicated staff or other external groups implementing software designed to assist customers with 
   inquiries, such as a Q&A page or real-time online customer support. 
   
   Increase the number of customers of Pichincha Bank to 2 million: Internationally, Pichincha Bank has roughly 1.5 million users. Stakeholders aim to increase this number to roughly 2 million, which shall increase the 
   rate of transactions and further increase company profits. This metric can be attained through increased customer satisfaction, in doing so, customers may refer Pichincha Bank to their family and friends and therefore 
   increase the total number of customers intending to process international transfers with Pichincha Bank.
   
   75% of users complete transactions through the app: With stakeholders intending to shift roughly 80% of transactions online, a goal of increased use of the mobile app to process transactions remotely is 
   an objective that stakeholders will attempt to implement. This metric can be accomplished through methods such as technology staff or an external developer group implementing user interfaces or improved accessibility 
   to the app components used by customers when processing transactions. 

   5. **Product Vision Statement**  
   The International Bank Transfer System is a system integrated into the existing Pichincha Bank web and mobile applications that provides customers the ability to perform an international transfer without the need to meet with a bank employee in person. The system will provide customers the ability to add and store international contacts to which funds can be transferred, as well as providing a digital interface for completing the RTA form, allowing customers to provide and submit the required information to complete an international transfer remotely. The functionality of the system also extends to administrative users, providing a review and processing portal for a bank employee to process international transfer requests created by a customer. By providing an alternative to in person, paper form international transfers, the International Bank Transfer System aims to direct 80% of the international transfer customer base to a Pichincha Bank application, thus freeing teller resources for tasks requiring in person support.

3. **Scope and Limitations**  

   1. **Major Features**  
   The implemented system needs to be an addition to the current bank app which will facilitate international transfers. There is a customer facing side of the app and an employee facing side which each require different features.

      The major features for the customer facing side are:
       * Digital RTA (“Request for Transfers Abroad”) Form: A digital form which prompts an ordering customer for the information required to make an international transfer. The digital form will request the same information as the current physical RTA form.
       * Add New International Contact: Create a new contact will have the ordering customer fill out the digital RTA form for a new beneficiary and then add the new contact to the their contact list.
       * Auto-Fill Form: Provide the ordering customer with the option to save RTA form data the first time they fill it out to be auto-filled for all future uses. Saved and auto filled information will be data specific to the ordering customer and not the beneficiary.
       * Saved Contacts: Allow the ordering customer to view a list of every contact they have previously submitted the RTA form for. Each contact must have a contact page which states whether previous transfers were successfully completed, date of transaction, and transaction amount for that contact.
       * Transfer to Saved Contact: Ordering customer is able to make an international transfer to one of the saved contacts without filling out the RTA form again. Transaction specific information including the transfer amount and reason must be collected.
       * International Transfer Security Pin: A 4-digit pin must be entered upon each attempt to enter the International Transfer section of the bank app. The pin must be changed in the current app’s user settings page.
       * Transfer Status Notifications: After a teller marks a transfer as either completed or rejected (see employee facing features for details), the ordering customer will receive a notification (via either email or SMS depending on preferred method selected in user settings). The notification must state success status, and for failed transfers must state next steps.
       * Help Information: Help text is displayed containing more information about what is required to be entered for each data entry box on the digital RTA form.
      
      The major features for the employee facing side are:
       * International Transfer Processing Portal: An interface in which a bank employee will view all requested international transfers and the RTA form corresponding to the transfer. The portal must sort all requested transfers into four categories: Unprocessed (new beneficiary), Unprocessed (existing beneficiary), In processing, and Completed.
       * Claim a Transfer: A Teller claims a transfer from the unprocessed transfers to show that they will be verifying the information in the transfer form and entering the information into the SWIFT alliance system to send a transfer. Once a transfer is claimed the software will sort it into the “in processing” category.
       * Complete a Transfer: After an international transfer is successfully deposited to the beneficiary the teller processing that transfer will manually mark the transfer as complete. The software then sorts the transfer into the “completed” category.
       * Reject Transfer: If there is an issue with the transfer which prevents it from being deposited the Teller will manually reject the transfer. The software then sorts the transfer into the “completed” category.
       * Auto-Reject Transfer: Whenever a new transfer is requested the software will automatically check if there is an insufficient balance in the account for the transfer, then if there is insufficient balance label the transfer as rejected and sort it into “completed”. If there is sufficient balance the system will sort the transfer into the correct “unprocessed" category.
       * Dealing with Rejected Transfers: If a customer contacts the bank to fix a rejected transfer, a teller will claim the transfer and the system will move it to “in processing”.
         

   2. **Project Scope**  
   The project should deliver an addition to the current Pichincha Bank app which facilitates international transfers. Customer and employee interfaces need to be created to allow for the various tasks undertaken by different user groups. The purpose of the software is to allow for international transfers to be made digitally, lowering strain on the brick and mortar bank while increasing ease of use for customers. 

      The final product will support the business goals described in Section 2.
       * Improve staff productivity: The software will improve staff productivity by allowing customers to make international transfers without direct interaction with staff. As well the software “Help Information” feature will provide extra information to ordering customers. This will save the tellers time to spend on other important tasks.
       * Reduce wait times: The software will eliminate wait times to fill out RTA forms for online international transfers by immediately providing online users with RTA forms. The in person wait time to fill out RTA forms will also be reduced as the majority of ordering customers will prefer the benefits filling out the form online provides. 
       * Customer satisfaction: The software will contain numerous features designed to improve customer satisfaction. Ordering customers will be pleased by not needing to travel to the bank to make international transfers, as the software will allow all necessary tasks to be performed online saving time and energy. The saved contacts feature the software provides will also save ordering customers the hassle of trying to send money to an international beneficiary repeatedly as it is now easily facilitated within the app reducing need for tellers to process the same information each time a transfer to the same beneficiary, shortening time till transaction is made.
       * Employee satisfaction: Employee satisfaction will increase as they will not have to work with paper forms for the majority of international transfers. The employee portal will easily allow for information to be read and added to the SWIFT Alliance app, employees will not need to worry about the confusion of misreading customers’ handwriting.
      

   3. **Limitations and Exclusions**  

4. **Context Description**  

   1. **User Classes and Characteristics**  
   Identify the various user classes that you anticipate will use this product. User classes may be differentiated based on frequency of use, subset of product functions used, technical expertise, security or privilege levels, educational level, or experience. Describe the characteristics of each user class. Certain requirements may pertain only to certain user classes. Distinguish the favored user classes from those who are less important to satisfy.

   2. **Operating Environment**  
   
   CON-1. Hardware platform: The operating environment for the system encompasses mobile devices and web browsers. For 
   users accessing the Pinchincha Bank mobile app, the platform includes mobile devices. Meanwhile, ordering customers 
   accessing the app through the website, utilize a web browser.

   CON-2. Operating systems: The supported operating systems comprise iOS and Android. Specifically, the system is designed 
   to function seamlessly on the latest versions of both iOS and Android. Additionally, compatibility is maintained across 
   various browsers such as Chrome, Microsoft Edge, Safari, and others for ordering customers accessing the app through the 
   website.

   CON-3. Software components or applications: The system is integrated into an environment where it must coexist with the 
   existing Pichincha Bank web and mobile app. The primary application is the Pichincha Bank mobile app, an existing app 
   tailored for banking services. Additionally, the system interacts with the Swift Alliance program.  


   3. **Design and Implmentation Constraints**

   Issues that will limit the options available to the developers:

   CON-4. Regulatory compliance: The development of the system is bound by strict regulatory compliance requirements. The 
   development process must adhere to both local and international banking regulations, ensuring the system’s alignment 
   with established standards. Furthermore, compliance with data protection laws, such as the General Data Protection 
   Regulation (GDPR), is of paramount importance, particularly concerning the handling of financial information.

   CON-5. The designed system should conform and integrate seamlessly with the existing app.

   CON-6. The software should align with the current technology infrastructure and databases employed by the Pichincha Bank.

   CON-7. Language requirements: The software is mandated to support both English and Spanish languages. This linguistic 
   flexibility is essential to cater to a diverse user base and enhance accessibility for customers who communicate in 
   either language.

   CON-8. Parallel operations: The system should be capable of executing international transfer operations concurrently. 
   This constraint emphasizes the need for efficient parallel processing, ensuring that multiple international transfer 
   operations committed within the same time frame can be executed simultaneously. 

   CON-9. Security considerations: Security is a top priority, requiring robust measures to safeguard user data and 
   financial transactions. The software must implement encryption protocols for secure data transmission, preventing 
   unauthorized access. Additional security features include the introduction of the PIN for completing new forms related 
   to international transfers, with provisions to change the PIN. Moreover, the use of Docusign for filling signatures on 
   forms contributes to the overall security and authentication of transactions.

   CON-10. Design conventions or programming standards: Given that the system is an added component to the Pinchincha Bank 
   mobile app, it is crucial to adhere to the already established design conventions and programming standards. 
   Importantly, the responsibility for maintaining the app post-delivery will rest with the current app maintainers.

   4. **Assumptions and Dependencies**  
   The successful implementation of this project relies on several critical assumptions and dependencies. The following factors form the foundation upon which the project’s framework is built:
      - User Authentication: We assume that the mechanisms for user authentication in Pichincha Bank's current application are robust and secure. This includes the assumption that the current security protocols are sufficient to protect sensitive financial transactions and personal data against potential cyber threats. Any changes or failures in this area could impact user trust and system integrity.
      - Existing Technological Infrastructure: We rely on the current app and website’s ability to support the addition of new features without compromising performance. This includes assumptions about the scalability of the current system to handle an increase in user traffic and international transfer demands.
      - Third Party Services: We depend on the stability and reliability of external platforms like SWIFT Alliance for processing transactions and Docusign for digital signatures. Any significant disruptions in these services could impact the functionality and reliability of the international transfer system.
      - Legal Compliance: We assume that the addition of international transfers to the existing application will comply with current and future international regulations. Changes in banking regulations could require significant adjustments to the project scope or design. 
      - User Adoption: We assume that users will readily transition to the new online method for international transfers.
     
      These assumptions should be regularly reviewed to ensure they remain valid throughout the project’s development.
   
   5. **Glossary of Terms**  
   Define all the terms necessary to properly interpret the RD, including acronyms and abbreviations.

   6. **References**  
   List any other documents or Web addresses to which this RD refers. These may include user interface style guides, contracts, standards, system requirements specifications or use case documents. Provide enough information so that the reader could access a copy of each reference, including title, author, version number, date, and source or location.

[1]“Banco Pichincha,” Wikipedia, Jan. 28, 2024. https://es.wikipedia.org/wiki/Banco_Pichincha (accessed Feb. 02, 2024).

---

5. **System Features** (Due Iteration 2 and beyond)  
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
