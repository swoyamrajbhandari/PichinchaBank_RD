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
   Describe the business problem that is being solved or the process being improved. Describe the needs of typical customers or of the target market. Present customer problems that the new product will address. 

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
   Write a concise vision statement that summarizes the long-term purpose and intent of the product.   Describe the context and origin of the product being specified in this RD. For example, state whether this product is a follow-on member of a product family, a replacement for certain existing systems, or a new, self-contained product. If the RD defines a component of a larger system, relate the requirements of the larger system to the functionality of this software and identify interfaces between the two. A simple diagram that shows the major components of the overall system, subsystem interconnections, and external interfaces can be helpful but not required.

3. **Scope and Limitations**  

   1. **Major Features**  
   Summarize the major features the product contains or the significant functions that it performs or lets the user perform. Details will be provided in Section 5, so only a high level summary is needed here. Organize the functions to make them understandable to any reader of the RD. Think about how users will use the features to ensure the list is complete. Also ensure that it does not include unnecessary features that sound interesting, but does not provide customer value.     

   2. **Project Scope**  
   Provide a short description of the software being specified and its purpose, including relevant benefits, objectives, and goals. Relate the software to corporate goals or business strategies.

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

   5. **Assumptions and Dependencies**  
   List any assumed factors (as opposed to known facts) that could affect the requirements stated in the RD. These could include third-party or commercial components that you plan to use, issues around the development or operating environment, or constraints. The project could be affected if these assumptions are incorrect, are not shared, or change. Also identify any dependencies the project has on external factors, such as software components that you intend to reuse from another project.
   
   6. **Glossary of Terms**  
   Define all the terms necessary to properly interpret the RD, including acronyms and abbreviations.

   7. **References**  
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
