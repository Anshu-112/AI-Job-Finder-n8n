# AI Job Finder – AI-Powered Job Discovery & Matching Automation

## Overview
AI Job Finder is an automated job discovery and matching system built using n8n, Google Gemini, and the Adzuna API. It retrieves job listings, filters relevant opportunities, evaluates them against a candidate's technical profile using an LLM, and sends job notifications through Gmail.

## Problem Statement
Job seekers often spend significant time manually searching multiple job portals and checking whether opportunities match their skills, experience, and preferred location.

## Objectives
- Automate job discovery using an external job API.
- Filter listings based on job roles and location.
- Use an LLM to evaluate candidate-job compatibility.
- Assign a match score and assess fresher eligibility.
- Store evaluated opportunities in Google Sheets.
- Send automated email notifications.

## Tech Stack
- **Automation:** n8n
- **LLM:** Google Gemini
- **Job Data:** Adzuna API
- **Programming:** JavaScript
- **Database/Storage:** Google Sheets
- **Notifications:** Gmail

## Workflow
1. Schedule Trigger starts the workflow daily.
2. HTTP Request retrieves job listings from Adzuna.
3. JavaScript normalizes the API response.
4. Duplicate jobs are removed using job URLs.
5. IF nodes filter jobs by role and location.
6. Gemini evaluates job relevance and fresher eligibility.
7. JavaScript parses the LLM response and calculates the structured result.
8. Google Sheets stores the evaluated jobs.
9. Gmail sends job notifications.

## AI Evaluation Criteria
- Technical skills match
- Fresher eligibility
- Experience requirements
- Location relevance
- Missing skills
- Overall match score
- Apply / Skip / Review recommendation

## Future Improvements
- Prevent duplicate email notifications.
- Support multiple candidate profiles.
- Add more job sources.
- Generate a consolidated daily job digest.
- Improve error handling and retry mechanisms.

## Note
This project is an internship-level automation MVP. AI-generated match scores are recommendations and should be verified against the original job listing.
