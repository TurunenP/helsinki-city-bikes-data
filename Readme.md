
## Data Cleaning

1 - Download the data from the link provided in the course website using python notebook.

2 - Load the data into a dataframe using pandas.

3 - Check the data for missing values and remove the rows with missing values.

4 - Check the data for duplicates and remove the duplicates.

5 - Check the data for outliers and remove the outliers.

6 - Check the data for any other inconsistencies and remove them.

7 - Save the cleaned data into a new file.

## Data Formating to JSON

1 - Load the cleaned data into a dataframe using pandas.

2 - Convert the dataframe into a list of dictionaries.

3 - Save the list of dictionaries into a JSON file.


## Exporting the Data to MongoDB

1 - Load the JSON file into a dataframe using pandas.

2 - Convert the dataframe into a list of dictionaries.

3 - Connect to MongoDB and insert the list of dictionaries into the database.

## Bash Script to Import the Data to MongoDB

1 - Create a bash script to import the data to MongoDB.


### Journey Data

```bash

#!/bin/bash

mongoimport --uri "mongodb+srv://doadmin:3Cn2Kp4jcJ80W659@db-mongodb-nyc1-22526-ccc29d80.mongo.ondigitalocean.com/admin?tls=true&authSource=admin" --collection journey --jsonArray --type json  --file data.json





```
### Station Data

```bash

#!/bin/bash

mongoimport --uri "mongodb+srv://doadmin:3Cn2Kp4jcJ80W659@db-mongodb-nyc1-22526-ccc29d80.mongo.ondigitalocean.com/admin?tls=true&authSource=admin" --collection stations --jsonArray --type json  --file station_data.json





```


### Run the bash script for Journey Data

```bash

chmod +x data_import.sh

./data_import.sh

```


### Run the bash script for Station Data

```bash

chmod +x station_data_import.sh

./station_data_import.sh

```










