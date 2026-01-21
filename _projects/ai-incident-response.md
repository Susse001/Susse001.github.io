---
layout: default
title: AI-Powered Incident Response System
excerpt: Spring Boot application leveraging AI to enrich, classify, and assist with incident response workflows.
tech:
  - Java
  - AWS DynamoDB
  - AI / LLM Integration
  - REST APIs
  - Asynchronous Processing
  - Cloud Deployment
github: https://github.com/Susse001/Stephenusselman.incidentreport
---

## AI-Powered Incident Response System

A production-style backend service built with Spring Boot that manages incident reports and enriches them using AI-generated analysis.
The system is designed to mirror real-world incident response workflows by highlighting severity, categorization, summaries, and recommended remediation steps.

---

## Overview

This project explores how AI can be safely integrated into backend systems to augment—not replace—core business logic.
Incidents are persisted as structured data and asynchronously enriched with AI-generated context to support faster triage and investigation.

The application emphasizes correctness, testability, and cloud-ready architecture rather than UI concerns.

---

## Core Features

### Incident ingestion and retrieval
- Create and retrieve incidents via REST APIs
- Query incidents by severity or category
- Pagination support for large result sets using DynamoDB keys

### AI-driven enrichment pipeline
- Asynchronous AI enrichment triggered after incident creation
- AI-generated summaries, classifications, and remediation suggestions
- AI failures do not block persistence or API responses

### DynamoDB data modeling
- Single-table design with Global Secondary Indexes (GSIs)
- Efficient indexed queries by severity and category
- Clear separation between domain models and API response DTOs

### Production-oriented design
- Environment-specific configuration (local vs. production)
- Deployed on AWS Elastic Beanstalk
- Defensive handling of external AI dependencies

---

## Technical Implementation

### Backend architecture
- Layered design following Controller → Service → Repository
- DTO-based API responses to decouple persistence models from external contracts
- Use of the DynamoDB Enhanced Client for typed, strongly modeled data access

### Asynchronous processing
- AI enrichment executed independently of the request lifecycle
- Ensures low-latency incident creation and non-blocking API responses
- Asynchronous execution managed through Spring’s async facilities

### AI integration
- Prompt-based enrichment with strict JSON response expectations
- Defensive parsing and fail-fast handling of malformed AI output
- AI treated as an advisory system rather than a source of truth

### Data persistence and querying
- Single-table DynamoDB design with Global Secondary Indexes (GSIs)
- Indexed queries supported for severity- and category-based access patterns
- Pagination implemented using DynamoDB `LastEvaluatedKey`

### Testing and quality
- Unit and integration tests across service and repository layers
- JaCoCo-enforced test coverage thresholds
- Deterministic DynamoDB test data for reliable query validation

---

## Concepts Demonstrated

- Backend system design and REST API development
- Safe and defensive AI integration in production workflows
- Asynchronous execution and concurrency management
- NoSQL data modeling with indexed access patterns
- Cloud deployment and environment-specific configuration
- Test coverage enforcement and validation-driven development

---

## API Endpoints

### Base URLs

**Production**
http://incidentservice-susse-env.eba-vipmqwyp.us-east-2.elasticbeanstalk.com/api/incidents

**Local**
http://localhost:8080/api/incidents

---

### Create Incident

**POST /**

**Request**
```json
{
  "description": "Database connection timeout affecting checkout service",
  "reportedBy": "Stephen Usselman",
  "severity": "HIGH",
  "category": "DATABASE"
}
```

**Response**
```json
{
  "incidentId": "22cb7619-b777-4581-85d0-bacbfe72305a",
  "description": "Database connection timeout affecting checkout service",
  "reportedBy": "Stephen Usselman",
  "severity": "HIGH",
  "category": "DATABASE",
  "aiStatus": "PENDING",
  "createdAt": "2026-01-20T21:58:12Z"
}
```

**Response After Enrichment**
```json
{
  "incidentId": "22cb7619-b777-4581-85d0-bacbfe72305a",
  "description": "Database connection timeout affecting checkout service",
  "reportedBy": "Stephen Usselman",
  "severity": "HIGH",
  "category": "DATABASE",
  "aiStatus": "ENRICHED",
  "aiSummary": "A database outage is causing elevated latency and request failures in the checkout service.",
  "aiRemediation": "Investigate database connection pool saturation, check recent deployments, and consider scaling the database cluster.",
  "createdAt": "2026-01-20T21:58:12Z"
}
```

## Repository

[View on GitHub](https://github.com/Susse001/Stephenusselman.incidentreport)
