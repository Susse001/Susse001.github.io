---
excerpt: Full-stack distributed simulation of a procedural galactic
  economy featuring autonomous AI traders, dynamic markets, and
  cloud-native deployment on AWS.
layout: default
tech:
- Java
- Spring Boot
- React
- TypeScript
- PostgreSQL
- Docker
- AWS
- GitHub Actions
- REST APIs
title: Galaxy Trade Simulator
---

# Galaxy Trade Simulator

A full-stack simulation platform built with Spring Boot and React that
models a living galactic economy. Autonomous traders analyze regional
markets, purchase commodities, travel between procedurally generated
star systems, and attempt to maximize profit as market conditions
continuously evolve.

The project emphasizes backend architecture, simulation design, cloud
deployment, and scalable system organization rather than game mechanics
or graphics.

------------------------------------------------------------------------

## Overview

Galaxy Trade Simulator explores how complex simulation systems can be
built using production-oriented backend practices. The backend owns all
economic and simulation logic while the frontend visualizes the current
state of the galaxy in real time.

The application combines procedural content generation, autonomous
decision making, dynamic market simulation, and modern DevOps practices
into a cohesive distributed application deployed on AWS.

------------------------------------------------------------------------

## Core Features

### Procedural galaxy generation

-   Automatically generates a galaxy of uniquely positioned star systems
-   Assigns each system to regional economic zones
-   Seeds regional commodity markets during initialization

### Autonomous trader simulation

-   AI-controlled traders continuously search for profitable trade
    routes
-   State-machine driven trading lifecycle including travel, purchasing,
    and selling
-   Strategy profiles support different trading behaviors

### Dynamic economy

-   Independent market for every commodity within every star system
-   Prices fluctuate based on local supply and demand
-   Regional specialization influences commodity availability and
    pricing

### Interactive visualization

-   React-based galaxy map displaying systems and trader locations
-   Trade route visualization
-   Detailed system and trader information panels

------------------------------------------------------------------------

## Technical Implementation

### Backend architecture

-   Domain-driven package organization (Controller → Service →
    Repository)
-   Clear separation between entities and API DTOs
-   Business logic centralized within simulation services
-   Spring Data JPA with PostgreSQL persistence

### Simulation engine

-   Tick-based simulation updates market conditions and trader behavior
-   Modular services handle market updates, trader decisions, and travel
    calculations
-   Opportunity scoring determines optimal trade routes for autonomous
    traders

### Frontend architecture

-   React with TypeScript and Vite
-   Component-based rendering with minimal business logic
-   Backend state consumed through REST APIs
-   Shared utility modules for rendering and travel interpolation

### Cloud deployment

-   Fully containerized using Docker and Docker Compose
-   Automated CI/CD pipeline with GitHub Actions
-   Images published to Amazon ECR
-   Production deployment on AWS EC2
-   Secure GitHub-to-AWS authentication using OpenID Connect (OIDC) and
    IAM roles

------------------------------------------------------------------------

## Concepts Demonstrated

-   Full-stack application architecture
-   Simulation engine design
-   Autonomous AI agent behavior
-   Object-oriented domain modeling
-   REST API development
-   PostgreSQL data modeling with Spring Data JPA
-   React and TypeScript frontend development
-   Docker containerization
-   AWS cloud deployment
-   Continuous Integration and Continuous Deployment (CI/CD)
-   Infrastructure security using IAM and OpenID Connect (OIDC)

------------------------------------------------------------------------

## Future Development

Planned enhancements include:

-   Commodity production and consumption chains
-   More sophisticated trader decision algorithms
-   Regional economic specialization
-   Live simulation updates and analytics
-   Monitoring and observability
-   HTTPS, health checks, and production infrastructure improvements

The architecture has been intentionally designed to allow new economic
systems and simulation mechanics to be introduced incrementally without
requiring major structural changes.
