### 📂 Project Overview: Superstore Management System

**Project Overview:**
This project focuses on a database management system for a superstore, designed to streamline product purchasing, billing, and transactions. The primary goal is to provide a secure and efficient way to store and manage sales data. The system allows both employees and owners to easily monitor and modify business transactions.

---

### 📝 Project Proposal Highlights

**Definition of a Superstore:**
A superstore is a large retail establishment that offers a wide variety of consumer goods across different product categories.

**Purpose of the Proposed System:**
The proposed management system aims to address the complexities of managing large quantities of goods, a significant number of importers, and numerous customers.

**Key Benefits:**

* **Improved Efficiency**: The system is designed to improve the overall work efficiency of the superstore.
* **Reduced Burden**: It helps reduce the administrative burden on managers by automating the transmission and control of goods.
* **Core Functionality**: The system provides essential functions for maintaining basic information about employees, customers, and products, enabling managers and employees to add, delete, and modify data.
* **Transaction Management**: It is specifically developed to computerize all store transactions. Details of products purchased from importers, including name, ID, phone number, and email, are recorded, and the quantity is updated in the stock. Similarly, customer purchases, including payment transactions, are also meticulously recorded.

---

### 📊 Database Design and Structure

The database schema is structured to manage the various entities and their relationships within the superstore.

#### 🧩 Key Tables & Entities:

* **`Admin`**: Manages administrator data, including `admin_id`, `user_name`, and `password`.
* **`Importer`**: Stores information about suppliers, identified by `Importer_id`, `i_Name`, `i_Address`, `i_PhoneNumber`, and `i_Email`, linked to an `Admin`.
* **`Employee`**: Contains employee details such as `Employee_id`, `EmployeeName`, `e_Address`, `e_PhoneNumber`, and `e_Email`, also linked to an `Admin`.
* **`Customer`**: Holds customer information, including `Customer_id`, `c_Name`, `c_Address`, `c_PhoneNumber`, and `c_Email`, linked to an `Admin`.
* **`Transaction`**: Records all transaction details, identified by `T_id`, and includes `Item-Code`, `Sales_Type`, `Item_name`, `Quantity`, `Time&Date`, and `Customer_id`.
* **`Item`**: Stores product details, with attributes like `Id`, `Item_name`, `Category-Id`, `Price`, `Brand`, `Size`, and `Quantity`.
* **`Category`**: Defines product categories with `Category_id` and `Category_name`.
* **`emp_cust`**: A link table that associates employees with customers via `Employee_id` and `Customer_id`.
* **`Item_Cate`**: A link table that connects items to categories using `Id` and `Category_id`.

---

### 🔍 Database Normalization

The database design has been normalized to the **3rd Normal Form (3NF)** to ensure data integrity and minimize redundancy.

* **1NF (First Normal Form)**: Multivalued attributes, such as `Phone Number`, were addressed.
* **2NF (Second Normal Form)**: The relations were broken down to eliminate partial dependencies on the primary key.
* **3NF (Third Normal Form)**: The final design ensures there are no transitive dependencies, meaning the relations are fully normalized and already in 3NF.

