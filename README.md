# Real-Time-Sales-Data-Analysis-Application
A real-time sales data analysis Application using Spark Structured Streaming, Kafka as a messaging system, PostgreSQL as a storage for processed data, and Superset for creating a dashboard.

## Project Description
Mya Gon Yaung is a men's traditional clothing retail shop that manually records everything in a book. Since sales are only written in a book, it is easy to find daily sales but difficult to know monthly or yearly sales. As a result, the shop owners do not know their monthly and yearly sales, what products are sold most in which month, and which stocks need to be refilled and which don't. As they don't know the answers to these questions, they often overstock or understock many products which greatly affects their profits.

This project is used to find out whether having a real-time sales data analysis application will be a solution to solve the problems faced at Mya Gon Yaung.



![image](https://github.com/user-attachments/assets/2e045846-fad4-48f8-b126-2dde89aa2ecb)



The Data Platform Architecture of the Real-Time Sales Data Analysis Application is designed to provide a streamlined and efficient process for handling sales data from its inception to real-time analytics. Customer purchase information is initially generated and transmitted through a Kafka producer, which then sends the data to a designated Kafka topic. Subsequently, an Apache Spark streaming application processes the data, extracting pertinent information and transforming it for further analysis. The processed data finds a reliable home in a PostgreSQL database, offering structured storage. 

Finally, the stored data is leveraged to create live dashboards using Apache Superset, enabling real-time analytics and visualization of key metrics. This architecture ensures a seamless and comprehensive flow of data, empowering the application to deliver timely insights into sales trends and inventory management.


## Project Workflow

### 1. Data Source

To simulate product checkouts, a Kaggle [sales dataset](https://www.kaggle.com/datasets/knightbearr/sales-product-data) is utilized in the Kafka Producer.

### 2. Data Preparation

The Kaggle dataset undergoes cleaning and column trimming to ensure data quality. Two primary datasets are prepared: Sales Data and Stock Quantity Data.

#### Sample Data:

![image](https://github.com/user-attachments/assets/0bbdb6cf-3e7a-45ca-b57a-4ae6308c02a3)


![image](https://github.com/user-attachments/assets/db16dfb4-607f-4b97-b66a-32ed3262da22)


### 3. Data Producer

A dedicated Kafka Producer streams sales data to the "sales" topic in Kafka, ensuring a reliable and real-time data flow.

### 4. Data Storage

A Python script creates a PostgreSQL database and tables for storing processed data, providing a structured storage solution.

### 5. Spark Structured Streaming

A Python script handles data ingestion, processing, and storage from the "sales" Kafka topic into PostgreSQL. It includes steps such as streaming data from Kafka using Spark, transforming data, and aggregating results in PostgreSQL.

### 6. Data Visualization with Apache Superset

The stored data in PostgreSQL is leveraged to build live dashboards using Apache Superset. This step enables real-time analytics and visualization of key metrics derived from the processed data.

This organized structure provides a clear understanding of the project, its architecture, and the detailed workflow. Contributors and users can easily navigate and comprehend the different components and steps involved in the Real-Time Sales Data Analysis Application.


## Prerequisites

Ensure that you have the following prerequisites installed on your system:

- Apache Spark
- Apache Kafka
- PostgreSQL
- Apache Superset
- Python (3.6 or higher)

## Dashboard Demo

Check out a brief demo of the Real-Time Sales Data Analysis Application dashboard:

[Images/real-time-dashboard.mp4](https://github.com/alaahgag/Real-Time-Sales-Data-Analysis-Application/assets/101465586/00d5e50c-1a91-434e-b178-bc40b1c17e93)

    
## Conclusion

The Real-Time Sales Data Analysis Application is a robust solution designed to address the challenges faced by Mya Gon Yaung, a traditional men's clothing retail shop. By leveraging the power of Spark Structured Streaming, Kafka, PostgreSQL, and Apache Superset, the application provides a seamless and efficient pipeline for processing, analyzing, and visualizing sales data in real-time.

### Key Achievements

- **Real-Time Analytics:** The application enables real-time analytics, allowing Mya Gon Yaung to monitor sales trends, identify popular products, and make informed decisions promptly.
  
- **Inventory Optimization:** By integrating with Spark Structured Streaming, the shop can now optimize inventory management, reducing instances of overstocking or understocking and ultimately improving profitability.

- **User-Friendly Dashboards:** The use of Apache Superset facilitates the creation of user-friendly dashboards, empowering shop owners to gain insights into their business without the need for complex queries or data analysis.

### Future Enhancements

While the Real-Time Sales Data Analysis Application has achieved significant milestones, continuous improvement is essential. Future enhancements may include:

- **Machine Learning Integration:** Incorporating machine learning models for predictive analytics, helping forecast sales trends and further refine inventory management.

- **Extended Data Sources:** Integrating additional data sources beyond sales data, such as customer feedback or external market trends, to provide a more comprehensive analysis.

- **Scalability:** Ensuring the application is scalable to accommodate the growth of Mya Gon Yaung or similar businesses.


