# AI LeadGen Automation

An AI-powered local-business lead generation and data-processing workflow built for a real client use case.

## Overview

This project automates a local-business lead generation workflow from business/service requirements and target locations through AI processing, Google Maps data collection, data extraction, duplicate detection, cleanup, and structured storage.

The system combines AI, workflow automation, API integration, web data extraction, batch processing, and data quality management into a single automation pipeline.

## Problem

Finding local businesses manually can require repetitive research across multiple cities and service categories.

The process can involve:

- Searching for businesses across different locations
- Repeating the same research for multiple cities
- Organizing business information consistently
- Processing large amounts of scraped data
- Checking existing records for duplicates
- Cleaning lead data before storing it

Without automation, these steps can become time-consuming and difficult to manage consistently.

## Solution

The workflow automates the lead-generation process from initial requirements through structured business-data storage.

The automation combines Google Gemini, n8n, Bright Data, Google Maps data, REST APIs, and Google Sheets to process requirements, collect business information, handle batches, detect duplicates, and maintain a cleaner lead database.

## Architecture

Form Submission
      ↓
Google Gemini
      ↓
City / Service Processing
      ↓
Separate Data by City
      ↓
Batch Processing
      ↓
Bright Data Google Maps Scraper
      ↓
Scraping Job Status Check
      ↓
Polling / Wait
      ↓
Fetch Scraped Data
      ↓
Business Data Extraction
      ↓
Existing Data Check
      ↓
Duplicate Detection
      ↓
Duplicate Processing
      ↓
Data Cleaning
      ↓
Google Sheets
Yes. **Replace the entire current `README.md` with this single block from top to bottom.** No separate pieces, no extra sections afterward.

# AI LeadGen Automation

An AI-powered local-business lead generation and data-processing workflow built for a real client use case.

## Overview

This project automates a local-business lead generation workflow from business/service requirements and target locations through AI processing, Google Maps data collection, data extraction, duplicate detection, cleanup, and structured storage.

The system combines AI, workflow automation, API integration, web data extraction, batch processing, and data quality management into a single automation pipeline.

## Problem

Finding local businesses manually can require repetitive research across multiple cities and service categories.

The process can involve:

- Searching for businesses across different locations
- Repeating the same research for multiple cities
- Organizing business information consistently
- Processing large amounts of scraped data
- Checking existing records for duplicates
- Cleaning lead data before storing it

Without automation, these steps can become time-consuming and difficult to manage consistently.

## Solution

The workflow automates the lead-generation process from initial requirements through structured business-data storage.

The automation combines Google Gemini, n8n, Bright Data, Google Maps data, REST APIs, and Google Sheets to process requirements, collect business information, handle batches, detect duplicates, and maintain a cleaner lead database.

## Architecture

Form Submission
      ↓
Google Gemini
      ↓
City / Service Processing
      ↓
Separate Data by City
      ↓
Batch Processing
      ↓
Bright Data Google Maps Scraper
      ↓
Scraping Job Status Check
      ↓
Polling / Wait
      ↓
Fetch Scraped Data
      ↓
Business Data Extraction
      ↓
Existing Data Check
      ↓
Duplicate Detection
      ↓
Duplicate Processing
      ↓
Data Cleaning
      ↓
Google Sheets

## How It Works

### 1. Input

The workflow begins with a form submission containing the required business or service information and target locations.

### 2. AI Processing

Google Gemini processes the submitted requirements and generates or normalizes the required city and service information.

### 3. City Processing

The workflow separates the generated location data so individual cities can be processed systematically.

### 4. Batch Processing

Cities are processed in batches to organize the workflow and manage multiple locations through the automation.

### 5. Data Collection

Bright Data is used to collect Google Maps business information based on the processed service and location requirements.

### 6. Scraping Job Polling

Because the external scraping process is asynchronous, the workflow checks the scraping job status and waits for the required data to become available.

### 7. Data Retrieval & Extraction

Once the scraping job is ready, the workflow retrieves the results and extracts business information into structured lead records.

### 8. Duplicate Detection

Existing business data is checked and duplicate records are identified for further processing.

### 9. Data Cleaning

Duplicate entries are processed and unnecessary duplicate rows can be removed to maintain cleaner downstream records.

### 10. Storage

The processed business information is stored in Google Sheets as a structured lead database.

## Business Data Collected

The workflow can process available business information such as:

* Business name
* Business category
* Rating
* Number of reviews
* Phone number
* Website
* Address
* Google Maps URL
* Other available business information from the scraping result
## Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Google Gemini | AI processing |
| Bright Data | Google Maps data collection |
| REST APIs | External service integration |
| Webhooks / HTTP | Workflow communication |
| Google Sheets | Lead data storage |
| JavaScript | Data transformation |

## Key Automation Features

* AI-assisted location and service processing
* Automated Google Maps business discovery
* Batch processing across multiple cities
* API-based scraping workflow
* Asynchronous scraping-job status polling
* Structured business-data extraction
* Existing-data checking
* Duplicate detection and processing
* Data cleaning
* Google Sheets integration
* End-to-end workflow orchestration
* Reduced manual lead research

## Challenges & Engineering Decisions

Building the workflow involved several practical engineering challenges.

### Asynchronous Scraping Jobs

The Bright Data scraping process does not necessarily return the final dataset immediately. The workflow therefore uses job-status checking and polling logic before retrieving the completed data.

### Batch Processing

Multiple cities need to be processed systematically. Batch processing was used to organize location-based execution and manage the workflow more reliably.

### Data Flow Between Workflow Branches

Passing the correct data between different workflow branches required careful handling of intermediate results and downstream processing.

### Duplicate Records

Scraped business data can contain records that already exist in the destination dataset. The workflow therefore checks existing records and processes potential duplicates before final storage.

### Data Quality

Downstream Google Sheets records need to remain structured and usable. Data transformation and duplicate handling are used to improve the quality of the final dataset.

### API Response Handling

External API responses must be interpreted and transformed before they can be used by later workflow stages.

## Current Status

**Core automation workflow is built and functional, with ongoing refinement of data-processing and downstream record handling.**

The workflow has successfully demonstrated business-data extraction and the overall lead-generation pipeline, while some downstream data-flow and record-processing behavior continues to be refined.

## Portfolio Evidence

Screenshots included in this repository may demonstrate:

* n8n workflow architecture
* AI processing stages
* Bright Data API integration
* Google Maps data collection
* Batch processing
* Data extraction
* Duplicate detection and cleanup
* Google Sheets output

All portfolio evidence should use sanitized or sample data.

## Security & Privacy

This repository is a sanitized portfolio representation of a client automation.

The repository must not contain:

* API keys
* API tokens
* Client credentials
* Google OAuth credentials
* Private client information
* Real client lead databases
* Personal phone numbers
* Personal email addresses
* Private Google Sheets
* Private n8n credentials
* Bright Data credentials
* Webhook secrets

Client-specific implementation details and credentials are intentionally excluded.

## What This Project Demonstrates

This project demonstrates practical experience in:

* AI automation
* n8n workflow engineering
* LLM integration
* API integration
* Web data extraction
* Batch processing
* Data transformation
* Data quality management
* Duplicate detection
* Google Workspace automation
* Business process automation

## Limitations

The public repository documents the architecture, engineering approach, and portfolio evidence rather than exposing the private client implementation.

No specific total number of leads generated is claimed because the downstream system is still undergoing refinement.

## Future Improvements

Potential improvements include:

* More robust error handling
* Improved scraping-job monitoring
* Stronger data validation
* More advanced duplicate matching
* Improved downstream data processing
* Additional lead-database integrations
* Workflow monitoring and reporting

