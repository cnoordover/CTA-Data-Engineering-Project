# CTA "Locations API"
This project uses one of the three public APIs that the CTA publishes (Arrivals, Follow This Train, Locations)

The Locations API provides the location (in lat and lon) of every train in the CTA system

Additional information provided by Locations API: next station, final destination, run number, route color

## Information about API
Directly published by CTA: https://www.transitchicago.com/developers/ttdocs/#locations

CTA gets data from its rail infrastructure (not direct GPS data from railcars)

Maximum transaction limit from this API is 100,000 transactions per day

Currently in Beta

## Access Key Information
Must apply for an access key from CTA directly (link: https://www.transitchicago.com/developers/traintrackerapply/)

Took me less than 5 minutes to get approved (will send the key to the email you provide in the form)

## Parameters
Use URL query string method.

![image](https://github.com/user-attachments/assets/6758cabd-7cdd-4d95-a404-63e1430f1d30)

## Response fields:
Note: variables that I will be extracting are bolded.

![image](https://github.com/user-attachments/assets/d630af62-b494-4beb-acee-687c4d1edc31)

## Example Output from API 
You see an example for the output of just one train of one route in the system. 
![image](https://github.com/user-attachments/assets/1e943c98-c66b-46e9-a0ab-62ac2446dc23)
