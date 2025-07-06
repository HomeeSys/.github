# Homee System

> A portfolio application showcasing skills in advanced backend technologies with .NET, with a focus on **microservices** and **Azure**.

## Overview

The application simulates a system for collecting data from sensors and storing it, along with the ability to generate reports.  
It manages devices capable of taking various measurements (temperature, humidity, CO₂, etc.).  
These measurements are sent by small devices deployed throughout a house.

> ℹ️ **Note:** Physical devices will not be implemented, as this would require significant additional work (microcontroller software, libraries, communication). Instead, a dedicated simulator application will emulate the behavior of such devices by periodically sending sample data.

The main goal of the project is to utilize as many technologies as possible, including:  
**Docker, Microservices, SQL Server, PostgreSQL, Azure, CosmosDB, Azure Events, RabbitMQ, gRPC, Azure Blob Storage.**  
This should serve both as a portfolio piece and as preparation for the **AZ-204** exam.

> ℹ️ **AZ-204 [Azure Developer Associate Certification](https://learn.microsoft.com/en-us/credentials/certifications/azure-developer/?practice-assessment-type=certification)** — This certification is valuable as many job postings require knowledge of **Azure**.

---

## Backend

The backend will be implemented as a set of microservices:

- **Devices**  
  Handles operations on devices in the system: registration, modification, and deletion.  
  This microservice uses its own database (**Microsoft SQL Server**) with **Entity Framework** as the ORM. Other frameworks and libraries will also be used as needed.

- **Measurements**  
  Responsible for collecting and storing measurement data from all devices.  
  This service uses **CosmosDB** as its database.

- **Reports**  
  Responsible for generating and storing reports in **PDF** format.  
  Reports are stored in **Azure Blob Storage**.

---

## Frontend

A web application is planned as the frontend, to allow testing and deployment on **Azure** and to enable browser-based interaction.  
Existing **Syncfusion** UI components will be used for a polished user interface.

> ❗**Note:** Backend technologies remain the main priority. The frontend will only be developed if time allows, and at minimum, only the essential functionality will be implemented.

Some form of **authentication** and **authorization** will also be required.

---
