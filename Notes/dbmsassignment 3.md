  

Model

---

### **Assignment-3**

**Subject Co-ordinator: Prof. Vaidehi Gondaliya**  
**Branch: CE/IT/SPL**  
**Subject Name: DBMS**  
**Semester: 3rd**

**1. Define Entity Relationship (ER) Model. Draw and explain an ER diagram for a "Library Management System.**

The **Entity-Relationship (ER) Model** is a high-level conceptual data model that describes the structure of a database in a graphical way. It represents real-world objects as entities, their characteristics as attributes, and the associations between entities as relationships. It's widely used in database design to understand and visualize data requirements.

**Components of an ER Model:**

- **Entities:** Real-world objects or concepts (e.g., Book, Borrower, Librarian). Represented by rectangles.
    
- **Attributes:** Properties or characteristics of an entity (e.g., BookID, Title, Author for a Book). Represented by ovals.
    
- **Relationships:** Associations between two or more entities (e.g., a Borrower borrows a Book). Represented by diamonds.
    
- **Cardinality:** Defines the number of instances of one entity that can be associated with instances of another entity (e.g., one-to-one, one-to-many, many-to-many).
    

**ER Diagram for a "Library Management System":**  
**Refer to a diagram depicting the following entities, relationships, and attributes:**

- **Entities:**
    
    - **BOOK:** (Attributes: BookID (PK), Title, Author, ISBN, PublicationYear, Status)
        
    - **BORROWER:** (Attributes: BorrowerID (PK), Name, Address, Phone, Email)
        
    - **LIBRARIAN:** (Attributes: LibrarianID (PK), Name, EmployeeID)
        
- **Relationships:**
    
    - **BORROWS:** (Between BORROWER and BOOK) - Many-to-Many (M:N) with attributes like BorrowDate, DueDate, ReturnDate. (A Borrower can borrow multiple Books, and a Book can be borrowed by multiple Borrowers over time).
        
    - **MANAGES:** (Between LIBRARIAN and BOOK) - One-to-Many (1:N) (A Librarian can manage multiple Books, but a Book is managed by one Librarian).
        

**Explanation:**

- **BOOK** and **BORROWER** are two main entities.
    
- A **BORROWER** can BORROW many **BOOKS**, and a **BOOK** can be BORROWED by many **BORROWER**s over time (many-to-many relationship). The BORROWS relationship might have attributes like BorrowDate, DueDate, and ReturnDate.
    
- A **LIBRARIAN** MANAGES **BOOKS**. This is typically a one-to-many relationship where one LIBRARIAN can MANAGE multiple BOOK entities.
    

**2. What are Codd's rules? Write any five rules in detail.**

**Codd's rules** are a set of 12 (plus Rule 0) guidelines proposed by Dr. Edgar F. Codd, the inventor of the relational model, to define what qualities a database management system (DBMS) must possess to be considered a true Relational Database Management System (RDBMS). These rules ensure that a system fully adheres to the principles of the relational model, promoting data integrity, consistency, and independence.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEv20wIG9qbvn9JzoYjgnCGHx8QHBW5eX_UnDaObTSFceRMofcIJJgSOXtw6yfK1cNV9VEmW1VGQJACuotdSX45w11NKHurnvQywyvpA2BbbQqxTnGFgEKZeioY8tP4z7pXP6wqKQQa-PFz3APu8ZGcC_cpMNqQoLMhhYy2RuEB)][[2](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGGC-FqI-tLouYXgw3T9SArIWMv7HkpLnoWRAwwp_zABB9tbdeJErocK25AZ73ksNFGdennUiGglLHY7Y6JIsEU-6dmRA6qQ2veBctG-db6k1rbD9z2LhlSVeVATGvxBGP2Na4Z3a6i9mWxZABeCj5uc2zBBg%3D%3D)][[3](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEzfhn6dmOOgTQyj6zoNa6nSn9rD4LAPJjDIdJVvYSeUd5CwWCvS-XCT2H-KyZG9NduASjtiz8kVOGoOuCGJ6biTyFotOfYfV-0vxBuvTZKppqUY6XZr-u7buyYLE_6IzKI-e33xBKn5Iie)]

Here are five of Codd's rules:

1. **Rule 0: The Foundation Rule**
    
    - **Detail:** For a system to be considered a relational database management system, it must be able to manage databases entirely through its relational capabilities.[[3](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEzfhn6dmOOgTQyj6zoNa6nSn9rD4LAPJjDIdJVvYSeUd5CwWCvS-XCT2H-KyZG9NduASjtiz8kVOGoOuCGJ6biTyFotOfYfV-0vxBuvTZKppqUY6XZr-u7buyYLE_6IzKI-e33xBKn5Iie)][[4](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyJbPENITuyeBo8EWkjvEDDkKKpaPQeleJHIpvpl-zQti94orrwalcMc1n0g9IVtNEdn0v7Ylz9WYBhyEb_PBsGthR1xqn8c2nsUuFFpVzOAjAl1VRkDC7VdT84zOaH5VHvB7z_HXIhafdHHY%3D)] This means all data operations, including storage, retrieval, and manipulation, must be performed using relational operations (e.g., SQL statements).
        
