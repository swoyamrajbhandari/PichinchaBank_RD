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
   Summarize the rationale and context for the new product or for changes to be made to an existing one. 

   2. **Business Opportunity**  
   Describe the business problem that is being solved or the process being improved. Describe the needs of typical customers or of the target market. Present customer problems that the new product will address. 

   3. **Business Objectives**  
   Summarize the important business benefits the product will provide in a quantitative and measurable way. Organizations generally undertake a project to solve a problem or exploit an opportunity. Business objectives define ways to measure achievement of business goals. 

   4. **Success Metrics**  
   Indicators that stakeholders will use to define and measure success on the project. What are the factors that will have the greatest impact on achieving success (i.e., could include aspects within and external to the organization).

   5. **Product Vision Statement**  
   Write a concise vision statement that summarizes the long-term purpose and intent of the product.   Describe the context and origin of the product being specified in this RD. For example, state whether this product is a follow-on member of a product family, a replacement for certain existing systems, or a new, self-contained product. If the RD defines a component of a larger system, relate the requirements of the larger system to the functionality of this software and identify interfaces between the two. A simple diagram that shows the major components of the overall system, subsystem interconnections, and external interfaces can be helpful but not required.

3. **Scope and Limitations**  

   1. **Major Features**  
   Summarize the major features the product contains or the significant functions that it performs or lets the user perform. Details will be provided in Section 5, so only a high level summary is needed here. Organize the functions to make them understandable to any reader of the RD. Think about how users will use the features to ensure the list is complete. Also ensure that it does not include unnecessary features that sound interesting, but does not provide customer value.     

   2. **Project Scope**  
   Provide a short description of the software being specified and its purpose, including relevant benefits, objectives, and goals. Relate the software to corporate goals or business strategies.

   3. **Limitations and Exclusions**
      The Pichincha Bank international transfer project aims to enhance the efficiency and user-friendliness of cross-border transactions through its mobile and web applications. This initiative is driven by the need to improve customer and staff satisfaction, reduce transaction times, and address the current system's inefficiencies. However, the project's scope is defined by certain limitations and exclusions that are essential to understand for setting realistic expectations and achieving the desired outcomes. Below is an expanded view of the limitations, including newly identified constraints based on the detailed project document, and the exclusions that shape the project's framework.

**Limitations:**

**Delayed Interactions with Real-World Bank Tellers:** The project is limited by the inherent delays in interactions with bank tellers, which can extend the processing time for international transfers. This limitation is a consequence of the current reliance on manual verification and data entry processes.

**Interactions with the Swift System:** The efficiency of international transfers is also limited by the interactions with the Swift System, which is an external dependency with its own processing times and operational constraints.

**Integration with Existing Banking Systems:** The project must seamlessly integrate with Pichincha Bank's current banking systems and protocols, which may limit the flexibility in implementing certain features or require additional time for compatibility adjustments.

**Technological Constraints:** The project is limited by the current technological infrastructure of Pichincha Bank, including hardware capabilities, software compatibility, and the operational capacity of the mobile and web platforms.

**Dependency on External Services:** The reliance on third-party services such as Swift Alliance and Docusign introduces limitations related to their availability, reliability, and compatibility with the bank's systems.

**Exclusions:**

**Legality and Security:** Issues related to legality and security, while critical to the banking operations, are excluded from the project's direct scope. These areas are assumed to be addressed by other specialized teams within Pichincha Bank, ensuring compliance with relevant laws and regulations without burdening the project team with areas outside their expertise.

**Customer Education on Financial Regulations:** Educating customers on the complexities of international financial regulations is outside the scope of this project. While the app aims to simplify the transfer process, the responsibility for understanding the legal implications of international transfers remains with the customers.

By clearly defining these limitations and exclusions, Pichincha Bank sets a realistic framework for the international transfer project, ensuring that stakeholders have a clear understanding of what the project will deliver and the areas that are beyond its immediate scope. This clarity is essential for managing expectations and focusing efforts on achieving the project's primary objectives of improving efficiency, customer satisfaction, and staff productivity within the defined constraints.


