# Backend Task

This task involves creating APIs to interact with a third-party JSON data source related to product transactions. The primary objectives include initializing a database with seed data from the provided API, listing transactions with search and pagination functionalities, generating statistics, and producing visualizations in the form of bar and pie charts.

## Data Source

- **Third Party API URL:** [https://s3.amazonaws.com/roxiler.com/product_transaction.json](https://s3.amazonaws.com/roxiler.com/product_transaction.json)
- **Request Method:** GET
- **Response Format:** JSON

## Initializing the Database

Create an API to initialize the database by fetching JSON data from the third-party API and populating the database with seed data. You have the flexibility to define an efficient table/collection structure.

## Instructions

- All APIs mentioned below should accept a month (expected value: any month between January to December) as input and match it against the field `dateOfSale`, regardless of the year.

### List All Transactions

Create an API to list all transactions.

- The API should support search and pagination on product transactions.
- Based on the search parameters, it should match the search text on product title/description/price, returning the matching product transactions.
- If the search parameter is empty, it should return all records based on applied pagination.

#### Pagination Defaults
- Page: 1
- Per Page: 10

### Statistics API

Create an API for generating statistics:

- Total sale amount of the selected month.
- Total number of sold items for the selected month.
- Total number of unsold items for the selected month.

### Bar Chart API

Create an API for generating a bar chart:

- The response should contain price ranges and the number of items in each range for the selected month, regardless of the year.

#### Price Ranges
- 0 - 100
- 101 - 200
- 201 - 300
- 301 - 400
- 401 - 500
- 501 - 600
- 601 - 700
- 701 - 800
- 801 - 900
- 901 - Above

### Pie Chart API

Create an API for generating a pie chart:

- Find unique categories and the number of items from each category for the selected month, regardless of the year.

#### Example Output
- X Category: 20 (items)
- Y Category: 5 (items)
- Z Category: 3 (items)

### Combined Data API

Create an API that fetches data from all the aforementioned APIs, combines the responses, and sends a final response as a combined JSON.

---

Feel free to reach out with any questions or clarifications. Happy coding! 🚀