2. **Rule 1: The Information Rule**
    
    - **Detail:** All information in a relational database, including table names, column names, and data itself, must be represented explicitly as values in tables.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEv20wIG9qbvn9JzoYjgnCGHx8QHBW5eX_UnDaObTSFceRMofcIJJgSOXtw6yfK1cNV9VEmW1VGQJACuotdSX45w11NKHurnvQywyvpA2BbbQqxTnGFgEKZeioY8tP4z7pXP6wqKQQa-PFz3APu8ZGcC_cpMNqQoLMhhYy2RuEB)][[3](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEzfhn6dmOOgTQyj6zoNa6nSn9rD4LAPJjDIdJVvYSeUd5CwWCvS-XCT2H-KyZG9NduASjtiz8kVOGoOuCGJ6biTyFotOfYfV-0vxBuvTZKppqUY6XZr-u7buyYLE_6IzKI-e33xBKn5Iie)][[4](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyJbPENITuyeBo8EWkjvEDDkKKpaPQeleJHIpvpl-zQti94orrwalcMc1n0g9IVtNEdn0v7Ylz9WYBhyEb_PBsGthR1xqn8c2nsUuFFpVzOAjAl1VRkDC7VdT84zOaH5VHvB7z_HXIhafdHHY%3D)][[5](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQED_aENONQxfwmeKGEczoFg9EAaufbpVGMkAtZBk_v1QeP3vecgQ_u63HqX-4pF6wLKsLAcxwi8NWe3kb6TLp0VdxnRTSN7hVFIcO9hBoENGrcr3Z_27ckNEHmV76cv88vyLPE9E7WLVbv8N62Otfqb_nG10iL8hDuC-RTcb1TsjBCyYq3Djg%3D%3D)] There should be no hidden information; everything should be stored as data in tables (rows and columns).
        
3. **Rule 2: Guaranteed Access Rule**
    
    - **Detail:** Every single piece of data (every atomic value) in a relational database must be logically accessible by using a combination of the table name, its primary key value (row identifier), and its column name.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEv20wIG9qbvn9JzoYjgnCGHx8QHBW5eX_UnDaObTSFceRMofcIJJgSOXtw6yfK1cNV9VEmW1VGQJACuotdSX45w11NKHurnvQywyvpA2BbbQqxTnGFgEKZeioY8tP4z7pXP6wqKQQa-PFz3APu8ZGcC_cpMNqQoLMhhYy2RuEB)][[4](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyJbPENITuyeBo8EWkjvEDDkKKpaPQeleJHIpvpl-zQti94orrwalcMc1n0g9IVtNEdn0v7Ylz9WYBhyEb_PBsGthR1xqn8c2nsUuFFpVzOAjAl1VRkDC7VdT84zOaH5VHvB7z_HXIhafdHHY%3D)][[5](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQED_aENONQxfwmeKGEczoFg9EAaufbpVGMkAtZBk_v1QeP3vecgQ_u63HqX-4pF6wLKsLAcxwi8NWe3kb6TLp0VdxnRTSN7hVFIcO9hBoENGrcr3Z_27ckNEHmV76cv88vyLPE9E7WLVbv8N62Otfqb_nG10iL8hDuC-RTcb1TsjBCyYq3Djg%3D%3D)] This ensures that data can be precisely located and retrieved.
        
4. **Rule 3: Systematic Treatment of Null Values**
    
    - **Detail:** The RDBMS must systematically support the representation and handling of "null values" for missing or inapplicable information.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEv20wIG9qbvn9JzoYjgnCGHx8QHBW5eX_UnDaObTSFceRMofcIJJgSOXtw6yfK1cNV9VEmW1VGQJACuotdSX45w11NKHurnvQywyvpA2BbbQqxTnGFgEKZeioY8tP4z7pXP6wqKQQa-PFz3APu8ZGcC_cpMNqQoLMhhYy2RuEB)][[2](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGGC-FqI-tLouYXgw3T9SArIWMv7HkpLnoWRAwwp_zABB9tbdeJErocK25AZ73ksNFGdennUiGglLHY7Y6JIsEU-6dmRA6qQ2veBctG-db6k1rbD9z2LhlSVeVATGvxBGP2Na4Z3a6i9mWxZABeCj5uc2zBBg%3D%3D)][[3](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEzfhn6dmOOgTQyj6zoNa6nSn9rD4LAPJjDIdJVvYSeUd5CwWCvS-XCT2H-KyZG9NduASjtiz8kVOGoOuCGJ6biTyFotOfYfV-0vxBuvTZKppqUY6XZr-u7buyYLE_6IzKI-e33xBKn5Iie)][[4](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyJbPENITuyeBo8EWkjvEDDkKKpaPQeleJHIpvpl-zQti94orrwalcMc1n0g9IVtNEdn0v7Ylz9WYBhyEb_PBsGthR1xqn8c2nsUuFFpVzOAjAl1VRkDC7VdT84zOaH5VHvB7z_HXIhafdHHY%3D)][[5](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQED_aENONQxfwmeKGEczoFg9EAaufbpVGMkAtZBk_v1QeP3vecgQ_u63HqX-4pF6wLKsLAcxwi8NWe3kb6TLp0VdxnRTSN7hVFIcO9hBoENGrcr3Z_27ckNEHmV76cv88vyLPE9E7WLVbv8N62Otfqb_nG10iL8hDuC-RTcb1TsjBCyYq3Djg%3D%3D)] These nulls must be distinct from empty strings, blanks, or zeros, and their treatment must be consistent across the database.
        
