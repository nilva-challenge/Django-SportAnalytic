# In the Name of Allah

## Introduction

Welcome to the challenge for building a Sports Analytics Platform! In this task, you will create a backend service that integrates with an existing sports API to retrieve and analyze fixtures. The goal is to provide insightful analytics and summaries that can help users understand trends and performance over a period of time.

This challenge is designed to test your skills in backend development, data analysis, and integration with external services using Django. Additionally, you'll implement caching with Redis to enhance performance and provide a fallback mechanism using a database cache to ensure reliability. You'll be working on creating endpoints that not only retrieve data but also process and analyze it to generate valuable insights. This platform can serve as a tool for sports enthusiasts, analysts, and teams to make data-driven decisions.

By the end of this challenge, you should have a robust backend system capable of fetching, storing, and analyzing sports fixtures data, along with providing comprehensive summaries and insights through well-documented API endpoints. Your focus should be on clean, readable, and maintainable code with proper error handling and data validation.

### Key Features:
- Integration with a sports API to retrieve fixtures
- Storage and analysis of fixture data over a specified date range
- Caching with Redis to improve performance and fallback mechanism using a database cache (advanced)
- Generation of summaries and insights based on the collected data
- Providing API documentation and ensuring code quality

### Note
We do NOT want any kind of UI from you

## Expectations:

We want clean, readable, and maintainable code with meaningful comments and docstrings. Also, you need to provide Postman API documentation for the web app.

1. Fork this repository
2. Develop the challenge with Django 3 or higher
3. Push your code to your repository
4. Send us a pull request, we will review and get back to you
5. Enjoy

## Detailed Requirements:

### API Endpoints:

- GET /analytics/summary/?start=\<YYYY-MM-dd\>&end=\<YYYY-MM-dd\>: Retrieve a summary of analytics for a specified date range (fields: start_date, end_date), summary is:
  - Total number of games played
  - Average goals scored per game
  - Win/loss ratios for teams
- GET /analytics/top-teams/?start=\<YYYY-MM-dd\>&end=\<YYYY-MM-dd\>: Retrieve the 5 top teams based on each metric over a specified date range (fields: start_date, end_date, metric)

### Data Extraction and Storage:

Integrate with the external sports API to retrieve fixture data for specific dates.
API url is [https://core-sport-api.zarebin.ir/api/football/fixtures/?date=YYYY-MM-dd](https://core-sport-api.zarebin.ir/api/football/fixtures/?date=YYYY-MM-dd).
Store the retrieved data in the database for analysis.
Cache fixture data using Redis for faster subsequent retrieval and implement a fallback mechanism to use database cache if Redis is unavailable.

### Analytics and Insights:

Analyze the stored fixture data to generate summaries, such as:
- Total number of games played
- Average goals scored per game
- Win/loss ratios for teams
Identify and retrieve the top teams based on each metric.

### Caching with Redis:

Use Redis to cache fixture data responses to improve performance.
Implement a fallback mechanism to retrieve data from the database cache if Redis fails. (advanced)

\***note** that advanced marked features are not necessary to implement, they are considered extra points.\*

### Error Handling:

Return appropriate HTTP status codes for errors (e.g., 400 for bad requests, 404 for not found).
Include error messages in the response body.
