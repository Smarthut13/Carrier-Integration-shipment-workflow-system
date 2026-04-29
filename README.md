# Carrier Integration & Shipment Workflow Backend System

A Java Spring Boot backend project that simulates transportation carrier integration, shipment creation, carrier selection, shipping label generation, electronic manifest creation, and invoice validation.

This project is designed around real-world logistics and transportation technology workflows.

## Tech Stack

- Java
- Spring Boot
- MySQL
- REST APIs
- Object-Oriented Programming
- Data Structures
- Exception Handling
- Logging
- Linux basics

## Key Features

- Create and manage shipments
- Select carriers based on cost, serviceability, delivery speed, and shipment type
- Generate shipping labels
- Create electronic carrier manifests
- Validate carrier invoices against expected shipment cost
- Track shipment status
- Handle exceptions and operational failures
- Maintain structured logs for debugging and root cause analysis

## Core Modules

### 1. Shipment Management
Creates shipment records with customer, package, destination, and delivery details.

### 2. Carrier Selection
Selects the best carrier based on:
- Delivery speed
- Shipment weight
- Destination serviceability
- Cost
- Service level

### 3. Shipping Label Generation
Generates a label response containing:
- Shipment ID
- Carrier name
- Tracking number
- Origin
- Destination
- Service type

### 4. Electronic Manifest
Groups shipments by carrier and shipping date for carrier handoff.

### 5. Invoice Validation
Compares carrier invoice amount with expected shipping cost and flags mismatches.

## Sample API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | /api/shipments | Create shipment |
| GET | /api/shipments/{id} | Get shipment details |
| POST | /api/carriers/select | Select best carrier |
| POST | /api/labels/generate | Generate shipping label |
| POST | /api/manifests/create | Create carrier manifest |
| POST | /api/invoices/validate | Validate carrier invoice |
| PUT | /api/shipments/{id}/status | Update shipment status |

## Database Tables

- shipments
- carriers
- shipping_labels
- manifests
- manifest_shipments
- invoices

## Example Shipment Request

```json
{
  "customerName": "Hutchinson Martin",
  "originCity": "Hyderabad",
  "destinationCity": "Bangalore",
  "packageWeight": 2.5,
  "shipmentType": "STANDARD",
  "deliverySpeed": "TWO_DAY"
}
