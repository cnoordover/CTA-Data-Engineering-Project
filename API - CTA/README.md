# CTA "Locations API"
This project uses one of the three public APIs that the CTA publishes (Arrivals, Follow This Train, Locations)

The Locations API provides the location (in lat and lon) of every train in the CTA system

Additional information provided by Locations API: next station, final destination, run number, route color

## What is in this Data set? (data we will use is bolded)
**Name                Description**

ctatt               Root element

**./tmst              Shows time when response was generated in format: yyyyMMdd HH:mm:ss (24-hour format, time local to Chicago)**

./errCd             Numeric error code (see appendices)

./errNm             Textual error description/message (see appendices)

**./route name=       Container element (one per route in response), name attribute indicates route per GTFS-matching route identifiers (see appendices)**

**././train           Container element (one per train in response)**

**./././rn            Run number**

**./././destSt        GTFS unique stop ID where this train is expected to ultimately end its service run (experimental and supplemental only—see note below)**

./././destNm        Friendly destination description (see note below)

./././trDr          Numeric train route direction code (see appendices)

./././nextStaId     Next station ID (parent station ID matching GTFS)

./././nextStpId     Next stop ID (stop ID matching GTFS)

**./././nextStaNm     Proper name of next station**

./././prdt          Date-time format stamp for when the prediction was generated:  yyyyMMdd HH:mm:ss (24-hour format, time local to Chicago)

./././arrT          Date-time format stamp for when a train is expected to arrive/depart: yyyyMMdd HH:mm:ss (24-hour format, time local to Chicago)

./././isApp         Indicates that Train Tracker is now declaring “Approaching” or “Due” on site for this train

./././isDly         Boolean flag to indicate whether a train is considered “delayed” in Train Tracker

./././flags         Train flags (not presently in use)

**./././lat           Latitude position of the train in decimal degrees**

**./././lon           Longitude position of the train in decimal degrees**

./././heading       Heading, expressed in standard bearing degrees (0 = North, 90 = East, 180 = South, and 270 = West; range is 0 to 359, progressing clockwise)

## Information about API
Directly published by CTA: https://www.transitchicago.com/developers/ttdocs/#locations

CTA gets data from its rail infrastructure (not direct GPS data from railcars)

Maximum transaction limit from this API is 100,000 transactions per day

Currently in Beta

## Access Key Information
Must apply for an access key from CTA directly (link: https://www.transitchicago.com/developers/traintrackerapply/)

Took me less than 5 minutes to get approved (will send the key to the email you provide in the form)

## Example Output from API 
You see an example for the output of just one train of one route in the system. 
![image](https://github.com/user-attachments/assets/1e943c98-c66b-46e9-a0ab-62ac2446dc23)