5. **Rule 5: The Comprehensive Data Sublanguage Rule**
    
    - **Detail:** The system must support at least one relational language that can be used both interactively and within application programs, and that supports data definition (DDL), data manipulation (DML), security and integrity constraints, and transaction management operations.[[1](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEv20wIG9qbvn9JzoYjgnCGHx8QHBW5eX_UnDaObTSFceRMofcIJJgSOXtw6yfK1cNV9VEmW1VGQJACuotdSX45w11NKHurnvQywyvpA2BbbQqxTnGFgEKZeioY8tP4z7pXP6wqKQQa-PFz3APu8ZGcC_cpMNqQoLMhhYy2RuEB)][[3](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEzfhn6dmOOgTQyj6zoNa6nSn9rD4LAPJjDIdJVvYSeUd5CwWCvS-XCT2H-KyZG9NduASjtiz8kVOGoOuCGJ6biTyFotOfYfV-0vxBuvTZKppqUY6XZr-u7buyYLE_6IzKI-e33xBKn5Iie)][[4](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyJbPENITuyeBo8EWkjvEDDkKKpaPQeleJHIpvpl-zQti94orrwalcMc1n0g9IVtNEdn0v7Ylz9WYBhyEb_PBsGthR1xqn8c2nsUuFFpVzOAjAl1VRkDC7VdT84zOaH5VHvB7z_HXIhafdHHY%3D)][[5](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQED_aENONQxfwmeKGEczoFg9EAaufbpVGMkAtZBk_v1QeP3vecgQ_u63HqX-4pF6wLKsLAcxwi8NWe3kb6TLp0VdxnRTSN7hVFIcO9hBoENGrcr3Z_27ckNEHmV76cv88vyLPE9E7WLVbv8N62Otfqb_nG10iL8hDuC-RTcb1TsjBCyYq3Djg%3D%3D)] SQL is a prime example of such a language.
        

**3. Explain the concept of Keys in the relational database model with examples.**

In the relational database model, **keys** are attributes or sets of attributes that uniquely identify tuples (rows) within a relation (table) and establish relationships between different relations. They are fundamental for maintaining data integrity and enabling efficient data retrieval.

- **1. Super Key:**
    
    - A set of one or more attributes that, taken collectively, can uniquely identify a tuple in a relation.
        
    - **Example:** In a STUDENT table (StudentID, Name, Email, Age), (StudentID, Name, Email) is a super key. (StudentID, Name) is also a super key. (StudentID) alone is also a super key.
        
- **2. Candidate Key:**
    
    - A minimal super key; it means it's a super key from which no attribute can be removed without losing the uniqueness property.
        
    - A relation may have multiple candidate keys.
        
    - **Example:** In STUDENT (StudentID, Name, Email, Age), if both StudentID and Email can uniquely identify a student, then (StudentID) and (Email) are both candidate keys.
        
- **3. Primary Key (PK):**
    
    - One of the candidate keys chosen by the database designer to uniquely identify each tuple in a relation. It cannot contain NULL values.
        
    - **Example:** From the STUDENT table, if (StudentID) is chosen as the primary key, it will uniquely identify each student record.
        
