# Data Workflow

Real-time customer data monitoring and analytics platform using Kafka and Azure services Design

graph TD
    A[User Interactions] -->|Sends Data| B(Apache Kafka)
    B -->|Triggers| C(Azure Function)
    C -->|Stores Raw Data| D[Azure Data Lake Storage Raw]
    C -->|Sends to Databricks| E(Azure Databricks)
    E -->|Processes & Enriches| F[Azure Data Lake Storage Processed]
    E -->|Real-time Analytics| G[Analytics Dashboard]
    F -->|Batch Analytics & ML| G

