# Strapi Local Project

A local-only Strapi application configured for development with SQLite. This project is optimized for a lightweight and fast local development experience.

##  Getting Started

Follow these instructions to get the project up and running on your local machine.

### Prerequisites

Ensure you have the following installed:

*   **Node.js**: `v20.0.0` or higher (Supported: `v20.x`, `v22.x`, `v24.x`).
    *   *Note: Current configuration also supports `v25.x`.*
*   **npm**: `v6.0.0` or higher.

###  Installation 

1.  **Clone the repository** (if you haven't already):
    ```bash
    git clone <your-repo-url>
    cd my-project
    ```

2.  **Install dependencies**:
    ```bash
    npm install
    ```

###  Assignment Steps Completed

1.  **Repository Setup**: Project initialized and pushed to GitHub.
2.  **Folder Structure**: Explored standard Strapi structure (`src`, `config`, `.env`).
3.  **Content Type**: Created `Article` content type (see `src/api/article`).
4.  **Admin Panel**: Verified access at `http://localhost:1337/admin`.
5.  **Documentation**: This README documents all steps.

###  Configuration

The application uses a `.env` file for configuration. A basic setup is already provided.

**Database**: SQLite (Local file at `.tmp/data.db`)

**Key Environment Variables** (`.env`):
```bash
HOST=0.0.0.0
PORT=1337
APP_KEYS=...
API_TOKEN_SALT=...
ADMIN_JWT_SECRET=...
TRANSFER_TOKEN_SALT=...
DATABASE_CLIENT=sqlite
DATABASE_FILENAME=.tmp/data.db
JWT_SECRET=...
```



---

##  Running the Application

### Development Server
Start the server in development mode with auto-reload enabled:

```bash
npm run dev
```

Once started, the application will be accessible at:
*   **Admin Panel**: [http://localhost:1337/admin](http://localhost:1337/admin)
*   **API**: [http://localhost:1337/api](http://localhost:1337/api)

### Production Build
To build the admin panel for production:

```bash
npm run build
```

To start the production server:

```bash
npm run start
```

---

##  Project Structure

*   `src/api` - Your API definitions (Content Types, Controllers, Services).
*   `src/admin` - Admin panel customization.
*   `config/` - Configuration files (Database, Server, etc.).
*   `.tmp/` - Contains the local SQLite database (`data.db`).
*   `public/` - Static assets.

##  Troubleshooting

**"Unsupported engine" error**:
If you see warnings about Node.js versions, ensure you are using a compatible version (e.g., `v20` LTS). We have relaxed strict engine checks in `package.json` to allow newer versions, but LTS is recommended for stability.

**"Build failed"**:
If the admin panel fails to build, try cleaning the cache:
```bash
rm -rf .strapi dist .cache
npm run build
```

---

*Built with [Strapi](https://strapi.io) v5.34.0*
