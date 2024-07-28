# Orbit Travel Technical Test

Case 1
====================
<h3>Test Strategy and Test Risks</h3>
<table>
    <tr>
        <th>Number</th>
        <th>Test Risk</th>
        <th>Description</th>
        <th>Likelihood</th>
        <th>Impact</th>
        <th>Mitigation Strategy</th>
    </tr>
    <tr>
    </tr>
</table>

<h3>Test Suite and Test Cases</h3>
<table>
    <tr>
        <th>Number</th>
        <th>Test Case</th>
        <th>Description</th>
        <th>Priority</th>
    </tr>
    <tr>
        <td></td>
        <td>Connect to Database</td>
        <td>Ensure that a connection can be made from the service to the database</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing a valid SELECT query that returns rows from the database</td>
        <td>Run a basic SELECT query that is valid and that should return entries from the database (ie, will return a result from the database) and ensure that the returned results are as expected</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing a valid SELECT query that returns no results</td>
        <td>Run a basic SELECT query that is valid and that should not return entries from the database (ie, will return a result of no rows from the database) and ensure that the returned results are as expected, and that the service displays this well</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing an invalid SELECT query</td>
        <td>Run a basic SELECT query that is invalid (ie, will return an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing a valid basic INSERT query</td>
        <td>Run a basic INSERT query that is valid (ie, will successfully update the database) and ensure that the database is modified accordingly</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing an invalid INSERT query</td>
        <td>Run a basic INSERT query that is invalid (ie, will return an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing an UPDATE query</td>
        <td>Run a basic UPDATE query and ensure that the user is not able to make an update to the database, and that they are denied permissions gracefully by the service</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Executing a DELETE query</td>
        <td>Run a basic DELETE query and ensure that the user is not able to delete entries in the database, and that they are denied permissions gracefully by the service</td>
        <td>High</td>
    </tr>
    <tr>
        <td></td>
        <td>Execute a prepared valid SELECT query that returns rows from the database</td>
        <td>Run a valid prepared SELECT query, where the prepared query is sent to the server separate from the data, and ensure that the returned results are as expected</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Execute a prepared valid SELECT query that returns no results</td>
        <td>Run a valid prepared SELECT query, where the prepared query is sent to the server separate from the data, that should not return entries from the database (ie, will return a result of no rows from the database) and ensure that the returned results are as expected, and that the service displays this well</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Execute a prepared invalid SELECT query</td>
        <td>Run an invalid prepared SELECT query, where the prepared query is sent to the server separate from the data, that is invalid (ie, will return an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Execute a prepared valid INSERT query</td>
        <td>Run a valid prepared INSERT query, where the prepared query is sent to the server separate from the data, and ensure that the database is modified accordingly</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Execute a prepared invalid INSERT query</td>
        <td>Run an invalid prepared INSERT query (ie, will return an error from the database), where the prepared query is sent to the server separate from the data, and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Using Promise Wrappers that Resolve Successfully for SELECT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a SELECT query that resolves successfully (ie, does not return an error from the database) and ensure that the returned results are as expected</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Using Promise Wrappers that Does not Resolve Successfully for SELECT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a SELECT query that does not resolve successfully (ie, returns an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Using Promise Wrappers that Resolve Successfully for INSERT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a INSERT query that resolves successfully (ie, does not return an error from the database) and ensure that the database is modified accordingly</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Using Promise Wrappers that Does not Resolve Successfully for INSERT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a INSERT query that that does not resolve successfully (ie, returns an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td></td>
        <td>Using Connection Pools</td>
        <td>Ensure that the service is able to utilize connection pools that are provided by MYSQL2 for better latency of queries</td>
        <td>Low</td>
    </tr>
    <tr>
        <td></td>
        <td>Using Whitelist Protection for Query Parts</td>
        <td>Ensure that the service can work with a whitelist of SQL query parts to protect against SQL injection</td>
        <td>Low</td>
    </tr>
    <tr>
        <td></td>
        <td>Run Multithreads of Queries as a Performance Test</td>
        <td></td>
        <td>Low</td>
    </tr>
</table>

Case 2
====================
Are there any issues with the input data?
---------------------
Yes. The following are the issues that I identified:
* The Check In Date and Check Out Date columns are reversed. The data values in the file all have Check Out Date data values that predate Check In Date data values.
* In the second data row, the date value in the Invoice Date column is invalid.
* In the fourth data row, there is an extra column. This is indicated by the fact that there are additional commas at the end of the row.
* In the fifth data row, the data values from the Rental Agreement No column is missing. Additionally, the data from the Inovice Date column onwards are all "shifted left", making them present in the wrong columns, with the final Check In Date column having no corresponding data value.
* In the sixth data row, there is a non-numeric value in the Account Number column.

Describe some of the test cases for a service that processes CSV files.
---------------------
<h3>Test Suite and Test Cases</h3>
<table>
    <tr>
        <th>Number</th>
        <th>Test Case</th>
        <th>Description</th>
        <th>Priority</th>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td>High</td>
    </tr>
</table>


Case 3
====================

* Mathematically, no. To round a number up:
    * If the number to the right of the place value being rounded to is between 0 and 4 (inclusive), then the number in the place value being rounded to stays the same while all numbers to the right of the place value being rounded to are made 0.
    * If the number to the right of the place value being rounded to is between 5 and 9 (inclusive), then the number in the place value being rounded to is increased by 1 while all numbers to the right of the place value being rounded to are made 0.
* However, rounding is conte