# Monolithic Web Application Starter

This repository contains a starter template for a monolithic web application architecture. The frontend is built with React and Vite, while the backend is built with Flask. The frontend is served as static files by the Flask backend.

## Architecture

This project follows a **Monolithic Architecture** where:

- The frontend and backend are tightly integrated and served from a single server.
- The backend (Flask) serves both the static files for the frontend (React) and provides API endpoints.
- The frontend and backend are developed in different languages but are coupled and deployed together.

### Advantages

1. **Simplified Deployment**: Serving the frontend as static files from the Flask backend simplifies deployment since you only need to deploy one server.
2. **Single Origin**: Avoids CORS issues since both frontend and backend are served from the same origin.
3. **Easier Routing**: Flask can handle both API and frontend routes, making it easier to manage routing.
4. **Unified Codebase**: Easier to manage and maintain a single codebase for both frontend and backend.

### Disadvantages

1. **Tight Coupling**: The frontend and backend are tightly coupled, making it harder to scale or replace one without affecting the other.
2. **Limited Scalability**: Scaling the backend also means scaling the frontend, which might not be efficient.
3. **Build Process**: Requires a build process to generate static files and serve them, which can add complexity.

### Other Common Architectures

1. **Entire App in React**: In this architecture, the entire application is built using React, including both the frontend and backend logic. This can be achieved using frameworks like Next.js, which allows for server-side rendering and API routes within a single React application.

2. **Independent Backend and Frontend Servers**: In this architecture, the frontend and backend are completely independent and communicate over HTTP, typically using libraries like Axios for API requests. The frontend is usually a single-page application (SPA) built with frameworks like React, Angular, or Vue.js, while the backend can be built with any server-side technology (e.g., Flask, Express.js, Django). This separation allows for more flexibility and scalability, as each part can be developed, deployed, and scaled independently.

## Project Structure
```
.
├── backend
│   ├── app.py
│   └── static
├── frontend
│   ├── src
│   │   ├── App.tsx
│   │   └── App.css
│   ├── vite.config.ts
│   └── ...
├── README.md
└── ...
```
## Getting Started

### Prerequisites

- Python
- Node.js
- npm or yarn

### Backend Setup

1. Navigate to the `backend` directory:
   ```sh
   cd backend
   ```
   
2. Install the required Python packages:
   ```sh
   pip install -r requirements.txt
   ```

3. Run the Flask server:
    ```sh
    python app.py
    ```

### Frontend Setup

1. Navigate to the frontend directory:
    ```sh
    cd frontend
    ```

2. Install the required Node.js packages:
    ```sh
    npm install
    ```
    or
    ```sh
    yarn install
    ```

3. Build the frontend:
    ```sh
    npm run build
    ```
    or
    ```sh
    yarn build
    ```

### Running the Application
1. Ensure the Flask server is running.
2. Open your browser and navigate to http://localhost:5000.