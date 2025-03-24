# Syncthreads Assignment 

## Step-by-Step Instructions

### Project Setup and Initialization
1. Create a new React project using Create React App or a similar tool.
2. Navigate to the project directory in the command line.
3. Install the necessary dependencies, including React Router, an open-source mapping library (e.g., Leaflet or OpenLayers), a library for making API requests (e.g., Axios or Fetch), and any styling libraries (e.g., Material UI, Bootstrap, or Styled Components).

### Setup of the Project
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/kavyaa25/Assignment-by-kavya.git
   cd Syncthreads-Assignment-
   ```

2. **Install Dependencies:**
   - Navigate to the React frontend directory and install the dependencies:
     ```bash
     cd frontend
     npm install
     ```
   - Navigate to the Node.js backend directory and install the dependencies:
     ```bash
     cd ../backend
     npm install
     ```

3. **Environment Variables:**
   - Create a `.env` file in the backend directory and add the necessary environment variables, such as database connection strings and JWT secret keys.
   - Example:
     ```plaintext
     PORT=5000
     JWT_SECRET=your_jwt_secret
     MONGO_URI=your_mongo_connection_string
     ```

4. **Run the Backend Server:**
   - Start the backend server:
     ```bash
     npm start
     ```
   - The backend server should be running on the port specified in the `.env` file (default: 5000).

5. **Run the React Frontend:**
   - Navigate to the frontend directory and start the React development server:
     ```bash
     cd ../frontend
     npm start
     ```
   - The React frontend should be running on `http://localhost:3000`.

### Development Process

#### Backend API Development
1. Set up a Node.js backend with Express to handle API requests.
2. Implement the following API endpoints:
   - **Login API:** Create an endpoint (`/api/login`) that accepts user credentials (username and password) and authenticates the user. Implement a robust authentication mechanism (e.g., JWT - JSON Web Tokens).
   - **Dashboard API:** Create an endpoint (`/api/dashboard`) that returns data for the dashboard, including card component information. This endpoint should be protected and only accessible to logged-in users.
   - **Map View API:** Create an endpoint (`/api/map`) that returns necessary data for the map view, such as the initial map center coordinates, zoom level, or other relevant map configurations. This endpoint should also be protected.
3. Implement error handling to return appropriate messages (e.g., "User not logged in") when a user is not authenticated.

#### Authentication Implementation
1. Implement a JWT-based authentication system.
2. Upon successful login, generate a JWT token and send it to the client.
3. Store the JWT token in the client (e.g., using local storage or cookies).
4. Include the JWT token in the headers of subsequent API requests to authenticate the user.
5. On the backend, verify the JWT token on protected routes before processing the request.

#### React Frontend Development
1. Create React components for the following:
   - **Login Page:** Design a user interface for the login page with input fields for username and password, and a submit button.
   - **Dashboard:** Create a dashboard component that displays card components. Each card should have a unique ID.
   - **Map View:** Create a map view component that displays the map of India using the chosen open-source mapping library.
2. Implement routing using React Router to navigate between the login page, dashboard, and map view.
3. Implement the logic for handling user login and storing the JWT token.
4. Implement the logic for making API requests to fetch data for the dashboard and map view.
5. Implement the logic for redirecting the user to the dashboard if they are logged in.
6. Implement the logic for displaying the "User not logged in" message if the user is not authenticated and tries to access the dashboard or map view.
7. Implement the logic for zooming in and zooming out on the map.

### Map Integration
1. Integrate the chosen open-source mapping library (Leaflet or OpenLayers) into the Map View component.
2. Display the map of India.
3. Set the initial zoom level to show a zoomed-out view of India.
4. Implement zoom in and zoom out functionality using the mapping library's API.

### Component Interaction
1. When a card component on the dashboard is clicked, navigate the user to the Map View component.
2. Pass the unique ID of the card component to the Map View component (optional - if the card ID is relevant to the map view).

### Styling and Design
1. Implement the UI design for the login page, dashboard, and map view.
2. Use CSS, a CSS framework (e.g., Material UI, Bootstrap), or a CSS-in-JS library (e.g., Styled Components) to style the components.
3. Ensure the UI is visually appealing, responsive, and user-friendly.
4. Pay attention to UI/UX principles, such as color scheme, typography, and layout.
5. Refer to the Figma portfolio for design inspiration and consistency.

### Deployment
1. Choose a suitable platform for deploying the backend API (e.g., Heroku, AWS, or Google Cloud).
2. Deploy the backend API to the chosen platform.
3. Choose a platform for deploying the React frontend (e.g., Netlify, Vercel, or AWS S3).
4. Configure the React frontend to point to the deployed backend API.
5. Deploy the React frontend to the chosen platform.

### Submission Guidelines
1. Submit the entire project code, including the React frontend and the Node.js backend.
2. Include a `README.md` file with clear instructions on how to set up and run the project.
3. Document all the packages used in the project and explain their purpose.
4. Include the link to your Figma portfolio in the `README.md` file.
5. Ensure the code is well-organized, readable, and follows coding standards.
6. Submit the assignment as a ZIP file or a link to a Git repository.
