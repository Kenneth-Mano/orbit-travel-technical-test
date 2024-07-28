# Orbit Travel Technical Test

Case 1
====================
<h3>Test Strategy</h3>

The following are some of the testing phases that will be performed as part of testing this service:
1. Funtional testing - Ensuring basic functions of the service are working as expected.
2. Security testing - Ensuring that there is a basic level of security protections that are provided in the service.
3. Accessibility testing - Ensuring that the documentation that is provided for the service allows installation and use by a new user of the service.
4. Performance testing - Determining the current performance capabilities of the service and publishing them in the documentation. It is likely the case that future performance augmentations, including meeting performance SLAs will be left to future iterations of the service.

The testing tools used will be a combination of manual and automated tools. Manual testing can be used to ensure that the basic functionality of the service is provided, for ensuring basic security protections are in place, and for ensuring that the service is accessible. Automated testing will be especially useful for longevity of the service. This can be by creating automated smoke checks, as well as for performance testing of the service.

Finally, in the absence of clear requirements on the functional and non-functional aspects of the service, exploratory and risk-based testing approaches should be used. This will allow testers to seek out any and all information available regarding the product, to create tests based on the information gathered, to rank these in order of priority, and to therefore achieve a sufficient level of coverage for a minimum viable service to be developed and deployed, with respect to the constraints of the project.

