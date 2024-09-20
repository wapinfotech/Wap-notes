### Task: Movie Cards React Application

**Objective:**  
Create a React application that fetches data from an API and displays it in a card-like UI.

**Instructions:**

1. **Setup the React Application:**
   - Create a new React application using `create-react-app`.
   - Set up the project structure as needed.

2. **Fetch Movie Data:**
   - Use the provided API snippet below to fetch data about the top 100 movies from IMDb.
   - Install `axios` if it's not already included in your project.
  
   ```javascript
   import axios from 'axios';

   const options = {
     method: 'GET',
     url: 'https://imdb-top-100-movies.p.rapidapi.com/',
     headers: {
       'x-rapidapi-key': '8d964e6930mshbe793652a519173p14e284jsn8624e6ef0bad',
       'x-rapidapi-host': 'imdb-top-100-movies.p.rapidapi.com'
     }
   };

   try {
     const response = await axios.request(options);
     console.log(response.data);
   } catch (error) {
     console.error(error);
   }
   ```

3. **Understand the API Response:**
   - Review the data structure returned by the API to identify the relevant fields for displaying movie details.

4. **Create the Movie Cards UI:**
   - Design a card component that displays the movie's title, poster, release year, and any other relevant information.
   - Use the UI reference provided *[here](https://drive.google.com/file/d/13jG3w3-Rpa4cv4tPcAp1k97mNxVQcbiK/view?usp=sharing)* to style your cards.
   - Ensure that the cards are responsive and visually appealing.

5. **Display the Movie Data:**
   - Map through the fetched movie data and render a card for each movie on the screen.
