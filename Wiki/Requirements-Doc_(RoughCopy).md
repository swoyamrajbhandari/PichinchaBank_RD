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
       * Complete a Transfer: After an international transfer is successfully deposited to the beneficiary the teller processing that transfer will mark the transfer as complete. The software then sorts the transfer into the “completed” category.
       * Reject Transfer: If there is an issue with the transfer which prevents it from being deposited the Teller will reject the transfer. The software then sorts the transfer into the “completed” category.
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