<h3>Test Risks</h3>
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
        <td>1</td>
        <td>Unclear Service Delivery Timeline</td>
        <td>The timeline for the delivery of the service is unclear (ie, the amount of time to deliver the project is unknown, what milestones need to be achieved for the service, etc.)</td>
        <td>High</td>
        <td>Severe</td>
        <td>Speaking to stakeholders and others to gain greater clarity on the timeline. Modelling several different project timelines with different values to the unknown variables (duration, features in a minimum viable product, training time, buffers for project delays, etc.).</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Unclear Functional Requirements</td>
        <td>There is insufficient information about what functionality is required from the service in terms of its capabilities.</td>
        <td>High</td>
        <td>Severe</td>
        <td>Speaking to stakeholders and others to gain greater clarity on the functional requirements. Adopt a blue-sky approach to identifying different capabilities that could be expected of the service, ranking them in order of risk and priority, and performing testing informed by this knowledge.</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Unclear Use Cases</td>
        <td>There is insufficient information about how the service will be consumed (ie, will it be used via a command-line or consumed by an application, what the users of the service might want to see from it, etc).</td>
        <td>High</td>
        <td>Severe</td>
        <td>Speaking to stakeholders and others to gain greater clarity on how the service will be used. Adapting the testing methodology according to whether the service is being exposed directly or consumed by an application.</td>
    </tr>
    <tr>
        <td>4</td>
        <td>Test Effort Resourcing</td>
        <td>There are few dedicated test resources to testing the service.</td>
        <td>High</td>
        <td>Medium</td>
        <td>Involving testers earlier in the process of creating the service, so that they can raise concerns about the service early to reduce the turnaround time and the chances of defects being built into the service. Involving developers in testing, for instance via unit-testing.</td>
    </tr>
    <tr>
        <td>5</td>
        <td>No Non-Functional Requirements</td>
        <td>There is no information about what non-functional capabilities are required of the service, for instance in terms of performance, security, accessibility, etc.</td>
        <td>High</td>
        <td>Medium</td>
        <td>Speaking to stakeholders and others to gain greater clarity on the functional requirements. Adopt a blue-sky approach to identifying common non-functional benchmarks that could be expected of the service (in terms of performance, security, accessibility, etc.), ranking them in order of risk and priority, and performing testing informed by this knowledge.</td>
    </tr>
    <tr>
        <td>6</td>
        <td>Unskilled Testing Resources</td>
        <td>The test resources that are dedicated to the project are not specifically skilled in the testing that is being performed, especially with regards to non-functional requirements (security, accessibility).</td>
        <td>Medium</td>
        <td>Medium</td>
        <td>Ensuring that the testers are provided with a basic level of training in these areas. Seeking dedicated expert help with the specific types of non-functional tests that the team are not skilled at, for instance, by hiring an external security consultant to perform a security checks on the service.</td>
    </tr>
    <tr>
        <td>7</td>
        <td>Issues in the Libraries and Components for the Service</td>
        <td>There can be issues identified in any of the libraries and components used to create the service, whether it be in terms of the code and the implementation of it or the documentation and understanding how to use it.</td>
        <td>Low</td>
        <td>Low</td>
        <td>Mantaining a watch on the issues that are opened against the libraries and components for the service. Researching the libraries and components beforehand to identify any workarounds that might be required and any experts whose advice can be sought if such an issue is identified.</td>
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
        <td>1</td>
        <td>Install the Service</td>
        <td>Ensure that the service can be easily installed in several widely-used operating systems.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Connect to Database using the Service</td>
        <td>Ensure that a connection can be made from the service to the database</td>
        <td>High</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Executing a valid SELECT query that returns rows from the database</td>
        <td>Run a basic SELECT query that is valid and that should return entries from the database (ie, will return a result from the database) and ensure that the returned results are as expected</td>
        <td>High</td>
    </tr>
    <tr>
        <td>4</td>
        <td>Executing a valid SELECT query that returns no results</td>
        <td>Run a basic SELECT query that is valid and that should not return entries from the database (ie, will return a result of no rows from the database) and ensure that the returned results are as expected, and that the service displays this well</td>
        <td>High</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Executing an invalid SELECT query</td>
        <td>Run a basic SELECT query that is invalid (ie, will return an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>High</td>
    </tr>
    <tr>
        <td>6</td>
        <td>Executing a valid basic INSERT query</td>
        <td>Run a basic INSERT query that is valid (ie, will successfully update the database) and ensure that the database is modified accordingly</td>
        <td>High</td>
    </tr>
    <tr>
        <td>7</td>
        <td>Executing an invalid INSERT query</td>
        <td>Run a basic INSERT query that is invalid (ie, will return an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>High</td>
    </tr>
    <tr>
        <td>8</td>
        <td>Executing an UPDATE query</td>
        <td>Run a basic UPDATE query and ensure that the user is not able to make an update to the database, and that they are denied permissions gracefully by the service</td>
        <td>High</td>
    </tr>
    <tr>
        <td>9</td>
        <td>Executing a DELETE query</td>
        <td>Run a basic DELETE query and ensure that the user is not able to delete entries in the database, and that they are denied permissions gracefully by the service</td>
        <td>High</td>
    </tr>
    <tr>
        <td>10</td>
        <td>Execute a prepared valid SELECT query that returns rows from the database</td>
        <td>Run a valid prepared SELECT query, where the prepared query is sent to the server separate from the data, and ensure that the returned results are as expected</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>11</td>
        <td>Execute a prepared valid SELECT query that returns no results</td>
        <td>Run a valid prepared SELECT query, where the prepared query is sent to the server separate from the data, that should not return entries from the database (ie, will return a result of no rows from the database) and ensure that the returned results are as expected, and that the service displays this well</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>12</td>
        <td>Execute a prepared invalid SELECT query</td>
        <td>Run an invalid prepared SELECT query, where the prepared query is sent to the server separate from the data, that is invalid (ie, will return an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>13</td>
        <td>Execute a prepared valid INSERT query</td>
        <td>Run a valid prepared INSERT query, where the prepared query is sent to the server separate from the data, and ensure that the database is modified accordingly</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>14</td>
        <td>Execute a prepared invalid INSERT query</td>
        <td>Run an invalid prepared INSERT query (ie, will return an error from the database), where the prepared query is sent to the server separate from the data, and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    </tr>
        <tr>
        <td>15</td>
        <td>Interrupting the Service</td>
        <td>Ensure that the service can be interrupted that it can be easily terminated and handles that termination gracefully.</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>16</td>
        <td>Using Promise Wrappers that Resolve Successfully for SELECT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a SELECT query that resolves successfully (ie, does not return an error from the database) and ensure that the returned results are as expected</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>17</td>
        <td>Using Promise Wrappers that Does not Resolve Successfully for SELECT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a SELECT query that does not resolve successfully (ie, returns an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>18</td>
        <td>Using Promise Wrappers that Resolve Successfully for INSERT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a INSERT query that resolves successfully (ie, does not return an error from the database) and ensure that the database is modified accordingly</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>19</td>
        <td>Using Promise Wrappers that Does not Resolve Successfully for INSERT queries</td>
        <td>Ensure that the service is able to handle promise wrappers for a INSERT query that that does not resolve successfully (ie, returns an error from the database) and ensure that the service can handle this error gracefully</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>20</td>
        <td>Ensuring that the Provided Documentation for the Service is Sufficient</td>
        <td>Ensure that a user with no knowledge of the product does not have difficulty with comprehending and following the instructions that are provided in the documentation for the service</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>21</td>
        <td>Using Connection Pools</td>
        <td>Ensure that the service is able to utilize connection pools that are provided by MYSQL2 for better latency of queries</td>
        <td>Low</td>
    </tr>
    <tr>
        <td>22</td>
        <td>Using Whitelist Protection for Query Parts</td>
        <td>Ensure that the service can work with a whitelist of SQL query parts to protect against SQL injection</td>
        <td>Low</td>
    </tr>
    <tr>
        <td>23</td>
        <td>Run Multithreads of Queries</td>
        <td>Setting up multiple remote hosts to use the service to query the database, and ensuring that the service can handle this.</td>
        <td>Low</td>
    </tr>
    <tr>
        <td>24</td>
        <td>Run Multithreads of Queries as a Performance Test</td>
        <td>Gradually increasing the number of queries being run by the service to test the performance capabilities of the service.</td>
        <td>Low</td>
    </tr>
        <tr>
        <td>25</td>
        <td>Running Queries above the Established Performance Benchmark</td>
        <td>Ensuring that the service can either gracefully terminate or queue queries that are being sent to it if it is being sent more queries than it can handle.</td>
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
        <td>1</td>
        <td>Installing the Service</td>
        <td>Ensure that the service can be easily installed in several widely-used operating systems.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>2</td>
        <td>Consuming a Well-formatted CSV File with some Data Values</td>
        <td>Ensure that the service can consume a well-formatted CSV file with some values</td>
        <td>High</td>
    </tr>
    <tr>
        <td>3</td>
        <td>Consuming a Well-formatted CSV File with no Data Values</td>
        <td>Ensure that the service can consume a well-formatted CSV file that has no data values</td>
        <td>High</td>
    </tr>
    <tr>
        <td>4</td>
        <td>Consuming a Wrongly-Formatted CSV File</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with the wrong-format (ie, with additional data values that don't correspond to certain columns) and returns a useful error to the user.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>5</td>
        <td>Consuming a CSV File that has Invalid Data</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with invalid data (ie, invalid date values in a date column) and returns a useful error to the user.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>6</td>
        <td>Consuming a CSV File that has Quoted Data</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with quoted data.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>7</td>
        <td>Consuming a CSV File that has a Combination of Quoted and Unquoted Data</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with a combination of quoted and unquoted data.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>8</td>
        <td>Consuming a CSV File that has Quoted Data with Embedded Commas</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with quoted data that contains commas.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>9</td>
        <td>Consuming a CSV File that has Quoted Data with Embedded Quotes</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with quoted data that contain embedded quotes.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>10</td>
        <td>Consuming a CSV File that has Quoted Data with Embedded Newlines</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with quoted data that contain the newline character.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>11</td>
        <td>Distinguishing Between Empty String and Nulls</td>
        <td>Ensure that the service can distinguish between an empty string and a null if required (ie, by the specific column or at a configuration level).</td>
        <td>High</td>
    </tr>
    <tr>
        <td>12</td>
        <td>Consuming a CSV File that has Trailing Blank Lines</td>
        <td>Ensure that the service gracefully handles consuming a CSV file with trailing blank lines.</td>
        <td>High</td>
    </tr>
    <tr>
        <td>13</td>
        <td>Consuming a file that is not a CSV File</td>
        <td>Ensure that the service gracefully handles consuming a file that is not a CSV file and returns a useful error to the user.</td>
        <td>Medium</td>
    </tr>
    </tr>
        <tr>
        <td>14</td>
        <td>Interrupting the Service</td>
        <td>Ensure that the service can be interrupted while it is consuming a CSV file, that it can be easily terminated and handles that termination gracefully.</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>15</td>
        <td>Consuming a Well-formatted CSV File with a very large Number of Data Values</td>
        <td>Ensure that the service can consume a well-formatted CSV file that has a very large number of data values, with an appropriate indicator to the user if the service is still processing the file that has been provided, and good error handling if the service times out.</td>
        <td>Medium</td>
    </tr>
        <tr>
        <td>16</td>
        <td>Modifying a Configurable Timeout Value</td>
        <td>Ensure that the service has a configurable timeout value, and that the configured value does effectively alter the service time out time, and that it times out gracefully.</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>17</td>
        <td>Handling a Well-formatted CSV File with a CSV Injection of Malicious Code</td>
        <td>Ensure that the service can identify and reject a CSV file that has a CSV injection, with that rejection being handled gracefully.</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>18</td>
        <td>Ensuring that the Provided Documentation for the Service is Sufficient</td>
        <td>Ensure that a user with no knowledge of the product does not have difficulty with comprehending and following the instructions that are provided in the documentation for the service</td>
        <td>Medium</td>
    </tr>
    <tr>
        <td>19</td>
        <td>Ensuring Multi-threading Works for the Service</td>
        <td>Ensure that the service can be multi-threaded for multiple CSVs to be processed at once.</td>
        <td>Low</td>
    </tr>
</table>


Case 3
====================

* Mathematically, no. To round a number up:
    * If the number to the right of the place value being rounded to is between 0 and 4 (inclusive), then the number in the place value being rounded to stays the same while all numbers to the right of the place value being rounded to are made 0.
    * If the number to the right of the place value being rounded to is between 5 and 9 (inclusive), then the number in the place value being rounded to is increased by 1 while all numbers to the right of the place value being rounded to are made 0.
* However, there are other considerations too, including rounding-rules and numerical accuracy.