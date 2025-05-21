    **Project Documentation: ITR Filing Website**

## **Overview**
This document outlines the structure and features of the ITR (Income Tax Return) filing website. The website will allow users to log in, upload necessary data, and file their ITR. Website will have 3 Types of user which are (Super Admin, Admin, Client)


## **Technology Stack**
- **Frontend:** React, TypeScript
- **Backend:** Node.js, Express.js
- **Database:** MongoDB 
- **State Management:** React Query / Redux Toolkit (if needed)
- **Authentication:** Firebase/Auth0/Custom JWT Auth/Twilio
- **Payment Integration:** Razorpay/Stripe
- **Animations:** Framer Motion
- **Theme:** Light & Dark Mode
- **ReactHookForm:** for All the forms
- **Yup:** Frontend Form Validation


## **Flow of the Website**

**User Side** 

1. User will land on your website i.e landing page
2. From landing page user will navigate to login Screen 
3. User will be loggedIn through Phone Number and OTP
4. After login user land on the Stepper Page
    - Stepper will have couple of Steps, without Filling these steps we will not allow user to move ahead

    - Step 1: Personal Details, user need to fill his personal Details like (Name, email, address PAN, Age)

    - Step 2: Will be an Questionaire i.e select your source Income, There will be 6 Question, with answer of yes or no. - With help of this, we will deciding the ITR Type

        - Q1) Income from Salary/Pension? - Yes/No
        - Q2) Income from House Property (Home Loan/ Rental Income, etc) - Yes/No
        - Q3) Income from Business/Profession ? - Yes/No
        - Q4) Income from Capital Gains (Shares/ Mutual Funds/Property etc) ? - Yes/No
        - Q5) Income from Other Sources ? - Yes/No
        - Q6) Income from Foreign Source ? - Yes/No


    - Step 3: After selecting the Source Income, next step is document upload, user will upload all the necessary documents, which are required for filling the ITR

    - Step 4: After uploding all the document, and based on source Income selection (STEP 2) amount will be displayed on the Payment Screen, and user need to pay the amount

    - Step 5: This will be an optional Step, where we will be taking the password of Income tax portal from the user

4. Once Amount is done, User Stepper will be completed and user will navigate to the Dashboard, Payment is also an Optional Step. User can complete the payment or opt for Pay Now

5. In the User Dashboard, user can see his/her data and can check the ITR Status whether it is Filled or Not Filled, and on the another side, there will be admin panel, where admin can see that a new ITR is Received and admin need to Fill the ITR based on the information user provided, Yes here on the admin Side, admin will manually file the user ITR and when ITR is Filled user will be notified

6. In the userDashboard we will also provide an tax calculator

**Admin Side**

1. There will be 2 types of admin - SuperAdmin, Admin 
2. Once admin is loggedIn, we will be navigated to the admin Dashboard
3. In the Dashboard we will be showing stats i.e Total ITR count, Pending ITR Count, Completed ITR Count

4. In the Admin panel we will have sidebar that will consists of
    - Dashboard
    - User Management
    - Payment Management

5. In the user Management, we will showing all the user that are registered on the website in a tabular format

6. Table will have mutipe CTA button like: Edit, Delete, View

7. When admin click on the user name, he will be navigate to user Details screen, where we will showing all the deatils of that user that we have taken, along with its documents, there will also an option to download all the documents

    8. There will be a another column in the table, which depicts the current user Journey i.e (abhi user Kha pe hai)
        - Wheter user has just registered - Step 1
        - User has given his/her personal Details - Step 2
        - User has Select his/her Source Income - Step 3
        - User has uploaded the document - Step 4
        - User has done the payment - Step 5       

9. There will be a another column in the table named as AssignedTO, superAdmin can assign that particular user/ITR to other admins...assignedTO will be an dropdown from where superAdmin can select other admin fellows or assign to himself

10. There will be mutiple Filters in the Table i.e
    - Search based on Phone Number, name and Email
    - Filter based on User Journey (currently where is the user)
    - Filter based on AssignedTo
        - AssignedTo will be 3-4 name i.e Rahul, Akshay, Ankush, Yash
        - this basically means that the reponsibility of Filling this ITR is with this person
    - Filter based on ITR Status
        - Filled, InProgress, Pending, blocked, pending on client
    - There will be an option to download the entire table as an excel or export to excel

11. When ITR will be Filled, then we need to send the notification/alert to the user on his email, Phone Number, and on the User Dashboard

10. There will be a Table of Payment Management, where admin can see all the status of the payments that are made by user in a tabular format

## **Pages & Features that need to build**

### **1. Landing Page**
### Landing Page will have following Section:
- **Navbar** (Home, Features, Pricing, Login, Signup, Theme Toggle)
- **Header** (Which Displays the information regarding ITR filling)
- **Hero Section** (Catchy CTA, Tax filing benefits)
- **Features** (ITR filing, Secure Storage, Payment Integration, etc.)
- **Why Choose Us** (Security, Fast Processing, Reliable)
- **Testimonials**
- **FAQ Section**
- **Footer** (Quick Links, Social Media, Contact Info)

### **2. Authentication Pages**
- **Login Page** (Login Through Phone Number and OTP Verification)
- **Signup Page** (User Registration Phone Number and OTP Verification and basic Details)
- **Forgot Password Page** (Password reset functionality)

### **3. User Dashboard**
- **User Dashboard** 
- **Profile Management** (Edit personal details, change password)
- **Upload Documents** (user can upload more documents, that are required for Tax Filling)
- **Payment Section** User can Check the payment status and payment Deatils and can also download the reciept

### **4. Admin Panel**
- **User Management** (View/Edit/Delete Users)
- **Payment Management** (Confirm payments, generate receipts)
- **Subadmin & Minor Admin Roles** (This will be a table, which will show all the admin)

### **5. Payment Page**
- **PreSelect ITR Plan based on Income Source** (Pricing options based on complexity)
- **Payment Gateway Integration** (Stripe/Razorpay)

### **6. ITR Filing Confirmation Page**
- **Acknowledgment of Submission** (User receives a confirmation)
- **Email & Notification System** (ITR filing updates sent to user)

### **7. Contact & Support Page**
- **Support Form** (Users can submit queries)
- **FAQ Section** (Common queries about ITR filing)

---

### Other Important Points 
- We will be selling this product as all the ITR will be filled by the CA-assisted filing, so every customer is premium for us

- UI should be Responsive

- User Documents such as PAN, documents, and financial details must be encrypted 
- Allow users to retry failed payments without restarting the process.
- Use WhatsApp/SMS for reminders (e.g., "Deadline: 3 days left!").
- I need to build all these Feature, Please help me in building this
 Everything should be Responsive and UI should be top notch. it should be neat and Clean

## Prices
- ITR 1 = 299 =>
     Income from Salary/Pension
     Income from House Property
     Income from Other Sources 

- ITR 2 = 1499
     Income from Salary/Pension
     Income from House Property
     Income from Other Sources
     Income from Capital Gains (Shares/ Mutual Funds/Property etc)
     Income from Foreign Source

- ITR 3 = 1999
     Income from Salary/Pension
     Income from House Property
     Income from Other Sources
     Income from Capital Gains (Shares/ Mutual Funds/Property etc)
     Income from Foreign Source
     Income from Business/Profession

- ITR 4 = 799
     Income from Salary/Pension
     Income from House Property
     Income from Other Sources
     Income from Business/Profession

