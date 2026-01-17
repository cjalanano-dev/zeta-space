**Project Overview** 

IsItRaceWeek is a modern, web-based dashboard designed for Formula 1 fans to instantly check the status of the upcoming race weekend. Built with Next.js 16 and React 19, the application serves as a real-time hub that answers the primary question—"Is it race week?"—while providing detailed scheduling, countdowns, and track conditions for the next Grand Prix.

**Technical Architecture**

- **Data Integration:** The application interfaces directly with the OpenF1 API to fetch real-time data regarding race meetings, session schedules, and weather telemetry. It handles data synchronization for current and future seasons to ensure continuity between years.
    
- **Client-Side Logic:** Utilizing React's client-side hooks (`useEffect`, `useState`), the application performs asynchronous data fetching to determine the current date context, filter for upcoming events, and calculate countdown timers dynamically in the user's browser.
    
- **Responsive Design:** The UI is constructed using Tailwind CSS, implementing a mobile-first approach that adapts layouts (grids, font sizes, and spacing) across different device sizes.
    

**Key Features**

- **Race Week Status:** A prominent, boolean-logic based indicator that visually alerts users if the current date falls within a 3-day window of a race weekend start date.
    
- **Global Countdown Timer:** A dynamic timer tracking the precise time remaining until the next on-track session, automatically adjusting to the next available event (e.g., Free Practice, Qualifying, or the Race itself).
    
- **Localized Scheduling:** Displays a comprehensive schedule of all sessions (Practice 1-3, Qualifying, Sprint, Race) with start and end times automatically converted to the user's local timezone.
    
- **Event Information:** Provides detailed metadata about the current or upcoming meeting, including the official meeting name, circuit name, and location (Country/City).
    
- **Live Weather Integration:** During active race weeks, the dashboard fetches and displays weather telemetry data specific to the circuit location.
    
- **Error Handling:** Includes error states and a retry mechanism to handle API failures or network issues gracefully.
    

**Tech Stack**

- **Framework:** Next.js 16.1.1 (App Router)
    
- **UI Library:** React 19
    
- **Styling:** Tailwind CSS v4
    
- **Icons:** Lucide React
    
- **Date Management:** date-fns, date-fns-tz
    
- **External API:** OpenF1 API