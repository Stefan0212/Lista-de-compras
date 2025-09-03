# Lista de Compras

[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/Stefan0212/Lista-de-compras.git)

This is a full-stack web application for creating and managing a simple shopping list. The project is separated into a frontend client and a backend server, providing a complete solution for basic CRUD (Create, Read, Update, Delete) operations on shopping items.

## Features

-   **Add Items:** Add new products with a name and price to your list.
-   **View List:** See all the current items in your shopping list, sorted by creation date.
-   **Edit Items:** Modify the name and price of an existing item directly in the UI.
-   **Delete Items:** Remove items you no longer need.
-   **Responsive UI:** A clean and responsive user interface built with Tailwind CSS that works on both desktop and mobile devices.

## Tech Stack

-   **Frontend:**
    -   HTML
    -   Tailwind CSS (via CDN)
    -   Vanilla JavaScript (ES6+)
-   **Backend:**
    -   Node.js
    -   Express.js
    -   TypeScript
-   **Database:**
    -   MongoDB
    -   Mongoose ODM

## Project Structure

```
.
├── backend/        # Contains the Node.js/Express backend
│   ├── src/
│   │   ├── controllers/ # Business logic for API routes (controlador.ts)
│   │   ├── models/      # Mongoose data models (modelo.ts)
│   │   ├── routes/      # API route definitions (shopping.ts)
│   │   └── server.ts    # Server entry point and DB connection
│   ├── package.json
│   └── tsconfig.json
└── frontend/       # Contains the client-side application
    └── index.html  # Main HTML file with all frontend logic and styling
```

## Getting Started

### Prerequisites

-   [Node.js](https://nodejs.org/) (version 16 or later recommended)
-   npm (or yarn)
-   [MongoDB](https://www.mongodb.com/try/download/community) installed and running locally.

### Backend Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/stefan0212/Lista-de-compras.git
    cd Lista-de-compras
    ```

2.  **Navigate to the backend directory:**
    ```sh
    cd lista_de_compras/backend
    ```

3.  **Install dependencies:**
    ```sh
    npm install
    ```

4.  **Start the server:**
    The server will attempt to connect to a local MongoDB instance at `mongodb://127.0.0.1:27017/shopping-list`. Ensure your MongoDB service is running before starting the server.
    ```sh
    npm start
    ```
    The backend will be running on `http://localhost:5000`.

### Frontend Usage

1.  Once the backend server is running, open the `frontend/index.html` file in your preferred web browser.

    For example, you can right-click the file in your file explorer and choose "Open with" your favorite browser.

2.  The application is now ready to use. You can start adding, editing, and deleting items from your shopping list.

## API Endpoints

All endpoints are prefixed with `/api/shopping`. The backend server runs on `http://localhost:5000`.

| Method | Endpoint | Description | Request Body Example |
| :--- | :--- | :--- | :--- |
| `GET` | `/` | Fetches all shopping items. | N/A |
| `POST` | `/` | Adds a new shopping item. | `{ "name": "Leite", "price": 5.99 }` |
| `PUT` | `/:id` | Updates an existing item. | `{ "name": "Leite Integral", "price": 6.50 }` |
| `DELETE` | `/:id` | Deletes an item by its ID. | N/A |
