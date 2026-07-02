# Perfume-Review-Price-Analysis
A project comparing mens perfume reviews and prices with the goal of being able to find the best reviewed perfumes for the lowest price.

Perfume Prices were webscraped from a list of mens perfumes from the price checker site: https://pricespy.co.uk/c/perfume?98221=31505
These were then saved to a dataframe for processing.
A list of perfume names was then created from this dataframe.
A list of reviews for each perfume was webscraped from https://www.parfumo.com/ 
Selenium was used to search for each perfume from the list of mens perfumes and append the reviews to a list and added to a dataframe.
The dataframes for prices and reviews were then joined on perfume name. The price per ml was calculated by dividing the price by the ml size of each perfume.

Finding the top 10 perfumes with reviews above 8/10 and then sorting for the lowest cost per ml:

<img width="1204" height="397" alt="Image" src="https://github.com/user-attachments/assets/7f2327b1-a6df-435f-adaf-8b008be1b7ab" />



Finding the top 10 perfumes sorted first by highest review and then by lowest cost per ml:

<img width="1196" height="401" alt="Image" src="https://github.com/user-attachments/assets/0c92f5bb-7b75-491e-a955-50b7a9f3a61f" />



What are the best reviewed mens perfumes for less than £50?

<img width="1198" height="399" alt="Image" src="https://github.com/user-attachments/assets/8edbcb91-cf8e-4f6a-8352-cf737d9a5e8d" />



Next I looked at if there was a relationship between cost per ml and review score:

A very weak correlation of 0.08 was found showing that price is a bad estimate of review score.
This may have been partially moderated by reviewers taking into account price value when reviewing perfumes.
<img width="1202" height="167" alt="Image" src="https://github.com/user-attachments/assets/192051f1-83de-420c-bc10-6b563062e73d" />

<img width="1202" height="581" alt="Image" src="https://github.com/user-attachments/assets/8286d9d2-d085-460a-afd9-b42f31be7079" />
