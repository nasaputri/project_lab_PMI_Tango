# Project Lab BI for PMI Emergency Warehouse


# Background
* In this project, our team; Tango consist of Jeffri, Wira, and Natassa is making a BI model called WeCat.
* This dashboard expected to help PMI's Warehouse Manager to organized the warehouse in order to simplify tracking and monitoring process in the warehouse
* The dataset provided by Pacmann Team and PMI regarding PMI Emergency Warehouse data for COVID-19
* The problem itself triggered as we get through the data and find some of the goods are scattered in the several warehouse and some of the F&B items are mixed up with chemicals 
* Our team also done some wrangling the dataset in Python and done the EDA using Tableau which will be detailed below

# Objectives
The Objectives of this BI Model are:
* Enable user to reallocate misplaced item to the standard warehouse based on the suggestion
* Enable user to have a priority in organizing item placement across PMI Warehouse
* Facilitating PMI to maintain item grouping and Gudang Standard Mapping towards Item Group
* Enable user to give information about uncategorized item

# Methods
Below are the methods we use:

![Methods PLBI drawio](https://user-images.githubusercontent.com/95117954/151593551-d62b203b-982e-4535-bc0a-43c532eefe27.png)

# Wrangling Data
Data wrangling done using Python with steps as follows:

* After importing the data and libraries, we change numerical data that still read as string
* Replace NA value to 0 specifically for numerical data on Berat Masuk and Berat Keluar
* Pivoting the table of `Total Berat Masuk` and `Total Berat Keluar`
* Add Berat di Pindah column as a function of `Total Berat Masuk - Total Berat Keluar`
* Make items grouping based on its funtion (e.g Food, Beverages, Medical Equipment, Evacuation Equipment)
* Make warehouse categorization based on some sampling of the items already in the warehouse
* Categorized items that have no Item Grouping and Warehouse Categorization
* Make `Reallocation Suggestion` if items are not in the right warehouse
* Rename each column name
* Export to excel

# Exploratory Data Analysis
Simple Exploratory Data Analysis done using Tableau with steps as follows:
* Looking the items name in each warehouses
* Scrutinize each item grouping

# Dashboard
#### The Features and How to Use It
1.	The Stock Accuracy as the success metrics indicator &#8594; the monitoring indicator to know the items that already placed in the right warehouse
![image](https://user-images.githubusercontent.com/95117954/151598051-47497bd9-5794-4313-8744-82991f824085.png)


2.	Item Search and date filter &#8594; give user easiness to navigate through the data. User can directly search the Nama Barang, Group Barang, and Gudang Awal to make it easier to reallocate items in item search and move the date slider to search a certain date range.
![image](https://user-images.githubusercontent.com/95117954/151598081-123fc566-39c1-4e86-9642-b90528fe784b.png)

3.	Reallocation by Warehouse Matrix &#8594; gives user the sense of priority to the goods which needed to be reallocate based on weight balance (balance in – balance out). Ideally user should reallocate the top-10 items first before jumping on the next item.
![image](https://user-images.githubusercontent.com/95117954/151598105-0d85d1f0-dbdb-459f-abb0-bee738615b5a.png)
 
4.	Gudang Standard Mapping &#8594; gives a guideline for user to know the categorization of each warehouse. Can be customize according to PMI’s needs
![image](https://user-images.githubusercontent.com/95117954/151598133-dd1506fd-3137-4f58-b515-58fbc8ac1b62.png)

5.	Group Barang Item Monitor &#8594; gives a guideline of each Group Barang items. Easily filtered using dropdown filter
![image](https://user-images.githubusercontent.com/95117954/151598166-0807eb9d-2d08-4020-bfc9-6a0fbbbf37f9.png)

For the best experience: [Dashboard Link](https://public.tableau.com/app/profile/natassa.adi.putri/viz/WeCat/Wecat1_0?publish=yes)

# Analysis
* The features in this dashboard basically shows the reallocation based on the weight balance and expected to give the sense of priority to reallocate the items
* Based on our assessment, Good Storage Practice is quite important in medical warehouse and will simplify the turnover process which also save time
* Unfortunately we have no initial stock balance which can't be concluded if the warehouse is overcapacity or not.
* This dashboard also simplify the auditing process which quite important since the warehouse is all about donation goods

# Conclusion
This dashboard expected to help PMI warehouse manager to monitored stock accuracy. Other than monitoring, we also expect this dashboard can help PMI to organize their emergency warehouse and increased stock accuracy upto 90%. The success metrics itself depends on the timeframe implementation from PMI and we expect within the 6 months, PMI may achieve the stock accuracy until 90%


# Reference
* GOOD STORAGE AND DISTRIBUTION PRACTICES (May 2019) DRAFT FOR COMMENTS
* MANUAL LOGISTIK PMI

