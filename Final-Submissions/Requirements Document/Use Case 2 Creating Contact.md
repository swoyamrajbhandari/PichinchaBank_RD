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
| **Other Information:** | The system should allow for easy input and editing of contact details, with the ability to import from or export to external address books. |
| **Assumptions:** | - The system has a reliable and user-friendly interface for contact creation. <br> - The Contact Database is robust and capable of handling concurrent interactions from multiple users. |
