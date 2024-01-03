# Ticket Descriptions

The following ticket descriptions are the culmination of our collaborative discussions with Hip Hop, Pizza, and Wangs, a beloved community restaurant. These tickets encapsulate the essential functionalities and requirements that the client envisions for their new Point of Sale (POS) system.

Each ticket is meticulously crafted to provide a lucid understanding of the desired features, painting a clear picture of the context, the expected behavior, and the end goal. While the tickets offer a roadmap, they also leave room for the engineering team's creativity and expertise in determining the best technical solutions.

As the project progresses, these tickets will be the beacon, ensuring that the development aligns with the client's vision. The product manager, in tandem with the engineering team, will prioritize, refine, and track the evolution of each ticket, ensuring a seamless journey from ideation to implementation.

Please read through these ticket descriptions to fully comprehend the client's intended scope and objectives for the project.

---

### **User Authentication**

- **Given**: A cashier accessing the POS system.
- **When**: They attempt to log in.
- **Then**: They should be authenticated using firebase.
  - When your user is **logged out**:
     - They should NOT see the navbar.
     - They should see either an h1 or the Logo on the page that says Hip Hop Pizza and Wings
     - A button to login
---

### **Home Screen Display**

- **Given**: An authenticated cashier on the POS system.
- **When**: The app first loads.
- **Then**: They should see a welcome screen with options to view orders, create an order, and view revenue.

---

### **View All Orders**

- **Given**: An authenticated cashier.
- **When**: They choose to view all orders.
- **Then**: They should see a list of all orders with relevant details.

---

### **Order Details and Associated Items**

- **Given**: An authenticated cashier.  
- **When**: They click on a specific order to view its details.  
- **Then**: 
    - They should see the following details from the selected order:
        - Order Name
        - Order Status (either "open" or "closed")
        - Customer Phone Number
        - Customer Email Address
        - Order Type (either "phone" or "in-person")
    - They should also see a list of all the order items associated with the selected order. Each item should display:
        - Order Item Name
        - Order Item Price

---

### **Delete Orders**

- **Given**: An authenticated cashier.  
- **When**: They decide to delete an order.  
- **Then**: The selected order should be removed from the system, and all associated order items should also be deleted.  

---

### **Delete Order Items**

- **Given**: An authenticated cashier.  
- **When**: They decide to delete a specific order item from an order.  
- **Then**: The selected order item should be removed from the system.  

---

### **Create New Orders**

- **Given**: An authenticated cashier.
- **When**: They want to add a new order.
- **Then**: They should be able to input the necessary details for the order and add it to the system. 

---

### **Add Order Items**

- **Given**: An authenticated cashier
- **When**: They want to add items to an existing order.
- **Then**: They should be able to input the necessary details for the order item and associate it with the selected order.  

---

### **Update Order Details**

- **Given**: An authenticated cashier
- **When**: They want to modify details of an existing order.  
- **Then**: 
    - They should be able to update the following information on the selected order:
        - Order Name
        - Customer Phone Number
        - Customer Email Address
        - Order Type

---

### **Update Order Items**

- **Given**: An authenticated cashier.  
- **When**: They want to modify details of an order item associated with an order.  
- **Then**: 
    - They should be able to update the following information on the selected order item:
        - Item Name
        - Item Price

---

### **Close Order with Restrictions**

- **Given**: An authenticated cashier.  
- **When**: They're reviewing an open order and decide to finalize it.
- **Then**: 
    - They should be able to click a button that takes them to a "Close Order" form.
    - In the form, they should input:
        - Payment Type (options: cash, check, debit, credit, or mobile-payment)
        - Tip Amount
    - Upon submission, the order's status should change from "Open" to "Closed".
    - They should **NOT** be able to close an order that has already been closed.

---

### **Revenue Node Addition**

- **Given**: An authenticated cashier
- **When**: They close an order.  
- **Then**: 
    - A new revenue node is created capturing:
        - Total Order Amount (including tip)
        - Date of the order closure
        - Payment Type
        - Tip Amount
        - Order Type
---

### **View Total Revenue**

- **Given**: An authenticated cashier.
- **When**: They want to view the total revenue.
- **Then**: They should see the sum of all revenue entries.