4. **Context Description**  

   1. **User Classes and Characteristics**  
  The Pichincha Bank international transfer system is designed to cater to a diverse range of users, differentiated by their interaction frequency, technical expertise, security needs, and the specific functionalities they utilize. Given the system's dual focus on facilitating international transfers for both individual customers and businesses, as well as enabling administrative oversight and management, we have identified two primary user classes: the Customer Class and the Administrative Class. Each of these classes is further subdivided to address distinct user needs and priorities.

**Customer Class**

**Subclass 1: Regular User**

**Characteristics:** Individuals using the system for personal international money transfers. This group is characterized by a wide range of technical expertise, from novice to advanced users, and includes both infrequent and regular users.

**Privileges:** Regular Users are able to initiate and manage international transfers, access and fill out the digital RTA Form, save beneficiary details for future transactions, and receive status notifications about their transfers.

**Special Considerations:** While Regular Users have access to the full suite of transfer functionalities, their transactions are processed with standard priority, which may result in slightly longer processing times during peak periods compared to Business Users.

**Subclass 2: Business User**

**Characteristics:** Organizations or entities that require the system for business-related international transfers. This subclass includes small and medium enterprises, large corporations, and other financial entities. Business Users are expected to have a higher volume of transactions and a greater familiarity with international transfer processes.

**Privileges:** In addition to the privileges available to Regular Users, Business Users are given priority processing to accommodate the higher volume and urgency often associated with business transactions. This ensures faster processing times and supports the operational needs of businesses.

**Special Considerations:** Business Users may require additional support for batch processing of transactions and might benefit from enhanced security measures and detailed transaction reporting for accounting purposes.


**Administrative Class**

**Subclass 1: Bank Tellers**

**Characteristics:** Bank employees responsible for verifying and processing international transfer requests. This subclass possesses a high level of technical expertise and understanding of banking regulations and the Swift System.

**Privileges:** Bank Tellers can access and manage incoming transfer requests, verify transaction details, input information into the Swift System, and update the transaction status. They play a critical role in ensuring the accuracy and security of transfers.

**Responsibilities:** Their primary responsibility includes managing the transfer workflow, from claim to completion or rejection, and providing support to customers as needed.

**Subclass 2: System Administrators**

**Characteristics:** Technical staff responsible for the maintenance, security, and operational integrity of the international transfer system. This group has advanced technical expertise and comprehensive access to the system's backend.

**Privileges:** System Administrators have the highest level of access, including system configuration, user management, security protocol adjustments, and troubleshooting. They ensure the system's smooth operation and safeguard against technical issues or security threats.

**Responsibilities:** Monitoring system performance, implementing updates, ensuring compliance with security standards, and addressing any technical issues that arise.

By distinguishing between these user classes and their respective characteristics, Pichincha Bank can tailor the international transfer system to meet the varied needs of its users effectively, ensuring a seamless and secure experience for both customers and administrative personnel.

   2. **Operating Environment**  
   Describe the environment in which the software will operate, including the hardware platform, operating system and versions, and any other software components or applications with which it must peacefully coexist.

   3. **Design and Implmentation Constraints**  
   Describe any items or issues that will limit the options available to the developers. These might include: corporate or regulatory policies; hardware limitations (timing requirements, memory requirements); interfaces to other applications; specific technologies, tools, and databases to be used; parallel operations; language requirements; communications protocols; security considerations; design conventions or programming standards (for example, if the customer’s organization will be responsible for maintaining the delivered software).

   4. **Assumptions and Dependencies**  
   List any assumed factors (as opposed to known facts) that could affect the requirements stated in the RD. These could include third-party or commercial components that you plan to use, issues around the development or operating environment, or constraints. The project could be affected if these assumptions are incorrect, are not shared, or change. Also identify any dependencies the project has on external factors, such as software components that you intend to reuse from another project.
   
   5. **Glossary of Terms**  
   Define all the terms necessary to properly interpret the RD, including acronyms and abbreviations.

   6. **References**  
   List any other documents or Web addresses to which this RD refers. These may include user interface style guides, contracts, standards, system requirements specifications or use case documents. Provide enough information so that the reader could access a copy of each reference, including title, author, version number, date, and source or location.

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
