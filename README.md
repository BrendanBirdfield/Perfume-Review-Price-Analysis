# Perfume-Review-Price-Analysis
A project comparing mens perfume reviews and prices with the goal of being able to find the best reviewed perfumes for the lowest price.

Perfume Prices were webscraped from a list of mens perfumes from the price checker site: https://pricespy.co.uk/c/perfume?98221=31505
These were then saved to a dataframe for processing.
A list of perfume names was then created from this dataframe.
A list of reviews for each perfume was webscraped from https://www.parfumo.com/ 
Selenium was used to search for each perfume from the list of mens perfumes and append the reviews to a list and added to a dataframe.
The dataframes for prices and reviews were then joined on perfume name. The price per ml was calculated by dividing the price by the ml size of each perfume.

Finding the top 10 perfumes with reviews above 8/10 and then sorting for the lowest cost per ml.

<img width="1204" height="397" alt="Image" src="https://github.com/user-attachments/assets/7f2327b1-a6df-435f-adaf-8b008be1b7ab" />
