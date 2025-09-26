# 🎬 Movie App

A React-based movie search app using the TMDb API. Built to learn and apply React fundamentals through one project — fetching and displaying popular movies, searching by title, and handling UI states.

---
##Demo Video
[(https://youtu.be/zx7zRGhmDbM)]

## 🧠 Approach & Thinking

When starting this project, I followed a deliberate structure inspired by tutorials like *TechWithTim’s “Learn React In One Project”*:

1. **Define scope / MVP features**  
   - On load, display *popular movies*  
   - Search functionality (by movie title)  
   - Show movie poster, title, rating, release date  
   - Handle loading and error states  

2. **Choose stack / tools**  
   - **Frontend**: React (functional components + hooks)  
   - **Styling**: CSS modules / plain CSS  
   - **API**: TMDb  
   - **Dev environment**: `create-react-app` or similar so live-reload works  

3. **Data flow & architecture**  
   - Separate services for API calls (`services/api.js`)  
   - Components like `MovieCard` to display individual movie cards  
   - Page component (`Home.jsx`) to manage state (movies list, loading, error, search query)  
   - Use `useEffect` to fetch popular movies on mount  
   - On search, fetch searched movies  

4. **Handling real-world issues**  
   - TMDb and some APIs are blocked in certain regions (e.g. India). So either:  
     - Use a VPN to make API calls from the browser  
     - Or plan for a backend proxy + CORS when needed  
   - Ensure good UX: show loading indicator, error messages, prevent empty searches  

5. **Iterative development & polish**  
   - Start minimal: get popular movies showing up  
   - Add search bar functionality  
   - Add error & loading state handling  
   - Style the cards and grid layout  
   - Fill gaps: fallback images if poster not available, date formatting, rating display  

---

## 📖 Project Structure

MovieApp/
├─ src/
│ ├─ components/
│ │ └─ MovieCard.jsx # Displays a single movie
│ ├─ pages/
│ │ └─ Home.jsx # Main page: search + display movies
│ ├─ services/
│ │ └─ api.js # Functions: getPopularMovies, searchMovies
│ └─ css/
│ └─ Home.css # Styles for Home page & grid
├─ public/
├─ package.json
└─ README.md
