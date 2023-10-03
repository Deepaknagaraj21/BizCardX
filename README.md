# BizCardX
BizCardX: Extracting Business Card Data with OCR

Introduction to EasyOCR
EasyOCR is a Python package designed for computer vision developers, enabling seamless Optical Character Recognition (OCR). This Python library simplifies the process of extracting text from images and scanned documents. In this project, EasyOCR is utilized to extract text specifically from business cards.

EasyOCR stands out as the most straightforward choice for OCR due to the following reasons:

It can be effortlessly installed using a single pip command.
The package has minimal dependencies, streamlining the setup of your OCR development environment.
After installation, importing the package into your project requires just one import statement.
With only two lines of code, you can perform OCR: one to initialize the Reader class and another to perform OCR on the image using the readtext function.
Project Overview
BizCardX is a user-friendly tool designed to extract information from business cards. Leveraging OCR technology, this tool recognizes text on business cards and extracts the data into an SQL database, applying regular expressions for classification. Users can access the extracted information via a user-friendly graphical user interface (GUI) built using Streamlit.

The BizCardX application offers a simple and intuitive user interface, guiding users through the process of uploading a business card image and extracting its information. Extracted data is displayed in a clean and organized format, allowing users to easily add it to the database with a simple click. Additionally, users can efficiently read, update, and delete data stored in the database as needed.


Libraries and Modules Used
Pandas: Used to create a DataFrame with the scraped data.
mysql.connector: Facilitates storing and retrieving data from the SQL database.
Streamlit: Utilized to create the graphical user interface.
EasyOCR: Employs text extraction from images.
Workflow
To initiate data extraction with BizCardX, follow these steps:

Install the required libraries using the pip install command for Streamlit, mysql.connector, Pandas, and EasyOCR:

css
Copy code
pip install [Name of the library]
Execute the "BizCardX_main.py" using the streamlit run command:

arduino
Copy code
streamlit run BizCardX_main.py
A webpage will open in your browser, presenting three menu options: "HOME," "UPLOAD & EXTRACT," and "MODIFY." Users can upload a business card, extract, store, modify, or delete information as needed.

Once a business card is uploaded, EasyOCR is employed to extract text from it.

The extracted text is passed to the "get_data()" function (user-defined) for text classification, including company name, cardholder name, designation, mobile number, email address, website URL, area, city, state, and pin code, using loops and regular expressions.

The classified data is displayed on the screen and can be further edited by the user as necessary.

By clicking the "Upload to Database" button, the data is stored in the MySQL Database (Note: Provide respective host, user, password, and database name in create_database, sql_table_creation, and connect_database for establishing a connection).

With the "MODIFY" menu, users can access the uploaded data in the SQL Database for read, update, and delete operations.

By following these steps, BizCardX simplifies the process of extracting and managing business card data using EasyOCR and other libraries.
