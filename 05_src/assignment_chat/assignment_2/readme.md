#Assignment 2

## Overview

This AI system with a conversational interface is to provide users with engaging and informative interactions through 3main services: 1. a weather assistant, 2. a book recommendation system, and 3. a job trivia service.  Gradio is being used and a few APIs, the chat client offers a user-friendly interface that allows users to obtain real-time information, recommendations, and trivia questions in a conversational format.

## Services

### 1. WeatherBot

Functionality:
The WeatherBot, users enter a city name and receive current weather information. The bot fetches data from the WeatherStack API, including temperature, weather conditions, and other relevant metrics.

**Implementation Decisions:**  
- **Restricted Topics:** The WeatherBot checks for restricted topics to ensure compliance with guidelines.
- **Default Location:** If the user does not provide a location, the WeatherBot defaults to Toronto.

### 2. Book Recommendation System

**Functionality:**  
This service utilizes Langchain and ChromaDB to return book recommendations based on user queries. Users type in a book-related query and receive suggestions from a pre-populated collection of popular English literature.

**Implementation Decisions:**  
- **Embedding Function:** The service uses OpenAI's embedding functions for effective querying of the book database.
- **Pre-Population of Database:** A predefined list of books is included to ensure efficient access to book recommendations.

### 3. Job Skills Trivia Service

**Functionality:**  
The Job Skills Trivia service provides random trivia about various jobs, including their titles and associated skill requirements. It fetches data from the Data at Work API.

**Implementation Decisions:**  
- **Guardrails:** Similar to the WeatherBot, this service also checks for restricted topics to maintain compliance.
- **Random Job Fact:** The trivia includes a random job fact generated on each request, aiming to engage users in a fun manner.

## Technical Details

- The project relies on several libraries, including Gradio, OpenAI SDK, Langchain, and requests for API interactions.
- Environment variables are loaded using `dotenv` to safely manage API keys and sensitive information.
- The application is structured to ensure ease of maintenance with modular function definitions for each service.
