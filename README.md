# BloQCat

This service is used for aggregating Quantumcomputing Pattern concrete solutions.

---

This project is based on the [flask-template](https://github.com/buehlefs/flask-template) project. The template documentation can be found in `docs/templatedocumention.md`

---
## Development
1. to install the dependencies run

    ```bash
    poetry install
    ```
1. start the service with
    ```bash
    poetry run flask run
    ```

---

## REST API

### 🌐 Root Endpoints

- `GET /api/v1/`
  - Returns available top-level API routes.
  - **Response example:**
    ```json
    {
      "auth": "/api/v1/auth/",
      "bloqcat": "/api/v1/bloqcat/"
    }
    ```

- `GET /api/v1/auth/`
  - Lists authentication-related endpoints.
  - **Response example:**
    ```json
    {
      "login": "/api/v1/auth/login/",
      "refresh": "/api/v1/auth/refresh/",
      "whoami": "/api/v1/auth/whoami/"
    }
    ```

- `GET /api/v1/bloqcat/`
  - Lists Bloqcat-specific endpoints.
  - **Response example:**
    ```json
    {
      "deploy": "/api/v1/bloqcat/winery/topology/deploy/json"
    }
    ```

---

### 🔐 Authentication Endpoints

- `POST /api/v1/auth/login/`
  - Login with credentials to receive JWT tokens.
  - **Request body:**
    ```json
    {
      "username": "your_user",
      "password": "your_password"
    }
    ```
  - **Response:**
    ```json
    {
      "access_token": "token",
      "refresh_token": "token"
    }
    ```

- `POST /api/v1/auth/refresh/`
  - Uses a refresh token to obtain a new access token.
  - **Headers:** `Authorization: Bearer <refresh_token>`
  - **Response:**
    ```json
    {
      "access_token": "new_access_token"
    }
    ```

- `GET /api/v1/auth/whoami/`
  - Returns the currently authenticated user.
  - **Headers:** `Authorization: Bearer <access_token>`
  - **Response:**
    ```json
    {
      "username": "your_user"
    }
    ```

---

### ⚙️ Bloqcat Endpoint

- `POST /api/v1/bloqcat/winery/topology/deploy/json`
  - Accepts a JSON topology (node and relationship templates), validates it, and returns a `.qasm` file.
  - **Request body:**
    ```json
    {
      "nodeTemplates": [...],
      "relationshipTemplates": [...]
    }
    ```
  - **Response:** `.qasm` file with aggregated content.
  - **Typical use:** Deployment of a quantum pattern topology into a runnable solution.

---

### 🌐 Interactive API Documentation

- Swagger UI : http://localhost:5000/api/swagger-ui – Explore and test API endpoints interactively.
- RapiDoc : http://localhost:5000/api/rapidoc – Alternative interface for API exploration.

> **Note**: Replace `localhost:5000` with your actual host and port if deploying elsewhere.

## Disclaimer of Warranty

Unless required by applicable law or agreed to in writing, Licensor provides the Work (and each Contributor provides its
Contributions) on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied, including,
without limitation, any warranties or conditions of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
PARTICULAR PURPOSE. You are solely responsible for determining the appropriateness of using or redistributing the Work
and assume any risks associated with Your exercise of permissions under this License.

## Haftungsausschluss

Dies ist ein Forschungsprototyp. Die Haftung für entgangenen Gewinn, Produktionsausfall, Betriebsunterbrechung,
entgangene Nutzungen, Verlust von Daten und Informationen, Finanzierungsaufwendungen sowie sonstige Vermögens- und
Folgeschäden ist, außer in Fällen von grober Fahrlässigkeit, Vorsatz und Personenschäden, ausgeschlossen.

## Acknowledgements

The initial code contribution has been supported by the
project [SeQuenC](https://www.iaas.uni-stuttgart.de/forschung/projekte/sequenc/).

