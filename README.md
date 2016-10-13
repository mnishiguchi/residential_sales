Residential sales
=================

In this repository, I will study data visualization in Rails. This app is a sample app from the book [Data Visualization Toolkit: Using JavaScript, Rails, and Postgres to Present Data and Geospatial Information](https://www.amazon.com/Data-Visualization-Toolkit-Addison-Wesley-Professional/dp/0134464435) by Barrett Clark

- [source of original app](https://github.com/DataVizToolkit/residential_sales)


## Data

- [Data.gov :: Maryland Total Residential Sales - PFA - 2012 - Zipcode](http://catalog.data.gov/dataset/maryland-total-residential-sales-pfa-2012-zipcode-00dc0)
- [Maryland.gov :: Maryland Total Residential Sales - PFA - 2012 - Zipcode](https://data.maryland.gov/Demographic/Maryland-Total-Residential-Sales-PFA-2012-Zipcode/ag7x-nwtv)

#### Downloading the CSV file directly from the terminal

```
curl -o data.csv https://data.maryland.gov/api/views/ag7x-nwtv/rows.csv?accessType=DOWNLOAD
```

## Evaluating Data

- format of data
  + check the delimiter if the data is CSV
  + prettify it if the data is JSON
- fields and data types
  + more than one piece of data?
  + range?
  + geographic data(latitude and longitude)?
  + contains data that needs to be cleaned?

### Tips from the auther
- Avoid modifying data significantly.
- Don't create new data.

## Data Dictionary

- Define fields in the dataset

## Rake Task

- Helps us streamline tedious or repetitive tasks.

#### Generating a new rake task

```
rails g task seed import_maryland_residential_sales
```

## Extract, Transform, Load (ETL)

### Extract
- Get data.

### Transform
- Clean up the data.

### Load
- Load the data into the database.

## Dealing with invalid values
- e.g., Prevent an invalid value from being coerced to 0.
- e.g., Raise an exception when data is invalid so that we ca figure out what todo from there.


## Misc

### Checking line count of a given file

```
wc -l db/data_files/data.csv
```
