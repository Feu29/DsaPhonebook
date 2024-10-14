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
- Data Structure:  The phonebook application will use a linked list data structure. A linked list will allow us to dynamically manage contacts, making it easier to insert and delete contacts without worrying about fixed sizes. 
 
PhoneBook System 
 
Module/function Pseudocode Representation  
1. Insert Contact 
- Allows us to add a new contact to the phonebook 
 
FUNCTION InsertContact(head, newContact) 
    IF head IS NULL THEN         head = newContact     ELSE         current = head         WHILE current.next IS NOT NULL DO 
            current = current.next         ENDWHILE 
        current.next = newContact 
    ENDIF 
    RETURN head 
END FUNCTION 
 
 
  
2. Search Contact 
-Finds a contact by name 
 
FUNCTION SearchContact(head, name)     current = head 
    WHILE current IS NOT NULL DO 
        IF current.name == name THEN 
            RETURN current         ENDIF 
        current = current.next 
    ENDWHILE 
    RETURN "Contact not found" END FUNCTION 
 
 
3. Display All Contacts 
-Shows all the contacts in the phonebook 
 
FUNCTION DisplayContacts(head)     current = head 
    WHILE current IS NOT NULL DO 
        PRINT current.name + ": " + current.phoneNumber 
        current = current.next 
    ENDWHILE 
END FUNCTION 
 
4. Delete Contact 
-Removes a contact from the phonebook 
 
FUNCTION DeleteContact(head, name) 
    IF head IS NULL THEN 
        PRINT "Phonebook is empty" 
        RETURN head 
    ENDIF 
 
    IF head.name == name THEN         head = head.next 
        RETURN head 
    ENDIF 
 
    current = head 
    WHILE current.next IS NOT NULL DO         IF current.next.name == name THEN             current.next = current.next.next 
            RETURN head         ENDIF 
        current = current.next 
    ENDWHILE 
    PRINT "Contact not found" 
    RETURN head END FUNCTION 
 
 
 
5. Update Contact 
-Changes the details of an existing contact 
 
FUNCTION UpdateContact(head, name, newContact)     current = head 
    WHILE current IS NOT NULL DO 
        IF current.name == name THEN             current.name = newContact.name 
            current.phoneNumber = newContact.phoneNumber 
            RETURN         ENDIF 
        current = current.next 
    ENDWHILE 
    PRINT "Contact not found" END FUNCTION 
 
 
 
6. Sort Contacts (optional) 
-Organizes the contacts in alphabetical order by name 
 
FUNCTION SortContacts(head) 
    IF head IS NULL OR head.next IS NULL THEN 
        RETURN head 
 
    sorted = NULL     current = head 
    WHILE current IS NOT NULL DO 
        next = current.next 
        sorted = SortedInsert(sorted, current) 
        current = next 
    ENDWHILE 
    RETURN sorted 
END FUNCTION 
 
FUNCTION SortedInsert(sorted, newContact) 
    IF sorted IS NULL OR sorted.name >= newContact.name THEN         newContact.next = sorted 
        RETURN newContact 
    ENDIF 
 
    current = sorted 
    WHILE current.next IS NOT NULL AND current.next.name < 
newContact.name DO 
        current = current.next     ENDWHILE 
    newContact.next = current.next     current.next = newContact 
    RETURN sorted END FUNCTION 
 
 
 
 
7. Analyze Search Efficiency 
-Measures how long the search operation takes 
 
FUNCTION AnalyzeSearchEfficiency(head, name) 
    startTime = CURRENT_TIME     SearchContact(head, name)     endTime = CURRENT_TIME 
    PRINT "Search Time: " + (endTime - startTime) END FUNCTION 
 
 
 
 
 
 
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
 
 
  
 
 
 
 
 
 
 
 
 
 
3.	Display All Contacts 
  
 
 
 
 
 
 
 
 
4.	Delete Contact 
  
 
 
 
 
 
 
 
 
 
5.	Update Contact 
 
 
  
 
 
 
 
 
 
 
 
 
6.	Sort Contacts (optional) 
	i. 	For sorted contacts(lone diagram)  
 
 	

 
 
 
 
 
 
 	 
	ii. 	For SortedInsert 
  
 
 
 
 
 
 
7.Analyze Search Efficiency 
 
 
 
 
 
 
  
 
 
 
 
 
 
 
 




FLOW Chart OF THE ENTIRE PHONE BOOK



 

 