- **4. Alternate Key:**
    
    - Candidate keys that are not chosen as the primary key.
        
    - **Example:** If StudentID is the primary key in STUDENT, then Email (if it's also a candidate key) would be an alternate key.
        
- **5. Foreign Key (FK):**
    
    - An attribute or set of attributes in one relation (the referencing or child table) that refers to the primary key of another relation (the referenced or parent table). It establishes a link between tables, enforcing referential integrity.
        
    - **Example:** In a COURSE table (CourseID, Title, Credits) and an ENROLLMENT table (EnrollmentID, StudentID, CourseID, Grade), CourseID in ENROLLMENT is a foreign key referencing CourseID (PK) in the COURSE table. StudentID in ENROLLMENT would be a foreign key referencing StudentID (PK) in the STUDENT table.
        

**4. Define Normalization. Explain 1NF, 2NF, 3NF and BCNF with examples.**

**Normalization** is a systematic process in database design used to reduce data redundancy, eliminate undesirable characteristics like insertion, update, and deletion anomalies, and ensure data integrity.[[6](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQE-3fjD2lFU2kv-5IqqA0bZWm8nIg6f5f0rDgVqasclpU1bzh_bneKK1rZPhUKDw0P77euLmF5HLsVT7El2sRtUO8AGn9bKl8jizqL9JpSkgZEDZSNUm-57FXp26qsy2O7wLX1qTZtgqIm8XXLq7bFBGJOHojssoc7G9lrvkSRvHrP_f-Z520k8fMaFGZU9Z95og89U5SV620GXcuBQdCqw41eEyH8W6Dkf0nHfnDQaqA%3D%3D)][[7](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGRp3bFRHzBke5N4yQEzYN886TItTysnqL8d2IwHoQtYLxvJNcY5Z9vc-lMHoLUFX8nN06-1MZ5tGOGTRNSKFvUliGTekQKujtBkmA84y4G7kGraCrHTElUIoQOd-lkG1Vrr2e_e9yMJT9PBA9A22OiQu8qDYz2MQ%3D%3D)][[8](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEjaa3DHeTOBiS6-Kvt2BqqnxjciigoRjdj2ZiKUOBH3HgHHQbexFLW_X8UX4vaWM1yXmVDK-cQQThGoiVk60-J6_l6-m56Tin5UxBGlDW2h9TqwYNQGyfmR0ojnPLriuO574O4hBAe)] It achieves this by organizing fields and tables in a relational database according to a series of "normal forms."[[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)]

**Normal Forms:**

1. **First Normal Form (1NF):**
    
    - **Definition:** A relation is in 1NF if all attributes contain only atomic (indivisible) values, and there are no repeating groups or multi-valued attributes.[[6](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQE-3fjD2lFU2kv-5IqqA0bZWm8nIg6f5f0rDgVqasclpU1bzh_bneKK1rZPhUKDw0P77euLmF5HLsVT7El2sRtUO8AGn9bKl8jizqL9JpSkgZEDZSNUm-57FXp26qsy2O7wLX1qTZtgqIm8XXLq7bFBGJOHojssoc7G9lrvkSRvHrP_f-Z520k8fMaFGZU9Z95og89U5SV620GXcuBQdCqw41eEyH8W6Dkf0nHfnDQaqA%3D%3D)][[7](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGRp3bFRHzBke5N4yQEzYN886TItTysnqL8d2IwHoQtYLxvJNcY5Z9vc-lMHoLUFX8nN06-1MZ5tGOGTRNSKFvUliGTekQKujtBkmA84y4G7kGraCrHTElUIoQOd-lkG1Vrr2e_e9yMJT9PBA9A22OiQu8qDYz2MQ%3D%3D)][[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)] Each column must have a unique name, and the order of data storage doesn't matter.[[6](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQE-3fjD2lFU2kv-5IqqA0bZWm8nIg6f5f0rDgVqasclpU1bzh_bneKK1rZPhUKDw0P77euLmF5HLsVT7El2sRtUO8AGn9bKl8jizqL9JpSkgZEDZSNUm-57FXp26qsy2O7wLX1qTZtgqIm8XXLq7bFBGJOHojssoc7G9lrvkSRvHrP_f-Z520k8fMaFGZU9Z95og89U5SV620GXcuBQdCqw41eEyH8W6Dkf0nHfnDQaqA%3D%3D)]
        
    - **Example (Not in 1NF):**
        
        codeCode
        
        ```
        StudentCourse (StudentID, StudentName, CoursesEnrolled)
        -------------------------------------------------
        101        Alice        "Math, Physics"
        102        Bob          "Chemistry"
        ```
        
        CoursesEnrolled is multi-valued.
        
    - **Example (In 1NF):**
        
        codeCode
        
        ```
        StudentCourse (StudentID, StudentName, Course)
        ------------------------------------------
        101        Alice        Math
        101        Alice        Physics
        102        Bob          Chemistry
        ```
        
2. **Second Normal Form (2NF):**
    
    - **Definition:** A relation is in 2NF if it is in 1NF and all non-key attributes are fully functionally dependent on the entire primary key.[[6](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQE-3fjD2lFU2kv-5IqqA0bZWm8nIg6f5f0rDgVqasclpU1bzh_bneKK1rZPhUKDw0P77euLmF5HLsVT7El2sRtUO8AGn9bKl8jizqL9JpSkgZEDZSNUm-57FXp26qsy2O7wLX1qTZtgqIm8XXLq7bFBGJOHojssoc7G9lrvkSRvHrP_f-Z520k8fMaFGZU9Z95og89U5SV620GXcuBQdCqw41eEyH8W6Dkf0nHfnDQaqA%3D%3D)][[7](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGRp3bFRHzBke5N4yQEzYN886TItTysnqL8d2IwHoQtYLxvJNcY5Z9vc-lMHoLUFX8nN06-1MZ5tGOGTRNSKFvUliGTekQKujtBkmA84y4G7kGraCrHTElUIoQOd-lkG1Vrr2e_e9yMJT9PBA9A22OiQu8qDYz2MQ%3D%3D)][[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)] This eliminates partial dependencies where a non-key attribute depends only on a part of a composite primary key.
        
    - **Example (Not in 2NF):**
        
        codeCode
        
        ```
        OrderDetails (OrderID, ProductID, ProductName, Quantity)
        ----------------------------------------------------
        PK: (OrderID, ProductID)
        1          P1           Laptop       2
        1          P2           Mouse        1
        2          P1           Laptop       3
        ```
        
        Here, ProductName depends only on ProductID (part of the composite key), not OrderID.
        
    - **Example (In 2NF):**
        
        codeCode
        
        ```
        Order (OrderID, Quantity)
        ---------------------
        1          2
        1          1
        2          3
        
        Product (ProductID, ProductName)
        ----------------------------
        P1          Laptop
        P2          Mouse
        ```
        
3. **Third Normal Form (3NF):**
    
    - **Definition:** A relation is in 3NF if it is in 2NF and there are no transitive dependencies.[[7](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGRp3bFRHzBke5N4yQEzYN886TItTysnqL8d2IwHoQtYLxvJNcY5Z9vc-lMHoLUFX8nN06-1MZ5tGOGTRNSKFvUliGTekQKujtBkmA84y4G7kGraCrHTElUIoQOd-lkG1Vrr2e_e9yMJT9PBA9A22OiQu8qDYz2MQ%3D%3D)][[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)] A transitive dependency occurs when a non-key attribute depends on another non-key attribute, which in turn depends on the primary key.[[6](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQE-3fjD2lFU2kv-5IqqA0bZWm8nIg6f5f0rDgVqasclpU1bzh_bneKK1rZPhUKDw0P77euLmF5HLsVT7El2sRtUO8AGn9bKl8jizqL9JpSkgZEDZSNUm-57FXp26qsy2O7wLX1qTZtgqIm8XXLq7bFBGJOHojssoc7G9lrvkSRvHrP_f-Z520k8fMaFGZU9Z95og89U5SV620GXcuBQdCqw41eEyH8W6Dkf0nHfnDQaqA%3D%3D)][[8](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEjaa3DHeTOBiS6-Kvt2BqqnxjciigoRjdj2ZiKUOBH3HgHHQbexFLW_X8UX4vaWM1yXmVDK-cQQThGoiVk60-J6_l6-m56Tin5UxBGlDW2h9TqwYNQGyfmR0ojnPLriuO574O4hBAe)]
        
    - **Example (Not in 3NF):**
        
        codeCode
        
        ```
        StudentDetails (StudentID, StudentName, DeptID, DeptName)
        -----------------------------------------------------
        PK: StudentID
        101        Alice        D1      Computer Science
        102        Bob          D2      Electrical Engineering
        ```
        
        Here, DeptName depends on DeptID, and DeptID depends on StudentID. DeptName transitively depends on StudentID.
        
    - **Example (In 3NF):**
        
        codeCode
        
        ```
        Student (StudentID, StudentName, DeptID)
        -----------------------------------
        101        Alice        D1
        102        Bob          D2
        
        Department (DeptID, DeptName)
        ---------------------------
        D1         Computer Science
        D2         Electrical Engineering
        ```
        
4. **Boyce-Codd Normal Form (BCNF):**
    
    - **Definition:** A relation is in BCNF if it is in 3NF and for every non-trivial functional dependency (X → Y), X must be a superkey.[[7](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGRp3bFRHzBke5N4yQEzYN886TItTysnqL8d2IwHoQtYLxvJNcY5Z9vc-lMHoLUFX8nN06-1MZ5tGOGTRNSKFvUliGTekQKujtBkmA84y4G7kGraCrHTElUIoQOd-lkG1Vrr2e_e9yMJT9PBA9A22OiQu8qDYz2MQ%3D%3D)][[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)] This is a stricter form of 3NF, addressing anomalies that 3NF might miss, particularly when a table has multiple overlapping candidate keys.[[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)] In simpler terms, every determinant must be a candidate key.[[9](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)]
        
    - **Example (Not in BCNF, but in 3NF):**  
        Consider a table StudentCourseTeacher (StudentID, Course, Teacher).
        
        - Assume: A student can take a course with only one teacher. A teacher can teach multiple courses. A course can be taught by multiple teachers (e.g., different sections).
            
        - Dependencies:
            
            - (StudentID, Course) → Teacher (Primary Key)
                
            - Teacher → Course (If a teacher teaches only one course, this would imply BCNF violation)
                
        - If Teacher uniquely determines Course, but Teacher is not a superkey, it violates BCNF.
            
    - **Example (In BCNF):** Decompose StudentCourseTeacher into:
        
        codeCode
        
        ```
        StudentEnrollment (StudentID, Course)
        ----------------------------------
        
        CourseAssignment (Teacher, Course)
        -------------------------------
        ```
        

**5. Give an example of a relational schema.**

A **relational schema** is a blueprint or a logical design of a relational database. It defines the structure of each table (relation), including the relation name, the names of its attributes (columns), and their associated data types and constraints.[[10](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGPAaTAttr-guDjWyfymcELYN6QFEYrBVQdFuIP-hSlwHmwkz0UqXEG-B30e5SF-Dgf5ik_ZArk6LxY9tq0L2XXnQMupIHUDIDpoAMk8Ys1OpOS8D_pOhcrG1Ws02alyxqkiTn_DKhEUN95wnTcR699HKfS57Oew32p2ORgIDlQL9Gwdw%3D%3D)][[11](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEumRXaw3xrsTftKkVyp1yALRHoyuFrdpLyJW_lxy7ctGunj9oGwZYb0FPAOsYYa5ic680KlmHDh3UhoAhpGr-2fM094PTnXEYXBgVOpMXhpfCYBssRu9-9hSrlwsz1VqwmQmBdk4gKbZF4BeMbqmPn7bZlcSw0)] It essentially describes how the data is organized.[[10](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGPAaTAttr-guDjWyfymcELYN6QFEYrBVQdFuIP-hSlwHmwkz0UqXEG-B30e5SF-Dgf5ik_ZArk6LxY9tq0L2XXnQMupIHUDIDpoAMk8Ys1OpOS8D_pOhcrG1Ws02alyxqkiTn_DKhEUN95wnTcR699HKfS57Oew32p2ORgIDlQL9Gwdw%3D%3D)]

**Example: A Company Database Relational Schema**

This schema defines several tables (relations) for managing employee, department, and project information within a company.[[10](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGPAaTAttr-guDjWyfymcELYN6QFEYrBVQdFuIP-hSlwHmwkz0UqXEG-B30e5SF-Dgf5ik_ZArk6LxY9tq0L2XXnQMupIHUDIDpoAMk8Ys1OpOS8D_pOhcrG1Ws02alyxqkiTn_DKhEUN95wnTcR699HKfS57Oew32p2ORgIDlQL9Gwdw%3D%3D)][[12](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQF6oyxaEYVzPZaYXTWR1xsWSVMXpgefy8ZzkLxcA1DLbW5DZT8hHQSZwl-vbQ-Vjp8EZdpN7sVW5yvHATq1h9glUAHLHZjmS9SpgYRnvFXwykyA8h0E5Z3ToZDIWVGEfipZo-SuIc862s_DGt-DdnBJRyw%3D)]

- **EMPLOYEE** (<u>Ssn</u>, Fname, Minit, Lname, Bdate, Address, Sex, Salary, Super_ssn, Dno)
    
    - **Attributes:**
        
        - Ssn: Employee Social Security Number (Primary Key)
            
        - Fname: First Name
            
        - Minit: Middle Initial
            
        - Lname: Last Name
            
        - Bdate: Birth Date
            
        - Address: Employee Address
            
        - Sex: Gender
            
        - Salary: Employee Salary
            
        - Super_ssn: Supervisor's Ssn (Foreign Key referencing EMPLOYEE.Ssn)
            
        - Dno: Department Number (Foreign Key referencing DEPARTMENT.Dnumber)
            
- **DEPARTMENT** (<u>Dnumber</u>, Dname, Mgr_ssn, Mgr_start_date)
    
    - **Attributes:**
        
        - Dnumber: Department Number (Primary Key)
            
        - Dname: Department Name
            
        - Mgr_ssn: Manager's Ssn (Foreign Key referencing EMPLOYEE.Ssn)
            
        - Mgr_start_date: Date Manager started in role
            
- **PROJECT** (<u>Pnumber</u>, Pname, Plocation, Dnum)
    
    - **Attributes:**
        
        - Pnumber: Project Number (Primary Key)
            
        - Pname: Project Name
            
        - Plocation: Project Location
            
        - Dnum: Department Number (Foreign Key referencing DEPARTMENT.Dnumber)
            
- **WORKS_ON** (<u>Essn</u>, <u>Pno</u>, Hours)
    
    - **Attributes:**
        
        - Essn: Employee Ssn (Foreign Key referencing EMPLOYEE.Ssn)
            
        - Pno: Project Number (Foreign Key referencing PROJECT.Pnumber)
            
        - Hours: Hours worked on the project
            
        - **(Essn, Pno)**: Composite Primary Key
            
- **DEPENDENT** (<u>Essn</u>, <u>Dependent_name</u>, Sex, Bdate, Relationship)
    
    - **Attributes:**
        
        - Essn: Employee Ssn (Foreign Key referencing EMPLOYEE.Ssn)
            
        - Dependent_name: Name of the dependent
            
        - Sex: Gender of dependent
            
        - Bdate: Birth date of dependent
            
        - Relationship: Relationship to employee
            
        - **(Essn, Dependent_name)**: Composite Primary Key
            

**Explanation of Notation:**

- Underlined attributes (e.g., Ssn) indicate the **Primary Key**.
    
- Attributes followed by (FK referencing Table.Column) indicate a **Foreign Key**.
    

**6. Define Constraints. Explain types of Constraints in DBMS.**

**Constraints** in a Database Management System (DBMS) are rules enforced on data columns of a table.[[13](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEnM01zI3A5Wtx4S4jLFXmbD_RbibowSvKOCo7NL_mFi2mQUJGSjb41msSampbbd2Zjf9jHMR4a4_7QsENqVKijd-CajQ-kG_CwdCxlGng4BaEjPxFS9WdPuH43d5xECa59YIyJD1wZrDkVT2I%3D)] Their purpose is to ensure the accuracy, consistency, integrity, and reliability of the data stored in a database.[[13](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEnM01zI3A5Wtx4S4jLFXmbD_RbibowSvKOCo7NL_mFi2mQUJGSjb41msSampbbd2Zjf9jHMR4a4_7QsENqVKijd-CajQ-kG_CwdCxlGng4BaEjPxFS9WdPuH43d5xECa59YIyJD1wZrDkVT2I%3D)][[14](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQG31-VxPbNrx-EFCJSMgxBjAdgLes1S9p1c9sliohrU2bDLDT8EFwcX13vf7ccf9r-h0tsj0wZDKQm6pwahSNsikRlrJbs0AKhCGTyh3Dr6FHiiQOqcyvULhI3oqmPajLDwnqvjcuCXODbhP9kKQiKSK4N2mw%3D%3D)] Constraints prevent invalid data entries and define relationships between tables.[[13](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEnM01zI3A5Wtx4S4jLFXmbD_RbibowSvKOCo7NL_mFi2mQUJGSjb41msSampbbd2Zjf9jHMR4a4_7QsENqVKijd-CajQ-kG_CwdCxlGng4BaEjPxFS9WdPuH43d5xECa59YIyJD1wZrDkVT2I%3D)]

**Types of Constraints in DBMS:**

1. **Domain Constraints:**
    
    - **Definition:** These define the valid set of values for an attribute (column).[[14](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQG31-VxPbNrx-EFCJSMgxBjAdgLes1S9p1c9sliohrU2bDLDT8EFwcX13vf7ccf9r-h0tsj0wZDKQm6pwahSNsikRlrJbs0AKhCGTyh3Dr6FHiiQOqcyvULhI3oqmPajLDwnqvjcuCXODbhP9kKQiKSK4N2mw%3D%3D)] They restrict the type and range of data that can be stored in a column, ensuring data integrity and consistency.[[14](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQG31-VxPbNrx-EFCJSMgxBjAdgLes1S9p1c9sliohrU2bDLDT8EFwcX13vf7ccf9r-h0tsj0wZDKQm6pwahSNsikRlrJbs0AKhCGTyh3Dr6FHiiQOqcyvULhI3oqmPajLDwnqvjcuCXODbhP9kKQiKSK4N2mw%3D%3D)]
        
    - **Example:** An Age attribute must be an integer between 0 and 120. A Gender attribute can only accept 'M' or 'F'.
        
2. **Key Constraints:**
    
    - **Definition:** These constraints define attributes or sets of attributes that can uniquely identify each tuple (row) in a relation.[[13](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEnM01zI3A5Wtx4S4jLFXmbD_RbibowSvKOCo7NL_mFi2mQUJGSjb41msSampbbd2Zjf9jHMR4a4_7QsENqVKijd-CajQ-kG_CwdCxlGng4BaEjPxFS9WdPuH43d5xECa59YIyJD1wZrDkVT2I%3D)][[15](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHAmfDQv8_Eff-o7I2RjBH3_mKNH9sUni2R1v8UTTCm9t7oK5d3SzpylGlBoTojjp5BojMro4KEs-bTM5JpDvxT484Ji_ZxXt9w_xpHZ0xOPKFsldpYNziYjqk7mtYxVwP7NXxLJjF7xSpUCrXP)]
        
    - **Types:**
        
        - **Primary Key Constraint:** Uniquely identifies each record in a table. It must contain unique, non-null values.[[15](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHAmfDQv8_Eff-o7I2RjBH3_mKNH9sUni2R1v8UTTCm9t7oK5d3SzpylGlBoTojjp5BojMro4KEs-bTM5JpDvxT484Ji_ZxXt9w_xpHZ0xOPKFsldpYNziYjqk7mtYxVwP7NXxLJjF7xSpUCrXP)][[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)] (e.g., StudentID in a Student table).
            
        - **Unique Constraint:** Ensures that all values in a specified column or set of columns are unique, but unlike a primary key, it can allow one NULL value.[[15](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHAmfDQv8_Eff-o7I2RjBH3_mKNH9sUni2R1v8UTTCm9t7oK5d3SzpylGlBoTojjp5BojMro4KEs-bTM5JpDvxT484Ji_ZxXt9w_xpHZ0xOPKFsldpYNziYjqk7mtYxVwP7NXxLJjF7xSpUCrXP)][[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)] (e.g., Email address in a Student table).
            
3. **Entity Integrity Constraints:**
    
    - **Definition:** This rule states that the primary key of a relation cannot contain NULL values.[[15](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHAmfDQv8_Eff-o7I2RjBH3_mKNH9sUni2R1v8UTTCm9t7oK5d3SzpylGlBoTojjp5BojMro4KEs-bTM5JpDvxT484Ji_ZxXt9w_xpHZ0xOPKFsldpYNziYjqk7mtYxVwP7NXxLJjF7xSpUCrXP)][[17](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQFx2Al_7L_cNthTMLN2uCrM7HQG8liGnPWwUPxVTSc1LV0meOO2GkjnEON1Z8YQVSAdBL7XI4u9YGBNAFb0n4ICQKGrkT50u4mtRtHViflngWsF9zEkNL2p7DfW_ZPam-yBIG4afYF10iHAHgQ-jU3WosBNFuxKuKpbwh4qzdIII9eSGQ%3D%3D)] This ensures that every record in a table can be uniquely identified.
        
4. **Referential Integrity Constraints (Foreign Key Constraints):**
    
    - **Definition:** These constraints establish and maintain relationships between two tables.[[14](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQG31-VxPbNrx-EFCJSMgxBjAdgLes1S9p1c9sliohrU2bDLDT8EFwcX13vf7ccf9r-h0tsj0wZDKQm6pwahSNsikRlrJbs0AKhCGTyh3Dr6FHiiQOqcyvULhI3oqmPajLDwnqvjcuCXODbhP9kKQiKSK4N2mw%3D%3D)][[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)] A foreign key in one table (child table) must either match a primary key value in another table (parent table) or be NULL.[[15](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHAmfDQv8_Eff-o7I2RjBH3_mKNH9sUni2R1v8UTTCm9t7oK5d3SzpylGlBoTojjp5BojMro4KEs-bTM5JpDvxT484Ji_ZxXt9w_xpHZ0xOPKFsldpYNziYjqk7mtYxVwP7NXxLJjF7xSpUCrXP)][[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)]
        
    - **Example:** In an ENROLLMENT table, CourseID (Foreign Key) must correspond to an existing CourseID (Primary Key) in the COURSE table.
        
5. **NOT NULL Constraint:**
    
    - **Definition:** This constraint ensures that a column cannot contain any NULL values.[[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)][[17](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQFx2Al_7L_cNthTMLN2uCrM7HQG8liGnPWwUPxVTSc1LV0meOO2GkjnEON1Z8YQVSAdBL7XI4u9YGBNAFb0n4ICQKGrkT50u4mtRtHViflngWsF9zEkNL2p7DfW_ZPam-yBIG4afYF10iHAHgQ-jU3WosBNFuxKuKpbwh4qzdIII9eSGQ%3D%3D)] It ensures that a column always has a value and cannot be left empty.
        
    - **Example:** An EmployeeName column might be defined as NOT NULL.
        
6. **CHECK Constraint:**
    
    - **Definition:** This constraint specifies a condition that all values in a column must satisfy.[[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)] It defines a database rule that restricts the range of values allowed in one or more columns of every row.[[16](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)]
        
    - **Example:** A Salary column might have a CHECK constraint that ensures Salary > 0. A Grade column might have CHECK (Grade BETWEEN 'A' AND 'F').
        

---

Sourceshelp

1. [ohiocomputeracademy.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEv20wIG9qbvn9JzoYjgnCGHx8QHBW5eX_UnDaObTSFceRMofcIJJgSOXtw6yfK1cNV9VEmW1VGQJACuotdSX45w11NKHurnvQywyvpA2BbbQqxTnGFgEKZeioY8tP4z7pXP6wqKQQa-PFz3APu8ZGcC_cpMNqQoLMhhYy2RuEB)
2. [naukri.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGGC-FqI-tLouYXgw3T9SArIWMv7HkpLnoWRAwwp_zABB9tbdeJErocK25AZ73ksNFGdennUiGglLHY7Y6JIsEU-6dmRA6qQ2veBctG-db6k1rbD9z2LhlSVeVATGvxBGP2Na4Z3a6i9mWxZABeCj5uc2zBBg%3D%3D)
3. [studytonight.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEzfhn6dmOOgTQyj6zoNa6nSn9rD4LAPJjDIdJVvYSeUd5CwWCvS-XCT2H-KyZG9NduASjtiz8kVOGoOuCGJ6biTyFotOfYfV-0vxBuvTZKppqUY6XZr-u7buyYLE_6IzKI-e33xBKn5Iie)
4. [byjus.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEyJbPENITuyeBo8EWkjvEDDkKKpaPQeleJHIpvpl-zQti94orrwalcMc1n0g9IVtNEdn0v7Ylz9WYBhyEb_PBsGthR1xqn8c2nsUuFFpVzOAjAl1VRkDC7VdT84zOaH5VHvB7z_HXIhafdHHY%3D)
5. [oreilly.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQED_aENONQxfwmeKGEczoFg9EAaufbpVGMkAtZBk_v1QeP3vecgQ_u63HqX-4pF6wLKsLAcxwi8NWe3kb6TLp0VdxnRTSN7hVFIcO9hBoENGrcr3Z_27ckNEHmV76cv88vyLPE9E7WLVbv8N62Otfqb_nG10iL8hDuC-RTcb1TsjBCyYq3Djg%3D%3D)
6. [medium.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQE-3fjD2lFU2kv-5IqqA0bZWm8nIg6f5f0rDgVqasclpU1bzh_bneKK1rZPhUKDw0P77euLmF5HLsVT7El2sRtUO8AGn9bKl8jizqL9JpSkgZEDZSNUm-57FXp26qsy2O7wLX1qTZtgqIm8XXLq7bFBGJOHojssoc7G9lrvkSRvHrP_f-Z520k8fMaFGZU9Z95og89U5SV620GXcuBQdCqw41eEyH8W6Dkf0nHfnDQaqA%3D%3D)
7. [naukri.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGRp3bFRHzBke5N4yQEzYN886TItTysnqL8d2IwHoQtYLxvJNcY5Z9vc-lMHoLUFX8nN06-1MZ5tGOGTRNSKFvUliGTekQKujtBkmA84y4G7kGraCrHTElUIoQOd-lkG1Vrr2e_e9yMJT9PBA9A22OiQu8qDYz2MQ%3D%3D)
8. [popsql.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEjaa3DHeTOBiS6-Kvt2BqqnxjciigoRjdj2ZiKUOBH3HgHHQbexFLW_X8UX4vaWM1yXmVDK-cQQThGoiVk60-J6_l6-m56Tin5UxBGlDW2h9TqwYNQGyfmR0ojnPLriuO574O4hBAe)
9. [digitalocean.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHEo6c7QuLc9hojkIMOK4grHiTctwYAlrFIKMNS0xlgeb1aEkP18rQrMgvj7Vq5bALeoWEv5Dt5FhgIhTOAGs_QygjXwLwmWlWSFDA3-XFJsxoD7Z4WG-c23HpZYHjZEUzk-qDktT7WCF1AfKkRXLx6B6bmuvJ9acGOiVA9tgizVYOL)
10. [tutorialspoint.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQGPAaTAttr-guDjWyfymcELYN6QFEYrBVQdFuIP-hSlwHmwkz0UqXEG-B30e5SF-Dgf5ik_ZArk6LxY9tq0L2XXnQMupIHUDIDpoAMk8Ys1OpOS8D_pOhcrG1Ws02alyxqkiTn_DKhEUN95wnTcR699HKfS57Oew32p2ORgIDlQL9Gwdw%3D%3D)
11. [geeksforgeeks.org](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEumRXaw3xrsTftKkVyp1yALRHoyuFrdpLyJW_lxy7ctGunj9oGwZYb0FPAOsYYa5ic680KlmHDh3UhoAhpGr-2fM094PTnXEYXBgVOpMXhpfCYBssRu9-9hSrlwsz1VqwmQmBdk4gKbZF4BeMbqmPn7bZlcSw0)
12. [wright.edu](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQF6oyxaEYVzPZaYXTWR1xsWSVMXpgefy8ZzkLxcA1DLbW5DZT8hHQSZwl-vbQ-Vjp8EZdpN7sVW5yvHATq1h9glUAHLHZjmS9SpgYRnvFXwykyA8h0E5Z3ToZDIWVGEfipZo-SuIc862s_DGt-DdnBJRyw%3D)
13. [webandcrafts.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQEnM01zI3A5Wtx4S4jLFXmbD_RbibowSvKOCo7NL_mFi2mQUJGSjb41msSampbbd2Zjf9jHMR4a4_7QsENqVKijd-CajQ-kG_CwdCxlGng4BaEjPxFS9WdPuH43d5xECa59YIyJD1wZrDkVT2I%3D)
14. [prepbytes.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQG31-VxPbNrx-EFCJSMgxBjAdgLes1S9p1c9sliohrU2bDLDT8EFwcX13vf7ccf9r-h0tsj0wZDKQm6pwahSNsikRlrJbs0AKhCGTyh3Dr6FHiiQOqcyvULhI3oqmPajLDwnqvjcuCXODbhP9kKQiKSK4N2mw%3D%3D)
15. [tutorialspoint.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHAmfDQv8_Eff-o7I2RjBH3_mKNH9sUni2R1v8UTTCm9t7oK5d3SzpylGlBoTojjp5BojMro4KEs-bTM5JpDvxT484Ji_ZxXt9w_xpHZ0xOPKFsldpYNziYjqk7mtYxVwP7NXxLJjF7xSpUCrXP)
16. [ibm.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQHFlSKHJr8tA44xGviLIg9FHXu1QON81YlQNLpQopF4pU5KT2CjpWnggdF7hX5ElAJxXId5bGDn-rBD79d_Ia0lY0JCHBjtex3RSWObqv4uR5Rj0k0qJj12JbvTwrDZsZRjFWGjzWxwKz8sQyetj8ZHQQc%3D)
17. [medium.com](https://www.google.com/url?sa=E&q=https%3A%2F%2Fvertexaisearch.cloud.google.com%2Fgrounding-api-redirect%2FAUZIYQFx2Al_7L_cNthTMLN2uCrM7HQG8liGnPWwUPxVTSc1LV0meOO2GkjnEON1Z8YQVSAdBL7XI4u9YGBNAFb0n4ICQKGrkT50u4mtRtHViflngWsF9zEkNL2p7DfW_ZPam-yBIG4afYF10iHAHgQ-jU3WosBNFuxKuKpbwh4qzdIII9eSGQ%3D%3D)

##### Google Search Suggestions