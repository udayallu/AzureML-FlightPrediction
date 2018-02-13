# AzureML-FlightPrediction
The challenge is based on a dataset containing information about flights, including details of whether flights were on-time, early, or late. Your goal is to explore the data to identify features that might be predictive of how many minutes late or early a flight will be.
## Ingest Flight Data
Start by signing in to your Azure Machine Learning Workspace and creating a new experiment. It doesn't matter what you name the experiment, just use an appropriate name like "Flights Challenge". After you've created the experiment, add the Flights Delay Data sample dataset to the experiment, and then visualize its contents.

## Join the Airport Codes Dataset
Note that the Flight Delays Data dataset includes the following columns:
1. OriginAirportID
2. DestAirportID
These are numeric identifiers for the origin airport and destination airport for each flight.
To see the details of the airports, add the Airport Codes Dataset sample dataset to the experiment, and join it to the Flight Delays Data dataset. You will need to create two joins; one to join the origin airport and one to join the destination airport. You can use built-in Azure Machine Learning Join Data modules to accomplish this, or you could use custom SQL, R, or Python code. The resulting joined dataset should contain the original flight data as well as the name, city, and state for both the origin and destination airports.

## Remove Duplicates and Replace Missing Values
2 points possible (graded)
Before you can explore the data, you must cleane it by removing duplicate rows and replacing missing values.

### Remove Duplicates
First, remove duplicate rows (retaining the first instance of each row). Rows are considered duplicates in this dataset if they have matching values for all the following fields:

1. Year
2. Month
3. DayofMonth
4. Carrier
5. OriginAirportID
6. DestAirportID
7.CRSDepTime
8. CRSArrTime
You can use the built-in Azure Machine Learning Remove Duplicate Rows module, or you can write a custom SQL, R, or Python script.
