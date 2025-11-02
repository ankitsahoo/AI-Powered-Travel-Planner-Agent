# AI-Powered-Travel-Planner-Agent

# Screenshot of the application
<img width="2797" height="1504" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/21b4b3da-9aef-4154-b3b2-fb899264e9b4" />

# Overview:
The AI-Powered Travel Planner is an interactive web application that helps users plan personalized trips effortlessly. It leverages AI agents, real-time flight and hotel search APIs, and user preferences to generate a complete travel itinerary, including flights, accommodations, activities, and recommendations tailored to the user’s travel style.

# Key Features:
- Personalized Trip Planning: Users can input departure and destination cities, trip duration, travel theme, and preferred activities.
- Flight Search & Recommendations: Fetches top flight options from Google Flights via SerpApi and ranks the cheapest or most suitable flights.
- AI Research on Destination: AI agents gather destination-specific details like attractions, culture, safety tips, and activities based on user preferences.
- Hotel & Restaurant Recommendations: AI agents suggest hotels and restaurants matching budget, rating, and proximity to attractions.
- Custom Itinerary Generation: The planner AI creates a detailed day-by-day itinerary integrating flights, accommodations, and activities.
- Interactive UI with Streamlit: Users can visualize flights, hotels, and itinerary with a clean, intuitive interface.
- Sidebar Features: Travel essentials, packing checklist, visa requirements, travel insurance, and currency converter options.


# Tech Stack Used

**Frontend:**
**Streamlit:** Interactive web application framework for Python. Provides sliders, input fields, and layout customization.
**HTML/CSS:** Custom styling embedded in Streamlit for improved UI/UX.

**Backend & AI:**
**Python 3.x:** Core programming language for logic and API integration.
**Gemini AI Model:** AI agents (Researcher, Planner, Hotel & Restaurant Finder) generate insights, recommendations, and itineraries.
**Agno Framework:** Orchestrates AI agent creation, instructions, and execution.

**APIs & Data Sources:**
**SerpApi (Google Flights API):** Real-time flight search and booking data.
**Google APIs:** Optional key usage for extended Google services.

**Others:**
**Datetime module:** For date formatting and schedule calculations.
**JSON & OS modules:** For API handling and environment variable management.

### AI Travel Planner Workflow

```plaintext
User Input
(Departure, Destination, Dates, Preferences)
        |
        v
+--------------------+
| Flight Search      | <-- SerpApi + Google Flights
+--------------------+
        |
        v
+--------------------+
| AI Research Agent  | <-- Gemini AI
| (Destination Info) |
+--------------------+
        |
        v
+-------------------------------+
| Hotel & Restaurant Agent      | <-- Gemini AI + SerpApi
+-------------------------------+
        |
        v
+----------------------------+
| Planner Agent              | <-- Gemini AI
| Generates Itinerary        |
+----------------------------+
        |
        v
+----------------------------+
| Streamlit UI               |
| Displays Flights, Hotels,  |
| Restaurants, and Itinerary |
+----------------------------+


################ Explanation of Workflow:######################
- User enters travel details and preferences in the Streamlit frontend.
- Flight data is fetched via SerpApi's Google Flights API.
- AI “Researcher” agent gathers destination information and activity recommendations.
- AI “Hotel & Restaurant Finder” agent identifies suitable accommodations and dining options.
- AI “Planner” agent compiles all data to generate a personalized itinerary.
- Streamlit UI presents the results visually, including flight cards, hotel lists, and a day-by-day itinerary.


