# Hotel Recommendation System

This project implements a Hotel Recommendation System using Zomato data to suggest hotels based on user preferences. Leveraging a Content-Based Filtering approach, the system provides personalized and relevant recommendations by analyzing hotel attributes and user preferences. It aims to enhance user satisfaction and simplify the hotel discovery process.




## Features

- Content-Based Filtering: Recommendations are generated based on hotel attributes like location, amenities, ratings, and services.

- User-Centric Suggestions: Matches hotels with user preferences for accurate and personalized recommendations.

- Scalable: Designed to accommodate larger datasets and incorporate additional hotel features as needed.


## Libraries Used
- NumPy (numpy): Efficient handling of numerical arrays and mathematical operations.

- Pandas (pandas): Data manipulation and analysis with DataFrame structures.

- Seaborn (seaborn): Advanced, aesthetic data visualization.

- Matplotlib (matplotlib.pyplot): Basic plotting for static and interactive visualizations.

- Scikit-learn (sklearn): Machine learning algorithms, data splitting, and evaluation metrics.

- Warnings (warnings): Suppresses unwanted warnings during execution.

- NLTK (nltk): Natural language processing, including stop word removal.


- CountVectorizer: Converts text into a sparse matrix of word counts.

- TfidfVectorizer: Transforms text into TF-IDF weighted features.
## Dataset
The project uses the Zomato Restaurant Dataset, which contains information about restaurants, user reviews, ratings, and more. You can download the dataset from sources like Kaggle.
Link:-https://www.kaggle.com/datasets/rajeshrampure/zomato-dataset
## Project Workflow
1.Data Loading:
The dataset was loaded as a CSV file into a Pandas DataFrame.

2.Data Cleaning:
Renamed columns for better readability.
Converted the cost column to numeric and handled missing values.
Processed the rate column to exclude invalid entries such as "NEW" and "-".
Standardized boolean columns like online_order and book_table.

3.Text Preprocessing:
Lowercased all reviews and removed stopwords using NLTK.
Stripped URLs and irrelevant patterns from the text data.

4.Feature Engineering:
Added a new column Mean Rating initialized to zero.
Performed tokenization and vectorization of reviews using TfidfVectorizer.

5.Modeling:
Calculated cosine similarity scores on processed reviews.
Implemented a recommendation function to suggest restaurants based on similarity.

Recommendation Output:
Generated a list of similar restaurants with cuisines, cost, and ratings.
### Clone the repository
 https://github.com/your_name/Hotel-Recommendation-System.git
## Output
Input the name of a restaurant to get similar recommendations.

Input: 'Jalsa'

Output:
List of top 10 restaurants similar to 'Jalsa' with their cuisines, cost, and ratings.
## Future Enhancements

- Deploy the system as a web application using Flask or FastAPI.
- Incorporate real-time user feedback to refine recommendations.
