# AutoInsight-LLM-AI-Intelligent-Car-Market-Analyzer-and-Assistant
AutoInsight AI is a cutting-edge, AI-powered platform that revolutionizes the car buying and selling experience. By seamlessly integrating advanced data analysis techniques, machine learning algorithms, and natural language processing, this intelligent system provides unparalleled insights into the automotive market. By combining traditional data analysis techniques with LLM-generated insights to provide a user-friendly car buying assistant.

## Dataset

The project utilizes the Vehicle Sales Data from Kaggle:
[Vehicle Sales Data](https://www.kaggle.com/datasets/syedanwarafridi/vehicle-sales-data)

### Dataset Structure:
- **year**: The manufacturing year of the vehicle
- **make**: The brand or manufacturer of the vehicle
- **model**: The specific model of the vehicle
- **trim**: Additional designation for the vehicle model
- **body**: The body type of the vehicle (e.g., SUV, Sedan)
- **transmission**: The type of transmission in the vehicle
- **vin**: Vehicle Identification Number
- **state**: The state where the vehicle is registered
- **condition**: Condition of the vehicle, rated on a scale
- **odometer**: The mileage or distance traveled by the vehicle
- **color**: Exterior color of the vehicle
- **interior**: Interior color or material
- **seller**: Information about the seller
- **mmr**: Manheim Market Report value
- **sellingprice**: The price at which the vehicle was sold
- **saledate**: The date of the sale

## Key Features

1. **Natural Language Query Processing**: Utilizes LLMs to interpret user queries about car purchases.
2. **Data-Driven Insights**: Provides statistics and recommendations based on the comprehensive car sales dataset.
3. **Top Recommendations**: Offers top 5 car suggestions based on recent year, good condition, and lower price.

## Implementation Details

### Data Loading and Preprocessing
- The dataset is loaded from a CSV file using pandas.
- Basic data cleaning is performed, including handling missing values and converting data types.

### Query Processing
- The system uses regular expressions to extract relevant information (make and model) from user queries.
- This extraction is done using the `extract_make_model` function.

### Data Analysis
- The `search_cars` function filters the dataset based on the extracted make and model.
- `generate_car_summary` calculates statistics (average year, condition, odometer, price) and identifies top suggestions.
- Top suggestions are sorted based on recent year, good condition, and lower price.

### LLM Integration
The project uses an LLM (GPT-2 in this implementation) to:
1. Generate human-readable insights based on the data analysis results.
2. Provide a more natural language interpretation of the statistical findings.

### Input and Output
- **Input**: Natural language queries about car purchases (e.g., "I want to buy a Toyota Camry")
- **Output**: 
  - Average statistics (year, condition, odometer, price)
  - Top 5 recommendations based on specified criteria
  - LLM-generated insights interpreting the analysis results

### Main Function
The `car_assistant` function:
1. Prompts the user for input
2. Extracts make and model from the query
3. Searches for matching cars in the dataset
4. Generates a summary of findings
5. Uses the LLM to provide additional insights on the results

This implementation combines traditional data analysis techniques with LLM-generated insights to provide a user-friendly car buying assistant.
## Advantages of Using LLMs

1. **Flexibility**: Can handle a wide variety of natural language queries without hardcoding.
2. **Adaptability**: The system can potentially adapt to new types of queries or data without major code changes.
3. **Natural Language Understanding**: Provides a more intuitive user interface.
4. **Code Generation**: Allows for dynamic creation of analysis code based on user needs.

## Interpretation of Results

The analysis provides insights into:
1. Average characteristics of desired car models
2. Price trends and value propositions
3. Availability and popularity of specific makes and models
4. Relationship between car condition, age, and price

These insights help potential buyers make informed decisions by understanding the market landscape for their desired vehicles.

## Future Enhancements

1. Implement selling functionality
2. Expand the range of analyzable factors
3. Integrate more advanced ML models for price prediction
4. Enhance the LLM's training for more accurate and specific car-related queries

## Sample Query and Results

### Query
"I want to buy a audi a4"
![Audi A4 Query](q1.png)

### Results
![Audi A4 Query Results](q1_res.png)

#### Average Statistics for Audi A4:
- Average Year: 2008
- Average Condition: 29.4/5
- Average Odometer: 75,397 miles
- Average Price: $12,476.40

#### Top 5 Suggestions:
1. 2015 Audi A4: Condition 49.0/5, Odometer 10,559.0 miles, Price $27,400.00
2. 2015 Audi A4: Condition 49.0/5, Odometer 2,365.0 miles, Price $28,000.00
3. 2015 Audi A4: Condition 49.0/5, Odometer 7,136.0 miles, Price $30,250.00
4. 2015 Audi A4: Condition 48.0/5, Odometer 4,164.0 miles, Price $30,400.00
5. 2015 Audi A4: Condition 46.0/5, Odometer 3,827.0 miles, Price $29,500.00

### Interpretation

1. **Market Overview**: The average Audi A4 in the dataset is from 2008, indicating a mix of older and newer models. The average price of $12,476.40 reflects this mix of model years.

2. **Condition Discrepancy**: There's a significant difference between the average condition (29.4/5) and the conditions of the top suggestions (46-49/5). This suggests that newer models are generally in much better condition, or there might be an issue with condition scoring for older models.

3. **Mileage Impact**: The average odometer reading of 75,397 miles is considerably higher than the top suggestions (all under 11,000 miles). This indicates that mileage significantly influences the car's value and ranking in suggestions.

4. **Price Range**: There's a large gap between the average price ($12,476.40) and the prices of top suggestions ($27,400 - $30,400). This emphasizes the premium placed on newer, low-mileage models.

5. **Model Year Preference**: All top suggestions are from 2015, indicating a strong preference or availability for this specific year in the high-end Audi A4 market.

6. **Condition vs. Price**: Among the top suggestions, there isn't a strict correlation between condition and price. For example, the highest-priced car ($30,400) isn't the highest-rated in condition, suggesting other factors (like specific features or trim levels) may influence pricing.

7. **Mileage Sensitivity**: Within the top suggestions, even small differences in mileage seem to affect pricing. For instance, the lowest-mileage car (2,365 miles) isn't the most expensive, indicating that factors beyond just mileage influence the high-end market.

This analysis demonstrates the car assistant's ability to provide a comprehensive market overview, from average statistics to top-tier options, allowing users to make informed decisions based on their preferences for model year, condition, mileage, and price.



