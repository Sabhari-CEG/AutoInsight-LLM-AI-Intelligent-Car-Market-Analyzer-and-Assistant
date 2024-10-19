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

