# Task 3: Multi-Cloud Architecture – Google Cloud & AWS

## Objective
To design a multi-cloud architecture that distributes application services across two cloud providers — Google Cloud Platform (GCP) and Amazon Web Services (AWS) — demonstrating interoperability, flexibility, and vendor independence.

---

## Architecture Overview

This architecture represents a basic **Blog Web App** where:

- **Frontend Layer** is hosted on **Google Cloud (GCP)**
  - App Engine or Cloud Run handles dynamic content
  - Static assets are served from **Google Cloud Storage (GCS)**

- **Backend Layer** runs on **Amazon Web Services (AWS)**
  - AWS Lambda or EC2 handles API logic
  - Data is stored in **AWS RDS (MySQL)**

Communication between the layers is done through **HTTP-based API calls**.

---

## Architecture Diagram

![Multi-Cloud Architecture Diagram](screenshots/multi-cloud-diagram.png)

*Note: This diagram illustrates the user’s request to the GCP-hosted frontend and the API call from GCP to AWS services.*

---

## Components Used

| Layer        | Service            | Platform     |
|--------------|--------------------|--------------|
| Frontend     | App Engine / Cloud Run | GCP      |
| Static Assets| Cloud Storage      | GCP          |
| Backend Logic| AWS Lambda / EC2   | AWS          |
| Database     | AWS RDS (MySQL)    | AWS          |

---

## Benefits of Multi-Cloud Approach

- **Avoids Vendor Lock-In:** Freedom to switch between providers or mix and match best tools.
- **Increased Redundancy:** Failure in one platform doesn't affect the entire system.
- **Optimized Costs & Features:** Use each platform’s strengths (e.g., GCP for scalable apps, AWS for robust backend).

---

## Potential Enhancements

- Use **API Gateway** on AWS to manage and secure API endpoints
- Enable **Cloud Monitoring** in both clouds for unified observability
- Set up **CI/CD pipelines** to deploy frontend and backend independently

---

## Screenshots
- `multi-cloud-diagram.png`: Visual representation of the architecture

---

## Notes
This architecture demonstrates interoperability between two major cloud providers and serves as a foundation for real-world scalable applications.

