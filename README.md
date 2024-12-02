# NanoJobs_Changes


## change 1:
Add a new link in the Home Navbar for the branches - the link name **Farnchise**. The **Farnchise** link will go to a new web page containing text and at the end of the page will be fields to fill and three check boxes:

 - field 1: Name
 - field 2: Vorname
 - field 3: User Email
 - field 4: Telefon
 - field 5: Ort
 - field 6: Beruf
 - field 7: Nachricht -> A text box to write the questions and notes
 - 3 check boxes
 - Senden button to send the data by Email

**Note: Check the PDF file below**

examples:
![change1](./Assets/change1.png)

[Franchise page PDF file]()

URL: http://client.nanojobs-gmbh.de/#/home-page 


 ----
 ## change 2:
Reorder the Home Navbar links after adding the **Franchise** link to be in this order: 
Home - Jobseekers - Company - Franchise - Blog - About Us - Contact Us

URL: http://client.nanojobs-gmbh.de/#/home-page 

----

## Change 3: 
Replace the column title in blue in the bottom navbar **Privacy** To -> **Nano Jobs** and move the **Privacy** To be as (a link) below the **Terms & Conditions and Impressum** links.

![change3](./Assets/change3_privecy.png)

URL: http://client.nanojobs-gmbh.de/#/home-page 

----

## change 3-2:
Replace the Text "Nano Jobs Personnel GmbH" in the lower navbar to -> "Nano Jobs Personal Dienstleistungen GmbH"

![change3-2](./Assets/change3-2.png)

## Change 4:
The **worker-data-info** page will be split into two sections:

 - The First section will be for the data the worker has already filled. (There are changes on the Mobile app which will be covered later in these docs.)

 - The Second section will have 9 fields that the Admin should fill.

![change4](./Assets/change4.jpeg)

***Note: Mobile app adds 8 fields, Admin fills 9 new fields.***

URL: http://admin.nanojobs-gmbh.de/#/dashboard/workers/details-worker/1/worker-data-info

---
## Change 5:

The **Exit Date** field In the **worker-data-info** page should accept both a date and an empty value to handle two cases (if there is an Exit Date or if it's empty with no date).

![change4_2](./Assets/Change4_2.png)

URL: http://admin.nanojobs-gmbh.de/#/dashboard/workers/details-worker/1/worker-data-info

 ---

## change 6:
In the **Mobile App** Add 8 fields in the **Account info** page and ***Note*** that the old 13 fields will stay as is after calling the info from the Registration process
The new Required fields are inside the PDF file below.
The ***Signature*** field should be the first and last name.

![Account_info_mobile](Assets/Account_info_mobile.jpg)

[Account info PDF]()

## change 7:

In the **Mobile App** the **Fill Data** pages (Questions & Fields) should fill a PDF file and give the Admin the abitlity to Print it from the **Fill data** section.

### example of Implementation Steps

#### Mobile App (Flutter):
- Capture data from the workers.
- Send the data to the server.

#### Server (Backend - .NET Core):
- Receive data from the mobile app.
- Use a PDF manipulation library (e.g., iTextSharp) to populate the PDF template.
- Store the completed PDF or make it available for download.

#### Admin Dashboard (Angular):
- Provide an interface to download, or print the completed PDF. Instead of Displaying the fields.

![Fill_data_Admin](./Assets/Fill_data_Admin.png)

URL: http://admin.nanojobs-gmbh.de/#/dashboard/workers/details-worker/1/worker-fill-data

**Note**: ***There is information (Yellow colored) in the PDF file below that has been entered previously, such as the first and last name and the job title...etc in case you can use it***

[Fill Data PDF]()

## Change 8: 

Do the same idea -> In the **Mobile App** the **Exam** pages/check boxes should fill the ***Exam PDF file*** and the Admin should be able to download it from **Exam** page.

### Key Points:

#### Preventing Edits:
- Once the worker submits the exam, lock the responses on the server-side to prevent any changes.
- Mark the exam as completed and disable further edits on the mobile app.

#### Generating PDF:
- Populate the PDF with the worker's responses using a server-side PDF generation library.
- Provide a **download or print** option for the admin in the **Exam page**.

URL: http://admin.nanojobs-gmbh.de/#/dashboard/workers/details-worker/1/worker-exam

**Note**: ***There is information (Notes Add on the PDF) in the PDF file below that has been entered previously, such as the first and last name and the job title...etc in case you can use it***

[Fragenborgen Alten- und Krankenpflege_Exam]()

## Change 9:

In the **Mobile App** The **Sign Contract** page inside the **User data**:

 - Remove Application Form field
 - Change the **Terms & Conditions** To be -> **Contract** 
 - and the text in that page will be changed later!


## Change 10: 

In the **Mobile App** in the -> **Upload Documents** Section

- Remove The additional texts and the Example Image for the ID Card as showen in the image below!
- If there is a front and back of the document, there must be two boxes to add both of them, as in the personal ID card. However, if the document only contains one front, one box only must be displayed to upload the document. 
- File upload should be optional so only available files are uploaded by the worker(Add a skip button please!)

![ID CARD](./Assets/IDCardUpdate.jpg)




## Change :

display a Personal number (ID) for each woker next to or below the Worker Name in the **Hour-recording** section

![change6](./Assets/Change6.png)

URL: http://admin.nanojobs-gmbh.de/#/dashboard/workers/details-worker/1/worker-hour-recording