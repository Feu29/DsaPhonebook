# DsaPhonebook


DSA PROJECT


 
GROUP MEMBER 	STUDENT NUMBER 
Mutuku Aloys 	224052470 
Siyamba Alfeus  	224065092 
Simasiku Muhinda 	224064924 
Erick Ipangelwa 	224080385 
Uendjipa Kaukuetu 	224064657 
Shikundule T Mesias 	224033689 
 
 



 
 
SECTION A 
- Data Structure:  We used an array to store the data that a user enters and the array loads the data into into the text file and and this textfile as a database . 
 
PhoneBook System 
 
Module/function Pseudocode Representation  
1.FUNCTION InsertContact(contacts, newContact)
    IF contacts IS NULL THEN
        contacts = new ArrayList
    ENDIF
    contacts.add(newContact)  // Add the contact to the list
    writeContactToFile(newContact)  // Write contact to file
END FUNCTION

 
  
2. FUNCTION SearchContact(contacts){
   String search;  
       FOR(int i = 0 ; i<contacts; i++){
        IF (contact.firstName = search OR contact.lastName == search OR contact.phoneNumber == search OR contact.address == search) THEN
             RETURN resultList
    END FOR
    IF resultList IS EMPTY THEN
        RETURN "Contact not found"
END FUNCTION

FUNCTION DisplayContacts(contacts)
    FOR each contact IN contacts DO
        DISPLAY (contact.firstName , contact.lastName,contact.phoneNumber,contact.address);
    END FOR
END FUNCTION
 
 
4. Display All Contacts 
-Shows all the contacts in the phonebook 
 
FUNCTION DisplayContacts(head)     current = head 
    WHILE current IS NOT NULL DO 
        PRINT current.name + ": " + current.phoneNumber 
        current = current.next 
    ENDWHILE 
END FUNCTION 
 
FUNCTION DeleteContact(contacts, index)
    IF index >= 0 AND index < contacts.size THEN
        contacts.remove(index)
        saveContactsToFile(contacts)
    ELSE
        PRINT "Contact not found"
    ENDIF
END FUNCTION
 
 
5.FUNCTION UpdateContact(contacts, index, newContact)
    IF index >= 0 AND index < contacts.size THEN
        contacts[index] = newContact
        saveContactsToFile(contacts)
    ELSE
        PRINT "Contact not found"
    ENDIF
END FUNCTION
 
 
6.FUNCTION SortContacts(contacts, ascending)
    IF ascending IS TRUE THEN
        SORT contacts BY contact.firstName + " " + contact.lastName ASC
    ELSE
        SORT contacts BY contact.firstName + " " + contact.lastName DESC
    ENDIF
    saveContactsToFile(contacts)  // Save sorted contacts to file
    RETURN contacts
END FUNCTION

 
 
 
 
7. FUNCTION AnalyzeSearchEfficiency(contacts, query)
    startTime = CURRENT_TIME
    SearchContact(contacts, query)
    endTime = CURRENT_TIME
    PRINT "Search Time: " + (endTime - startTime)
END FUNCTION
 
 
 
 
 
 
Efficiency Analysis 
•	Insertion: O(n) (average) since we traverse to the end of the list. 
•	Search: O(n) (linear) since we may need to check each contact. 
•	Display: O(n) as we go through the entire list. 
•	Deletion: O(n) for searching. 
•	Update: O(n) to find the contact. 
•	Sort: O(n^2) (insertion sort) for linked list; could use merge sort for better efficiency. 
   
Flowchart Representation 
 
1.	Insert Contact 
 
  ![image](https://github.com/user-attachments/assets/48c5caaa-9eda-4e36-aa20-afa4a71305e4)

 
 
 
 
2.	Search Contact 
 
 
  ![image](https://github.com/user-attachments/assets/6cb20e6c-7ac9-420f-ae1b-cad631787ecf)

 
 
 
 
 
 
 
 
 
 
3.	Display All Contacts 
  
 
 
 
 ![image](https://github.com/user-attachments/assets/9d4bdea6-2b22-4410-a580-d72ed394c0f1)

 
 
 
 
4.	Delete Contact 
  
 
 
 
 ![image](https://github.com/user-attachments/assets/a52dd233-84ae-4513-8897-c77d465ea856)

 
 
 
 
 
5.	Update Contact 
 
 
  
 ![image](https://github.com/user-attachments/assets/09328faa-99f7-466f-a9d4-2924d71b0395)

 
 
 
 
 
 
 
 
6.	Sort Contacts (optional) 
	i. 	For sorted contacts(lone diagram)  
 
 	

 ![image](https://github.com/user-attachments/assets/329a28d2-c20b-4a6b-91c8-294e76403085)

 
 
 
 
 
 	 
	ii. 	For SortedInsert 
  
 ![image](https://github.com/user-attachments/assets/287f2f9f-4273-4f19-bec6-9e7f6dd1befe)

 
 
 
 
 
7.Analyze Search Efficiency 
 
 
 ![image](https://github.com/user-attachments/assets/aec83e5c-84ef-4061-936f-7bb86a6ae001)

 
 
 
  
 
 
 
 
 
 
 
 




FLOW Chart OF THE ENTIRE PHONE BOOK



 ![image](https://github.com/user-attachments/assets/4309e1ff-0353-424c-ae63-482fab6e09eb)


 
