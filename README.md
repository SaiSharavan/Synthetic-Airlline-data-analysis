# Airline Dataset

## Introduction
This dataset contains detailed information about airline passengers, flights, and airports. It includes fields such as passenger details, flight dates, and additional derived fields like age groups and departure year and month.

## Preprocessing Steps
The original dataset was preprocessed using Qlik Cloud, and the following transformations were applied:
1. **Loaded Original CSV File:** The original dataset was loaded into Qlik Cloud.
2. **Added Age Group:** A new field `age_group` was created based on passenger ages using the following logic:
   - **Age Group Categories:**
     - `0-1` : Baby
     - `2-4` : Toddler
     - `5-9` : Child
     - `10-12` : Tween
     - `13-19` : Teen
     - `20-24` : Young Adult
     - `25-39` : Adult
     - `40-54` : Middle-aged Adult
     - `55-79` : Elder
     - `80+` : Just plain old
3. **Extracted Departure Year:** The `departure_year` field was extracted from the `departure_date`.
4. **Extracted Departure Month:** The `departure_month` field was extracted from the `departure_date`.

## Data Dictionary
| Column Name           | Data Type | Description                                           |
|-----------------------|-----------|-------------------------------------------------------|
| passenger_id          | Integer   | Unique identifier for each passenger.                 |
| first_name            | String    | First name of the passenger.                          |
| last_name             | String    | Last name of the passenger.                           |
| gender                | String    | Gender of the passenger.                              |
| age                   | Integer   | Age of the passenger.                                 |
| nationality           | String    | Nationality of the passenger.                         |
| airport_name          | String    | Name of the departure airport.                        |
| airport_country_code  | String    | Country code of the departure airport.                |
| country_name          | String    | Country name of the departure airport.                |
| airport_continent     | String    | Continent of the departure airport.                   |
| continents            | String    | Continents involved in the flight.                    |
| departure_date        | Date      | Date of the flight departure.                         |
| arrival_airport       | String    | Name of the arrival airport.                          |
| pilot_name            | String    | Name of the pilot.                                    |
| flight_status         | String    | Status of the flight (e.g., on-time, delayed).        |
| age_group             | String    | Age group of the passenger (e.g., 'Baby', 'Tween').   |
| departure_year        | Integer   | Year extracted from the departure date.               |
| departure_month       | String    | Month extracted from the departure date.              |

## Age Group Categories
- **0-1:** Baby
- **2-4:** Toddler
- **5-9:** Child
- **10-12:** Tween
- **13-19:** Teen
- **20-24:** Young Adult
- **25-39:** Adult
- **40-54:** Middle-aged Adult
- **55-79:** Elder
- **80+:** Just plain old

## Usage Instructions
The dataset can be used for various analyses, including:
- Understanding passenger demographics.
- Analyzing flight patterns by year and month.
- Examining the distribution of age groups across different flights.

To use the data:
1. Load the CSV file into Qlik Cloud or another data analysis tool.
2. Use the data dictionary above to understand the structure of the dataset.
3. Apply your analysis or visualization techniques as needed.

## Sample Data Preview
Here is a preview of the first few rows of the dataset:

| passenger_id | first_name | last_name | gender | age | nationality | airport_name | airport_country_code | country_name | airport_continent | continents | departure_date | arrival_airport | pilot_name | flight_status | age_group        | departure_year | departure_month |
|--------------|------------|-----------|--------|-----|-------------|--------------|---------------------|--------------|------------------|------------|----------------|-----------------|------------|---------------|------------------|----------------|-----------------|
| ABVWIg       | Edithe     | Leggis    | Female | 62  | Japan       | Coldfoot Airport | US  | United States | NAM  | North America  | 2022-06-28  | CXF             | Fransisco Hazeldine | On Time   | Elder            | 2022           | June            |
| jkXXAX       | Elwood     | Catt      | Male   | 62  | Nicaragua   | Kugluktuk Airport | CA  | Canada        | NAM  | North America  | 2022-12-26  | YCO             | Marla Parsonage   | On Time   | Elder            | 2022           | December        |
| CdUz2g       | Darby      | Felgate   | Male   | 67  | Russia      | Grenoble-Isère Airport | FR  | France     | EU   | Europe         | 2022-01-18  | GNB             | Rhonda Amber      | On Time   | Elder            | 2022           | January         |
| BRS38V       | Dominica   | Pyle      | Female | 71  | China       | Ottawa / Gatineau Airport | CA  | Canada    | NAM  | North America  | 2022-09-16  | YND             | Kacie Commucci    | Delayed   | Elder            | 2022           | September       |
| 9kvTLo       | Bay        | Pencost   | Male   | 21  | China       | Gillespie Field | US  | United States   | NAM  | North America  | 2022-02-25  | SEE             | Ebonee Tree       | On Time   | Young Adult      | 2022           | February        |
| nMJKVh       | Lora       | Durbann   | Female | 55  | Brazil      | Coronel Horácio de Mattos Airport | BR  | Brazil | SAM  | South America | 2022-06-10  | LEC             | Inglis Dolley     | On Time   | Elder            | 2022           | June            |
| 8IPFPE       | Rand       | Bram      | Male   | 73  | Ivory Coast | Duxford Aerodrome | GB  | United Kingdom | EU  | Europe         | 2022-10-30  | QFO             | Stanislas Tiffin  | Cancelled | Elder            | 2022           | October         |
| pqixbY       | Perceval   | Dallosso  | Male   | 36  | Vietnam     | Maestro Wilson Fonseca Airport | BR  | Brazil  | SAM  | South America | 2022-04-07  | STM             | Sharyl Eastmead   | Cancelled | Adult             | 2022           | April           |
| QNAs2R       | Aleda      | Pigram    | Female | 35  | Palestinian Territory | Venice Marco Polo Airport | IT  | Italy   | EU   | Europe         | 2022-08-20  | VCE             | Daryn Bardsley    | On Time   | Adult             | 2022           | August          |
| 3jmudz       | Burlie     | Schustl   | Male   | 13  | Thailand    | Vermilion Airport | CA  | Canada        | NAM  | North America  | 2022-04-06  | YVG             | Alameda Carlyle   | On Time   | Teen             | 2022           | April           |
| 2P41gZ       | Porty      | Jori      | Male   | 39  | Tunisia     | Nuevo Casas Grandes Airport | MX  | Mexico  | NAM  | North America  | 2022-05-27  | NCG             | Rasia Fidelus     | Cancelled | Adult             | 2022           | May             |
| sBf524       | Briant     | De La Haye | Male  | 71  | Russia      | Ruben Cantu Airport | PA  | Panama       | NAM  | North America  | 2022-02-06  | SYP             | Alina Flooks      | Delayed   | Elder            | 2022           | February        |
| PlwJZT       | Kalie      | Scoble    | Female | 47  | Sweden      | Loralai Airport | PK  | Pakistan       | AS   | Asia           | 2022-03-19  | LRG             | Madelena Lennarde | Delayed   | Middle-aged Adult | 2022           | March           |

