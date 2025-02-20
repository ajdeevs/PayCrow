# PayCrow - Web-Based Payments App

PayCrow is a modern, web-based payments application built with a focus on speed, reliability, and developer experience. It utilizes a monorepo architecture powered by Turborepo, leveraging Next.js for the frontend, Node.js and Express for auxiliary backends, Tailwind CSS for styling, and Redis for data caching and session management.

## Architecture
![Screenshot_20241102_203603](https://github.com/user-attachments/assets/64aea4d2-02e5-44b0-bdfe-e58e30e45cf8)



* **Frontend (Next.js):** The user-facing application, built with React and Next.js, provides a seamless and responsive user experience.
* **Backend (Node.js/Express):** Auxiliary backend services that handle specific functionalities, such as API integrations, data processing, or background tasks.
* **Turborepo:** Manages the monorepo, enabling efficient code sharing and dependency management across the frontend and backend services.
* **Tailwind CSS:** Provides a utility-first CSS framework for rapid and consistent styling.
* **Redis:** Used for caching frequently accessed data and managing user sessions, improving application performance.

## Technologies Used

* **Frontend:**
    * Next.js
    * React
    * Tailwind CSS
* **Backend:**
    * Node.js
    * Express.js
* **Monorepo:**
    * Turborepo
* **Data/Caching:**
    * Redis

## Getting Started

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/ajdeevs/PayCrow
    cd paycrow
    ```

2.  **Install dependencies:**

    ```bash
    npm install
    ```

3.  **Configure environment variables:**

    * Create `.env.local` files in the root and within each `apps/*` folder that requires them.
    * Define the necessary environment variables (e.g., API keys, database connection strings, Redis configuration). Example:

    ```
    # .env.local (root)
    REDIS_URL=redis://127.0.0.1:6379
    ```

    ```
    # .env.local (apps/web)
    NEXT_PUBLIC_API_URL=http://localhost:3001/api
    ```

    ```
    # .env.local (apps/api)
    PORT=3001
    ```

4.  **Start the development servers:**

    ```bash
    npm run dev
    ```

    This command will start the development servers for all applications in the monorepo concurrently.

5.  **Access the application:**

    * The Next.js frontend will be available at `http://localhost:3000`.
    * The Express backend(s) will be available at their respective ports (e.g., `http://localhost:3001`).
