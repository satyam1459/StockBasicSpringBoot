<h1 align="center"> 
Stock </h1>
The stock controller is responsible for handling stock-related operations in the application. It provides RESTful endpoints for managing stocks, such as updating stock information, retrieving stocks based on certain criteria, and deleting stocks.

>### Prerequisites
 * ![SpringBoot](https://img.shields.io/badge/Framework-SpringBoot-green)


* ![Java](https://img.shields.io/badge/Language-Java%208%20or%20higher-yellow)

>## Installation

To run this application locally, you will need to have Java and MySQL installed on your machine.

* Clone the repository to your preferred IDE.

* Update the `application.properties` file in the `src/main/resources` directory to configure H2 database
* Run the application using your IDE or by running the command `mvn spring-boot:run` in the project directory
* Access the APIs using any HTTP client such as Postman or cURL.
>## Data flow
 The application is built using the SpringBoot framework and consists of three layers: model, service, and repository.-

* **Controller** - The controller layer handles the HTTP requests, translates the JSON parameter to object, and authenticates the request and transfer it to the business (service) layer. In short, it consists of views i.e., frontend part.
* **Service** -The business layer handles all the business logic. It consists of service classes and uses services provided by data access layers.
* **Repository** - This layer mainatains the h2-database thing on which CRUD operations are performed
* **Model** - This layer consists basically the class level things- the various classes required for the project and these classes consists the attributes to be stored.

>## Key Features:
* Stock Management: The stock controller allows updating stock information, such as stock type, market capitalization, and owner count. It also provides endpoints for creating new stocks and deleting stocks based on owner count.

* Stock Retrieval: The application supports retrieving stocks based on stock type, market capitalization percentage, and criteria such as price and birth timestamp.
* H2 Database Integration: The project utilizes the H2 database as the data storage solution. The database provides an in-memory, lightweight option for storing and querying stock data.
* To run the project, make sure you have installed the JDK, Spring Boot framework, and H2 database. You can then compile and execute the project using your preferred development environment or by using command-line tools

> ## Endpoints

* PUT /stock/stock/{id}
Update stock information for a specific stock identified by its ID.
* PUT /stock/stock/type/{type}/id/{id}
* Update the stock type for a specific stock identified by its ID.
* PUT /stock/marketCap/{marketCap}/id/{id}
* Update the market capitalization value for a specific stock identified by its ID.
* POST /stock
* Create a new stock.
* GET /stock/type/{stockType}
* Retrieve stocks based on the stock type.
* GET /stock/cap/{capPercentage}
* Retrieve stocks based on the percentage of market capitalization.
* GET /stock/abovePrice/price/{price}/lowerData/date/{date}
  Retrieve stocks with a price higher than a specified value and birth timestamp lower than a specified date.
* DELETE /stock/ownerCount/{count}
Delete stocks based on the stock owner count.
>## Contributors

Satyam Jaiswal(satyam1459)

>## Project Summary
The project is a Spring Boot application with an integrated H2 database. It provides a stock controller that handles various stock-related operations. The application exposes RESTful endpoints for managing stocks, such as updating stock information, creating new stocks, retrieving stocks based on specific criteria, and deleting stocks.

This project serves as a starting point for building stock management applications with Spring Boot and H2 database. It can be extended and customized to meet specific business requirements related to stock management and analysis.
