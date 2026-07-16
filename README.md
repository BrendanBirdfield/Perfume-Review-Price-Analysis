# Perfume-Review-Price-Analysis

***Summary:***
Mens perfume price and review score analysis using Python, webscraping, statistics and seaborn visualisations. 
Goals were to find the best best reviewed perfumes for the lowest price and to explore correlation between price per ml and review score.
Data for reviews and prices were webscraped from a perfume review site and price checking website using the selenium library and then joined into a single csv file.
This data was processed in Python including regex expressions to split perfume names from amounts in ml. 
This was then used to create a new column showing the price per ml for every perfume.
Missing and duplicate values were removed or replaced with meaningful values and values were reformatted for consitency.
Tables were created showing the top ten cheapest perfumes with a review score above 8/10 and the top ten reviewed perfumes under £50.
A correlation and scatterplot was created to show the relationship between cost per ml and review score.

#
***Data Collection:***

Perfume Prices were webscraped from a list of mens perfumes from the price checker site: https://pricespy.co.uk/c/perfume?98221=31505

A for loop was used to search through all 110 pages of the review site.
Try except blocks were used to handle errors in the webscraping process.
Name and price were stored as lists and then used to create a dataframe. 

<img width="1090" height="680" alt="Image" src="https://github.com/user-attachments/assets/a6ef67bc-1360-493b-9e47-203b7e667096" />


A list of perfume names was then created from this dataframe.

This list was then iterated over to webscrape the review for each one from:  from https://www.parfumo.com/ 

A nested try except block was used to remove certain terms from the names when terms such as 'for men', 'for him' etc. caused errors in the search.
<img width="1088" height="661" alt="Image" src="https://github.com/user-attachments/assets/069cc92e-17d0-4e26-955e-619937877c05" />


#
***Data Cleaning/Processing:***

Values in the price dataframe that contained errors from the webscraping process were dropped:
<img width="1097" height="540" alt="Image" src="https://github.com/user-attachments/assets/1dd13029-7340-4f36-98a3-e5b6b02c064b" />

Values for price that were too long were removed
<img width="1095" height="47" alt="Image" src="https://github.com/user-attachments/assets/cabcb418-58e9-461a-8526-ceb69808be26" />

The pound sign in the price column was removed aswell as comma values in order to convert price into a float value.
<img width="1093" height="49" alt="Image" src="https://github.com/user-attachments/assets/6dbf9641-6e57-4896-84e9-73d7068d247d" />
<img width="1093" height="85" alt="Image" src="https://github.com/user-attachments/assets/4af34ee0-bdfb-4f07-9e97-95d154135da4" />

Duplicate values in the name column were dropped.
<img width="1095" height="318" alt="Image" src="https://github.com/user-attachments/assets/4c64def0-5c48-44db-8bf4-45da2dc7f788" />

Regex / regular expressions was used to seperate the amount eg. "100ml" from the name of the perfume.
<img width="1095" height="677" alt="Image" src="https://github.com/user-attachments/assets/36e31c2b-9961-4830-ab5d-1efd08d6432c" />

The review score column from the reviews webscraped dataframe was reduced to include just the number and then converted to an integer data type.
<img width="1090" height="89" alt="Image" src="https://github.com/user-attachments/assets/cf2e5d58-be51-45d9-957b-252a16830e9e" />

Checked for duplicate values and dropped them.
<img width="1093" height="122" alt="Image" src="https://github.com/user-attachments/assets/6d62839d-b938-4207-8611-196180a78a8d" />

In order to merge the review dataframe with the price dataframe the names of the perfumes needed to be reformatted in the price dataframe to remove strings like edt or edp so that the perfume names matched.
<img width="1098" height="61" alt="Image" src="https://github.com/user-attachments/assets/300037a8-4ced-4983-8851-e2e91cd36013" />

Merged the price and review dataframes on the name column.
<img width="1095" height="43" alt="Image" src="https://github.com/user-attachments/assets/d531f817-bff7-4020-92f7-b0f2a34a086e" />

Used the price and amount column to create a new 'cost per ml' column
<img width="1095" height="53" alt="Image" src="https://github.com/user-attachments/assets/f97d1767-0906-4163-84f0-8ccbf38643f9" />

As a final data check, histograms were created of each numerical column to check the distribution showing outliers for price
<img width="1089" height="506" alt="Image" src="https://github.com/user-attachments/assets/6051b924-2c07-41ce-928d-30d2022cfe5b" />

After checking the price of this specific perfume online. changed the price from £3500 to the correct £35
<img width="1104" height="434" alt="Image" src="https://github.com/user-attachments/assets/dcd087c3-7a1c-4b2f-bcb8-034ed90a3fd1" />

One last data check was performed to assess missing values and data types
<img width="1093" height="251" alt="Image" src="https://github.com/user-attachments/assets/b6766096-8153-4a20-a1ac-ff1ea8b68079" />

#
***Results / Final Output***

Finding the top 10 perfumes with reviews above 8/10 and then sorting for the lowest cost per ml:

<img width="1093" height="394" alt="Image" src="https://github.com/user-attachments/assets/e5471e70-deaa-4186-859e-09fc9d5373e2" />



Finding the top 10 perfumes sorted first by highest review and then by lowest cost per ml:

<img width="1090" height="391" alt="Image" src="https://github.com/user-attachments/assets/b5ba2bdc-4bdd-4e04-94b0-4f410a565271" />



What are the best reviewed mens perfumes for less than £50?

<img width="1097" height="390" alt="Image" src="https://github.com/user-attachments/assets/bd3719ae-e669-4e63-a14b-82c2b3dcf2c5" />



Next I looked at if there was a relationship between cost per ml and review score:

A very weak correlation of 0.08 was found showing that price is a bad estimate of review score.
This may have been partially moderated by reviewers taking into account price value when reviewing perfumes.
<img width="1202" height="167" alt="Image" src="https://github.com/user-attachments/assets/192051f1-83de-420c-bc10-6b563062e73d" />

<img width="1202" height="581" alt="Image" src="https://github.com/user-attachments/assets/8286d9d2-d085-460a-afd9-b42f31be7079" />
