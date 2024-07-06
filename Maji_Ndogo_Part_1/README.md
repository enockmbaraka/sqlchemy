# Maji Ndogo: From Analysis to Action

Welcome to **Maji Ndogo: From Analysis to Action**. This project, led by the dedicated team at ExploreAI, focuses on leveraging extensive water survey data to address the pressing water crisis in Maji Ndogo. Our mission is to transform this data into actionable insights that will inform solutions and improve water accessibility and quality in the region.

## Table of Contents
- [Project Overview](#project-overview)
- [Project Goals](#project-goals)
- [Data Overview](#data-overview)
- [Tasks and Timeline](#tasks-and-timeline)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Data Model](#data-model)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Project Overview

Maji Ndogo, a region plagued by water scarcity and quality issues, is the focus of this project. We have collected a vast amount of data (over 60,000 records) through the hard work of engineers, field workers, scientists, and analysts. This dataset contains crucial information about water sources, pollution levels, employee activities, and more.

Our task is to analyze this dataset, uncover hidden patterns, and extract insights that will guide actionable solutions to enhance water services in Maji Ndogo.

**Fictitious Project Lead:** Aziza Naledi  
**Fictitious Mentor:** Chidi Kunto

## Project Goals

1. **Explore the Data:** Understand the structure, variables, and connections within the dataset.
2. **Identify Patterns:** Use exploratory data analysis to uncover trends and correlations.
3. **Data Cleaning:** Address inconsistencies and errors within the dataset.
4. **Insight Generation:** Develop insights that can inform solutions to improve water quality and accessibility.
5. **Action Plan:** Create data-driven recommendations for addressing water issues in Maji Ndogo.

## Data Overview

The data collected is structured into several tables, each focusing on different aspects of the water survey:

- **employee:** Information about employees involved in data collection.
- **global_water_access:** Global water access statistics by country and region.
- **location:** Details about various locations within Maji Ndogo.
- **visits:** Records of visits to water sources and locations.
- **water_quality:** Data on the quality of water sources.
- **water_source:** Information about different types of water sources.
- **well_pollution:** Pollution test results for various water sources.

A comprehensive data dictionary is provided to understand the data columns, types, and descriptions.

## Tasks and Timeline

Over the next few weeks, we will undertake the following tasks:

### Week 1: Data Familiarization and Exploration

- **Objective:** Get acquainted with the dataset, its structure, and contents.
- **Tasks:**
  - Load the dataset into your preferred analysis tool.
  - Explore the foundational tables and their structures.
  - Identify key variables and their relationships.

### Week 2: In-depth Data Analysis

- **Objective:** Dive deeper into the data to understand different sources and visit patterns.
- **Tasks:**
  - Use SELECT queries to explore data sources.
  - Analyze visit patterns to various water sources.
  - Document initial findings and potential areas of interest.

### Week 3: Water Quality and Pollution Analysis

- **Objective:** Focus on water quality and pollution issues.
- **Tasks:**
  - Analyze water quality scores and trends.
  - Correct pollution data using LIKE and string operations.
  - Identify key pollution issues and their impact.

### Week 4: Insight Generation and Reporting

- **Objective:** Extract meaningful insights and prepare for reporting.
- **Tasks:**
  - Compile findings from previous weeks.
  - Generate insights related to water quality, accessibility, and pollution.
  - Prepare a comprehensive report summarizing the insights and recommendations.

### Week 5: Actionable Recommendations

- **Objective:** Develop data-driven recommendations to improve water services.
- **Tasks:**
  - Create actionable plans based on insights.
  - Outline steps for implementation and potential impact.
  - Present recommendations to the team.

## Getting Started

### Prerequisites

- **Python 3.x** or any other preferred programming language for data analysis.
- **SQL** knowledge for querying the database.
- **Data Analysis Libraries**: pandas, numpy, matplotlib, etc. (if using Python).
- **Database Management Tool**: MySQL, PostgreSQL, etc.

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/ExploreAI/Maji-Ndogo.git
    cd Maji-Ndogo
    ```

2. Set up the virtual environment and install dependencies:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```

3. Configure the database connection:

    - Update `config/database.yml` with your database credentials.

### Usage

1. **Load the Data:**

   Follow the instructions in `scripts/load_data.py` to load the dataset into your analysis tool or database.

2. **Explore the Data:**

   Use `notebooks/data_exploration.ipynb` to begin your exploratory data analysis.

3. **Generate Insights:**

   Follow `scripts/analysis.py` for analyzing water quality, pollution issues, and more.

## Data Model

Here is a brief overview of the tables in our database:

### employee

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| assigned_employee_id | Unique ID assigned to each employee.     | INT            |
| employee_name       | Name of the employee.                    | VARCHAR(255)   |
| phone_number        | Contact number of the employee.          | VARCHAR(15)    |
| email               | Email address of the employee.           | VARCHAR(255)   |
| address             | Residential address of the employee.     | VARCHAR(255)   |
| town_name           | Name of the town where the employee resides. | VARCHAR(255)|
| province_name       | Name of the province where the employee resides. | VARCHAR(255)|
| position            | Position or job title of the employee.   | VARCHAR(255)   |

### global_water_access

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| name                | The country or area name.                | VARCHAR(255)   |
| region              | Geographical region.                     | VARCHAR(255)   |
| year                | Year of the data record.                 | INT            |
| pop_n               | The national population size estimate in thousands. | FLOAT   |
| pop_u               | The urban population share estimate in percentage points (%) | FLOAT |
| wat_bas_n           | The estimated national share of people with at least basic service (%) | FLOAT |
| wat_lim_n           | The estimated national share of people with limited service (%) | FLOAT |
| wat_unimp_n         | The estimated national share of people with unimproved service (%) | FLOAT |
| wat_sur_n           | The estimated national share of people with surface service (%) | FLOAT |
| wat_bas_r           | The estimated rural share of people with at least basic service (%) | FLOAT |
| wat_lim_r           | The estimated rural share of people with limited service (%) | FLOAT |
| wat_unimp_r         | The estimated rural share of people with unimproved service (%) | FLOAT |
| wat_sur_r           | The estimated rural share of people with surface service (%) | FLOAT |
| wat_bas_u           | The estimated urban share of people with at least basic service (%) | FLOAT |
| wat_lim_u           | The estimated urban share of people with limited service (%) | FLOAT |
| wat_unimp_u         | The estimated urban share of people with unimproved service (%) | FLOAT |
| wat_sur_u           | The estimated urban share of people with surface service (%) | FLOAT |

### location

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| location_id         | Unique ID assigned to each location.     | VARCHAR(255)   |
| address             | Address of the location.                 | VARCHAR(255)   |
| province_name       | Name of the province where the location is situated. | VARCHAR(255)|
| town_name           | Name of the town where the location is situated. | VARCHAR(255)|
| location_type       | Type or category of the location.        | VARCHAR(255)   |

### visits

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| record_id           | Unique ID assigned to each visit.        | INT            |
| location_id         | ID of the location visited.              | VARCHAR(255)   |
| source_id           | ID of the water source visited.          | VARCHAR(510)   |
| time_of_record      | Date and time of the visit.              | DATETIME       |
| visit_count         | Number of visits made to this location.  | INT            |
| time_in_queue       | Time spent by people waiting for water in a queue at the location. | INT |
| assigned_employee_id| ID of the employee who visited the location. | INT            |

### water_quality

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| record_id           | Unique ID assigned to each record.       | INT            |
| subjective_quality_score | Score representing the subjective quality of the water source. | INT |
| visit_count         | Number of visits made for data collection.| INT            |

### water_source

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| source

_id           | Unique ID assigned to each water source. | INT            |
| type_of_water_source| Type or category of the water source. Can be: tap_in_home, tap_in_home_broken, well, shared_tap, river. | VARCHAR(255) |
| number_of_people_served | Number of people served by this water source. | INT            |

### well_pollution

| Column Name         | Description                              | Data Type      |
|---------------------|------------------------------------------|----------------|
| source_id           | ID of the water source being tested for pollution. | VARCHAR(258) |
| date                | Date of the pollution test.              | DATETIME       |
| description         | Description of the pollution test.       | VARCHAR(255)   |
| pollutant_ppm       | Result of the pollution test in parts per million. | FLOAT       |
| biological          | Biological contamination level.          | FLOAT          |
| results             | Result of the pollution test.            | VARCHAR(255)   |

## Contributing

We welcome contributions from the community. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the ExploreAI license.  
**Please do not copy without permission. © ExploreAI 2023.**

## Contact

For any questions or support, please contact:

**Paschal Ugwu** - Author  
**Email:** ugwupaschal@gmail.com

We look forward to your active participation and the incredible insights we'll discover together on this journey to improve Maji Ndogo's water situation. Let's make a difference!
