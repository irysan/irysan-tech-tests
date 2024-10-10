# Tech Challenge: Build an API for Air Quality Data Transformation

## Objective:
The goal of this challenge is to assess your ability to create a RESTful API that performs data transformations, handles filtering and analytics, and leverages clean coding practices. You will be working with a dataset focused on global annual PM2.5 air pollution levels, which represents critical environmental data.

## Dataset Overview:
You will be using the **Global Annual PM2.5 Grids** dataset provided by SEDAC. This dataset contains information on PM2.5 (particulate matter) air pollution levels collected from various satellite and observation sources.
https://sedac.ciesin.columbia.edu/data/set/sdei-global-annual-gwr-pm2-5-modis-misr-seawifs-viirs-aod-v5-gl-04

The dataset includes fields such as:
- **Latitude**: The latitude of the data point.
- **Longitude**: The longitude of the data point.
- **Year**: The year the data was collected.
- **PM2.5 Level**: The concentration of PM2.5 in µg/m³ (micrograms per cubic meter).

You will create a RESTful API that allows users to interact with this dataset, perform transformations, and run analytics.

## Task Overview:
You are required to build a RESTful API that:
1. Loads the dataset into memory for processing.
2. Exposes endpoints that allow basic interaction with the data, including CRUD operations, filtering, and simple statistics.
3. Containerizes the application using Docker.

## Requirements:
1. **Programming Language**: Choose between Python (Flask/FastAPI) or TypeScript (Express.js).
2. **Database**: In-memory storage (e.g., Pandas for Python or a simple in-memory array/object for Node.js) will be used for the dataset.
3. **Data Transformation**: Implement specified transformations and analytics on the air quality data (see details below).
4. **API Endpoints**:
   - `GET /data`: Retrieve all available data.
   - `GET /data/:id`: Fetch a specific data entry by ID.
   - `POST /data`: Add a new data entry (validate required fields).
   - `PUT /data/:id`: Update an existing data entry.
   - `DELETE /data/:id`: Delete a data entry.
   - `GET /data/filter?year=:year&lat=:lat&long=:long`: Filter the dataset based on year, latitude, and longitude.
   - `GET /data/stats`: Provide basic statistics (count, average PM2.5, min, max) across the dataset.
   - `GET /data/region?lat_min=:lat_min&lat_max=:lat_max&long_min=:long_min&long_max=:long_max`: Retrieve data within a bounding box (defined by latitude/longitude).
5. **Docker**: Create a `Dockerfile` to containerize the API.

## Dataset Fields:
You will be working with the following dataset columns:
- **Year**: Year the PM2.5 levels were recorded.
- **Latitude**: The geographic latitude where data was recorded.
- **Longitude**: The geographic longitude where data was recorded.
- **PM2.5 Level**: The concentration of PM2.5 (particulate matter) in µg/m³.

## Transformations & Analytics:
- **Basic Statistics**: The API should provide aggregate statistics like count, mean, min, and max PM2.5 levels across the entire dataset.
- **Filtering**: Users should be able to filter by year, latitude/longitude, or specify a bounding box to retrieve data for a specific region.
- **PM2.5 Range Normalization**: Implement an endpoint that normalizes the PM2.5 levels to a scale between 0 and 1 for comparison purposes.
- **Top 10 Polluted Locations**: An endpoint to return the top 10 most polluted locations in the dataset for a given year.

## Expected Deliverables:
1. A working RESTful API with the defined endpoints.
2. A Dockerfile that allows the API to be containerized.
3. Instructions on how to run the API (via Docker or locally).
4. Bonus: Include basic tests for your API functionality.

## Evaluation Criteria:
- **Code Quality**: Clean, maintainable, and modular code.
- **API Design**: Well-designed RESTful endpoints and adherence to best practices.
- **Error Handling**: Robust error handling and input validation.
- **Performance**: Efficient querying and filtering of data.
- **Best Practices**: Clean code, test coverage, and version control usage (e.g., Git).
- **Bonus**: Use of CI/CD practices, unit testing, or extra analytics.

## Time Limit:
- **90 minutes** to complete the task.

## Submission:
- Submit a GitHub repository with your solution.
- Include a `README.md` with instructions on how to run your API (locally or with Docker).

Good luck!
