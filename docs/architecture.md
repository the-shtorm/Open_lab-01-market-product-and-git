# Yandex Go

## Product Choise

> **link**: https://taxi.yandex.ru/

### Description

Yandex Go is one of the most beautiful taxi services in Russia. I love Yandex Go. Praise Yandex. Glory to the Yandex

![Yandex Go Component Diagram](./diagrams/out/yandex-go/architecture-component/Component%20Diagram.svg)
![Yandex Go Component Diagram code](./diagrams/src/yandex-go/architecture-component.puml)

> **Notification Service:**
> Service to provide notifications for users ("you cant miss this beautiful price for taxi")

> **Pricing Service:**
> Detects user interest for taxi and decide which price must be used for travel

> **Yandex Pay:** 
> Accepts payments form users (external service)

> **Yandex Map:**
> Proprietary Map service to make travels more convenient

> **Mobile App:** special app for 

## Data flow

![Yandex Go Sequence Diagram](./diagrams/out/yandex-go/architecture-sequence/Sequence%20Diagram.svg)

![Yandex Go Sequence Diagram code](./diagrams/src/yandex-go/architecture-sequence.puml)

### Group group #F9F9F9 1. App Initialization & Auth

#### Steps

- user goes to app and opens app
- App activates Gateway
- User session created
- User data caches
- User session deleted
- Authentification
- Gateway closes

#### Excange data

- Validation token 
- Auth token
- Some sessinn data

## Deployment

![Yandex Go Deployment](./diagrams/out/yandex-go/architecture-deployment/Deployment%20Diagram.svg)
![Yandex Go Deployment code](./diagrams/src/yandex-go/architecture-deployment.puml)

### Deployment Components

Main components were deployed into Kubernetes Cluster
External components deployed into other special clusters

## Assumptions

Yandex maps are used to create routes for taxi and manages routes depending on traffic and etc.

Routing Service parse data from Yandex maps to create safe routes for taxi

## Open questions

How pricing service decides actual price for taxi travel
What info caches by cache service for quick access 